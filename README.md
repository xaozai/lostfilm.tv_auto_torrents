Скрипт скачивает RSS-ленту с новыми релизами с lostfilm.tv, выбирает из ленты нужные сериалы и скачивает их torrent-файлы.

Далее эти торрент файлы можно скопировать в каталог, который мониторится торрент-клиентом или можно использовать другой способ передачи их клиенту (какое-нибудь API). Например, автором используется API Synology DownloadStation для создания задач на скачивание.

Скрипт можно поместить в crontab или другой системный планировщик и выполнять с нужным интервалом (например, каждый час).

[rssdd_transf.xsl](rssdd_transf.xsl) - это специальный шаблон для преобразования RSS (XML), он должен находитья в директории этого скрипта.

Перед запуском скрипта, необходимо указать в нём ваши идентификационные данные на lostfilm.tv (см. [скрипт](lf_get_torrents.sh)) и сделать его исполняемым:
```
chmod +x lf_get_torrents.sh
```

Пример использования:
```
./lf_get_torrents.sh
```
В текущем варианте, после завершения работы скрипт выведет пути/наименования скачанных файлов.
