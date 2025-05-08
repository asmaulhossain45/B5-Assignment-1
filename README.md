## Differences between any, unknown and never types in typescript

### any types

In typescript, we use any type when we're not sure what type will be the variable or function.The any type disable all type checking of TypeScript and behave like Javascript. So when we decalare any type on a variable or function then we can do anything without typescript type checking. We can declare or return string, number, boolean, etc. using any type.

```
let example: any;
example = "hello";
example = 1;
example = true;
```