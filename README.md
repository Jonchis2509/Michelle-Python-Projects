# 🧠 Study Hours Analyzer

This repository is part of my journey as a Python developer. It features a simple but useful program that calculates and analyzes the number of study hours per week.

The **Study Hours Analyzer** prompts the user to enter how many hours they study each day and then calculates the **total hours** and the **average per day**, providing motivational feedback based on the result.

---

## 🚀 Features

- Asks the user for study hours from Monday to Sunday.
- Calculates the **total** and **average** study hours.
- Displays motivational feedback depending on consistency.
- Written in clean, beginner-friendly Python.

---

## 📄 Sample Code Overview

```python
# Welcome message
print("----------Welcome to Study Hours Analyzer!----------")
print("With this program you can obtain the average of the hours that you study per week.")

# List to store the hours
hours = []
week_days = ["monday", "tuesday", "wednesday", "thursday", "friday", "saturday", "sunday"]

# Function to calculate and display stats
def avg():
    for day in week_days:
        data = float(input(f"How many hours you studied on {day.capitalize()}: "))
        hours.append(data)

    average = sum(hours) / len(hours)
    total = sum(hours)

    print("-" * 30)
    print(f"Total hours studied: {total}")
    print(f"Average per day: {average:.2f}")

    message = "Feedback: "
    if average >= 4:
        print(f"{message}Great consistency!")
    elif 2 < average < 4:
        print(f"{message}Not bad. Try to increase a bit.")
    else:
        print(f"{message}You need to study more!")

# Run the function
avg()
```
python study_hours_analyzer.py
Michelle Portilla (Python Developer)

---


