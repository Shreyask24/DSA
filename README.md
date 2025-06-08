# 🔁 Loops in JavaScript - Practice Examples

---

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


# 🔁 Loop in loop in JavaScript - Practice Examples
![image](https://github.com/user-attachments/assets/2d39139d-cf94-43e3-aac2-2d116c38e98c)

```js
let n = 4
for (let i = 0; i < n; i++) {
    let row = ""
    for (let j = 0; j < n; j++) {
        row = row + " * "
    }
    console.log(row)
}
```

![image](https://github.com/user-attachments/assets/2a49a88c-a460-4173-94bf-44de0a05e7c1)
```js
let n = 4
for (let i = 0; i < n; i++) {
    let row = ""

    for (let j = 0; j <= i; j++) {
        row = row + " * "
    }
    console.log(row)
}
```

![image](https://github.com/user-attachments/assets/2c059d5b-cb47-43b0-bdcf-b14293c578ca)
```js
let n = 4
for (let i = 0; i < n; i++) {
    let row = ""

    for (let j = 0; j <= i; j++) {
        row = row + " " + (j + 1)
    }
    console.log(row)
}
```

![image](https://github.com/user-attachments/assets/83e36ff3-21b5-4e8f-b21c-f49334ab5294)
```js
let n = 4
for (let i = 0; i < n; i++) {
    let row = ""
    for (let j = 0; j <= i; j++) {
        row = row + " " + (i + 1)
    }
    console.log(row)
}
```

![image](https://github.com/user-attachments/assets/bfceb543-face-4c6e-b6a8-8055e8e634f7)
```js
let n = 4
for (let i = 0; i < n; i++) {
    let row = ""
    for (let j = 0; j < n - i; j++) {
        row = row + " " + (j + 1)
    }
    console.log(row)
}
```

![image](https://github.com/user-attachments/assets/7d25780c-ac45-49fe-a0f8-ff8886be3994)
``` js
let n = 4
for (let i = 0; i < n; i++) {
    let row = ""
    for (let j = 0; j < n - i; j++) {
        row = row + " * "
    }
    console.log(row)
}
```

![image](https://github.com/user-attachments/assets/8c47e1d6-4094-442e-b37d-12763fe97d63)
``` js
let n = 4
for (let i = 0; i < n; i++) {
    let row = ""

    //adding empty spaces
    for (let j = 0; j < n - (i + 1); j++) {
        row = row + " - "
    }

    // adding stars
    for (let k = 0; k < i + 1; k++) {
        row = row + " * "
    }
    console.log(row)
}
```

![image](https://github.com/user-attachments/assets/b9998b3c-121d-48c4-835e-5eb2390eaca2)
```js
let n = 4
for (let i = 0; i < n; i++) {
    let row = "";
    let toggle = 1

    //adding empty spaces
    for (let j = 0; j < i + 1; j++) {
        row = row + " " + toggle
        if (toggle === 1) {
            toggle = 0
        }
        else {
            toggle = 1
        }

    }

    console.log(row)
}
```

![image](https://github.com/user-attachments/assets/1d2f1c8b-e851-43c0-afd2-effb593fca89)
```js
let toggle = 1
for (let i = 0; i < n; i++) {
    let row = "";

    //adding empty spaces
    for (let j = 0; j < i + 1; j++) {
        row = row + " " + toggle
        if (toggle === 1) {
            toggle = 0
        }
        else {
            toggle = 1
        }

    }

    console.log(row)
}
```


