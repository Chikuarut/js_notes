# 1. JavaScript Fundamentals Part 1
---

## 1.  Hello World
```js
console.log("Hello World!")
```

## 2. A brief introduction to Javascript

_JavaScript_ was initially created to “make web pages alive”.

The programs in this language are called _scripts_. They can be written right in a web page’s HTML and run automatically as the page loads.

Scripts are provided and executed as plain text. They don’t need special preparation or compilation to run.

## 3. Linking a JavaScript File

 ```js
let js = "amazing";
console.log(40 + 8 + 23 - 10);
```


##  4. Values and Variables

```js
console.log("xoraus");
console.log(23);

let firstName = "Matilda";

console.log(firstName);
console.log(firstName);
console.log(firstName);
```

5. ## Variable name conventions

```js
let xoraus_matilda = "JM";
let $function = 27;

let person = "xoraus";
let PI = 3.1415;

let myFirstJob = "Coder";
let myCurrentJob = "Teacher";

let job1 = "programmer";
let job2 = "teacher";

console.log(myFirstJob);
```

## 6. Data Types

```js
let javascriptIsFun = true;
console.log(javascriptIsFun);

console.log(typeof true);
console.log(typeof javascriptIsFun);
console.log(typeof 23);
console.log(typeof 'xoraus');

javascriptIsFun = 'YES!';
console.log(typeof javascriptIsFun);

let year;

console.log(year);
console.log(typeof year);

year = 1991;

console.log(typeof year);
console.log(typeof null);  

let, const and var // us let when you're sure that the vaule will change in future

// let is block scoped
// VAR is function-scoped

let age = 30;
age = 31; // here let (age) is mutable

const birthYear = 1991; // it is immutable
birthYear = 1990;

const job; // this will throw an error;  
var job = 'programmer'; // used in legacy codebases

job = 'teacher'


lastName = 'Ahmed';
console.log(lastName);
```

## 7. Basic Operators

###### Math operators

```js
const now = 2037;
const ageXoraus = now - 1991;
const ageSarah = now - 2018;

console.log(ageXoraus, ageSarah);
console.log(ageXoraus * 2, ageXoraus 10, 2 ** 3);

// 2 ** 3 means 2 to the power of 3 = 2 * 2 * 2

const firstName = 'xoraus';
const lastName = 'Ahmed';

console.log(firstName + ' ' + lastName);
```
###### Assignment operators

```js
let x = 10 + 5; // output: 15

x += 10; // x = x + 10 - Output: 25

x *= 4; // x = x * 4 - Output: 100

x++; // x = x + 1
x--; // x = x - 1
x--;

console.log(x);
```

###### Comparison operators

```js
console.log(ageXoraus > ageSarah); //  >, <, >=, <=
console.log(ageSarah >= 18);  // Output: true

const isFullAge = ageSarah >= 18;

console.log(now - 1991 > now - 2018);
```

## 8. Operator Precedence

```js
const now = 2037;
const ageXoraus = now - 1991;
const ageSarah = now - 2018;

console.log(now - 1991 > now - 2018);

let x, y;

x = y = 25 - 10 - 5; // Output: x = y = 10, x = 10 - Assignment works from right to left

console.log(x, y);

const averageAge = (ageXoraus + ageSarah) 2;

console.log(ageXoraus, ageSarah, averageAge);
```

## 9. Coding Challenge ##1

Mark and John are trying to compare their BMI (Body Mass Index), which is calculated using the formula: BMI = mass / height ** 2 = mass / (height * height). (mass in kg and height in meter).

1. Store Mark's and John's mass and height in variables
2. Calculate both their BMIs using the formula (you can even implement both versions)
3. Create a boolean variable 'markHigherBMI' containing information about whether Mark has a higher BMI than John.

- TEST DATA 1: Marks weights 78 kg and is 1.69 m tall. John weights 92 kg and is 1.95 m tall.
- TEST DATA 2: Marks weights 95 kg and is 1.88 m tall. John weights 85 kg and is 1.76 m tall.

**My Solution**
```js
const markMass = 78;
const markHeight = 1.69;

const johnMass = 92;
const johnHeight = 1.95;

function calculateBMI(mass, height) {
	let BMI;
	BMI = mass / height ** 2;
	return BMI
}

const markBMI = calculateBMI(markMass,markHeight);
const johnBMI = calculateBMI(johnMass, johnHeight);
const markHigherBMI =  markBMI > johnBMI
console.log(markBMI)
console.log(johnBMI)
console.log(markHigherBMI)
```

**Solution by xoraus**

```js
const massMark = 78;
const heightMark = 1.69;

const massJohn = 92;
const heightJohn = 1.95;

const massMark = 95;
const heightMark = 1.88;

const massJohn = 85;
const heightJohn = 1.76;

const BMIMark = massMark heightMark ** 2;
const BMIJohn = massJohn (heightJohn * heightJohn);

const markHigherBMI = BMIMark > BMIJohn;

console.log(BMIMark, BMIJohn, markHigherBMI);
```

 ## 10. Strings and Template Literals

```js
const firstName = 'xoraus';
const job = 'teacher';

const birthYear = 1991;
const year = 2037;

const xoraus = "I'm " + firstName + ', a ' + (year - birthYear) + ' year old ' + job + '!'; // concept of type coercion

console.log(xoraus);

const xorausNew = `I'm ${firstName}, a ${year - birthYear} year old ${job}!`; // one of most used ES6 Feature :)

console.log(xorausNew);

console.log(`Just a regular string...`);
  
console.log('String with \n\
multiple \n\
lines');

console.log(`String
multiple
lines`);
```

## 11. Taking Decisions: if else Statements

```js
const age = 15;
if (age >= 18) {
  console.log('Sarah can start driving license 🚗');
} else {
  const yearsLeft = 18 - age;
  console.log(`Sarah is too young. Wait another ${yearsLeft} years :)`);
}

const birthYear = 2012;

let century;
if (birthYear <= 2000) {
  century = 20;
} else {
  century = 21;
}
console.log(century);
```

## 12. Coding Challenge ##2

Use the BMI example from Challenge ##1, and the code you already wrote, and improve it:

1. Print a nice output to the console, saying who has the higher BMI. The message can be either "Mark's BMI is higher than John's!" or "John's BMI is higher than Mark's!"
2. Use a template literal to include the BMI values in the outputs. Example: "Mark's BMI (28.3) is higher than John's (23.9)!"

**My Solution**

```js
const markMass = 78;
const markHeight = 1.69;

const johnMass = 92;
const johnHeight = 1.95;

function calculateBMI(mass, height) {
	let BMI;
	BMI = mass / height ** 2;
	return BMI
}

const markBMI = calculateBMI(markMass,markHeight);
const johnBMI = calculateBMI(johnMass, johnHeight);

// console.log(`BMI of Mark is ${markBMI}`)
// console.log(`BMI of John is ${johnBMI}`)
// console.log(`Does Mark has higher BMI - ${markHigherBMI}`)

if (markBMI > johnBMI) {
	console.log(`Mark's BMI (${markBMI}) is higher than John's (${johnBMI})!`)
} else {
	console.log(`John's BMI (${johnBMI}) is higher than Marks's (${markBMI})!`)
}
```

**Another Solution**

```js
const massMark = 78;
const heightMark = 1.69;

const massJohn = 92;
const heightJohn = 1.95;


const massMark = 95;
const heightMark = 1.88;

const massJohn = 85;
const heightJohn = 1.76;

const BMIMark = massMark heightMark ** 2;
const BMIJohn = massJohn (heightJohn * heightJohn);

console.log(BMIMark, BMIJohn);

if (BMIMark > BMIJohn) {
	console.log(`Mark's BMI (${BMIMark}) is higher than John's (${BMIJohn})!`)
} else {
	console.log(`John's BMI (${BMIJohn}) is higher than Marks's (${BMIMark})!`)
}
```

##  13. Type Conversion and Coercion
```js
// type conversion - type conversion is when we manuallyconvert from one type to another.

const inputYear = '1991';

console.log(Number(inputYear), inputYear);
console.log(Number(inputYear) + 18);

console.log(Number('xoraus')); // Outuput: NaN (Not a Number - it actually means invalid number)
console.log(typeof NaN); // output: number

console.log(String(23), 23); // String(23) is a string; 23 is a number

// type coercion - type coercion is when JavaScript automatically converts types behind the scenes for us.
// So basically, type coercion happens whenever an operator is dealing with two values that have different types.


console.log('I am ' + 23 + ' years old'); // output: I am 23 years old. Since Javascript has type coercion, the number will be automatically be converted into string.
console.log('23' - '10' - 3); // output: Here the strings are converted to numbers because of (- minus) operator.
console.log('23' * '2'); // strings are converted to numbers
console.log('23' / '2'); // strings are converted to numbers

let n = '1' + 1; // String - '11'
n = n - 1; // String 11 will be converted to number 11 then 11 - 1 = 10

console.log(n); // 10

console.log(2+3+4+'5') // output: 95 as string ; 9 + '5' → 95
console.log('10'-'4'-'3'-2 +'5') // output: 15 as string ;  1 + '5' → 15

```

## 14. Truthy and Falsy Values

```js
// In javascript there are 5 falsy values: 0, '', undefined, null, NaN
console.log(Boolean(0)); // output: false
console.log(Boolean(undefined)); // output: false
console.log(Boolean('Jonas')); // output: true
console.log(Boolean({})); // output: true
console.log(Boolean('')); // output:  false

const money = 100;
if (money) {
  console.log("Don't spend it all ;)");
} else {
  console.log('You should get a job!');
}

let height = 0; 
if (height) { 
  console.log('YAY! Height is defined');
} else {
  console.log('Height is UNDEFINED'); // this will be the ouput because 0 is a falsy value. But this is a bug because we have defined height as 0. We can fix this using logical operators.
}
```
So in practice, the conversion to boolean is always implicit, not explicit, or in other words is always typed coercion that JavaScript does automatically behind the scenes.

But when exactly does JavaScript do type coercion to booleans? Well, it happens in two scenarios. First, when using logical operators, and Second in logical context, like for example, in the condition of an if else statement.

## 15. Equality Operators: == vs. ===

```js
const age = '18';
if (age === 18) console.log('You just became an adult :D (strict)'); // output: true (strict equality doesn't perform type coercion)
if (age == 18) console.log('You just became an adult :D (loose)'); // Lose equality does the type coercion therefore output: true (the string '18' will be converted to number before checking) 

const favourite = Number(prompt("What's your favourite number?"));
console.log(favourite);
console.log(typeof favourite);

if (favourite === 23) { // 22 === 23 -> FALSE
  console.log('Cool! 23 is an amzaing number!')
} else if (favourite === 7) {
  console.log('7 is also a cool number')
} else if (favourite === 9) {
  console.log('9 is also a cool number')
} else {
  console.log('Number is not 23 or 7 or 9')
}

if (favourite !== 23) console.log('Why not 23?');
```
So as a general rule for clean code, avoid the loose equality operator as much as you can. So when comparing values, always use strict equality with the three equal signs,

## 16. Logical Operators

```js
const hasDriversLicense = true; // A
const hasGoodVision = true; // B

console.log(hasDriversLicense && hasGoodVision); // output: true
console.log(hasDriversLicense || hasGoodVision); // output: true
console.log(!hasDriversLicense); // output: false

// if (hasDriversLicense && hasGoodVision) {
//   console.log('Sarah is able to drive!');
// } else {
//   console.log('Someone else should drive...');
// }

const isTired = false; // C
console.log(hasDriversLicense && hasGoodVision && isTired); output: false

if (hasDriversLicense && hasGoodVision && !isTired) {
  console.log('Sarah is able to drive!'); 
} else {
  console.log('Someone else should drive...');
}
// output: Sarah is able to drive! 
```

The NOT operator actually has proceedings over the OR and AND operators.

## 17. Coding Challenge ##3

There are two gymnastics teams, Dolphins and Koalas. They compete against each other 3 times. The winner with the highest average score wins the a trophy!
1. Calculate the average score for each team, using the test data below
2. Compare the team's average scores to determine the winner of the competition, and print it to the console. Don't forget that there can be a draw, so test for that as well (draw means they have the same average score).
3. BONUS 1: Include a requirement for a minimum score of 100. With this rule, a team only wins if it has a higher score than the other team, and the same time a score of at least 100 points. HINT: Use a logical operator to test for minimum score, as well as multiple else-if blocks 😉
4. BONUS 2: Minimum score also applies to a draw! So a draw only happens when both teams have the same score and both have a score greater or equal 100 points. Otherwise, no team wins the trophy.

TEST DATA: Dolphins score 96, 108 and 89. Koalas score 88, 91 and 110
TEST DATA BONUS 1: Dolphins score 97, 112 and 101. Koalas score 109, 95 and 123
TEST DATA BONUS 2: Dolphins score 97, 112 and 101. Koalas score 109, 95 and 106

**My Solution**

```js
const scoreDolphins = (96 + 108 + 89) / 3;
const scoreKoalas = (88 + 91 + 110) / 3;

console.log(scoreDolphins, scoreKoalas);

if (scoreDolphins > scoreKoalas) {
	console.log('Dolphins win the trophy 🏆');
} else if (scoreKoalas > scoreDolphins) {
	console.log('Koalas win the trophy 🏆');
} else if (scoreDolphins === scoreKoalas) {
	console.log('Both win the trophy!');
}
```

BONUS 1

```js
const scoreDolphins = (97 + 112 + 80) 3;
const scoreKoalas = (109 + 95 + 50) 3;

console.log(scoreDolphins, scoreKoalas);

if (scoreDolphins > scoreKoalas && scoreDolphins >= 100) {
	console.log('Dolphins win the trophy 🏆');
} else if (scoreKoalas > scoreDolphins && scoreKoalas >= 100) {
	console.log('Koalas win the trophy 🏆');
} else if (scoreDolphins === scoreKoalas && scoreDolphins >= 100 && scoreKoalas >= 100) {
console.log('Both win the trophy!');
} else {
console.log('No one wins the trophy 😭');
}
```

## 18. The switch Statement
```js
const day = 'friday';

switch (day) {
  case 'monday': // day === 'monday'
    console.log('Plan course structure');
    console.log('Go to coding meetup');
    break;
  case 'tuesday':
    console.log('Prepare theory videos');
    break;
  case 'wednesday':
  case 'thursday':
    console.log('Write code examples');
    break;
  case 'friday':
    console.log('Record videos');
    break;
  case 'saturday':
  case 'sunday':
    console.log('Enjoy the weekend :D');
    break;
  default:
    console.log('Not a valid day!');
}

if (day === 'monday') {
  console.log('Plan course structure');
  console.log('Go to coding meetup');
} else if (day === 'tuesday') {
  console.log('Prepare theory videos');
} else if (day === 'wednesday' || day === 'thursday') {
  console.log('Write code examples');
} else if (day === 'friday') {
  console.log('Record videos');
} else if (day === 'saturday' || day === 'sunday') {
  console.log('Enjoy the weekend :D');
} else {
  console.log('Not a valid day!');
}
```  

## 19. Statements and Expressions
```js
3 + 4 // output: 7 - an expression
1991
true && false && !false

// Following is a Statement
if (50 > 10) {
  const str = '50 is bigger';
}

const me = 'Xoraus';
console.log(`I'm ${2050 - 1997} years old ${me}`); // In javascript literals we can use expressions but not statements.
```  

- an expression is a piece of code that produces a value.
- statements are like full sentences that translate our actions.

## 20. The Conditional (Ternary) Operator
```js
const age = 23;
// age >= 18 ? console.log('I like to drink wine 🍷') : console.log('I like to drink water 💧');

const drink = age >= 18 ? 'Sharbat-e-Jaam 🍷' : 'water 💧';
console.log(drink);

let drink2;
if (age >= 18) {
  drink2 = 'Sharbat-e-Jaam 🍷';
} else {
  drink2 = 'water 💧';
}
console.log(drink2);

console.log(`I like to drink ${age >= 18 ? 'Sharbat-e-Jaam 🍷' : 'water 💧'}`);
```
  
## 21. Coding Challenge ##4

Steven wants to build a very simple tip calculator for whenever he goes eating in a restaurant. In his country, it's usual to tip 15% if the bill value is between 50 and 300. If the value is different, the tip is 20%.
1. Your task is to calculate the tip, depending on the bill value. Create a variable called 'tip' for this. It's not allowed to use an if else statement 😅 (If it's easier for you, you can start with an if else statement, and then try to convert it to a ternary operator!)
2. Print a string to the console containing the bill value, the tip, and the final value (bill + tip). Example: 'The bill was 275, the tip was 41.25, and the total value 316.25'

TEST DATA: Test for bill values 275, 40 and 430  

HINT: To calculate 20% of a value, simply multiply it by 20/100 = 0.2
HINT: Value X is between 50 and 300, if it's >= 50 && <= 300 😉

```js
const bill = 275;
const tip = (bill >= 50 && bill <= 300) ? 0.15 * bill : 0.20 * bill;

const totalValue = bill + tip;

console.log(`The bill was ${bill}, the tip was ${tip}, and the total value ${bill + tip}`);
```





29




JS --------------------------------------------------------------------------------------------------22222222222222222222222222222222222222222222222222222222222222





# 2. JavaScript Fundamentals Part 2
---
## 32. Activating Strict Mode
```js
'use strict'; // to activate strict mode to 
```
- Always put strict mode in the beginning of the file
- It makes it easier for developer to avoid accidental errors.

First, strict mode forbids us to do certain things and second, it will actually create visible errors for us in certain situations in which without strict mode JavaScript will simply fail silently without letting us know that we did a mistake.
```js
'use strict';

let hasDriversLicense = false;
const passTest = true;

if (passTest) hasDriversLicense = true; // if in  hasDriver(s)License s is missing the code will behave  unexpectedly
if (hasDriversLicense) console.log('I can drive :D');

// const interface = 'Audio'; // Uncaught SyntaxError: Missing initializer in const declaration
// const private = 534; // Uncaught SyntaxError: Missing initializer in const declaration
```

## 33. Functions
```js
function logger() {
  console.log('My name is xoraus');
}

// calling / running / invoking function
logger(); // output: My name is xoraus
logger(); // output: My name is xoraus
logger(); // output: My name is xoraus

function fruitProcessor(apples, oranges) {
  const juice = `Juice with ${apples} apples and ${oranges} oranges.`;
  return juice;
}

const appleJuice = fruitProcessor(10, 5);
console.log(appleJuice);1

const appleOrangeJuice = fruitProcessor(4, 8);
console.log(appleOrangeJuice);

const num = Number('6833');
```

Clean Code - **DRY Principle** that is _Don't Repeat Yourself_ 

## 34. Function Declarations vs. Expressions

```js
// Function declaration
function calcAge1(birthYeah) {
  return 2047 - birthYeah;
}
const age1 = calcAge1(1997);
// Function expression
const calcAge2 = function (birthYeah) { // Anonymous Functions - this function is an expression. Expressions produce value.
  return 2047 - birthYeah;
}
const age2 = calcAge2(1997);

console.log(age1, age2);
```
- The parameter is a kind of placeholder in the function and the argument is then the actual value that we use to fill in that placeholder that is the parameter.
- In Javascript functions are just values

## 35. Arrow Functions
```js
const calcAge3 = birthYeah => 2047 - birthYeah;
const age3 = calcAge3(1997);
console.log(age3);

const yearsUntilRetirement = (birthYeah, firstName) => {
  const age = 2047 - birthYeah;
  const retirement = 65 - age;
  // return retirement;
  return `${firstName} retires in ${retirement} years`;
}

console.log(yearsUntilRetirement(1997, 'xoraus')); console.log(yearsUntilRetirement(2005, 'ahmed'));
```

## 36. Functions Calling Other Functions
```js
function cutFruitPieces(fruit) {
  return fruit * 4;
}

function fruitProcessor(apples, oranges) {
  const applePieces = cutFruitPieces(apples);
  const orangePieces = cutFruitPieces(oranges);

  const juice = `Juice with ${applePieces} piece of apple and ${orangePieces} pieces of orange.`;
  return juice;
}
console.log(fruitProcessor(2, 3));
```

- Arrow functions do not get the **this Keyword**

## 37. Reviewing Functions
```js
const calcAge = function (birthYeah) {
  return 2047 - birthYeah;
}

const yearsUntilRetirement = function (birthYeah, firstName) {
  const age = calcAge(birthYeah);
  const retirement = 65 - age;

  if (retirement > 0) {
    console.log(`${firstName} retires in ${retirement} years`);
    return retirement;
  } else {
    console.log(`${firstName} has already retired 🎉`);
    return -1;
  }
}

console.log(yearsUntilRetirement(1997, 'xoraus'));
console.log(yearsUntilRetirement(1980, 'Jordan'));
```
![[2. JavaScript Fundamentals Part 2-20220824162950.png]]

## 38. Coding Challenge 1
Back to the two gymnastics teams, the Dolphins and the Koalas! There is a new gymnastics discipline, which works differently. Each team competes 3 times, and then the average of the 3 scores is calculated (so one average score per team). A team ONLY wins if it has at least DOUBLE the average score of the other team. Otherwise, no team wins!

1. Create an arrow function 'calcAverage' to calculate the average of 3 scores
2. Use the function to calculate the average for both teams
3. Create a function 'checkWinner' that takes the average score of each team as parameters ('avgDolhins' and 'avgKoalas'), and then logs the winner to the console, together with the victory points, according to the rule above. Example: "Koalas win (30 vs. 13)".
4. Use the 'checkWinner' function to determine the winner for both DATA 1 and DATA 2.
5. Ignore draws this time.

TEST DATA 1: Dolphins score 44, 23 and 71. Koalas score 65, 54 and 49
TEST DATA 2: Dolphins score 85, 54 and 41. Koalas score 23, 34 and 27

HINT: To calculate average of 3 values, add them all together and divide by 3
HINT: To check if number A is at least double number B, check for A >= 2 * B. Apply this to the team's average scores 😉

```js
calcAverage = (scoreA, scoreB, scoreC) => (scoreA, scoreB, scoreC) / 3

const teamDolphinAvg = Math.floor(calcAverage(85,54,41));
const teamKoalaAvg = Math.floor(calcAverage(23,34,27));

console.log(teamDolphinAvg,teamKoalaAvg)

function checkWinner(teamDolphinAvg,teamKoalaAvg) {
 if (teamDolphinAvg >= 2 * teamKoalaAvg) {
	 console.log(`Dolphins win 🏆 ${teamDolphinAvg} vs ${teamKoalaAvg}`)
 } else if (teamKoalaAvg >= 2 * teamDolphinAvg) {
	 console.log(`Koalas win 🏆 ${teamKoalaAvg} vs. ${teamDolphinAvg}`)
 } else {
	 console.log(`No body won :(`)
 }
}

checkWinner(800,351)

// Test 2
scoreDolphins = calcAverage(85, 54, 41);
scoreKoalas = calcAverage(23, 34, 27);
console.log(scoreDolphins, scoreKoalas);
checkWinner(scoreDolphins, scoreKoalas);

```


## 39. Introduction to Arrays
```js
const friend1 = 'Al-Farabi';
const friend2 = 'Al-Ghazali';
const friend3 = 'Al- Razi';

const friends = ['Al-Farabi', 'Al-Ghazali', 'Al- Razi'];
console.log(friends);

const y = new Array(1991, 1984, 2008, 2020);

console.log(friends[0]); // output: Al-Farabi
console.log(friends[2]); // output: Al- Razi

console.log(friends.length); // outpt: 3
console.log(friends[friends.length - 1]); // output: Peter

friends[3] = 'Al-Qalbi';
console.log(friends); // output: Al-Farabi, Al-Ghazali, Al- Razi
// friends = ['Bob', 'Alice']

const firstName = 'Jordan';
const xoraus = [firstName, 'Ahmed', 2047 - 1997, 'teacher', friends];
console.log(xoraus);
console.log(xoraus.length);

// Exercise
const calcAge = function (birthYeah) {
  return 2047 - birthYeah;
}
const years = [1990, 1967, 2002, 2010, 2018];

const age1 = calcAge(years[0]);
const age2 = calcAge(years[1]);
const age3 = calcAge(years[years.length - 1]);
console.log(age1, age2, age3);

const ages = [calcAge(years[0]), calcAge(years[1]), calcAge(years[years.length - 1])];
console.log(ages);
```

## 40. Basic Array Operations (Methods)
```js
const friends = ['Al-Farabi', 'Al-Ghazali', 'Al- Razi'];
// const friends = ['Michael', 'Steven', 'Peter'];

// Add elements
const newLength = friends.push('xoraus');
console.log(friends);
console.log(newLength);

friends.unshift('Jordan');
console.log(friends);

// Remove elements
friends.pop(); // Last
const popped = friends.pop();
console.log(popped);
console.log(friends);

friends.shift(); // First
console.log(friends);

console.log(friends.indexOf('Al-Farabi'));
console.log(friends.indexOf('Al-Ghazali'));

friends.push(25);
console.log(friends.includes('Al- Razi'));
console.log(friends.includes('Ahmed'));
console.log(friends.includes(25));

if (friends.includes('Al-Ghazali')) {
  console.log('You have a friend called Al-Ghazali');
}
```

## 41. Coding Challenge ##2
Ahmed is still building his tip calculator, using the same rules as before: Tip 15% of the bill if the bill value is between 50 and 300, and if the value is different, the tip is 20%.

1. Write a function 'calcTip' that takes any bill value as an input and returns the corresponding tip, calculated based on the rules above (you can check out the code from first tip calculator challenge if you need to). Use the function type you like the most. Test the function using a bill value of 100.
2. And now let's use arrays! So create an array 'bills' containing the test data below.
3. Create an array 'tips' containing the tip value for each bill, calculated from the function you created before.
4. BONUS: Create an array 'total' containing the total values, so the bill + tip.

TEST DATA: 125, 555 and 44

HINT: Remember that an array needs a value in each position, and that value can actually be the returned value of a function! So you can just call a function as array values (so don't store the tip values in separate variables first, but right in the new array) 

```js
const calcTip = function (bill) {
  return bill >= 50 && bill <= 300 ? bill * 0.15 : bill * 0.2;
}
// const calcTip = bill => bill >= 50 && bill <= 300 ? bill * 0.15 : bill * 0.2;

const bills = [125, 555, 44];
const tips = [calcTip(bills[0]), calcTip(bills[1]), calcTip(bills[2])];
const totals = [bills[0] + tips[0], bills[1] + tips[1], bills[2] + tips[2]];

console.log(bills, tips, totals);
```

## 42. Introduction to Objects
```js
const xorausArray = [
  'Jordan',
  'Ahmed',
  2027 - 1997,
  'teacher',
  ['Ali', 'Khan', 'Sal']
];

const xoraus = {
  firstName: 'Jordan',
  lastName: 'Ahmed',
  age: 2027 - 1997,
  job: 'teacher',
  friends: ['Ali', 'K', 'Sal']
};
```

## 43. Dot vs. Bracket Notation
```js
const xoraus = {
  firstName: 'Jordan',
  lastName: 'Ahmed',
  age: 2027 - 1997,
  job: 'teacher',
  friends: ['Plato', 'Aristotle', 'Socrates']
};
console.log(xoraus); 

console.log(xoraus.lastName); // output: Ahmed
console.log(xoraus['lastName']); // output: Ahmed

const nameKey = 'Name';
console.log(xoraus['first' + nameKey]); // output: Jordan
console.log(xoraus['last' + nameKey]); // output: Ahmed

// console.log(xoraus.'last' + nameKey) // this will not work

const interestedIn = prompt('What do you want to know about Jordan? Choose between firstName, lastName, age, job, and friends');

if (xoraus[interestedIn]) {
  console.log(xoraus[interestedIn]);
} else {
  console.log('Wrong request! Choose between firstName, lastName, age, job, and friends');
}

xoraus.location = 'India';
xoraus['twitter'] = '@xoraus';
console.log(xoraus);

// Challenge
// "Jonas has 3 friends, and his best friend is called Aristotle"
console.log(`${xoraus.firstName} has ${xoraus.friends.length} friends, and his best friend is called ${xoraus.friends[1]}`);

```

- when we need to first compute the property name,  then we have to use the bracket notation otherwise use dot notation.
- we get **undefined ** when when we try to access a property on an object that does not exist.

## 44. Object Methods
```js
const xoraus = {
  firstName: 'Jordan',
  lastName: 'Ahmed',
  birthYeah: 1997,
  job: 'Programmer',
  friends: ['Socrates', 'Plato', 'Aristotle'],
  hasDriversLicense: true,

  // calcAge: function (birthYeah) {
  //   return 2037 - birthYeah;
  // }

  // calcAge: function () {
  //   // console.log(this);
  //   return 2027 - this.birthYeah;
  // }

  calcAge: function () {
    this.age = 2027 - this.birthYeah;
    return this.age;
  },

  getSummary: function () {
    return `${this.firstName} is a ${this.calcAge()}-year old ${xoraus.job}, and he has ${this.hasDriversLicense ? 'a' : 'no'} driver's license.`
  }
};

console.log(xoraus.calcAge());

console.log(xoraus.age);
console.log(xoraus.age);
console.log(xoraus.age);

// Challenge
// "Jonas is a 30-year old programmer, and he has a driver's license"
console.log(xoraus.getSummary());
```
- Any function that is attached to an object is called a method.

## 45. Coding Challenge ##3
Let's go back to Mark and John comparing their BMIs! This time, let's use objects to implement the calculations! Remember: BMI = mass / height ** 2 = mass / (height * height). (mass in kg and height in meter)

1. For each of them, create an object with properties for their full name, mass, and height (Mark Miller and John Smith)
2. Create a 'calcBMI' method on each object to calculate the BMI (the same method on both objects). Store the BMI value to a property, and also return it from the method.
3. Log to the console who has the higher BMI, together with the full name and the respective BMI. Example: "John Smith's BMI (28.3) is higher than Mark Miller's (23.9)!"

TEST DATA: Marks weights 78 kg and is 1.69 m tall. John weights 92 kg and is 1.95 m tall.

```js
const mark = {
  fullName: 'Mark Miller',
  mass: 78,
  height: 1.69,
  calcBMI: function () {
    this.bmi = this.mass / this.height ** 2;
    return this.bmi;
  }
};

const john = {
  fullName: 'John Smith',
  mass: 92,
  height: 1.95,
  calcBMI: function () {
    this.bmi = this.mass / this.height ** 2;
    return this.bmi;
  }
};

mark.calcBMI();
john.calcBMI();

console.log(mark.bmi, john.bmi);

// "John Smith's BMI (28.3) is higher than Mark Miller's (23.9)!"

if (mark.bmi > john.bmi) {
  console.log(`${mark.fullName}'s BMI (${mark.bmi}) is higher than ${john.fullName}'s BMI (${john.bmi})`)
} else if (john.bmi > mark.bmi) {
  console.log(`${john.fullName}'s BMI (${john.bmi}) is higher than ${mark.fullName}'s BMI (${mark.bmi})`)
}

```

## 46. Iteration: The for Loop
```js
// console.log('Lifting weights repetition 1 🏋️‍♀️');
// console.log('Lifting weights repetition 2 🏋️‍♀️');
// console.log('Lifting weights repetition 3 🏋️‍♀️');
// console.log('Lifting weights repetition 4 🏋️‍♀️');
// console.log('Lifting weights repetition 5 🏋️‍♀️');
// console.log('Lifting weights repetition 6 🏋️‍♀️');
// console.log('Lifting weights repetition 7 🏋️‍♀️');
// console.log('Lifting weights repetition 8 🏋️‍♀️');
// console.log('Lifting weights repetition 9 🏋️‍♀️');
// console.log('Lifting weights repetition 10 🏋️‍♀️');

// for loop keeps running while condition is TRUE
for (let rep = 1; rep <= 30; rep++) {
  console.log(`Lifting weights repetition ${rep} 🏋️‍♀️`);
}
```

## 47. Looping Arrays, Breaking and Continuing
```js
const jonas = [
  'Jonas',
  'Schmedtmann',
  2037 - 1991,
  'teacher',
  ['Michael', 'Peter', 'Steven'],
  true
];
const types = [];

// console.log(jonas[0])
// console.log(jonas[1])
// ...
// console.log(jonas[4])
// jonas[5] does NOT exist

for (let i = 0; i < jonas.length; i++) {
  // Reading from jonas array
  console.log(jonas[i], typeof jonas[i]);

  // Filling types array
  // types[i] = typeof jonas[i];
  types.push(typeof jonas[i]);
}

console.log(types);

const years = [1991, 2007, 1969, 2020];
const ages = [];

for (let i = 0; i < years.length; i++) {
  ages.push(2037 - years[i]);
}
console.log(ages);

// continue and break
console.log('--- ONLY STRINGS ---')
for (let i = 0; i < jonas.length; i++) {
  if (typeof jonas[i] !== 'string') continue;

  console.log(jonas[i], typeof jonas[i]);
}

console.log('--- BREAK WITH NUMBER ---')
for (let i = 0; i < jonas.length; i++) {
  if (typeof jonas[i] === 'number') break;

  console.log(jonas[i], typeof jonas[i]);
}

```

## 48. Looping Backwards and Loops in Loops
```js
const jonas = [
  'Jonas',
  'Schmedtmann',
  2037 - 1991,
  'teacher',
  ['Michael', 'Peter', 'Steven'],
  true
];

// 0, 1, ..., 4
// 4, 3, ..., 0

for (let i = jonas.length - 1; i >= 0; i--) {
  console.log(i, jonas[i]);
}

for (let exercise = 1; exercise < 4; exercise++) {
  console.log(`-------- Starting exercise ${exercise}`);

  for (let rep = 1; rep < 6; rep++) {
    console.log(`Exercise ${exercise}: Lifting weight repetition ${rep} 🏋️‍♀️`);
  }
}
```

## 49. The while Loop
```js
for (let rep = 1; rep <= 10; rep++) {
  console.log(`Lifting weights repetition ${rep} 🏋️‍♀️`);
}

let rep = 1;
while (rep <= 10) {
  // console.log(`WHILE: Lifting weights repetition ${rep} 🏋️‍♀️`);
  rep++;
}

let dice = Math.trunc(Math.random() * 6) + 1;

while (dice !== 6) {
  console.log(`You rolled a ${dice}`);
  dice = Math.trunc(Math.random() * 6) + 1;
  if (dice === 6) console.log('Loop is about to end...');
}
```

## 50. Coding Challenge ##4

Let's improve Steven's tip calculator even more, this time using loops!
1. Create an array 'bills' containing all 10 test bill values
2. Create empty arrays for the tips and the totals ('tips' and 'totals')
3. Use the 'calcTip' function we wrote before (no need to repeat) to calculate tips and total values (bill + tip) for every bill value in the bills array. Use a for loop to perform the 10 calculations!

TEST DATA: 22, 295, 176, 440, 37, 105, 10, 1100, 86 and 52

HINT: Call calcTip in the loop and use the push method to add values to the tips and totals arrays 😉

1. BONUS: Write a function 'calcAverage' which takes an array called 'arr' as an argument. This function calculates the average of all numbers in the given array. This is a DIFFICULT challenge (we haven't done this before)! Here is how to solve it:
  4.1. First, you will need to add up all values in the array. To do the addition, start by creating a variable 'sum' that starts at 0. Then loop over the array using a for loop. In each iteration, add the current value to the 'sum' variable. This way, by the end of the loop, you have all values added together
  4.2. To calculate the average, divide the sum you calculated before by the length of the array (because that's the number of elements)
  4.3. Call the function with the 'totals' array

```js
const calcTip = function (bill) {
  return bill >= 50 && bill <= 300 ? bill * 0.15 : bill * 0.2;
}
const bills = [22, 295, 176, 440, 37, 105, 10, 1100, 86, 52];
const tips = [];
const totals = [];

for (let i = 0; i < bills.length; i++) {
  const tip = calcTip(bills[i]);
  tips.push(tip);
  totals.push(tip + bills[i]);
}
console.log(bills, tips, totals);

const calcAverage = function (arr) {
  let sum = 0;
  for (let i = 0; i < arr.length; i++) {
    // sum = sum + arr[i];
    sum += arr[i];
  }
  return sum / arr.length;
}
console.log(calcAverage([2, 3, 7]));
console.log(calcAverage(totals));
console.log(calcAverage(tips));
```
