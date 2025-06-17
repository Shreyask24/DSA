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

Palindrome

```js
function palindrome(num) {
    if (num < 0) return false

    let numCopy = num
    let rev = 0

    while (num > 0) {
        let rem = num % 10
        rev = (10 * rev) + rem
        num = Math.floor(num / 10)
    }

    return rev === numCopy
}

console.log(palindrome(121))
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

# Spirally traversing a matrix

You are given a rectangular matrix mat[][] of size n x m, and your task is to return an array while traversing the matrix in spiral form.

```js
function spirallyTraverse(mat) {
    const n = mat.length;
    const m = mat[0].length;

    const result = [];

    let top = 0, bottom = n - 1;
    let left = 0, right = m - 1;

    while (top <= bottom && left <= right) {
        // Traverse top row (left to right)
        for (let i = left; i <= right; i++) {
            result.push(mat[top][i]);
        }
        top++;

        // Traverse right column (top to bottom)
        for (let i = top; i <= bottom; i++) {
            result.push(mat[i][right]);
        }
        right--;

        // Traverse bottom row (right to left)
        if (top <= bottom) {
            for (let i = right; i >= left; i--) {
                result.push(mat[bottom][i]);
            }
            bottom--;
        }

        // Traverse left column (bottom to top)
        if (left <= right) {
            for (let i = bottom; i >= top; i--) {
                result.push(mat[i][left]);
            }
            left++;
        }
    }

    return result;
}
```

# Given an array of integers values and an integer k, perform the following operations:

- Find the k smallest numbers from the array.
- Find the k largest numbers from the array.
- Compute the median of the k smallest numbers.
- Compute the median of the k largest numbers.
- If k is odd, take the middle value.
- If k is even, take the lower median (i.e., the left one of the two middle values).

- Return an array where:
- The first element is the median of the k largest numbers
- The second element is the median of the k smallest numbers

```js
function medians(values, k) {
    values.sort((a, b) => a - b); // sort ascending

    // Pick k smallest → minMedian
    const smallestK = values.slice(0, k);
    const minMedian = getMedian(smallestK, k);

    // Pick k largest → maxMedian
    const largestK = values.slice(values.length - k);
    const maxMedian = getMedian(largestK, k);

    return [maxMedian, minMedian];
}

// Helper to return median from a sorted array
function getMedian(arr, k) {
    if (k % 2 === 1) {
        return arr[Math.floor(k / 2)];
    } else {
        return arr[Math.floor(k / 2) - 1]; // as per problem, use lower median
    }
}


console.log(medians([1, 2, 3, 5, 8, 6], 4))
```
