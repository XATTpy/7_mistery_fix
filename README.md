# Решатель квадратных уравнений

Скрипт **tests.py** производит **unittest** функции модуля **quadratic_equation.py**

# Как использовать

**tests.py** содержит **Test case**, состоящий из 4 тестов, применяемых к функции **get_roots** модуля **quadratic_equation.py**. 

В каждом тесте используются разные числа в качестве аргументов функции get_roots для симуляции ситуаций когда:

* Дискриминант > 0
* Д == 0
* Д < 0

Формат ответа юниттеста выглядит следующим образом : 

* Изоброжение порядка проводимых тестов, где "Е" - тест вызвавший исключение. Например: .EE.
* Название теста, вызвавшего ошибку (!)
* Описание исключения (!)
* Время, затраченное на прохождение всех тестов
* Результат теста (количество ошибок, если есть)

Импорт проверяемого модуля. Для поддержки чистоты окружения, мы можем импортировать отдельные функции модуля, вместо того, чтобы импортировать модуль целиком:

```python
from quadratic_equation import get_roots
```

Использование проверяемой функции:

```python
from quadratic_equation import get_roots

get_roots(3, 5, 4)
>>> (2.0, -1.0)
```

# Как запустить

Скрипт требует для своей работы установленного интерпретатора Python версии 3.5

Запуск на Linux:

```bash
python tests.py # может понадобиться вызов python3 вместо python, зависит от настроек операционной системы
E...
======================================================================
ERROR: test_first_root_less_than_second (__main__.QuadraticEquationTestCase)
----------------------------------------------------------------------
Traceback (most recent call last):
  File "tests.py", line 12, in test_first_root_less_than_second
    root1, root2 = get_roots(1, 2, -3)
TypeError: 'NoneType' object is not iterable

----------------------------------------------------------------------
Ran 4 tests in 0.000s

FAILED (errors=1)
```

Запуск на Windows происходит аналогично.

# Цели проекта

Код создан в учебных целях. В рамках учебного курса по веб-разработке ― [DEVMAN.org](https://devman.org)
