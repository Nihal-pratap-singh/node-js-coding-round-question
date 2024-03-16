 Here are 50 Node.js machine coding round questions with answers:

**1. Write a function to reverse a string in Node.js.**
```javascript
function reverseString(str) {
  return str.split('').reverse().join('');
}
```

**2. Implement a function to find the factorial of a number in Node.js.**
```javascript
function factorial(n) {
  if (n === 0 || n === 1) return 1;
  return n * factorial(n - 1);
}
```

**3. Create a function to check if a given number is prime or not in Node.js.**
```javascript
function isPrime(num) {
  if (num <= 1) return false;
  if (num <= 3) return true;
  if (num % 2 === 0 || num % 3 === 0) return false;
  let i = 5;
  while (i * i <= num) {
    if (num % i === 0 || num % (i + 2) === 0) return false;
    i += 6;
  }
  return true;
}
```

**4. Write a function to sort an array of numbers in ascending order in Node.js.**
```javascript
function sortArray(arr) {
  return arr.sort((a, b) => a - b);
}
```

**5. Implement a function to find the sum of all elements in an array in Node.js.**
```javascript
function sumArray(arr) {
  return arr.reduce((acc, curr) => acc + curr, 0);
}
```

**6. Create a function to check if a string is a palindrome in Node.js.**
```javascript
function isPalindrome(str) {
  const cleanStr = str.toLowerCase().replace(/[\W_]/g, '');
  return cleanStr === cleanStr.split('').reverse().join('');
}
```

**7. Write a function to convert a temperature from Celsius to Fahrenheit in Node.js.**
```javascript
function celsiusToFahrenheit(celsius) {
  return (celsius * 9 / 5) + 32;
}
```

**8. Implement a function to remove duplicates from an array in Node.js.**
```javascript
function removeDuplicates(arr) {
  return [...new Set(arr)];
}
```

**9. Create a function to find the maximum element in an array in Node.js.**
```javascript
function maxArrayElement(arr) {
  return Math.max(...arr);
}
```

**10. Write a function to capitalize the first letter of each word in a sentence in Node.js.**
```javascript
function capitalizeSentence(sentence) {
  return sentence.replace(/\b\w/g, char => char.toUpperCase());
}
```

**11. Implement a function to check if two strings are anagrams in Node.js.**
```javascript
function areAnagrams(str1, str2) {
  const cleanStr1 = str1.toLowerCase().replace(/[\W_]/g, '');
  const cleanStr2 = str2.toLowerCase().replace(/[\W_]/g, '');
  return cleanStr1.split('').sort().join('') === cleanStr2.split('').sort().join('');
}
```

**12. Create a function to generate a random number within a specified range in Node.js.**
```javascript
function getRandomNumber(min, max) {
  return Math.floor(Math.random() * (max - min + 1)) + min;
}
```

**13. Write a function to find the intersection of two arrays in Node.js.**
```javascript
function arrayIntersection(arr1, arr2) {
  return arr1.filter(value => arr2.includes(value));
}
```

**14. Implement a function to check if a given year is a leap year in Node.js.**
```javascript
function isLeapYear(year) {
  return (year % 4 === 0 && year % 100 !== 0) || (year % 400 === 0);
}
```

**15. Create a function to count the number of vowels in a string in Node.js.**
```javascript
function countVowels(str) {
  const vowels = 'aeiouAEIOU';
  return str.split('').filter(char => vowels.includes(char)).length;
}
```

**16. Write a function to flatten a nested array in Node.js.**
```javascript
function flattenArray(arr) {
  return arr.reduce((acc, val) => Array.isArray(val) ? acc.concat(flattenArray(val)) : acc.concat(val), []);
}
```

**17. Implement a function to rotate elements of an array to the left by a given number of positions in Node.js.**
```javascript
function rotateLeft(arr, positions) {
  return arr.slice(positions).concat(arr.slice(0, positions));
}
```

**18. Create a function to find the longest word in a sentence in Node.js.**
```javascript
function longestWord(sentence) {
  const words = sentence.split(' ');
  return words.reduce((longest, current) => current.length > longest.length ? current : longest, '');
}
```

**19. Write a function to convert a number to its Roman numeral equivalent in Node.js.**
```javascript
function toRoman(num) {
  const romanNumeralMap = [
    { value: 1000, symbol: 'M' },
    { value: 900, symbol: 'CM' },
    // Add other numerals here
  ];

  let result = '';
  for (const item of romanNumeralMap) {
    while (num >= item.value) {
      result += item.symbol;
      num -= item.value;
    }
  }
  return result;
}
```

**20. Implement a function to find the second largest element in an array in Node.js.**
```javascript
function secondLargest(arr) {
  const sortedArr = arr.sort((a, b) => b - a);
  return sortedArr[1];
}
```

**21. Create a function to find the median of an array of numbers in Node.js.**
```javascript
function median(arr) {
  const sortedArr = arr.sort((a, b) => a - b);
  const mid = Math.floor(sortedArr.length / 2);
  return sortedArr.length % 2 !== 0 ? sortedArr[mid] : (sortedArr[mid - 1] + sortedArr[mid]) / 2;
}
```

**22. Write a function to check if a given string contains only digits in Node.js.**
```javascript
function containsOnlyDigits(str) {
  return /^\d+$/.test(str);
}
```

**23. Implement a function to generate a Fibonacci sequence up to a given number of terms in Node.js.**
```javascript
function fibonacci(n) {
  const sequence = [0, 1];
  for (let i = 2; i < n; i++) {
    sequence.push(sequence[i - 1] + sequence[i - 2]);
  }
  return sequence;
}
```

**24. Create a function to convert a binary number to its decimal equivalent in Node.js.**
```javascript
function binaryToDecimal(binary) {
  return parseInt(binary, 2);
}
```

**25. Write a function to generate all permutations of a given string in Node.js.**
```javascript
function permutations(str) {
  if (str.length === 1) return

 [str];
  const perms = [];
  for (let i = 0; i < str.length; i++) {
    const char = str[i];
    const remainingChars = str.slice(0, i) + str.slice(i + 1);
    const innerPerms = permutations(remainingChars);
    for (let perm of innerPerms) {
      perms.push(char + perm);
    }
  }
  return perms;
}
```

**26. Implement a function to reverse the words in a sentence in Node.js.**
```javascript
function reverseWords(sentence) {
  return sentence.split(' ').reverse().join(' ');
}
```

**27. Create a function to find the power of a number in Node.js.**
```javascript
function power(base, exponent) {
  return Math.pow(base, exponent);
}
```

**28. Write a function to convert a decimal number to its binary equivalent in Node.js.**
```javascript
function decimalToBinary(decimal) {
  return decimal.toString(2);
}
```

**29. Implement a function to calculate the area of a circle in Node.js.**
```javascript
function circleArea(radius) {
  return Math.PI * Math.pow(radius, 2);
}
```

**30. Create a function to remove a specific element from an array in Node.js.**
```javascript
function removeElement(arr, element) {
  return arr.filter(item => item !== element);
}
```

**31. Write a function to check if a string contains a substring in Node.js.**
```javascript
function containsSubstring(str, substring) {
  return str.includes(substring);
}
```

**32. Implement a function to reverse the order of words in a sentence without using built-in functions in Node.js.**
```javascript
function reverseWords(sentence) {
  let reversed = '';
  let word = '';
  for (let i = 0; i < sentence.length; i++) {
    if (sentence[i] === ' ') {
      reversed = word + ' ' + reversed;
      word = '';
    } else {
      word += sentence[i];
    }
  }
  reversed = word + ' ' + reversed;
  return reversed.trim();
}
```

**33. Create a function to calculate the sum of squares of numbers in an array in Node.js.**
```javascript
function sumOfSquares(arr) {
  return arr.reduce((sum, num) => sum + Math.pow(num, 2), 0);
}
```

**34. Write a function to find the greatest common divisor (GCD) of two numbers in Node.js.**
```javascript
function gcd(a, b) {
  if (!b) return a;
  return gcd(b, a % b);
}
```

**35. Implement a function to check if a number is a perfect square in Node.js.**
```javascript
function isPerfectSquare(num) {
  return Math.sqrt(num) % 1 === 0;
}
```

**36. Create a function to reverse the order of elements in an array in Node.js.**
```javascript
function reverseArray(arr) {
  return arr.reverse();
}
```

**37. Write a function to find the mode (most frequent element) in an array in Node.js.**
```javascript
function mode(arr) {
  const frequencyMap = {};
  let maxFrequency = 0;
  let mode;
  arr.forEach(item => {
    frequencyMap[item] = (frequencyMap[item] || 0) + 1;
    if (frequencyMap[item] > maxFrequency) {
      maxFrequency = frequencyMap[item];
      mode = item;
    }
  });
  return mode;
}
```

**38. Implement a function to shuffle elements of an array randomly in Node.js.**
```javascript
function shuffleArray(arr) {
  for (let i = arr.length - 1; i > 0; i--) {
    const j = Math.floor(Math.random() * (i + 1));
    [arr[i], arr[j]] = [arr[j], arr[i]];
  }
  return arr;
}
```

**39. Create a function to check if a string is a valid email address in Node.js.**
```javascript
function isValidEmail(email) {
  const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
  return emailRegex.test(email);
}
```

**40. Write a function to find the sum of all prime numbers up to a given number in Node.js.**
```javascript
function sumOfPrimes(limit) {
  let sum = 0;
  for (let i = 2; i <= limit; i++) {
    if (isPrime(i)) {
      sum += i;
    }
  }
  return sum;
}
```

**41. Implement a function to perform a binary search on a sorted array in Node.js.**
```javascript
function binarySearch(arr, target) {
  let low = 0;
  let high = arr.length - 1;
  while (low <= high) {
    const mid = Math.floor((low + high) / 2);
    if (arr[mid] === target) return mid;
    if (arr[mid] < target) low = mid + 1;
    else high = mid - 1;
  }
  return -1;
}
```

**42. Create a function to check if a given string is a valid palindrome in Node.js.**
```javascript
function isPalindrome(str) {
  const cleanStr = str.toLowerCase().replace(/[\W_]/g, '');
  return cleanStr === cleanStr.split('').reverse().join('');
}
```

**43. Write a function to find the number of words in a sentence in Node.js.**
```javascript
function countWords(sentence) {
  return sentence.split(' ').length;
}
```

**44. Implement a function to check if a given string is an integer or not in Node.js.**
```javascript
function isInteger(str) {
  return /^-?\d+$/.test(str);
}
```

**45. Create a function to check if a given array is sorted in ascending order in Node.js.**
```javascript
function isSorted(arr) {
  return arr.every((value, index, array) => index === 0 || value >= array[index - 1]);
}
```

**46. Write a function to find the intersection of two arrays without using built-in functions in Node.js.**
```javascript
function arrayIntersection(arr1, arr2) {
  const result = [];
  for (const element of arr1) {
    if (arr2.includes(element) && !result.includes(element)) {
      result.push(element);
    }
  }
  return result;
}
```

**47. Implement a function to calculate the factorial of a number iteratively in Node.js.**
```javascript
function factorial(n) {
  let result = 1;
  for (let i = 2; i <= n; i++) {
    result *= i;
  }
  return result;
}
```

**48. Create a function to find the difference between two arrays in Node.js.**
```javascript
function arrayDifference(arr1, arr2) {
  return arr1.filter(element => !arr2.includes(element));
}
```

**49. Write a function to remove all white spaces from a string in Node.js.**
```javascript
function removeSpaces(str

) {
  return str.replace(/\s/g, '');
}
```

**50. Implement a function to calculate the nth Fibonacci number in Node.js.**
```javascript
function fibonacci(n) {
  let a = 0, b = 1;
  if (n <= 1) return n;
  for (let i = 2; i <= n; i++) {
    [a, b] = [b, a + b];
  }
  return b;
}
```

These questions cover a variety of topics and difficulty levels commonly encountered in Node.js coding interviews.
