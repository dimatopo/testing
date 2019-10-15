## Доклад на тему: Что такое Unicode, UTF-16 и UTF-8




### Оглавление 



1. Вступление, немного истории

2. Кодировка ASCII
	
3. Что такое Unicode, UTF-16 и UTF-8  

4. Заключение  

<br />
<br />
  
#### 1. Вступление, немного истории  


<p align="justify">Текст</p>
<p align="justify">
С древнейших времен, на заре зарождения разума у первобытного человека, уже тогда появилась необходимость передачи информации. Сначала это были простейшие звуки издаваемые гортанью кем-то из соплеменников – они позволили первобытным людям предупреждать друг друга об опасности, о найденной пище и пр. Потом, количество звуков увеличивалось, они становились сложнее – звуки превращались в слова, зарождалась устная речь!<br />  
</p>
<p align="justify">
Именно тогда человечество изобрело первый способ передачи и кодирования информации. Вы даже не можете себе представить, насколько устная речь подстегнула развитие человечества! Теперь члены одного племени могли скоординировать свои действия во время охоты, собирательства плодов, переходах от одного места стоянки племени к другому и т.д., что в свою очередь пользу положительно сказывалось на уровне жизни этого племени.  
</p>
<p align="justify">
Уже тогда было подмечено, что люди из разных племен не всегда понимают речь друг друга. По сути дела один индивидуум не мог понять закодированного посредством звуков информационного сообщения другого индивидуума! Поверьте, когда возникали такие «сложности в общении», для кого-то это заканчивалось не очень хорошо ))).  
</p>
<p align="justify">
Постепенно у людей тех дремучих веков назрела необходимость придумать новый способ кодировки и передачи простейшей информации между теми, кто не мог понять речь друг друга. Это был способ рисования картинок, т.е. графический способ. При помощи этого способа люди смогли не только передавать, но и сохранять информацию в течение длительного времени. Наверное, всем известна наскальная живопись? (вставить ссылку на рисунок наскальной живописи) Часть ученых считает, что это не только искусство древних, но это еще (причем в первую очередь) и инструкции  для различных жизненных ситуаций оставляемых последующим поколениям.  
</p>
<p align="justify">
С течением времени (довольно продолжительного надо сказать), развитием устной речи, да и человечества в целом, назрела необходимость сохранения такой информации, которая уже не могла быть представлена простейшим рисунком на скале. Рисунки постепенно усложнялись, становились похожими на символы, символов становилось все больше и больше.… Так появилась письменность. Первая письменность возникла 5000 лет назад в шумерской цивилизации и называлась клинопись (вставить ссылку на википедию).  
</p>
<p align="justify">
Все дальнейшие столетия и до наших дней, письменность развивалась, усложнялась, появлялись и исчезали алфавиты, возникла наука криптография (вставить ссылку на википедию) (наука изучающая методы шифрования данных при помощи).  
</p>
<p align="justify">
К середине 19-го века у человечества появилась возможность передачи информации при помощи проводов, а в последующем и при помощи радио волн. Кодировка информации в этом случае осуществлялась при помощи кода Морзе (вставить ссылку на википедию). Думаю, что пояснения тут не уместны, т.к. всем известна Азбука Морзе – последовательность длинных (тире) и коротких (точка) сигналов, при помощи которых закодированы буквы, цифры, а так же знаки препинания алфавита.  
</p>
<p align="justify">
В конце вступительного слова, справедливости ради, хотелось бы отметить еще два оригинальных способа кодирования информации придуманных для людей с ограниченными возможностями. Это сурдоперевод (язык жестов) для тех, кто плохо слышит и азбуку Брайля  для тех, кто плохо видит.  
</p>
<p align="justify">
Примерно в середине 20 века после окончания Второй мировой войны, для решения широкого спектра задач, распространение получили ЭВМ (электронно-вычислительные машины). Проблему кодировки информации для расчета в таких ЭВМ каждый разработчик решал по своему, что в скором времени привело к полной неразберихе.
</p>	
<br />
<br />
  

#### 2. Кодировка ASCII 
<p align="justify">
Лишь в начале 60-х годов 20-го века в США занялись проблемой стандартизации кодирования символов для компьютеров. Так на свет появился код ASCII  (American Standard Code for Information Interchange) – американский стандартный код для обмена информации. Он послужил прародителем для всех современных кодировок.  
</p>
<p align="justify">
Так как код был 7-ми битным, то общее количество символов в нем не превышало 2<sup>7</sup> =128 (см рис.1). Первые 32 символа были управляющими, а остальные изображаемыми, т.е. имели графическое изображение. 
</p>
 
![альт](https://ds04.infourok.ru/uploads/ex/0b2e/001665d5-80a5617c/img27.jpg "Таблица кодировки ASCII")  

<center>*Рис.1 Кодировка ASCII*</center>    
<br />
  
К изображаемым символам относят:

*	Буквы латинского алфавита (и строчные и прописные);  
*	Арабские цифры;
*	Знаки препинания и знаки арифметических операций;
*	Скобки и некоторые специальные символы.  
<p align="justify">
Стандарт ASCII был рассчитан  для передачи только английского текста. Каким образом передать текст не английского происхождения? Дело в том, что в один байт информации можно записать не 128 символов, а целых 256 значений (т.к. 2<sup>8</sup> =256). Если кто-то не помнит что такое байт, бит или двоичная система счисления, вам сначала [сюда](https://ru.wikipedia.org/wiki/%D0%94%D0%B2%D0%BE%D0%B8%D1%87%D0%BD%D0%B0%D1%8F_%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D0%B0_%D1%81%D1%87%D0%B8%D1%81%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F).  
</p>
Многие страны, взяв за основу ASCII, стали делать свои расширенные кодировки. В таких кодировках первые 128 символов совпадали с кодировкой ASCII, а следующие (со 129 по 256 символ) были использованы для кодировки букв национальных алфавитов, валют и пр. В нашей стране наибольшую популярность получили кодировки под названием CP866, KOI8-R, Windows 1251.
<br />
<br />

#### 3. Что такое Unicode, UTF-16 и UTF-8

Итак, мы выяснили, что расширенные кодировки – это старая-добрая ASCII плюс какой-то национальный алфавит с символами и элементами псевдографики. Постепенно под давлением технического прогресса DOS-системы стали вытесняться все более и более популярными графическими операционными системами и надобность в псевдографике отпала. Так же из-за большого количества кодировок (только в Росси их было больше десятка) у многих начались проблемы с передачей информации! Т.е. допустим, один человек отправил файл другому в кодировке KOI8-R, а у получателя такой кодировки не оказалось. Как результат конечный пользователь информации не может воспользоваться полученными данными. В таких случаях на экране монитора высвечивается что-то, похожее на рисунок 2:

![альт](https://webgyry.info/wp-content/uploads/2012/12/codifica-error.png "Таблица кодировки ASCII")
 
<center>*Рис.2 Ошибка кодировки ASCII*</center>    


В конце концов, это многим надоело, назрела необходимость создания чего-то нового, чего-то универсального, что смогло бы заменить собой все разнообразие уже созданных кодировок. Результатом этих чаяний стало создание консорциума под названием Unicode (*анг. - Unicode Consortium*). В этот консорциум влились все заинтересованные стороны – производители софта, программисты, создатели шрифтов и т.д. По сути, консорциум создал единое кодовое пространство с общим стандартом кодирования для всех письменных языков мира. Общее количество кодовых позиций в стандарте Юникод составляет 1 114 112 штук (диапазон от 0 до 10FFFF). Так же в обиход ввели понятие  юникод-символа – это абстрактный символ, имеющий свою кодовую позицию (code point) в кодовом пространстве Юникода, с присвоенным ему (символу) неотрицательным числом. Например, слово «Документ» в пространстве Юникода будет выглядеть следующим образом:  

<center>U+0414  U+043E  U+043A  U+0443  U+043C  U+0435  U+043D  U+0442,</center>
зная Юникод, теперь любой человек в мире сможет декодировать этот код обратно в написанное на кириллице слово «Документ».  

Первым детищем консорциума стала кодировка под названием **UTF-32** (анг - Unicode Transformation Format). Цифра 32 в названии кодировки обозначает, что именно 32 бита информации (или 4 байта)  вам понадобится для кодировки одного символа или знака. Т.е. теперь, чтобы закодировать 1 символ надо потратить уже не 1 байт, а 4. Т.е. файл закодированный с помощью UTF-32 будет «весить» в 4 раза больше, чем файл с такой же информацией, но закодированный при помощи ASCII. При кажущемся недостатке появился и плюс в виде практически неограниченного количества символов, которые можно было бы закодировать при помощи UTF-32, ведь 2^32 = 4 294 967 296. Такой «запас» в количестве символов сделали в угоду странам Азии, где количество иероглифов было на много больше, чем умещалось в кодировке ASCII (напомню, что в ASCII максимальное количество символов равняется 2^8= 256). Европейские страны не смогли смириться с UTF-32, так как не собирались использовать такое количество символов, а это значит, что система была избыточна. Плюс, напомню, файлы, закодированные в UTF-32 становились «тяжелее» в 4 раза, чем фалы с кодировкой ASCII, а это влекло за собой увеличение интернет-трафика и объема хранимой информации.  

Дальнейшим развитием кодировки стало создание **UTF-16**. Данная система кодирования оказалась настолько успешной, что стала использоваться как базовое пространство для всех символов, которыми мы сейчас пользуемся. В UTF-16 используется 2 байта для кодирования одного знака, а это значит, что максимальное количество символов, которые можно закодировать в этой системе составит 2^16 =  65536. На данный момент существуют способы, позволяющие закодировать с помощью этой кодировки порядка двух миллионов символов, но консорциум принял решение ограничить расширение пространства миллионом символов.  

Несмотря на успешность UTF-16 нашлись и недовольные. В основном это были страны, где использовался английский алфавит, а так же производители софта, которые не планировали в своих программах использовать язык кроме английского. Причины недовольства были те же что и при использовании UTF-32: это увеличение интернет-трафика и объема хранимой информации, только не в 4, а 2 раза.Для таких пользователей консорциум Unicode выпустил кодировку под названием **UTF-8**. Особенностью этой системы стала возможность кодирования символов в последовательность длиной от 1 до 6 байт, т.е. кодировка стала иметь переменную длину. Таким образом, буквы латинского языка в UTF-8 кодируются в 1 байт, так же как в ASCII*, кириллические знаки в 2 байта, а, например, грузинские знаки в 3 байта и т.д. Добавлю, что на практике используется диапазон кодировки длиной от 1 до  4 байтов, этого более чем достаточно.  

Сейчас в пространстве Unicode использовано  порядка 130 000 позиций. Ради удобства это пространство поделили на 17 плоскостей, но на данный момент задействовано только 6 из них. Базовой многоязыковой плоскостью принято считать плоскость под названием Basic Multilingual Plane  (сокращенно BMP). Она находится в диапазоне юникод-символов от U+0000 до U+FFFF. 

Одним из основных различий между кодировками UTF-8 и UTF-16 является BOM (анг - Byte Order Mark) – это порядок кодирования символов, по-другому сигнатура. Другими словами, в UTF-16 есть возможность кодирования символов как в прямой, так и в обратной последовательности. Например, буква «Д» в UTF-16 может быть закодирована как U041или 041U. Проявление BOM в процессе кодировки файлов посредством UTF-16 выражается путем добавления трех байтов в начало этого фала. Кодировка UTF-8 возможности кодирования  символов в обратной последовательности лишена.  
<br />
<br />
#### 4. Заключение
В свете темы доклада хотелось бы отметить, что для успешной разработки программных продуктов производителям софта в первую очередь необходимо определится с целевой аудиторией. И уже исходя из этого использовать необходимую кодировку символов в своем программном продукте.  

К **основным преимуществам UTF-8** можно отнести:  
•	Кодировку переменной длины;  
•	Совместимость с софтом не понимающим Unicode;  
•	Меньший вес данных по отношению к UTF-16.  
К **недостаткам UTF-8** можно отнести неспособность понимать данные, закодированные при помощи UTF-16 с обратной кодировкой символов.  

К **основным преимуществам UTF-16** можно отнести:  
•	Возможность кодирования символов как в прямой, так и в обратной последовательностях;  
•	Фиксированная длина кодировки символов, что будет удобно для программистов.  
К **недостаткам UTF-16** можно отнести несколько больший вес данных по отношению к UTF-8.  

Ну и, напоследок, интересный факт: программы, не понимающие Unicode, смогут считать информацию из файла кодированного UTF-8, в котором использовалась только латиница.
</p>
<br />
<br />
<br />


<center>  **Спасибо за внимание!**</center>  

