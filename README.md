# Recap-phase-0-Week2


- [Functions](#functions)
  - [Modular Functions](#modular-functions)
- [Array](#array)
  - [Multi-dimentional Array](#multi-dimentional-array)
- [References for Self-Taught](#references-for-self-taught)

![](https://media2.giphy.com/media/13HBDT4QSTpveU/giphy.gif?cid=ecf05e472bbvvvot2l5wgkrxliz9wppl5w285tmrfc05ynmx&rid=giphy.gif&ct=g)

# Functions

- Functions adalah sebuah code block yang disusun untuk menjalankan suatu proses.
- Setelah menyelesaikan suatu proses, functions dapat mengembalikan `value` dengan menggunakan syntax `return`.

Bentuk functions

```js
// Functions dengan return
function nameFunc(param1, param2, ..., paramN) {
  /* Isi dari function berupa tindakan */
  // ...
  return [expression];
}
//pemanggilan function
console.log(<namaFunction>(arg1, arg2, ...., argN))

// Functions dengan tanpa return
function nameFunc2(param1, param2, ..., paramN) {
  /* Isi dari function berupa tindakan */
  // ...
}
// pemanggilan function
console.log(<namaFunction>(arg1, arg2, ...., argN))

// DEFAULT PARAMETER
let num1 = 10
let num2 = 20
function getSum(angka1, angka2, angka3 = 10){
    let sum = angka1 + angka2 + angka3
    return sum
}

console.log(getSum(num1, num2)); // the result is not a NaN but 40 cause angka3 has default parameter when there's no argumen sent for angka3 from the function invoke
```

## Modular Functions

- Kita dapat membuat sebuah program yang terdiri dari beberapa functions, dimana setiap functions tersebut dapat saling terhubung.

Contoh modular function:

```js
function funcA(param1, param2, ..., paramN) {
  /* Isi dari function berupa tindakan */
  // ...
  return [expression];
}

function funcB(param1, param2, ..., paramN) {
  // funcB memanggil funcA untuk dapat menyelesaikan proses
  // ...
  return [expression]
}

console.log(funcB)
```

# Array

- Sebuah tipe data yang terstruktur, yang berguna untuk menyimpan kumpulan data yang sejenis. Contoh: array of strings, array of numbers, array of objects, etc.
- Kita dapat memanipulasi isi dari array dengan menggunakan beberapa built-in functions, seperti `push`, `pop`, `unshift`, `shift`, dsb.

Contoh array

```js
// create an array
let arrA = [data1, data2, ..., dataN]

// accessing one element/ value in array
arrA[0] // data in index 0
arrA[3] // data in index 3
arrA[N] // data in index N


// accessing every element / value in array
// you can use for or for of
for(let i = 0; i < arrA.length; i++){
    console.log(arrA[i])
}

for(let item of arrA){ // this loop will access every value in array and put in the item into variable item
    console.log(item)
}

// reassign item in array
aarA[0] = <newValue> 

// push new value to array (add new item into array and put it on the end of array)
arrA.push(value)

// pop value from array (delete the last item in array)
arrA.pop(value)

// unshift() adds new items to the beginning of an array
arrA.unshift(value) 

// shift() removes the first item of an array
arrA.shift()


// get length of an array
arrA.length

// how to sort Array (you only need to change the argumen <arr> with the variable)

function sortData(data) {
  for (let i = 0; i < data.length; i++) {
    for (let j = 0; j < data.length; j++) {
      if (data[j] > data[j + 1]) {
        let tmp = data[j];
        data[j] = data[j + 1];
        data[j + 1] = tmp;
      }
    }
  }
}
console.log(sortData(<arr>));

```

## Multi-dimentional Array

- Sebuah array yang terdiri dari array (nested array)

![](https://media0.giphy.com/media/lXu72d4iKwqek/giphy.gif?cid=ecf05e47cqktbb7eabmkvuggvlflafdl59ubb4zdhcilz2bj&rid=giphy.gif&ct=g)

Contoh array multi-dimensi

```js
// create multi-dimentional array
let students = [
    ['tama', 'al', 'derrick', 'agri', 'kosong'], // baris ke 0
//     00      01      02        03       04  
    ['fatur', 'rocky', 'rahmat', 'calvin', 'rais', 'nadel'], // baris ke 1
//     10       11         12        13       14      15
    ['nadia', 'kasfi', 'dea', 'kosong', 'adel', 'chris'], // baris ke 2
//     20        21      22      23      24         25
    ['tristan', 'kosong', 'benita', 'agung', 'joseph', 'robin', 'hasir'] // baris ke 3
//      30          31        32        33      34        35       36          
]


// accessing element in multi-dimentional array
console.log(students[2][2])
console.log(students[3][4][0])
console.log(students[0][0], students[3][3], students[3][3][1]);

//how to accessing every element in multi-dimentional array
for(let baris = 0; baris < students.length; baris++){
    let name = ""
    // console.log(students[baris]);
    let perBaris = students[baris]
    for(let coloumn = 0; coloumn < perBaris.length; coloumn++){
        let student = perBaris[coloumn]
        console.log(student)
    }
}   

//or you can use this way
for(let perBaris of students){
    for(let student of perBaris){
        console.log(student)
    }
}


//change value in array multi dimensi
students[0][4] = 'hamim' 


```

# References for Self-Taught

![](https://media2.giphy.com/media/j1Xyt3DHfJcmk/200.webp?cid=ecf05e47212x7wjpd6cexz5ccj1hmfvpym003js8cwknf6vl&rid=200.webp&ct=g)

- [Functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Functions)
- [Arrow Functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions)
- [Default Parameters](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Default_parameters)
- [Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)
- [Multi-dimentional Array](https://www.geeksforgeeks.org/javascript-multidimensional-array/)

## Video References

- [Array](https://youtu.be/CW5pfpafgDE)
- [Functions](https://youtu.be/6-UqHXBtYkg)
