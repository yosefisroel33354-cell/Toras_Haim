# Ешива «Торат Хаим» (ישיבת תורת חיים) — Next.js Digital Rebirth

Модульная архитектура новой версии официального сайта **https://eshiva.ru/**.

## Особенности архитектуры
1. **Отделение контента от представления (`src/data/`)**:
   - `src/data/rabbis.ts` — дословные биографии, роли и оригинальные фотографии раввинов со страницы `https://eshiva.ru/rabbies`.
   - `src/data/photoArchive.ts` — структура 13 томов исторического фотоархива (`https://eshiva.ru/photo`, `vol1`–`vol13`) с возможностью добавления новых частей и фотографий без изменения React-компонентов.
   - `src/data/alumni.ts` — хроника встреч выпускников в Иерусалиме (`bogrim_2022`, `bogrim_2023`) и 17 полей анкеты выпускника (`registration`).
2. **SEO, Sitemap, Robots и безопасность (`src/app/`)**:
   - `src/app/layout.tsx` — Open Graph, метаданные, шрифты Cormorant Garamond, Inter и Frank Ruhl Libre (`dir="rtl"` для иврита).
   - `src/app/sitemap.ts` и `src/app/robots.ts` — автоматическая генерация карты сайта и правил индексации.
3. **Дизайн-система Apple Liquid Glass**:
   - Поддержка тёмной (`Midnight Navy` + `Obsidian Black` + `Champagne Gold`) и светлой академической (`Warm Ivory` + `Deep Graphite`) тем.
