---
title: Добавление хвостика к облаку
author: admin
type: post
date: 2012-12-26T20:10:25+00:00
url: /dobavlenie-xvostika-k-oblaku/
categories:
  - Css 3

---
Благодаря скругленным углам поля комментариев стали гораздо больше похожи на облачка, однако облако прямой речи выглядит незавершенным, если у него нет указателя или стрелки (обычно называемой «хвостиком»), связанной с автором этой прямой речи. Для добавления хвостика никакие изображения не требуются. Более того, это можно сделать, даже не прибегая к возможностям CSS3, — данный метод основывается на свойствах и селекторах из CSS2.

Создание треугольников из рамок

Для добавления хвостика нам требуется только простой треугольник, который очень легко создать из обычных рамок с помощью чистого CSS. Если внимательно посмотреть на угол поля, то вы увидите, что у отрезков, составляющих его рамку, края скошены (рис. 2.5). Уменьшите значения width и height для этого поля до нуля, выберите для всех отрезков рамки большее значение толщины и разные цвета, и у вас получится фигура из составленных вместе четырех треугольников, указывающих в разных направлениях (рис. 2.6).

<a href="http://formstyle.com.ua/?attachment_id=1191" rel="attachment wp-att-1191"><img class="aligncenter size-full wp-image-1191" alt="Создание треугольников из рамок" src="http://formstyle.com.ua/wp-content/uploads/2012/12/Создание-треугольников-из-рамок.png" width="63" height="63" /></a><a href="http://formstyle.com.ua/?attachment_id=1201" rel="attachment wp-att-1201"><img class="aligncenter size-full wp-image-1201" alt="Создание треугольников из рамок 2" src="http://formstyle.com.ua/wp-content/uploads/2012/12/Создание-треугольников-из-рамок-2.png" width="184" height="101" /></a>

Выбрав для верхнего отрезка рамки другой цвет, легко увидеть, что его концы скошены

Когда ширина и высота поля равны нулю, отрезки рамки превращаются в треугольники

Помните, что если в коде CSS одному свойству соответствуют сразу четыре значения (как свойству border-color в приведенном фрагменте кода), то первое описывает верхний элемент, второе — правый, третье — нижний, а четвертое — левый. Вы обходите фигуру по часовой стрелке, начиная сверху.

Далее представлен код HTML и CSS, определяющий фигуру на рис. 2.6:

<div class=&#187;triangle-left&#187;></div>

.triangles {

border-color: red green blue orange; border-style: solid; border-width: 20px; width: 0; height: 0;

<sup>}</sup>

Но что произойдет, если верхний, левый и нижний отрезки рамки сделать не цветными, а прозрачными? Тогда на странице мы увидим только правый отрезок, который будет выглядеть как треугольник, указывающий влево (рис. 2.7):

<div class=&#187;triangle-left&#187;></div>

<a href="http://formstyle.com.ua/?attachment_id=1211" rel="attachment wp-att-1211"><img class="aligncenter size-full wp-image-1211" alt="Тогда на странице мы увидим только правый отрезок, который будет выглядеть как треугольник, указывающий влево" src="http://formstyle.com.ua/wp-content/uploads/2012/12/Тогда-на-странице-мы-увидим-только-правый-отрезок-который-будет-выглядеть-как-треугольник-указывающий-влево.png" width="83" height="86" /></a>

&nbsp;

.triangle-left {

border-color: transparent green transparent transparent; border-style: solid; border-width: 20px; width: 0; height: 0;

<div>
  <p>
    Все отрезки рамки, за исключением правого, прозрачные; правый отрезок выглядит как треугольник
  </p>
</div>

&nbsp;

<sup>}</sup>

Таким образом, для того чтобы создать треугольник с помощью кода CSS, вам нужно уменьшить ширину и высоту элемента до нуля, добавить толстую рамку и все

отрезки рамки, за исключением одного, сделать прозрачными. Степень остроты угла можно варьировать, устанавливая разные значения толщины для разных отрезков рамки.