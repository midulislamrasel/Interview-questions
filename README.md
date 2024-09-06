## JavaScript

OOP-এর ফুল ফর্ম হলো Object-Oriented Programming। এটি একটি প্রোগ্রামিং প্যারাডাইম যা ডেটাকে অবজেক্ট হিসেবে মডেল করে এবং কোডকে পুনঃব্যবহারযোগ্য এবং মডুলার করে তুলতে সাহায্য করে। OOP-এর চারটি প্রধান বৈশিষ্ট্য হলো:

* Encapsulation: ডেটা এবং ফাংশনগুলোকে একত্রে বাঁধাই করা, যাতে ডেটা সরাসরি অ্যাক্সেস না করা যায় এবং শুধুমাত্র নির্দিষ্ট পদ্ধতির মাধ্যমে ডেটা ম্যানিপুলেট করা যায়।

* Inheritance: এক শ্রেণি (class) অন্য শ্রেণির বৈশিষ্ট্য ও পদ্ধতিগুলি উত্তরাধিকারসূত্রে প্রাপ্ত করে, কোড পুনঃব্যবহারের সুবিধা দেয়।

* Polymorphism: একাধিক রূপে কোনো জিনিসের উপস্থিতি, যেখানে একই ফাংশন বা অপারেশন বিভিন্ন পরিস্থিতিতে বিভিন্নভাবে আচরণ করে।

* Abstraction: জটিলতাগুলো লুকিয়ে রেখে শুধুমাত্র প্রয়োজনীয় বৈশিষ্ট্যগুলো দেখানো, যাতে ব্যবহারকারী অপ্রয়োজনীয় বিবরণ থেকে বিচ্ছিন্ন থাকে।



#### JavaScript কী ?
* উত্তর: JavaScript হলো একটি high-level, interpreted প্রোগ্রামিং ভাষা, যা সাধারণত ওয়েব ব্রাউজারগুলোতে ক্লায়েন্ট-সাইড স্ক্রিপ্টিং করার জন্য ব্যবহৃত হয়। এটি HTML এবং CSS এর সাথে ওয়েবপেজকে ডায়নামিক ও ইন্টারঅ্যাকটিভ করতে সাহায্য করে।


#### JavaScript-এ ভ্যারিয়েবল ডিক্লেয়ার করার উপায় কী কী?
* var: ES5-এর আগে ব্যবহার হত, function-scoped এবং রিডিক্লেয়ার করা যায়।
* let: ES6-এ ইন্ট্রোডিউস করা হয়েছে, block-scoped এবং রিডিক্লেয়ার করা যায় না।
* const: ES6-এ ইন্ট্রোডিউস করা হয়েছে, block-scoped, constant ভ্যারিয়েবল যা পরে পরিবর্তন করা যায় না।

** বিশ্লেষণ: ভ্যারিয়েবল ডিক্লেয়ার করার বিভিন্ন উপায় সম্পর্কে জ্ঞান পরীক্ষা করার জন্য এই প্রশ্নটি গুরুত্বপূর্ণ। এটি প্রমাণ করে আপনি ES6 ফিচার সম্পর্কে কতটা জানেন।


#### 3. JavaScript-এ == এবং === এর মধ্যে পার্থক্য কী?
*  == (Loose Equality): দুই ভ্যালুর টাইপের উপর নির্ভর না করে ভ্যালু মিলে গেলে true রিটার্ন করে। এটি টাইপ কনভার্সন করে।
*  === (Strict Equality): দুই ভ্যালুর টাইপ এবং ভ্যালু উভয়ই মিলে গেলে true রিটার্ন করে। এটি টাইপ কনভার্সন করে না।

** বিশ্লেষণ: এই প্রশ্নটি আপনাকে টাইপ কনভার্সন এবং তুলনা অপারেটর সম্পর্কে জ্ঞান যাচাই করতে সাহায্য করে। এটি একটি সাধারণ কিন্তু গুরুত্বপূর্ণ প্রশ্ন।



#### 4. JavaScript-এ Closures কী?
* উত্তর: Closures হলো এমন একটি ফাংশন যা তার লেক্সিক্যাল স্কোপের বাইরে থেকেও তার নিজস্ব স্কোপে থাকা ভ্যারিয়েবলগুলোর অ্যাক্সেস পায়। এটি ফাংশনের অভ্যন্তরের ডেটা ব্যবস্থাপনা করার ক্ষমতা প্রমাণ করে।


````js
function outer() {
    let count = 0;
    return function inner() {
        count++;
        return count;
    }
}

const counter = outer();
console.log(counter()); // 1
console.log(counter()); // 2

````


#### 5. JavaScript-এ Hoisting কী?
* উত্তর: Hoisting হলো JavaScript-এর একটি ডিফল্ট আচরণ, যেখানে ভ্যারিয়েবল এবং ফাংশন ডিক্লেয়ারেশনগুলো স্কোপের শুরুর দিকে তুলে আনা হয়। তবে, ভ্যারিয়েবলের ভ্যালু অ্যাসাইনমেন্ট হোস্ট হয় না।

````js
console.log(a); // Undefined
var a = 5;
````


#### 6. Event Delegation কী?
* উত্তর: Event Delegation একটি টেকনিক, যেখানে একাধিক চাইল্ড এলিমেন্টের ইভেন্ট হ্যান্ডলার পৃথকভাবে অ্যাটাচ করার পরিবর্তে প্যারেন্ট এলিমেন্টের উপর একটি ইভেন্ট হ্যান্ডলার অ্যাটাচ করা হয় এবং ইভেন্টগুলি সেই প্যারেন্টে প্রোপাগেট হয়।
* Event Delegation বড় DOM ট্রি-এর পারফরম্যান্স উন্নত করার জন্য ব্যবহৃত হয়।

````js
  document.getElementById('parent').addEventListener('click', function(event) {
    if (event.target && event.target.matches("button.class")) {
        console.log('Button clicked!');
    }
});
`````


####  7. JavaScript-এ call(), apply(), এবং bind() এর মধ্যে পার্থক্য কী?
* call(): এটি একটি ফাংশনকে এক্সিকিউট করে এবং প্রয়োজনীয় আর্গুমেন্টগুলোকে কমা দ্বারা আলাদা করে পাস করে।
* apply(): এটি একটি ফাংশনকে এক্সিকিউট করে এবং আর্গুমেন্টগুলোকে একটি অ্যারের মধ্যে পাস করে।
* bind(): এটি একটি নতুন ফাংশন তৈরি করে এবং সেটিকে একটি নির্দিষ্ট this এর সাথে বেঁধে দেয়, যা পরে কল করা যায়।

````js
function greet(greeting, punctuation) {
    console.log(greeting + ', ' + this.name + punctuation);
}

const person = { name: 'John' };
greet.call(person, 'Hello', '!');   // Hello, John!
greet.apply(person, ['Hi', '!']);   // Hi, John!
const boundGreet = greet.bind(person);
boundGreet('Hey', '!');             // Hey, John!
````


#### 8. Arrow Function এবং Regular Function এর মধ্যে পার্থক্য কী?
* Arrow Functions: এটি নতুন ES6 ফিচার। এর this ডিফাইনিং স্কোপের সাথে বাউন্ড হয় এবং এর ফাংশন বডির মধ্যে this পরিবর্তন করা যায় না।
* Regular Functions: এর this ভ্যালু পরিবর্তন হতে পারে এবং এটি ফাংশন কলের উপর নির্ভর করে।
````js
const obj = {
    name: "John",
    regularFunc: function() { console.log(this.name); },
    arrowFunc: () => { console.log(this.name); }
};

obj.regularFunc(); // John
obj.arrowFunc();   // Undefined (arrow function does not bind `this`)
````


#### . JavaScript-এ Promises কী এবং এটি কীভাবে কাজ করে?
*  Promise হলো একটি ES6 ফিচার, যা অ্যাসিনক্রোনাস অপারেশন পরিচালনা করে। এটি তিনটি স্টেট নিয়ে কাজ করে:
      * Pending: অপারেশন চলছে।
      * Fulfilled: অপারেশন সফলভাবে শেষ হয়েছে।
      * Rejected: অপারেশন ব্যর্থ হয়েছে।
````js
const myPromise = new Promise((resolve, reject) => {
    const success = true;
    if (success) {
        resolve('Operation successful');
    } else {
        reject('Operation failed');
    }
});

myPromise.then(result => {
    console.log(result);
}).catch(error => {
    console.log(error);
});
````


#### 10. JavaScript-এ Async/Await কী?
* উত্তর: Async/Await হলো Promises-এর উপর ভিত্তি করে গঠিত ES8 ফিচার, যা অ্যাসিনক্রোনাস কোড লেখাকে আরও সহজ এবং সিঙ্ক্রোনাস স্টাইলে দেখায়।
````js
async function fetchData() {
    try {
        let response = await fetch('https://api.example.com/data');
        let data = await response.json();
        console.log(data);
    } catch (error
````


#### 11. JavaScript-এ map(), forEach(), এবং filter() এর মধ্যে পার্থক্য কী?
* map(): এটি একটি নতুন অ্যারে রিটার্ন করে এবং প্রতিটি এলিমেন্টের উপর একটি ফাংশন অ্যাপ্লাই করে।
* forEach(): এটি প্রতিটি এলিমেন্টের উপর একটি ফাংশন এক্সিকিউট করে, কিন্তু কিছু রিটার্ন করে না।
* filter(): এটি একটি নতুন অ্যারে রিটার্ন করে, যেটিতে শুধুমাত্র সেই এলিমেন্টগুলো থাকবে যেগুলো শর্ত পূরণ করে।
````js
const arr = [1, 2, 3, 4, 5];

const mappedArr = arr.map(num => num * 2); // [2, 4, 6, 8, 10]
arr.forEach(num => console.log(num));      // 1 2 3 4 5
const filteredArr = arr.filter(num => num > 3); // [4, 5]
````


#### 12. JavaScript-এ Event Loop কী এবং এটি কীভাবে কাজ করে?
* উত্তর: JavaScript একটি single-threaded, asynchronous ভাষা। Event Loop এমন একটি প্রক্রিয়া, যা কলস্ট্যাক এবং মাইক্রোটাস্ক/ম্যাক্রোটাস্ক কিউর মধ্যে অ্যাসিনক্রোনাস অপারেশনগুলো পরিচালনা করে। এটি কোডের অ্যাসিনক্রোনাস কাজগুলো সম্পন্ন করার জন্য কোডের সিকোয়েন্স ম্যানেজ করে।
````js
console.log('Start');

setTimeout(() => {
    console.log('Inside Timeout');
}, 0);

console.log('End');

# OUTPUT #
Start
End
Inside Timeout
````  



#### 13. JavaScript-এ Prototypal Inheritance কী?
* Prototypal Inheritance হলো JavaScript-এর একটি মেকানিজম, যেখানে একটি অবজেক্ট অন্য একটি অবজেক্ট থেকে প্রোপার্টি ও মেথড ইনহেরিট করে। প্রতিটি অবজেক্টের একটি prototype থাকে, যা থেকে এটি ইনহেরিট করে।
````js
function Person(name, age) {
    this.name = name;
    this.age = age;
}

Person.prototype.greet = function() {
    console.log('Hello, ' + this.name);
};

const john = new Person('John', 30);
john.greet(); // Hello, John
````

#### 14. JavaScript-এ async এবং defer অ্যাট্রিবিউটের মধ্যে পার্থক্য কী?
* async: স্ক্রিপ্টকে ডাউনলোড এবং এক্সিকিউট করা হয় প্যারালাললি, অর্থাৎ HTML লোড হওয়ার সময় থেমে যাবে না।
* defer: স্ক্রিপ্টটি ডাউনলোড করা হয় প্যারালাললি, কিন্তু HTML লোড হওয়ার পর এক্সিকিউট করা হয়।
````js
<script src="script.js" async></script>
<script src="script.js" defer></script>
````


#### 15. JavaScript-এ Callback এবং Promise এর মধ্যে পার্থক্য কী?
* Callback: একটি ফাংশন যা অন্য ফাংশনের আর্গুমেন্ট হিসেবে পাস করা হয় এবং কিছু নির্দিষ্ট কাজ শেষে কল করা হয়।
* Callback function হলো একটি ফাংশন যা আরেকটি ফাংশনকে আর্গুমেন্ট হিসেবে পাস করা হয় এবং তারপর দ্বিতীয় ফাংশনের ভিতরে এক্সিকিউট হয়। এটি অ্যাসিনক্রোনাস প্রোগ্রামিংয়ে ব্যবহৃত হয়।
* Promise: একটি ES6 ফিচার, যা অ্যাসিনক্রোনাস অপারেশনের ফলাফল পাস করার জন্য ব্যবহৃত হয় এবং এতে then() ও catch() মেথড থাকে।

````js
// Callback
function getData(callback) {
    setTimeout(() => {
        callback('Data fetched');
    }, 1000);
}

getData(data => console.log(data));

// Promise
function getDataPromise() {
    return new Promise((resolve, reject) => {
        setTimeout(() => {
            resolve('Data fetched');
        }, 1000);
    });
}

getDataPromise().then(data => console.log(data));
````

#### 16 What is the difference between null and undefined in JavaScript?
* null: এটি একটি মান, যা ইচ্ছাকৃতভাবে "কিছু নেই" বা "খালি মান" নির্দেশ করে।
* undefined: এটি একটি ভ্যারিয়েবল, যার জন্য কোনও মান অ্যাসাইন করা হয়নি বা ভ্যারিয়েবল ডিক্লেয়ার করা হয়েছে কিন্তু ইন্টারনালভাবে কোনও মান দেয়া হয়নি।

````js
let a;
console.log(a); // undefined

let b = null;
console.log(b); // null
````



#### 17. JavaScript-এ setTimeout() এবং setInterval() এর মধ্যে পার্থক্য কী?
* setTimeout(): এটি একটি নির্দিষ্ট সময় পরে শুধুমাত্র একবার একটি ফাংশন কল করে।
* setInterval(): এটি একটি নির্দিষ্ট সময়ের ইন্টারভালে বারবার একটি ফাংশন কল করে যতক্ষণ না সেটি বন্ধ করা হয়।
````js
setTimeout(() => {
    console.log('Executed after 2 seconds');
}, 2000);

const interval = setInterval(() => {
    console.log('Executed every 2 seconds');
}, 2000);

// Stop the interval after 6 seconds
setTimeout(() => clearInterval(interval), 6000);
````


#### 18. What are Higher-Order Functions in JavaScript?
* Higher-order function হলো এমন একটি ফাংশন, যা অন্য একটি ফাংশনকে আর্গুমেন্ট হিসেবে গ্রহণ করে বা অন্য একটি ফাংশনকে রিটার্ন করে।

````js
function higherOrderFunction(fn) {
    return function() {
        return fn();
    };
}

function sayHello() {
    return 'Hello!';
}

const hello = higherOrderFunction(sayHello);
console.log(hello()); // Hello!
````


#### 19. What is this keyword in JavaScript?

* this হলো একটি কিওয়ার্ড যা বর্তমানে যে অবজেক্টটি কনটেক্সট হিসেবে কাজ করছে সেটাকে নির্দেশ করে। this এর মান ফাংশনের ডিফাইনিং কনটেক্সট অনুযায়ী পরিবর্তিত হয়। এটি চারটি উপায়ে ব্যবহার করা যেতে পারে:
         * Global Context: এটি গ্লোবাল অবজেক্টকে নির্দেশ করে।
         * Method Context: এটি সেই অবজেক্টকে নির্দেশ করে, যেখানে ফাংশনটি মেথড হিসেবে কল হয়েছে।
         * Constructor Function: এটি নতুন অবজেক্টটিকে নির্দেশ করে।
         * Explicit Binding: call(), apply(), এবং bind() ব্যবহার করে this এর মান সেট করা যায়।


````js
const obj = {
    name: 'Alice',
    greet: function() {
        console.log(this.name);
    }
};

obj.greet(); // Alice
````



#### 21. What is the difference between splice() and slice() in JavaScript?
* splice(): এটি একটি অ্যারের নির্দিষ্ট অংশ মুছে দেয় এবং ঐ অংশের স্থানে নতুন এলিমেন্ট যোগ করে। এটি মূল অ্যারেটিকে পরিবর্তন করে।
* slice(): এটি একটি অ্যারের অংশকে কপি করে এবং নতুন অ্যারে রিটার্ন করে, কিন্তু মূল অ্যারেটিকে পরিবর্তন করে না।

````js
const arr = [1, 2, 3, 4, 5];

const splicedArr = arr.splice(2, 2); // [3, 4] (Removed elements)
console.log(arr); // [1, 2, 5] (Original array modified)

const slicedArr = arr.slice(1, 3); // [2, 5] (Copied elements)
console.log(arr); // [1, 2, 5] (Original array unchanged)
````


#### 23. What is the purpose of try...catch in JavaScript?
* try...catch ব্লক JavaScript-এ এরর হ্যান্ডলিংয়ের জন্য ব্যবহৃত হয়। যদি try ব্লকের মধ্যে কোনো এরর ঘটে, তাহলে সেটি catch ব্লকে ক্যাপচার করা হয় এবং এরর ম্যানেজ করা হয়।

````js
try {
    // Code that may throw an error
    let result = someUndefinedFunction();
} catch (error) {
    console.log('An error occurred:', error.message);
} finally {
    console.log('This will always run');
}
````


#### 24. What is the difference between synchronous and asynchronous programming in JavaScript?
* Synchronous Programming: সব কাজ সিকোয়েন্স অনুযায়ী একটির পর একটি এক্সিকিউট হয়, মানে একটি কাজ শেষ না হওয়া পর্যন্ত পরবর্তী কাজ শুরু হয় না।
* Asynchronous Programming: কিছু কাজের এক্সিকিউশন অন্য কাজের সাথে সমান্তরালে ঘটে, মানে কিছু কাজ শেষ হওয়ার অপেক্ষা না করে পরবর্তী কাজ শুরু হয়।

````js
console.log('Synchronous code start');
console.log('Synchronous code end');

console.log('Asynchronous code start');
setTimeout(() => {
    console.log('Asynchronous code inside setTimeout');
}, 1000);
console.log('Asynchronous code end');
````



#### 26. What is fetch() API in JavaScript?
* fetch() হলো একটি ব্রাউজার API যা HTTP অনুরোধ পাঠানোর জন্য ব্যবহৃত হয়। এটি একটি Promise রিটার্ন করে এবং অ্যাসিনক্রোনাস ভাবে ডেটা প্রসেস করে।

````js
fetch('https://api.example.com/data')
    .then(response => response.json())
    .then(data => console.log(data))
    .catch(error => console.log('Error:', error));
````




#### 28. What are let, const, and var in JavaScript, and how do they differ?

* var: ES5-এ ব্যবহৃত, এটি ফাংশন-স্কোপড এবং পুনঃঘোষণা করা যেতে পারে।
* let: ES6-এ পরিচিত, এটি ব্লক-স্কোপড এবং পুনঃঘোষণা করা সম্ভব নয় যদি একই স্কোপে হয়।
* const: ES6-এ পরিচিত, এটি ব্লক-স্কোপড এবং একবার মান নির্ধারণ করা হলে তা পরিবর্তন করা যায় না।

````js
var a = 1;
let b = 2;
const c = 3;

if (true) {
    var a = 4; // Changes the value of a globally
    let b = 5; // Scoped to this block
    const c = 6; // Scoped to this block
}

console.log(a); // 4
console.log(b); // 2
console.log(c); // 3
````

#### 33. What is the purpose of the debugger statement in JavaScript?
* debugger স্টেটমেন্ট কোড এক্সিকিউশন থামিয়ে ডিবাগার এপ্লিকেশন চালু করে, যা ডেভেলপারদের কোডের ত্রুটি সন্ধান এবং সংশোধনে সহায়ক।

````js
function testDebug() {
    let a = 1;
    debugger; // Execution will pause here
    let b = 2;
    console.log(a + b);
}

testDebug();
````

#### What is the bind() method in JavaScript?
* bind() মেথড একটি নতুন ফাংশন তৈরি করে যার this কিওয়ার্ড নির্দিষ্ট মানে সেট করা থাকে। এটি একটি ফাংশনের কনটেক্সট স্থির করতে ব্যবহৃত হয়।

````js
function greet() {
    console.log('Hello, ' + this.name);
}

const person = { name: 'Alice' };
const boundGreet = greet.bind(person);
boundGreet(); // Hello, Alice
````

#### What are JavaScript data types?
-  JavaScript-এর প্রধান ডেটা টাইপগুলো হলো:
* Primitive Types: undefined, null, boolean, number, string, symbol (ES6)
* Object Types: object, array, function

````js
let num = 10; // number
let str = 'Hello'; // string
let bool = true; // boolean
let arr = [1, 2, 3]; // array (object)
let obj = { name: 'Alice' }; // object

````


#### . What are JavaScript's built-in objects?
উত্তর: JavaScript-এ কিছু built-in objects রয়েছে যা বিভিন্ন কাজের জন্য ব্যবহৃত হয়, যেমন:
* Object: সাধারণ অবজেক্ট তৈরি করার জন্য।
* Array: অ্যারের ডেটা সংরক্ষণ ও পরিচালনার জন্য।
* Date: তারিখ ও সময় পরিচালনার জন্য।
* Math: গণনার জন্য মেথড এবং কনস্ট্যান্টস প্রদান করে।
* RegExp: রেগুলার এক্সপ্রেশন ম্যানিপুলেশনের জন্য।



####  What is localStorage and sessionStorage in JavaScript?
* localStorage: এটি ডেটা সংরক্ষণের জন্য ব্যবহৃত হয় যা ব্রাউজার বন্ধ করার পরও স্থায়ী থাকে। এটি বৃহৎ পরিমাণে ডেটা সংরক্ষণ করতে সক্ষম।
* sessionStorage: এটি ডেটা সংরক্ষণের জন্য ব্যবহৃত হয় যা শুধুমাত্র একটিভ সেশন (ব্রাউজার ট্যাব) চলাকালীন থাকে এবং ব্রাউজার ট্যাব বন্ধ হলে মুছে যায়।

````js
// Using localStorage
localStorage.setItem('key', 'value');
console.log(localStorage.getItem('key')); // value

// Using sessionStorage
sessionStorage.setItem('key', 'value');
console.log(sessionStorage.getItem('key')); // value
````



#### What is a “service worker” in JavaScript?
* Service worker হলো একটি স্ক্রিপ্ট যা ব্রাউজারের ব্যাকগ্রাউন্ডে চলতে পারে এবং নেটওয়ার্ক রিকোয়েস্ট, কেশিং, এবং অফলাইন ফাংশনালিটি পরিচালনা করতে সহায়ক। এটি মূলত প্রগ্রাম্যাটিক্যালি কাজ করে এবং পুশ নোটিফিকেশন, কেশিং, ও অফলাইন সাপোর্টের জন্য ব্যবহৃত হয়।


####  What is the new keyword in JavaScript?
* new কিওয়ার্ড একটি নতুন অবজেক্ট তৈরি করে এবং এটি কনস্ট্রাকটর ফাংশনকে কল করে। এটি নতুন ইনস্ট্যান্স তৈরি করার জন্য ব্যবহৃত হয় এবং কনস্ট্রাকটর ফাংশনের ভিতরে থাকা প্রপার্টি ও মেথডগুলি ইনস্ট্যান্সে অ্যাসাইন করে।

````js
function Person(name) {
    this.name = name;
}

const person = new Person('Alice');
console.log(person.name); // Alice
````


#### What is the rest parameter in JavaScript?
* উত্তর: rest প্যারামিটার (...) ফাংশনের আর্গুমেন্টগুলির একটি অপরিচিত সংখ্যা সংগ্রহ করতে ব্যবহৃত হয় এবং এটি একটি অ্যারে হিসেবে পাস করা হয়।

````js
function sum(...numbers) {
    return numbers.reduce((total, num) => total + num, 0);
}

console.log(sum(1, 2, 3, 4)); // 10
````
#### What is the constructor function in JavaScript classes?
* উত্তর: constructor হলো একটি বিশেষ মেথড যা একটি নতুন অবজেক্ট তৈরি করার সময় স্বয়ংক্রিয়ভাবে কল হয়। এটি ক্লাসের ইনস্ট্যান্সের প্রাথমিক স্টেট সেটআপ করতে ব্যবহৃত হয়।

````js
class Person {
    constructor(name) {
        this.name = name;
    }

    greet() {
        console.log(`Hello, ${this.name}`);
    }
}

const person = new Person('Alice');
person.greet(); // Hello, Alice
````



#### What is Array.prototype.every() method in JavaScript?
উত্তর: every() মেথড একটি অ্যারের প্রতিটি উপাদান একটি নির্দিষ্ট শর্ত পূরণ করে কিনা তা যাচাই করে এবং যদি হয় তবে true রিটার্ন করে।

````js
const numbers = [2, 4, 6, 8];
const allEven = numbers.every(num => num % 2 === 0);
console.log(allEven); // true
````




## =====================================================================================================

## PHP

#### Encapsulation
- Encapsulation হলো Object-Oriented Programming (OOP)-এর একটি গুরুত্বপূর্ণ নীতি। PHP-তে encapsulation বলতে ডেটা (যেমন ভ্যারিয়েবল) এবং ঐ ডেটার ওপর কার্যকরী মেথডগুলোকে একসাথে একটি ইউনিট বা ক্লাসে বেঁধে রাখা বোঝায়, যেখানে কিছু উপাদানের অ্যাক্সেস সীমিত রাখা হয়। এর ফলে অবজেক্টের অভ্যন্তরীণ অবস্থা সুরক্ষিত থাকে এবং এর ডেটা শুধুমাত্র নির্দিষ্ট মেথডের মাধ্যমে পরিবর্তন করা যায়।

###### Access Modifiers:

* public: প্রপার্টি বা মেথড যেকোনো জায়গা থেকে অ্যাক্সেস করা যায়, অর্থাৎ ক্লাসের ভিতরে বা বাইরে।
* private: প্রপার্টি বা মেথড শুধুমাত্র ঐ ক্লাসের ভিতরে অ্যাক্সেস করা যায়।
* protected: প্রপার্টি বা মেথড শুধুমাত্র ক্লাস এবং এর child class (উত্তরাধিকারী ক্লাস) এর ভিতর থেকে অ্যাক্সেস করা যায়।


###### Getters এবং Setters:

* Getters এবং setters হলো মেথড, যেগুলোর মাধ্যমে private বা protected প্রপার্টিগুলো ক্লাসের বাইরে থেকেও অ্যাক্সেস বা পরিবর্তন করা যায়। এর মাধ্যমে ডেটার উপরে নিয়ন্ত্রণ রাখা হয় এবং প্রয়োজনীয় যাচাই-বাছাই করা সম্ভব হয়।

````php
<?php
class Product {
    private $name;
    private $price;

    // Constructor দিয়ে ভ্যালু initialize করা
    public function __construct($name, $price) {
        $this->name = $name;
        $this->price = $price;
    }

    // Name-এর getter
    public function getName() {
        return $this->name;
    }

    // Name-এর setter
    public function setName($name) {
        $this->name = $name;
    }

    // Price-এর getter
    public function getPrice() {
        return $this->price;
    }

    // Price-এর setter, যেখানে validation আছে
    public function setPrice($price) {
        if ($price > 0) {
            $this->price = $price;
        } else {
            echo "মূল্য অবশ্যই পজিটিভ সংখ্যা হতে হবে!";
        }
    }
}

// Product ক্লাসের একটি অবজেক্ট তৈরি করা
$product = new Product("Laptop", 1200);

// Getter এবং Setter ব্যবহার করে প্রপার্টি অ্যাক্সেস ও পরিবর্তন করা
echo $product->getName();  // আউটপুট: Laptop
$product->setPrice(1500);  // মূল্যে পরিবর্তন করে 1500 করা হলো
echo $product->getPrice(); // আউটপুট: 1500

$product->setPrice(-500);  // আউটপুট: মূল্য অবশ্যই পজিটিভ সংখ্যা হতে হবে!
?>
````



#### Inheritance
* Inheritance হল Object-Oriented Programming (OOP)-এর একটি মৌলিক ধারণা, যা একটি ক্লাসকে অন্য একটি ক্লাসের বৈশিষ্ট্য ও আচরণ উত্তরাধিকারসূত্রে গ্রহণ করার অনুমতি দেয়। PHP-তে inheritance ব্যবহার করে, আপনি একটি ক্লাস থেকে অন্য ক্লাস তৈরি করতে পারেন যা পূর্বের ক্লাসের (parent class) প্রপার্টি ও মেথডগুলিকে ধার নিতে পারে। এইভাবে কোড পুনঃব্যবহার করা সহজ হয় এবং ক্লাসগুলোর মধ্যে সম্পর্ক স্থাপন করা যায়।


* Parent Class: যেই ক্লাস থেকে অন্য ক্লাস বৈশিষ্ট্য ও আচরণ উত্তরাধিকারসূত্রে গ্রহণ করে, তাকে parent class বা base class বলা হয়।
* Child Class: যেই ক্লাস parent class থেকে বৈশিষ্ট্য ও আচরণ গ্রহণ করে, তাকে child class বা derived class বলা হয়।

````php
<?php
// Parent Class
class Animal {
    public $name;

    // Constructor
    public function __construct($name) {
        $this->name = $name;
    }

    // Method
    public function speak() {
        return "I am an animal.";
    }
}

// Child Class
class Dog extends Animal {
    // Overriding method
    public function speak() {
        return "Woof! I am a dog.";
    }

    // Additional method
    public function fetch() {
        return "Fetching the ball!";
    }
}

// Creating an object of Dog class
$dog = new Dog("Buddy");

// Accessing properties and methods
echo $dog->name;          // Output: Buddy
echo $dog->speak();       // Output: Woof! I am a dog.
echo $dog->fetch();       // Output: Fetching the ball!
?>
````


#### Polymorphism
Polymorphism হল Object-Oriented Programming (OOP)-এর একটি গুরুত্বপূর্ণ নীতি যা একই নামের মেথড বা অপারেটরকে বিভিন্ন ধরণের আর্গুমেন্ট বা অবজেক্টের সাথে বিভিন্নভাবে আচরণ করতে দেয়। এটি দুটি প্রধান ধরনের হয়ে থাকে:


* Method Overloading (PHP তে প্রকৃতপক্ষে সমর্থিত নয়, কিন্তু ধারণাটি বোঝানো যেতে পারে): একই নামের একাধিক মেথড কিন্তু বিভিন্ন পরামিতি লিস্টের সাথে।
* Method Overriding: একটি child class প্যারেন্ট ক্লাসের মেথডকে নতুনভাবে বাস্তবায়ন করা।

###### Method Overloading (PHP তে সীমিত)
* PHP তে মেথড ওভারলোডিং সরাসরি সমর্থিত নয়, কারণ PHP-তে একই নামের একাধিক মেথড তৈরি করা যায় না। তবে, আপনি প্যারামিটার সংখ্যা বা ধরন অনুযায়ী বিভিন্ন আচরণ তৈরির জন্য কন্ডিশনাল লজিক ব্যবহার করতে পারেন।

###### Method Overriding (PHP তে সাধারণত ব্যবহৃত)
* Method overriding এ child class প্যারেন্ট ক্লাসের মেথডকে পুনরায় সংজ্ঞায়িত করে নতুন আচরণ প্রদান করতে পারে।
````php
<?php
// Parent Class
class Shape {
    public function draw() {
        return "Drawing a shape.";
    }
}

// Child Class
class Circle extends Shape {
    // Method Overriding
    public function draw() {
        return "Drawing a circle.";
    }
}

// Another Child Class
class Square extends Shape {
    // Method Overriding
    public function draw() {
        return "Drawing a square.";
    }
}

// Function to display shape drawing
function displayDrawing(Shape $shape) {
    echo $shape->draw();
}

// Creating objects
$circle = new Circle();
$square = new Square();

// Using polymorphism
displayDrawing($circle); // Output: Drawing a circle.
displayDrawing($square); // Output: Drawing a square.
?>
````


#### Abstraction
* Abstraction হল Object-Oriented Programming (OOP)-এর একটি মূল নীতি যা জটিলতাকে লুকিয়ে রেখে শুধুমাত্র প্রয়োজনীয় বৈশিষ্ট্য ও আচরণ প্রকাশ করে। এটি মূলত ব্যবহারকারীদের জটিলতা বা অপ্রয়োজনীয় বিবরণ থেকে মুক্ত রেখে তাদের কেবল গুরুত্বপূর্ণ তথ্য প্রদান করে।


###### Abstraction-এর মূল বৈশিষ্ট্য:
* Abstract Classes: এমন ক্লাস যা সম্পূর্ণভাবে বাস্তবায়িত নয়, সাধারণত শুধুমাত্র কিছু অংশের বাস্তবায়ন থাকে এবং অন্য অংশগুলি সাবক্লাসগুলির দ্বারা বাস্তবায়িত হয়।
* Abstract Methods: এসব মেথড কোনো বাস্তবায়ন প্রদান করে না; এগুলোর বাস্তবায়ন সাবক্লাসে প্রদান করা হয়।


````php
<?php
// Abstract Class
abstract class Vehicle {
    // Abstract Method (does not have a body)
    abstract public function start();

    // Regular Method
    public function stop() {
        return "Stopping the vehicle.";
    }
}

// Subclass (inheriting from Abstract Class)
class Car extends Vehicle {
    // Implementing the abstract method
    public function start() {
        return "Starting the car.";
    }
}

// Another Subclass
class Bike extends Vehicle {
    // Implementing the abstract method
    public function start() {
        return "Starting the bike.";
    }
}

// Creating objects of subclasses
$car = new Car();
$bike = new Bike();

// Using the methods
echo $car->start(); // Output: Starting the car.
echo $car->stop();  // Output: Stopping the vehicle.

echo $bike->start(); // Output: Starting the bike.
echo $bike->stop();  // Output: Stopping the vehicle.
?>
````


###### Abstract Class (Vehicle):

* Abstract Method (start()): এটি কোনো বাস্তবায়ন প্রদান করে না; এটি সাবক্লাসে বাস্তবায়িত হতে হবে।
* Regular Method (stop()): এটি একটি সম্পূর্ণভাবে বাস্তবায়িত মেথড যা সকল সাবক্লাসে ব্যবহার করা যেতে পারে।

###### Subclasses (Car, Bike):
* Abstract Method Implementation: Car এবং Bike ক্লাসগুলি Vehicle ক্লাসের start() মেথডকে বাস্তবায়িত করেছে।
* Regular Method Usage: stop() মেথডটি Vehicle ক্লাস থেকে উত্তরাধিকারসূত্রে প্রাপ্ত এবং সাবক্লাসগুলিতে ব্যবহার করা হয়েছে।





















