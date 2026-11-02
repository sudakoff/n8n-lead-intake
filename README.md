# Приём заявки: Telegram и LLM

Короткий шаблон n8n, не клиентский проект.

Человек пишет боту заявку свободным текстом. Узел с моделью возвращает JSON `{name, phone, request}`. Дальше POST на ваш webhook (CRM, таблица, другой сценарий) и короткий ответ в Telegram.

Файл: [`workflows/lead-intake.json`](workflows/lead-intake.json)

## Что подставить

- `YOUR_OPENAI_API_KEY` в узле «Разобрать заявку»
- `https://example.com/hooks/YOUR_INTAKE_WEBHOOK` — адрес вашей CRM или второго сценария
- credentials Telegram на триггере и на узле ответа

`/start` не уходит в модель: бот просит прислать имя, телефон и суть одним сообщением.
