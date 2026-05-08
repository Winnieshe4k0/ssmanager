# База · Свой Сап — Инструкция по деплою

## Проект: ssmanager-2f782

---

## Шаг 1 — Установить Firebase CLI (один раз)

```bash
npm install -g firebase-tools
firebase login
```

---

## Шаг 2 — Привязать проект

В папке с файлами приложения:

```bash
firebase use ssmanager-2f782
```

Если команда не найдёт проект:
```bash
firebase use --add
# Выбрать ssmanager-2f782 из списка
```

---

## Шаг 3 — Задеплоить

```bash
firebase deploy --only hosting,database
```

После деплоя приложение будет доступно по адресу:
**https://ssmanager-2f782.web.app**

---

## Добавить на экран телефона (PWA)

**Android (Chrome):** меню браузера → «Добавить на главный экран»

**iPhone (Safari):** кнопка «Поделиться» → «На экран "Домой"»

---

## Структура данных в Realtime Database

```
entries/
  2026-05-15/
    date: "2026-05-15"
    revenue: 25000
    guests: 18
    staff: 8000
    createdAt: 1747123200000
  2026-05-16/
    ...
```

*Ключ документа = дата (YYYY-MM-DD), что исключает дубли.*

---

## Обновление приложения

```bash
firebase deploy --only hosting
```
