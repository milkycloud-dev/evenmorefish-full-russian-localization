# Changelog

## 1.0.2 (2026-11-20)

- Fish lore uses `{fisherman_lore}` and `{length_lore}` again, so fish without a length no longer show a literal `{length}`; both lore templates are translated.
- `competitions/main.yml`, `sunday.yml` and `weekend.yml` are complete disabled templates with `id`, `type` and `duration`.

## 1.0.1 (2026-11-17)

- Fix bossbar layout spacing: added missing space in `bossbar.layout` (`{time-formatted} <reset>{remaining}`) preventing formatted time and remaining label from concatenating (`9м 9состалось` -> `9м 9с осталось`).
- Fix typo in `time-alert`: corrected `оконцания` to `окончания`.
- 100% full Russian localization of `messages.yml`: translated all admin commands, help page, leaderboard metrics, bait lore, AFK messages, and system alerts.
- Added comprehensive tournament management and competition configuration guide to README.md, documenting the recursive file loading behavior in `competitions/` and safe backup placement.

## 1.0.0 (2026-11-17)

First public release of the Russian localization package for EvenMoreFish v2.5.3.

- Complete translation of all 7 rarity categories (`common`, `rare`, `epic`, `legendary`, `junk`, `lava`, `void`).
- Full Russian display names for all 86 custom fish species.
- Polished Russian translation of `messages.yml` (MiniMessage format), including catch notifications, hunting broadcasts, and competition event announcements.
- Verified compatibility with Paper and Purpur 26.3.
- Pre-built binary package attached in GitHub Releases.
