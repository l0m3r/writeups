# **UGRA_CTF**
Link to [course](https://course.ugractf.ru)

## **Keys**

### **01. Стеганография**

**Задача A.** Нужно открыть изображение из таска с помощью `wxhexeditor`. Далее через поиск найти начало ключа `ugra_`. Обратить внимание, что ключ состоит из нескольких частей! (`ugra_like_sage_but_it_is_white_b95cbe94e`)

**Задача B.** Нужно открыть изображение из таска с помощью `Stegsolve`. Далее листать срезы с помощью кнопки > внизу. Отсканировать найденный QR-код. (`ugra_distant_places_are_distant_7eee394b7`)

**Задача С.** Нужно открыть pdf через графический редактор `ImageMagick` (можно попробовать другое ПО, либо в редакторе pdf поиграться с цветовом шрифта). В явновом виде будут видны части флага.
(`ugra_invisible_4beef2984`)

**Задача D.** С помощью `binwalk` изучить содержимое скачанного docx и извлечь все содержимое (`-e`). Ключ находится в файле flag.txt.
(`ugra_docx_is_zip_26aa3745f6a3`)

**Задача E.*** Для начала стоит ознакомиться со [статьей](https://habr.com/ru/articles/130472/). Затем:
1. Используя `wxhexeditor` найти чанк IHDR и определить размеры изображения;
2. Попробовать изменить ранее найденные параметры и CRC часть, чтобы избежать ошибки подсчета контрольной суммы;
3. Повторно открыть "увеличенное" изображение и увидеть флаг.
(`ugra_wow_extra_size_42b457`)




