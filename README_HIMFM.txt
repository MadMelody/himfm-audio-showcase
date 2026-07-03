ХИМFM — автообновление аудио-витрины

Структура проекта:

папка-проекта/
├─ index.html
├─ tracks.js
├─ himfm_update_site.exe
└─ OUT/
   ├─ ваши mp3/wav/m4a/ogg файлы
   └─ ...

Как работает:
1. Сайт берет список треков из tracks.js.
2. EXE сканирует папку OUT и заново создает tracks.js.
3. Если появился файл с Theme 17 — сайт сам создаст Theme 17.
4. Если файл удален из OUT — после обновления он пропадет с сайта.
5. Служебные цифры перед элементом не показываются: 1_BASIC_ID -> BASIC ID, 2_RAMP -> RAMP.

Как обновить вручную:
1. Положите/удалите треки в OUT.
2. Запустите himfm_update_site.exe двойным кликом.
3. Обновите страницу index.html в браузере.

Как включить автонаблюдение:
1. Положите start_watch.bat рядом с himfm_update_site.exe.
2. Запустите start_watch.bat.
3. Пока окно открыто, изменения в OUT будут автоматически отражаться в tracks.js.

Как собрать EXE из Python:
1. Установите Python для Windows.
2. Положите himfm_update_site.py и build_exe.bat в одну папку.
3. Запустите build_exe.bat.
4. Заберите готовый файл из dist/himfm_update_site.exe.
