# Домашнее задание к работе 2

## Условие задачи

Написать и отладить программу пересчета терабит в гигабайт и наоборот.

## 1. Алгоритм и блок-схема

### Алгоритм

1. **Начало**
2. **Объявить константы:**
   * `TBIT_TO_GB` = 128.0 — коэффициент перевода Терабит в Гигабайты.
   * `GB_TO_TBIT` = 0.0078125 — коэффициент перевода Гигабайт в Терабиты.
3. **Задать исходные данные:**
   * `tbit` — количество Терабит.
   * `gb_input` — количество Гигабайт.
4. **Вычислить значение в Гигабайтах:**
   * `gb = tbit * TBIT_TO_GB`
5. **Вычислить значение в Терабитах:**
   * `tbit_result = gb_input * GB_TO_TBIT`
6. **Вывести результаты расчетов с подстановкой всех значений в текст.**
7. **Конец**

### Блок-схема
https://www.draw.io?lightbox=1&highlight=0000ff&edit=_blank&layers=1&nav=1&title=%D0%BB%D0%B0%D0%B1%D0%B03%D0%B4%D0%B7.drawio#R1Vldk5sgFP01vnRmOwJ%2B5bFm0%2B1Du7udPLRvOyRStYPiEIxJf30hosZqUjPTaH0IgQPEyz33wJUYaJkcnjjOoi8sINSAZnAw0KMBIbBMS34p5FgiruOVQMjjQA9qgHX8i2jQ1GgeB2TXGigYoyLO2uCWpSnZihaGOWdFe9gPRttPzXBIOsB6i2kX%2FRYHIipRD7oN%2FonEYVQ9GTiLsifB1WC9kl2EA1acQWhloCVnTJS15LAkVDmv8ks57%2BOF3towTlIxZEL0%2FSs9FM8LXzw9U5uCxcPLywPUtoljtWASyPXrJuMiYiFLMV01qM9ZngZE%2FaopW82Yz4xlEgQS%2FEmEOGoycS6YhCKRUN1bPlM96OJSNLRjOd%2BSK%2FZXIYF5SMSVcah2uIxUwhIi%2BFHO44RiEe%2FbdmAdMmE9rp76ymJpITR1eFsAlVOOdbi3f6K0S89quJGVMzMa6MTYDexpg%2FeY5noJhuRk8ahK3zSksz23qsvSP5WrLuWUSjkpaosoFmSd4ZPPC6noPuL2hAtyuE5d19V6ArLbLqvUUTTiAhUWnQnLMy%2BT03LrrT60Zq4ANFABzigKgGhcBaB%2BBZxKH%2Bp4V6WlfLSJRYdtuS1nqip9jykllIUcJ5KijPBYWkf4n32vTccEegFooGCcewlmMXPBjCMENLIQnI4Qwo1sn6o68M138gOg997sMNjmZ4JTYOgxcLeoBqDjlHmFNTD7Pf6P49oaOa6r94CeHV5mN37vPq8if967PJp8l69on68e4MDECFijCMceWzjwltQo3LzFaZbPPj2ypheOPXfhjKMHB46sB6ujB5UWvXGyy6moU6VGCKYy4X9NmOzpEyZ37nHuDD0gvFEE4YKRBdF9ZfhrZtVSzLxPCmd6BXn9BHw4c3p5lWefKHG6gpvw4s69482dbDb34mW8N%2F8uoNVv
## 2. Реализация программы

```c
#include <stdio.h>
#include <locale.h>
#include <stdlib.h> // Нужна для функции system()

int main() {
    // Объявление и инициализация констант
    // Коэффициент перевода: 1 Терабит = 128 Гигабайт
    const float TBIT_TO_GB = 128.0f;
    const float GB_TO_TBIT = 1.0f / 128.0f;

    setlocale(LC_CTYPE, "");

    // Шаг 1: Задание исходного значения переменной
    float tbit; // Значение в Терабитах

    printf("ПЕРЕСЧЕТ ТЕРАБИТ В ГИГАБАЙТЫ И НАОБОРОТ\n");
    printf("======================================\n\n");

    // --- Прямой пересчет: Терабиты -> Гигабайты ---
    printf("Введите количество Терабит (например, 1.5): ");
    scanf("%f", &tbit);

    // Шаг 2: Вычисление значения в Гигабайтах
    float gb = tbit * TBIT_TO_GB;

    // Шаг 3: Вывод результата
    printf("-> %.3f Терабит = %.3f Гигабайт\n\n", tbit, gb);

    // --- Обратный пересчет: Гигабайты -> Терабиты ---
    float gb_input; // Значение в Гигабайтах

    printf("Введите количество Гигабайт (например, 256): ");
    scanf("%f", &gb_input);

    // Шаг 4: Вычисление значения в Терабитах
    float tbit_result = gb_input * GB_TO_TBIT;

    // Шаг 5: Вывод результата
    printf("-> %.3f Гигабайт = %.3f Терабит\n\n", gb_input, tbit_result);

    // Шаг 6: Пауза перед закрытием консоли
    system("pause");

    return 0;
}

## 3. Результаты работы программы
ПЕРЕСЧЕТ ТЕРАБИТ В ГИГАБАЙТЫ И НАОБОРОТ
======================================

Введите количество Терабит (например, 1.5): 4.5
-> 4.500 Терабит = 576.000 Гигабайт

Введите количество Гигабайт (например, 256): 512
-> 512.000 Гигабайт = 4.000 Терабит

Для продолжения нажмите любую клавишу . . .

## 4. Информация о разработчике
Щербаков Дмитрий бИЦТ-261
