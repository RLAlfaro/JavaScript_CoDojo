# JavaScript Coding Dojo

### Funcion Basica I

```js
function a(){
    return 35;
}
console.log(a())

// 35
```

```js
function a(){
    return 4;
}
console.log(a()+a());

// 8
```

```js
function a(b){
    return b;
}
console.log(a(2)+a(4));

// 6
```

```js
function a(b){
    console.log(b);
    return b*3;
}
console.log(a(3));

// 3
// 9
```

```js
function a(b){
   return b*4;
   console.log(b);
}
console.log(a(10));

// 40
```

```js
function a(b){
    if(b<10) {
        return 2;
    }
    else     {
        return 4;
    }
    console.log(b);
}
console.log(a(15));

// 4
```

```js
function a(b,c){
    return b*c;
}
console.log(10,3);
console.log( a(3,10) );

// 10 3
// 30
```

```js
function a(b){
    for(var i=0; i<10; i++){
        console.log(i);
    }
    return i;
}
console.log(3);
console.log(4);

// 3
// 4
```

```js
function a(){
    for(var i=0; i<10; i++){
        i = i +2;
        console.log(i);
    }
}
a();

// 2
// 5
// 8
// 11
```

```js
function a(b,c){
    for(var i=b; i<c; i++) {
       console.log(i);
   }
   return b*c;
}
a(0,10);
console.log(a(0,10));

// 0
// 1
// 2
// 3
// 4
// 5
// 6
// 7
// 8
// 9
// 0
// 1
// 2
// 3
// 4
// 5
// 6
// 7
// 8
// 9
// 0
```

```js
function a(){
    for(var i=0; i<10; i++){
       for(var j=0; j<10; j++){
           console.log(j);
       }
       console.log(i);
    }
}

// -- NO SE IMPRIME NADA --
```

```js
function a(){
    for(var i=0; i<10; i++){
        for(var j=0; j<10; j++){
            console.log(i,j);
        }
        console.log(j,i);
    }
}

// -- NO SE IMPRIME NADA --
```

```js
var z = 10;
function a(){
    var z = 15;
    console.log(z);
}
console.log(z);

// 10
```

```js
var z = 10;
function a(){
    var z = 15;
    console.log(z);
}
a();
console.log(z);

// 15
// 10
```

```js
var z = 10;
function a(){
    var z = 15;
    console.log(z);
    return z;
}
z = a();
console.log(z);

// 15
// 15
```

### Fundamentos Basicos I

1. Obtén del 1 al 255
```js
function numberPrinter(x) {
    if (x <= 0) {
        return false
    }
    else {
        for(var i = 1; i <= x; i++) {
        console.log(i)
        }
    }
}
numberPrinter(255);
```

2. Consigue pares hasta 1000
```js
function evenNumberPrinter(x) {
    if (x <= 0) {
        return false
    }
    else {
        for(var i = 1; i <= x; i++) {
          if(i % 2 === 0){
            console.log(i)
          }
        }
    }
}
evenNumberPrinter(1000)
```

3. Suma impares hasta 5000
```js
function oddNumberSum(x) {
    var sum = 0;
    if (x <= 0) {
        return false
    }
    else {
        for(var i = 1; i <= x; i++) {
          if(i % 2 === 1){
            sum = sum + i;
          }
        }
    }
    console.log(sum)
}
oddNumberSum(5000)
```

4. Itera un array || suma || (ej:  [1,2,5] retorna 8. [-5,2,5,12] retorna 14). 
```js
function arraySum(x) {
  var sum = 0;
    for(var i = 0; i <= x.length-1; i++) {
      sum = sum + x[i];
  }
  console.log(sum)
}
var x = [-5,2,5,12];
arraySum(x)
```

5. Encuentra el max || (ej: para [-3,3,5,7] el número mayor (max) es 7). 
```js
function maxElem(x) {
    var currentMax = x[0];
    for (var i = 0; i < x.length; i++) {
        if (x[i] > currentMax) {
            currentMax = x[i]
        }
    }
    return currentMax;
}
var x = [-3,3,5,7];
console.log(maxElem(x));
```

6. Encuentra el promedio (avg) || (ej: para [1,3,5,7,20] el promedio es 7.2).
```js
function arrayAvg(x) {
    var sum = 0;
    for (var i = 0; i < x.length; i++) {
      sum = sum + x[i];
    }
    var avg = sum / x.length;
    return avg;
}
var x = [1,3,5,7,20];
console.log(arrayAvg(x));
```

7. Array de impares || números impares entre 1 y 50
```js
function oddArray(x) {
  let array = [];
  for(var i = 1; i <= x; i++) {
    if(i % 2 === 1){
      array.push(i);
    }
  }
  console.log(array)
}
oddArray(50)
```

8. Mayor que Y || arr = [1,3,5,7] y Y = 3, tu función devolverá 2 (hay 2 números en el array mayores que 3, esto son 5 y 7). 
```js
function countHigherThanY(x,y) {
    var counter = 0;
    for (var i = 0; i < x.length; i++) {
        if (x[i] > y) {
            counter++;
        }
    }
    return counter;
}
var x = [-3,3,5,7];
var y = 3
console.log(countHigherThanY(x,y));
```

9. Cuadrados || (ej: [1,5,10,-2] será [1,25,100,4]).
```js
function arraySquared(x) {
  var squared = [];
  for (var i = 0; i < x.length; i++) {
    squared.push(x[i]*x[i]);
    
  }
  return squared;
}
var x = [1,5,10,-2];
console.log(arraySquared(x));
```

10. Negativos ||  (ej: [1,5,10,-2] se convertirá en [1,5,10,0])
```js
function positivinaitor(x) {
  for (var i = 0; i < x.length; i++) {
    if (x[i] < 0) {
        x[i] = x[i]*-1
    }
  }
  return x;
}
var x = [1,5,10,-2];
console.log(positivinaitor(x));
```

11. Max/Min/Avg || (ej: [1,5,10,-2] devolverá [10,-2,3.5])
```js
function maxMinAvg(x) {
  var currentMin = x[0];
  var currentMax = x[0];
  var sum = 0;
  for (var i = 0; i < x.length; i++) {
    sum = sum + x[i];
  }
  var avg = sum / x.length;
  for (var j = 0; j < x.length; j++) {
    if (x[j] > currentMax) {
      currentMax = x[j]
    }
  }
  for (var k = 0; k < x.length; k++) {
    if (x[k] < currentMax) {
      currentMin = x[k]
    }
  }
  var arrange = [currentMax, currentMin, avg];
  return arrange;
}  
var x = [1,5,10,-2];
console.log(maxMinAvg(x));
```

12. Intercambia Valores ||  intercambie el primer y el último valor  || (ej: [1,5,10,-2] será [-2,5,10,1]). 
```js
function changeFirstLast(x) {
  var first = x[0];
  var last = x[x.length-1];
  x[0] = last;
  x[x.length-1] = first;
  return x;
}
var x = [1,5,10,-2];
console.log(changeFirstLast(x));
```

13. De Número a String || Negativo a 'dojo' ||  dado el array = [-1,-3,2], tu función devolverá [‘Dojo’,‘Dojo’,2].
```js
function positivinaitor(x) {
  for (var i = 0; i < x.length; i++) {
    if (x[i] < 0) {
        x[i] = 'dojo'
    }
  }
  return x;
}
var x = [-1,-3,2];
console.log(positivinaitor(x));
```





