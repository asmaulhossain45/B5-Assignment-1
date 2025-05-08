## Differences between any, unknown and never types in typescript

### any type

In typescript, we use any type when we're not sure what type will be the variable or function.The any type disable all type checking of TypeScript and behave like Javascript. So when we decalare any type on a variable or function then we can do anything without typescript type checking. We can declare or return string, number, boolean, etc. using any type.

```
let example: any;
example = "hello";
example = 1;
example = true;
```

### unknown type

Unknown type is better than any type. Because unknown type doesnt disable type checking, but it force to check the type before using the value. Using uknown we can set any type of value but we need to check and verify the type before doing something.

```
let value: unknown = "hello";
if (typeof value === "string") {
  console.log(value.toUpperCase());
}
```

### never type

The never type in TypeScript is use for value that will never happen. It use those functions that don’t return anything, like a function that always throw an error or run forever. When a function is never type, it means it will never finish or return a value.

```
function throwError(message: string): never {
  throw new Error(message);
}
```

## Example of using union and intersection types in TypeScript.

### Union Types

The union type let us to declare more than single type of value. Then we can use the varibale value either one type or another. We use | symbol for accept multiple type and its work like "or". So if we are not sure what type of value will be then we can accept or allow multiple type using union type.

```
let value: string | number;

value = "Hello";
value = 32614;

```

### Intersection Types

The intersection type give us the power to combine multiple types into a single type.  When we use intersection, the variable must have all the properties from each type. We use the & symbol for intersection, and it works like "and".

```
interface Boy {
  name: string;
}

interface Student {
  education: string;
}

let example: Boy & Student = {
  name: "Alif",
  education: "HSC",
};


```
