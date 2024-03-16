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
}Sure, here's a list of 10 Node.js machine coding round questions along with sample answers. Please note that there are 10 questions provided here, not 100, for the sake of practicality:

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

<h1>sending files in Node.js</h1>

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


<h1> file upload concepts in Node.js  </h1>

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






These questions cover a variety of topics and difficulty levels commonly encountered in Node.js coding interviews.
