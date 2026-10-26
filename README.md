# mphub-browsers

Запасная копия закреплённого браузера Camoufox и библиотек для MP Hub. Нужна на случай, если у автора Camoufox
(https://github.com/daijro/camoufox) нужный выпуск пропадёт: установщик MP Hub сначала берёт сборку у автора и
только если не вышло, скачивает её отсюда и сверяет sha256.

- браузер: Camoufox 152.0.4-beta.31 (файлы без изменений, байт в байт как у автора);
- библиотеки: camoufox 0.5.8, playwright 1.62.0, psutil 7.2.2 (колёса для Python 3.12) вместе с зависимостями;
- модель отпечатков fpgen model-2/2026 (https://github.com/scrapfly/fingerprint-generator).

Файлы лежат в выпуске `camoufox-0.5.8-browser-152.0.4-beta.31` (раздел Releases), не в самом репозитории.

| Файл | Размер | sha256 |
|---|---|---|
| `camoufox-152.0.4-beta.31-lin.arm64.zip` | 623.6 МБ | `98dbffa9b687d42693dd0abebc47737e651b9e4b6991ba8571c3c29062645c04` |
| `camoufox-152.0.4-beta.31-lin.x86_64.zip` | 632.7 МБ | `3a7958c84c0c1962574bb177a10a247b614823557308ccb7cf2e2bc9ce406c55` |
| `camoufox-152.0.4-beta.31-mac.arm64.zip` | 298.2 МБ | `7b8d12d61de9a9fbd3ce9c034399ba5307e44f4d8951873cc53ad39d20957737` |
| `camoufox-152.0.4-beta.31-mac.x86_64.zip` | 305.1 МБ | `4a6f02ffc1992a41306b00851fc0ef339ff555c92a547fe865690f89b58d8840` |
| `camoufox-152.0.4-beta.31-win.x86_64.zip` | 470.3 МБ | `ed63ea51d2a07f99bacdae0f43b9ff5518bfc9ac2f15d84e2251fe06c7141e81` |
| `camoufox-libs-0.5.8-lin.x86_64.zip` | 74.0 МБ | `edd3a96d130d7e51c13eefc8a4f32110a7b5f1755ee550f2623f1b9385971e06` |
| `camoufox-libs-0.5.8-mac.arm64.zip` | 67.6 МБ | `607566669965684ae8f88d8a58087178711fe3e5df49165c362db048e030f01b` |
| `camoufox-libs-0.5.8-mac.x86_64.zip` | 73.7 МБ | `1f0399e288adedf706ef176e9915b9ec2d7bfac94d6aefc89c1f6cf72bf5b562` |
| `camoufox-libs-0.5.8-win.x86_64.zip` | 55.2 МБ | `412786cb0eb52580ecb30e5e28046be2c69d55364ac787fb21bc9b2a7c23e68d` |
| `fpgen-model-2-2026-model-release.zip` | 1.5 МБ | `6530b8322cdaa4ec042921c8d9a0369a0e6e0269ba636c01a7203e4a2f109936` |

Те же хеши — в файле `SHA256SUMS`. Проверка: `sha256sum -c SHA256SUMS`.

## Откуда

Архивы браузера скопированы из выпуска `font-bundle-v1` репозитория daijro/camoufox, хеши совпадают с опубликованными
автором. Колёса скачаны с PyPI. Архив `camoufox-libs-0.5.8-<платформа>.zip` — плоская папка колёс, ставится так:
`pip install --no-index --find-links <папка> camoufox==0.5.8 playwright==1.62.0 psutil==7.2.2`.

## Лицензия

Camoufox распространяется по лицензии MPL-2.0 (текст — в файле `LICENSE`). Исходный код браузера и всех его
изменений — у автора: https://github.com/daijro/camoufox. Здесь исходников нет: это зеркало готовых сборок.
