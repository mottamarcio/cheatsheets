## TYPESCRIPT

**Basic Types:**

| Type | Description | Example |
|---|---|---|
| `number` | Numeric values | `let age: number = 30;` |
| `string` | Textual data | `let name: string = "John Doe";` |
| `boolean` | True or False values | `let isAdult: boolean = true;` |
| `any` | Any type (use sparingly) | `let something: any = "hello";` |
| `void` | No type, often used for function return types | `function log(message: string): void { ... }` |
| `null` | Intentional absence of a value | `let value: null = null;` |
| `undefined` | Uninitialized variable | `let value: undefined;` |

**Arrays & Tuples:**

| Type | Description | Example |
|---|---|---|
| `Array<T>` or `T[]` | Array of type `T` | `let numbers: number[] = [1, 2, 3];` |
| `[T, U]` | Tuple with fixed types | `let person: [string, number] = ["John", 30];` |

**Objects & Interfaces:**

```typescript
// Object type
let user: { name: string, age: number } = { name: "John", age: 30 };

// Interface
interface User {
  name: string;
  age: number;
}
let user: User = { name: "John", age: 30 };
```

**Functions:**

```typescript
function add(x: number, y: number): number {
  return x + y;
}
```

**Classes:**

```typescript
class Dog {
  name: string;

  constructor(name: string) {
    this.name = name;
  }

  bark(): void {
    console.log("Woof!");
  }
}
```

**Generics:**

```typescript
function identity<T>(value: T): T {
  return value;
}
```

**Enums:**

```typescript
enum Direction {
  Up,
  Down,
  Left,
  Right,
}
```

**Type Assertions:**

```typescript
let someValue: any = "this is a string";
let strLength: number = (someValue as string).length;
```

**Advanced Types:**

| Type | Description | Example |
|---|---|---|
| `Union` | Allows a variable to hold values of different types | `let id: string | number = 123;` |
| `Intersection` | Combines multiple types into one | `type Admin = User & { isAdmin: true };` |
| `Literal Types` | Allows only specific values | `let status: "success" | "error" = "success";` |
| `Conditional Types` | Types that depend on a condition | `T extends U ? X : Y` |
| `Mapped Types` | Create new types based on existing ones | `type Readonly<T> = { readonly [P in keyof T]: T[P] };` |
| `Index Signatures` | Define types for object properties with unknown keys | `interface StringArray { [index: number]: string; }` |

**Tips and Tricks:**

  * Use type inference whenever possible.
  * Use interfaces to define the shape of objects.
  * Use generics to write reusable code.
  * Use strict mode for better type checking.
  * Leverage linters like ESLint with TypeScript plugins for code quality.

**Resources:**

  * **Official TypeScript website:** [www.typescriptlang.org](www.typescriptlang.org)
  * **TypeScript Handbook:** [www.typescriptlang.org/docs/handbook/intro.html](https://www.google.com/url?sa=E&source=gmail&q=www.typescriptlang.org/docs/handbook/intro.html)
  * **TypeScript Playground:** [www.typescriptlang.org/play](https://www.google.com/url?sa=E&source=gmail&q=www.typescriptlang.org/play)
  * **DefinitelyTyped:** [definitelytyped.org](https://www.google.com/url?sa=E&source=gmail&q=definitelytyped.org)