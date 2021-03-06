---
title: коротко об использовании нескольких Фоновых изображений
author: admin
type: post
date: 2013-01-03T17:26:32+00:00
url: /korotko-ob-ispolzovanii-neskolkix-fonovyx-izobrazhenij/
categories:
  - Css 3

---
Добавление нескольких фоновых изображений к одному элементу — это новая возможность свойств background и background-image, а не новое свойство. Указанные свойства входят в модуль Backgrounds and Borders (Фон и границы), расположенный по адресу http://www.w3.org/TR/css3-background.

Перечислите все фоновые изображения внутри свойства background-image или background, разделив их запятыми. Фоновые изображения отображаются одно поверх другого, и первое объявленное изображение выводится наверху стека.

Каждое изображение можно разместить, повторить, масштабировать и скорректировать иным образом независимо от остальных. Для этого нужно добавить информацию о настройке отображения к URL-адресу данного изображения в свойстве background или вставить список разделенных запятой значений в каждое независимое свойство описания фона, например background-repeat: no-repeat, no-repeat, repeat-x, repeat. Каждое значение в таком списке сопоставляется с соответствующим пунктом в списке фоновых изображений. Помимо заполнения бумажного фона многоуровневыми изображениями пятен, возможность добавления нескольких фоновых изображений помогает решать следующие задачи:

•    создание гибких полей с узорными или неправильными углами и краями, которые невозможно описать с помощью других свойств CSS3, таких как border-radius; например добавление на страницу декоративных кнопок (см. http://css-tricks.com/26-css3-multiple-backgrounds-obsoletes-sliding-doors);

•    изображения открывающейся и закрывающейся кавычек для блока blockquote (см. http://css.dzone.com/news/multiple-backgrounds-oh-what-beautiful-thing);

•    эффект параллакса, когда изменение размера окна или наведение указателя мыши на блок div заставляет изображения двигаться с разными скоростями по отношению друг к другу (см. http://www.paulrhayes.com/2009-04/auto-scrolling-parallax-effect-without-javascript);

•    заполнение всей ширины поля или страницы единым изображением, которое в действительности состоит из множества фрагментов. Например, вам требуется пейзаж, в котором солнце всегда отображается в правом верхнем углу, а дерево — в левом нижнем;

•    заполнение поля по всей высоте и ширине изображениями с указанием их относительного местоположения (доля от общей длины или ширины поля) — для того чтобы картинки находились на расстоянии друг от друга; например, поверх голубого фонового цвета можно вывести множество изображений облаков;

•    имитация реального трехмерного объекта путем добавления в одно поле изображений, представляющих верхний срез, нескольких промежуточных срезов и нижний срез;

•    добавление генерируемого с помощью CSS3 градиента (помните, что он определяется в свойстве background-image, а не background-color) к фоновому изображению, для того чтобы постепенно сводить на нет текстуру, размывать края изображения до сплошного цвета или показывать пользователю только нужные части изображения по мере того, как он прокручивает страницу (см. http://atomicrobotdesign.com/blog/htmlcss/make-the-thinkgeek-background-effect-using-css3).

Поддержка нескольких фоновых изображений для одного элемента в браузерах

<table border="1">
  <tr>
    <td>
      IE
    </td>
    
    <td>
      Firefox
    </td>
    
    <td>
      Opera
    </td>
    
    <td>
      Safari Chrome
    </td>
  </tr>
  
  <tr>
    <td>
      Да, начиная с версии 9
    </td>
    
    <td>
      Да, начиная с версии 3.6
    </td>
    
    <td>
      Да, начиная с версии 10.5
    </td>
    
    <td>
      Да Да
    </td>
  </tr>
</table>

Обходные пути для не поддерживающих данную возможность браузеров

Браузер IE 8 и более ранних версий, а также старые версии Firefox и Opera не поддерживают добавление к одному элементу нескольких фоновых изображений. В случаях, подобных нашему, когда дополнительные изображения — это всего лишь вариант украшения страницы, не стоит беспокоиться о реализации каких-то обходных путей. Пользователи все так же увидят линованный фон, который сам по себе представляет завершенное изображение. У них не создастся впечатления, будто на странице чего-то не хватает.

Однако возможны ситуации, когда отсутствие дополнительных изображений создает впечатление, будто бы веб-сайт недоделан или сломан. Например, вы с помощью нескольких изображений создаете сложную кнопку, которая выглядит сломанной, если отображается только один из составляющих ее графических объектов. Будьте очень внимательны и осторожны, применяя несколько фоновых изображений, поскольку обходных путей не так много:

■    использование одного альтернативного изображения. Самый простой обходной путь для не поддерживающих данную возможность браузеров — добавить одно альтернативное изображение вместо множества, составляющих многослойный фон. Для этого вставьте отдельное объявление background-image перед тем, где перечисляются несколько изображений (выше мы прибегали к этому решению), или воспользуйтесь помощью Modernizr. Удостоверьтесь, что этого изображения будет достаточно для того, чтобы страница смотрелась целостной. Данный обходной путь легко реализовать, и он не искажает страницу в устаревших браузерах, однако может оказаться недостаточно эффективным в ситуациях, когда без дополнительных изображений страница действительно выглядит неполной;

<a name="bookmark82"></a>■    использование вложенных блоков div с дополнительными изображениями.

Более надежный, но трудоемкий обходной путь подразумевает возвращение к старому испытанному методу с вложенными блоками div и добавлением разных изображений к разным полям. Если вы решите прибегнуть к нему, вам понадобится помощь сценария Modernizr или условных комментариев IE для передачи разных правил браузерам с разными уровнями поддержки. В противном случае в браузерах, поддерживающих несколько фоновых изображений, фон будет двоиться. Разумеется, если вы в любом случае собирались добавлять эти дополнительные блоки div и правила для обработки фона, можно полностью отказаться от новой возможности и применять старую технику для всех браузеров, независимо от того, понимают они элементы с несколькими фоновыми изображениями или нет. Таким образом, я не уверена, что этот обходной путь действительно имеет смысл;

<a name="bookmark83"></a>■    генерирование дополнительных элементов для добавочных изображений.

Более изящный способ реализации обходного пути с вложенными блоками div подразумевает использование псевдоэлементов :before и :after для генерации дополнительных элементов, с которыми затем можно связывать нужные фоновые изображения. О том, как это делается, рассказывает Николас Галлахер (Nicolas Gallagher) в своей статье на странице http://nicolasgallagher.com/multiple-backgrounds-and-borders-with-css2. Это прекрасный вариант, например, для IE 8 и Firefox 3.5, однако версии IE 6 и 7 не поддерживают такие псевдоэлементы, следовательно, данная техника в них не будет работать, если только не добавить еще один сценарий, заставляющий старые версии IE понимать подобные селекторы. Но тогда обходной путь излишне усложнится. И снова вы должны самостоятельно решить, стоит ли вам и вашим пользователям идти на такие жертвы ради простого украшения;

■ использование элемента canvas. Если вы знакомы с написанием сценариев, можете связать несколько изображений с одним элементом, применив элемент HTML5 canvas. IE 8 и более ранние версии не поддерживают canvas, но эту проблему можно решить с помощью сценария explorer-canvas от Google (http://code.google.com/p/explorercanvas). Подробное рассмотрение принципов использования элемента canvas лежит за пределами тематики данной книги. Кроме того, всю работу за вас уже сделал Hans Pinckaers, сценарий mb.js которого (http://github.com/HansPinckaers/mb.js) позволяет реализовать множественные фоновые изображения в IE и старых версиях других браузеров.