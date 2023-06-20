# Домашняя работа
Для связи насчет проверки домашней работы - тг @ktoSts

## Network
**1. На вкладке Network**
* [Записать и сохранить в HAR архив профиль загрузки ресурсов при открытии страницы](./main/1/main.har)
### Найти неоптимальные места
1) Различные дубликаты ресурсов
   <img src="./main/1/double_0.JPG" width=90%>
   <img src="./main/1/double_1.JPG" width=90%>
   <img src="./main/1/double_2.JPG" width=90%>
   |Шрифты, код на js загружаются по нескольку раз. Также 2 файла code.js с одинаковым кодом(см. HAR профиль).
   user-recognition отправляет несколько POST запросов с ответом 200 и еще 2 OPTION запроса с ответом 204(см. HAR профиль).
2) Лишний размер ресурса. Файлы с лишними комментариями/большими отступами.
   imageLeft_1628667062.5843.jpg и imageRight_1628667062.7146.jpg
   одна и та же картинка, просто отзеркалено (см. HAR профиль).
   <img src="./main/1/overWeight_0.JPG" width=90%>
   <img src="./main/1/overWeight_1.JPG" width=90%>
   <img src="./main/1/overWeight_3.JPG" width=90%>
   <img src="./main/1/overWeight_4.JPG" width=90%>
   На иконках используются не сжатые спрайты пнг(файл linkTo__sprite.png см. HAR профиль).
   Немало файлов без минификации, с ненужными комментариями и лишними отступами.
3) Медленно загружающиеся ресурсы
   <img src="./main/1/waterfall.JPG" width=90%>
4) Ресурсы, блокирующие загрузку
   <img src="./main/1/block.JPG" width=90%>
   <img src="./main/1/wateer.JPG" width=90%>
5) Что-то ещё (ресурсы которые упали с ошибкой)
   <img src="./main/1/error.JPG" width=90%>
   Также много ответов со статусом 302, которые приводят к лишним запросам(см. HAR профиль).
### На вкладке Performance
1) [Записать и сохранить в файл профиль загрузки страницы](./main/2/main.json)
2) Измерить время в миллисекундах от начала навигации до событий First Paint (FP), First Contentful Paint (FCP), Largest Contentful Paint (LCP), DOM Content Loaded (DCL), Load
   <img src="./main/2/2.2fp.JPG" width=90%>
   <img src="./main/2/2.2fcp.JPG" width=90%>
   <img src="./main/2/2.2LCP.JPG" width=90%>
   <img src="./main/2/2.2domCont.JPG" width=90%>
3) Определить, на каком DOM-элементе происходит LCP
   <img src="./main/2/2.3LCP.JPG" width=90%>
4) Измерить, сколько времени в миллисекундах тратится на разные этапы обработки документа (Loading, Scripting, Rendering, Painting)
   <img src="./main/2/2.4time.JPG" width=90%>
### На вкладке Coverage
1) Cохранить скриншот вкладки после загрузки страницы
   <img src="./main/3/1.JPG" width=90%>
2) Измерить в килобайтах объём неиспользованного CSS в ходе загрузки страницы(565kB)
   <img src="./main/3/2.cssCover.JPG" width=90%>
3) Измерить в килобайтах объём неиспользованного JS в ходе загрузки страницы(2.3MB)
   <img src="./main/3/3.js.JPG" width=90%>

## Дополнительное задание Slow 3G и CPU 4x slowdown
### Найти неоптимальные места
Slow частично совпадает с анализом неоптимальных мест в нормальном режиме
1) [Записать и сохранить в HAR архив профиль загрузки ресурсов при открытии страницы](./slow_3G/1/optionally.har)
2) Медленно загружающиеся ресурсы и блокирующие
   <img src="./slow_3G/1/slow.JPG" width=90%>
   <img src="./slow_3G/1/waterf.JPG" width=90%>
### На вкладке Performance
1) [Записать и сохранить в файл профиль загрузки страницы(из-за ограничений на размер файлов профиль на гугл диске)]( https://drive.google.com/file/d/1fmkPtkNmAQ35TSDkeDCBfTLm0M-0ki__/view?usp=sharing )
2) Измерить время в миллисекундах от начала навигации до событий First Paint (FP), First Contentful Paint (FCP), Largest Contentful Paint (LCP), DOM Content Loaded (DCL), Load
      <img src="./slow_3G/2/2.2FP.JPG" width=90%>
      <img src="./slow_3G/2/2.2FSP.JPG" width=90%>
      <img src="./slow_3G/2/2.2LCP.JPG" width=90%>
      <img src="./slow_3G/2/2.2DOM.JPG" width=90%>

3) Определить, на каком DOM-элементе происходит LCP - на том же элементе, что и в первом варианте

4) Измерить, сколько времени в миллисекундах тратится на разные этапы обработки документа (Loading, Scripting, Rendering, Painting)
   <img src="./slow_3G/2/2.4g.JPG" width=90%>

### На вкладке Coverage
1) Cохранить скриншот вкладки после загрузки страницы
   <img src="./slow_3G/3/1.cover.JPG" width=90%>
2) Измерить в килобайтах объём неиспользованного CSS в ходе загрузки страницы
   <img src="./slow_3G/3/2.JPG" width=90%>
3) Измерить в килобайтах объём неиспользованного JS в ходе загрузки страницы
   <img src="./slow_3G/3/3.JPG" width=90%>