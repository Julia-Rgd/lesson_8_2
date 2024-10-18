def personal_sum(numbers):
    result = 0
    incorrect_data = 0
    for i in numbers:
        try:
            result += i
        except TypeError:
            incorrect_data += 1
            print(f"Некорректный тип данных для подсчета суммы - {i}")
    return result, incorrect_data

def calculate_average(numbers):
    try:
        per_sum = personal_sum(numbers)
        avg = per_sum[0] / (len(numbers) - per_sum[1])
        return avg
    except ZeroDivisionError:
        return 0
    except TypeError:
        print("В numbers некорректный тип данных")
        return None
 Всё должно работать


"C:\Users\User\PycharmProjects\HELLO WORLD\.venv\Scripts\python.exe" "C:\Users\User\PycharmProjects\HELLO WORLD\module_8_2.py" 
Некорректный тип данных для подсчета суммы - 1
Некорректный тип данных для подсчета суммы - ,
Некорректный тип данных для подсчета суммы -  
Некорректный тип данных для подсчета суммы - 2
Некорректный тип данных для подсчета суммы - ,
Некорректный тип данных для подсчета суммы -  
Некорректный тип данных для подсчета суммы - 3
Результат 1: 0
Некорректный тип данных для подсчета суммы - Строка
Некорректный тип данных для подсчета суммы - Ещё Строка
Результат 2: 2.0
В numbers некорректный тип данных
Результат 3: None
Результат 4: 26.5

Process finished with exit code 0


