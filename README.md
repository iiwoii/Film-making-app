# Создание фильмов на базе художественных произведений авторов


  1. Формулировка задачи: что вы делаете и зачем это нужно?
     
     Зачем нужно:
     Предложить авторам книг, обладающих авторскими правами на свои художественные произведения, инструмент для автоматизированного, персонализированного создания фильмов на основе их художественных произведений - "экранизация книг" с помощью технологий машинного обучения.

     Что делаем:
     Используем text-to-video models для генерации видео из текста с использованием различных технологий машинного обучения на языке программирования Python.

   
     Credits: https://byby.dev/ai-text-to-video-models

     
  2. Данные: откуда вы их собираетесь брать (конкретные ссылки), какие у них есть особенности, что может стать проблемой, почему этих данных достаточно для решения поставленной задачи?

     особенности: лицензирование, лимиты на использование - географического, иного плана; 
     проблема: платное или бесплатное использование; 
     достаточно ли данных: правило "10" означает, что количество исходных данных (т.е. количество примеров) должно быть в десять раз больше,чем количество степеней свободы модели. Под степенями свободы подразумеваются признаки в наборе данных. Данных со ссылкой на контекстное содержание записей 1 недели курса - достаточно. 
     
     1) https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset 
     2) https://developer.imdb.com/non-commercial-datasets/
     3) https://archive.ics.uci.edu/dataset/132/movie
     4) https://developer.themoviedb.org/docs/getting-started
     5) https://www.omdbapi.com/
     6) https://data.world/adrianmcmahon/imdb-dataset-all-indian-movies
     7) https://github.com/topics/movies-dataset
     8) https://paperswithcode.com/datasets?mod=videos&page=1
     9) https://paperswithcode.com/datasets?mod=audio
     10) https://paperswithcode.com/datasets?mod=texts&page=1
        
      
  3. Подход к моделированию: какие модели (имена нейросетей, библиотек) вы будете использовать в решении вашей задачи, какова будет конфигурация решения? Можно приложить схему.
     
     Имена нейросетей:
     
     a. OpenAI models - ChatGPT (если бесплатное решение) или другие OpenAI решения, content generation APIs, как Sora (в случае использования платных решений)
     
     b. ali-vilab/text-to-video-ms-1.7b
     
     c. возможно использования дополнительных к указанным или альтернативных аналогичных моделей.
     


     Библиотеки:
     
     a. mutagen, gTTS, PIL, moviepy, ESpeakng, Pyttsx3 и др.
     
     b. diffusers, transformers, accelerate, pytorch

     c. др. в зависимости от подзадач.

     

     Конфигурация решения (сочетание I,II,III существующих решений + авторский скрипт):
     
     I.) OpenAI API, ali-vilab models для использования возможностей готовых моделей - конвертация текста в аудио, текста в видео - создание скрипта.
     
     II.) Конвейер, который преобразует длинный текст в небольшие предложения, создающие несколько изображений, которые позже обрабатываются для создания видео с субтитрами и синтетическим голосом.
         Шаг 1 — Установка библиотек
         Шаг 2 — Импорт библиотек
         Шаг 3 — Создание приложения: использование текста для создания видео
         Шаг 4 — Создание субтитров
         Шаг 5 — Добавление субтитров к изображениям
         Шаг 6 — Создание видео
         Шаг 7 — Создание звука
         Шаг 8 — Объедините аудиофайлы
         Шаг 9 — Создание видеоролика с настроенным временем звука
         Шаг 10 — Объединить видео + аудио

    III.) 






    

     Credits: (https://medium.com/@ruslanmv/how-to-create-a-video-with-artificial-intelligence-from-a-text-1dd3ebd49a95)
     
     Credits: (https://medium.com/@kamaljp/text-to-video-pipeline-python-automation-using-open-ai-models-f4341555c8d9)
     
     Сredits: (https://huggingface.co/ali-vilab/text-to-video-ms-1.7b)
     
     Credits: (https://www.youtube.com/watch?v=Tlxe3l_m3PA)

     Credits: (https://www.leewayhertz.com/create-generative-video-model/)
 
  5. Способ предсказания: после обучения модели вам нужно будет обернуть модель в продакшен пайплайн - какие шаги в нём необходимы, как вы видите финальное применение? Схема также не будет лишней.

     Логика финального применения:
     
     1. использование возможностей готовых нейросетей.
     2. конвертация текста в аудио, текста в видео - создание скрипта
     3. создание скрипта для монтажа полной и короткой версии видео фильма.
     4. загрузка короткой версии фильма (shorts) в YouTube
     5. *Real-time означает синхронный процесс, при котором пользователь запрашивает прогноз, запрос передается на бэкэнд-сервис посредством вызовов HTTP API, а затем передается в ML-сервис.

     Этот способ подходит, если вам нужны персонализированные предсказания, учитывающие недавнюю контекстную информацию, что совпадает с вектором задач данного проекта.

     
     Credits: (https://habr.com/ru/articles/739316/)
![image](https://github.com/iiwoii/film_making/assets/121694433/56f9409a-9ba1-4f16-af82-52375593e871)


     
