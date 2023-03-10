# Сквозная задача

Создано приложение, с графическим интерфейсом для разархивации, декодирования входного файла, обработки математических выражений из этого файла с последующими архивацией и кодированием полученных данных по желанию пользователя.

![Alt-текст](https://github.com/DianaBarinova/Skvoznay_zadacha_/blob/master/gif/gggif.gif "gif")

### Описание:
 1. В качестве входных данных используется файл(по выбору пользователя), который может быть зашифрован и заархивирован. После получения входного файла начинается процесс расшифровки и распаковки до получения исходного файла с расширениями `“.txt”`, `“.json”`, `“.xml”`.  
В приложении реализована поддержка обработки многоуровневой вложенности шифрования и архивирования(файл может быть несколько раз в любой последовательности заархивирован и зашифровон). Например: `"input.xml.encrypted.zip.rar.jar.zip.zip"`.    
  
  
 2. Обработка данных может осуществляться одним из двух способов:  
-	С помощью регулярных выражений   
-	С помощью библиотеки `Javaluator`.     
Данная библиотека имеет преимущества над регулярными выражениями, так как имеет следующий функционал:    
 -	Поддержка констант.    
 -	Поддержка переменных (пример "sin(x)").    
 -	Также легко определить свои собственные пары скобок ({}, [] и т.д.) или добавить свои собственные операторы, функции или константы.  
 -	Расширяемость: Эта библиотека снабжена вычислителем, который имеет дело с выражением для действительных чисел, если вам нужен такой для комплексных чисел или для       чего-либо еще, вы можете реализовать свой собственный.    
 -	Локализация: имена функций и констант могут быть легко изменены    
 -	Проверка синтаксиса выражения: Базовые средства оценки инфиксов рассматривают такие выражения, как "4 3 +", как допустимые выражения. Javaluator выполняет полную       проверку синтаксиса при вычислении выражения.   
  
    
 3. После обработки, данные записываются в файл с расширением по желанию пользователя, независимо от расширения исходного файла, то есть пользователь может выбрать любое расширение для файла, например: `“xml”`, `“json”`, `“txt”`.  
   
 4. После записи данных в файл, пользователь может зашифровать и архивировать свой файл.  
Поддерживаются следующие типы архивации:  
-	Jar  
-	Rar  
-	Zip  
    
Для архивации используется  `ZipArchive` - класс для архивирования и распаковки файлов в Windows, Linux.  

Для реализованных функций были написаны `Unit-тесты` с помощью библиотеки `Junit`.  

Графический интерфейс реализован на основе библиотеки `JavaFX`. JavaFX предназначен для создания приложений с поддержкой каскадных таблиц стилей (CSS).  

### Демонстрация приложения:
Интерфейс приложения состоит из основного окна, на котором можно выбрать исходный файл, обработать данные из файла, сохранить результат, и вторичного окна на котором можно выбрать по желанию архивацию файла и кодировку. Так же на основном окне отображаются данные исходного файла и результаты вычисления, таким образом пользователь может просмотреть решения примеров без сохранения файла, что позволяет сэкономить время и память, если пользователь не нуждается в файле с результатами.  
При нажатий на кнопку `"Select a file"` открывается проводник для выбора файла пользователем, что является более удобным, чем прописывать путь к исходному файлу.      
Кнопки меняют свой цвет при наведении на них курсора, а текст, на кнопках, меняет цвет при нажатии на них, что делает интерфейс интереснее и красочнее.   

![image](https://github.com/DianaBarinova/Skvoznay_zadacha_/blob/master/gif/3buttons.jpg)  


Для реализации приятного и удобного дизайна был использован CSS.  


  




