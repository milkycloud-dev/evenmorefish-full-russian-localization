<p align="center"><img src="assets/icon.png" width="128" height="128" alt="EvenMoreFish: Full Russian Localization icon"></p>

<h1 align="center">EvenMoreFish: Full Russian Localization</h1>

<p align="center">
  Polished Russian localization package for EvenMoreFish v2.5.3 (all 7 rarities, 86 fish, messages, and competition guide).<br>
  Полный пакет русской локализации плагина EvenMoreFish v2.5.3 (все 7 редкостей, 86 видов рыб, сообщения и руководство по турнирам).
</p>

<p align="center">
  <a href="https://github.com/milkycloud-dev/evenmorefish-full-russian-localization/actions/workflows/build.yml"><img src="https://github.com/milkycloud-dev/evenmorefish-full-russian-localization/actions/workflows/build.yml/badge.svg" alt="Build"></a>
  <a href="https://github.com/milkycloud-dev/evenmorefish-full-russian-localization/releases/latest"><img src="https://img.shields.io/github/v/release/milkycloud-dev/evenmorefish-full-russian-localization" alt="Release"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-MIT-lightgrey" alt="License: MIT"></a>
</p>

<p align="center">
  <a href="#english">English</a> | <a href="#русский">Русский</a>
</p>

---

<a id="english"></a>

## English

### Overview

This repository provides clean, standalone Russian localization and configuration files for **EvenMoreFish v2.5.3 (OsomExplosion)**.
It contains complete configuration, language messages, and rarity definitions to respect original author licensing and copyright requirements.

### Content

- `rarities/*.yml`: Complete Russian localization for all 7 rarity files:
  - `common.yml`: 21 fish species
  - `rare.yml`: 21 fish species
  - `epic.yml`: 21 fish species
  - `legendary.yml`: 13 fish species
  - `junk.yml`: 4 junk items
  - `lava.yml`: 4 lava species
  - `void.yml`: 2 end void species
- `messages.yml`: 100% Russian translation in MiniMessage format:
  - Fixes bossbar spacing bug: `bossbar.layout` (`'{prefix}<reset>{time-formatted} <reset>{remaining}'`) prevents timer and remaining text from concatenating (`9м 9состалось` -> `9м 9с осталось`).
  - Fixes typo in `time-alert` (`оконцания` -> `окончания`).
  - Fully translates admin commands, user help menu, competition leaderboards, bait lores, AFK warnings, and toggle messages.
- `config.yml`: Production configuration configured for `locale: ru`.

### Competition and Tournament Management

If you wish to disable automated fishing tournaments completely (e.g. to prevent intrusive bossbars on survival servers):
1. In `competitions/main.yml`, `competitions/sunday.yml`, and `competitions/weekend.yml`, set:
   ```yaml
   disabled: true
   times: []
   days: {}
   ```
2. **Critical Implementation Detail**: EvenMoreFish's internal `AbstractFileBasedManager.loadItemsFromFiles()` invokes `FileUtil.getFilesInDirectory()` with recursive file discovery. It scans and attempts to parse **every single file** inside `plugins/EvenMoreFish/competitions/`, ignoring file extensions. If backup files such as `main.yml.bak-12345` remain inside `competitions/`, EvenMoreFish will load them as active competitions!
3. Always store backups outside `competitions/` (for example, in `plugins/EvenMoreFish/backups/competitions/`).
4. End any active competition via console:
   ```bash
   emf admin competition end
   ```

### Auto-Updater Protection

If your server runs an automated plugin updater (such as `vanilla-plugin-updater` or similar tools), make sure to exclude or configure `EvenMoreFish` appropriately to avoid overwriting your custom localizations or competition schedules:
```json
"EvenMoreFish": {
  "ignore": true,
  "auto": false
}
```

### Installation

1. Stop your Minecraft server or prepare your console.
2. Copy `rarities/` folder and `messages.yml` into your server's `plugins/EvenMoreFish/` directory.
3. Start the server, or execute `/emf admin reload` from console.

### Releases

Pre-built ready-to-use binaries and zip archives are available for download in [Releases](https://github.com/milkycloud-dev/evenmorefish-full-russian-localization/releases/latest).

### License

MIT License. Created by milkycloud-dev (2026).

---

<a id="русский"></a>

## Русский

### Описание

Репозиторий содержит готовые файлы русской локализации для рыболовного плагина **EvenMoreFish v2.5.3 (OsomExplosion)**.
В состав включены исключительно файлы конфигурации и переводов, без модификации закрытого кода, с соблюдением требований лицензии автора.

### Содержимое

- `rarities/*.yml`: Полная русская локализация всех 7 категорий редкости и 86 видов рыб:
  - `common.yml` (Обычная): 21 вид рыбы
  - `rare.yml` (Необычная): 21 вид рыбы
  - `epic.yml` (Эпическая): 21 вид рыбы
  - `legendary.yml` (Легендарная): 13 видов рыбы
  - `junk.yml` (Мусор): 4 предмета
  - `lava.yml` (Лавовая): 4 лавовых существа
  - `void.yml` (Пустотная): 2 пустотных обитателя Энда
- `messages.yml`: 100% русский перевод всех сообщений в формате MiniMessage:
  - Исправлен дефект слипания текста в боссбаре: в `bossbar.layout` добавлен обязательный пробел между форматированным временем и подписью остатка (`'{prefix}<reset>{time-formatted} <reset>{remaining}'`), устраняющий появление строки `9м 9состалось` вместо `9м 9с осталось`.
  - Исправлена опечатка в сообщении `time-alert` (`оконцания` заменено на `окончания`).
  - Полностью переведены команды администратора, справочное меню, лидерборды, описания наживок, предупреждения об AFK-рыбалке и переключатели режимов.
- `config.yml`: Преднастроенный файл конфигурации с параметром `locale: ru`.

### Управление соревнованиями и турнирами

Если вы хотите полностью отключить автоматические рыболовные соревнования (например, чтобы убрать навязчивый боссбар):
1. В файлах `competitions/main.yml`, `competitions/sunday.yml` и `competitions/weekend.yml` установите:
   ```yaml
   disabled: true
   times: []
   days: {}
   ```
2. **Важная техническая деталь реализации**: внутренний загрузчик `AbstractFileBasedManager.loadItemsFromFiles()` в EvenMoreFish вызывает `FileUtil.getFilesInDirectory()` с рекурсивным поиском файлов и загружает абсолютно все файлы внутри папки `plugins/EvenMoreFish/competitions/`, не фильтруя по расширению `.yml`. Если внутри папки остаются резервные копии вроде `main.yml.bak-12345`, плагин продолжит считывать их как активные соревнования.
3. Все резервные копии необходимо хранить вне папки `competitions/` (например, в `plugins/EvenMoreFish/backups/competitions/`).
4. Завершите активный турнир консольной командой:
   ```bash
   emf admin competition end
   ```

### Защита от автообновлений

При использовании автообновлятора плагинов (например, `vanilla-plugin-updater`) добавьте `EvenMoreFish` в список исключений, чтобы обновлятор не сбросил ваши настройки и локализации:
```json
"EvenMoreFish": {
  "ignore": true,
  "auto": false
}
```

### Установка

1. Остановите сервер или подготовьте консоль.
2. Скопируйте папку `rarities/` и файл `messages.yml` в папку `plugins/EvenMoreFish/`.
3. Запустите сервер или выполните команду `/emf admin reload`.

### Релизы

Готовые архивы и пакеты доступны для загрузки в разделе [Releases](https://github.com/milkycloud-dev/evenmorefish-full-russian-localization/releases/latest).

### Лицензия

MIT License. Создано milkycloud-dev (2026).
