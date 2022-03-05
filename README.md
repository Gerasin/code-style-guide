# Code style guide: Inetstudio [frontend]

## Среда разработки

### 1. Пакетный менеджер

- [yarn](https://classic.yarnpkg.com/en/docs/install) // Обязательно для проектов на Laravel, рекомендуется для новых проектов и старых, не имеющих сборки
- npm // если используется сейчас, допустимо продолжать использовать

### 2. Линтер

    EsLint

#### Настройка Eslint

1. [Установить eslint](https://eslint.org/docs/user-guide/getting-started)
2. для vue дополнительно поставить [eslint-plugin-vue](https://eslint.vuejs.org/user-guide/#installation)
3. Установить расширение для своей IDE

    - [VS Code расширение](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)

    - [PHP Storm расширение](https://www.jetbrains.com/help/phpstorm/eslint.html)

    - [Другие IDE и интеграции](https://eslint.org/docs/user-guide/integrations)
4. Скопировать конфиг `.eslint.js` в корень проекта
5. Добавить `.eslint.js` в `.gitignore` на период утверждения конфига. После утверждения будем держать его в гите.
6. Перезапустить IDE
7. Настроить секции конфига `.eslint.js`
    - секция `extends` (vue2/vue3)
    - секция `globals` (глобальные переменные сторонних библиотек, глобальных хранилищ и т.д.)

### 3. Сборщик/Бандлер

Выбирается с учетом нужд проекта и контекста.

- для модульного кода (es6+/vue):

  - [laravel-mix](https://laravel-mix.com/docs/6.0/what-is-mix)
  - [webpack](https://webpack.js.org/)
  - [vite](https://vitejs.dev/guide/)

- для легаси кода (non-module/es5):

  - [gulp](https://gulpjs.com/docs/en/getting-started/quick-start)
  - [grunt](https://gruntjs.com/getting-started)

Или любой другой по вашему выбору.

### 4. Минимальная документация

*! ОБЯЗАТЕЛЬНО ОПИСАНИЕ СБОРКИ, ОСНОВНЫХ КОМАНД, ЛОКАЦИИ ИСХОДНИКОВ В quick start guide:*

    // пример в текущем репозитории:

    README.FRONTEND.md

### 5. Политика перехода на новые версии библиотек и поддержка в актуальном состоянии

Не используем в продакшне beta-версии/версии под флагами и т.п.

Всегда стараемся использовать последнюю стабильную версию, если нет специфических ограничений (например, по какой-то из зависимостей еще нет обновления)

По актуальным поддерживаемым проектам проверяем наличие обновлений не реже, чем раз в 6 месяцев.
