Массив 
В отличие от переменных, массив может хранить несколько значений. Каждое значение в массиве имеет индекс, а каждый индекс имеет ссылку в адресе памяти. Каждое значение может быть доступно с помощью их индексов. Индекс массива начинается с 0, а последний элемент на единицу меньше длины массива.

Массив - это коллекция различных типов данных, которые упорядочены и изменяемы (модифицируемы). Массив позволяет хранить повторяющиеся элементы и различные типы данных. Массив может быть пустым или иметь разные значения типа данных.


Как создать пустой массив :
В JavaScript мы можем создать массив различными способами. Давайте по-разному создадим массив. Очень часто используется const вместо let для объявления переменной массива. Если вы используете const, это означает, что вы больше не используете это имя.

- Используя конструктор  Array
```
// синтаксис 
const arr = Array(); 
// or 
// let arr = new Array() 
console.log(arr); // []
```

- Используя квадратные скобки 
```
// синтаксис 
// Это наиболее рекомендуемый способ создания пустого списка 
const arr = []; 
console.log(arr);
```

Как создать массив со значениями 
Массив с начальными значениями . Мы используем свойство  lenght ,  чтоб найти длину массива :

```
const numbers = [0, 3.14, 9.81, 37, 98.6, 100]; // массив из чисел 
const fruits = ["banana", "orange", "mango", "lemon"]; // массив из строк, fruits 
const vegetables = ["Tomato", "Potato", "Cabbage", "Onion", "Carrot"]; // массив из строк, vegetables 
const animalProducts = ["milk", "meat", "butter", "yoghurt"]; // массив из строк, products 
const webTechs = ["HTML", "CSS", "JS", "React", "Redux", "Node", "MongDB"]; // массив из веб технологий 
const countries = ["Finland", "Denmark", "Sweden", "Norway", "Iceland"]; // массив из строк, countries 
// Распечатать массив и его длину 
console.log("Numbers:", numbers); 
console.log("Number of numbers:", numbers.length); 
console.log("Fruits:", fruits); 
console.log("Number of fruits:", fruits.length); 
console.log("Vegetables:", vegetables); 
console.log("Number of vegetables:", vegetables.length); 
console.log("Animal products:", animalProducts); 
console.log("Number of animal products:", animalProducts.length); 
console.log("Web technologies:", webTechs); 
console.log("Number of web technologies:", webTechs.length); 
console.log("Countries:", countries); 
console.log("Number of countries:", countries.length);
```

```
Numbers: [0, 3.14, 9.81, 37, 98.6, 100] 
Number of numbers: 6 
Fruits: ['banana', 'orange', 'mango', 'lemon'] 
Number of fruits: 4 
Vegetables: ['Tomato', 'Potato', 'Cabbage', 'Onion', 'Carrot'] 
Number of vegetables: 5 
Animal products: ['milk', 'meat', 'butter', 'yoghurt'] 
Number of animal products: 4 
Web technologies: ['HTML', 'CSS', 'JS', 'React', 'Redux', 'Node', 'MongDB'] 
Number of web technologies: 7 
Countries: ['Finland', 'Estonia', 'Denmark', 'Sweden', 'Norway'] 
Number of countries: 5
```

- Массив может иметь элементы разных типов данных
```
const arr = [ 
  "Asabeneh", 
  250, 
  true, 
  { country: "Finland", city: "Helsinki" }, 
  { skills: ["HTML", "CSS", "JS", "React", "Python"] } 
]; // arr содержит разные типы данных 
console.log(arr);
```

Создание массива с использование split :

Как мы видели в предыдущем разделе, мы можем разбить строку в разных позициях и перейти в массив. Давайте посмотрим на примеры ниже.

```
let js = "JavaScript"; 
const charsInJavaScript = js.split(""); 
console.log(charsInJavaScript); // ["J", "a", "v", "a", "S", "c", "r", "i", "p", "t"] 
let companiesString = "Facebook, Google, Microsoft, Apple, IBM, Oracle, Amazon"; 
const companies = companiesString.split(","); 
console.log(companies); // ["Facebook", " Google", " Microsoft", " Apple", " IBM", " Oracle", " Amazon"] 
let txt = 
  "I love teaching and empowering people. I teach HTML, CSS, JS, React, Python."; 
const words = txt.split(" "); 
console.log(words); 
// в тексте есть специальные символы, подумайте, как можно получить только слова 
// ["I", "love", "teaching", "and", "empowering", "people.", "I", "teach", "HTML,", "CSS,", "JS,", "React,", "Python"]
```

Доступ к элементам массива по индексу 
Мы получаем доступ к каждому элементу в массиве, используя их индекс. Индекс массива начинается с 0.

```
const fruits = ["banana", "orange", "mango", "lemon"]; 
let firstFruit = fruits[0]; // мы получаем доступ к первому элементу, используя его индекс 
console.log(firstFruit); // banana 
secondFruit = fruits[1]; 
console.log(secondFruit); // orange 
let lastFruit = fruits[3]; 
console.log(lastFruit); // lemon 
// Последний индекс можно рассчитать следующим образом 
let lastIndex = fruits.length - 1; 
lastFruit = fruits[lastIndex]; 
console.log(lastFruit); // lemon
```

```
const numbers = [0, 3.14, 9.81, 37, 98.6, 100]; // набор чисел 
console.log(numbers.length); // => узнать размер массива, который 6 
console.log(numbers); // -> [0, 3.14, 9.81, 37, 98.6, 100] 
console.log(numbers[0]); //  -> 0 
console.log(numbers[5]); //  -> 100 
let lastIndex = numbers.length - 1; 
console.log(numbers[lastIndex]); // -> 100
```

```
const webTechs = [ 
  "HTML", 
  "CSS", 
  "JavaScript", 
  "React", 
  "Redux", 
  "Node", 
  "MongoDB" 
]; // Список веб-технологий 
console.log(webTechs); // все элементы массива 
console.log(webTechs.length); // => узнать размер массива, который 7 
console.log(webTechs[0]); //  -> HTML 
console.log(webTechs[6]); //  -> MongoDB 
let lastIndex = webTechs.length - 1; 
console.log(webTechs[lastIndex]); // -> MongoDB
```

```
const countries = [ 
  "Albania", 
  "Bolivia", 
  "Canada", 
  "Denmark", 
  "Ethiopia", 
  "Finland", 
  "Germany", 
  "Hungary", 
  "Ireland", 
  "Japan", 
  "Kenya" 
]; // Список стран 
console.log(countries); // -> все страны в масиве 
console.log(countries[0]); //  -> Albania 
console.log(countries[10]); //  -> Kenya 
let lastIndex = countries.length - 1; 
console.log(countries[lastIndex]); //  -> Kenya
```

```
const shoppingCart = [ 
  "Milk", 
  "Mango", 
  "Tomato", 
  "Potato", 
  "Avocado", 
  "Meat", 
  "Eggs", 
  "Sugar" 
]; // Список продуктов питания 
console.log(shoppingCart); // -> все shoppingCart в массиве 
console.log(shoppingCart[0]); //  -> Milk 
console.log(shoppingCart[7]); //  -> Sugar 
let lastIndex = shoppingCart.length - 1; 
console.log(shoppingCart[lastIndex]); //  -> Sugar
```

Изменение элемента массива 
Массив является изменяемым (модифицируемым). После создания массива мы можем изменить содержимое элементов массива.

```
const numbers = [1, 2, 3, 4, 5]; 
numbers[0] = 10; // изменение 1 на индекс 0 до 10 
numbers[1] = 20; // изменение 2 на индекс 1 до 20 
console.log(numbers); // [10, 20, 3, 4, 5] 
const countries = [ 
  "Albania", 
  "Bolivia", 
  "Canada", 
  "Denmark", 
  "Ethiopia", 
  "Finland", 
  "Germany", 
  "Hungary", 
  "Ireland", 
  "Japan", 
  "Kenya" 
]; 
countries[0] = "Afghanistan"; // Замена Albania на Afghanistan 
let lastIndex = countries.length - 1; 
countries[lastIndex] = "Korea"; // Замена Kenya на Korea 
console.log(countries);
```

```
["Afghanistan", "Bolivia", "Canada", "Denmark", "Ethiopia", "Finland", "Germany", "Hungary", "Ireland", "Japan", "Korea"]
```

Методы манипулирования массивом 
Существуют разные методы манипулирования массивом. Вот некоторые из доступных методов для работы с массивами: Array, length, concat, indexOf, slice, splice, join, toString, includes, lastIndexOf, isArray, fill, push, pop, shift, unshift


Конструктор массива

Массив: для создания массива.
```
const arr = Array(); // создает пустой массив 
console.log(arr); 
const eightEmptyValues = Array(8); // он создает восемь пустых значений 
console.log(eightEmptyValues); // [empty x 8]
```

Создание массивов со значением 

```
const arr = Array(); // создает пустой массив 
console.log(arr); 
const eightXvalues = Array(8).fill("X"); // он создает восемь значений элементов, заполненных 'X' 
console.log(eightXvalues); // ['X', 'X','X','X','X','X','X','X'] 
const eight0values = Array(8).fill(0); // он создает восемь значений элементов, заполненных '0' 
console.log(eight0values); // [0, 0, 0, 0, 0, 0, 0, 0] 
const four4values = Array(4).fill(4); // он создает 4 значения элемента, заполненные '4' 
console.log(four4values); // [4, 4, 4, 4]
```


Конкатенация массива с использованием concat 



concat: объединение двух массивов.

```
const firstList = [1, 2, 3];
const secondList = [4, 5, 6];
const thirdList = firstList.concat(secondList);

console.log(thirdList); // [1, 2, 3, 4, 5, 6]
```




```
const fruits = ["banana", "orange", "mango", "lemon"]; // массив из fruits
const vegetables = ["Tomato", "Potato", "Cabbage", "Onion", "Carrot"]; // массив из vegetables
const fruitsAndVegetables = fruits.concat(vegetables); // объединение двух массивов

console.log(fruitsAndVegetables);
```

Получение длинны массива :
length: чтобы узнать размер массива

```
const numbers = [1, 2, 3, 4, 5];
console.log(numbers.length); // -> 5 это размер массива
```


Получение индекса элемента в массиве arr

indexOf: проверить, существует ли элемент в массиве. Если он существует, он возвращает индекс, иначе он возвращает -1.

```
const numbers = [1, 2, 3, 4, 5];

console.log(numbers.indexOf(5)); // -> 4
console.log(numbers.indexOf(0)); // -> -1
console.log(numbers.indexOf(1)); // -> 0
console.log(numbers.indexOf(6)); // -> -1
```

Проверьте элемент, если он существует в массиве.

- Проверьте элементы в списке
```
// давайте проверим, существует ли banana в массиве

const fruits = ["banana", "orange", "mango", "lemon"];
let index = fruits.indexOf("banana"); // 0

if (index != -1) {
  console.log("Этот фрукт существует в массиве");
} else {
  console.log("Этот фрукт не существует в массиве");
}
// Этот фрукт существует в массиве

// мы можем использовать также тернарный оператор здесь
index != -1
  ? console.log("Этот фрукт существует в массиве")
  : console.log("Этот фрукт не существует в массиве");

// давайте проверим, существует ли в массиве avocado
let indexOfAvocado = fruits.indexOf("avocado"); // -1, если элемент не найден, индекс -1
if (indexOfAvocado != -1) {
  console.log("Этот фрукт существует в массиве");
} else {
  console.log("Этот фрукт не существует в массиве");
}
// Этот фрукт не существует в массиве
```


Получение последнего индекса элемента в массиве

lastIndexOf: отдает позицию последнего элемента в массиве. Если он существует, он возвращает индекс, иначе он возвращает -1.

```
const numbers = [1, 2, 3, 4, 5, 3, 1, 2];

console.log(numbers.lastIndexOf(2)); // 7
console.log(numbers.lastIndexOf(0)); // -1
console.log(numbers.lastIndexOf(1)); //  6
console.log(numbers.lastIndexOf(4)); //  3
console.log(numbers.lastIndexOf(6)); // -1
```

includes в себя: чтобы проверить, существует ли элемент в массиве. Если он существует, он возвращает истину, иначе он возвращает ложь.

```
const numbers = [1, 2, 3, 4, 5];

console.log(numbers.includes(5)); // true
console.log(numbers.includes(0)); // false
console.log(numbers.includes(1)); // true
console.log(numbers.includes(6)); // false

const webTechs = [
  "HTML",
  "CSS",
  "JavaScript",
  "React",
  "Redux",
  "Node",
  "MongoDB"
]; // Список веб-технологий

console.log(webTechs.includes("Node")); // true
console.log(webTechs.includes("C")); // false
```


Проверка массива

Array.isArray: чтобы проверить, является ли тип данных массивом

```
const numbers = [1, 2, 3, 4, 5];
console.log(Array.isArray(numbers)); // true

const number = 100;
console.log(Array.isArray(number)); // false
```


Преобразование массива в строку

toString: преобразовывает массив в строку

```
const numbers = [1, 2, 3, 4, 5];
console.log(numbers.toString()); // 1,2,3,4,5

const names = ["Asabeneh", "Mathias", "Elias", "Brook"];
console.log(names.toString()); // Asabeneh,Mathias,Elias,Brook
```


Объединение элементов массива

join: используется для соединения элементов массива, аргумент, переданный в методе join, будет объединен в массив и возвращен в виде строки. По умолчанию он соединяется запятой, но мы можем передать другой строковый параметр, который можно объединить между элементами. 



```
const numbers = [1, 2, 3, 4, 5]; 
console.log(numbers.join()); // 1,2,3,4,5 
const names = ["Asabeneh", "Mathias", "Elias", "Brook"]; 
console.log(names.join()); // Asabeneh,Mathias,Elias,Brook 
console.log(names.join("")); //AsabenehMathiasEliasBrook 
console.log(names.join(" ")); //Asabeneh Mathias Elias Brook 
console.log(names.join(", ")); //Asabeneh, Mathias, Elias, Brook 
console.log(names.join(" # ")); //Asabeneh # Mathias # Elias # Brook 
const webTechs = [ 
  "HTML", 
  "CSS", 
  "JavaScript", 
  "React", 
  "Redux", 
  "Node", 
  "MongoDB" 
]; // Список веб-технологий 
console.log(webTechs.join()); // "HTML,CSS,JavaScript,React,Redux,Node,MongoDB" 
console.log(webTechs.join(" # ")); // "HTML # CSS # JavaScript # React # Redux # Node # MongoDB"
```



Элементы массива срезов

slice: вырезает несколько предметов из диапазона. Требуется два параметра: начальная и конечная позиция. Это не включает в себя конечную позицию. 



```
const numbers = [1, 2, 3, 4, 5]; 
console.log(numbers.slice()); // -> it copies all  item 
console.log(numbers.slice(0)); // -> it copies all  item 
console.log(numbers.slice(0, numbers.length)); // it copies all  item 
console.log(numbers.slice(1, 4)); // -> [2,3,4] // it doesn't include the ending position
```


Метод сращивания в массиве

splice: требуется три параметра: начальная позиция, количество удалений и количество добавляемых элементов.

```
const numbers = [1, 2, 3, 4, 5];

console.log(numbers.splice()); // -> удалить все предметы
```

```
const numbers = [1, 2, 3, 4, 5];
console.log(numbers.splice(0, 1)); // удалить первый элемент
```

```
const numbers = [1, 2, 3, 4, 5];
console.log(numbers.splice(3, 3, 6, 7, 8)); // -> [1, 2, 3, 6, 7, 8] // удаляет два элемента 
```



Добавление элемента в массив с помощью push

push: добавление элемента в конце. Чтобы добавить элемент в конец существующего массива, мы используем метод push.

```
// синтаксис
const arr = ["item1", "item2", "item3"];
arr.push("new item");

console.log(arr);
// ['item1', 'item2','item3','new item']
```

```
const numbers = [1, 2, 3, 4, 5];
numbers.push(6);

console.log(numbers); // -> [1,2,3,4,5,6]

numbers.pop(); // -> убрать один предмет с конца
console.log(numbers); // -> [1,2,3,4,5]
```

```
let fruits = ["banana", "orange", "mango", "lemon"];
fruits.push("apple");

console.log(fruits); // ['banana', 'orange', 'mango', 'lemon', 'apple']

fruits.push("lime");
console.log(fruits); // ['banana', 'orange', 'mango', 'lemon', 'apple', 'lime']
```

Удаление конечного элемента с помощью pop

pop: удаление элемента в конце.

```
const numbers = [1, 2, 3, 4, 5];
numbers.pop(); // -> убрать один предмет с конца

console.log(numbers); // -> [1,2,3,4]
```

Удаление элемента с самого начала

shift: удаление одного элемента массива в начале массива.

```
const numbers = [1, 2, 3, 4, 5];
numbers.shift(); // -> удаление одного элемента с начала

console.log(numbers); // -> [2,3,4,5]
```

Добавить элемент с начала

unshift: добавление элемента массива в начало массива.

```
const numbers = [1, 2, 3, 4, 5];
numbers.unshift(0); // -> добавить один элемент с начала

console.log(numbers); // -> [0,1,2,3,4,5]
```



Обратный порядок массивов

reverse: обратный порядок массива.

```
const numbers = [1, 2, 3, 4, 5];
numbers.reverse(); // -> обратный порядок массива

console.log(numbers); // [5, 4, 3, 2, 1]

numbers.reverse();
console.log(numbers); // [1, 2, 3, 4, 5]
```


Сортировка элементов в массиве

sort: расположить элементы массива в порядке возрастания. Сортировка принимает функцию обратного вызова, мы увидим, как мы используем сортировку с функцией обратного вызова в следующих разделах.

```
const webTechs = [
  "HTML",
  "CSS",
  "JavaScript",
  "React",
  "Redux",
  "Node",
  "MongoDB"
];

webTechs.sort();
console.log(webTechs); // ["CSS", "HTML", "JavaScript", "MongoDB", "Node", "React", "Redux"]

webTechs.reverse(); // после сортировки мы можем изменить это
console.log(webTechs); // ["Redux", "React", "Node", "MongoDB", "JavaScript", "HT
```


Массив массивов

Массив может хранить различные типы данных, включая сам массив. Давайте создадим массив массивов

```
const firstNums = [1, 2, 3];
const secondNums = [1, 4, 9];

const arrayOfArray = [
  [1, 2, 3],
  [1, 2, 3]
];
console.log(arrayOfArray[0]); // [1, 2, 3]

const frontEnd = ["HTML", "CSS", "JS", "React", "Redux"];
const backEnd = ["Node", "Express", "MongoDB"];
const fullStack = [frontEnd, backEnd];
console.log(fullStack); // [["HTML", "CSS", "JS", "React", "Redux"], ["Node", "Express", "MongoDB"]]
console.log(fullStack.length); // 2
console.log(fullStack[0]); // ["HTML", "CSS", "JS", "React", "Redux"]
console.log(fullStack[1]); // ["Node", "Express", "MongoDB"]
```


