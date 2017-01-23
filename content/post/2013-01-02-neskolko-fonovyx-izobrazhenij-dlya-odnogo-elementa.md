---
title: Несколько Фоновых изображений для одного элемента
author: admin
type: post
date: 2013-01-02T17:22:16+00:00
url: /neskolko-fonovyx-izobrazhenij-dlya-odnogo-elementa/
categories:
  - Css 3

---
Одним из самых долгожданных и приятных для веб-дизайнеров изменений в CSS стала возможность добавлять к одному элементу несколько фоновых изображений. В нашем примере мы воспользуемся ею для того, чтобы придать бумаге более реалистичный вид, — мы добавим на нее следы времени, наложив изображения пятен, а сверху воткнем в нее канцелярскую кнопку.

Во времена, предшествующие появлению CSS3, у поля могло быть только одно фоновое изображение, поэтому вам приходилось добавлять новый блок div для каждого изображения и в каждом из div использовать только одно изображение. Если внутри блоков div использовались другие блоки — например, элемент h3 всегда был первым вложенным элементом, — в качестве альтернативы фоновые изображения можно было связывать с этими дополнительными блоками, что избавляло от необходимости добавлять излишние блоки div. Однако такой подход нес определенный риск, ведь вам приходилось полагаться на то, что определенный тип содержимого всегда будет выводиться на странице — и всегда в определенных местах. Если содержимое по каким-то причинам не отображалось, разумеется, со страницы исчезали и соответствующие фоновые изображения.

Метод с вложенными блоками div не представлял сложности, однако делал код довольно неопрятным. Разметка становилась плохо читаемой, а размер файла значительно увеличивался. Если позднее возникала необходимость добавить новые изображения, приходилось редактировать не только CSS, но и код HTML.

Теперь благодаря CSS3 можно избавить HTML от чрезмерной опеки и просто перечислить все фоновые изображения в свойстве background-image или background, разделив их запятыми. Местоположение, количество повторений, размер и другие показатели для каждого из них настраиваются индивидуально и независимо от остальных.

<div>
  <p>
    Переносы строк и отступы внутри свойства background добавлены исключительно для упрощения восприятия кода CSS. Вы можете записать содержимое свойства на одной строке или на нескольких — работать оба варианта будут одинаково.
  </p>
</div>

&nbsp;

На рис. 3.9 показаны дополнительные изображения, которые мы добавим в блок div в коде нашей статьи. Добавьте в правило #paper новое объявление background, поместив его под существующим:

#paper {

float: left; margin: 40px;

padding: 3.2em 1.6em 1.6em 1.6em; background: url(images/paperlines.gif) #FBFBF9;

background: url(images/thumbtack.png), url(images/stains1.png), url(images/stains2.png), url(images/stains3.png), url(images/stains4.png), url(images/paperlines.gif) #FBFBF9; -moz-background-size: auto 1.6em; -webkit-background-size: auto 1.6em; background-size: auto 1.6em;

}

<div id="attachment_1961" style="width: 745px" class="wp-caption aligncenter">
  <a href="http://formstyle.com.ua/?attachment_id=1961" rel="attachment wp-att-1961"><img class="size-full wp-image-1961" title="Пять фоновых изображений, которые добавят графические детали на наш лист линованной бумаги" alt="Пять фоновых изображений, которые добавят графические детали на наш лист линованной бумаги" src="http://formstyle.com.ua/wp-content/uploads/2012/12/Пять-фоновых-изображений-которые-добавят-графические-детали-на-наш-лист-линованной-бумаги.png" width="735" height="225" srcset="http://formstyle.com.ua/wp-content/uploads/2012/12/Пять-фоновых-изображений-которые-добавят-графические-детали-на-наш-лист-линованной-бумаги.png 735w, http://formstyle.com.ua/wp-content/uploads/2012/12/Пять-фоновых-изображений-которые-добавят-графические-детали-на-наш-лист-линованной-бумаги-300x91.png 300w" sizes="(max-width: 735px) 100vw, 735px" /></a>
  
  <p class="wp-caption-text">
    Пять фоновых изображений, которые добавят графические детали на наш лист линованной бумаги
  </p>
</div>

Первое объявление background будет использоваться браузером IE и другими браузерами, не поддерживающими наличие у элемента несколько фоновых изображений. Так как они не понимают синтаксис второго объявления background, они попросту игнорируют его. Браузеры, поддерживающие добавление нескольких фоновых изображений, переопределяют первое объявление, как только считывают второе.

<div>
  <p>
    Водянистые пятна, показанные на рис. 3.9, созданы в приложении Photoshop с использованием кистей от Obsidian Dawn (см. http://www.obsidiandawn.com/water-stains-photoshop-gimp-brushes).
  </p>
</div>

Фоновые изображения выводятся одно поверх другого, причем первое из объявленных оказывается наверху стека. Вот почему изображение кнопки находится на самом верху списка, а изображение линии — внизу.

Но это еще не все. Мы пока что не сообщили браузеру, каким образом следует повторять, размещать и масштабировать каждое из изображений. Каждый фрагмент кода между запятыми следует рассматривать как отдельное собирательное свойство background и соответствующим образом записывать свойства, относящиеся

к фоновому изображению. На рис. 3.10 перечислены все составляющие, которые можно добавить к собирательному свойству background. Для некоторых из них порядок следования важен, для других нет. Чтобы не запутаться и случайно не сделать ошибку, я рекомендую придерживаться порядка, показанного на рис. 3.10 (лично я в противном случае обязательно сразу же запуталась бы!).

Прикрепление

Изображение Позиция Размер Повторение    Источник    Обрезка

\_I\\_\_I_ \_I\\_\_I\_\_I\_\_I_\_I\_

background: url(top.gif} 50% О /    к    по-repeat fixed padding-box padding-box, Верхний слой

url(middle.gif) 50% 0 no-repeat content-box, Второй слой url(bottom.gif)0 0/ auto 20px repea #FFF; Последний слой

Цвет

Собирательное свойство background может состоять из нескольких слоев; на этом рисунке верхний слой включает все возможные составляющие свойства (за исключением цвета, который всегда добавляется в последний слой)

С учетом порядка следования составляющих, показанного на рис. 3.10, добавьте значения позиции и повторения для каждого из изображений в свойстве background:

background: url(images/thumbtack.png) 50% 5px no-repeat, url(images/stains1.png) 90% -20px no-repeat, url(images/stains2.png) 30% 8% no-repeat, url(images/stains3.png) 20% 50% no-repeat, url(images/stains4.png) 40% 60% no-repeat, url(images/paperlines.gif) #FBFBF9;

Затем отредактируйте свойства background-size таким образом, чтобы браузер выводил изображения с исходными размерами; исключение необходимо сделать только для последнего изображения, представляющего линии на странице:

-moz-background-size: auto, auto, auto, auto, auto,

auto 1.6em;

-webkit-background-size: auto, auto, auto, auto, auto,

auto 1.6em;

background-size: auto, auto, auto, auto, auto, auto 1.6em;

Каждое из перечисленных через запятую значений соответствует находящемуся на аналогичном месте значению свойства background.

<div>
  <p>
    Страница со всеми внесенными до настоящего момента изменениями называется paper_1.html. Она находится в папке с файлами упражнений, которую вы загрузили для этой главы.
  </p>
</div>

С технической точки зрения информацию background-size можно добавить в составное свойство background, однако пока что такой вариант работать не будет. В старых версиях Firefox и Safari объявлять background-size необходимо с указанием браузерных префиксов. Несмотря на то что Opera, Chrome, Safari 5, Firefox 4 и IE 9 распознают наличие background-size внутри свойства background, указанные старые версии Firefox и Safari не понимают подобную запись и не способны отобразить нужные фоновые изображения. Таким образом, для того чтобы эти свойства работали в любых браузерах, а также для того чтобы вы не путались в значениях background-posit ion и background-size (а их спутать очень просто!), всегда записывайте background-size отдельно от background.

Сохраните страницу и откройте ее в современном браузере. Вы увидите, что текст выровнен по линеечкам на странице, которая наверху «прикреплена» к экрану канцелярской кнопкой. Кроме того, на странице теперь есть четыре мокрых пятна (рис. 3.11).

<div id="attachment_1981" style="width: 778px" class="wp-caption aligncenter">
  <a href="http://formstyle.com.ua/neskolko-fonovyx-izobrazhenij-dlya-odnogo-elementa/vse-shest-fonovyx-izobrazhenij-iz-bloka-div-otobrazhayutsya-v-raznyx-mestax-stranicy/" rel="attachment wp-att-1981"><img class="size-full wp-image-1981" title="Все шесть фоновых изображений из блока div отображаются в разных местах страницы" alt="Все шесть фоновых изображений из блока div отображаются в разных местах страницы" src="http://formstyle.com.ua/wp-content/uploads/2013/01/Все-шесть-фоновых-изображений-из-блока-div-отображаются-в-разных-местах-страницы.png" width="768" height="358" srcset="http://formstyle.com.ua/wp-content/uploads/2013/01/Все-шесть-фоновых-изображений-из-блока-div-отображаются-в-разных-местах-страницы.png 768w, http://formstyle.com.ua/wp-content/uploads/2013/01/Все-шесть-фоновых-изображений-из-блока-div-отображаются-в-разных-местах-страницы-300x139.png 300w" sizes="(max-width: 768px) 100vw, 768px" /></a>
  
  <p class="wp-caption-text">
    Все шесть фоновых изображений из блока div отображаются в разных местах страницы
  </p>
</div>

В настройке изображений по отдельности, в противоположность объединению их в одно большое изображение, определяемое внутри общего вложенного div, самое приятное — то, что в зависимости от размера блока div изображения могут занимать разные позиции на экране. Вне зависимости от размера и габаритов блока div изображения пятен всегда будут аккуратно распределяться по странице, а не скапливаться в одном месте.