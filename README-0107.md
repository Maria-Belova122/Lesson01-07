# Задание по теме "Базовые структуры данных"
grades = [[5, 3, 3, 5, 4], [2, 2, 2, 3], [4, 5, 5, 2], [4, 4, 3], [5, 5, 5, 4, 5]] # Список наборов оценок студентов
length1 = len(grades) # Кол-во элементов в списке grades
students = {'Johnny', 'Bilbo', 'Steve', 'Khendrik', 'Aaron'} # Множество имен студентов
keys_students = list(students) # Перевод множества в список студентов
r = keys_students.sort() # Сортировка списка студентов по алфавиту
length2 = len(keys_students) # Кол-во элементов в списке студентов
values_av_grade1 = list() # Создание пустого списка значений 1 (для создания списка средних баллов в цикле FOR)
for i in range(length1): # Повтор операций для каждого элемента списка grades / Цикл запускается 'length1' раз
    av_grade = sum(grades[i]) / len(grades[i]) # Расчет среднего балла для i-го набора оценок
    values_av_grade1.append(av_grade) # Добавление среднего балла в список values_av_grade1
dict_average_grade1 = dict() # Создание пустого словаря 1
for i in range(length2): # Создание словаря 1 в цикле FOR  / Цикл запускается 'length2' раз
    dict_average_grade1[keys_students[i]] = values_av_grade1[i]
print('Словарь 1:', dict_average_grade1) # Вывод словаря 1 на консоль
values_av_grade2 = list() # Создание пустого списка значений 2 (для создания списка средних баллов в цикле WHILE)
while len(grades) != 0: # Цикл запускается пока список grades не будет пуст, т.е. пока мы не извлечем из него все элементы
    first_list_grade = grades.pop(0) # Извлечение первого элемента из списка grades
    av_grade = sum(first_list_grade) / len(first_list_grade) # Среднее арифметическое первого набора оценок
    values_av_grade2.append(av_grade) # Добавление среднего балла в список values_av_grade2
dict_average_grade2 = dict(zip(keys_students, values_av_grade2)) # Создание словаря 1
print('Словарь 2:', dict_average_grade2) # Вывод словаря 2 на консоль
print(dict_average_grade1 == dict_average_grade2) # Сравнение полученных словарей