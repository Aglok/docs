# Майнтентерам и составителям доки
- Сразу извиняюсь за неудобство)
- При составлении документации попросите доступ к [переводам](https://www.transifex.com/sleepingowl/sleepingowl-admin-panel/)
- Кратко описывайте новое значение, стараясь уменьшить кол-во слов и строк для перевода
- Все файлы `*.md` из корня генерятся, править их нет смысла


## Инструкция по обновлению доки
- Правим шаблон нужного файла документации в папке `_convert\template`
- Все переменны к конкретному файлу доки ДОБАВЛЯЕМ (!) в английскую версию локализации (папка `_convert\lng\en`)
- В шаблоне все переменные должны быть {{UPPERCASE}} без пробелов и без пробелов к фигурным скобкам
- В JSON файле ключи без CamelCase
- Не повторяем имена ключей из файла `_convert\lng\en\_sidebar.json` - он подключается ко всем остальным файлам, пользуемся этими ключами для навигаци в подвале
- На сайте переводов нужно обновить ваш измененный `*.json`, для добавления новых строк перевода
- Переводим на русский сами и обновляем его из сайта переводов в репу
- Выполняем файл `_convert\parse.php` в браузере (пока еще новые файлы генерятся в папку `_convert\output`, переносим новые сгенерированные файлы)
- Для перегенерации прибиваем локально папку `_convert\output`
- пушим (на оф. сайте переводы подтягиваются прямо из гита)
