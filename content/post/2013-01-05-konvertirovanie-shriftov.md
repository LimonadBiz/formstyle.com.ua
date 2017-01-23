---
title: конвертирование шрифтов
author: admin
type: post
date: 2013-01-05T17:58:10+00:00
url: /konvertirovanie-shriftov/
categories:
  - Css 3

---
Некоторые поставщики шрифтов с поддержкой @font-face сразу включают в комплект файлы во всех форматах, которые могут потребоваться в разных браузерах. Например, Font Squirrel предлагает так называемые наборы @font-face kit, каждый из которых включает исходный шрифт в формате TTF или OTF, версию SVG, версию WOFF, версию EOT, пример таблицы стилей с правилами @font-face и HTML-страницу, демонстрирующую результат. Список наборов вы найдете на странице http://www.fontsquirrel.com/fontface.

Коллекция Font Squirrel не может не восхищать, но созданный ими же генератор комплектов @font-face, расположенный по адресу http://www.fontsquirrel.com/ fontface/generator, еще лучше. Вы просто загружаете свой шрифт и преобразуете его в любой подходящий формат. При этом можно настраивать синтаксис кода CSS, указывать только необходимый набор символов для уменьшения размера файла и применять множество других параметров тонкой настройки шрифтов (рис. 3.27).

<div id="attachment_2291" style="width: 498px" class="wp-caption aligncenter">
  <a href="http://formstyle.com.ua/?attachment_id=2291" rel="attachment wp-att-2291"><img class="size-full wp-image-2291" title="Утилита @font-face Kit Generator от Font Squirrel" alt="Утилита @font-face Kit Generator от Font Squirrel" src="http://formstyle.com.ua/wp-content/uploads/2012/12/Утилита-@font-face-Kit-Generator-от-Font-Squirrel.png" width="488" height="586" srcset="http://formstyle.com.ua/wp-content/uploads/2012/12/Утилита-@font-face-Kit-Generator-от-Font-Squirrel.png 488w, http://formstyle.com.ua/wp-content/uploads/2012/12/Утилита-@font-face-Kit-Generator-от-Font-Squirrel-249x300.png 249w" sizes="(max-width: 488px) 100vw, 488px" /></a>
  
  <p class="wp-caption-text">
    Утилита @font-face Kit Generator от Font Squirrel
  </p>
</div>

Чаще всего вам будет вполне достаточно файлов, предоставляемых Font Squirrel, однако я хочу рассказать о паре утилит, предназначенных для оптимизации файлов EOT и SVG. EOTFAST, — это бесплатное приложение для настольного компьютера (загрузите его со страницы <http://eotfast.com>). Оно преобразует файлы TTF в сжатые без потерь файлы EOT (Font Squirrel предлагает только не сжатые файлы EOT). Утилита командной строки ttf2svg (<http://xmlgraphics.apache.org/batik/tools/> font-converter.html) конвертирует файлы TTF в файлы SVG такого же или меньшего размера; для того чтобы использовать ее, необходима система с установленными Java и комплектом инструментов Java SVG Batik.

<a name="bookmark93"></a>Шрифт Prelude на странице Font Squirrel

Среди файлов упражнений для этой главы вы найдете папку под названием fonts, содержащую все восемь версий шрифта Prelude, которые понадобятся нам для нашей страницы: файлы EOT, SVG, TTF и WOFF как для обычного, так и для полужирного начертания. Я создала эти файлы с помощью инструмента Font Squirrel Generator, применив настройки, показанные на рис. 3.27. Затем я обработала файлы EOT в приложении EOTFAST и уменьшила их размер приблизительно вполовину.

&nbsp;

&nbsp;