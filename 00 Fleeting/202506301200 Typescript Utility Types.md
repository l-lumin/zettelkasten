# Typescript Utility Types

## `Pick<Type, Keys>`
Constructs a type be picking the set of properties `Keys` (string literal or union of string literals) from `Type`

```ts
interface Todo {
	title: string;
	description: string;
	completed: boolean;
}

type TodoPreview = Pick<Todo, "title" | "completed">

const todo: TodoPreview = {
	title: "Clean room",
	completed: false,
};

todo;
```
