# crater_analysis
Hypothesis testing, crater analysis,  visualizations. 

### Задачи проекта: #

>1. Проверить, отличается ли время прохождения различных этапов для пользователей, которые прошли обучение, от пользователей, не начинавших обучение. 
---
>2. Посмотреть, существует ли зависимость между вероятностью оплаты вопросов и количеством обучений, которые начинал или завершал пользователь. 
---
>3. Выяснить как часто пользователи начинают обучение после того, как они выбрали уровень сложности.

### Целью проекта является проверка следующих гипотез: #

> 1. **"По идее, должна быть разница в поведении групп, которые проходят и не проходят обучение. Но так ли это? Влияет ли обучение на скорость прохождения других этапов игры?"** Это мы должны проверить в рамках 1 задачи.
---

> 2. **"Кажется, повторное прохождение обучения положительно влияет на оплату, верно?"** Это мы должны узнать в рамках 2 задачи. 
---

> 3. **"Если пользователь сначала выбирает сложность обучения, будет ли он потом проходить обучение?"** Нам нужно понять, насколько прозрачен процесс взаимодействия с игрой: если пользователи после выбора уровня сложности обращаются к обучению, значит, работа с приложением непонятна. Это мы должны проверить в рамках 3 задачи.
---
### Описание данных #
 Проектный анализ будет проводиться на данных игры ***QUIZ FREEZE*** 
 
 Анализ будет выполняться на основе данных пользователей, которые зарегистрировались в ***2018 году***. 
## Этапы из которых состоит игра: ##
---

  * **Регистрация** (registration) 

  * **Старт обучения** (tutorial_start)

  * **Завершение обучения** (tutorial_finish) 

  * **Выбор уровня сложности вопросов** (level_choice)
  * **Выбор пакетов вопросов** (pack_choice, или training_choice) 

  * **Покупка платных пакетов вопросов** (хранятся в таблице purchase)

    ## Используемые датасеты: 
---
***Таблица Event***

| Название поля      | Описание                | 
| :------------- |:------------------|
| id    |идентификатор события | 
| user_id    | уникальный идентификатор пользователя, совершившего событие в приложении |  
| start_time  | дата и время события| 
| event_type  | тип события (значения: registration — регистрация; tutorial_start — начало обучения; tutorial_finish — завершение обучения; level_choice — выбор уровня сложности; pack_choice — выбор пакетов вопросов)|
| tutorial_id | идентификатор обучения (этот идентификатор есть только у событий обучения)|
| selected_level | выбранный уровень сложности обучения | 

---
***Таблица Purchase***

| Название поля      | Описание                | 
| :------------- |:------------------|
| id | идентификатор события |
| user_id | уникальный идентификатор пользователя, совершившего событие в приложении |
| event_datetime | дата и время события/покупки |
| amount | сумма оплаты |

