Purpose: 
- easy to understand
- easy to enhance and extend
- protected from anomalies (insertion, update, deletion)

Kind of Normalization Form

First Normal Form (1NF)
- row order cannot convey information
- mix data types in a column not allowed
- a table without a primary key is not allowed
- no repeating groups

Second Normal Form (2NF)
Every non-key attribute must depend on the entire primary key

Third Normal Form (3NF)
No transitive dependencies - non-key attributes must depend directly on the primary key, not on other non-key attributes

Four Normal Form (4NF)
No multivalued dependencies except on the key itself

Fifth Normal Form (5NF)
Cannot be decomposed into smaller tables without loss of information