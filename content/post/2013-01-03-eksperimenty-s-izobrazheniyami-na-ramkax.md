---
title: Эксперименты с изображениями на рамках
author: admin
type: post
date: 2013-01-03T17:40:14+00:00
url: /eksperimenty-s-izobrazheniyami-na-ramkax/
categories:
  - Css 3

---
В особенностях свойства border-image не так легко разобраться, и я не собираюсь это отрицать. Если даже после выполнения предыдущих упражнений вы все еще чувствуете себя неуверенно, я настоятельно рекомендую вам ознакомиться со следующими сетевыми инструментами, предназначенными специально для оформления рамок:

•    border-image-generator автора Kevin Decker (http://border-image.com) позволяет загружать любые изображения, для того чтобы посмотреть, как они будут выглядеть в качестве рамки элемента. Вы можете настроить по своему вкусу нарезку изображения, ширину всех отрезков рамки и способ повторения рисунка, одновременно отслеживая все изменения на экране;

•    Grokking CSS3 border-image автора Nora Brown (http://www.norabrowndesign.com/ css-experiments/border-image-anim.html) предлагает пять стандартных изображений и несколько значений border-image — вы просто выбираете любое сочетание и смотрите, как такой вариант выглядит на экране.

Возможность на лету поменять значения и проверить, как это отразится на визуальном представлении, — один из лучших способов разобраться в хитростях той или иной функции CSS.

Теперь можно встроить само изображение рамки: стандартное свойство border-image предназначено для Chrome и Opera, а варианты с префиксами — для Firefox и Safari:

#paper {

float: left; margin: 40px;

padding: 3.2em 1.6em 1.6em 1.6em; border-width: 0 0 0 50px;

-moz-border-image: url(images/edge.png) 0 0 0 50 round; -webkit-border-image: url(images/edge.png) 0 0 0 50  round;

border-image: url(images/edge.png) 0 0 0 50 round;

background: url(images/paperlines.gif) #FBFBF9; background: url(images/thumbtack.png) 50% 5px no-repeat, url(images/stains1.png) 90% -20px no-repeat, url(images/stains2.png) 30% 8% no-repeat, url(images/stains3.png) 20% 50% no-repeat, url(images/stains4.png) 40% 60% no-repeat, url(images/paperlines.gif) #FBFBF9;

-moz-background-size: auto, auto, auto, auto, auto,

auto 1.6em;

-webkit-background-size: auto, auto, auto, auto, auto,

auto 1.6em;

background-size: auto, auto, auto, auto, auto,

auto 1.6em;

<sup>}</sup>

Мы передали ненулевую координату разреза только для левого фрагмента изображения; сверху, справа и снизу оно обрезаться не будет. Однако слева отрезается полоса шириной 50 пикселов, что равно ширине самого изображения — именно это нам и требуется, так как все изображение целиком должно закрывать собой левый отрезок рамки.

<a href="http://formstyle.com.ua/?attachment_id=2111" rel="attachment wp-att-2111"><img class="aligncenter size-full wp-image-2111" alt="Копии изображения кромки листа, вырванного из блокнота" src="http://formstyle.com.ua/wp-content/uploads/2012/12/Копии-изображения-кромки-листа-вырванного-из-блокнота.png" width="346" height="469" srcset="http://formstyle.com.ua/wp-content/uploads/2012/12/Копии-изображения-кромки-листа-вырванного-из-блокнота.png 346w, http://formstyle.com.ua/wp-content/uploads/2012/12/Копии-изображения-кромки-листа-вырванного-из-блокнота-221x300.png 221w" sizes="(max-width: 346px) 100vw, 346px" /></a>

<a name="bookmark85"></a>Копии изображения кромки листа, вырванного из блокнота, последовательно выводятся вдоль левого края страницы поверх фонового изображения

Кроме того, мы добавили ключевое слово round для того, чтобы изображение повторялось несколько раз вдоль левого края страницы, но не обрезалось где-нибудь посередине отверстия. Поскольку Safari и Chrome не поддерживают это значение,

они обрабатывают изображение так, как диктует значение по умолчанию (repeat), — это допустимый компромисс.

&nbsp;