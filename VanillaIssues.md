# Дополнительная информация о данном VanillaIssues.md
- Здесь будут опубликованы дополнительные письменные/видео материалы, чтобы не засорять основной README.md


- Данная статья рассчитана на настройку под Ubuntu / Debian. Основные рекомендации также могут быть применены для ARM
  систем. Однако, если у вас Arch Linux или другие Unix системы - пожалуйста ознакомьтесь с документацией по установке
  пакетов на эту ОС или поищите альтернативные пакеты.


- < NOTICE > Для AUR репозиториев настоятельно рекомендуется проверять исходники скрипта установки. В любом случае это
  рекомендуется делать и для других репозиториев.


- < NOTICE > Некоторые функции могут работать неправильно или вовсе не работать на вашей системе.

# Почему ванильные сервера испытывают трудности?

- Основными причинами потери тиков являются мобы / сущности и, в относительно редких случаях, тикающие фрагменты мира.
- Конечно, патч с новой системой света/чанков от SpottedLeaf был опубликован в новых версиях Paper, но это не означает, что ваш сервер теперь никогда не будет лагать из-за прогрузки/загрузки фрагментов игрового мира.
- Новые фрагменты - наиболее сложны для обработки сервером. Представьте, что 50 игроков вашего сервера загружают новые блоки + мобы и сущности загружают ваш сервер.
### Принцип нагрузки MSPT
- Ваш MSPT (миллисекунды на тик) составляет ~ 25-35 из-за количества мобов и сущностей, затем при загрузке новых блоков это может увеличить ваш средний MSPT, например, с 35 до 45-55 или даже до 60-75 на короткое время, а затем вернуться снова.

# Что же делать с энтити/мобами и другими тикающими однопоточными объектами?

- К сожалению, в настоящее время не существует общедоступного стабильного способа перевести всех мобов в многопоточный режим процессора. Конечно, есть разработки от разных разработчиков, но они могут вызвать массу проблем, которые вы, возможно, не исправите в конфигурации или таким образом повредите файлы вашего мира, поэтому они всегда помечаются авторами как:
- < ! > Доступна новая разработка от PaperMC -> __[Folia](https://github.com/PaperMC/Folia)__


- Under Heavy Development / Not recommended for production / Heavy Alpha / PreAlpha / Unstable и т.д
