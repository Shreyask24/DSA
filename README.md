# 🔁 Loops in JavaScript - Practice Examples

---

## 🔍 Search Element in Array

Searches for a given number in the array and returns its index if found, otherwise returns `-1`.

```js
let arr = [4, 2, -80, -57, 0, 10, 30, 50, 50, 0, -5, -6, -3, -20]

function searchIndex(num) {
    for (let i = 0; i < arr.length; i++) {
        if (num === arr[i]) {
            return i;
        }
    }
    return -1;
}

console.log(searchIndex(2));
```

Find All Negative Numbers

```js
let arr = [4, 2, -80, -57, 0, 10, 30, 50, 50, 0, -5, -6, -3, -20]

function searchNegativeNum(arr) {
    let newArr = [];
    for (let i = 0; i < arr.length; i++) {
        if (arr[i] < 0) {
            newArr.push(arr[i]);
        }
    }
    return newArr;
}

console.log(searchNegativeNum(arr));
```

Find the Largest Element

```js
let arr = [4, 2, -80, -57, 0, 10, 30, 50, 50, 0, -5, -6, -3, -20]

function largestNum(arr) {
    let max = -Infinity;
    for (let i = 0; i < arr.length; i++) {
        if (arr[i] > max) {
            max = arr[i];
        }
    }
    return max;
}

console.log(largestNum(arr));
```

Find the Second Largest Element

```js
let arr = [4, 2, -80, -57, 0, 10, 30, 50, 50, 0, -5, -6, -3, -20]

function secondLargest(arr) {
    let first_Largest = -Infinity;
    let second_Largest = -Infinity;

    for (let i = 0; i < arr.length; i++) {
        if (arr[i] > first_Largest) {
            second_Largest = first_Largest;
            first_Largest = arr[i];
        } else if (arr[i] > second_Largest && arr[i] != first_Largest) {
            second_Largest = arr[i];
        }
    }

    return second_Largest;
}

console.log(secondLargest(arr));
```
