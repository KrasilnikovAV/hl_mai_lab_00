# Контекст решения
<!-- Окружение системы (роли, участники, внешние системы) и связи системы с ним. Диаграмма контекста C4 и текстовое описание. 
-->
```plantuml
@startuml
!include https://raw.githubusercontent.com/plantuml-stdlib/C4-PlantUML/master/C4_Container.puml

Person(admin, "Администратор")
Person(moderator, "Модератор")
Person(user, "Пользователь")

System(conference_site, "Сайт поиска попутчиков", "Веб-сайт для поиска попутчиков")



Rel(admin, conference_site, "Просмотр и редактирование информации о пользователях и поездках")
Rel(moderator, conference_site, "Модерация поездок и пользователей")
Rel(user, conference_site, "Регистрация, просмотр/изменение информации о поездках")



@enduml
```
## Назначение систем
|Система| Описание|
|-------|---------|
| Сайт поиска попутчиков | Веб-интерфейс, обеспечивающий доступ к созданию и просмотру информации о поездках. Бэкенд сервиса реализован в виде микросервисной архитектуры |

