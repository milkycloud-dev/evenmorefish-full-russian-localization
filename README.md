<p align="center"><img src="assets/icon.png" width="128" height="128" alt="EvenMoreFish: Full Russian Localization icon"></p>

<h1 align="center">EvenMoreFish: Full Russian Localization</h1>

<p align="center">
  Polished Russian localization package for EvenMoreFish v2.5.3 (all 7 rarities, 86 fish, messages).<br>
  Полный пакет русской локализации плагина EvenMoreFish v2.5.3 (все 7 редкостей, 86 видов рыб, сообщения).
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
It contains configuration and translation files to respect original author licensing and copyright requirements.

### Content

- `rarities/*.yml`: Complete Russian localization for all 7 rarity files:
  - `common.yml`: 21 fish species
  - `rare.yml`: 21 fish species
  - `epic.yml`: 21 fish species
  - `legendary.yml`: 13 fish species
  - `junk.yml`: 4 junk items
  - `lava.yml`: 4 lava species
  - `void.yml`: 2 end void species
- `messages.yml`: MiniMessage formatted Russian messages for catch broadcasts, hunt notifications, and competition events.
- `config.yml`: Default configuration configured for `locale: ru`.

### Installation

1. Stop your Minecraft server.
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
- `messages.yml`: Перевод всех сообщений в формате MiniMessage (оповещения о вылове, охоте, турнирах).
- `config.yml`: Преднастроенный файл конфигурации с параметром `locale: ru`.

### Установка

1. Остановите сервер или подготовьте консоль.
2. Скопируйте папку `rarities/` и файл `messages.yml` в папку `plugins/EvenMoreFish/`.
3. Запустите сервер или выполните команду `/emf admin reload`.

### Релизы

Готовые архивы и пакеты доступны для загрузки в разделе [Releases](https://github.com/milkycloud-dev/evenmorefish-full-russian-localization/releases/latest).

### Лицензия

MIT License. Создано milkycloud-dev (2026).
