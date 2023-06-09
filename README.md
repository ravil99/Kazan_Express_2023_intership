# Тестовое задание на стажировку DS Kazan Express 2023

## Описание задачи - https://remarkable-cockatoo-98b.notion.site/KazanExpress-d1c9915724544e1693afd0ca1b61a957

## Алгоритм решения:

1. После анализа и чистки датасета для предикта было решено использовать только `shop_id` и поле `title` из `text_fields`, так как они кажутся самыми значимыми для классификации по категории.

2. Генерация эмбеддингов из текста. Была использована SOTA русскоязычная сеть `RuBERT-2 tiny` от Сбера. Из 2 текстовых полей было получено 2 вектора размерность по 312.

3. Классификация через CatBoost. Для более точной оценки weighted F1 для модели была использована 5-Fold Cross Validation. Модели показали высокие метрики. Из 5 обученных моделей была выбрана одна (с лучшими метриками).

## Более детальное описание работы смотрите в MarkDown в самом ноутбуке.

Все необходимые пакеты в requirments.txt и в самой первой ячейке в ноутбуке.

## Результаты

Данное решение позволило мне получить приглашение на техническое собеседование. Всего было приглашено 22 человека из 76 кандидатов.
