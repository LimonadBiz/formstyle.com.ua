---
title: Повышение производительности
author: admin
type: post
date: 2013-01-07T18:03:34+00:00
url: /povyshenie-proizvoditelnosti/
categories:
  - Css 3

---
Если вы сейчас просматриваете страницу в браузере, вы могли обратить внимание на задержку между загрузкой основного содержимого и написанных от руки заголовков. Браузеры на базе Webkit отображают текст, стилизованный с помощью @font-face, только после того как полностью загружают файл шрифта (рис. 3.31).

<a href="http://formstyle.com.ua/?attachment_id=2401" rel="attachment wp-att-2401"><img class="aligncenter size-full wp-image-2401" alt="Повышение производительности" src="http://formstyle.com.ua/wp-content/uploads/2012/12/Повышение-производительности.png" width="725" height="363" srcset="http://formstyle.com.ua/wp-content/uploads/2012/12/Повышение-производительности.png 725w, http://formstyle.com.ua/wp-content/uploads/2012/12/Повышение-производительности-300x150.png 300w" sizes="(max-width: 725px) 100vw, 725px" /></a>

В Firefox и Opera такой текст на мгновение отображается с использованием альтернативных шрифтов, но, как только файл нужного шрифта загружается, браузер обновляет текст и выводит его уже с новым шрифтом. Уже знакомый вам Пол Айриш придумал для этого явления остроумный термин «проблеск нестилизованного текста» (Flash of Unstyled Text или FOUT).

Задержка загрузки шрифта обычно бывает очень небольшой, и пользователи ее почти не замечают, однако вполне возможны ситуации, когда она может превратиться в большую проблему.

<div>
  <p>
    Свойство font-size-adjust, которое упоминалось выше, не уменьшает длительность проблеска нестилизованного текста, однако оно может сделать процесс загрузки шрифта менее очевидным для пользователя за счет того, что высота символов альтернативного шрифта подгоняется под размеры основного веб-шрифта и страница выглядит более аккуратной. Еще раз добавлю, однако, что это работает только в Firefox.
  </p>
</div>

&nbsp;

Шрифты восточных языков, таких как китайский или японский, содержат тысячи символов, а размер файла может достигать нескольких мегабайт.

Разумеется, загрузка такого большого файла потребует довольно много времени. Помимо этого, пользователям мобильных устройств в зонах с плохим покрытием сети, а также гостям отелей, в которых, как известно, редко можно встретить скоростное подключение, приходится подолгу дожидаться завершения загрузки веб-шрифтов.

Есть несколько решений, помогающих минимизировать или даже избавиться от проблеска нестилизованного текста в браузерах на базе Webkit:

■    прежде всего, как можно сильнее уменьшайте файлы шрифтов. В этом смысле очень хорошо помогает создание выборок символов из каждого шрифта и отбрасывание ненужных букв и знаков; кстати, это можно сделать прямо на странице Font Squirrel Generator;

■    помещайте правила @font-face в начало таблиц стилей. Это увеличивает вероятность того, что браузер загрузит шрифты до загрузки остальных файлов, на которые ссылается ваш код CSS, таких как фоновые изображения;

■    можно заставить браузер заранее загрузить файл шрифта, например, обратившись к нему в скрытом элементе в самом начале страницы. Многие техники предварительной загрузки изображений можно адаптировать к файлам шрифтов; обширный список таких решений вы найдете на странице http://perishablepress.com/press/tag/preload-images;

■    храните файлы шрифтов в другом месте. Хранение шрифтов на популярном сервере повышает вероятность того, что у посетителя вашего сайта нужный файл шрифта найдется в кэше, и тогда ему не придется загружать в точности такой же файл из другого местоположения. Такую возможность предлагают службы встраивания шрифтов, перечисленные выше, а также Google Font Directory. Шрифты собственной разработки можно также загружать на сервер службы

TypeFront (http://typefront.com). TypeFront хранит загруженные шрифты, преобразует их во все необходимые формы и загружает только на указанные вами сайты;

■    в файле .htaccess в заголовке Expires установите дату из далекого будущего. Тогда единожды загруженный файл шрифта сохранится в кэше браузера, и еще очень долго браузер не будет пытаться заново загружать его и обновлять существующую версию. Этот решение никак не влияет на первоначальную загрузку страницы, когда браузеру в любом случае необходимо загрузить все ресурсы, но может помочь при повторных посещениях (подробнее об этом рассказывается в статье автора Steve Lamm на странице http://code.google.com/speed/articles/caching.html);

■    сжимайте файлы шрифтов в архивы gzip. Стоян Стефанов выяснил, что в среднем файлы уменьшаются при этом на 40-45% (см. http://www.phpied.com/gzip-your-fontface-files). Однако он также выяснил, что такой подход не помогает решать вопрос с проблеском нестилизованных шрифтов в Firefox, так как для файлов WOFF и так используется формат с сильным сжатием, и дополнительно уменьшить их не удастся (см. http://www.phpied.com/font-facegzipping-take-ii). Однако сжатие в архив gzip помогает избежать или минимизировать проблеск нестилизованных шрифтов в Opera, а в Safari и Chrome — быстрее отобразить текст;

■    с помощью сценария скрывайте все содержимое на пару секунд, пока браузер загружает шрифты. Разумеется, это решение не ускоряет загрузку файлов шрифтов, но зато пользователя не сбивает с толку замена шрифтов на странице. Пол Айриш предлагает два таких сценария JavaScript; один — на базе Google WebFont Loader JavaScript (http://paulirish.com/2009/fighting-the-font-face-fout).

В наших файлах шрифтов используются поднаборы символов, и эти файлы вызываются в самом начале кода CSS. Таким образом, мы воплотили большинство простейших рекомендаций по повышению производительности @font-face. Добавление сценариев и реализация различных техник на серверной стороне лежат за пределами тематики данной книги, однако вы можете поэкспериментировать с ними, если столкнетесь с серьезными проблемами при загрузке веб-шрифтов.

<a name="bookmark21"></a>Готовая страница

Мы закончили стилизацию страницы, и теперь она выглядит в точности как вырванный из блокнота бумажный лист. В любом современном браузере, кроме IE.