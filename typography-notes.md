# Typography notes — Samal Detox

## Рабочие пары

1. **Cormorant Garamond Italic + IBM Plex Sans** — наиболее редакционная и выразительная пара.
2. **PT Serif Italic + Inter** — спокойная, привычная и собранная пара.
3. **Lora Italic + Noto Sans** — мягкий человеческий ритм с хорошей читаемостью на мобильном.

Во всех трёх парах локализованы отдельные normal/italic-файлы и подключены относительными путями из `assets/fonts/`. Данные образца одинаковы во всех карточках.

## Источники и лицензии

- Cormorant Garamond — Google Fonts, OFL-1.1: <https://fonts.google.com/specimen/Cormorant+Garamond>
- IBM Plex Sans — IBM, OFL-1.0: <https://fonts.google.com/specimen/IBM+Plex+Sans>
- PT Serif — ParaType, OFL-1.1: <https://fonts.google.com/specimen/PT+Serif>
- Inter — Rasmus Andersson, OFL-1.1: <https://fonts.google.com/specimen/Inter>
- Lora — Cyreal, OFL-1.1: <https://fonts.google.com/specimen/Lora>
- Noto Sans — Google, OFL-1.1: <https://fonts.google.com/noto/specimen/Noto+Sans>

Файлы в проекте получены из опубликованных Google Fonts CSS endpoints 2026-09-10. Лицензии OFL допускают встраивание и распространение шрифтов при сохранении текста лицензии; для production рекомендуется сохранить полные LICENSE-файлы рядом с ассетами.

## Coverage evidence

Проверена таблица `cmap` каждого локального файла через `fontTools.ttLib.TTFont`. Набор проверки включал символы из реального образца:

`С заботой о вас. На каждом этапе. Самал Булатханкызы ә ғ қ ң ө ұ ү һ і Ә Ғ Қ Ң Ө Ұ Ү Һ І ₸ ₽ $`

Результат по всем файлам ниже: **missing = none**.

| Файл | Роль | Проверка |
| --- | --- | --- |
| `cormorant-garamond.ttf` | italic heading | normal text + Kazakh + currencies |
| `ibm-plex-sans.ttf` | sans body | normal text + Kazakh + currencies |
| `pt-serif.ttf` | italic heading | normal text + Kazakh + currencies |
| `inter-variable.ttf` | sans body | normal text + Kazakh + currencies |
| `lora-italic.ttf` | italic heading | normal text + Kazakh + currencies |
| `noto-sans-normal.ttf` | sans body | normal text + Kazakh + currencies |

Примечание: `cmap` подтверждает наличие glyph mapping в локальном файле, но не заменяет визуальную proofread-проверку форм отдельных знаков в production-браузерах.

## Исключённые кандидаты

- Manrope: в скачанном файле отсутствовали казахские `ә ғ қ ң ұ` и `₸`.
- PT Sans: в скачанном файле отсутствовал `₸`.
- Petrona Italic из локальной коллекции: файл не покрывал русскую/казахскую кириллицу.
