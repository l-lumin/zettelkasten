While both MySQL (InnoDB) and PostgreSQL use B-Tree as their default index type, their underlying storage mechanisms differ  significantly.
- **MySQL (Clustered Index):** MySQL stores the actual table data inside the primary key's B-Tree. Secondary indexes do not point directly to the data; instead, they store the primry key value. Therefore, querying a secondary index requires a two-step lookup: searching the secondary B-Tree to get the primary key (ID), and then searching the primary B-Tree to fetch the actual record.
- **PostgreSQL (Heap Storage):** PostgreSQL stores the table records (tuples) in an unordered structure called a heap. All indexes, including the primary key index, store a direct pointer (CTID, representing the block and offset) to the physical location of the row in the heap. A query using an index returns this physical location directly.

**The Impact of these Mechanics:**
Because of these different mechanics, they affect database performance in different ways.
- In MySQL, secondary indexes are smaller, but looking up data through them take slightly longer due to the double B-Tree traversal.
- In PostgreSQL, index lookups are faster because they point directly to the data. However, if a row is updated and changes its physical location in the heap, every single index pointing to that row must also be updated.