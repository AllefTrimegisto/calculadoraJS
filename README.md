# calculadoraJS

Com os conceitos aprendidos, crie um programa de calculadora que: 

receba dois valores, que devem ser salvos em variáveis; 
o usuário deve colocar qual operador ele vai utilizar por meio dos símbolos aritméticos; 
com os dois valores e o operador definido, o programa deve fazer a operação e retornar o resultado; 
se houver divisão, você deve retornar o resultado e a sobra, caso haja alguma. 


function calculator(num1, num2, operator) {
  let result;
  let remainder;

  // Realiza a operação de acordo com o operador especificado
  switch (operator) {
    case "+":
      result = num1 + num2;
      break;
    case "-":
      result = num1 - num2;
      break;
    case "*":
      result = num1 * num2;
      break;
    case "/":
      result = Math.floor(num1 / num2); // Obtém o resultado da divisão inteira
      remainder = num1 % num2; // Obtém o resto da divisão
      break;
    default:
      console.log("Operador inválido");
      return;
  }

  // Mostra o resultado da operação
  console.log("Resultado:", result);

  // Se houver resto, mostra a sobra
  if (remainder) {
    console.log("Sobra:", remainder);
  }
}

// Testa o programa de calculadora com alguns exemplos
calculator(10, 5, "+"); // Resultado: 15
calculator(10, 5, "-"); // Resultado: 5
calculator(10, 5, "*"); // Resultado: 50
calculator(10, 5, "/"); // Resultado: 2, Sobra: 0
calculator(10, 5, "^"); // Operador inválido
