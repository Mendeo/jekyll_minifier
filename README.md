# Jekyll Minifier

**Перед использованием на реальном сайте, сначала убедитесь, что у вас всё работает как нужно!**

Данный скрипт разработан для минификации html при использовании Jekyll в качестве генератора статических сайтов. Скрипт написан полностью на Liquid, поэтому не требует установки дополнительных модулей, а также полностью совместим с GitHub Pages.  
Под минификацией понимается:
* Удаление html комментариев.
* Удаление ненужных пробелов, табуляций и переносов строк.
* Чувствительные к таким манипуляциям участки html оставить не тронутыми.

Целью разработки собственного минификатора явилось то, что аналоги не удовлетворяли моим запросам. Например портили мне встроенный JS. А В данном минификаторе можно указать какие теги не нужно минифицировать. По умолчанию - это теги script, pre и textarea.
Планируется разработка минификатора JS.

## Как использовать
1. Поместите minifier.html в папку _layouts вашего проекта.
2. Укажите в html файлах проекта шаблон minifier. Например, в большинстве случаев достаточно в начало _layouts/default.html поместить следующее:
```
---
layout: minifier
---
```
Если все ваши html файлы основаны на шаблоне default, то в этом случае они автоматически минифицируются.

Скорректировать какие теги нужно оставлять интактными можно в первой строчке скрипта.