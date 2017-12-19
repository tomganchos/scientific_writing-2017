Решение должно представлять собой билиотеку или фреймворк, позволяющий создавать решающие компоненты (единицы декомпозиции) и объединять их в единую гибкую вычислительную сеть. Предоставляющую простой инетрфейс взаимодействия со всеми вычислительным единицами. Также необходимо пользовательское приложение для наблюдения за состоянием системы и настройки отдельных компонентов и общего решающего модуля.

Поскольку ставится задача обеспечить возможность оперативного изменения структуры модели (под моделью будем понимать алгоритм верхнего уровня, решающий глобальную задачу), это накладывает следующие требования к архитектуре: 

 - унификация структуры компонента модели; 

 - унифицированный доступ к параметрам, переменным состояния, входным и выходным данным компонентов; 

 - средства добавления новых компонентов в модель, удаления существующих, создание связей между компонентами; 

 - возможность замены или изменения компонентов во время расчета; 

Для обеспечения быстрой скорости работы столь сложной системы выбран язык реализации С++ и схема обмена данных без непосредственного копирования. Для упрощения реализации выбран объектно ореинторванный подход для реализации решающих узлов (компонентов).