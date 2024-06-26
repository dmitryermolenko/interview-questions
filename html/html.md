- **Как расшифровывается HTML?**  
  Ответ: *Язык гипертекстовой разметки.*


- **Для чего он нужен?**  
  Ответ: *Для описания структуры документа.*  


- **Что такое тег**?  
  Ответ: *Это "кирпичик", базовая единица HTML, c помощью которых описывается структура документа.*  


- **Из чего состоит тег?**  
  Ответ: *Непарный тег состоит из открывающей угловой скобки, названия тега, /, закрывающей угловой скобки (`<img />`).  
  Парный тег состоит из открывающей угловой скобки, названия тега, закрывающей угловой скобки, открывающй угловй скобки, /, названия тега, закрывающей угловой скобки (`<div></div>`).*  


- **Какие использовал теги на практике?**  
  Ответ: _Назвать все теги, что были когда-либо использованы_    

  
- **Зачем столько тегов?**  
  Ответ: _Каждый тег имеет свою зону ответственности и свою функциональную нагрузку: одни - технические, другие - семантические, третьи - просто вспомогательные._  


- **Кто занимается стандартизацией HTML?**  
  Ответ: _W3C(World Wide Web Consortium)_.  


- **Какая на сегодняшний день актульная версия стандарта HTML?**  
  Ответ: _5_     


- **Как выглядит базовая структура html-документа?**  
  Ответ: Базовая структура HTML-документа выглядит так:
 ```
  <!DOCTYPE html>
   <html>
     <head>
       <meta charset="UTF-8">
       <title>Заголовок документа</title>
     </head>
   <body>
    <!-- Содержимое страницы -->
   </body>
  </html>
 ```   

- **Для чего предназначен тег `<head>`?**  
  Ответ:   


- **Для чего предназначен  тег `<title>`?**  
  Ответ: _Определяет название документа. Отображается на вкладке пользователя, в сохраненных закладках._  


- **Почему существует 6 типов заголовков?**  
  Материалы для изучения:
   - https://web-standards.ru/articles/heading-levels/
   - https://htmlacademy.ru/blog/html/headers 
  
  Ответ: _Для лучшего структурирования текста._    
  

- **Можно ли использовать несколько тегов `<h1>`?**  
  Ответ: _Технически никаких ограничений нет, но с точки зрения SEO - нежелательно._


- **В чем отличие тега `<head>` от `<header>`?**  
  Ответ: ` <header>` _- семантический тег, предназначенный для обозначения шапки как всего сайта, так и некого раздела_  
  `<head>` _- тег для подключения стилий, скриптов, мета-тегов, тега title_  


- **Сколько раз мы можем использовать тег `<header>`?**  
  Ответ: _Сколько угодно._  

  
- **В чем смысл тегов `<section>`, `<header>`, `<article>`, `<button>`, `<a>`, `<p>` и т.д?**  
  Ответ: _Придавать семантичность документу._    


- Что такое семантическая верстка?  
  Материалы для изучения:
  - https://htmlacademy.ru/blog/html/semantics
  - https://doka.guide/html/semantics/ 
  
  Ответ: _Это подход к разметке, который опирается не на содержание сайта, а на смысловое предназначение каждого блока и логическую структуру документа._


- **Можно ли использовать вместо всех вышеперечисленных тегов тег `<div>`?**  
  Ответ: _Да, можем._


- **Влечет ли за собой какие-либо проблемы верстка, выполненная на тегах ` <div>`?**  
  Ответ: _Да, проблемы с семантикой и доступностью, скринридеры и поисковики плохо будут анализировать такие документы._  


- **Чем семантика отличается от доступности?**  
  Ответ: _Семантика является частью доступности, она ее улучшает._   


- **Какие существуют практики сделать сайт доступным?**   
  Материалы для изучения:
   - https://doka.guide/a11y/a11y-html/   
  
  Ответ: _Существуют следующие способы сделать сайт доступным:_  
  1. [x] правильное использование семантических тегов
  2. [x] использование осмысленного текстового содержимого тегов
  3. [x] использование тега `<label>` для подписей элементов форм
  4. [x] использование тега `<legend> `для подписи группы элементов форм
  5. [x] использование тега `<caption>` для подписей таблиц
  6. [x] использование тега `<figcaption>` для подписей иллюстрации
  7. [x] использование атрибута `alt` с осмысленным текстовым содержимым в теге `<img>`
  8. [x] использование доступных подписей через атрибут `aria-label` или класс `.visually-hidden `


- **Какие существуют способы скрыть содержимое?**   
  Материалы для изучения:
    - https://doka.guide/a11y/content-hidden/  
    - https://www.youtube.com/watch?v=Ns0zijQJxH4&ab_channel=HTMLAcademy  
   Ответ:
       1. [x] атрибут `aria-hidden:true` - скрывает только от скринридеров
       2. [x] специальный класс `.visually-hidden` - скрывает только визуально, вырывается из потока
         ```
           .visually-hidden {
             clip: rect(0 0 0 0);
             clip-path: inset(50%);
             height: 1px;
             overflow: hidden;
             position: absolute;
             white-space: nowrap;
             width: 1px;
           }
        ```
       3. [x] атрибут `aria-label` - скрывает только визуально, подходит для кнопок, ссылок, элементов форм, не всегда хорошо поддерживается скринридерами
       4. [x] css-свойство `visibility: hidden` - скрывает как визуально, так и от скринридеров, но не вырывается из потока
       5. [x] css-свойство `display: none` - скрывает как визуально, так и от скринридеров, в потоке не остается
       6. [x] атрибут hidden - скрывает как визуально, так и от скринридеров, но вырвается из потока  


- **Когда использовать кнопки, а когда ссылки?**  
  Ответ: _ссылки - для навигации, кнопки - для действий_  


- **Как можно сфокусироваться на неинтерактивном элементе?**  
  Ответ: _Использовать атрибут `tabindex`._
