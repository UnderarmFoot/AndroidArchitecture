# task1 - Спроектировать схему многомодульного приложения **«Чат»**.

## Модули приложения

### `:app`
Точка входа в приложение. Собирает все feature-модули и содержит основной граф навигации.

### Feature-модули

- `:feature:user_list` — экран списка пользователей.
- `:feature:chat` — экран чата с пользователем.
- `:feature:profile` — экран профиля пользователя.
- `:feature:settings` — экран настроек приложения.
- `:feature:auth` — авторизация пользователя.
- `:feature:registration` — регистрация нового пользователя.

### Core-модули

- `:core:model` — общие модели данных, используемые разными модулями.
- `:core:network` — работа с REST API и сетевыми запросами.
- `:core:ui` — общие UI-компоненты, темы и ресурсы интерфейса.
- `:core:navigation` — общие маршруты и контракты навигации между фичами.


# task2 - Спроектировать схему взаимодействия между слоями Clean Architecture для приложения **«Чат»** с использованием **MVVM**.

## Реализация

Для фич `user_list` и `chat` выделены слои:

- `Data` — работа с REST API, DTO, RepositoryImpl и Mapper.
- `Domain` — Entity, Repository interface и UseCase.
- `Presentation` — ViewModel, UI-модели, Mapper и Compose Screen.

# task3 - Переписать предыдущую архитектуру приложения **«Чат»** с использованием **MVP** и **MVI**.

## MVP

- `Data` и `Domain` остаются без изменений.
- `Presentation` содержит `Screen`, `View interface`, `Presenter`, UI-модели и Mapper.

## MVI

- `Data` и `Domain` остаются без изменений.
- `Presentation` содержит `Screen`, `ViewModel`, `Intent`, `State`, UI-модели и Mapper.
