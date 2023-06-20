# Методы JavaScript
Методы JavaScript — это действия, которые можно выполнять над объектами.

Метод JavaScript — это свойство, содержащее определение функции .

Методы — это функции, хранящиеся в виде свойств объекта.

# Нить
Объект Stringиспользуется для представления и управления последовательностью символов.
# Описание
Строки полезны для хранения данных, которые могут быть представлены в текстовой форме. Некоторые из наиболее часто используемых операций со строками — это проверка их **length**, их построение и объединение с помощью **строковых операторов + и +=** , проверка существования или расположения подстрок с помощью **indexOf()**метода или извлечение подстрок с помощью этого **substring()**метода.
## Создание строк
Строки могут быть созданы как примитивы, из строковых литералов или как объекты с помощью **String()** конструктора:
1. const string1 = "A string primitive";
2. const string2 = 'Also a string primitive';
3. const string3 = `Yet another string primitive`;

- const string4 = new String("A String object");

Строковые примитивы и строковые объекты имеют много общего поведения, но имеют другие важные отличия и предостережения. См. раздел " [Примитивы String и объекты String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String#string_primitives_and_string_objects) " ниже.

Строковые литералы можно указывать с помощью одинарных или двойных кавычек, которые обрабатываются одинаково, или с помощью символа обратной кавычки `. Эта последняя форма определяет литерал шаблона : с помощью этой формы вы можете интерполировать выражения. Дополнительные сведения о синтаксисе строковых литералов см. в разделе лексическая грамматика .

#### JAVA SCRIPT STRING METHODS 
- ➢ charAt() 
- ➢ concat()
- ➢ trim() 
- ➢ includes() 
- ➢ indexOf()
- ➢ replace() 
- ➢ replaceAll() 
- ➢ repeat() 
- ➢ slice()
- ➢ substring()
- ➢ plit()
- ➢ tring()
- ➢ werCase()
- ➢ toUpperCase()

# Доступ персонажа
Есть два способа получить доступ к отдельному символу в строке. Первый метод **charAt()**:
- "cat".charAt(1); // gives value "a"

Другой способ — рассматривать строку как объект, подобный массиву, где отдельные символы соответствуют числовому индексу:
- "cat"[1]; // gives value "a"

# Сравнение строк
Используйте [операторы меньше и больше](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators) для сравнения строк:
- const a = "a";
const b = "b";
if (a < b) {
  // true
  console.log(`${a} is less than ${b}`);
} else if (a > b) {
  console.log(`${a} is greater than ${b}`);
} else {
  console.log(`${a} and ${b} are equal.`);
}

Обратите внимание, что все операторы сравнения, включая **===и ==**, сравнивают строки с учетом регистра. Распространенным способом сравнения строк без учета регистра является преобразование обеих строк в один и тот же регистр (верхний или нижний) перед их сравнением.
- function areEqualCaseInsensitive(str1, str2) {
  return str1.toUpperCase() === str2.toUpperCase();
}

# Сводка      "concat()"

Метод concat() объединяет текст из двух или более строк и возвращает новую строку 
###### Описание
Метод concat() объединяет текст из двух или более строк и возвращает новую строку. Изменения в тексте в одной строке не затрагивают остальные строки.
###### Примеры
Пример: использование метода concat()
В следующем примере несколько строк объединяются в одну.
- var hello = 'Привет, ';
console.log(hello.concat('Кевин', ', удачного дня.'));
/* Привет, Кевин, удачного дня. */

### String.prototype.replace()
Метод replace()возвращает новую строку с одним, несколькими или всеми совпадениями, patternзамененными на replacement. Может patternбыть строкой или RegExp, а также replacementможет быть строкой или функцией, вызываемой для каждого совпадения. Если patternэто строка, будет заменено только первое вхождение. Исходная строка остается неизменной.
- const p = 'The quick brown fox jumps over the lazy dog. If the dog reacted, was it really lazy?';
console.log(p.replace('dog', 'monkey'));
// Expected output: "The quick brown fox jumps over the lazy monkey. If the dog reacted, was it really lazy?"
-  const regex = /Dog/i;
console.log(p.replace(regex, 'ferret'));
// Expected output: "The quick brown fox jumps over the lazy ferret. If the dog reacted, was it really lazy?"

#### String.prototype.split()
Метод split()принимает шаблон и делит его [String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) на упорядоченный список подстрок путем поиска шаблона, помещает эти подстроки в массив и возвращает массив.
- const str = 'The quick brown fox jumps over the lazy dog.';
const words = str.split(' ');
console.log(words[3]);
// Expected output: "fox"
- const chars = str.split('');
console.log(chars[8]);
// Expected output: "k"
- const strCopy = str.split();
console.log(strCopy);
// Expected output: Array ["The quick brown fox jumps over the lazy dog."]

#### String.prototype.trim()
Метод trim()удаляет пробелы с обоих концов строки и возвращает новую строку без изменения исходной строки.

Чтобы вернуть новую строку с пробелами, обрезанными только с одного конца, используйте **trimStart()** или **trimEnd()**.
- const greeting = '   Hello world!   ';
console.log(greeting);
// Expected output: "   Hello world!   ";
console.log(greeting.trim());
// Expected output: "Hello world!";

#### Array.prototype.includes()
Метод includes() определяет, содержит ли массив определённый элемент, возвращая в зависимости от этого true или false.
- const array1 = [1, 2, 3];
console.log(array1.includes(2));
// Expected output: true
- const pets = ['cat', 'dog', 'bat'];
console.log(pets.includes('cat'));
// Expected output: true
- console.log(pets.includes('at'));
// Expected output: false

###### JavaScript Number methods
1. Math.ceil()
Возвращает наименьшее целое число, большее или равное x.
2. Math.floor()
Возвращает наибольшее целое число, меньшее или равное x.
3. Math.max()
Возвращает наибольшее из нуля или более чисел.
4. Math.min()
Возвращает наименьшее из нуля или более чисел.
5.Math.pow()
Возвращает основание xстепени степени y(то есть x^y).
6. Math.random()
Возвращает псевдослучайное число между 0и 1.
7. Math.round()
Возвращает значение числа x, округленное до ближайшего целого числа.
8. Math.sqrt()
Возвращает положительный квадратный корень из x.
9. Math.abs()
Возвращает абсолютное значение x.





