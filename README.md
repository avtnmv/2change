# 2Change - Проект с подключенными шрифтами FuturaPT

## Подключенные шрифты

В проекте успешно подключены шрифты семейства FuturaPT из папки `font/`:

### Основные веса шрифтов:

- **FuturaPT-Book** - вес 400 (normal) - для основного текста
- **FuturaPT-Medium** - вес 500 (medium) - для заголовков и акцентов
- **FuturaPT-Bold** - вес 700 (bold) - для важных элементов

### Дополнительные веса (доступны в CSS):

- **FuturaPT-Light** - вес 300 (light)
- **FuturaPT-ExtraBold** - вес 800 (extra bold)
- **FuturaPT-Heavy** - вес 900 (heavy)

## Структура файлов

```
/font/
├── FuturaPT-Book.woff2      # Основной текст (400)
├── FuturaPT-Medium.woff2    # Заголовки (500)
├── FuturaPT-Bold.woff2      # Важные элементы (700)
├── futurapt.css             # CSS с подключением шрифтов
└── ...                      # Другие форматы и веса

/index.html                  # Основная страница с подключенными шрифтами
/font-test.html              # Тестовая страница для проверки шрифтов
```

## Как использовать

### 1. В HTML (уже подключено):

```html
<!-- Шрифты автоматически подключаются через CSS -->
<link rel="stylesheet" href="/font/futurapt.css" type="text/css" media="all"/>
```

### 2. В CSS:

```css
/* Основной текст */
body {
    font-family: 'FuturaPT', Arial, sans-serif;
    font-weight: 400; /* normal */
}

/* Заголовки */
h1, h2, h3 {
    font-family: 'FuturaPT', Arial, sans-serif;
    font-weight: 500; /* medium */
}

/* Важные элементы */
.btn, .nav-brand {
    font-family: 'FuturaPT', Arial, sans-serif;
    font-weight: 700; /* bold */
}
```

### 3. Utility классы (доступны в futurapt.css):

```css
.font-normal    { font-weight: 400; }
.font-medium    { font-weight: 500; }
.font-bold      { font-weight: 700; }
.font-light     { font-weight: 300; }
.font-extrabold { font-weight: 800; }
.font-heavy     { font-weight: 900; }
```

## Тестирование

Для проверки работы шрифтов откройте `font-test.html` в браузере. Эта страница демонстрирует все доступные веса и стили шрифтов FuturaPT.

## Особенности

- **font-display: swap** - шрифты загружаются с оптимизацией для производительности
- **Preload** - основные шрифты предзагружаются для быстрого отображения
- **Fallback** - используются системные шрифты как резервные
- **Responsive** - адаптивная типографика для мобильных устройств

## Поддержка браузеров

- ✅ Chrome 36+
- ✅ Firefox 39+
- ✅ Safari 10+
- ✅ Edge 12+
- ✅ IE 9+ (с fallback на TTF)

## Форматы файлов

Каждый шрифт доступен в нескольких форматах:
- **WOFF2** - современный, сжатый формат (рекомендуется)
- **WOFF** - широко поддерживаемый формат
- **TTF** - универсальный формат для fallback
- **EOT** - для старых версий IE

## Производительность

- Шрифты оптимизированы для веба
- Используется `font-display: swap` для быстрого отображения
- Preload для критических шрифтов
- Автоматический fallback на системные шрифты
