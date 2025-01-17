Отчет по лабораторной работе № 1

№ группы: ПМ-2403

Выполнил: Комаров Максим Олегович

Вариант: 13

Содержание:

	1.	Постановка задачи
	2.	Входные и выходные данные
	3.	Выбор структуры данных
	4.	Алгоритм
	5.	Программа
	6.	Анализ правильности решения

1. Постановка задачи

На координатной плоскости расположена точка с координатами x, y. Известно, что x \neq 0 и y \neq 0. Нужно определить, ближе к какой числовой оси (X или Y) и к какой её части (положительная или отрицательная) находится точка. На вход программы подаются два целых числа x и y.

Пример:

	•	Если x = 5, y = 3, точка находится в положительной части оси X.
	•	Если x = -4, y = -7, точка находится в отрицательной части оси X.

2. Входные и выходные данные

Данные на вход:

	•	x (целое число) -10^9 \leq x \leq 10^9
	•	y (целое число) -10^9 \leq y \leq 10^9

Данные на выход:

Одно из значений:

	•	“Положительная часть оси X”
	•	“Отрицательная часть оси X”
	•	“Положительная часть оси Y”
	•	“Отрицательная часть оси Y”

3. Выбор структуры данных

Для решения задачи будем использовать простые целочисленные переменные x и y. Для хранения результата будем использовать строку, которую выведем в зависимости от условий.

4. Алгоритм

Алгоритм выполнения программы:

	1.	Ввести два целых числа x и y.
	2.	Проверить условия:
	•	Если абсолютное значение x больше y, то точка ближе к оси X:
	•	Если x > 0, вывести “Положительная часть оси X”.
	•	Если x < 0, вывести “Отрицательная часть оси X”.
	•	Если абсолютное значение y больше x, то точка ближе к оси Y:
	•	Если y > 0, вывести “Положительная часть оси Y”.
	•	Если y < 0, вывести “Отрицательная часть оси Y”.
	3.	Завершить программу.

5. Программа

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        // Создаем сканер для считывания входных данных
        Scanner scanner = new Scanner(System.in);

        // Вводим координаты x и y
        int x = scanner.nextInt();
        int y = scanner.nextInt();

        // Логика определения ближней оси
        if (Math.abs(x) > Math.abs(y)) {
            if (x > 0) {
                System.out.println("Положительная часть оси X");
            } else {
                System.out.println("Отрицательная часть оси X");
            }
        } else {
            if (y > 0) {
                System.out.println("Положительная часть оси Y");
            } else {
                System.out.println("Отрицательная часть оси Y");
            }
        }

        // Закрываем сканер
        scanner.close();
    }
}

6. Анализ правильности решения

Программа работает корректно на всем множестве решений с учётом ограничений.

	1.	Тест на x = 5, y = 3:
	•	Input: 5 3
	•	Output: Положительная часть оси X
	2.	Тест на x = -4, y = -7:
	•	Input: -4 -7
	•	Output: Отрицательная часть оси Y
	3.	Тест на x = 2, y = 9:
	•	Input: 2 9
	•	Output: Положительная часть оси Y
	4.	Тест на x = -8, y = -1:
	•	Input: -8 -1
	•	Output: Отрицательная часть оси X
