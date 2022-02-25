<h1>Week 2 CoreCode Challenges</h1>

<h2>Monday | Week 2 Challenges</h2>

<h3>Challenge 1</h3>
Follow the github course, you can find it here
<h3>Challenge 2</h3>
Watch <a href="https://www.youtube.com/watch?v=A37-3lflh8I" target="_blank">this</a> video
<h3>Challenge 3</h3>
Read <a href="https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/Math" target="_blank">this</a>
<h3>Challenge 4</h3>
Create an account in Codewars

<h2>Tuesday | Week 2 Challennges</2>

<h3>Challenge 0</h3>
Watch <a href="https://www.youtube.com/watch?v=cEBkvm0-rg0" target="_blank"> video


<h3>Challenge 1</h3>
<strong>Multiply</strong><br>
This code does not execute properly. Try to figure out why.

```Javascript
function multiply(a, b){
  a * b;
}
```
	
Answer:
```Javascript
function multiply(a, b){
  return a * b;
}
```

<h3>Challenge 2</h3>
<strong>ASCII Total</strong><br>
You'll be given a string, and have to return the sum of all characters as an int. The function should be able to handle all ASCII characters.

examples:
```
uniTotal("a") == 97 uniTotal("aaa") == 291
```
Answer:
```Javascript
function uniTotal (string) {
  let arr = Array.from(string);//SE CONVIERTE LA CADENA A UN ARREGLO => [a,a,a]
  let sum = 0;
  for (let i = 0; i < arr.length; i++) {// se hace un for para iterar el arreglo
	  sum += arr[i].charCodeAt(0); //con charCodeAt(0) se convierrte al numero ascii y se va sumando
  }
  return sum; // como es una funcion debe de devolver un valor 
}
```

<h3>Challenge 3</h3>
<strong>get character from ASCII Value</strong><br>
Write a function `get_char() / getChar()` which takes a number and returns the corresponding ASCII `char` for that value.

Example:

`get_char(65)`

should return:

`'A'`

Answer:
```Javascript
function getChar(c){
  return String.fromCharCode(c)
}
```

<h3>Challenge 4</h3>
<strong>Binary Addition</strong><br>
Implement a function that adds two numbers together and returns their sum in binary. The conversion can be done before, or after the addition. The binary number returned should be a string.

Examples:(Input1, Input2 --> Output (explanation)))

1, 1 --> "10" (1 + 1 = 2 in decimal or 10 in binary)
5, 9 --> "1110" (5 + 9 = 14 in decimal or 1110 in binary)

Answer:
```Javascript
function addBinary(a,b) {
  return(a + b).toString(2);
}
```

<h3>Challenge 5</h3>
<strong>Student's Final Grade</strong><br>
Create a function finalGrade, which calculates the final grade of a student depending on two parameters: a grade for the exam and a number of completed projects. This function should take two arguments: exam - grade for exam (from 0 to 100); projects - number of completed projects (from 0 and above); This function should return a number (final grade). There are four types of final grades:

100, if a grade for the exam is more than 90 or if a number of completed projects more than 10.
90, if a grade for the exam is more than 75 and if a number of completed projects is minimum 5.
75, if a grade for the exam is more than 50 and if a number of completed projects is minimum 2.
0, in other cases

Answer:
```Javascript
function finalGrade (exam, projects) {
  if (exam <= 100 && exam >= 0){
    if (exam > 90 || projects > 10){
      return 100;
    } else if (exam > 75 && projects >= 5){
      return 90;
    } else if (exam > 50 && projects >= 2){
      return 75;
    } else {return 0;}
  } else { return "Not a valid number";}
}
```

<h2>Wednesday | Week 2 Challenges</2>

<h3>Challenge 1</h3>
<strong>Holiday VIII - Duty Free</strong><br>
The purpose of this kata is to work out just how many bottles of duty free whiskey you would have to buy such that the saving over the normal high street price would effectively cover the cost of your holiday. You will be given the high street price (normPrice), the duty free discount (discount) and the cost of the holiday. For example, if a bottle cost £10 normally and the discount in duty free was 10%, you would save £1 per bottle. If your holiday cost £500, the answer you should return would be 500. All inputs will be integers. Please return an integer. Round down.

Answer:
```Javascript
function dutyFree(normPrice, discount, hol){
  return Math.trunc( hol / ( normPrice * ( discount
/ 100)));
}
```
<h3>Challenge 2</h3>
<strong>Twice as old</strong><br>
Your function takes two arguments:
1. current father's age (years)
2. current age of his son (years)
Сalculate how many years ago the father was twice as old as his son (or in how many years he will be twice as old).

Answer:
```Javascript
function twiceAsOld(dadYearsOld, sonYearsOld) {
  return Math.abs(dadYearsOld - 2 * sonYearsOld);
}
```
<h3>Challenge 3</h3>
<strong>Valid Spacing</strong><br>
Your task is to write a function called valid_spacing() or validSpacing() which checks if a string has valid spacing. The function should return either true or false (or the corresponding value in each language). For this kata, the definition of valid spacing is one space between words, and no leading or trailing spaces. Words can be any consecutive sequence of non space characters. Below are some examples of what the function should return:

Answer:
```Javascript
function validSpacing(s) {
  return s.trim() == s && !s.includes('  ');
}
```

<h3>Challenge 4</h3>
<strong>Fake Binary</strong><br>
Given a string of digits, you should replace any digit below 5 with '0' and any digit 5 and above with '1'. Return the resulting string. Note: input will never be an empty string

Answer:
```Javascript
/*This is my solution*/
function fakeBin(x){
  const toArr = x.split('');
  const newArr = toArr.map(y => parseInt(y) < 5 ? "0" : "1")
  return newArr.join('');
}
```
or
```Javascript
function fakeBin(x) {
    return x.split('').map(n => n < 5 ? 0 : 1).join('');
}
```
or
```Javascript
function fakeBin(x){
var bin = "";
for (var i = 0; i<x.length; i++){
if(x[i]<5){
bin+=0;}

else if (x[i]>=5){
bin+=1;
}
}
return bin;
}
```
<h2>Thursday | Week 2 Challenges</h2>

<h3>Challenge 1</h3>
<strong>Exclamation marks series #2: Remove all exclamation marks from the end of sentence</strong><br>
Remove all exclamation marks from the end of sentence.

Examples
```Javascript
remove("Hi!") === "Hi"
remove("Hi!!!") === "Hi"
remove("!Hi") === "!Hi"
remove("!Hi!") === "!Hi"
remove("Hi! Hi!") === "Hi! Hi"
remove("Hi") === "Hi"
```
Answer:
```Javascript
function remove(s)
{
    while(s && s.slice(-1) == "!") 
    { 
        s = s.slice(0,-1) 
    }
    return s;
}
```
<h3>Challenge 2</h3>
<strong>Vowel remover</strong><br>
Create a function called shortcut to remove the lowercase vowels (a, e, i, o, u ) in a given string.

Examples
```Javascript
"hello"     -->  "hll"
"codewars"  -->  "cdwrs"
"goodbye"   -->  "gdby"
"HELLO"     -->  "HELLO"
```
-Don't worry about uppercase vowels<br>
-y is not considered a vowel for this kata

Answer:
```Javascript
function shortcut(string){
  return string.replace(/[aeiou]/g,'')
}
```
<h3>Challenge 3</h3>
<strong>Rock Paper Scissors!</strong><br>
Let's play! You have to return which player won! In case of a draw return Draw!.

Examples:
```Javascript
rps('scissors','paper') // Player 1 won!
rps('scissors','rock') // Player 2 won!
rps('paper','paper') // Draw!
```

Answer:
```Javascript
const rps = (p1, p2) => {
  if (p1 === p2) return 'Draw!'
  
  const rules = { paper: 'rock', rock: 'scissors', scissors: 'paper'}
  return rules[p1] === p2 ? 'Player 1 won!' : 'Player 2 won!'
 
};
```
<h3>Challenge 4</h3>
<strong>Persistent Bugger.</strong><br>
Write a function, persistence, that takes in a positive parameter num and returns its multiplicative persistence, which is the number of times you must multiply the digits in num until you reach a single digit.

For example (Input --> Output):
```Javascript
39 --> 3 (because 3*9 = 27, 2*7 = 14, 1*4 = 4 and 4 has only one digit)
999 --> 4 (because 9*9*9 = 729, 7*2*9 = 126, 1*2*6 = 12, and finally 1*2 = 2)
4 --> 0 (because 4 is already a one-digit number)
```

Answer:
```Javascript
function persistence(num) {
   let i = 0;
   while (num.toString().length !== 1) {
     num = num.toString().split("").reduce((a,b)=>a*b);
     i++;
   }
   return i;
}
```
<h3>Challenge 5</h3>
<strong>Mission statement</strong><br>
Let’s write our Mission Statement! In one paragraph, please answer to the next 5 questions:

1. Who are you?
2. What background do you have?
3. Who do you want to be?
4. What do you want to do?
5. What are the core values and principles that govern your character and contributions?

<table><tr><td>I’m a software developer aspirant with knowledge in JavaScript, HTML, CSS, React, Bash, Git & GitHub. Passionate about technology and all the possibilities that computing entails. I consider myself a result-driven person and long-life learner.</td></tr></table>
