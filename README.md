# Решение для хакатона HSE AI Assistant Hack: Python

## О проекте

Каждый из нас, наверняка, помнит типовые задачи по программированию: вывести отсортированный словарь всех стран, в написании которых есть буква "н", или найти все взаимно простые пары чисел в списке. 

Как часто мы обращались к товарищам за помощью, или часами изучали Stack Overflow, чтобы найти ответы на вопросы? Было бы здорово, если бы существовал цифровой ассистент, который мог бы помочь исправить ошибки в коде, но не выдавал готового решения! 

Проект создан в рамках хакатона **HSE AI Assistant Hack: Python**, организованного Высшей школой экономики.  
Целью было разработать Python-ассистента на основе LLM, который:
- Указывает на возможные ошибки в коде.
- Помогает пройти проваленные тесты.
- Устойчив к джейлбрейкам, сохраняя при этом обучающую роль.

---

## Устройство репозитория

- **`submit.py`** — скрипты подготовки сабмита.
- **`main.py`** — основной файл, обеспечивший итоговый скор 0.58 (перед запуском требуется добавить API-ключи Яндекса).

---

## Особенности проекта

В процессе разработки было протестировано множество подходов: 
1. **`p_tuning (3)`** — p-тюнинг.  
2. **`training_hse_bot_legenda_p_tuning`** — тестирование p-тюнинга и SFT локально в Google Colab на модели с 1B параметров.  
3. **`baseline_Danila_old`** — первичный анализ данных и SFT.  
4. **`validation_pipeline_for_hse_hack`** — использование EDA и цепочек рассуждений.  
5. **`dpo_preparations_for_12B`** — обучение с использованием DPO.  
6. **`desc_n_sol_60c`** — генерация синтетических данных и парсинг.  
7. **`llm_classifier`** — выделение классов из обучающего датасета для последующей классификации через LLM или обучения отдельного классификатора.

---
## Установка и запуск

Для воспроизведения решения выполните следующие шаги:

1. Установите все зависимости:
   ```bash
   pip install -r requirements.txt
   main.py
---

## Технологии

- ![Python](https://img.shields.io/badge/Python-3.x-blue) — основной язык программирования.
- ![Hugging Face](https://img.shields.io/badge/Hugging%20Face-yellow) — фреймворк для работы с LLM.
- ![PEFT](https://img.shields.io/badge/PEFT-green) — библиотека для эффективной дообучаемости больших моделей.

---

## Команда разработки

- **Малинин Данила** (БИВТ-23-10) — Машинное обучение  
- **Калинин Алексей** (БИВТ-23-10) — Машинное обучение  
- **Сергеев Даниил** (БИВТ-23-10) — Машинное обучение  
- **Трушков Глеб** (БИВТ-23-5) — Машинное обучение  
- **Колокольцев Ярослав** (БПИ-23-2) — Дизайнер  

---

## Почему этот проект важен?

Этот проект нацелен не на прямое решение задач за пользователя, а на предоставление полезных подсказок, направляющих его к правильному ответу. Отличительные особенности:
- **Обучающий подход**: вместо готовых решений ассистент помогает пользователю понять ошибку и исправить её самостоятельно.
- **Сопротивление джейлбрейкам**: ассистент устойчив к попыткам обойти систему и получить готовый код.
- **Универсальность**: ассистент применим как для начинающих разработчиков, так и для более опытных специалистов.

Проект улучшает образовательный процесс, делая его более интерактивным и направленным на развитие навыков программирования.

---

## Лицензия

Данный проект распространяется под лицензией [MIT](LICENSE). Вы можете использовать, изменять и распространять проект в соответствии с условиями лицензии.
