<p align="center">
  <h1 align="center">
    <a href="https://github.com/server-ok/rudetext/">
      <img alt="RUDETEXT" src="https://rudetext.vercel.app/api?text=RUDETEXT&font_size=128&font=punky&height=128&anchor=middle"/>
      <br/>
      <img alt="text with character" src="https://rudetext.vercel.app/api?text=text+with+character&font=punky&font_size=32&animation=rainbow&duration=10&text_color=00000000&delay=0.5&anchor=middle"/>
    </a>
  </h1>
</p>
<p align="center">
  <a href="https://github.com/server-ok/">
    <img alt="GitHub commit activity" src="https://img.shields.io/badge/i_love-milk-black?style=for-the-badge&labelColor=FFFFFF"/>
  </a>
  <a href="https://github.com/server-ok/rudetext/">
    <img alt="GitHub commit activity" src="https://img.shields.io/badge/this_TEXT-is_very_RUDE-black?style=for-the-badge&labelColor=FFFFFF&color=000000"/>
  </a>
  <a href="https://github.com/server-ok/rudetext/commits/">
    <img alt="GitHub commit activity" src="https://img.shields.io/github/commit-activity/t/server-ok/rudetext?style=for-the-badge&label=COMMITS&labelColor=FFFFFF&color=000000"/>
  </a>
  <a href="https://github.com/server-ok/rudetext/graphs/contributors">
    <img alt="GitHub commit activity" src="https://img.shields.io/github/contributors/server-ok/rudetext?style=for-the-badge&label=CONTRIBUTORS&labelColor=FFFFFF&color=000000"/>
  </a>
  <a href="https://github.com/server-ok/rudetext/issues/">
    <img alt="GitHub commit activity" src="https://img.shields.io/github/issues/server-ok/rudetext?style=for-the-badge&label=ISSUES&labelColor=FFFFFF&color=000000"/>
  </a>
  <a href="https://github.com/server-ok/rudetext/pulls/">
    <img alt="GitHub commit activity" src="https://img.shields.io/github/issues-pr/server-ok/rudetext?style=for-the-badge&label=PULL+REQUESTS&labelColor=FFFFFF&color=000000"/>
  </a>
</p>

##### Rudetext - это генератор анимированных svg-текстов, цель которого - сделать ваши README более живыми.. Он [работает на Vercel](https://vercel.com), поэтому его можно использовать без собственного хостинга, обратившись к нему с текущим доменом:  https://rudetext.vercel.app/api. Если вы хотите разместить его у себя, вы можете создать форк и сделать /src/ корневым каталогом Vercel. 

# ![Обзор](https://rudetext.vercel.app/api?text=Обзор&font=Segoe+UI&font_size=32&animation=rainbow&duration=10&height=32)
  - [Использование RUDETEXT](#использование-rudetext)
  - [Text + SVG](#text--svg)
    - [Кастомизации](#настройки-текста)
  - [Анимации](#анимации)
    - [Кастомизации](#настройки-анимации)

# Использование RUDETEXT
Чтобы использовать RUDETEXT в разметке, вы используете `![alt text](image)`. Например, `![Rainbow Text](https://rudetext.vercel.app/api?text=Rainbow+Text&animation=rainbow&height=16&width=96&dominant_baseline=auto)` отображается как ![Rainbow Text](https://rudetext.vercel.app/api?text=Rainbow+Text&animation=rainbow&height=16&width=96&dominant_baseline=auto). Параметры запроса разделяются символом `&`. Пробелы могут быть добавлены с помощью `+` или `%20`. Знак + может быть добавлен с помощью `%2b`. Поэтому перед использованием строк в RUDETEXT их следует экранировать.
  
# Text + SVG
Текст может быть передан RUDETEXT с помощью параметра запроса `text`.  
Поскольку RUDETEXT не может получить доступ к DOM для расчета ширины и высоты текста, дефолтные размеры SVG равны `width = font_size * (text.length + 2) / 2` and `height = font_size * 1.5`.  
Вы можете задать ширину и высоту в пикселях вручную, передав параметры запроса `width` и `height`.    
  
# Настройки текста
`text_color` - Цвет текста в RGB HEX. (по умолчанию #FFFFFF)  
`font` - Шрифт текста. Является строкой (string). (по умолчанию `Segoe UI`)  
`font_size` - Размер шрифта текста в пикселях. (16 по умолчанию)  
`anchor` - Привязка текста. `start`, `middle`, `end` и т. д. (по умолчанию `start`)  
`dominant_baseline` - доминирующая базовая линия текста. `авто`, `средняя`, `висячая`. (по умолчанию `средняя`).
  
# Анимации
В RUDETEXT существует множество анимаций. Вы можете выбрать анимацию, передав параметр запроса `animation`.  

Одноразовые анимации: `fall`.  
Цикличные анимации: `rainbow`.  
  
`fall` пример анимации:  
`![RAHH!!](https://rudetext.vercel.app/api?text=RAHH!!&animation=fall&iteration_count=infinite&dominant_baseline=hanging)`  
![RAHH!!](https://rudetext.vercel.app/api?text=RAHH!!&animation=fall&iteration_count=infinite&dominant_baseline=hanging)  

`rainbow` пример анимации:  
`![Rainbowy Rainbows :3](https://rudetext.vercel.app/api?text=Rainbowy+Rainbows+:3&animation=rainbow&duration=3)`  
![Rainbowy Rainbows :3](https://rudetext.vercel.app/api?text=Rainbowy+Rainbows+:3&animation=rainbow&duration=3)  

# Настройки анимации
`delay` - Задержка анимации. Может использоваться для "цепочки" нескольких SVG RUDETEXT. (`0` по умолчанию)  
`duration` - Продолжительность анимации в секундах. Может использоваться для ускорения или замедления анимации. (`0.5` по умолчанию)  
`iteration_count` - Количество повторений анимации. Может быть `бесконечным`, чтобы зациклить ее навсегда. (`1` для однократной анимации, `infinite` для повторяющейся анимации по умолчанию)
