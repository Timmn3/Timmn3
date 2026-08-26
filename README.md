## Tim

Backend-разработчик на Python. Пишу асинхронные сервисы и сам их эксплуатирую:
от архитектуры и кода до деплоя, мониторинга и разбора аварий на проде.

Основное направление - Telegram-сервисы с платёжной частью, REST API на FastAPI и Django,
парсинг и автоматизация. Почти всё, что здесь лежит, работает или работало на боевых
серверах с реальными пользователями и деньгами.

### Цифры

| | |
|---|---|
| Непрерывная разработка | окт. 2024 - авг. 2026, без пустых месяцев |
| Проектов в продакшне | 10+ на собственных серверах |
| Платёжных интеграций | 12: YooKassa, Tinkoff, CKassa, FreeKassa, PayOK, StreamPay, Lava, AnyPay, Cryptomus, QIWI, Telegram Stars |
| SMS и почтовых провайдеров | 8: OnlineSim, SMS-Activate, SMSFast, Numlex, SMSA, FirstMail, mail.tm |
| Крупнейший проект | 741 коммит, 32 000 строк, в поддержке 22 месяца |

### Стек

**Python** 3.12, asyncio · aiogram 3 · FastAPI · Django 5 · SQLAlchemy 2 async · Tortoise ORM
· PostgreSQL · Redis · Celery · RabbitMQ · APScheduler
**Frontend** React 18 · TypeScript · Vite · TailwindCSS
**Инфраструктура** Docker · GitHub Actions · Nginx · Prometheus + Grafana · Linux · supervisor · systemd
**Прочее** Playwright · Selenium · pytest · Alembic · Aerich · Sentry

### Проекты

| Проект | О чём |
|---|---|
| [EmailFast](https://github.com/Timmn3/EmailFast) | Коммерческий сервис приёма SMS и аренды e-mail. 10+ платёжек с идемпотентным зачислением, партнёрская программа, circuit breaker на проверке оплат, автоматический failover между серверами |
| [Avito Duff](https://github.com/Timmn3/Avito_Duff) | SaaS-мониторинг объявлений. FastAPI + React/TypeScript, метрики в Grafana, CI с тестовой БД, нагрузочные тесты Locust |
| [Call Masking Bot](https://github.com/Timmn3/call_masking_bot) | Заказная система маскированных звонков: amoCRM + Mango Office. Менеджер звонит клиенту, не видя его номера |
| [NanoBanana](https://github.com/Timmn3/nanobanana) | Платформа генерации изображений и видео нейросетями: Django + Celery, Telegram Web App под каждую модель, биллинг в токенах |
| [AI Telegram Bot](https://github.com/Timmn3/AI_telegram-bot-chatgpt-midjourney) | ChatGPT и Midjourney в Telegram: подписки с автопродлением картой, 6 способов оплаты, реферальная программа |
| [YouTube Telega](https://github.com/Timmn3/YouTube_Telega) | Скачивание видео в Telegram через локальный Bot API: файлы до 2 ГБ, нарезка больших роликов, очередь, переживающая рестарт |
| [ClaudeScheduler](https://github.com/Timmn3/ClaudeScheduler) | Автоматизация Claude.ai по расписанию через Chrome DevTools Protocol |
| [CityCatalog](https://github.com/Timmn3/CityCatalog) | Каталог организаций: FastAPI + React, SQLAlchemy, Alembic, Docker |

### Чем занимаюсь кроме кода

- **Эксплуатация.** Деплой через `git push` с post-receive хуками сразу на несколько серверов,
  supervisor и systemd, ротация логов, ночные дампы PostgreSQL со сторожевым процессом,
  который пишет в Telegram, если дамп не появился.
- **Разбор инцидентов.** Когда лёг сервер, обслуживавший почти всю выручку сервиса,
  перевёл проверку платежей на прямой Shop API провайдера и написал скрипт закрытия
  компенсированных платежей, чтобы никому не зачислить дважды.
- **Производительность.** Обход почтовых ящиков ускорен с 28 минут до 2 - линейный перебор
  заменён на сканирование по активности владельца.
- **Надёжность как привычка.** Circuit breaker, таймауты на весь проход задачи,
  идемпотентность зачислений, флаги в конфиге для рискованных механик, чтобы выключать
  фичу на бою без релиза.

### AI-инструменты

Работаю с Claude Code как с частью процесса: `CLAUDE.md` с правилами в каждом проекте,
собственные скиллы и субагенты под ревью и research, Conventional Commits.
Отдельный проект по автоматизации Claude.ai через CDP.

---

Почта: timmn@mail.ru
