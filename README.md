# Kuramoto Model Simulation | Симуляция модели Курамото

[![Python Version](https://img.shields.io/badge/python-3.11-green.svg)](https://www.python.org/downloads/)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

This repository contains a Python simulation of the Kuramoto model using Pygame. The simulation visualizes the synchronization of three oscillators with different frequencies and phases. The model uses the Runge-Kutta 4th order method for solving the differential equations that govern the oscillators' phases.

Этот репозиторий содержит симуляцию модели Курамото на Python с использованием Pygame. Симуляция визуализирует синхронизацию трех осцилляторов с разными частотами и фазами. Модель использует метод Рунге-Кутты 4-го порядка для решения дифференциальных уравнений, управляющих фазами осцилляторов.

## Prerequisites | Необходимые условия

Make sure you have Python installed on your system. You can download Python from [python.org](https://www.python.org/downloads/).

Убедитесь, что у вас установлен Python. Вы можете скачать Python с сайта [python.org](https://www.python.org/downloads/).

### Required Libraries | Необходимые библиотеки

Install the required libraries using pip:

Установите необходимые библиотеки с помощью pip:

```bash
pip install pygame pygame-widgets
```

## Running the Simulation | Запуск симуляции

To run the simulation, execute the following command:

Для запуска симуляции выполните следующую команду:

```bash
python main.py
```

## Features | Возможности

- **Sliders for K and dt:** Adjust the coupling strength (K) and the time step (dt) using sliders.
- **Buttons for fine adjustment:** Increase or decrease the values of K and dt using "+" and "-" buttons.
- **Toggle Drawing Lines:** Draw lines between the operators to visualize the distances.
- **Synchronization Detection:** The simulation detects when the oscillators synchronize and displays the synchronization time.

- **Слайдеры для K и dt:** Регулируйте силу связи (K) и временной шаг (dt) с помощью слайдеров.
- **Кнопки для точной настройки:** Увеличивайте или уменьшайте значения K и dt с помощью кнопок "+" и "-".
- **Переключение рисования линий:** Рисуйте линии между операторами для визуализации расстояний.
- **Обнаружение синхронизации:** Симуляция определяет, когда осцилляторы синхронизируются, и отображает время синхронизации.

## Classes | Классы

### Operator | Оператор

Represents an operator (oscillator) in the simulation.

Представляет оператора (осциллятор) в симуляции.

#### Attributes | Атрибуты:
- `name`: The name of the operator. | Имя оператора.
- `freq`: The frequency of the operator. | Частота оператора.
- `phase`: The initial phase of the operator. | Начальная фаза оператора.

### Settings | Настройки

Stores all the settings for the simulation.

Сохраняет все настройки для симуляции.

#### Attributes | Атрибуты:
- `K`: Coupling strength. | Сила связи.
- `dt`: Time step. | Временной шаг.
- `dt_counter`: Counter for the time steps. | Счетчик временных шагов.
- `syncTrue`: Indicates if the oscillators are synchronized. | Указывает, синхронизированы ли осцилляторы.
- `syncTime`: Time at which synchronization occurred. | Время, когда произошла синхронизация.
- `run`: Controls the simulation loop. | Управляет циклом симуляции.
- `showSync`: Indicates if synchronization status should be shown. | Указывает, следует ли показывать статус синхронизации.
- `syncStatus`: Status of synchronization. | Статус синхронизации.
- `max_distance`: List to store the maximum distances between operators. | Список для хранения максимальных расстояний между операторами.

## Functions | Функции

### rk4

Runge-Kutta 4th order method for solving differential equations.

Метод Рунге-Кутты 4-го порядка для решения дифференциальных уравнений.

### update

Updates the phases of the operators.

Обновляет фазы операторов.

### getPosition | получитьПозицию

Returns the x, y coordinates representing the position of an operator.

Возвращает координаты x, y, представляющие положение оператора.

### draw_circles | рисовать_круги

Draws the circles representing the operators.

Рисует круги, представляющие операторов.

### getDistance | получитьРасстояние

Calculates the distance between two operators.

Вычисляет расстояние между двумя операторами.

### draw_lines | рисовать_линии

Draws lines between operators based on their distance.

Рисует линии между операторами на основе их расстояния.

## User Interface | Пользовательский интерфейс

### Sliders | Слайдеры

- **K Slider:** Adjust the coupling strength. | Регулирует силу связи.
- **dt Slider:** Adjust the time step. | Регулирует временной шаг.

### Buttons | Кнопки

- **K + and - Buttons:** Fine adjustment of the coupling strength. | Точная настройка силы связи.
- **dt + and - Buttons:** Fine adjustment of the time step. | Точная настройка временного шага.
- **Draw Lines Button:** Toggles the drawing of lines between operators. | Переключает рисование линий между операторами.

### Text Boxes | Текстовые поля

- **K Text Box:** Displays the current value of K. | Отображает текущее значение K.
- **dt Text Box:** Displays the current value of dt. | Отображает текущее значение dt.
- **Colors of Operators Text Box:** Displays the colors representing the operators and their frequencies. | Отображает цвета, представляющие операторов и их частоты.

## License | Лицензия

This project is licensed under the MIT License. See the LICENSE file for details.

Этот проект лицензирован по лицензии MIT. Подробности см. в файле LICENSE.
