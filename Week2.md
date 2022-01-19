#Week 2
##Week Challenges (Monday)

##Week Challenges (Tuesday)

0. Watch this video :white_check_mark:

1. Multiply :white_check_mark: | This code does not execute properly. Try to figure out why.

function multiply(a, b){
  a * b;
}

Answer:

function multiply(a, b){
  return a * b;
}

2. ASCII Total :white_check_mark: | You'll be given a string, and have to return the sum of all characters as an int. The function should be able to handle all ASCII characters.

examples:

uniTotal("a") == 97 uniTotal("aaa") == 291

Answer:

function uniTotal (string) {
  let arr = Array.from(string);//SE CONVIERTE LA CADENA A UN ARREGLO => [a,a,a]
  let sum = 0;
  for (let i = 0; i < arr.length; i++) {// se hace un for para iterar el arreglo
	  sum += arr[i].charCodeAt(0); //con charCodeAt(0) se convierrte al numero ascii y se va sumando
  }
  return sum; // como es una funcion debe de devolver un valor 
}

3. get character from ASCII Value :white_check_mark: | Write a function get_char() / getChar() which takes a number and returns the corresponding ASCII char for that value.

Example:

get_char(65)

should return:

'A'

Answer:

function getChar(c){
  return String.fromCharCode(c)
}

4. Binary Addition :white_check_mark: | Implement a function that adds two numbers together and returns their sum in binary. The conversion can be done before, or after the addition.

The binary number returned should be a string.

Examples:(Input1, Input2 --> Output (explanation)))

1, 1 --> "10" (1 + 1 = 2 in decimal or 10 in binary)
5, 9 --> "1110" (5 + 9 = 14 in decimal or 1110 in binary)

Answer:
