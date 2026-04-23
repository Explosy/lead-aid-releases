# LeadAid

Local-first Electron-приложение для тимлидов и engineering manager'ов.
Помогает вести 1:1 встречи с командой: записывать, локально транскрибировать,
извлекать commitments и следить за их выполнением.

**Весь пайплайн работает offline** — аудио, транскрипты, LLM-саммари,
БД. Данные никогда не покидают ваш компьютер.

## Что умеет

**Встречи 1:1**
- Запись аудио прямо из приложения
- Локальная транскрипция (Whisper) и автосаммари (локальный LLM)
- Извлечение commitments, TL;DR, key moments
- SBI feedback templates, post-meeting debrief

**Подготовка**
- Home Dashboard с понедельничным брифингом
- 1:1 Prep: что обсудить, открытые commitments, свежие сигналы
- Coaching mode — пять подсказывающих вопросов, обновляются раз в сутки
- Agenda-mode с carry-over нерешённого

**Follow-through**
- CommitmentList с bulk-операциями, тегами, dueback-напоминаниями
- Cadence tracker — кто давно не встречался
- Mood/pulse, evidence binder для 360-feedback и ревью
- Growth goals на человека

**Команда и нагрузка**
- Person-centric view: встречи, таски, commitments, заметки, наблюдения, goals
- Team heatmap по здоровью 1:1
- Workload drill-down по задачам из трекера (GitLab, GitHub, Yandex Tracker)

**Системное**
- Close-to-tray с меню (паттерн Telegram/Slack)
- Quick-capture push-to-talk, command palette
- Зашифрованная БД (SQLCipher), секреты через системный keychain
- Windows auto-update (Squirrel)

## Установка

### Windows

1. Скачайте `LeadAid-<version>.Setup.exe` из [последнего релиза](https://github.com/Explosy/lead-aid-releases/releases/latest).
2. Запустите — Squirrel поставит приложение в `%LOCALAPPDATA%\LeadAid`.
3. Обновления прилетают автоматически в фоне; при следующем запуске будет предложено перезапуститься.

### macOS / Linux

Пока не публикуются — сборки отключены. Если есть интерес, заведите issue.

## Приватность

LeadAid — solo-tool для менеджера, не облачный продукт. Приложение **не отправляет**
наружу аудио, транскрипты, содержимое commitments, заметок или метрики.

Исходящая сеть — только то, что вы сами настроили: API выбранного трекера
(GitHub/GitLab/Yandex Tracker), OAuth-провайдер для логина, и GitHub Releases
для проверки обновлений.
