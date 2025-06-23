# **Дипломный проект по профессии «Инженер по тестированию»**

Тестовая документация
[План](https://github.com/GorElena/Diploma-Project/blob/main/Documentation/Plan.md) по проверке и автоматизации приложения (`Documentation/Plan.m`)

[Чек-лист](https://github.com/GorElena/Diploma-Project/blob/main/Documentation/Check.xlsx) c отметками о пройденных и не пройденных тестах (`Documentation/Check.xlsx`).

[Тест-кейсы](https://github.com/GorElena/Diploma-Project/blob/main/Documentation/Cases.xlsx) для проверки приложения (`Documentation/Cases.xlsx`).

[Баг-репорты](https://github.com/GorElena/Diploma-Project/issues) оформленные как (`issues`).

[Allure-отчет](https://github.com/GorElena/Diploma-Project/blob/main/Documentation/allure-results.zip) с результатами прогона авто-тестов, а так же запакованный в (`allure-results.zip`).

[Отчет о тестировании](https://github.com/GorElena/Diploma-Project/blob/main/Documentation/Result.md) со сравнением ручного и автоматизированного тестирования, затраченного времени, найденные проблемы (`Result.md`).



# **Запуск авто-тестов и создание Allure-отчёта в Android Studio**
**1. Условия для запуска авто-тестов**
**Java JDK 11:** Убедитесь, что у вас установлена Java Development Kit версии 11.
**Android Studio:** Убедитесь, что у вас установлена последняя версия Android Studio с настроенной файловой средой:
1. Добавлен путь до JAVA_HOME в переменные окружения.
2. Настроена переменная ANDROID_HOME, указан путь до SDK Android.
3. Эмулятор Android: Убедитесь, что у вас установлен и настроен эмулятор Android с версией API 29.

**2. Клонирование и настройка проекта**

  1.Склонируйте репозиторий проекта:

   ```
    git clone https://github.com/GorElena/Diploma-Project.git

   ```
 2. Откройте проект в Android Studio.
 3. Подождите, пока завершится индексация и синхронизация проекта с Gradle.
**3. Запуск авто-тестов**
 1. В верхней части окна Android Studio, непосредственно над каталогом проекта, выберите вкладку `«Project».`
 2. Разверните структуру проекта и перейдите в директорию `app/src/androidTest/java/ru.iteco.fmhandroid.ui/test.`
 3. Правой кнопкой мыши кликните на папку test и выберите опцию `«Run 'Tests in iteco.fmhandroid.ui'»`, чтобы запустить все тесты данного пакета.
 _Начнется процесс сборки и запуска тестов._
 _Прогресс выполнения будет отображаться в окне «Run»._

**4. Формирование Allure-отчёта**

 Установите [Allure](https://allurereport.org/docs/install/) на вашем ПК
 
**5. Экспорт результатов тестов**
После завершения тестов откройте окно Device Explorer в Android Studio (Это можно сделать через поисковик 🔍).
Перейдите в директорию `/data/data/ru.iteco.fmhandroid.ui/files/allure-results`.
Щёлкните правой кнопкой мыши на папке `files` и выберите опцию `Save As`....
Сохраните папку `allure-result` в корневую директорию вашего проекта.
Если вам нужно сохранить папку `allure-result` в какую-то подпапку внутри вашего проекта, сначала необходимо перейти в эту подпапку, а затем выполнить команду для запуска.

**6. Генерация отчёта**
Перейдите в терминал и убедитесь, что находитесь в корневой директории проекта.
Выполните необходимую вам команду:

  
  
  для быстрого анализа результатов тестирования
    запускает временный веб-сервер, который динамически генерирует и показывает отчет на основе JSON-данных:
 ```
  allure serve
 ```

 для генерации HTML-отчёта:
  
 ```
  allure generate allure-results -o allure-report
 ```

 открывает сгенерированный HTML-отчёт в браузере:
    
```  
 allure open allure-report
```

