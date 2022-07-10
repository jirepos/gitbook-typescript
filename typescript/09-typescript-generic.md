# Generidc

## Generic Class 
```jsx
class Stack<T> {
  private data: T[] = [];

  constructor() {}

  push(item: T): void {
    this.data.push(item);
  }

  pop(): T {
    return this.data.pop();
  }
}
```

```jsx

const numberStack = new Stack<number>();
const stringStack = new Stack<string>();
numberStack.push(1);
stringStack.push('a');

console.log(numberStack.pop());
console.log(stringStack.pop());
```





## Generic Function

```jsx

function first<T>(arr: T[]): T {
  return arr[0];
}
```


```jsx
let rv = first<number>([1, 2, 3]); // 1
console.log(rv);

```