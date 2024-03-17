<h1> Here are 300  Node.js machine coding round questions with answers:</h1>

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
};
````

1. **Question: Create a simple HTTP server in Node.js that returns "Hello, World!" when accessed.**
```javascript
// Answer:
const http = require('http');
const server = http.createServer((req, res) => {
  res.writeHead(200, {'Content-Type': 'text/plain'});
  res.end('Hello, World!\n');
});
server.listen(3000, 'localhost', () => {
  console.log('Server running at http://localhost:3000/');
});
```

2. **Question: Write a function in Node.js to find the factorial of a given number.**
```javascript
// Answer:
function factorial(n) {
  if (n === 0 || n === 1) return 1;
  return n * factorial(n - 1);
}
console.log(factorial(5)); // Output: 120
```

3. **Question: Implement a basic CRUD (Create, Read, Update, Delete) API using Express.js and MongoDB.**
```javascript
// Answer:
// (Assuming MongoDB is running locally)
const express = require('express');
const bodyParser = require('body-parser');
const mongoose = require('mongoose');

mongoose.connect('mongodb://localhost/test', { useNewUrlParser: true, useUnifiedTopology: true });

const app = express();
app.use(bodyParser.json());

const Schema = mongoose.Schema;
const userSchema = new Schema({
  name: String,
  email: String,
});

const User = mongoose.model('User', userSchema);

// Routes
app.post('/users', async (req, res) => {
  const user = new User(req.body);
  await user.save();
  res.send(user);
});

app.get('/users', async (req, res) => {
  const users = await User.find();
  res.send(users);
});

app.listen(3000, () => {
  console.log('Server is running on port 3000');
});
```

4. **Question: Write a function in Node.js to reverse a string.**
```javascript
// Answer:
function reverseString(str) {
  return str.split('').reverse().join('');
}
console.log(reverseString('hello')); // Output: 'olleh'
```

5. **Question: Implement a basic authentication system using JSON Web Tokens (JWT) in Node.js.**
```javascript
// Answer:
const jwt = require('jsonwebtoken');
const secretKey = 'your-secret-key';

function generateToken(user) {
  return jwt.sign({ user }, secretKey, { expiresIn: '1h' });
}

function verifyToken(token) {
  try {
    return jwt.verify(token, secretKey);
  } catch (err) {
    return null;
  }
}

const user = { id: 1, username: 'example_user' };
const token = generateToken(user);
console.log(token);

const decoded = verifyToken(token);
console.log(decoded);
```

6. **Question: Write a function in Node.js to check if a given string is a palindrome.**
```javascript
// Answer:
function isPalindrome(str) {
  const reversed = str.split('').reverse().join('');
  return str === reversed;
}
console.log(isPalindrome('racecar')); // Output: true
```

7. **Question: Create a script in Node.js to read a JSON file and print its content.**
```javascript
// Answer:
const fs = require('fs');

fs.readFile('data.json', 'utf8', (err, data) => {
  if (err) {
    console.error(err);
    return;
  }
  console.log(data);
});
```

8. **Question: Implement a function in Node.js to find the maximum number in an array.**
```javascript
// Answer:
function findMax(arr) {
  return Math.max(...arr);
}
console.log(findMax([1, 5, 3, 9, 2])); // Output: 9
```

9. **Question: Write a function in Node.js to sort an array of numbers in ascending order.**
```javascript
// Answer:
function sortAscending(arr) {
  return arr.sort((a, b) => a - b);
}
console.log(sortAscending([3, 1, 4, 2])); // Output: [1, 2, 3, 4]
```

10. **Question: Create a script in Node.js to make an HTTP request to an external API and log the response.**
```javascript
// Answer:
const https = require('https');

https.get('https://api.example.com/data', (resp) => {
  let data = '';

  // A chunk of data has been received.
  resp.on('data', (chunk) => {
    data += chunk;
  });

  // The whole response has been received. Print out the result.
  resp.on('end', () => {
    console.log(JSON.parse(data));
  });

}).on('error', (err) => {
  console.log('Error: ' + err.message);
});
```

<h1>Here are five coding questions that focus on the callback concept in Node.js, which are commonly asked in job interviews:</h1>

1. **Question: Write a function `sumAsync` in Node.js that takes two numbers and a callback function as arguments. Inside the function, perform the addition asynchronously and invoke the callback with the result.**

```javascript
// Answer:
function sumAsync(num1, num2, callback) {
  setTimeout(() => {
    const result = num1 + num2;
    callback(result);
  }, 1000); // Simulating delay of 1 second
}

// Usage
sumAsync(3, 5, (result) => {
  console.log('Sum:', result);
});
```

2. **Question: Implement a function `findLargest` in Node.js that takes an array of numbers and a callback function. The function should find the largest number in the array asynchronously and invoke the callback with the result.**

```javascript
// Answer:
function findLargest(numbers, callback) {
  setTimeout(() => {
    const largest = Math.max(...numbers);
    callback(largest);
  }, 1000); // Simulating delay of 1 second
}

// Usage
findLargest([10, 5, 8, 20, 15], (result) => {
  console.log('Largest Number:', result);
});
```

3. **Question: Write a function `filterEven` in Node.js that takes an array of numbers and a callback function. The function should filter out the even numbers from the array asynchronously and invoke the callback with the filtered result.**

```javascript
// Answer:
function filterEven(numbers, callback) {
  setTimeout(() => {
    const evenNumbers = numbers.filter(num => num % 2 === 0);
    callback(evenNumbers);
  }, 1000); // Simulating delay of 1 second
}

// Usage
filterEven([1, 2, 3, 4, 5, 6, 7, 8, 9], (result) => {
  console.log('Even Numbers:', result);
});
```

4. **Question: Implement a function `fetchData` in Node.js that simulates fetching data from an API asynchronously. The function should take a URL and a callback function. It should fetch data from the URL and invoke the callback with the fetched data.**

```javascript
// Answer:
const axios = require('axios');

function fetchData(url, callback) {
  axios.get(url)
    .then(response => {
      callback(response.data);
    })
    .catch(error => {
      console.error('Error fetching data:', error);
    });
}

// Usage
fetchData('https://jsonplaceholder.typicode.com/posts/1', (data) => {
  console.log('Fetched Data:', data);
});
```

5. **Question: Write a function `processFiles` in Node.js that processes an array of file paths asynchronously. The function should read each file and invoke a callback with its content.**

```javascript
// Answer:
const fs = require('fs');

function processFiles(filePaths, callback) {
  const fileContents = [];
  let filesProcessed = 0;

  filePaths.forEach(filePath => {
    fs.readFile(filePath, 'utf8', (err, data) => {
      if (err) {
        console.error('Error reading file:', err);
        return;
      }
      fileContents.push(data);
      filesProcessed++;
      if (filesProcessed === filePaths.length) {
        callback(fileContents);
      }
    });
  });
}

// Usage
processFiles(['file1.txt', 'file2.txt', 'file3.txt'], (contents) => {
  console.log('File Contents:', contents);
});
````

<h3>sending files in Node.js</h3>

1. **File Sending API Endpoint**:

**Question**:
Write a Node.js API endpoint using Express.js that sends a file to the client upon receiving a GET request. The endpoint should accept a file path as a parameter, read the file from the server's filesystem, and send it as a response to the client. Handle errors appropriately, such as file not found or inaccessible file paths.

**Solution**:

```javascript
const express = require('express');
const fs = require('fs');
const app = express();

app.get('/download/:filename', (req, res) => {
    const filename = req.params.filename;
    const filePath = `./uploads/${filename}`;

    fs.readFile(filePath, (err, data) => {
        if (err) {
            res.status(404).send('File not found.');
            return;
        }
        res.setHeader('Content-Disposition', `attachment; filename=${filename}`);
        res.send(data);
    });
});

app.listen(3000, () => {
    console.log('Server is running on port 3000');
});
```

2. **Secure File Sending with Authentication**:

**Question**:
Extend the previous scenario to include user authentication. Modify the file sending endpoint to require user authentication. Only authenticated users with the correct permissions should be able to access and download files from the server.

**Solution**:

```javascript
// Implement authentication middleware (e.g., using JWT or sessions)
function authenticate(req, res, next) {
    // Check authentication logic here
    // For example, verify JWT token or check session
    // For simplicity, let's assume authentication is handled elsewhere
    const isAuthenticated = true; // Sample authentication logic
    if (isAuthenticated) {
        next();
    } else {
        res.status(401).send('Unauthorized');
    }
}

app.get('/download/:filename', authenticate, (req, res) => {
    // Same as previous solution
    // Only authenticated users can access this endpoint
});
```

3. **Chunked File Sending**:

**Question**:
Implement a Node.js application that sends large files to clients in smaller, manageable chunks. Create a mechanism to read the file in chunks from the server's filesystem and send them as separate responses to the client. Ensure that the client can assemble the chunks into the original file.

**Solution**:

```javascript
// Chunked file sending logic can be implemented using streams
const fileStream = fs.createReadStream(filePath);
fileStream.on('data', (chunk) => {
    res.write(chunk);
});
fileStream.on('end', () => {
    res.end();
});
```

4. **File Streaming for Large File Sending**:

**Question**:
Develop a Node.js application that efficiently streams large files to clients. Implement a file streaming mechanism that reads chunks of a file from the server's filesystem and streams them as responses to clients. Optimize the streaming process to handle large files without consuming excessive memory or causing performance issues.

**Solution**:

```javascript
const fileStream = fs.createReadStream(filePath);
fileStream.pipe(res);
```

5. **Progressive File Sending**:

**Question**:
Extend an existing Node.js file sending application to support progressive file sending. Implement a mechanism to send the file to the client progressively, meaning the client should start receiving and rendering the file content as soon as the initial portion is available, without waiting for the entire file to be transferred.

**Solution**:

```javascript
// Implement a streaming response with 'data' event
const fileStream = fs.createReadStream(filePath);
fileStream.on('data', (chunk) => {
    res.write(chunk);
});
fileStream.on('end', () => {
    res.end();
});
``````

<h2> file upload concepts in Node.js  </h2>

1. **File Upload API Endpoint**:

**Question**:
Write a Node.js API endpoint using Express.js that accepts file uploads. The endpoint should accept multipart form-data POST requests containing a file, and upon successful upload, should respond with a success message. Include error handling for cases where no file is provided or if the file size exceeds a specified limit.

**Solution**:
```javascript
const express = require('express');
const multer = require('multer');
const app = express();
const upload = multer({ dest: 'uploads/' });

app.post('/upload', upload.single('file'), (req, res) => {
    if (!req.file) {
        return res.status(400).send('No file uploaded.');
    }
    // File upload successful
    res.send('File uploaded successfully.');
});

app.listen(3000, () => {
    console.log('Server is running on port 3000');
});
```

2. **Image Resizing on Upload**:

**Question**:
Create a Node.js script that accepts an image upload and resizes it to specified dimensions (e.g., 300x300 pixels). Use the `multer` middleware for handling file uploads and `sharp` for image resizing. Ensure proper error handling for invalid image uploads or resizing failures.

**Solution**:
```javascript
const express = require('express');
const multer = require('multer');
const sharp = require('sharp');
const app = express();
const upload = multer({ dest: 'uploads/' });

app.post('/upload', upload.single('image'), (req, res) => {
    if (!req.file) {
        return res.status(400).send('No image uploaded.');
    }
    sharp(req.file.path)
        .resize(300, 300)
        .toFile('uploads/resized_image.jpg', (err) => {
            if (err) {
                return res.status(500).send('Error resizing image.');
            }
            res.send('Image uploaded and resized successfully.');
        });
});

app.listen(3000, () => {
    console.log('Server is running on port 3000');
});
```

3. **CSV File Processing**:

**Question**:
Implement a Node.js script that accepts CSV file uploads and processes the data within the CSV file. Upon upload, parse the CSV file and log its contents to the console. Handle errors gracefully, such as incorrect file format or parsing failures.

**Solution**:
```javascript
const express = require('express');
const multer = require('multer');
const csv = require('csv-parser');
const fs = require('fs');
const app = express();
const upload = multer({ dest: 'uploads/' });

app.post('/upload', upload.single('csv'), (req, res) => {
    if (!req.file) {
        return res.status(400).send('No CSV file uploaded.');
    }
    const results = [];
    fs.createReadStream(req.file.path)
        .pipe(csv())
        .on('data', (data) => results.push(data))
        .on('end', () => {
            console.log(results);
            res.send('CSV file uploaded and processed successfully.');
        })
        .on('error', (err) => {
            console.error('Error parsing CSV:', err);
            res.status(500).send('Error parsing CSV file.');
        });
});

app.listen(3000, () => {
    console.log('Server is running on port 3000');
});
```

4. **File Upload Progress Tracking**:

**Question**:
Develop a Node.js application that allows users to track the progress of file uploads. Use `express` and `multer` to handle file uploads and implement a progress bar or percentage indicator to display the progress of the file upload in real-time on the client-side.

**Solution**:
```javascript
// Progress tracking can be achieved using the `progress` event provided by `multer`
const express = require('express');
const multer = require('multer');
const app = express();
const upload = multer({ dest: 'uploads/' });

app.post('/upload', upload.single('file'), (req, res) => {
    // Upload progress tracking
    upload(req, res, function (err) {
        if (err) {
            console.error('Error uploading file:', err);
            return res.status(500).send('Error uploading file.');
        }
        // File upload successful
        res.send('File uploaded successfully.');
    });
});

app.listen(3000, () => {
    console.log('Server is running on port 3000');
});
```

5. **File Upload with Authentication**:

**Question**:
Extend an existing Node.js application with user authentication to support secure file uploads. Ensure that only authenticated users can upload files. Implement role-based access control to allow certain users (e.g., administrators) to upload files of any size while restricting others to smaller file sizes.

**Solution**:
```javascript
// Implement authentication middleware (e.g., using JWT or sessions)
function authenticate(req, res, next) {
    // Check authentication logic here
    // For example, verify JWT token or check session
    // For simplicity, let's assume authentication is handled elsewhere
    const isAuthenticated = true; // Sample authentication logic
    if (isAuthenticated) {
        next();
    } else {
        res.status(401).send('Unauthorized');
    }
}

const upload = multer({
    dest: 'uploads/',
    limits: { fileSize: 10 * 1024 * 1024 } // 10MB file size limit
});

app.post('/upload', authenticate, upload.single('file'), (req, res) => {
    // Only authenticated users can upload files
    if (!req.file) {
        return res.status(400).send('No file uploaded.');
    }
    // File upload successful
    res.send('File uploaded successfully.');
});
```

<h2> event , event loop , event emitter </h2>

1. **Understanding Event Emitters:**
   ```javascript
   // Example of using Event Emitters in Node.js
   const EventEmitter = require('events');

   // Create a new EventEmitter instance
   const myEmitter = new EventEmitter();

   // Define an event
   const eventName = 'greet';

   // Listener function for the event
   myEmitter.on(eventName, (name) => {
       console.log(`Hello, ${name}!`);
   });

   // Emit the event with some data
   myEmitter.emit(eventName, 'John');
   ```

2. **Event Loop Mechanics:**
   - The event loop in Node.js is a single-threaded mechanism that enables asynchronous I/O operations without blocking the execution of other tasks. It continuously checks for events and executes their associated callback functions. Below is a conceptual example:
   ```javascript
   const fs = require('fs');

   // Asynchronous file read operation
   fs.readFile('example.txt', 'utf8', (err, data) => {
       if (err) {
           console.error('Error reading file:', err);
           return;
       }
       console.log('File data:', data);
   });

   console.log('File read operation initiated.');
   ```

3. **Custom Event Handling:**
   ```javascript
   const EventEmitter = require('events');

   class MyEmitter extends EventEmitter {}

   const myEmitter = new MyEmitter();

   // Event listeners
   myEmitter.on('start', () => {
       console.log('Starting process...');
   });

   myEmitter.on('finish', () => {
       console.log('Process completed.');
   });

   // Emitting custom events
   myEmitter.emit('start');
   // Process logic...
   myEmitter.emit('finish');
   ```

4. **Event Emitter Inheritance:**
   ```javascript
   const EventEmitter = require('events');

   // Parent EventEmitter
   class ParentEmitter extends EventEmitter {
       constructor() {
           super();
       }
   }

   // Child EventEmitter inheriting from Parent
   class ChildEmitter extends ParentEmitter {}

   const parentEmitter = new ParentEmitter();
   const childEmitter = new ChildEmitter();

   // Event listeners
   parentEmitter.on('parentEvent', () => {
       console.log('Parent event triggered.');
   });

   // Inherited event listener
   childEmitter.on('childEvent', () => {
       console.log('Child event triggered.');
   });

   // Emit events
   parentEmitter.emit('parentEvent');
   childEmitter.emit('childEvent');
   ```

5. **Handling Memory Leaks with EventEmitters:**
   - One common strategy to prevent memory leaks with EventEmitters in Node.js is to ensure that all event listeners are properly removed when they are no longer needed. This can be achieved using the `removeListener()` method. Here's an example:
   ```javascript
   const EventEmitter = require('events');

   class MyEmitter extends EventEmitter {}

   const myEmitter = new MyEmitter();

   function listener() {
       console.log('Event handled.');
   }

   // Adding event listener
   myEmitter.on('event', listener);

   // Removing event listener after it's no longer needed
   setTimeout(() => {
       myEmitter.removeListener('event', listener);
       console.log('Event listener removed.');
   }, 5000);
   ```
   <h4>Here are five important coding questions with answers for EventEmitter in Node.js:</h4> 

1. **Question:** How do you create an instance of EventEmitter in Node.js?

**Answer:**
```javascript
const EventEmitter = require('events');
const myEmitter = new EventEmitter();
```

2. **Question:** How do you listen for an event using EventEmitter?

**Answer:**
```javascript
myEmitter.on('eventName', () => {
  console.log('Event occurred!');
});
```

3. **Question:** How do you emit an event with data using EventEmitter?

**Answer:**
```javascript
myEmitter.emit('eventName', data);
```

4. **Question:** How do you remove an event listener using EventEmitter?

**Answer:**
```javascript
// Define the listener function
const myListener = () => {
  console.log('Event occurred!');
};

// Add the listener
myEmitter.on('eventName', myListener);

// Remove the listener
myEmitter.removeListener('eventName', myListener);
```

5. **Question:** How do you handle one-time events with EventEmitter?

**Answer:**
```javascript
myEmitter.once('eventName', () => {
  console.log('This listener will only be called once.');
});
```
Sure, here are five important coding questions related to process concept in Node.js along with their answers:

1. **Question: How can you get the process ID (PID) of a Node.js application?**
   
   **Answer:** In Node.js, you can obtain the process ID (PID) using the `process.pid` property. Here's an example:

   ```javascript
   console.log("Process ID:", process.pid);
   ```

2. **Question: How can you handle command-line arguments passed to a Node.js application?**

   **Answer:** Node.js provides access to command-line arguments through the `process.argv` array. Here's a simple example:

   ```javascript
   // Print all command-line arguments
   process.argv.forEach((arg, index) => {
       console.log(`Argument ${index}: ${arg}`);
   });
   ```

3. **Question: How can you exit a Node.js application programmatically?**

   **Answer:** You can exit a Node.js application programmatically by calling `process.exit(code)`, where `code` is an optional exit code. Here's an example:

   ```javascript
   // Exit the application with exit code 0 (success)
   process.exit(0);
   ```

4. **Question: How can you set environment variables in a Node.js application?**

   **Answer:** You can set environment variables using the `process.env` object. Here's how you can set and access an environment variable:

   ```javascript
   // Set an environment variable
   process.env.PORT = 3000;

   // Access the environment variable
   console.log("Port:", process.env.PORT);
   ```

5. **Question: How can you listen for signals like SIGINT (Ctrl+C) in a Node.js application?**

   **Answer:** You can listen for signals using the `process.on()` method. Here's how you can handle the SIGINT signal (Ctrl+C):

   ```javascript
   // Handle SIGINT signal (Ctrl+C)
   process.on('SIGINT', () => {
       console.log('Received SIGINT signal');
       // Perform cleanup or exit the application
       process.exit(0);
   });
   ```
  <h5>Here are 20 important machine coding round questions related to RESTful concepts in Node.js at an intermediate level along with their answers:</h5> 

1. **Question: Create a RESTful API endpoint to fetch a list of users from a database.**

   Answer: 
   ```javascript
   const express = require('express');
   const app = express();

   // Mock user data
   const users = [{ id: 1, name: 'John' }, { id: 2, name: 'Alice' }];

   app.get('/users', (req, res) => {
       res.json(users);
   });

   app.listen(3000, () => {
       console.log('Server running on port 3000');
   });
   ```

2. **Question: Implement an endpoint to add a new user to the database using POST request.**

   Answer:
   ```javascript
   app.post('/users', (req, res) => {
       const newUser = req.body;
       users.push(newUser);
       res.status(201).json(newUser);
   });
   ```

3. **Question: Write a route to fetch details of a specific user by their ID.**

   Answer:
   ```javascript
   app.get('/users/:id', (req, res) => {
       const userId = parseInt(req.params.id);
       const user = users.find(user => user.id === userId);
       if (user) {
           res.json(user);
       } else {
           res.status(404).json({ message: 'User not found' });
       }
   });
   ```

4. **Question: Implement an endpoint to update user details using PUT request.**

   Answer:
   ```javascript
   app.put('/users/:id', (req, res) => {
       const userId = parseInt(req.params.id);
       const updateUser = req.body;
       const index = users.findIndex(user => user.id === userId);
       if (index !== -1) {
           users[index] = { ...users[index], ...updateUser };
           res.json(users[index]);
       } else {
           res.status(404).json({ message: 'User not found' });
       }
   });
   ```

5. **Question: Create a route to delete a user by their ID.**

   Answer:
   ```javascript
   app.delete('/users/:id', (req, res) => {
       const userId = parseInt(req.params.id);
       const index = users.findIndex(user => user.id === userId);
       if (index !== -1) {
           const deletedUser = users.splice(index, 1);
           res.json({ message: 'User deleted', user: deletedUser });
       } else {
           res.status(404).json({ message: 'User not found' });
       }
   });
   ```

6. **Question: Implement pagination for fetching users (limit and offset).**

   Answer:
   ```javascript
   app.get('/users', (req, res) => {
       const limit = parseInt(req.query.limit) || 10;
       const offset = parseInt(req.query.offset) || 0;
       const paginatedUsers = users.slice(offset, offset + limit);
       res.json(paginatedUsers);
   });
   ```

7. **Question: Add authentication middleware to secure user-related endpoints.**

   Answer:
   ```javascript
   function authenticate(req, res, next) {
       const token = req.headers.authorization;
       if (token === 'secret_token') {
           next();
       } else {
           res.status(401).json({ message: 'Unauthorized' });
       }
   }

   app.use(authenticate);
   ```

8. **Question: Implement validation middleware to validate user input before processing.**

   Answer:
   ```javascript
   function validateUser(req, res, next) {
       const { name } = req.body;
       if (!name) {
           res.status(400).json({ message: 'Name is required' });
       } else {
           next();
       }
   }

   app.post('/users', validateUser, (req, res) => {
       // Add user to the database
   });
   ```

9. **Question: Write a route to upload a user's profile picture.**

   Answer:
   ```javascript
   const multer = require('multer');
   const upload = multer({ dest: 'uploads/' });

   app.post('/users/:id/profile-picture', upload.single('avatar'), (req, res) => {
       const userId = parseInt(req.params.id);
       const user = users.find(user => user.id === userId);
       if (user) {
           user.profilePicture = req.file.path;
           res.json({ message: 'Profile picture uploaded successfully' });
       } else {
           res.status(404).json({ message: 'User not found' });
       }
   });
   ```

10. **Question: Implement rate limiting to restrict the number of requests per minute from a single IP address.**

    Answer:
    ```javascript
    const rateLimit = require('express-rate-limit');
    const limiter = rateLimit({
        windowMs: 60 * 1000, // 1 minute
        max: 100 // limit each IP to 100 requests per windowMs
    });

    app.use(limiter);
    ```

11. **Question: Create a route to search for users by their name or email.**

    Answer:
    ```javascript
    app.get('/users/search', (req, res) => {
        const { q } = req.query;
        const filteredUsers = users.filter(user => 
            user.name.toLowerCase().includes(q.toLowerCase()) || 
            user.email.toLowerCase().includes(q.toLowerCase())
        );
        res.json(filteredUsers);
    });
    ```

12. **Question: Implement content compression to reduce response size and improve performance.**

    Answer:
    ```javascript
    const compression = require('compression');
    app.use(compression());
    ```

13. **Question: Write a route to handle file downloads.**

    Answer:
    ```javascript
    app.get('/files/:filename', (req, res) => {
        const filePath = `path/to/files/${req.params.filename}`;
        res.download(filePath);
    });
    ```

14. **Question: Implement a middleware to log incoming requests.**

    Answer:
    ```javascript
    function logger(req, res, next) {
        console.log(`${req.method} ${req.url}`);
        next();
    }

    app.use(logger);
    ```

15. **Question: Create a route to handle error responses with proper HTTP status codes and messages.**

    Answer:
    ```javascript
    app.use((err, req, res, next) => {
        console.error(err.stack);
        res.status(500).json({ message: 'Internal Server Error' });
    });
    ```

16. **Question: Implement content negotiation to support response format based on client preferences (JSON, XML, etc.).**

    Answer:
    ```javascript
    app.get('/users', (req, res) => {
        const accept = req.headers['accept'];
        if (accept === 'application/xml') {
            // Generate XML response
        } else {
            res.json(users);
        }
    });
    ```

17. **Question: Write a route to handle batch operations for users (e.g., delete multiple users at once).**

    Answer:
    ```javascript
    app.delete('/users', (req, res) => {
        const userIds

 = req.body.userIds;
        userIds.forEach(id => {
            const index = users.findIndex(user => user.id === id);
            if (index !== -1) {
                users.splice(index, 1);
            }
        });
        res.json({ message: 'Users deleted successfully' });
    });
    ```

18. **Question: Implement HATEOAS (Hypermedia as the Engine of Application State) in your API responses.**

    Answer:
    ```javascript
    app.get('/users', (req, res) => {
        const usersWithLinks = users.map(user => ({
            ...user,
            links: [
                { rel: 'self', href: `/users/${user.id}` },
                { rel: 'update', href: `/users/${user.id}`, method: 'PUT' },
                { rel: 'delete', href: `/users/${user.id}`, method: 'DELETE' }
            ]
        }));
        res.json(usersWithLinks);
    });
    ```

19. **Question: Write a route to handle partial updates for user details.**

    Answer:
    ```javascript
    app.patch('/users/:id', (req, res) => {
        const userId = parseInt(req.params.id);
        const updateUser = req.body;
        const index = users.findIndex(user => user.id === userId);
        if (index !== -1) {
            users[index] = { ...users[index], ...updateUser };
            res.json(users[index]);
        } else {
            res.status(404).json({ message: 'User not found' });
        }
    });
    ```

20. **Question: Implement content versioning in your API to support backward compatibility.**

    Answer:
    ```javascript
    app.get('/v1/users', (req, res) => {
        // Handle version 1 of the API
    });

    app.get('/v2/users', (req, res) => {
        // Handle version 2 of the API
    });
    ```

These questions and answers cover various aspects of building a RESTful API in Node.js, including CRUD operations, authentication, validation, file handling, error handling, content negotiation, and API versioning, suitable for an intermediate-level machine coding round.

 Here are 10 important coding questions along with their answers for the buffer concept in Node.js at an intermediate level:

1. **Question: How to create a buffer in Node.js?**

   Answer:
   ```javascript
   const buf = Buffer.alloc(10); // Creates a buffer of size 10 bytes filled with zeros
   ```

2. **Question: Write code to convert a string to a buffer in Node.js.**

   Answer:
   ```javascript
   const str = 'Hello, world!';
   const buf = Buffer.from(str);
   ```

3. **Question: Implement a function to concatenate multiple buffers in Node.js.**

   Answer:
   ```javascript
   function concatenateBuffers(buffers) {
       return Buffer.concat(buffers);
   }
   ```

4. **Question: How to encode a buffer to Base64 in Node.js?**

   Answer:
   ```javascript
   const buf = Buffer.from('Hello, world!');
   const base64Str = buf.toString('base64');
   ```

5. **Question: Write code to decode a Base64 string to a buffer in Node.js.**

   Answer:
   ```javascript
   const base64Str = 'SGVsbG8sIHdvcmxkIQ==';
   const buf = Buffer.from(base64Str, 'base64');
   ```

6. **Question: Implement a function to compare two buffers in Node.js.**

   Answer:
   ```javascript
   function compareBuffers(buf1, buf2) {
       return buf1.equals(buf2);
   }
   ```

7. **Question: How to slice a buffer in Node.js?**

   Answer:
   ```javascript
   const buf = Buffer.from('Hello, world!');
   const slicedBuf = buf.slice(0, 5); // Slice from index 0 to 4
   ```

8. **Question: Write code to find the index of a substring in a buffer in Node.js.**

   Answer:
   ```javascript
   const buf = Buffer.from('Hello, world!');
   const index = buf.indexOf('world');
   ```

9. **Question: Implement a function to copy data from one buffer to another in Node.js.**

   Answer:
   ```javascript
   function copyBuffer(source, target, targetStart, sourceStart, sourceEnd) {
       source.copy(target, targetStart, sourceStart, sourceEnd);
   }
   ```

10. **Question: How to convert a buffer to JSON in Node.js?**

    Answer:
    ```javascript
    const buf = Buffer.from('{"name":"John","age":30}');
    const json = buf.toJSON();
    ```

These questions and answers cover various aspects of working with buffers in Node.js, including creation, encoding, decoding, manipulation, comparison, slicing, searching, copying, and conversion to JSON, suitable for an intermediate-level understanding of buffer concepts.




Certainly! Here are 10 important coding questions related to stream concepts in Node.js at an intermediate level along with their answers:

1. **Question: How do you create a readable stream to read data from a file in Node.js?**

   Answer:
   ```javascript
   const fs = require('fs');
   const readableStream = fs.createReadStream('example.txt');
   ```

2. **Question: Write code to pipe data from a readable stream to a writable stream in Node.js.**

   Answer:
   ```javascript
   const fs = require('fs');
   const readableStream = fs.createReadStream('input.txt');
   const writableStream = fs.createWriteStream('output.txt');

   readableStream.pipe(writableStream);
   ```

3. **Question: Implement a transform stream to convert data from uppercase to lowercase as it passes through.**

   Answer:
   ```javascript
   const { Transform } = require('stream');

   const uppercaseToLowercase = new Transform({
       transform(chunk, encoding, callback) {
           this.push(chunk.toString().toLowerCase());
           callback();
       }
   });

   process.stdin.pipe(uppercaseToLowercase).pipe(process.stdout);
   ```

4. **Question: How do you handle errors in streams in Node.js?**

   Answer:
   ```javascript
   readableStream.on('error', (error) => {
       console.error('Error reading from stream:', error);
   });

   writableStream.on('error', (error) => {
       console.error('Error writing to stream:', error);
   });
   ```

5. **Question: Implement a readable stream that generates random numbers and emits them.**

   Answer:
   ```javascript
   const { Readable } = require('stream');

   class RandomNumberStream extends Readable {
       constructor(options) {
           super(options);
       }

       _read(size) {
           const randomNumber = Math.random();
           this.push(randomNumber.toString());
       }
   }

   const randomNumberStream = new RandomNumberStream();
   randomNumberStream.pipe(process.stdout);
   ```

6. **Question: How can you pause and resume a readable stream in Node.js?**

   Answer:
   ```javascript
   readableStream.pause();

   // Do something else...

   readableStream.resume();
   ```

7. **Question: Write code to create a writable stream that stores data in memory until it reaches a certain size limit, then flushes it to disk.**

   Answer:
   ```javascript
   const { Writable } = require('stream');
   const fs = require('fs');

   class MemoryWritableStream extends Writable {
       constructor(options) {
           super(options);
           this.buffer = [];
           this.sizeLimit = 1024 * 1024; // 1MB
       }

       _write(chunk, encoding, callback) {
           this.buffer.push(chunk);
           if (Buffer.concat(this.buffer).length >= this.sizeLimit) {
               fs.writeFile('output.txt', Buffer.concat(this.buffer), callback);
               this.buffer = [];
           } else {
               callback();
           }
       }
   }

   const memoryWritableStream = new MemoryWritableStream();
   process.stdin.pipe(memoryWritableStream);
   ```

8. **Question: How do you create a duplex stream in Node.js?**

   Answer:
   ```javascript
   const { Duplex } = require('stream');

   const duplexStream = new Duplex({
       read(size) {
           // Implement reading logic
       },
       write(chunk, encoding, callback) {
           // Implement writing logic
           callback();
       }
   });
   ```

9. **Question: Implement a writable stream that compresses data using gzip compression.**

   Answer:
   ```javascript
   const { createGzip } = require('zlib');
   const fs = require('fs');

   const gzipStream = createGzip();
   const writableStream = fs.createWriteStream('output.txt.gz');

   process.stdin.pipe(gzipStream).pipe(writableStream);
   ```

10. **Question: How do you handle the end of a stream in Node.js?**

    Answer:
    ```javascript
    readableStream.on('end', () => {
        console.log('End of stream reached');
    });

    writableStream.on('finish', () => {
        console.log('Data writing finished');
    });
    ```

These questions and answers cover various aspects of working with streams in Node.js, including creating streams, piping data, error handling, stream events, and implementing custom stream logic, suitable for an intermediate-level understanding of stream concepts.



These answers provide explanations and code examples to address the concepts and scenarios related to events and the event loop in Node.js.

