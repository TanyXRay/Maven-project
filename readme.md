# Пример работы с программой Maven

##### В данном проекте показан пример создания многомодульного проекта с помощью сборщика Maven.
##### Стандартный многомодульный проект имеет составляющие по функционалу:
- db - модуль работы с базой данных;
- api - модуль работы с web;
- service - слой сервисов.

## Структура программы:
1) в родительский pom.xml добавлен  packaging:
   < packaging >pom< /packaging > (pom  означает, что данный модуль будет parent, т.е. родительским, и как следствие многомодульным);
2) созданы 3 папки (модули): db, api, service;
3) в каждой из этих директорий (модулей) создано по pom.xml, в котором отражена информация < artifactId >, < groupId >,  < version >  о parent-модуле и о текущем модуле, также указан  < packaging >jar< /packaging >;
4) в корне проекта в родительском pom.xml подключены child-модули: db, api, service;
5) после создания многомодульного проекта, подключаются связанные модули между собой с помощью внесения < dependencies >;
6) сборка проекта: в командной строке ввод: mvn clean install;
7) в child-модулях созданы классы, для демонстрации работы проекта;
##### В результате получен модульный проект с разделением по функциональности.

