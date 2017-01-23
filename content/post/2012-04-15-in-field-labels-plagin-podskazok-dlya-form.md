---
title: 'In-Field Labels &#8212; плагин подсказок для форм'
author: admin
type: post
date: 2012-04-15T16:12:51+00:00
url: /in-field-labels-plagin-podskazok-dlya-form/
dsq_thread_id:
  - 650413322
categories:
  - Склад скриптов
tags:
  - JavaScript
  - jQuery
  - веб-формы
  - плагины
  - скрипты

---
<a href="http://formstyle.com.ua/wp-content/uploads/2012/04/in-field.label_.jpg" rel="lightbox[202]" title="in-field.label"><img src="http://formstyle.com.ua/wp-content/uploads/2012/04/in-field.label_-300x251.jpg" alt="" title="in-field.label" width="300" height="251" class="aligncenter size-medium wp-image-612" srcset="http://formstyle.com.ua/wp-content/uploads/2012/04/in-field.label_-300x251.jpg 300w, http://formstyle.com.ua/wp-content/uploads/2012/04/in-field.label_.jpg 421w" sizes="(max-width: 300px) 100vw, 300px" /></a>

<span style="color: #000000;"><strong>Требования:</strong> jQuery</span>

<span style="color: #000000;"><strong>Совместимость:</strong> IE6+, WebKit Browsers (Safari, Chrome), Firefox 2+</span>

<span style="color: #000000;"><strong>Официальная страница:</strong></span> <a title="Плагин, делающий ваши формы формами Apple" href="https://github.com/dcneiner/In-Field-Labels-jQuery-Plugin/" rel="noindex">https://github.com/dcneiner/In-Field-Labels-jQuery-Plugin/</a>

<span style="color: #000000;">Как утверждает автор данного плагина &#8212; он целую неделю бился над интересной проблемой. Автору нужно было выводить подсказки (лейблы) в полях формы, и чтобы они исчезали только в тот момент, когда пользователь начинает печатать информацию. А так, они должны держаться в полях формы, как приклееные. Даже если на поле тыкнуть мышкой. У автора имелся скрипт. К великому несчастью, этот скрипт очищал форму от подсказки, как только на ней тыкнуть мышью. </span>

<span style="color: #000000;">И тут автор вспомнил реализацию подобной идеи в веб-приложении Mobile Me компании Apple. Воодушевился и сварганил jQuery плагин, который направлен решить поставленную задачу. Плагин с открытым исходным кодом и расположен на сервисе GitHub. Автор призывает всех кодеров совершенствовать его творение. И совместными усилиями должна получиться стоящая вещь. Итак, плюшки плагина.</span><!--more-->

**<span style="color: #000000;">Плюшки:</span>**

<span style="color: #000000;">&#8212; плагин использует стандартную разметку для элементов формы;</span>

<span style="color: #000000;">&#8212; весит всего 1 килобайт, в сжатом состоянии;</span>

<span style="color: #000000;">&#8212; дабы  заставить плагин работать, нужно прописать всего-навсего одну строчку jQuery;</span>

<span style="color: #000000;">&#8212; подсказки могут быть изображениями, а также другими элементами html;</span>

<span style="color: #000000;">&#8212; плагин весьма кроссбраузерный, дружит со всеми современными браузерами (даже IE 6).</span>

**<span style="color: #000000;">Краткий обзорчик.</span>**

<span style="color: #000000;">Плагин весьма симпатичен. Вот что он умеет: накладывает подсказку на элементы инпута, поля пароля и текстового поля, а также делает эту подсказку полупрозрачной, когда на поле жамкнет мышкой пользователь; как только пользователь начинает что-то печатать в поле, подсказка исчезает полностью. Красота. Прямо как в эпловском Mobile Me.</span>

<span style="color: #000000;">Пример работы плагина смотрите в веб-приложении Mobile Me. Либо здесь</span> &#8212; <a href="http://fuelyourcoding.com/scripts/infield/" rel="noindex">http://fuelyourcoding.com/scripts/infield/</a>. <span style="color: #000000;">Исходники качаем на странице плагина (ссылка дана в начале поста).</span>