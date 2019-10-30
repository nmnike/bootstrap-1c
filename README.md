# Краткое описание проекта

Шаблон для быстрого создания проектов 1С.

## Требуемое программное окружение

* Git

## Состав проекта

```text
bootstrap-1c/
├── build/
├── doc/
├── examples/
├── features/
├── lib/
├── src/
├── test/
├── tools/
├── web/
├── .bsl-language-server.json
├── .gitlab-ci.yml
├── feature.bat
├── README.md
└── sonar-project.properties
```

### Расшифровка

#### Каталоги

`./build` - для хранения файловых баз данных, файлов хранилища конфигурации и т. д., используемых в процессе разработки и тестирования. Данные из этого каталога не выкладываются в удаленный репозиторий, поэтому должны быть добавлены в `.gitignore`;

`./doc` - для хранения файлов документации в формате Markdown. Содержит рекомендации разработчикам и команде проекта, описание релизов (RELEASE NOTES) и оперативного плана (ROADMAPS). **Не используется** для хранения пользовательских инструкций;

`./examples` - для хранения примеров кода c расширением bsl и хранения текстовых описаний на языках Gherkin и Markdown;

`./features` - для хранения feature-файлов на языке Gherkin (BDD);

`./lib` - для хранения внешних отчетов и обработок необходимых для работы продукта, разработанные в рамках создания продукта и не являющиеся сторонними разработками;

`./src` - для хранения исходного кода в текстовом формате. Для обычных форм файлы .bin должны быть распарсены до файлов модуля формы;

`./test` - для хранения тестов (TDD);

`./tools` - для хранения любых сторонних утилит, необходимых для настройки проекта или для дополнительной установки, например:

* allure
* oscript
* powershell
* wget
* ...

##### Windows

Для установки через командную строку в Windows используется http://chocolatey.org

##### Linux

В зависимости от установленной операционной системы - используется пакетные менеджеры `deb` или `yum`.

`./web` - для хранения настроек веб-серверов;

#### Файлы

`.bsl-language-server.json` - [конфигурационный файл с настройками LSP сервера](https://1c-syntax.github.io/bsl-language-server/#configuration);

`.gitignore` - для скрытия файлов и папок от системы контроля версий Git;

`.gitlab-ci.yml` - файл для настройки CI/CD сервера GitLab;

`feature.bat` - файл для запуска утилит, автоматизирующих процесс разработки (создание базы данных, хранилища конфигурации и т. д.);

`README.md` - файл с описанием проекта в формате Markdown. Предполагается, что сначала описание подготавливается в файле README.md (мастер), а затем импортируется в confluence через "Вставить разметку -  Вставить Confluence Wiki". Преобразовывать оформление можно через [конвертер разметки](http://chunpu.github.io/markdown2confluence/browser/). "Вставить разметку - Вставить Markdown" в Confluence 6.15.6 работает некорректно, ломая разметку. В более поздних версиях ситуация может измениться;

`sonar-project.properties` - файл с настройками SonarQube Scanner;
