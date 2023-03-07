# Проектирование кибериммунного устройства мониторинга оборудования

## Общее описание продукта

### Назначение и применение продукта

Данный продукт используется в промышленных сферах, где используется какое-либо оборудование для производства. Решение считывает показатели всех устройств и следит за их значениями. В случае превышения пороговых значений система генерирует событие, которое может получить пользователь для дальнейшего анализа. В данном случае предполагается использовать данную систему на заводе по производству лекарств.

### Ценности продукта

Данное решение позволяет в постоянном режиме следить за всеми показателями устройств на заводе, а в случае превышения какого-либо значения система генерирует события с соответствующими данными (время превышения, какой показатель был превышен, на какую величину, какой аппарат, что он выпускает и т.д.).

## Характеристики системы

### Активы



### Ущерб

Ущерб при атаке на данную систему - утечка данных показателей оборудования, невозможность считать показатели, неработоспособность системы.

### Возможные риски

Исходя из ущерба, можно выделить и риски - существует возможность утечки данных или вывода из строя системы или её частей.

## Концепция безопасности системы

Исходя из вышеперечисленных пунктов можно сформулировать основную концепцию безопасности данной системы - никакие данные не могут быть получены неавторизованными лицами и недопустим удалённый доступ ими к системе, а также недопустим выход системы из строя.

## Цели и предположения безопасности системы

### Цели безопасности

1.  Система считывает только подключенное к ней оборудование;

2.  Все оборудование выдаёт только реальные показатели, которые относятся именно к нему;

3.  Система сообщает о попытках взлома.

### Предположения безопасности

1.	Защита от неавторизованного доступа;

2.	Защита от намеренного искажения показателей оборудования;

3.	В случае бездействия пользователя, система выходит из его аккаунта.

## Сценарии использования системы

### Ключевые сценарии использования

1.	Просмотр характеристик оборудования;

2.	Изменение пороговых значений;

3.	Анализ событий, созданных системой при превышении пороговых значений.

### Негативные сценарии

1.	Установление слишком маленьких или слишком больших величин пороговых значений, вследствие чего возникает слишком много событий или система их не создаёт, когда надо;

2.	Удаление части оборудования из системы программных способов неавторизованным пользователем;

3.	Добавление несуществующего оборудования в систему.



