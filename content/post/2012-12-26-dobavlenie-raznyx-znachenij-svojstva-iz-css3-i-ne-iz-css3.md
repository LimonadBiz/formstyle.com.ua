---
title: 'Добавление разных значений свойства: из CSS3 и не из CSS3'
author: admin
type: post
date: 2012-12-26T15:51:06+00:00
url: /dobavlenie-raznyx-znachenij-svojstva-iz-css3-i-ne-iz-css3/
categories:
  - Css 3

---
Иногда в ситуациях, когда обеспечить обходной путь необходимо или желательно, это делается очень просто: вы всего лишь указываете несколько значений для свойства в одном и том же правиле. Первое значение будет использоваться в браузерах, не поддерживающих CSS3, а второе — в браузерах, где с поддержкой CSS3 все в порядке. Первая категория браузеров будет игнорировать правила, которые они понять не в силах, а браузеры с поддержкой CSS3 станут переопределять старые значения новыми.

Например, для случая с пропадающим цветом фона, упомянутого выше, можно сначала указать сплошной цвет заливки фона в шестнадцатеричном представлении, а затем версию HSLA или RGBA для новых браузеров:

div {

background: #CC0000;

background: hsla(0, 100%, 40%, .5);

}

Обратите внимание, что подобное решение очень редко позволяет имитировать истинное представление или поведение свойства CSS3 — скажем, здесь в браузерах, не поддерживающих CSS3, фон заливается сплошным непрозрачным цветом, а не полупрозрачным, как в версии CSS3. Однако это приемлемый вариант для ситуации, когда отсутствие какого-либо обходного пути полностью искажает страницу, делая невозможным использование ее в устаревших браузерах.