# DuckLake вместо Apache Iceberg: Мощная альтернатива для Data Lakehouse

- ✉️ Вопросы, обучение, консультации по Data Engineering — пиши в
  личку: https://korsak0v.notion.site/Data-Engineer-185c62fdf79345eb9da9928356884ea0
- 💥 Аналог Notion (если не работает ссылка выше) — https://www.dataengineers.pro/mentors/korsakov-ivan

## О видео

🔥 Что такое DuckLake и почему релиз версии 1.0 — это прямой и очень дерзкий вызов привычному Apache Iceberg? В
этом [видео](https://youtu.be/XR9LATp53mY) мы разберем DuckLake с точки зрения современного архитектурного подхода к
Data LakeHouse. Поговорим про три эпохи развития дата-платформ: от классических монолитных СУБД (ClickHouse, PostgreSQL,
GreenPlum) и хаоса Data Lake до появления полноценных LakeHouse-форматов.

💡 Выясним, почему идея DuckLake хранить метакаталог в реляционной СУБД (PostgreSQL) — это гениальное решение, и пройдем
полный путь от быстрого старта до продвинутой решения. А в конце видео вас ждут рекомендации по работе с DuckLake
(Parquet V2, сжатие Zstd, многопоточный инжест и пр).

🗂️ GitHub репозиторий с кодом: https://github.com/k0rsakov/pet_project_what_is_ducklake

✉️ Вопросы, обучение, консультации по Data Engineering — пиши в
личку: https://korsak0v.notion.site/Data-Engineer-185c62fdf79345eb9da9928356884ea0

💥 Аналог Notion (если не работает ссылка выше) — https://www.dataengineers.pro/mentors/korsakov-ivan

Мои соцсети и полезные ссылки:

- Mentorship/консультации по Data
  Engineering — https://korsak0v.notion.site/Data-Engineer-185c62fdf79345eb9da9928356884ea0
- TG-канал — https://t.me/DataLikeQWERTY
- Instagram — https://www.instagram.com/i__korsakov/
- Habr — https://habr.com/ru/users/k0rsakov/publications/articles/
- Видео про DuckDB — https://youtu.be/9L63L__fX0k
- Видео про алгоритмы сжатия данных — https://youtu.be/rYpZNKYPSAU

Таймкоды:

- 00:00 — Начало
- 00:18 — Классические монолитные базы данных
- 01:01 — Data Lake и эпоха хаоса
- 02:30 — Data Lakehouse
- 05:19 — Практика, разбор проекта
- 06:37 — Локальный DuckLake
- 10:43 — Уборка/гигиена в DuckLake
- 11:59 — Schema evolution в DuckLake
- 13:02 — Time travel в DuckLake
- 14:46 — Production DuckLake (PostgreSQL + MinIO)
- 18:29 — Изучение каталога DuckLake
- 19:16 — Рекомендации
- 19:42 — Умная работа со снапшотами и TTL
- 20:24 — Killer-фича, регистрация внешних файлов
- 20:53 — Простота из коробки и "экосистема"
- 21:21 — Переход на Parquet v2
- 21:42 — Сжатие алгоритмом ZSTD
- 22:08 — Многопоточная запись
- 22:29 — Агрессивный retry wait time
- 23:01 — Заключение

#ducklake #duckdb #datalakehouse #apacheiceberg #dataengineering #postgresql #s3 #parquet #bigdata #dataengineer
#analytics #sql #lakehouse #minio #etl

## О проекте

Запуск виртуального окружения для работы:

```bash
uv sync
```

Запуск `jupyter lab`:

```bash
uv run jupyter lab
```
