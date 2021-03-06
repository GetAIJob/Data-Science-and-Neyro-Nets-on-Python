# Домашнее задание No2 июльский курс-2020 PRO

## LIGHT
Создайте модель для распознавания рукописных цифр из набора MNIST (можно воспользоваться ноутбуком 1-го занятия) и проведите ряд тестов:

1. Запустите сеть с различными размерами обучающей и проверочной выборок:

a. Обучающая выборка 50.000 примеров 

b. Обучающая выборка 10.000 примеров 

c. Обучающая выборка 500 примеров 

2. Создайте еще два варианта сети и сравните значения точности на проверочной выборке (на последней эпохе) и на тестовой выборке. 
Сделайте сравнительную таблицу. 

3. Создайте сеть следующей архитектуры:

a. 4 Dense слоя b. 3 Dropout слоя

c. 3 BatchNormalization слоя
Напишите свои выводы по результатам проведенных тестов.

## PRO
### Вариант 1
Повысьте точность модели по обнаружению мин до 90 % на тестовой выборке. Можно использовать различные варианты слоев Dropout и BatchNormalization. Можно менять количество примеров в обучающей и проверочной выборках, но нельзя менять количество примеров в тестовой.

### Вариант 2
По подготовленным на занятии данным создайте обучающую, тестовую и проверочную выборки. 
По сформированным данным необходимо обучить модель для предсказания цены машины. Оцените качество работы созданной сети, определив средний процент ошибки на проверочной выборке. (Для этого потребуется привести предсказанные моделью значения к первоначальному диапазону цен. 

Это можно сделать с помощью следующего метода:
predict_inverse = y_scaler.inverse_transfrom(predict).flatten() где predict - результат предсказания модели). Затем подсчитайте ошибку на каждом примере тестовой выборки и суммарный процент ошибки. 

Рекомендации:

● В качестве ошибки рекомендуется использовать среднеквадратическую ошибку (mse).

● Метрику для данной задачи можно не использовать.

● Последний слой модели должен иметь 1 нейрон.
