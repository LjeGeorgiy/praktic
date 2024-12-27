import math

def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):
    return x * y

def divide(x, y):
    if y != 0:
        return x / y
    else:
        return "Ошибка: деление на ноль!"

def power(x, y):
    return x ** y

def sqrt(x):
    if x >= 0:
        return math.sqrt(x)
    else:
        return "Ошибка: отрицательное число!"

def main():
    print("Выберите операцию:")
    print("1. Сложение")
    print("2. Вычитание")
    print("3. Умножение")
    print("4. Деление")
    print("5. Возведение в степень")
    print("6. Квадратный корень")

    choice = input("Введите номер операции (1/2/3/4/5/6): ")

    if choice in ['1', '2', '3', '4', '5']:
        num1 = float(input("Введите первое число: "))
        num2 = float(input("Введите второе число: "))

        if choice == '1':
            print(f"{num1} + {num2} = {add(num1, num2)}")
        elif choice == '2':
            print(f"{num1} - {num2} = {subtract(num1, num2)}")
        elif choice == '3':
            print(f"{num1} * {num2} = {multiply(num1, num2)}")
        elif choice == '4':
            print(f"{num1} / {num2} = {divide(num1, num2)}")
        elif choice == '5':
            print(f"{num1} ** {num2} = {power(num1, num2)}")
    elif choice == '6':
        num = float(input("Введите число: "))
        print(f"√{num} = {sqrt(num)}")
    else:
        print("Неверный выбор операции!")

if __name__ == "__main__":
    main()
