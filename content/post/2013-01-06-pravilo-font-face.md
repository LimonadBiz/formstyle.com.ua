---
title: Правило @font-face
author: admin
type: post
date: 2013-01-06T18:02:46+00:00
url: /pravilo-font-face/
categories:
  - Css 3

---
Правило @font-face входит в модуль Fonts (Шрифты), который вы найдете по адресу: http://www.w3.org/TR/css3-fonts.

Правило @font-face позволяет связать с семейством шрифтов название по вашему выбору (для этого применяется дескриптор font-family) и указать пути к одному или нескольким файлам шрифтов (с помощью дескриптора src). Также допускается определение стилей отдельных гарнитур (с помощью font-weight, font-style и font-stretch). Для того чтобы объединить гарнитуры в одно семейство, укажите одно и то же имя font-family в нескольких правилах @font-face.

Использовать шрифты из правил @font-face просто: всего лишь добавляйте названия нужных семейств шрифтов в стеки шрифтов в свойстве font-family.

Помимо создания «рукописного» текста, правило @font-face позволяет решать следующие задачи:

• стилизация текста различными другими способами, недоступными при использовании стандартных безопасных для веб шрифтов;

•    сохранение единого фирменного стиля на отпечатанных материалах (логотип или рекламная брошюра) и веб-сайте;

•    отображение символов, не входящих в латинский алфавит, которые не всегда правильно выводятся в шрифтах по умолчанию. Использование шрифта, разработанного специально для требуемого языка, гарантирует правильное отображение всех символов.

Наверняка многих из вас посетила идея использовать правило @font-face для создания графических значков без использования изображений — с помощью символов шрифтов dingbat. Однако этот подход может повлечь серьезные проблемы с удобством доступа к содержимому. Подробнее о проблемах и возможных решениях рассказывается на страницах [http://filamentgroup.com/lab/dingbat\_webfonts\_accessibility_issues][1] и <http://jontangerine>. com/log/2010/08/web-fonts-dingbats-icons-and-unicode.

Поддержка правила @font-face в браузерах

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
      Safari Chrome
    </td>
  </tr>
  
  <tr>
    <td>
      Да
    </td>
    
    <td>
      Да, начиная с версии 3.5
    </td>
    
    <td>
      Да, начиная с версии 10
    </td>
    
    <td>
      а</p> 
      
      <p>
        Д
      </p>
      
      <p>
        а
      </p>
      
      <p>
        Д</td> </tr> </tbody> </table>

 [1]: http://filamentgroup.com/lab/dingbat_webfonts_accessibility_issues