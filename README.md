<h1 align="center">Bootloader Donldr</h1> 

## Загрузчик ядра, написан на FASM. 
#### Позваляет запускать свой код размером до 64 Кб из под голого железа, в real-addres mode процессора.
### Инструкция для использования:
1. Приготовьте USB накопитель с таблицей разделов MBR.
2. Скомпилируйте исходный код в бинарный файл.
3. Содержмое бинарного файла при помощи любого бинарного редактора добавьте в MBR запись, начиная с нулевого смещения.
### Внимание - данные MBR записи, которые находятся начиная с 446 байта и до конца сектара, не нужно модифицировать, что бы сохранить флэш накопитель в рабочем состоянии.   
4. Скомпилируйте исходный код, который вы собираетесь запустить в real-addres mode, в бинарный вид с названием kernel.sys.
5. Скопируйте бинарный файл kernel.sys в корень USB накопителя.
6. Перезагрузите ПК, и выберете в качестве загрузочного устройства ваш USB накопитель.
