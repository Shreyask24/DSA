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

Write a function that returns the count of digits in a number
```js
function countDigits(n) {
    // handling 0
    if (n == 0) return 1;

    // handling negative numbers
    n = Math.abs(n)

    let count = 0
    while (n > 0) {
        n = Math.floor(n / 10)
        count++
    }
    return count
}

let n = -41654

console.log(countDigits(n))
```


Anagram
```js
function areAnagrams(s1, s2) {
    // code here
    if (s1.length !== s2.length) return false;

    let freq = {};

    for (let i = 0; i < s1.length; i++) {
        let ch = s1[i];
        if (freq[ch] === undefined) {
            freq[ch] = 1;
        } else {
            freq[ch]++;
        }
    }

    for (let j = 0; j < s2.length; j++) {
        let ch = s2[j];
        if (freq[ch] === undefined || freq[ch] === 0) {
            return false;
        } else {
            freq[ch]--;
        }
    }

    return true;
}

console.log(areAnagrams("shreyas", "sayerhs"))
```

Find the majority element in the array. If no majority element exists, return -1.
```js
function majorityElement(arr) {
    // code here
    let n = arr.length;
    let freq = {};  // frequency map

    for (let i = 0; i < arr.length; i++) {
        let num = arr[i];

        // If not seen before, initialize count
        if (freq[num] === undefined) {
            freq[num] = 1;
        } else {
            freq[num]++;
        }

        // Check if it crossed majority threshold
        if (freq[num] > Math.floor(n / 2)) {
            return num;
        }
    }

    return -1;  // No majority element found
}

let arr = [3, 1, 3, 3, 2]
console.log(majorityElement(arr))
```

Given a string s, convert the first letter of each word in the string to uppercase. 
```js
function upperCaseConversion(s) {
    let result = ""

    for (let i = 0; i < s.length; i++) {
        if (i === 0 || s[i - 1] === ' ') {
            result += s[i].toUpperCase()
        } else {
            result += s[i]
        }
    }
    return result
}

console.log(upperCaseConversion("shreyas kallurkar"))
```

Given an array, arr[]. Sort the array using Bubble Sort Algorithm.
```js
function bubbleSort(arr) {
    let n = arr.length;

    for (let i = 0; i < n - 1; i++) {
        // Loop to compare adjacent elements
        for (let j = 0; j < n - i - 1; j++) {
            if (arr[j] > arr[j + 1]) {
                // Swap if elements are out of order
                let temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
            }
        }
    }

    return arr;
}

console.log(bubbleSort([4, 1, 3, 9, 7]))
```

# Linked List

Middle of Linked List: Given the head of a linked list, the task is to find the middle
```js
function getMiddle(node) {
    if (!node) return -1;

    let slow = node;
    let fast = node;

    while (fast !== null && fast.next !== null) {
        slow = slow.next;
        fast = fast.next.next;
    }

    return slow.data;

}
```
