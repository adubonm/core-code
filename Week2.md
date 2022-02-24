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
<strong>Multiply</strong>

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
<strong>ASCII Total</strong>

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
<strong>get character from ASCII Value</strong>

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
<strong>Binary Addition</strong>

Implement a function that adds two numbers together and returns their sum in binary. The conversion can be done before, or after the addition.

The binary number returned should be a string.

Examples:(Input1, Input2 --> Output (explanation)))

1, 1 --> "10" (1 + 1 = 2 in decimal or 10 in binary)
5, 9 --> "1110" (5 + 9 = 14 in decimal or 1110 in binary)

Answer:

<h3>Challenge 5</h3>
<strong>Student's Final Grade</strong>

Create a function finalGrade, which calculates the final grade of a student depending on two parameters: a grade for the exam and a number of completed projects.

This function should take two arguments: exam - grade for exam (from 0 to 100); projects - number of completed projects (from 0 and above);

This function should return a number (final grade). There are four types of final grades:

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

<h2>Wednesday | Week 2 Challennges</2>

<h3>Challenge 1</h3>
<strong>Holiday VIII - Duty Free</strong>

The purpose of this kata is to work out just how many bottles of duty free whiskey you would have to buy such that the saving over the normal high street price would effectively cover the cost of your holiday.

You will be given the high street price (normPrice), the duty free discount (discount) and the cost of the holiday.

For example, if a bottle cost £10 normally and the discount in duty free was 10%, you would save £1 per bottle. If your holiday cost £500, the answer you should return would be 500.

All inputs will be integers. Please return an integer. Round down.

Answer:
```Javascript
function dutyFree(normPrice, discount, hol){
  return Math.trunc( hol / ( normPrice * ( discount
/ 100)));
}
```
<h3>Challenge 2</h3>
<strong>Twice as old</strong>
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
<strong>Valid Spacing</strong>
Your task is to write a function called valid_spacing() or validSpacing() which checks if a string has valid spacing. The function should return either true or false (or the corresponding value in each language).

For this kata, the definition of valid spacing is one space between words, and no leading or trailing spaces. Words can be any consecutive sequence of non space characters. Below are some examples of what the function should return:

Answer:
```Javascript
function validSpacing(s) {
  return s.trim() == s && !s.includes('  ');
}
```

<h3>Challenge 4</h3>
<strong>Fake Binary</strong>
Given a string of digits, you should replace any digit below 5 with '0' and any digit 5 and above with '1'. Return the resulting string.

Note: input will never be an empty string

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
/*This is a better solution*/
function fakeBin(x) {
    return x.split('').map(n => n < 5 ? 0 : 1).join('');
}
```
