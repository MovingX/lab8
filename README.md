<h1 align="center"> МИНИСТЕРСТВО НАУКИ И ВЫСШЕГО ОБРАЗОВАНИЯ РОССИЙСКОЙ ФЕДЕРАЦИИ ФЕДЕРАЛЬНОЕ ГОСУДАРСТВЕННОЕ БЮДЖЕТНОЕ ОБРАЗОВАТЕЛЬНОЕ УЧРЕЖДЕНИЕ ВЫСШЕГО ОБРАЗОВАНИЯ «САХАЛИНСКИЙ ГОСУДАРСТВЕННЫЙ УНИВЕРСИТЕТ»</h1>
<br>
<br>
<br>
<br>
<br>
<br>
<p align="center">Лабораторная работа №8</p>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<p align="right">Выполнил: Морошкин Максим Александрович</p>
<p align="right">Проверил: Соболев Е. И.</p>
<br>
<br>
<br>
<br>
<br>
<br>

<p align="center">г. Южно-Сахалинск <br> 2023 год</p>

<h2 align="center">Введение</h2>
<p align="justify">Задачи на JavaScript</p>

<h2>Цели и задачи</h2>
Задачи:
1.	Напишите оператор if, такой, чтобы в качестве выражения в скобках у него были значения true, false (Например, if( true ) или if( false )). Посмотрите как работает этот оператор, поместив какую-нибудь команду после круглых скобок (Например, console.log(1)). 

2.	Создайте переменные m и n. В m поместите произвольное числовое значение. Напишите оператор ветвления if так, чтобы если m было больше 50, то в переменную n помещалось слово «большое», иначе — слово «маленькое».

3.	Определите сколько раз выполнится цикл while? Примечание: это можно сделать прочитав скрипт или запустив его консоли браузера.
var i = 2;
while( i < 9 ){
 	  console.log( i++ );
  }


4.	Напишите скрипт, который используя оператор while выведет все числа от 45 до 67.

5.	Напишите скрипт, который используя оператор while выведет все числа от 45 до 670, кратные 10.

6.	Напишите скрипт, который используя оператор for выполнит два предыдущих задания.

7.	Переменная n хранит целое число от 0 до 9. Используя оператор switch, написать скрипт, который в зависимости от числа будет выводить слово (Например, если n равно 3, то будет выводиться слово «три»)
var n = 5;
switch( n ){
 //Напишите тут свой код
}

8.	Используя document.write() и любую из циклических конструкций выведите  десять одинаковых изображений (надо выводить <img src="..." alt="..." />)

9.	В переменных size и unit хранятся размер и единицы измерения информации 120 и «Кб» соответственно. Зная что могут быть заданные Кб, Мб, Гб (кило-, мега- и гигабайты) и 1килобайт равен 1024 байта, найти количество байт в size.

10.	Постройте при помощи циклов JavaScript скрипт для календаря на HTML. Примечание: выполнить задание для одного месяца, используя HTML-элемент table

11.	Напишите функцию hello1(), которая при вызове будет возвращать строку «Привет, JavaScript!».

12.	Напишите функцию hello2(), которая при вызове будет принимать переменную name (например, «Василий») и выводить строку (в нашем случае «Привет, Василий»).  В случае отсутствующего аргумента выводить «Привет, гость»

13.	Напишите функцию mul(n,m), которая принимает два аргумента и возвращает произведение этих аргументов. Проверьте ее работу.


14.	Создайте функцию repeat(str, n), которая возвращает строку, состоящую и n повторений строки str. n — по умолчанию 2, str — пустая строка

15.	Создайте функцию rgb(), которая будет принимать три числовых аргумента и возвращать строку вида «rgb(23,100,134)». Если аргументы не заданы, считать их равными нулю. Не проверять переменные на тип данных

16.	Создайте функцию avg() , которая будет находить среднее значение по всем своим аргументам (аргументы величины числовые).

17.	Создайте функцию m(a,b) оболочку для mul(). m() должна принимать два аргумента а возвращать результат работы mul() с этими двумя аргументами После выполнения задания поэкспериментируйте, создайте функцию log(), которая будет принимать одно значение, а вызывать  console.log() с этим значением.

18.	Напишите функцию operation(m,n,o), в которой m и n — числовые переменные, а o — функциональный литерал, который берет два аргумента и выполняет математическую операцию над ними 


19.	Напишите функцию addN(n), которая вернёт другую функцию. Возвращенная функция должна складывать получаемый аргумент с аргументом n возвращающей функции. 

20.	Напишите функцию words(),  которая в зависимости от переданного в нее целочисленного аргумента n, будет выводить слово «товар» в нужно форме («12 товаров», но «22 товара»). По умолчанию аргумент d должен иметь значение 0


<h2>Решение задач</h2>

```html
<div class="Block1">	
			
			<h1>Задачи</h1>
			<button onclick="task1(true)">Задача 1 - true</button>
			<button onclick="task1(false)">Задача 1 - false</button>
			<br>		
			<button onclick="task2()">Задача 2</button><br>	
			<button onclick="task3()">Задача 3</button><br>	
			<button onclick="task4()">Задача 4</button><br>	
			<button onclick="task5()">Задача 5</button><br>	
			<button onclick="task6()">Задача 6</button><br>	
			<button onclick="task7()">Задача 7</button><br>
			<button onclick="task8()">Задача 8</button><br>
			<button onclick="task9()">Задача 9</button><br>
			<button onclick="task10()">Задача 10</button><br>
			<button onclick="alert(task11())">Задача 11</button><br>
			<button onclick="alert(task12())">Задача 12 - без имени</button>
			<button onclick="alert(task12('Василий'))">Задача 12 - с именеем</button>
			<br>
			<button onclick="alert(task13(3,5))">Задача 13</button><br>
			<button onclick="task14('пустая строка', 2)">Задача 14</button><br>
			<button onclick="task15(102,243,23)">Задача 15</button><br>
			<button onclick="alert(task16(1,2,3,4,5,6))">Задача 16</button><br>
			<button onclick="log(mul(3, 4))">Задача 17</button><br>
			<button onclick="alert(task18(2, 3, (a, b) => a ** b))">Задача 18</button><br>
			<button onclick="alert(task19(5)(3))">Задача 19</button><br>
			<button onclick="alert(task20(5))">Задача 20</button><br>

			<div id="result">Тут будет ответ!!!</div>
	
		</div>
		
		<script>
		
		function task1(value) {
			if (value) {
				console.log("Это true");
			} else {
				console.log("Это false");
			}
		}
		
		function task2() {
			var m = 51;
			if (m > 50) {
				var result = "большое";
			} else {
				var result = "маленькое";
			}
			document.getElementById("result").innerHTML = result;
		}
		
		function task3(){
			var i = 2;
			var result = 0;
			while( i < 9 ){
			console.log( i++ );
			result++;
			}
			document.getElementById("result").innerHTML = result;
		}
		
		function task4() {
			var i = 45;
			var stroka = "";
			while (i <= 67) {
				stroka +=i + " ";
				i++;
			}
			document.getElementById("result").innerHTML = stroka;
		}
		
		function task5() {
			var i = 50;
			var stroka = "";
			while (i <= 670) {
				stroka +=i + " ";
				i += 10;
			}
			document.getElementById("result").innerHTML = stroka;
		}
		
		function task6() {
			var stroka = "";
			// Task 4
			for (let i = 45; i <= 67; i++) {
				stroka +=i + " ";
			}
			
			// Task 5
			for (let i = 50; i <= 670; i += 10) {
				stroka +=i + " ";
			}
			document.getElementById("result").innerHTML = stroka;
		}
		
		function task7() {
			var n = 5;
			var word;
			switch (n) {
				case 0:
					word = "ноль";
					break;
				case 1:
					word = "один";
					break;
				case 2:
					word = "два";
					break;
				case 3:
					word = "три";
					break;
				case 4:
					word = "четыре";
					break;
				case 5:
					word = "пять";
					break;
				case 6:
					word = "шесть";
					break;
				case 7:
					word = "семь";
					break;
				case 8:
					word = "восемь";
					break;
				case 9:
					word = "девять";
					break;
			}
			document.getElementById("result").innerHTML = word;
		}
		
		function task8() {
			var img = ''
			for (var i = 0; i < 10; i++) {
				document.write('<img src="Dog.jpg" alt="изображение">') ;
			}
		}
		
		function task9() {
			var size = 120;
			var unit = "Кб";
			var byteCount;
				switch (unit) {
					case "Кб":
						byteCount = size * 1024;
						break;
					case "Мб":
						byteCount = size * 1024 * 1024;
						break;
					case "Гб":
						byteCount = size * 1024 * 1024 * 1024;
						break;

				}
			document.getElementById("result").innerHTML = byteCount + " байт";
		}
		
		//task10
		
		function task10(){
			var date = new Date();
			var year = date.getFullYear();
			var month = date.getMonth();
			var daysInMonth = new Date(year, month, 0).getDate();
			var firstDay = new Date(year, month, 1).getDay();
			var lastDay = new Date(year, month, daysInMonth).getDay();

			var calendar = "<table>";
			calendar += "<tr><th colspan='7'>" + year + " " + getMonthName(month) + "</th></tr>";
			calendar += "<tr><th>Пн</th><th>Вт</th><th>Ср</th><th>Чт</th><th>Пт</th><th>Сб</th><th>Вс</th></tr>";

			var dateCount = 1;
			for (var i = 0; i < 6; i++) {
				calendar += "<tr>";
				for (var j = 0; j < 7; j++) {
					if ((i == 0 & j < firstDay) || (i == 5 & j > lastDay)) {
						calendar += "<td></td>";
					} else {
						calendar += "<td>" + dateCount + "</td>";
						dateCount++;
					}
				}
				calendar += "</tr>";
			}
			calendar += "</table>";
			document.getElementById("result").innerHTML = calendar;
		}

		function getMonthName(month) {
			months = ["Январь", "Февраль", "Март", "Апрель", "Май", "Июнь", "Июль", "Август", "Сентябрь", "Октябрь", "Ноябрь", "Декабрь"];
			return months[month];
		}
		
		
		function task11() {
			return "Привет, JavaScript!";
		}
		
		function task12(name) {
			if (name) {
				return "Привет, " + name;
			} else {
				return "Привет, гость";
			}
		}	
		
		function task13(n, m) {
			return n * m;
		}
		
		function task14(str, n) {
			var result="";
			for (var i = 0; i < n; i++) {
				result +=str + " ";
			}
			document.getElementById("result").innerHTML = result;
		}
		
		function task15(a,b,c){
			var result="";
			if(a)
			{
				result +=a + ",";
			}
			else{ result +="0,";}
			
			if(b)
			{
				result +=b + ",";
			}
			else{ result +="0,";}
			
			if(c)
			{
				result +=c;
			}
			else{ result +="0";}
			
			document.getElementById("result").innerHTML = "rgb("+ result + ")";
		}
		
		function task16(...args)
		{
			var result = 0;
			for(var i = 0; i < args.length; i++) result+= args[i];
			return result / args.length;
		}
		
		//task17
		function mul(a, b) {
			return a * b;
		}

		function m(a, b) {
			return mul(a, b);
		}

		function log(value) {
			console.log(value);
		}
		
		function task18(m, n, o) {
			return o(m, n);
		}
		
		function task19(n) {
			return function(x) {
				return x + n;
			};
		}
		
		function task20(n) {
			var remainder = n % 10;
			if (remainder === 1 && n !== 11) {
				return n + ' товар';
			} else if ((remainder >= 2 && remainder <= 4) && (n < 10 || n > 20)) {
				return n + ' товара';
			} else {
				return n + ' товаров';
			}
		}
		
		</script>		
```

<h2>Вывод</h2>
Я зибора научился работать с JS
