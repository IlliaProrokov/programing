[workbook_lessons01-05_synthesis_Task_UA.ipynb](https://github.com/user-attachments/files/27277979/workbook_lessons01-05_synthesis_Task_UA.ipynb)
{
 "cells": [
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "# Робочий зошит — Синтез: Уроки 01–05 (Завдання)\n",
    "\n",
    "**Name:**  \n",
    "**Date:**  \n",
    "\n",
    "Цей зошит додає **comparison operators** (Урок 05) до всього, що ми вже вивчили:\n",
    "\n",
    "- **Lesson 01** — `print()` та коментарі\n",
    "- **Lesson 02** — змінні та типи даних (`int`, `float`, `str`, `bool`)\n",
    "- **Lesson 03** — `input()` та перетворення типів (`int()`, `float()`, `str()`)\n",
    "- **Lesson 04** — арифметичні оператори (`+ - * / // % **`) та f-strings\n",
    "- **Lesson 05** — comparison operators (`== != < > <= >=`) → завжди повертають `bool`\n",
    "\n",
    "**Правила для цього зошита:**\n",
    "\n",
    "1. Використовуйте **f-strings** для виводу, який поєднує текст і змінні.\n",
    "2. Назви змінних у стилі **camelCase**.\n",
    "3. Булеві змінні називайте з префіксом `is`, `has` або `can` (`isAdult`, `hasLicense`, `canVote`).\n",
    "4. Додавайте короткий коментар над кожною вправою, який пояснює, що робить ваш код.\n",
    "5. Запускайте кожну клітинку через **Shift+Enter** і перевіряйте вивід, перш ніж рухатися далі.\n",
    "\n",
    "У зошиті **7 завдань**."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---\n",
    "## Розділ A — Розминка: comparisons завжди повертають `bool`"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Завдання 1 — Predict the result\n",
    "\n",
    "Для кожного порівняння нижче напишіть свій здогад (`True` або `False`) у коментарі **перед** тим, як запустити клітинку. Потім запустіть і перевірте, скільки ви вгадали.\n",
    "\n",
    "Не змінюйте вирази — просто заповніть пропуски в коментарях."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 1,
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "True\n",
      "False\n",
      "True\n",
      "True\n",
      "False\n",
      "True\n",
      "False\n"
     ]
    }
   ],
   "source": [
    "# Guess: True\n",
    "print(5 == 5)\n",
    "\n",
    "# Guess: False\n",
    "print(5 != 5)\n",
    "\n",
    "# Guess: True\n",
    "print(10 > 7)\n",
    "\n",
    "# Guess: True\n",
    "print(3 >= 3)\n",
    "\n",
    "# Guess: False\n",
    "# Пояснення: Python чутливий до регістру, \"c\" та \"C\" — це різні символи\n",
    "print(\"cat\" == \"Cat\")\n",
    "\n",
    "# Guess: True\n",
    "# Пояснення: 7 // 2 дорівнює 3, тому 3 == 3 це True\n",
    "print(7 // 2 == 3)\n",
    "\n",
    "# Guess: False\n",
    "# Пояснення: 2 в кубі (2**3) дорівнює 8. Вираз каже, що 8 не дорівнює 8, що є хибним\n",
    "print(2 ** 3 != 8)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---\n",
    "## Розділ B — Збереження comparisons у boolean variables"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Завдання 2 — Voting age check\n",
    "\n",
    "Запитайте у користувача `age` (перетворіть на `int`). Потім збережіть **два** boolean values:\n",
    "\n",
    "- `isAdult` — `True`, якщо вік 18 або більше\n",
    "- `isTeen` — `True`, якщо вік від 13 до 19 включно (використайте chained comparison: `13 <= age <= 19`)\n",
    "\n",
    "Виведіть обидва через f-strings. Приклад:\n",
    "\n",
    "```\n",
    "Age: 17\n",
    "isAdult: False\n",
    "isTeen: True\n",
    "```"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 2,
   "metadata": {},
   "outputs": [
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Age:  17\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Age: 17\n",
      "isAdult: False\n",
      "isTeen: True\n"
     ]
    }
   ],
   "source": [
    "# Запитуємо у користувача вік та конвертуємо в ціле число (int)\n",
    "age = int(input(\"Age: \"))\n",
    "\n",
    "# Створюємо дві булеві змінні\n",
    "# Перевіряємо, чи вік 18 або більше\n",
    "isAdult = age >= 18\n",
    "\n",
    "# Використовуємо chained comparison для перевірки діапазону від 13 до 19 включно\n",
    "isTeen = 13 <= age <= 19\n",
    "\n",
    "# Виводимо результати за допомогою f-strings\n",
    "print(f\"Age: {age}\")\n",
    "print(f\"isAdult: {isAdult}\")\n",
    "print(f\"isTeen: {isTeen}\")"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Завдання 3 — Temperature flags\n",
    "\n",
    "Запитайте у користувача температуру в **градусах Фаренгейта** (перетворіть на `float`). Створіть чотири boolean flags:\n",
    "\n",
    "- `isFreezing` — температура 32 або нижче\n",
    "- `isCold` — температура нижче 50\n",
    "- `isWarm` — температура 70 або вище\n",
    "- `isHot` — температура 90 або вище\n",
    "\n",
    "Виведіть усі чотири. Приклад:\n",
    "\n",
    "```\n",
    "Temperature: 75.0°F\n",
    "  isFreezing: False\n",
    "  isCold:     False\n",
    "  isWarm:     True\n",
    "  isHot:      False\n",
    "```"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 3,
   "metadata": {},
   "outputs": [
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Enter temperature in Fahrenheit:  45\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Temperature: 45.0°F\n",
      "  isFreezing: False\n",
      "  isCold:     True\n",
      "  isWarm:     False\n",
      "  isHot:      False\n"
     ]
    }
   ],
   "source": [
    "# Запитуємо температуру у Фаренгейтах та конвертуємо у float\n",
    "temperature = float(input(\"Enter temperature in Fahrenheit: \"))\n",
    "\n",
    "# Створюємо булеві прапорці (flags) згідно з умовами\n",
    "isFreezing = temperature <= 32\n",
    "isCold = temperature < 50\n",
    "isWarm = temperature >= 70\n",
    "isHot = temperature >= 90\n",
    "\n",
    "# Виводимо результати через f-strings з акуратними відступами\n",
    "print(f\"Temperature: {temperature:.1f}°F\")\n",
    "print(f\"  isFreezing: {isFreezing}\")\n",
    "print(f\"  isCold:     {isCold}\")\n",
    "print(f\"  isWarm:     {isWarm}\")\n",
    "print(f\"  isHot:      {isHot}\")"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---\n",
    "## Розділ C — Порівняння рядків (case matters)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Завдання 4 — Yes/No that actually works\n",
    "\n",
    "Поставте користувачу yes/no запитання. Використайте `.lower()`, щоб порівняння працювало незалежно від того, як він напише відповідь (`yes`, `YES`, `Yes` — усі мають дати однаковий результат). Збережіть результат у `saidYes` і виведіть його.\n",
    "\n",
    "Приклад (усі ці варіанти мають дати `saidYes: True`):\n",
    "\n",
    "```\n",
    "Want to continue? (yes/no) yes\n",
    "saidYes: True\n",
    "\n",
    "Want to continue? (yes/no) YES\n",
    "saidYes: True\n",
    "\n",
    "Want to continue? (yes/no) Yes\n",
    "saidYes: True\n",
    "```"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 4,
   "metadata": {},
   "outputs": [
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Want to continue? (yes/no)  yes\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "saidYes: True\n"
     ]
    }
   ],
   "source": [
    "# Ставимо користувачу запитання yes/no\n",
    "answer = input(\"Want to continue? (yes/no) \")\n",
    "\n",
    "# Використовуємо .lower(), щоб перетворити ввід на малі літери та порівняти з \"yes\"\n",
    "# Це дозволить розпізнати \"Yes\", \"YES\", \"yEs\" як True\n",
    "saidYes = answer.lower() == \"yes\"\n",
    "\n",
    "# Виводимо результат через f-string\n",
    "print(f\"saidYes: {saidYes}\")"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---\n",
    "## Розділ D — Поєднання арифметики з comparisons"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Завдання 5 — Even or odd\n",
    "\n",
    "Запитайте у користувача ціле число (`int`). Використайте оператор `%`, щоб отримати залишок від ділення на 2. Число парне, коли цей залишок дорівнює 0.\n",
    "\n",
    "Збережіть `isEven` як boolean і виведіть:\n",
    "\n",
    "```\n",
    "Enter a whole number: 14\n",
    "14 % 2 = 0\n",
    "isEven: True\n",
    "```\n",
    "\n",
    "**Підказка:** `isEven = number % 2 == 0`"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 5,
   "metadata": {},
   "outputs": [
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Enter a whole number:  2\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "2 % 2 = 0\n",
      "isEven: True\n"
     ]
    }
   ],
   "source": [
    "# Запитуємо у користувача ціле число (int)\n",
    "number = int(input(\"Enter a whole number: \"))\n",
    "\n",
    "# Обчислюємо залишок від ділення на 2 за допомогою оператора %\n",
    "remainder = number % 2\n",
    "\n",
    "# isEven буде True, якщо залишок дорівнює 0\n",
    "isEven = remainder == 0\n",
    "\n",
    "# Виводимо результати згідно з прикладом\n",
    "print(f\"{number} % 2 = {remainder}\")\n",
    "print(f\"isEven: {isEven}\")"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---\n",
    "## Розділ E — Налагодження (Debugging)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Завдання 6 — Fix the broken program\n",
    "\n",
    "Програма нижче має запитати у користувача його вік і чи він студент, а потім зберегти кілька boolean flags. У ній **щонайменше три** помилки. Скопіюйте її у порожню клітинку, виправте та запустіть свою версію.\n",
    "\n",
    "```python\n",
    "firstName = input(\"Your name: \")\n",
    "age = input(\"Your age: \")\n",
    "isAdult = age >= 18\n",
    "\n",
    "answer = input(\"Are you a student? (yes/no) \")\n",
    "isStudent = answer == \"Yes\"\n",
    "\n",
    "print(\"Hi \" + firstName + \"! isAdult: \" + isAdult + \", isStudent: \" + isStudent)\n",
    "```\n",
    "\n",
    "Подумайте над цим:\n",
    "\n",
    "- Що завжди повертає `input()`? Чи можна порівнювати рядок з числом через `>=`? *(What does `input()` always return? Can you compare a string to a number with `>=`?)*\n",
    "- Що буде, якщо користувач напише `YES` або `Yes` замість `yes`? *(What if the user types `YES` or `Yes` instead of `yes`?)*\n",
    "- Чи можна використовувати `+`, щоб приклеїти `bool` до `str`? *(Can you use `+` to glue a `bool` onto a string?)*"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 6,
   "metadata": {},
   "outputs": [
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Your name:  Illia\n",
      "Your age:  17\n",
      "Are you a student? (yes/no)  yes\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Hi Illia! isAdult: False, isStudent: True\n"
     ]
    }
   ],
   "source": [
    "# Виправлений код: додано перетворення типів та f-string\n",
    "firstName = input(\"Your name: \")\n",
    "\n",
    "# Помилка 1: input() повертає рядок, тому додаємо int() для порівняння з числом\n",
    "age = int(input(\"Your age: \"))\n",
    "isAdult = age >= 18\n",
    "\n",
    "answer = input(\"Are you a student? (yes/no) \")\n",
    "# Помилка 2: Використовуємо .lower(), щоб \"Yes\" або \"YES\" також працювали\n",
    "isStudent = answer.lower() == \"yes\"\n",
    "\n",
    "# Помилка 3: Використовуємо f-string, бо не можна додавати bool до str через +\n",
    "print(f\"Hi {firstName}! isAdult: {isAdult}, isStudent: {isStudent}\")"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---\n",
    "## Розділ F — Все разом"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Завдання 7 — Profile flag generator (capstone)\n",
    "\n",
    "Напишіть програму, яка створює невеликий \"profile summary\", використовуючи все з Уроків 01–05. Запитайте у користувача:\n",
    "\n",
    "- `firstName` (str)\n",
    "- `age` (int)\n",
    "- `gpa` (float)\n",
    "- `favoriteSubject` (str)\n",
    "\n",
    "Потім створіть ці booleans:\n",
    "\n",
    "- `isTeen` — `13 <= age <= 19` (chained comparison)\n",
    "- `isAdult` — вік 18 або більше\n",
    "- `isHonorRoll` — gpa 3.5 або більше\n",
    "- `lovesMath` — favoriteSubject дорівнює `\"math\"` (case-insensitive — використайте `.lower()`)\n",
    "\n",
    "Виведіть акуратний summary через f-strings. Покажіть `gpa` з **2 знаками після коми**. Приклад:\n",
    "\n",
    "```\n",
    "------------------------------\n",
    "        PROFILE\n",
    "------------------------------\n",
    "Name: Maria\n",
    "Age: 17\n",
    "GPA: 3.80\n",
    "Favorite subject: Math\n",
    "\n",
    "Flags:\n",
    "  isTeen:       True\n",
    "  isAdult:      False\n",
    "  isHonorRoll:  True\n",
    "  lovesMath:    True\n",
    "------------------------------\n",
    "```\n",
    "\n",
    "На початку коду додайте header comment block з полями `Program:`, `Author:`, `Date:` та `Purpose:` (як в Уроці 01)."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 8,
   "metadata": {},
   "outputs": [
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Name:  illia\n",
      "Age:  17\n",
      "GPA:  70\n",
      "Favorite subject:  lunch\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "------------------------------\n",
      "        PROFILE\n",
      "------------------------------\n",
      "Name: illia\n",
      "Age: 17\n",
      "GPA: 70.00\n",
      "Favorite subject: lunch\n",
      "\n",
      "Flags:\n",
      "  isTeen:       True\n",
      "  isAdult:      False\n",
      "  isHonorRoll:  True\n",
      "  lovesMath:    False\n",
      "------------------------------\n"
     ]
    }
   ],
   "source": [
    "# Program: Profile Flag Generator\n",
    "# Author: [Ваше Ім'я]\n",
    "# Date: 01.05.2026\n",
    "# Purpose: Builds a profile summary with several boolean flags\n",
    "\n",
    "# 1. Запитуємо у користувача чотири фрагменти інформації\n",
    "firstName = input(\"Name: \")\n",
    "age = int(input(\"Age: \"))\n",
    "gpa = float(input(\"GPA: \"))\n",
    "favoriteSubject = input(\"Favorite subject: \")\n",
    "\n",
    "# 2. Створюємо чотири булеві прапорці\n",
    "# Використовуємо ланцюжкове порівняння для підліткового віку\n",
    "isTeen = 13 <= age <= 19\n",
    "\n",
    "# Перевіряємо, чи є користувач дорослим\n",
    "isAdult = age >= 18\n",
    "\n",
    "# Перевіряємо, чи є GPA високим (3.5+)\n",
    "isHonorRoll = gpa >= 3.5\n",
    "\n",
    "# Перевірка предмета (case-insensitive) за допомогою .lower()\n",
    "lovesMath = favoriteSubject.lower() == \"math\"\n",
    "\n",
    "# 3. Виводимо відформатований підсумок профілю\n",
    "print(\"------------------------------\")\n",
    "print(\"        PROFILE\")\n",
    "print(\"------------------------------\")\n",
    "print(f\"Name: {firstName}\")\n",
    "print(f\"Age: {age}\")\n",
    "print(f\"GPA: {gpa:.2f}\")\n",
    "print(f\"Favorite subject: {favoriteSubject}\")\n",
    "\n",
    "print(\"\\nFlags:\")\n",
    "print(f\"  isTeen:       {isTeen}\")\n",
    "print(f\"  isAdult:      {isAdult}\")\n",
    "print(f\"  isHonorRoll:  {isHonorRoll}\")\n",
    "print(f\"  lovesMath:    {lovesMath}\")\n",
    "print(\"------------------------------\")"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "---\n",
    "## Коли закінчите\n",
    "\n",
    "1. Збережіть зошит (**Ctrl+S**).\n",
    "2. Закомітьте у репозиторій з повідомленням `synthesis 01-05 complete`.\n",
    "3. Підніміть руку, щоб я перевірив роботу.\n",
    "\n",
    "**Перевірте себе перед тим, як підняти руку:**\n",
    "\n",
    "- [ ] Кожна клітинка з кодом запускається без помилок.\n",
    "- [ ] Ви використали f-strings (а не `+` і `str()`) для виводу, що поєднує текст і змінні.\n",
    "- [ ] Назви змінних у стилі camelCase, а булеві змінні починаються з `is`, `has` або `can`.\n",
    "- [ ] Ви використали `==` (а не `=`) кожного разу, коли треба було порівняти два значення.\n",
    "- [ ] Порівняння рядків, які залежать від введення користувача, використовують `.lower()`.\n",
    "- [ ] У кожному завданні є хоча б короткий коментар про те, що робить ваш код."
   ]
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3 (ipykernel)",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.13.9"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 4
}
