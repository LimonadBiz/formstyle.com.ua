---
title: Обойти отсутствие поддержки HSLA/RGBA в IE 8 и более ранних версиях
author: admin
type: post
date: 2012-12-30T16:20:00+00:00
url: /obojti-otsutstvie-podderzhki-hslargba-v-ie-8-i-bolee-rannix-versiyax/
categories:
  - Css 3

---
Обойти отсутствие поддержки HSLA/RGBA в IE 8 и более ранних версиях можно несколькими способами.

■    Можно задать сплошной фоновый цвет (в шестнадцатеричном представлении или синтаксисе RGB или HSL), который будет использоваться в качестве замены. Если в коде строка с определением сплошного фонового цвета предшествует версии HSLA/RGBA и вы используете собирательное свойство background в

обеих строках или только в определении HSLA/ RGBA, то IE 8 и предыдущие версии браузера понимают все правильно и игнорируют вариант HSLA/RGBA. Однако если для объявления цвета HSLA/RGBA использовать вместо background свойство background-color, в IE 7 и 6 сплошной цвет отображаться не будет. Эти версии попытаются применить цвет из объявления HSLA/ RGBA, но с учетом того, что это невозможно, в результате на странице не появится вообще никакого цвета. На некоторых сайтах это допустимо, если текст можно прочитать и без фоновой подложки. Однако когда текст становится нечитаемым и при этом собирательное свойство background использовать невозможно, значение сплошного фонового цвета приходится передавать IE 7 и более ранним версиям в правиле, которое способен считать только браузер IE. Подробнее об этом рассказывается в главе 1.

<div>
  <p>
    Существует возможность генерировать изображения PNG программным способом на серверной стороне. На странице http:// leaverou.me/2009/02/bulletproof-cross-browser-rgba-backgrounds вы найдете сценарий PHP, способный создавать их, основываясь на значениях RGBA в коде CSS.
  </p>
</div>

&nbsp;

■    Можно выложить фон крохотными полупрозрачными изображениями в формате PNG. По сравнению с первым вариантом это более продвинутый способ, так как в итоге вы получаете полупрозрачный фон, а не заливку сплошным цветом. Он работает в версиях IE 8 и 7, но не в IE 6 и более ранних, так как эти версии не поддерживают изображения PNG с прозрачностью в альфа-канале. Справиться с этим ограничением поможет фильтр AlphaImageLoader (или один из множества основанных на этом фильтре сценариев реализации прозрачности

в IE). Кроме того, вы можете передать IE 6 значение сплошного фонового цвета или изображение GIF или PNG8. Однако все эти подходы означают массу дополнительной работы и могут существенно снизить производительность страницы: фильтр AlphaImageLoader ужасно медленно работает, а загрузка изображения означает еще один HTTP-запрос.

(Плюс, в нашем случае они абсолютно неприменимы для создания хвостиков, так как каждый хвостик — это лишь отрезок рамки, с которым не может быть связано фоновое изображение.) В целом я не рекомендую использовать фоновые изображения PNG, разве что в ситуациях, когда нет необходимости беспокоиться об обходных путях для IE 6, который не поддерживает прозрачность в альфа-канале изображений PNG.

<div>
  <p>
    Сценарий PIE, о котором я упоминала ранее, также способен заставить IE понимать синтаксис RGBA, но лишь в определенных контекстах. Подробнее об этом рассказывается на странице http:// css3pie.com/documentation/ supported-css3-features.
  </p>
</div>

&nbsp;

■ Можно задать фильтр для IE под названием Gradient. Он работает во всех версиях, начиная с 5.5, и поддерживает полупрозрачные цвета (которые, разумеется, определяются с использованием собственного уникального синтаксиса). Просто выберите в качестве начального и конечного цветов одно и то же значение, для того чтобы избежать эффекта градиента.

Я рекомендую первый и третий варианты. Третий позволяет добиться результата, наиболее близкого к желаемому, — именно за счет полупрозрачного, а не сплошного фона. Однако стоит упомянуть, что фильтр Gradient может творить странные вещи со сглаживанием текста, делая строки немного неровными (взгляните на рис. 2.17). Вам придется делать выбор — стоит ли более симпатичный фон того, чтобы жертвовать красотой текста. Кроме того, добавление фильтра приводит к тому, что в IE 8 хвостик, представляющий собой генерируемое содержимое, исчезает (с другой стороны, в версиях 7 и 6 он вообще никогда не появлялся). Объяснить это я не в состоянии — это просто еще одна из загадок IE.

<a href="http://formstyle.com.ua/?attachment_id=1461" rel="attachment wp-att-1461"><img class="aligncenter size-full wp-image-1461" alt="До (слева) и после (справа) применения фильтра Gradient в IE 8" src="http://formstyle.com.ua/wp-content/uploads/2012/12/До-слева-и-после-справа-применения-фильтра-Gradient-в-IE-8.png" width="240" height="86" /></a><a href="http://formstyle.com.ua/?attachment_id=1471" rel="attachment wp-att-1471"><img class="aligncenter size-full wp-image-1471" alt="До (слева) и после (справа) применения фильтра Gradient в IE 8 right" src="http://formstyle.com.ua/wp-content/uploads/2012/12/До-слева-и-после-справа-применения-фильтра-Gradient-в-IE-8-right.png" width="242" height="88" /></a>

До (слева) и после (справа) применения фильтра Gradient в IE 8. Фильтр делает фоновый цвет полупрозрачным, но сбивает сглаживание текста

В данном случае я предлагаю прибегнуть к помощи фильтра. Поскольку в IE скругленные углы не отображаются и поле комментария теряет сходство с облачком, от хвостика также можно с легким сердцем отказаться.

Можно было бы добавить фильтр прямо внутри правила blockquote — остальные браузеры просто проигнорируют его — однако, как я уже говорила в главе 1, трюки и обходные пути лучше всегда отделять от стандартных правил. Для того чтобы изолировать фильтры, нужно либо создать отдельную таблицу стилей для IE, либо использовать трюк с условными комментариями и тегом html, который также описан в главе 1. Давайте реализуем второй вариант.

Перейдите к открывающему тегу html страницы и замените его следующим кодом:

<!&#8212;[if lt IE 7]><html lang=&#187;en&#187; class=&#187;ie6&#8243;><![endif]&#8212;>

<!&#8212;[if IE 7]><html lang=&#187;en&#187; class=&#187;ie7&#8243;><![endif]&#8212;>

<!&#8212;[if IE 8]><html lang=&#187;en&#187; class=&#187;ie8&#8243;><![endif]&#8212;>

<!&#8212;[if IE 9]><html lang=&#187;en&#187; class=&#187;ie9&#8243;><![endif]&#8212;>

<!&#8212;[if gt IE 9]><html lang=&#187;en&#187;><![endif]&#8212;>

<!&#8212;[if !IE]>&#8212;><html lang=&#187;en&#187;><!&#8212;<![endif]&#8212;>

Чтобы не вбивать весь этот код вручную (я вполне понимаю и разделяю это нежелание!), просто откройте файл speech-bubble_final.html из папки с файлами упражнений для этой главы и скопируйте его оттуда.

Теперь можно создать одно правило для IE 5.5, 6 и 7 и еще одно для IE 8 — синтаксис фильтра в этих двух правилах будет немного различаться. Для начала добавим правило для IE 7 и более ранних версий:

.ie6 blockquote, .ie7 blockquote { background: none;

filter: progid:DXImageTransform.Microsoft.gradient

(startColorstr=#99A6DADC, endColorstr=#99A6DADC); zoom: 1;

<sup>}</sup>

Значение filter разбито на две строки исключительно для удобства чтения. Вы можете перенести строку или записать все содержимое в одной строке, и это никак не повлияет на функционирование кода.

В фильтре Gradient мы просто объявляем начальный и конечный цвета, причем одинаковые. Но цветовые значения выглядят странно, вам не кажется? Это не стандартные шестизначные шестнадцатеричные коды. Дело в том, что первые две цифры описывают значение альфа-прозрачности; это может быть любое шестнадцатеричное значение от 00 до FF, где 00 обозначает полную прозрачность, а FF — полную непрозрачность. Последние шесть цифр — это стандартный шестнадцатеричный код цвета. Следовательно, значение #99A6DADC расшифровывается следующим образом: уровень альфа-прозрачности равен 99, и это шестнадцатеричный эквивалент уровня .6, который мы задавали в синтаксисе HSLA. Цвет остался прежним — A6DADC.

Помимо добавления фильтра, правило для IE 7 и предыдущих версий делает еще одну вещь, а именно — удаляет фоновый цвет; если соответствующую строку не добавить, то фоновый цвет будет отображаться вместо градиента. Кроме того, в IE 6 и предыдущих версиях необходимо включать для правил blockquote свойство hasLayout, без которого фильтр работать не будет. Именно для этого я добавила строку zoom: 1;.