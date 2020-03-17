## Основное задание

1. #### Network
  - HAR архив в репе
   - дублирование ресурсов
   В основном тут запросы на показ контекстной рекламы, но они подгружают каждый раз одно и тоже.
    ![](screen/duplicate1.png)
    ![](screen/duplicate2.png)
    ![](screen/duplicate3.png)

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
