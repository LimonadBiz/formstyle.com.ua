---
title: 'Ideal Forms &#8212; небольшой фреймворк для создания красивых веб-форм'
author: admin
type: post
date: 2012-04-06T12:55:58+00:00
url: /ideal-forms-nebol-shoj-frejmvork-dlya-sozdaniya-krasivy-h-veb-form/
dsq_thread_id:
  - 638901571
wp-syntax-cache-content:
  - |
    a:4:{i:1;s:16812:"
    <div class="wp_syntax" style="position:relative;"><table><tr><td class="line_numbers"><pre>1
    2
    3
    4
    5
    6
    7
    8
    9
    10
    11
    12
    13
    14
    15
    16
    17
    18
    19
    20
    21
    22
    23
    24
    25
    26
    27
    28
    29
    30
    31
    32
    33
    34
    35
    36
    37
    38
    39
    40
    41
    42
    43
    44
    45
    46
    47
    48
    49
    50
    51
    52
    53
    </pre></td><td class="code"><pre class="html4strict" style="font-family:monospace;"><span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">form</span> <span style="color: #000066;">id</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;myform&quot;</span> <span style="color: #000066;">method</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;post&quot;</span> <span style="color: #000066;">action</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;file.php&quot;</span>&gt;</span>
    &nbsp;
    <span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">fieldset</span>&gt;</span>
    &nbsp;
        <span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">h1</span>&gt;</span>Title<span style="color: #009900;">&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">h1</span>&gt;</span>
    &nbsp;
        <span style="color: #808080; font-style: italic;">&lt;!-- Текст для input --&gt;</span>
        <span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">div</span>&gt;</span>
            <span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">label</span> <span style="color: #000066;">class</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;required&quot;</span>&gt;</span>Name:<span style="color: #009900;">&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">label</span>&gt;</span>
            <span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">input</span> <span style="color: #000066;">type</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;text&quot;</span> <span style="color: #000066;">name</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;text&quot;</span> <span style="color: #66cc66;">/</span>&gt;</span>
        <span style="color: #009900;">&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">div</span>&gt;</span>
    &nbsp;
        <span style="color: #808080; font-style: italic;">&lt;!-- Пункты меню --&gt;</span>
        <span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">div</span>&gt;</span>
            <span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">label</span>&gt;</span>Options:<span style="color: #009900;">&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">label</span>&gt;</span>
            <span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">select</span> <span style="color: #000066;">name</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;select&quot;</span>&gt;</span>
                <span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">option</span>&gt;</span>Number 1<span style="color: #009900;">&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">option</span>&gt;</span>
                <span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">option</span>&gt;</span>Number 2<span style="color: #009900;">&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">option</span>&gt;</span>
                <span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">option</span>&gt;</span>Number 3<span style="color: #009900;">&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">option</span>&gt;</span>
            <span style="color: #009900;">&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">select</span>&gt;</span>
        <span style="color: #009900;">&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">div</span>&gt;</span>
    &nbsp;
        <span style="color: #808080; font-style: italic;">&lt;!-- Элементы radio --&gt;</span>
        <span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">div</span>&gt;</span>
            <span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">label</span>&gt;</span>Radios:<span style="color: #009900;">&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">label</span>&gt;</span>
            <span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">ul</span>&gt;</span>
                <span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">li</span>&gt;&lt;<span style="color: #000000; font-weight: bold;">label</span>&gt;&lt;<span style="color: #000000; font-weight: bold;">input</span> <span style="color: #000066;">type</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;radio&quot;</span> <span style="color: #000066;">name</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;radios&quot;</span> <span style="color: #000066;">value</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;option1&quot;</span> <span style="color: #000066;">checked</span> <span style="color: #66cc66;">/</span>&gt;</span>Option 1<span style="color: #009900;">&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">label</span>&gt;&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">li</span>&gt;</span>
                <span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">li</span>&gt;&lt;<span style="color: #000000; font-weight: bold;">label</span>&gt;&lt;<span style="color: #000000; font-weight: bold;">input</span> <span style="color: #000066;">type</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;radio&quot;</span> <span style="color: #000066;">name</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;radios&quot;</span> <span style="color: #000066;">value</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;option2&quot;</span> <span style="color: #66cc66;">/</span>&gt;</span>Option 2<span style="color: #009900;">&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">label</span>&gt;&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">li</span>&gt;</span>
                <span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">li</span>&gt;&lt;<span style="color: #000000; font-weight: bold;">label</span>&gt;&lt;<span style="color: #000000; font-weight: bold;">input</span> <span style="color: #000066;">type</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;radio&quot;</span> <span style="color: #000066;">name</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;radios&quot;</span> <span style="color: #000066;">value</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;option3&quot;</span> <span style="color: #66cc66;">/</span>&gt;</span>Option 3<span style="color: #009900;">&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">label</span>&gt;&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">li</span>&gt;</span>
            <span style="color: #009900;">&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">ul</span>&gt;</span>
        <span style="color: #009900;">&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">div</span>&gt;</span>
    &nbsp;
        <span style="color: #808080; font-style: italic;">&lt;!-- Чекбоксы checkbox --&gt;</span>
        <span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">div</span>&gt;</span>
            <span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">label</span>&gt;</span>Checks:<span style="color: #009900;">&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">label</span>&gt;</span>
            <span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">ul</span>&gt;</span>
                <span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">li</span>&gt;&lt;<span style="color: #000000; font-weight: bold;">label</span>&gt;&lt;<span style="color: #000000; font-weight: bold;">input</span> <span style="color: #000066;">type</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;checkbox&quot;</span> <span style="color: #000066;">name</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;checkboxes[]&quot;</span> <span style="color: #000066;">value</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;option1&quot;</span> <span style="color: #66cc66;">/</span>&gt;</span>Option 1<span style="color: #009900;">&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">label</span>&gt;&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">li</span>&gt;</span>
                <span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">li</span>&gt;&lt;<span style="color: #000000; font-weight: bold;">label</span>&gt;&lt;<span style="color: #000000; font-weight: bold;">input</span> <span style="color: #000066;">type</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;checkbox&quot;</span> <span style="color: #000066;">name</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;checkboxes[]&quot;</span> <span style="color: #000066;">value</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;option2&quot;</span> <span style="color: #66cc66;">/</span>&gt;</span>Option 2<span style="color: #009900;">&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">label</span>&gt;&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">li</span>&gt;</span>
                <span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">li</span>&gt;&lt;<span style="color: #000000; font-weight: bold;">label</span>&gt;&lt;<span style="color: #000000; font-weight: bold;">input</span> <span style="color: #000066;">type</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;checkbox&quot;</span> <span style="color: #000066;">name</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;checkboxes[]&quot;</span> <span style="color: #000066;">value</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;option3&quot;</span> <span style="color: #66cc66;">/</span>&gt;</span>Option 3<span style="color: #009900;">&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">label</span>&gt;&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">li</span>&gt;</span>
            <span style="color: #009900;">&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">ul</span>&gt;</span>
        <span style="color: #009900;">&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">div</span>&gt;</span>
    &nbsp;
        <span style="color: #808080; font-style: italic;">&lt;!-- Кнопки --&gt;</span>
        <span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">div</span>&gt;</span>
            <span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">label</span>&gt;</span><span style="color: #ddbb00;">&amp;nbsp;</span><span style="color: #009900;">&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">label</span>&gt;</span><span style="color: #808080; font-style: italic;">&lt;!-- Insert empty label to align buttons to the rest of elements --&gt;</span>
            <span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">button</span>&gt;&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">button</span>&gt;</span>
            <span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">input</span> <span style="color: #000066;">type</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;submit&quot;</span> <span style="color: #000066;">value</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;Submit&quot;</span> <span style="color: #66cc66;">/</span>&gt;</span>
            <span style="color: #009900;">&lt;<span style="color: #000000; font-weight: bold;">input</span> <span style="color: #000066;">type</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;reset&quot;</span> <span style="color: #000066;">value</span><span style="color: #66cc66;">=</span><span style="color: #ff0000;">&quot;Reset&quot;</span> <span style="color: #66cc66;">/</span>&gt;</span>
        <span style="color: #009900;">&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">div</span>&gt;</span>
    &nbsp;
    <span style="color: #009900;">&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">fieldset</span>&gt;</span>
    &nbsp;
    <span style="color: #009900;">&lt;<span style="color: #66cc66;">/</span><span style="color: #000000; font-weight: bold;">form</span>&gt;</span></pre></td></tr></table><p class="theCode" style="display:none;">&lt;form id=&quot;myform&quot; method=&quot;post&quot; action=&quot;file.php&quot;&gt;
    
    &lt;fieldset&gt;
    
        &lt;h1&gt;Title&lt;/h1&gt;
    
        &lt;!-- Текст для input --&gt;
        &lt;div&gt;
            &lt;label class=&quot;required&quot;&gt;Name:&lt;/label&gt;
            &lt;input type=&quot;text&quot; name=&quot;text&quot; /&gt;
        &lt;/div&gt;
    
        &lt;!-- Пункты меню --&gt;
        &lt;div&gt;
            &lt;label&gt;Options:&lt;/label&gt;
            &lt;select name=&quot;select&quot;&gt;
                &lt;option&gt;Number 1&lt;/option&gt;
                &lt;option&gt;Number 2&lt;/option&gt;
                &lt;option&gt;Number 3&lt;/option&gt;
            &lt;/select&gt;
        &lt;/div&gt;
    
        &lt;!-- Элементы radio --&gt;
        &lt;div&gt;
            &lt;label&gt;Radios:&lt;/label&gt;
            &lt;ul&gt;
                &lt;li&gt;&lt;label&gt;&lt;input type=&quot;radio&quot; name=&quot;radios&quot; value=&quot;option1&quot; checked /&gt;Option 1&lt;/label&gt;&lt;/li&gt;
                &lt;li&gt;&lt;label&gt;&lt;input type=&quot;radio&quot; name=&quot;radios&quot; value=&quot;option2&quot; /&gt;Option 2&lt;/label&gt;&lt;/li&gt;
                &lt;li&gt;&lt;label&gt;&lt;input type=&quot;radio&quot; name=&quot;radios&quot; value=&quot;option3&quot; /&gt;Option 3&lt;/label&gt;&lt;/li&gt;
            &lt;/ul&gt;
        &lt;/div&gt;
    
        &lt;!-- Чекбоксы checkbox --&gt;
        &lt;div&gt;
            &lt;label&gt;Checks:&lt;/label&gt;
            &lt;ul&gt;
                &lt;li&gt;&lt;label&gt;&lt;input type=&quot;checkbox&quot; name=&quot;checkboxes[]&quot; value=&quot;option1&quot; /&gt;Option 1&lt;/label&gt;&lt;/li&gt;
                &lt;li&gt;&lt;label&gt;&lt;input type=&quot;checkbox&quot; name=&quot;checkboxes[]&quot; value=&quot;option2&quot; /&gt;Option 2&lt;/label&gt;&lt;/li&gt;
                &lt;li&gt;&lt;label&gt;&lt;input type=&quot;checkbox&quot; name=&quot;checkboxes[]&quot; value=&quot;option3&quot; /&gt;Option 3&lt;/label&gt;&lt;/li&gt;
            &lt;/ul&gt;
        &lt;/div&gt;
    
        &lt;!-- Кнопки --&gt;
        &lt;div&gt;
            &lt;label&gt;&amp;nbsp;&lt;/label&gt;&lt;!-- Insert empty label to align buttons to the rest of elements --&gt;
            &lt;button&gt;&lt;/button&gt;
            &lt;input type=&quot;submit&quot; value=&quot;Submit&quot; /&gt;
            &lt;input type=&quot;reset&quot; value=&quot;Reset&quot; /&gt;
        &lt;/div&gt;
    
    &lt;/fieldset&gt;
    
    &lt;/form&gt;</p></div>
    ";i:2;s:1019:"
    <div class="wp_syntax" style="position:relative;"><table><tr><td class="line_numbers"><pre>1
    2
    </pre></td><td class="code"><pre class="css" style="font-family:monospace;">&lt;<span style="color: #F5758F;">link</span> href<span style="color: #00AA00;">=</span><span style="color: #ff0000;">&quot;css/normalize.css&quot;</span> rel<span style="color: #00AA00;">=</span><span style="color: #ff0000;">&quot;stylesheet&quot;</span>/<span style="color: #00AA00;">&gt;</span>
    &lt;<span style="color: #F5758F;">link</span> href<span style="color: #00AA00;">=</span><span style="color: #ff0000;">&quot;css/idealforms/idealforms.css&quot;</span> rel<span style="color: #00AA00;">=</span><span style="color: #ff0000;">&quot;stylesheet&quot;</span>/<span style="color: #00AA00;">&gt;</span></pre></td></tr></table><p class="theCode" style="display:none;">&lt;link href=&quot;css/normalize.css&quot; rel=&quot;stylesheet&quot;/&gt;
    &lt;link href=&quot;css/idealforms/idealforms.css&quot; rel=&quot;stylesheet&quot;/&gt;</p></div>
    ";i:3;s:3945:"
    <div class="wp_syntax" style="position:relative;"><table><tr><td class="line_numbers"><pre>1
    2
    3
    4
    5
    6
    7
    8
    9
    10
    11
    12
    13
    14
    15
    </pre></td><td class="code"><pre class="javascript" style="font-family:monospace;"><span style="color: #339933;">&lt;</span>script src<span style="color: #339933;">=</span><span style="color: #3366CC;">&quot;https://ajax.googleapis.com/ajax/libs/jquery/1.7.1/jquery.min.js&quot;</span><span style="color: #339933;">&gt;&lt;/</span>script<span style="color: #339933;">&gt;</span>
    <span style="color: #339933;">&lt;</span>script src<span style="color: #339933;">=</span><span style="color: #3366CC;">&quot;js/jquery.idealforms.js&quot;</span><span style="color: #339933;">&gt;&lt;/</span>script<span style="color: #339933;">&gt;</span>
    <span style="color: #339933;">&lt;</span>script<span style="color: #339933;">&gt;</span>
        <span style="color: #006600; font-style: italic;">// Easy</span>
        $<span style="color: #009900;">&#40;</span><span style="color: #000066; font-weight: bold;">function</span><span style="color: #009900;">&#40;</span><span style="color: #009900;">&#41;</span><span style="color: #009900;">&#123;</span>
            $<span style="color: #009900;">&#40;</span><span style="color: #3366CC;">'#myform'</span><span style="color: #009900;">&#41;</span>.<span style="color: #660066;">idealforms</span><span style="color: #009900;">&#40;</span><span style="color: #009900;">&#41;</span><span style="color: #339933;">;</span>
        <span style="color: #009900;">&#125;</span><span style="color: #009900;">&#41;</span><span style="color: #339933;">;</span>
    &nbsp;
        <span style="color: #006600; font-style: italic;">// Если вы желаете сделать возврат к старым формам</span>
        <span style="color: #006600; font-style: italic;">// на браузерах, которые не поддерживают что-то,</span>
        <span style="color: #006600; font-style: italic;">// вы всегда можете сделать следующее</span>
        <span style="color: #000066; font-weight: bold;">if</span> <span style="color: #009900;">&#40;</span><span style="color: #009900;">&#40;</span>$.<span style="color: #660066;">browser</span>.<span style="color: #660066;">msie</span><span style="color: #009900;">&#41;</span> <span style="color: #339933;">&amp;&amp;</span> <span style="color: #009900;">&#40;</span>$.<span style="color: #660066;">browser</span>.<span style="color: #660066;">version</span> <span style="color: #339933;">&gt;=</span> <span style="color: #3366CC;">'8.0'</span><span style="color: #009900;">&#41;</span><span style="color: #009900;">&#41;</span> <span style="color: #009900;">&#123;</span>
            $<span style="color: #009900;">&#40;</span><span style="color: #3366CC;">'#myform'</span><span style="color: #009900;">&#41;</span>.<span style="color: #660066;">idealforms</span><span style="color: #009900;">&#40;</span><span style="color: #009900;">&#41;</span><span style="color: #339933;">;</span>
        <span style="color: #009900;">&#125;</span>
    <span style="color: #339933;">&lt;/</span>script<span style="color: #339933;">&gt;</span></pre></td></tr></table><p class="theCode" style="display:none;">&lt;script src=&quot;https://ajax.googleapis.com/ajax/libs/jquery/1.7.1/jquery.min.js&quot;&gt;&lt;/script&gt;
    &lt;script src=&quot;js/jquery.idealforms.js&quot;&gt;&lt;/script&gt;
    &lt;script&gt;
        // Easy
        $(function(){
            $('#myform').idealforms();
        });
    
        // Если вы желаете сделать возврат к старым формам
        // на браузерах, которые не поддерживают что-то,
        // вы всегда можете сделать следующее
        if (($.browser.msie) &amp;&amp; ($.browser.version &gt;= '8.0')) {
            $('#myform').idealforms();
        }
    &lt;/script&gt;</p></div>
    ";i:4;s:1205:"
    <div class="wp_syntax" style="position:relative;"><table><tr><td class="line_numbers"><pre>1
    2
    3
    4
    5
    </pre></td><td class="code"><pre class="php" style="font-family:monospace;"><span style="color: #000000; font-weight: bold;">&lt;?php</span>
        <span style="color: #000088;">$id</span> <span style="color: #339933;">=</span> <span style="color: #000088;">$_POST</span><span style="color: #009900;">&#91;</span><span style="color: #0000ff;">&quot;name&quot;</span><span style="color: #009900;">&#93;</span><span style="color: #339933;">;</span>
        <span style="color: #666666; font-style: italic;">// Да, php :)</span>
        <span style="color: #666666; font-style: italic;">// Но вы, конечно же, можете использовать js/ajax для обработки запросов, при желании</span>
    <span style="color: #000000; font-weight: bold;">?&gt;</span></pre></td></tr></table><p class="theCode" style="display:none;">&lt;?php
        $id = $_POST[&quot;name&quot;];
        // Да, php :)
        // Но вы, конечно же, можете использовать js/ajax для обработки запросов, при желании
    ?&gt;</p></div>
    ";}
categories:
  - Склад скриптов
tags:
  - buttons
  - checkbox
  - ideal forms
  - input
  - radio
  - submit
  - веб-формы
  - кнопки
  - скрипты
  - фреймворки

---
<a href="http://formstyle.com.ua/wp-content/uploads/2012/04/cvsept_03_thumb.jpg" rel="lightbox[167]" title="cvsept_03_thumb"><img src="http://formstyle.com.ua/wp-content/uploads/2012/04/cvsept_03_thumb.jpg" alt="" title="cvsept_03_thumb" width="300" height="248" class="aligncenter size-full wp-image-618" /></a>

<span style="color: #000000;"><strong>Требования:</strong> jQuery</span>

<span style="color: #000000;"><strong>Совместимость: </strong>IE 7+, Firefox 3+, Chrome 3+, Safari 3.1+ and Opera 11+</span>

<span style="color: #000000;"><strong>Официальная страница: </strong></span><noindex><a href="http://code.google.com/p/idealforms/" target="_blank">http://code.google.com/p/idealforms/</a></noindex>

<span style="color: #000000;"><strong>Скачать:  </strong></span><noindex><a href="http://code.google.com/p/idealforms/downloads/list" target="_blank">http://code.google.com/p/idealforms/downloads/list</a></noindex>

<span style="color: #000000;">Описание под катом 🙂<!--more--></span>

<span style="color: #000000;">Ideal Forms &#8212; небольшой фреймворк, разработанный на основе jQuery и предназначенный для создания красивых и удобных веб-форм.</span>

<span style="color: #000000;">Фреймворк преобразует стандартные элементы < input > в красивые элементы со скруглёнными углами, обладающие привлекательным эффектом фокуса. К тому же, фреймворк позволяет полностью изменять элементы radio и checkbox.</span>

<span style="color: #000000;">Поскольку фреймворк не использует изображения, для построения форм требуется только минимальный html синтаксис. Формы видоизменяются полностью за счёт CSS (в дистрибутиве фреймворка содержится 3 темы оформления).</span>

<span style="color: #000000;">Фреймворк отлично работает даже при отключенном JavaScript.</span>

<span style="color: #000000;">Для работы с движком выполняем следующее:</span>

### <span style="color: #000000;">HTML</span>

<pre lang="html4strict" line="1" escaped="true">&lt;form id="myform" method="post" action="file.php"&gt;

&lt;fieldset&gt;

    &lt;h1&gt;Title&lt;/h1&gt;

    &lt;!-- Текст для input --&gt;
    &lt;div&gt;
        &lt;label class="required"&gt;Name:&lt;/label&gt;
        &lt;input type="text" name="text" /&gt;
    &lt;/div&gt;

    &lt;!-- Пункты меню --&gt;
    &lt;div&gt;
        &lt;label&gt;Options:&lt;/label&gt;
        &lt;select name="select"&gt;
            &lt;option&gt;Number 1&lt;/option&gt;
            &lt;option&gt;Number 2&lt;/option&gt;
            &lt;option&gt;Number 3&lt;/option&gt;
        &lt;/select&gt;
    &lt;/div&gt;

    &lt;!-- Элементы radio --&gt;
    &lt;div&gt;
        &lt;label&gt;Radios:&lt;/label&gt;
        &lt;ul&gt;
            &lt;li&gt;&lt;label&gt;&lt;input type="radio" name="radios" value="option1" checked /&gt;Option 1&lt;/label&gt;&lt;/li&gt;
            &lt;li&gt;&lt;label&gt;&lt;input type="radio" name="radios" value="option2" /&gt;Option 2&lt;/label&gt;&lt;/li&gt;
            &lt;li&gt;&lt;label&gt;&lt;input type="radio" name="radios" value="option3" /&gt;Option 3&lt;/label&gt;&lt;/li&gt;
        &lt;/ul&gt;
    &lt;/div&gt;

    &lt;!-- Чекбоксы checkbox --&gt;
    &lt;div&gt;
        &lt;label&gt;Checks:&lt;/label&gt;
        &lt;ul&gt;
            &lt;li&gt;&lt;label&gt;&lt;input type="checkbox" name="checkboxes[]" value="option1" /&gt;Option 1&lt;/label&gt;&lt;/li&gt;
            &lt;li&gt;&lt;label&gt;&lt;input type="checkbox" name="checkboxes[]" value="option2" /&gt;Option 2&lt;/label&gt;&lt;/li&gt;
            &lt;li&gt;&lt;label&gt;&lt;input type="checkbox" name="checkboxes[]" value="option3" /&gt;Option 3&lt;/label&gt;&lt;/li&gt;
        &lt;/ul&gt;
    &lt;/div&gt;

    &lt;!-- Кнопки --&gt;
    &lt;div&gt;
        &lt;label&gt;&nbsp;&lt;/label&gt;&lt;!-- Insert empty label to align buttons to the rest of elements --&gt;
        &lt;button&gt;&lt;/button&gt;
        &lt;input type="submit" value="Submit" /&gt;
        &lt;input type="reset" value="Reset" /&gt;
    &lt;/div&gt;

&lt;/fieldset&gt;

&lt;/form&gt;</pre>

### <span style="color: #000000;">CSS</span>

<pre lang="css" line="1" escaped="true">&lt;link href="css/normalize.css" rel="stylesheet"/&gt;
&lt;link href="css/idealforms/idealforms.css" rel="stylesheet"/&gt;</pre>

### <span style="color: #000000;">JavaScript</span>

<pre lang="javascript" line="1" escaped="true">&lt;script src="https://ajax.googleapis.com/ajax/libs/jquery/1.7.1/jquery.min.js"&gt;&lt;/script&gt;
&lt;script src="js/jquery.idealforms.js"&gt;&lt;/script&gt;
&lt;script&gt;
    // Easy
    $(function(){
        $('#myform').idealforms();
    });

    // Если вы желаете сделать возврат к старым формам
    // на браузерах, которые не поддерживают что-то,
    // вы всегда можете сделать следующее
    if (($.browser.msie) && ($.browser.version &gt;= '8.0')) {
        $('#myform').idealforms();
    }
&lt;/script&gt;</pre>

### <span style="color: #000000;">PHP</span>

<pre lang="php" line="1" escaped="true">&lt;?php
    $id = $_POST["name"];
    // Да, php 🙂
    // Но вы, конечно же, можете использовать js/ajax для обработки запросов, при желании
?&gt;</pre>

<span style="color: #000000;">В работе фреймворк можно оценить здесь</span> &#8212; <a href="http://spacirdesigns.com/jqidealforms/" target="_blank">http://spacirdesigns.com/jqidealforms/</a>.

<div id="attachment_170" style="width: 310px" class="wp-caption aligncenter">
  <a href="http://formstyle.com.ua/wp-content/uploads/2012/04/ori2c3.png" rel="lightbox[167]" title="ori2c3"><img class="size-medium wp-image-170" title="ori2c3" src="http://formstyle.com.ua/wp-content/uploads/2012/04/ori2c3-300x290.png" alt="" width="300" height="290" srcset="http://formstyle.com.ua/wp-content/uploads/2012/04/ori2c3-300x290.png 300w, http://formstyle.com.ua/wp-content/uploads/2012/04/ori2c3.png 769w" sizes="(max-width: 300px) 100vw, 300px" /></a>
  
  <p class="wp-caption-text">
    Фреймворк в работе
  </p>
</div>

<p style="text-align: center;">
  <div id="polls-1" class="wp-polls">
  </div>
  
  <div id="polls-1-loading" class="wp-polls-loading">
    <img src="http://formstyle.com.ua/wp-content/plugins/wp-polls/images/loading.gif" width="16" height="16" alt="Загрузка ..." title="Загрузка ..." class="wp-polls-image" />&nbsp;Загрузка ...
  </div>
</p>