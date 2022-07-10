# Iterables

객체가 Symbol.iterator프로퍼티에 대한 구현을 가지고 있다면 이터러블로 간주한다. Array, Map, Set, String, Int32Array, Uint32Array 등과 같은 일부 내장 타입에는 이미 Symbol.iterator 프로퍼티가 구현되어 있다. 객체의 Symbol.iterator 함수는 반복할 값 목록을 반환한다.

## for..of 문
```jsx
let someArray = [1, "string", false];

for (let entry of someArray)
 console.log(entry); // 1, "string", false
}
```

## for..of vs. for..in 문
for..of 및 for..in 문 모두 목록을 반복합니다; 반복되는 값은 다르지만, for..in은 반복되는 객체의 키 목록을 반환하고, 반면에 for..of는 반복되는 객체의 숫자 프로퍼티 값 목록을 반환합니다.

```jsx
let list = [4, 5, 6];

for (let i in list){
 console.log(i); // "0", "1", "2"
}

for (let i of list){
 console.log(i); // "4", "5", "6"
}
```
