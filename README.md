# Отчёт о тестировании приложения BonusService

## Краткое описание

30.06.2020 - 30.06.2020 было проведено функциональное тестирование методом «белого ящика» приложения BonusService.

На тестирование затрачено: 2 часа

В результате тестирования выявлены следующие дефекты:
* [При запуске приложения ошибка Error: java: RV_RETURN_VALUE_IGNORED_NO_SIDE_EFFECT](https://github.com/Nick-kf/Java5_2_3_2/issues/1#issue-648893878)

## Описание процесса тестирования

**В процессе тестирования использовались следующие артефакты:**

**Набор тест кейсов:**

1. Скачать проект из архива [bonus-service.zip](https://github.com/netology-code/javaqa-homeworks/blob/master/maven-junit/artifacts/bonus-service.zip)

2. Открыть проект как Maven в IDEA.

3. В IDEA, в открывшемся проекте, дважды кликнув на Control, запустить следующую команду Maven*: mvn clean compile spotbugs:check

   **Ожидаемый результат:** Приложение запустится корректно

   **Фактический результат:** появляется ошибка RV_RETURN_VALUE_IGNORED_NO_SIDE_EFFECT

>  [INFO] --- spotbugs-maven-plugin:3.1.12.2:check (default-cli) @ bonus-calculator ---

>  [INFO] BugInstance size is 1

>  [INFO] Error size is 0

>  [INFO] Total bugs: 1

>  [ERROR] Return value of BonusService.calculate(long, boolean) ignored, but method has no side effect [Main] At Main.java:[line 8] RV_RETURN_VALUE_IGNORED_NO_SIDE_EFFECT

>  [INFO] 

>  To see bug detail using the Spotbugs GUI, use the following command "mvn spotbugs:gui"

 
![image](https://user-images.githubusercontent.com/66060000/86237324-3d8e7b80-bba4-11ea-9ea0-7c040d1eecac.png)

**Окружение:**

ОС: Windows 10 Pro 64-разрядная

Версия Java: "11.0.7" 2020-04-14

