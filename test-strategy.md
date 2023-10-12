Errores del primer codigo con un # y la correcion con dos ## Gracias.

--------------------------------------------------------------------------
1. Error: La variable randomNumber mala, esto generará un número decimal entre 0 y 10, no un número entre 1 y 100 como se requiere.

Error del codigo: 
# let randomNumber = Math.random() * 10;

Solucion: Cambiar la inicializacion de ´randomNumber´ para que genere un numero aleatorio entre 1 y 100.

Solucion del codigo respectiva:
## let randomNumber = Math.floor(Math.random() * 100) + 1;

--------------------------------------------------------------------------

2. Error: El numero de intentos no era el correcto era de 5 intentos lo cual eran 10 intentos.

Error del codigo:
# const ATTEMPS = 5;

Solucion: Colocar el numero de intentos correcto la cual son 10 intentos.

Solucion del codigo respectiva:
## const ATTEMPS = 10;

--------------------------------------------------------------------------

3. Error: El selector para lowOrHi en el siguiente fragmento no incluye un punto para indicar una clase CSS.

Error del codigo:
# const lowOrHi = document.querySelector('lowOrHi');

Solucion: Agregar un punto al selector para que sea una clase CSS válida.

Solucion del codigo respectiva:
## const lowOrHi = document.querySelector('.lowOrHi');

--------------------------------------------------------------------------

4. Error: De que guessField.value es una cadena de texto, no un número y que utiliza variables regulares let.

Error del codigo:
# let userGuess = guessField.value;

Solucion: Modificar a que sea un numero entero agregando una verificacion parseInt y agregandole constantes con const,

Solucion del codigo respectiva:
## const userGuess = parseInt(guessField.value);

--------------------------------------------------------------------------

5. Error: En la logica los textContent no se encontraban de manera correcta mostraban un mensaje erroneo y no estaban ordenados de manera correcta y los colores al momento de mostrar el mensaje final se mostraba de manera erronea a los solicitados.

Error del codigo:
 if(userGuess === randomNumber) {
#     lastResult.textContent = '!!!Pérdistes!!!';
#     lastResult.style.backgroundColor = 'black';
      lowOrHi.textContent = '';
      setGameOver();
    } else if(guessCount === ATTEMPS) {
#     lastResult.textContent = 'Felicitaciones! adivinaste el número!';
      lastResult.style.backgroundColor = 'red';
      setGameOver();
     } else {
       lastResult.textContent = 'Incorrecto! ';
#      lastResult.style.backgroundColor = 'green';
 if(userGuess < randomNumber) {
        lowOrHi.textContent = 'El número es mayor!';
      } else if(userGuess > randomNumber) {
        lowOrHi.textContent = 'El número es menor!';
      }
    }

Solucion: Colocar de manera correcta el mensaje de cada textContent y colocar los colores solicitados correctos para mostrar el mensaje final de manera correcta en uno de black a green y el otro de green a black.

Solucion del codigo respectiva:
    if(userGuess === randomNumber) {
##    lastResult.textContent = '¡Felicitaciones! ¡Adivinaste el número!';
##    lastResult.style.backgroundColor = 'green';
      lowOrHi.textContent = '';
      setGameOver();
    } else if(guessCount === ATTEMPS) {
##    lastResult.textContent = '!!!Pérdistes!!!';
      lastResult.style.backgroundColor = 'red';
      setGameOver();
    } else {
      lastResult.textContent = 'Incorrecto! ';
##    lastResult.style.backgroundColor = 'black';
      if(userGuess < randomNumber) {
        lowOrHi.textContent = 'El número es mayor!';
      } else if(userGuess > randomNumber) {
        lowOrHi.textContent = 'El número es menor!';
      }
    }

--------------------------------------------------------------------------

6. Error: En el evento click del botón de envío (guessSubmit) se configura con addeventListener en lugar de addEventListener.

Error del codigo:
# guessSubmit.addeventListener('click', checkGuess);

Solucion: Cambiar donde se agrega el evento ´click´ para utilizar ´addEventListener´.

Solucion del codigo respectiva:
## guessSubmit.addEventListener('click', checkGuess);

--------------------------------------------------------------------------

7. Error: En el evento click del botón de envío (resetButton) se configura con addeventListener en lugar de addEventListener.

Error del codigo:
# resetButton.addeventListener('click', resetGame);

Solucion: Cambiar donde se agrega el evento ´click´ para utilizar ´addEventListener´.

Solucion del codigo respectiva:
## resetButton.addEventListener('click', resetGame); 

--------------------------------------------------------------------------

8. Error: En el ´Math.random()´ el cual produce un número decimal entre 0 y 1, y al usar Math.floor, siempre redondea hacia abajo a 0, haciendo que randomNumber sea igual a 1.

Error del codigo:
# randomNumber = Math.floor(Math.random()) + 1;

Solucion: Multiplica el número aleatorio por 100 antes de redondearlo hacia abajo, el cual ya genera un numero aleatorio entre 1 y 100 en lugar de siempre ser 1.

Solucion del codigo respectiva:
## randomNumber = Math.floor(Math.random() * 100) + 1;

--------------------------------------------------------------------------
- Se Coloco una alerta si no es del 1 al 100, igual que con letras, pide ingresar un numero entre 1 y 100, esta quedo documentada en el index.html

##    if (isNaN(userGuess) || userGuess < 1 || userGuess > 100) {
##          alert('Por favor, ingresa un número entero entre 1 y 100.');
##          return;
##        }
--------------------------------------------------------------------------
