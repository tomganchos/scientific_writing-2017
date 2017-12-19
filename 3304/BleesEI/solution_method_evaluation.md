## Исследование решения

Было проведено исследование работы исполняемого сценария на статьях, написанных студентами СПбГЭТУ "ЛЭТИ" в рамках своих научных исследований, а также, в качестве примера качественно написанной статьи, была взята статья Заславского М. М., Блееса Э. И., Баландина С. И. - "Метод обработки в реальном времени открытых данных, содержащих геоконтекстную разметку"[1].

### Определение рекомендаций по интерпретации результатов проверки

Необходимо определить рекомендации по интерпретации полученных результатов проверки.
Критерии допустимых уровней водности текста определены SEO-специалистами [2]. С поправкой на научность текста, что требует связанности, были приняты следующие уровни допустимости:

* до 20% - естественное содержание «воды» в тексте;

* от 20% до 30% - превышенное содержание «воды» в тексте;

* от 30% - высокое содержание «воды» в тексте.

Определение естественности текста осуществляется на основе отклонения графика частоты встречаемости слов от идеального графика по Ципфу.
Закономерность Ципфа: ![equation](https://wikimedia.org/api/rest_v1/media/math/render/svg/748f1048c708b58d3c38fc6c0ede5ff8103f5c9e), где ![equation](https://wikimedia.org/api/rest_v1/media/math/render/svg/5949c8b1de44005a1af3a11188361f2a830842d1) - частота встречаемости n-го по рангу слова; ![equation](https://wikimedia.org/api/rest_v1/media/math/render/svg/398f438d75434e6fbf48dc232c1ad7228a738568) - количество повторений самого популярного слова в тексте.
Показатель отклонения ![equation](https://latex.codecogs.com/gif.latex?%5Csigma) вычисляется на основе среднеквадратичного отклонения точек дискретной функции ![equation](https://latex.codecogs.com/gif.latex?f%28x%29) - практических показателей текста от точек дискретной функции ![equation](https://latex.codecogs.com/gif.latex?g%28x%29) - идеальной функции по Ципфу.
Показатель отклонения: ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20%5Csigma%20%3D%20%5Csqrt%7B%5Cfrac1N%5Csum_%7Bi%3D1%7D%5EN%28g%28x_i%29-f%28x_i%29%29%5E2%7D)

Допустимые уровни значений показателя отклонения были найдены экспериментально, используя функцию обратной линейной зависимости в качестве плохого примера, и функции, приближенной к идеальному распределению по Ципфу, как хорошего примера частотного распределения слов в тексте.
Допустимые уровни значений показателя отклонения от закона Ципфа:

* >= 12 - низкая естественность;

* 7-12 - средний уровень естественности;

* 2-7 - хороший уровень естественности;

* < 2 - идеальный текст.

### Результаты исследования

В качестве выборки статей использовались статьи студентов СПбГЭТУ "ЛЭТИ", написанные в рамках научных исследований. Выборка состояла из 17 статей.
Наблюдаемый показатель отклонения от идеального распределение по закону Ципфа находился в промежутке от 2.3869 до 8.7569. Среднее значение показателя отклонения составило 6.5566.
Результаты показали что 7 из 17 статей имеют средний уровень естественности, а остальные 10 хороший уровень.
Наблюдаемый показатель "водности" текста находился в промежутке от 14.6766 до 24.3655. Среднее значение показателя "водности" составило 20.0499.
Результаты показали что 8 из 17 статей имеют естественный уровень "воды" в тексте, а остальные 9 повышенный уровень.

Результаты проверки примера качественной статьи [1]: показатель отклонения 7.9469, уровень "воды" 20.9397, то есть средний уровень естественности и повышенный уровень "водности" текста.

Тенденцию к понижению уровня естественности в научно-технических статьях можно объяснить частым упоминанием ключевых для понимания текста связок слов. Повышенный уровень водности объясняется необходимостью в связи частей статьи в единое целое, для лучшего понимания читателя.

## Источники

1. Заславский М.М., Блеес Э.И., Баландин С.И. Метод обработки в реальном времени открытых данных, содержащих геоконтекстную разметку // Научно-технический вестник информационных технологий, механики и оптики. 2017. Т. 17. № 5. С. 850–858. doi: 10.17586/2226-1494-2017-17-5-850-858 
2. text.ru