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

print(f'Результат 1: {calculate_average("1, 2, 3")}') # Строка перебирается, но каждый символ - строковый тип
print(f'Результат 2: {calculate_average([1, "Строка", 3, "Ещё Строка"])}') # Учитываются только 1 и 3
print(f'Результат 3: {calculate_average(567)}') # Передана не коллекция
print(f'Результат 4: {calculate_average([42, 15, 36, 13])}') # Всё должно работать


"C:\Users\User\PycharmProjects\HELLO WORLD\.venv\Scripts\python.exe" "C:\Users\User\PycharmProjects\HELLO WORLD\module_8_2.py" 
Некорректный тип данных для подсчета суммы - 1
Результат 1: 0.0
Результат 2: 0.25
В numbers некорректный тип данных
Результат 3: None
Результат 4: 10.5

Process finished with exit code 0


