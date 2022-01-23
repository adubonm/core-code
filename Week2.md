Week 2
========
## Week Challenges (Monday)

**1. Follow the github course, you can find it here** :white_check_mark:<br>
**2. Watch this video** :white_check_mark:<br>
**3. Read this** :white_check_mark:<br>
**4. Create an account in Codewars** :white_check_mark:

## Week Challenges (Tuesday)

**0. Watch this video** :white_check_mark:

**1. Multiply** :white_check_mark:

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
**2. ASCII Total** :white_check_mark:

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
**3. get character from ASCII Value** :white_check_mark:

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
**4. Binary Addition** :white_check_mark:

Implement a function that adds two numbers together and returns their sum in binary. The conversion can be done before, or after the addition.

The binary number returned should be a string.

Examples:(Input1, Input2 --> Output (explanation)))

1, 1 --> "10" (1 + 1 = 2 in decimal or 10 in binary)
5, 9 --> "1110" (5 + 9 = 14 in decimal or 1110 in binary)

Answer:

**5. Student's Final Grade** :white_check_mark:

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

## Week Challenges (Wednesday)

**1. Holiday VIII - Duty Free** :white_check_mark:

The purpose of this kata is to work out just how many bottles of duty free whiskey you would have to buy such that the saving over the normal high street price would effectively cover the cost of your holiday.

You will be given the high street price (normPrice), the duty free discount (discount) and the cost of the holiday.

For example, if a bottle cost £10 normally and the discount in duty free was 10%, you would save £1 per bottle. If your holiday cost £500, the answer you should return would be 500.

All inputs will be integers. Please return an integer. Round down.

Answer:
```Javascript

```

## Week Challenges (Thursday)
