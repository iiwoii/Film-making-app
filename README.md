# Создание фильмов на базе художественных произведений авторов
  1. Формулировка задачи: что вы делаете и зачем это нужно?
     
     Предложить авторам книг, обладающих авторскими правами на свои художественные произведения, инструмент для автоматизированного, персонализированного создания фильмов на основе их художественных произведений - "экранизация книг" с помощью технологий машинного обучения.





     ** AI models learn to generate video from text by using various techniques such as deep learning, recurrent neural networks, transformers, diffusion models, and GANs. These techniques help the models to understand the context and semantics of the text input and 
        generate corresponding video frames that are realistic and coherent.

        Some of the common features of text-to-video AI models are:

        They can generate videos from text descriptions only, or from text and image inputs.
        They can generate videos in various artistic styles, moods, with 3D object understanding.
        They can generate videos that are short (a few seconds) or long (several minutes).
        They can perform instruction-guided video editing, such background or subject of a video.
        They can use publicly available datasets or fine-tune on specific datasets.
        They can be accessed through various platforms, such as Hugging Face, RunwayML, NightCafe, and others.

        Credits: https://byby.dev/ai-text-to-video-models

     
  3. Данные: откуда вы их собираетесь брать (конкретные ссылки), какие у них есть особенности, что может стать проблемой, почему этих данных достаточно для решения поставленной задачи?

     особенности: лицензирование, лимиты на использование - географического, иного плана; 
     проблема: платное или бесплатное использование; 
     достаточно ли данных: правило "10" означает, что количество исходных данных (т.е. количество примеров) должно быть в десять раз больше,чем количество степеней свободы модели. Под степенями свободы подразумеваются признаки в наборе данных. Чтобы ответить на данный вопрос необходимо дополнительное время.
     
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
        
      
  4. Подход к моделированию: какие модели (имена нейросетей, библиотек) вы будете использовать в решении вашей задачи, какова будет конфигурация решения? Можно приложить схему.
     
     Имена нейросетей: Sora, NUWA
     
     Библиотеки: NumPy,SciPy,OpenCV,NLTK,Gensim,Scikit–learn

     Предварительная схема:


     ![image](https://github.com/iiwoii/film_making/assets/121694433/4d2a8dd1-de04-4cb8-a72c-d0e82c75addf)

     ![image](https://github.com/iiwoii/film_making/assets/121694433/a02fbbd9-1fcd-4c39-a583-1a3ee6286bb1)


  ![image](https://github.com/iiwoii/film_making/assets/121694433/9ccb5888-0ef0-4d5d-b644-9d430b325705)

    Credits: https://medium.com/@FrankAdams7/step-by-step-breakdown-of-real-time-ml-operational-deployment-pipeline-848f290eb5d9
    Credits: https://bigdataschool.ru/blog/techstack-template-for-mlops-tools.html
 
  5. Способ предсказания: после обучения модели вам нужно будет обернуть модель в продакшен пайплайн - какие шаги в нём необходимы, как вы видите финальное применение? Схема также не будет лишней.
