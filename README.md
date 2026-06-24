# scrolltxt

![License](https://img.shields.io/badge/License-MIT-blue.svg)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)

<details>
<summary>🇬🇧 English</summary>

> **An endless feed of short articles in a card‑deck style.**  
> Scroll, discover new content, save to favorites. Minimalist, convenient, and no registration required.

## What This Project Is

`scrolltxt` is a single‑page web application that turns reading articles into an engaging card‑flipping experience. Each card contains a title, a brief summary, a category, and a source. It works like an endless feed (TikTok‑style interface) — but for text content.

The project is completely static — all data is loaded from a JSON file. Perfect for building a personal article collection, an educational digest, or just for quick content consumption.

## Features

- **Card feed** — smooth flip‑through animation (swipe / mouse wheel / keyboard).
- **Filtering** — search by title, content, or category; sort by category.
- **Favorites** — save articles to localStorage (persists between sessions).
- **Dark theme** — automatic toggle (saved in localStorage).
- **Zoom control** — increase/decrease font size for comfortable reading.
- **Responsive** — displays correctly on any device (from phones to desktops).
- **Hideable header** — for maximum content immersion.
- **Social & donation links** — built‑in footer with icons.

## Quick Start

1. **Download** all project files.
2. **Create** a `data.json` file with the article structure (see "Data Format" below).
3. **Open** `index.html` in any modern browser.
4. Enjoy!

*For development convenience, you can use `live-server` or any other local server.*

## Project Structure

```
scrolltxt/
├── index.html          # main page
├── scrolltxt.png       # logo (optional)
└── data.json           # article data file (created separately)
```

## Data Format (`data.json`)

The file must contain an object with the `ARTICLES` key, containing an array of article objects:

```json
{
  "ARTICLES": [
    {
      "id": 1,
      "title": "Deep Learning and Interpretability",
      "article": "Modern models... (brief text)",
      "section": "Machine Learning",
      "source": "Massachusetts Institute of Technology"
    },
    ...
  ]
}
```

**Fields:**
- `id` — unique number (integer).
- `title` — article title.
- `article` — brief summary (up to 300‑500 characters).
- `section` — category / rubric.
- `source` — source (university, journal, or organization).

## How It Works

- On page load, data is loaded from `data.json`.
- The category list is automatically built from the `section` field.
- Based on filters, a shuffled array of articles is created.
- Only three cards are displayed at a time: active (center), previous (top), and next (bottom).
- Navigation is done via mouse wheel, keyboard (up/down/left/right arrows), or touch swipe.
- The "Favorite" button adds/removes an article from localStorage.
- The "Favorites" filter shows only marked cards.

## Technical Details

- **Language**: Pure HTML, CSS, JavaScript (no external libraries).
- **Data**: JSON file loaded via `fetch`.
- **Animations**: CSS transitions with cubic‑bezier easing.
- **Storage**: `localStorage` for theme, header visibility, and favorites.
- **Responsiveness**: Media queries for all screen sizes.

## License

MIT — do whatever you want, just don't forget the author.

> *"Read fast, think deeper."*

</details>

<details>
<summary>🇷🇺 Русский</summary>
  
> **Бесконечная лента коротких статей в стиле карточной колоды.**  
> Прокручивай, открывай новое, сохраняй в избранное. Минимализм, удобство и никакой регистрации.

## О чём этот проект

`scrolltxt` — это одностраничное веб-приложение, которое превращает чтение статей в увлекательный процесс перелистывания карточек. Каждая карточка содержит заголовок, краткое содержание, категорию и источник. Всё работает как бесконечная лента (TikTok-подобный интерфейс), но для текстового контента.

Проект полностью статический — все данные подгружаются из JSON-файла. Идеально подходит для создания личной коллекции статей, образовательного дайджеста или просто для быстрого потребления контента.

## Возможности

- **Карточная лента** — плавная анимация перелистывания (свайп/колесо мыши/клавиатура).
- **Фильтрация** — поиск по названию, содержанию или категории, сортировка по категориям.
- **Избранное** — сохраняйте понравившиеся статьи в localStorage (сохраняются между сессиями).
- **Тёмная тема** — автоматическое переключение (сохраняется в localStorage).
- **Управление масштабом** — увеличивайте/уменьшайте шрифт для комфортного чтения.
- **Адаптивность** — корректно отображается на любых устройствах (от телефонов до десктопов).
- **Скрываемая шапка** — для максимального погружения в контент.
- **Ссылки на социальные сети и донаты** — встроенный футер с иконками.

## Быстрый старт

1. **Скачайте** все файлы проекта.
2. **Создайте** файл `data.json` со структурой статей (см. раздел «Формат данных» ниже).
3. **Откройте** `index.html` в любом современном браузере.
4. Наслаждайтесь!

*Для удобства разработки можно использовать `live-server` или любой другой локальный сервер.*

## Структура проекта

```
scrolltxt/
├── index.html          # главная страница
├── scrolltxt.png       # логотип (опционально)
└── data.json           # файл с данными статей (создаётся отдельно)
```

## Формат данных (`data.json`)

Файл должен содержать объект с ключом `ARTICLES`, содержащим массив объектов-статей:

```json
{
  "ARTICLES": [
    {
      "id": 1,
      "title": "Глубокое обучение и интерпретируемость",
      "article": "Современные модели... (краткий текст)",
      "section": "Машинное обучение",
      "source": "Массачусетский технологический институт"
    },
    ...
  ]
}
```

**Поля:**
- `id` — уникальный номер (целое число).
- `title` — заголовок статьи.
- `article` — краткое содержание (до 300-500 символов).
- `section` — категория/рубрика.
- `source` — источник (университет, журнал или организация).

## Как это работает

- При загрузке страницы данные загружаются из `data.json`.
- Список категорий автоматически формируется из поля `section`.
- На основе фильтров формируется перемешанный массив статей.
- Отображается только три карточки одновременно: активная (в центре), предыдущая (сверху) и следующая (снизу).
- Навигация происходит через колесо мыши, клавиатуру (стрелки вверх/вниз, влево/вправо) или сенсорный свайп.
- Кнопка «Избранное» добавляет/удаляет статью из localStorage.
- Фильтр «Избранное» показывает только отмеченные карточки.

## Технические детали

- **Язык**: Чистый HTML, CSS, JavaScript (без внешних библиотек).
- **Данные**: JSON-файл, подгружаемый через `fetch`.
- **Анимации**: CSS-переходы с кубическим безье.
- **Хранилище**: `localStorage` для темы, скрытия шапки и избранного.
- **Адаптивность**: Медиа-запросы для всех экранов.

## Лицензия

MIT — делайте что хотите, только не забывайте про автора.

> *«Читай быстро, думай глубже.»*

</details>
