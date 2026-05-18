"""
Модуль калькулятора для совместной разработки.
Каждый участник добавляет свою операцию.
"""

def add(a, b):
    """Возвращает сумму a и b."""
    return a + b

def subtract(a, b):
    """Возвращает разность a и b."""
    return a - b

def multiply(a, b):
    """Возвращает произведение a и b."""
    return a * b

def divide(a, b):
    """
    Возвращает частное a и b.
    При b = 0 возвращает ошибку.
    """
    if b == 0:
        raise ValueError("Деление на ноль невозможно")
    return a / b

def power(a, b):
    """Возвращает a в степени b."""
    return a ** b

def modulus(a, b):
    """Возвращает остаток от деления a на b."""
    if b == 0:
        raise ValueError("Деление на ноль невозможно")
    return a % b

def main():
    """Интерактивный режим калькулятора."""
    print("=== Калькулятор ===")
    print("Доступные операции: +, -, *, /, **, %")
    
    try:
        a = float(input("Введите первое число: "))
        op = input("Введите операцию (+, -, *, /, **, %): ")
        b = float(input("Введите второе число: "))
        
        if op == '+':
            result = add(a, b)
        elif op == '-':
            result = subtract(a, b)
        elif op == '*':
            result = multiply(a, b)
        elif op == '/':
            result = divide(a, b)
        elif op == '**':
            result = power(a, b)
        elif op == '%':
