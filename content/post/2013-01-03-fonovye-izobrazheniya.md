---
title: Фоновые изображения
author: admin
type: post
date: 2013-01-03T17:27:36+00:00
url: /fonovye-izobrazheniya/
categories:
  - Css 3

---
<div>
  <p>
    Кромка листа бумаги, вырванного из блокнота со спиральным креплением
  </p>
</div>

&nbsp;

Первый способ добавления рваной кромки — встроить в страницу еще одно фоновое изображение с повторением только по вертикали. Однако вдоль левого края изображения следуют одинаковые прозрачные области (дыры в бумаге), сквозь которые будут видны линии фонового изображения. Если бы фон нашей страницы был сплошным, а не узорным, мы могли бы залить сплошным цветом эти прозрачные области, аккуратно вписав «рваный край» в общую концепцию страницы. Однако в нашем случае такой вариант не сработает.

С учетом отсутствия сплошного фонового цвета на странице единственный доступный нам вариант — обернуть блок div, представляющий бумагу, еще одним блоком div и установить изображение с рваным краем в качестве фона этого обрамляющего блока. Обрамляющему блоку можно выделить достаточно большое поле слева страницы, для того чтобы внутренний div не накладывался на боковое изображение и не заслонял его. Нельзя сказать, что это идеальное решение — оно требует дополнительного кодирования, однако оно работает во всех браузерах и с любыми фонами.

Один небольшой недостаток установки «рваного края» в качестве фонового изображения заключается в том, что мы не можем управлять его обрезкой внизу блока div. Возможно, блок оборвется прямо посередине очередного отверстия в бумаге, а край настоящего листа из блокнота со спиральным креплением так выглядеть не может (рис. 3.13). Соглашусь, это не трагедия — всего лишь небольшая, пустячная проблема. Но если ее можно с легкостью решить, применив возможности CSS, почему бы не сделать это?

Чтобы исправить ситуацию с помощью CSS3, нужно выбрать для свойства background-repeat, представляющего изображение рваного края, значение round — новое значение, впервые появившееся в CSS3. Оно заставляет браузер повторять изображение максимальное число раз и, в случае необходимости, масштабировать его, чтобы избежать обрезки.

<a href="http://formstyle.com.ua/?attachment_id=2031" rel="attachment wp-att-2031"><img class="aligncenter size-full wp-image-2031" alt="картинка с рваным бумажным краем" src="http://formstyle.com.ua/wp-content/uploads/2012/12/картинка-с-рваным-бумажным-краем.png" width="138" height="144" /></a>

<div>
  <p>
    Когда картинка с рваным бумажным краем выбирается в качестве повторяющегося фонового изображения, вполне вероятно, что браузер обрежет ее прямо поперек отверстия
  </p>
</div>

&nbsp;

К сожалению, на момент написания этой главы значение round поддерживается только в IE 9 и Opera, причем в Opera его реализация далека от совершенства. Поэтому запись background-repeat: round в настоящее время использовать не рекомендуется. К счастью, мы можем полностью отказаться от идеи с фоновым изображением и вместо этого прибегнуть к помощи нового свойства border-image.

Использование свойства border-image

Помимо (или вместо) цвета и стиля линии CSS3 позволяет связать с рамкой элемента любое изображение. Браузер принимает одно изображение, нарезает его на кусочки и растягивает или выкладывает эти кусочки мозаикой вдоль всех отрезков рамки.

Предположим, например, что на рис. 3.14 показано изображение, с помощью которого мы хотим украсить рамку блока div. Верхние 30 пикселов изображения должны выводиться вдоль верхнего отрезка рамки, правые 25 пикселов — вдоль правого отрезка, нижние 27 — вдоль нижнего и левые 34 — вдоль левого отрезка рамки (рис. 3.15). Эти значения мы укажем и в качестве ширины рамки, и в качестве параметров нарезки изображения.

<div>
  <p>
    Допускается использование разных значений ширины рамки и ширины соответствующих фрагментов изображения. Браузер масштабирует каждое изображение, подгоняя его под ширину соответствующего отрезка рамки.
  </p>
</div>

&nbsp;

.clouds {

width: 400px; height: 150px;

border-width: 30px 25px 27px 34px; border-image: url(clouds.png) 30 25 27 34 stretch;

<a href="http://formstyle.com.ua/fonovye-izobrazheniya/ispolzovanie-raznyx-znachenij-shiriny-ramki-i-shiriny-sootvetstvuyushhix-fragmentov-izobrazheniya/" rel="attachment wp-att-2051"><img class="aligncenter size-full wp-image-2051" alt="использование разных значений ширины рамки и ширины соответствующих фрагментов изображения" src="http://formstyle.com.ua/wp-content/uploads/2013/01/использование-разных-значений-ширины-рамки-и-ширины-соответствующих-фрагментов-изображения.png" width="652" height="202" srcset="http://formstyle.com.ua/wp-content/uploads/2013/01/использование-разных-значений-ширины-рамки-и-ширины-соответствующих-фрагментов-изображения.png 652w, http://formstyle.com.ua/wp-content/uploads/2013/01/использование-разных-значений-ширины-рамки-и-ширины-соответствующих-фрагментов-изображения-300x92.png 300w" sizes="(max-width: 652px) 100vw, 652px" /></a>

У этого изображения неровные края, которые можно растянуть и выложить мозаикой, применив свойство border-image

По обозначенным линиям изображение виртуально «нарезается» на кусочки, которые затем натягиваются или накладываются на отрезки рамки

Первая часть значения border-image — это путь к изображению, и он работает точно так же, как любой другой путь в коде CSS.

<div>
  <p>
    Удивительно, но, указывая в свойстве border-image размер фрагментов для нарезки изображения, единицы измерения (px) добавлять не нужно. В качестве альтернативы можно использовать проценты, обозначающие ширину фрагментов по отношению к размеру самого изображения — и в этом случае необходимо после числового значения добавлять символ %.
  </p>
</div>

&nbsp;

Затем идет последовательность из одного или нескольких чисел, обозначающих места разреза изображения. В нашем примере мы добавили четыре значения, так как с каждого края отрезаются фрагменты разной ширины. Первое значение, 30 — это смещение внутрь от верхней кромки изображения, заданное в пикселах. Второе, 25 — это смещение внутрь от правой кромки; третье — смещение внутрь от нижней кромки; и четвертое — от левой. Браузер разрезает изображение по этим линиям, получая в результате девять фрагментов, которые он затем накладывает на каждый из отрезков рамки, на ее углы и внутреннюю часть поля.

ЦЕНТРАЛЬНЫЙ ФРАГМЕНТ

Центральный фрагмент нарезанного изображения закрывает всю внутреннюю область поля внутри рамок. Это не самое интуитивно понятное решение, однако оно обеспечивает определенные возможности стилизации. Если вы не хотите, чтобы центр изображения, предназначенного для оформления рамки, закрывал фоновое изображение или фоновый цвет поля, то откройте программу для обработки графики, сделайте центральный фрагмент этого изображения прозрачным и сохраните его в файле GIF или PNG с поддержкой прозрачности. В спецификации говорится, что по умолчанию центральный фрагмент отбрасывается, если только вы не добавили в список значений border-image слово fill. Однако создается впечатление, что в настоящее время ни один браузер ключевое слово fill не поддерживает, и они все по умолчанию заполняют центр поля, причем возможность отменить заполнение не предусмотрена.

Свойство border-image входит в модуль Backgrounds and Borders (Фон и границы), который вы найдете по адресу <http://www.w3.org/TR/css3-background>. Это собирательное свойство, однако отдельные свойства использовать пока что невозможно, так как никакие браузеры не поддерживают их объявление за пределами свойства border-image.

Внутри свойства border-image вы задаете путь к изображению и указываете, на каком расстоянии от каждого края производится разрез. Кроме того, можно выбрать способ повторения каждого фрагмента изображения (за исключением углов) вдоль соответствующего отрезка рамки.

Допускается использование от одного до четырех значений ширины отрезанных фрагментов; ваш выбор зависит от того, нужны вам фрагменты одинаковой ширины или разной. Если указано одно значение, то оно применяется ко всем четырем сторонам изображения; если два, то первое применяется к верхнему и нижнему краю, а второе к правому и левому; среди трех значений первое применяется к верхнему краю, второе к правому и левому, а третье к нижнему; если заданы все четыре значения, то они последовательно применяются к краям изображения, начиная с верхнего, по часовой стрелке. На рис. 3.15 показана схема нарезки изображения, предназначенного для оформления рамки.

Задать способ повторения можно четырьмя ключевыми словами: stretch, repeat, round и space. Если указано только одно значение, оно применяется ко всем четырем сторонам; если два, то первое применяется к верхнему и нижнему отрезкам рамки, а второе — к правому и левому. Значение repeat заставляет браузер последовательно заполнять все четыре отрезка рамки и центр поля копиями изображения; stretch означает растягивание изображения по размеру соответствующей области; round — это заполнение копиями с масштабированием, для того чтобы ни одна из копий не была обрезана; space означает заполнение рамки копиями без масштабирования — они равномерно распределяются вдоль отрезков, и между копиями остаются равные промежутки.

Не забывайте, что в дополнение к border-image всегда нужно определять свойство border-width, задающее ширину рамки, иначе ее невозможно будет заполнить изображениями. Также существует свойство border-image-width, но в настоящее время его не поддерживает ни один из браузеров, точно так же они не поддерживают border-image-outset.

К сожалению, изображения нельзя накладывать на рамки, скругленные с помощью свойства border-radius.

Помимо создания эффекта оторванной страницы, свойство border-image можно применять для решения следующих задач:

•    создание кнопок (см. <http://ejohn.org/blog/border-image-in-firefox>);

•    градиентные фоны;

•    украшение рамок поля зубцами — так его можно сделать похожим на марку или лотерейный билет;

•    оформление поля в «деревянную рамку» — как картину или сертификат (см. http:// [www.norabrowndesign.com/css-experiments/border-image-frame.html][1]);

•    скругление угла поля или просто изменение угла стыка на более острый или тупой;

•    создание скругленных или заостренных падающих теней для полей (box-shadow позволяет создавать только прямые тени, однако вы можете нарисовать неправильную тень и встроить ее в рамку поля).

Поддержка свойства border-image в браузерах

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
      Safari
    </td>
    
    <td>
      Chrome
    </td>
  </tr>
  
  <tr>
    <td>
      Нет
    </td>
    
    <td>
      Частично: с префиксом -moz-, начиная с 3.5
    </td>
    
    <td>
      Частично, начиная с версии 10.5
    </td>
    
    <td>
      Частично,</p> 
      
      <p>
        с префиксом -webkit-</td> 
        
        <td>
          Частично
        </td></tr> </tbody> </table> 
        
        <p>
          Конкретный способ наложения изображений на поле и его рамку зависит от третьей составляющей свойства border-image — значения, определяющего повторение. В нашем примере мы используем значение stretch, которое заставляет браузер растягивать все четыре изображения для рамки на все доступное пространство (то же самое происходит и с центральным фрагментом, но не с фрагментами, закрывающими углы), как на рис. 3.16. Можно также добавить значение repeat (рис. 3.17), round (рис. 3.18) или space. (В настоящее время значение round поддерживается только в браузерах Firefox и Opera.) Ни один из браузеров не поддерживает значение space, поэтому у меня нет возможности показать вам снимок экрана!
        </p>
        
        <div id="attachment_2071" style="width: 653px" class="wp-caption aligncenter">
          <a href="http://formstyle.com.ua/fonovye-izobrazheniya/tak-rabotaet-svojstvo-border/" rel="attachment wp-att-2071"><img class="size-full wp-image-2071" title="Так работает свойство border- Рис. 3.17. Так работает свойство border-image со значением stretch    image    со    значением    repeat" alt="Так работает свойство border-" src="http://formstyle.com.ua/wp-content/uploads/2013/01/Так-работает-свойство-border-.png" width="643" height="119" srcset="http://formstyle.com.ua/wp-content/uploads/2013/01/Так-работает-свойство-border-.png 643w, http://formstyle.com.ua/wp-content/uploads/2013/01/Так-работает-свойство-border--300x55.png 300w" sizes="(max-width: 643px) 100vw, 643px" /></a>
          
          <p class="wp-caption-text">
            Так работает свойство border- Рис. 3.17. Так работает свойство border-image со значением stretch image со значением repeat
          </p>
        </div>
        
        <div id="attachment_2081" style="width: 270px" class="wp-caption aligncenter">
          <a href="http://formstyle.com.ua/fonovye-izobrazheniya/border-image-so-znacheniem-round/" rel="attachment wp-att-2081"><img class="size-full wp-image-2081" alt="Так работает свойство border-image со значением round Добавление изображения оторванного края" src="http://formstyle.com.ua/wp-content/uploads/2013/01/border-image-со-значением-round.png" width="260" height="118" /></a>
          
          <p class="wp-caption-text">
            Так работает свойство border-image со значением round Добавление изображения оторванного края
          </p>
        </div>
        
        <p>
          Давайте, наконец, добавим свойство border-image в блок div нашей статьи, чтобы страница стала похожа на вырванный из блокнота лист бумаги, как на рис. 3.12. Изображение необходимо наложить только на левый отрезок рамки, поэтому для начала мы увеличим его размер до 50 пикселов (ширина изображения), а остальные отрезки той же рамки сделаем невидимыми, нулевой ширины:
        </p>
        
        <p>
          #paper {
        </p>
        
        <p>
          float: left; margin: 40px;
        </p>
        
        <p>
          padding: 3.2em 1.6em 1.6em 1.6em; border-width: 0 0 0 50px;
        </p>
        
        <p>
          background: url(images/paperlines.gif) #FBFBF9; background: url(images/thumbtack.png) 50% 5px no-repeat, url(images/stains1.png) 90% -20px no-repeat, url(images/stains2.png) 30% 8% no-repeat, url(images/stains3.png) 20% 50% no-repeat, url(images/stains4.png) 40% 60% no-repeat, url(images/paperlines.gif) #FBFBF9; -moz-background-size: auto, auto, auto, auto, auto,
        </p>
        
        <p>
          auto 1.6em;
        </p>
        
        <p>
          -webkit-background-size: auto, auto, auto, auto, auto,
        </p>
        
        <p>
          auto 1.6em;
        </p>
        
        <p>
          background-size: auto, auto, auto, auto, auto,
        </p>
        
        <p>
          auto 1.6em;
        </p>
        
        <p>
          <sup>}</sup>
        </p>
        
        <p>
          &nbsp;
        </p>

 [1]: http://www.norabrowndesign.com/css-experiments/border-image-frame.html