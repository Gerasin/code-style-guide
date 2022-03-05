
# SKIN MAKEUP GENERAL README

    VSCODE:
    Просмотр превью файла: ⇧⌘V
    Просмотр side-by-side: ⌘K V

## Этот репозиторий содержит сабмодуль git

В сабмодуле лежат общие файлы для обоих проектов.

После клонирования репозитория запустить команду

    git submodule update --init --recursive

## Файловая структура

все исходники лежат в

    resources/assets/front

кроме:
топ-баннеров и картинок слайдера главной страницы

    public/packages/promo - папка для баннеров
    public/packages/mainpage - папка для слайдера на главной (мейкап)

общие код для обоих проектов:

    resources/assets/front/pcore

## Сборка

Если используется docker, команды выполнять так (удобно положить в алиас):

    docker-compose run --rm node [your npm/yarn command]

При первом запуске проекта установить все зависимости

    yarn install

- Legacy

    Конфиг сборки

        Gruntfile.js

    билд для прода

        grunt build

    Следить за изменениями

        grunt watch

    Скопировать картинки/шрифты в паблик

        grunt copy

    Сгенерировать картинки для слайдера главной страницы на мейкапе

        grunt responsive

- Modern

    Конфиг сборки

        resources/assets/front/webpack.mix.js

    билд для прода

        npm run front-prod

    Следить за изменениями

        npm run front-watch

    Dev сборка

        npm run front-dev

## Список readme по отдельным модулям

- [Формы заявок](./REQUESTS_FORMS.md#requests-forms)
