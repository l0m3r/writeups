# **UGRA_CTF**
Link to [course](https://course.ugractf.ru)

## **Keys**

### **01. Стеганография**

**Задача А. Во все поля** Нужно открыть изображение из таска с помощью `wxhexeditor`. Далее через поиск найти начало ключа `ugra_`. Обратить внимание, что ключ состоит из нескольких частей!
(`ugra_like_sage_but_it_is_white_b95cbe94e`)

**Задача B. Коды-кодики** Нужно открыть изображение из таска с помощью `Stegsolve`. Далее листать срезы с помощью кнопки > внизу. Отсканировать найденный QR-код.
(`ugra_distant_places_are_distant_7eee394b7`)

**Задача C. Скрытый текст** Нужно открыть pdf через графический редактор `ImageMagick` (можно попробовать другое ПО, либо в редакторе pdf поиграться с цветовом шрифта). В явновом виде будут видны части флага.
(`ugra_invisible_4beef2984`)

**Задача D. OOXML** С помощью `binwalk` изучить содержимое скачанного docx и извлечь все содержимое (`-e`). Ключ находится в файле flag.txt.
(`ugra_docx_is_zip_26aa3745f6a3`)

**Задача E. Разрез** Для начала стоит ознакомиться со [статьей](https://habr.com/ru/articles/130472/). Затем:
1. Используя `wxhexeditor` найти чанк IHDR и определить размеры изображения;
2. Попробовать изменить ранее найденные параметры и CRC часть, чтобы избежать ошибки подсчета контрольной суммы;
3. Повторно открыть "увеличенное" изображение и увидеть флаг.
(`ugra_wow_extra_size_42b457`)

### **02. Форензика**

**Задача А. Лучшие снимки** Используя `photorec` восстановить данные их скачанного образа. Ключ находится в одном из файлов.
(`ugra_remember_your_backups_5fd3440e9ada`)

**Задача B. Лес густой** Скачать и открыть логи. Через поиск найти ключ.
(`ugra_find_and_let_it_be_found_ae5c3de717d`)

**Задача C. Загрузка** Открыть скачанный дамп с помощью `wireshark`. Меню File - Export Objects - HTTP. Ключ находится в картинке.
(`ugra_this_is_icon_96a7518c8a4357194f00732f265`)

**Задача D. Сетевая атака** Открыть скачанный дамп с помощью `wireshark`. Меню File - Export Objects - HTTP, выгрузить все, пробежаться по страницам и собрать ключ.
(`ugra_pcap_with_trash_6e2cc2999b78cc7`)

**Задача E. Энтерпрайз I** Скачать архив, используя `bunzip` распаковать архив memory_dump.gz.bz2. `zcat memory_dump.gz| fgrep -za ugra`.
(флаг вытащить не удалось, т.к. долго парсится архив)

### **03. Криптография**

**Задача А. Не Цезарь** Шифр Цезаря или ROT8
(`ugra_know_your_history_a6ee3b9de4`)

