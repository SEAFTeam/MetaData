# metadata
Расширение ИА seaf-core для храненияи и визуализации метаданных

Описание представлений читайте в разделе меню "Документы/Мета данные"
[Документы/Мета данные](/docs/seaf.md.description)

## metadata_discovery
Инструмент для сбора технических метаданных и проксирования слоев ИА

[https://github.com/medmikhr/MetaData_discovery](https://github.com/medmikhr/MetaData_discovery)

## Инструкция по использованию расширения metadata:

1. Скачиваем репозиторий
https://github.com/SEAFTeam/seaf-dzo-example

    *1.1 Опциональный шаг*

    Удаляем файлы примеров из папки architecture/ia.

    Переносим в нее файлы, полученные в результате работы MetaData_discovery

2. В корне проекта создаем папку _metamodel_ и скачиваем в нее репозитории:

https://github.com/SEAFTeam/seaf-core

https://github.com/medmikhr/metadata

3. В корне папке _metamodel_ создаем packages.yaml и заполняем, для подключения скачанных репозиториев

imports:
 - seaf-core/dochub.yaml
 - metadata/root.yaml

Финальная структура проекта:

SEAF-DZO-EXAMPLE

| _metamodel_ - Пакеты расширений

| |- metadata - Расширение для хранения и визуализации метаданных

| |- seaf-core - Sber Enterprise Architecture Framework (SEAF)

|- architecture - Пример описания архитектуры

| |- interface - Конфигурация пользовательского интерфейса

|- docs - Документация по пакетам

|- dochub.yaml - Корневой манифест

|- README.md - Описание репозитория