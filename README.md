# Polska Vault (Quartz)

Obsidian нотатки про польську мову, опубліковані за допомогою [Quartz 4](https://quartz.jzhao.xyz/). Жодних ручних меню чи `mkdocs.yml`: достатньо додавати/редагувати Markdown-файли, а Quartz будує навігацію автоматично.

## Структура

- `content/` — усі нотатки. Додавайте сюди будь-які `.md` файли; Quartz підійме їх автоматично.
- `quartz/`, `quartz.config.ts`, `quartz.layout.ts` — рушій та налаштування теми.
- `.github/workflows/deploy.yml` — GitHub Actions, що збирає і деплоїть сайт на Pages з гілки `main`.

## Локальний запуск

```bash
npm install         # один раз
npm run dev         # будує сайт і піднімає локальний сервер
```

Після цього сайт доступний за адресою `http://localhost:8080/` з автоматичним перезавантаженням.

## Публікація на GitHub Pages

1. Запуште репозиторій у GitHub (наприклад, `artu/Polska`).
2. У налаштуваннях репозиторію відкрийте **Pages** й переконайтеся, що джерело — **GitHub Actions**.
3. Кожен `git push` у `main` запустить workflow `.github/workflows/deploy.yml`, який:
   - виконає `npm ci`,
   - збере сайт `npm run build` (вивід у `public/`),
   - опублікує артефакт через `actions/deploy-pages`.

Якщо публікуєте в іншому репозиторії, відредагуйте `homepage`/`repository` у `package.json` та `baseUrl` у `quartz.config.ts` (зараз задано `artu.github.io/Polska`).

## Додавання нових нотаток

1. Створіть файл у `content/` (наприклад, `content/słownictwo.md`).
2. Користуйтеся Obsidian-стилем посилань `[[назва]]` — Quartz їх розпізнає.
3. Закомітьте зміни та виконайте `git push`.

Quartz сам оновить навігацію, список останніх нотаток, граф зв’язків та пошук без додаткових конфігів.

