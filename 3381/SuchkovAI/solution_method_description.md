﻿## Описание метода решения

Пусть дана звёздная цепочка длины ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20m-1) вида ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20%5Cleft%20%5C%7B%20c_i%20%5Cright%20%5C%7D_%7Bi%3D1%7D%5Em) ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20c_1%20%3D%201). Для каждой звёздной цепочки существует вектор добавок ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20%5Cleft%20%5C%7B%20r_i%20%5Cright%20%5C%7D_%7Bi%3D1%7D%5E%7Bm-1%7D) длины ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20m-1), такой, что

![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20r_i%20%3D%20%5C%7Bx%20%3A%201%20%5Cleq%20x%20%5Cleq%20i%5C%7D%2C%20%5C%2C%20c_i%20%3D%20c_%7Bi%20-%201%7D%20&plus;%20c_%7Br_%7Bi%20-%201%7D%7D%2C%20%5C%2C%202%20%5Cleq%20i%20%5Cleq%20m%20-%201).

Таким образом, ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20r_1) всегда равен 1, ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20r_2%20%3D%20%5C%7B1%3B2%5C%7D) и так далее. Последний элемент вектора добавок принимает значения от 1 до ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20m-1). Естественно считать, что наибольшая звёздная цепочка будет иметь вид ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20c%20%3D%20%5Cleft%20%5C%7B%201%3B%202%3B%204%3B%20%5Cdots%20%3B%202%5E%7Bm%20-%201%7D%5Cright%20%5C%7D), а её вектор добавок - ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20r%20%3D%20%5Cleft%20%5C%7B%201%3B%202%3B%203%3B%20%5Cdots%20%3B%20m%20-%201%5Cright%20%5C%7D); наименьшая звёздная цепочка имеет вид ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20c%20%3D%20%5Cleft%20%5C%7B%201%3B%202%3B%203%3B%20%5Cdots%20%3B%20m%20%5Cright%20%5C%7D), а её вектор добавок - ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20r%20%3D%20%5Cleft%20%5C%7B%201%3B%201%3B%201%3B%20%5Cdots%20%3B%201%20%5Cright%20%5C%7D).

Исходя из этого, можно сделать вывод, что объём множеств различных звёздных цепочек длины ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20m-1) равно ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20%28m-1%29%21), т.е. ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20%5C%23C%5C%7Bl%5E*%28N%29%20%3D%20m%20-%201%5C%7D%20%3D%20%28m%20-%201%29%21).

С помощью заданных понятий был разработан алгоритм, основанный на свойствах вектора добавок.

Пусть задано некое число ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20N). Необходимо найти минимальную звёздную цепочку, такую, что ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20c_m%20%3D%20N).

Представим заданное число в бинарном представлении: ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20N%20%3D%20%5Csum_%7Bi%20%3D%201%7D%5Es2%5E%7Bk_i%7D). Прямой алгоритм (перебор) заключается в следующем: перебираются вектора добавок вида ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20%5Cleft%20%5C%7B%20r_i%20%5Cright%20%5C%7D_%7Bi%3D1%7D%5E%7Bm-1%7D), по данным векторам добавок строится звёздная цепочка. Если для вектора добавок данной длины звёздная цепочка не найдена, увеличиваем вектор на одну позицию. На некотором шаге ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20m%20%5Cleq%20%5Clambda%28N%29%20&plus;%20%5Cnu%28N%29%20-%201) звёздная цепочка будет найдена. Таким образом необходимо выполнить ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20%5Csum_%7Bm%20%3D%20%5Clambda%28N%29%7D%5E%7B%5Clambda%28N%29%20&plus;%20%5Cnu%28N%29%20-%201%7Dm%21) операций перебора. Это достаточно много и займет много времени.

Можно заметить, что при изменении последнего элемента вектора добавок с ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20m-1) до 1, то и последний элемент звёздной цепочки монотонно убывает. Таким образом, можно уменьшать не весь вектор добавок сразу, а, например, половину. Рассмотрим вектор добавок вида ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20%5Cleft%20%5C%7B%20r_i%20%5Cright%20%5C%7D_%7Bi%20%3D%201%7D%5Eq%20%5Ccup%20%5Cleft%20%5C%7B%20%5Crho_j%20%5Cright%20%5C%7D_%7Bj%20%3D%20q%20&plus;%201%7D%5Em), где ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20%5Cleft%20%5C%7B%20r_i%20%5Cright%20%5C%7D_%7Bi%20%3D%201%7D%5Eq) - фиксированный вектор, a ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20%5Crho_j%20%3D%20%5Cleft%20%5C%7B%20x%20%3A%201%20%5Cleq%20x%20%5Cleq%20j%20%5Cright%20%5C%7D). Таких наборов получится ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20%5Cfrac%7Bm%21%7D%7Bq%21%7D) штук Монотонность при этом, конечно, исчезнет, но наибольшее значение ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20c_m) получится для вектора добавок ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20%5Cleft%20%5C%7B%20r_i%20%5Cright%20%5C%7D_%7Bi%20%3D%201%7D%5Eq%20%5Ccup%20%5Cleft%20%5C%7B%20q%20&plus;%201%2C%20%5Cdots%2C%20m%20%5Cright%20%5C%7D) а наименьшее - для вектора добавок ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20%5Cleft%20%5C%7B%20r_i%20%5Cright%20%5C%7D_%7Bi%20%3D%201%7D%5Eq%20%5Ccup%20%5Cleft%20%5C%7B%201%2C%20%5Cdots%2C%201%20%5Cright%20%5C%7D) Для того, чтобы вычислить максимальные и минимальные значения, достаточно знать ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20c_%7Bq%20&plus;%201%7D) последнее число цепочки для вектора добавок ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20%5Cleft%20%5C%7B%20r_i%20%5Cright%20%5C%7D_%7Bi%20%3D%201%7D%5Eq). Таким образом, ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20c_%7B%5Cmin%7D%20%3D%20c_%7Bq%20&plus;%201%7D%20&plus;%20m%20-%20q), а ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20c_%7B%5Cmax%7D%20%3D%20c_%7Bq%20&plus;%201%7D%20%5Ccdot%202%5E%7Bm%20-%20q%7D).

Алгоритм дробления вектора добавок:

1) Внешний цикл по длинам цепочек: ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20%5Cunderline%20l%28N%29%20%5Cleq%20l%28N%29%20%5Cleq%20%5Coverline%20l%28N%29). Выбирается число ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20q%2C%20%5C%2C%201%20%5Cleq%20q%20%5Cleq%20m%20-%201). Пусть ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20q%20%3D%20%5Cfrac%20m2).

2) Внутренний цикл перебора всех ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20%5Cleft%20%5C%7B%20r_i%20%5Cright%20%5C%7D_%7Bi%20%3D%201%7D%5Eq) (![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20q%21) шагов). На каждом шаге при фиксированом ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20%5Cleft%20%5C%7B%20r_i%20%5Cright%20%5C%7D_%7Bi%20%3D%201%7D%5Eq) находим ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20c_%5Cmin) и ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20c_%5Cmax):

a) Если ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20c_m%20%3D%20N) - задача решена;

b) Если ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20N) не находится между ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20c_%5Cmin) и ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20c_%5Cmax), то переходим к следующему набору ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20%5Cleft%20%5C%7B%20r_i%20%5Cright%20%5C%7D_%7Bi%20%3D%201%7D%5Eq);

c) Если ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20N) находится между ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20c_%5Cmin) и ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20c_%5Cmax), то организуем внутренний цикл перебора всех векторов добавок ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20%5Cleft%20%5C%7B%20%5Crho_j%20%5Cright%20%5C%7D_%7Bj%20%3D%20q%20&plus;%201%7D%5Em). Таких наборов ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20%5Cfrac%7Bm%21%7D%7Bq%21%7D);

d) Если обнаруживается ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20c_m%20%3D%20N) - задача решена;

e) Если в цикле таких векторов не оказалось, то переходим к следующему (по введённой упорядоченности) вектору добавок ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20%5Cleft%20%5C%7B%20r_i%20%5Cright%20%5C%7D_%7Bi%20%3D%201%7D%5Eq).

3) Если все наборы фиксированной длины исчерпаны, то увеличиваем их длину во внешнем цикле.

Данный алгоритм затрачивает меньше времени, чем для простого перебора векторов добавок, но тем не менее, достаточно велико. Модифицировать данный алгоритм можно с помощью выявления фиксированной длины звёздной цепочки с помощью теоремы описанной в [1]. Это значительно сократит перебор, особенно для особых случаев, ведь нам будет известна минимальная длина аддитивной цепочки, следовательно, нет причины перебирать вектор добавок меньшей и/или большей длины. Если число не удовлетворяет ни одному случаю из теоремы, то можно дробить вектор добавок не на 2 части, а на 3, 4 и т.д., в зависимости от ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20%5Cunderline%20l%28N%29) и ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20%5Coverline%20l%28N%29), что тоже сокращает время поиска.

Некоторые оптимисты считают оправданным предположение о том, что ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20l%28N%29%20%3D%20l%5E*%28N%29) Однако, это оказалось неправдой. Трудно было поверить, что по данной аддитивной цепочке минимальной длины нельзя найти цепочку, той же длины, содержащую только звёздные шаги. В 1958 году Вальтер Хансен в [2] привёл доказательство теоремы о том, что для определённых больших значений ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20N) выполняется условие ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20l%28N%29%20%3C%20l%5E*%28N%29). Минимальное ![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B120%7D%20%5Clarge%20N) для которого это условие выполняется равно 12509.

## Источники

1. Д. Кнут. Искусство программирования Т. 2. М.: Вильямс, 2001 . 503-524 с.

2. Hansen W. Zum Scholz-Brauerschen Problem // Journal für reine und angewandte Mathematik. 1959, вып. 202. С. 129–136.