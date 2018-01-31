# Function-scope-js

* **Track:** _Common Core_
* **Curso:** _Fundamentos de javascript_
* **Unidad:** _Producto final_
* **Tema:** _Function-scope_

***

## Objetivo

 Identificar las funciones globales, locales, funciones de callback, expresions, statement, clousure, scope, contextos de ejecucion, que funciones forman parte de la pila de ejecucion (stack execution) y que funciones forman parte de la cola de eventos (event queue).

1. Funciones/ Variables globales:

* Funciones globales: 

 ```js
  $(document).ready(function() {
  }
```
------------------------------------------
 ```js
function activeButton() {} 
function desactiveButton() {} 
function longitud(input) {}
function soloNumeros(input) {}
function isValidCreditCard(numberCard) {}
 ```

* Variables globales:

 ```js
var $inputCard = $('#card-number');
var $inputMonth = $('.input-month');
var $inputYear = $('.input-year');
var $buttonNext = $('#next');
var regexOnlyNumbers = /^[0-9]+$/;
var labelErrorOrSuccessMessages = $('label[for="card-number"]');  
 ```

2. Funciones/ Variables Locales:

* Funciones locales - Funciones statements

 ```js
function activeButton()   
function desactiveButton()   
function longitud(input)  
function soloNumeros(input)  
function isValidCreditCard(numberCard)  
$inputCard.on('input', function() {
});
```
* Variables locales

 ```js
var regex = /^[0-9]+$/;
var creditCardNumber = soloNumeros(longitud(numberCard));
var arr = [];
var sumaTotal = 0;
var index = creditCardNumber.length - 1; index >= 0; index--
```

3. Funciones Callback:

 ```js
  function longitud(input) {
    if (input.trim().length === 16) {
      return input;
    }
  }

  function soloNumeros(input) {
    var regex = /^[0-9]+$/;
    if (regex.test(input)) {
      return input;
    }
  }

  function isValidCreditCard(numberCard) {
    var creditCardNumber = soloNumeros(longitud(numberCard));
  }
```
4. Expressions:

5. Funciones Statement:

* Son las mismas que funciones locales (n° 2)

6. Clousure:

7. Scope:
```js
var creditCardNumber;
var arr;
var sumaTotal;
var index; (dentro de los ciclos for)
```
8. Contextos de ejecución:

9. Funciones que forman parte de la pila de ejecución (stack execution):

 ```js
function activeButton()
function desactiveButton()
function longitud()
function soloNumeros()
function isValidCreditCard()
```
10. Funcion de la cola de eventos (Event queq):
 ```js
$inputCard.on('input', function() {
  });
```

# Alumna
* Pamela De la cruz Lozano
