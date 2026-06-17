# Changelog

## [0.1.0-alpha.1] — Unreleased

### Добавлено

- Desktop-приложение МНЕНРАФОТО для Windows 10/11 x64.
- Импорт фотографий из файлов, папок и drag-and-drop.
- Поддержка JPG, JPEG, PNG, WebP, HEIC и HEIF.
- Пакетная обработка и выбор нескольких фотографий.
- Коррекция цвета: яркость, контраст, насыщенность, баланс белого, оттенок.
- Кадрирование, zoom, pan, поворот, выравнивание горизонта, отражение.
- Раскладки 1 / 2 / 4 на листе 10×15, 15×21 и A4.
- Пользовательские пресеты и применение настроек ко всем фотографиям.
- Undo / Redo для правок.
- Память текущего и предыдущего заказа.
- Печать с выбранной фотографии или листа через Windows spooler.
- Setup EXE и Portable EXE.
- Системный Windows HEIC decoder (`MnenraHeicDecoder.exe`) вместо heic2any.
- Onboarding и краткий тур по интерфейсу.

### Улучшено

- Raster WYSIWYG printing для Epson с внутренней калибровкой overscan/split.
- Применение настроек принтера через Windows PrintTicket перед печатью.
- Production-safe загрузка логотипа и иконок в packaged-сборке.
- Windows EXE metadata и embedded icon через post-pack resource editing.

### Исправлено

- Production load path для `dist/index.html` в Electron.
- Отсутствие иконки приложения в установленной Windows-сборке.
- Сломанный логотип в шапке при загрузке через `file://`.
- Лицензионно рискованный HEIC pipeline на базе heic2any/libheif.

### Проверено

- Setup EXE: установка, запуск, повторный запуск, uninstall/reinstall.
- Portable EXE: запуск без установки.
- HEIC: отдельно, пакетно, вместе с JPG/PNG/WebP, кириллица в именах файлов.
- Epson L805: 10×15, A4, layouts 1/2/4.
- Epson L1250: 10×15, layouts 1/2/4.
- JPG, PNG, WEBP, HEIC import без Node/npm/Vite на целевой машине.

### Известные ограничения

- Windows 10 ещё не проверена физически на целевом оборудовании.
- Установщик не подписан; SmartScreen может показать предупреждение.
- Ограниченный список физически проверенных принтеров.
- HEIC требует системных HEIF/HEVC extensions Windows.
- Некоторые HDR/sequence/live-photo HEIC могут не поддерживаться.
- Uninstall намеренно сохраняет пресеты и память заказов.
