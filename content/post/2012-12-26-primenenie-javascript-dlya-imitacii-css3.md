---
title: Применение JavaScript для имитации CSS3
author: admin
type: post
date: 2012-12-26T15:53:49+00:00
url: /primenenie-javascript-dlya-imitacii-css3/
categories:
  - Css 3

---
Пока что мы рассматривали обходные пути, предоставляющие не поддерживающим CSS3 браузерам возможность использовать альтернативный стиль, а не имитировать поведение CSS3. В большинстве случаев альтернативы вполне достаточно. Но если требуется, чтобы представление содержимого в разных браузерах выполнялось более единообразно, то выход один — эмуляция.

Зачастую с помощью JavaScript можно добиться тех же эффектов, которые в более продвинутых браузерах реализуются на базе CSS3. Например, уже много лет разработчики создают скругленные углы, применяя для этого сценарии.

В каждой главе этой книги мы будем изучать сценарии, подходящие для реализации рассматриваемой техники CSS3. Однако сейчас я хотела бы представить несколько популярных «универсальных» сценариев, которые решают сразу несколько задач эмуляции CSS3:

■    IE7 от Dean Edwards (http://code.google.com/p/ie7-js/). Заставляет псевдоклассы и селекторы атрибутов CSS3 работать в версиях IE с 6 по 8. Кроме того, обеспечивает функционирование свойств CSS3 box-sizing и opacity, а также некоторых свойств и селекторов CSS 2.1, которые не поддерживаются в старых версиях IE;

■    Selectivizr от Keith Clark (http://selectivizr.com/). Заставляет псевдоклассы и селекторы атрибутов CSS3 работать в версиях IE с 6 по 8. Необходимо использовать в сочетании с другой библиотекой JavaScript;

■    cssSandpaper от Zoltan Hawryluk (http://www.useragentman.com/blog/csssandpaper-a-css3-javascript-library). Заставляет 2D-трансформации, свойство box-shadow, градиенты, свойство opacity, синтаксисы RGBA и HSLA работать в IE и других не поддерживающих CSS3 браузерах;

■    PIE от Jason Johnston (http://css3pie.com/). Заставляет свойства border-radius, box-shadow, множественные фоны, свойства background-origin, background-clip и линейные градиенты работать в версиях IE с 6 по 8. Также включает ограниченную поддержку свойства border-image и синтаксиса RGBA.