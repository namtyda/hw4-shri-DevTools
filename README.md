## Основное задание

1. #### Network
  - HAR архив в репе
   - дублирование ресурсов
   В основном тут запросы на показ контекстной рекламы, но они подгружают каждый раз одно и тоже.
    ![](screen/duplicate1.png)
    ![](screen/duplicate2.png)
    ![](screen/duplicate3.png)
    ![](screen/duplicate4.png)

  - медленно загружающиеся ресурсы
  Картинки которые не пережаты, большие либы со скриптами.
  ![](screen/timeLoadedres.png)

  - ресурсы, блокирующие загрузку
  Здесь просто куча css и JS файлов.
    ![](screen/blockLoad.png)
   - Лишний размер ресурса
   Самый большой размер у картинок, которые не пережаты.
   ![](screen/sizeimg.png)

   - Еще подгружаются старые версии скриптов, вместе с новыми. В которых код дублируется, но не полностью.

2. #### Performance 
 - First Paint: 928ms
 - First Meaningful Paint: 1611ms
 - DOM Content Loaded: 2490ms
 - Load: 5314ms

- Loading, Scripting, Rendering, Painting
 ![](screen/rangeLoad.png)

3. #### Coverage
- Вкладка после загрузки

![](screen/Coverage.png)

- Объём неиспользованного CSS: ~380кб

- Объём неиспользованного JS: ~ 1360кб

## Бонусное задание

1. #### Network
  - HAR архив в репе
   - дублирование ресурсов
   Не изменилось
    

  - медленно загружающиеся ресурсы
  Те же самые ресурсы, только время увеличилось. Но некоторые так и не загрузились, например тот запрос который долго висел в первом случае. И оставался со status code 303
  ![](screen/network3gslow.png)

  - ресурсы, блокирующие загрузку
  Здесь просто куча css и JS файлов.
    ![](screen/blockSlow3g1.png)
    ![](screen/blockslow3g2.png)

   - Лишний размер ресурса
   Те же картинки, котоыре не пережаты. И js, с картинками ситуация ожидамое ухудшилась.
   ![](screen/sizeimg.png)

   - Часть ресурсов googlesyndication просто не догрузились, не дождавшись таймаута видимо. И дргуие похожие ресурсы контекстной рекламы тоже рипнулись.

   2. #### Performance 
 - First Paint: 10182ms
 - First Meaningful Paint: 13431ms
 - DOM Content Loaded: 27525ms
 - Load: 68925ms

- Loading, Scripting, Rendering, Painting
 ![](screen/rangeLoad3gSlow.png)

 3. #### Coverage
- Вкладка после загрузки

![](screen/coverageSlow3g.png)
Объем +- такой же

- Объём неиспользованного CSS: ~380кб

- Объём неиспользованного JS: ~ 1360кб