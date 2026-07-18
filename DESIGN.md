# Design

Единый файл: `index.html` (все стили инлайн в `<style>`), статика на GitHub Pages, домен beyondbeautyconcierge.ru.

## Color

- Ivory фон секций: `#f7f1ea` / `#fdfaf6` (чередование)
- Тёмные секции: `#241c15` (steps), body-подложка `#171009` с radial-градиентом
- Ink (текст): `#2a221c`; вторичный `#6e6258` / `#4a4038`
- Бронза (акцент): `#b8895a`, светлая `#cda478`, тёмная `#8a5f33`, линии `#c8a982`
- Светлый текст на тёмном: `#fdf8f2` / `#f0e6da`; акцент на тёмном `#f0d8be`

Стратегия — committed warm premium: identity зафиксирована и одобрена Сергеем, не менять (identity-preservation).

## Typography

- Заголовки: Cormorant Garamond 600 (serif). h1 hero: 46px mob / 62px desk; h2: 34/46px.
- Текст/UI: Manrope 400–700. Body 14.5–16.5px.
- Kicker-система: 11.5px uppercase letter-spacing 3px, цвет `#8a5f33` (осознанная бренд-система на каждой секции).

## Components

- `.btn.gold` — золотой градиентный pill CTA (главный), `.btn.dark` — тёмный pill.
- `.fcard` — строки решения с римскими цифрами; `.step` — шаги с крупными цифрами.
- `.chatcard` — тёмная карточка «как выглядит разбор» (имитация чата бота).
- `.case` — кейс: фото (в фас!) + разбор по зонам + «корень» + locked-блок Premium; на мобиле хвост сворачивается (checkbox-hack `.cmore-toggle`).
- `.pcard` — тарифная карточка; `.anchor` — ценовой якорь (филлер/пластика); `.guarantee` — гарантия.
- `.sticky-cta` — мобильная липкая CTA-полоса (появляется после hero, IntersectionObserver).

## Layout

- Мобиле-колонка max-width 600px; desktop ≥860px: wrap 1120px, двухколоночные списки, кейсы в строку (фото 38%).
- Breakpoint единственный: 860px.

## Motion

- Reveal `.rv` (translateY 18px + fade) через IntersectionObserver, только при `prefers-reduced-motion: no-preference`. Контент видим по умолчанию (reveal — прогрессивное улучшение).

## Rules

- Каждый CTA → `https://t.me/BeyondBeautyConcierge_bot?start=site`.
- Фото кейсов: красивые лица с ЕДВА заметными проблемами, строго в фас (правило Сергея).
- Слайдовый рендер соцконтента использует эту же палитру (см. проект bb-карусели-10).
