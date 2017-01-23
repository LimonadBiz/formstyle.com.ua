---
title: преобразование ЗНАЧЕНИЙ HSLA И RGBA ДЛЯ ФИЛЬТРА GRADIENT
author: admin
type: post
date: 2012-12-30T16:22:22+00:00
url: /preobrazovanie-znachenij-hsla-i-rgba-dlya-filtra-gradient/
categories:
  - Css 3

---
<div>
  <p>
    Для успешной работы с браузерами IE крайне важно понимать концепцию hasLayout. Если вы чувствуете, что вам не мешает обновить знания об этом странном «свойстве», рекомендую прочитать статью автора Ingo Chao «On having layout» по адресу http://www.satzansatz.de/cssd/onhavinglayout.html.
  </p>
</div>

&nbsp;

Для того чтобы в градиенте IE получить такую же степень прозрачности цвета, которая была задана в нотации HSLA, нужно попросту умножить значение прозрачности HSLA (в нашем случае .6) на 255 и перевести результат в шестнадцатеричную систему. Роберт Найман (Robert Nyman) объясняет, как это делается, в своей статье по адресу http://robertnyman.com/2010/01/11/css-background-transparency-without-affecting-child-elements-through-rgba-and-filters.

Проще всего, однако, использовать утилиту Майкла Бестера (Michael Bester) TGBa & HSLa CSS Generator for Internet Explorer, расположенную по адресу http://kimili.com/journal/rgba-hsla-css-generator-for-internet-explorer. Вставьте значение RGBA или HSLA, и она автоматически преобразует его в эквивалентное значение для фильтра Gradient.

В IE 8 фоновый цвет удалять не требуется, так как этот браузер умеет правильно игнорировать фоновый цвет HSLA в главном правиле blockquote. Также не нужно включать hasLayout. Однако синтаксис записи свойств фильтра немного отличается. Добавьте для IE 8 следующее правило:

.ie8 blockquote {

-ms-filter: &#171;progid:DXImageTransform.Microsoft.gradient (startColorstr=#99A6DADC, endColorstr=#99A6DADC)&#187;;

}

Этот синтаксис отличается тем, что фильтр носит название -ms-filter, а не просто filter, а значение свойства -ms-filter заключается в кавычки. Такой вариант лучше соответствует спецификациям CSS и больше похож на то, как фирменные свойства описываются в других браузерах.