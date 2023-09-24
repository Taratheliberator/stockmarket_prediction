# Прогнозирование цен на акции Сбербанка
Конечно изучая Data Science хочется применять знания для своих прикладных задач. То же самое я делал, когда работал нефтянником создал приложение для своих целей и сайт тоже для себя. Извечный вопрос трейдеров куда двинется цена? 

## Описание
Данный проект содержит Jupyter Notebook, разработанный для анализа и прогнозирования цен закрытия акций Сбербанка на основе исторических данных.

## Этапы работы
### Подготовка данных:

#### Загрузка данных:
 Исходные данные загружены из файла Прошлые данные - SBER.csv. Эти данные содержат информацию о дате, цене закрытия, цене открытия, максимальной и минимальной цене за день, объеме торгов и процентном изменении по сравнению с предыдущим днем.
#### Предобработка: 
Для удобства дальнейшего анализа даты были преобразованы в соответствующий формат. Цены и другие столбцы также были преобразованы в числовой формат.

#### Визуализация: 
График цен закрытия акций позволяет визуально оценить динамику цен и увидеть возможные тренды и сезонность. Это также может служить проверкой качества данных.

### Моделирование:

#### Модель случайного леса: 
Этот ансамблевый метод использует множество деревьев решений для прогнозирования. Основное преимущество этой модели - устойчивость к переобучению и возможность оценки важности признаков. На тестовой выборке модель показала среднеквадратичную ошибку около 18.90, что говорит о довольно хорошем качестве прогноза.
#### Модель градиентного бустинга: 
Еще один ансамблевый метод, который строит последовательность деревьев, где каждое следующее дерево пытается исправить ошибки предыдущего. Несмотря на то что этот метод часто показывает высокую производительность, в данном проекте его результаты были менее точными по сравнению со случайным лесом, с MSE около 43.19.
### Прогнозирование на будущее:

Обе модели были использованы для прогнозирования цен на следующие 5 дней. Эти прогнозы основаны на последних доступных данных и учитывают отставшие значения цен закрытия, что делает их особенно полезными для короткосрочного прогнозирования.
## Выводы
В ходе проекта было выполнено глубокое исследование данных о ценах закрытия акций Сбербанка и построены прогнозы с использованием двух различных моделей машинного обучения. Модель случайного леса показала себя лучше на тестовых данных, и ее можно рассматривать как основной инструмент для дальнейших прогнозов.