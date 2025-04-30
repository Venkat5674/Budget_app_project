# Budget App

## Project Overview
The Budget App is a Python project that allows users to create budget categories, track deposits and withdrawals, and visualize spending using a bar chart.

## Features
- Supports multiple budget categories (e.g., Food, Clothing).
- Allows deposits, withdrawals, and balance checks for each category.
- Provides a transfer function to move funds between categories.
- Generates a bar chart showing the percentage spent per category.

## Example Usage
```python
from budget_app import Category, create_spend_chart

food = Category("Food")
food.deposit(1000, "initial deposit")
food.withdraw(10.15, "groceries")
food.withdraw(15.89, "restaurant and more food for dessert")

clothing = Category("Clothing")
food.transfer(50, clothing)

entertainment = Category("Entertainment")
entertainment.deposit(500, "initial deposit")
entertainment.withdraw(200, "movies")

print(food)
print(create_spend_chart([food, clothing, entertainment]))
```

## Example Output
```
*************Food*************
initial deposit        1000.00
groceries               -10.15
restaurant and more foo -15.89
Transfer to Clothing    -50.00
Total: 923.96
Percentage spent by category
100|
 90|
 80|
 70|
 60|
 50|
 40|    o
 30|    o
 20| o  o
 10| o  o  o
  0| o  o  o
    ----------
     F  C  E
     o  l  n
     o  t  t
     d  h  e
        i  r
        n  t
        g
```

## How to Run
- Create budget categories using the `Category` class.
- Use the `create_spend_chart` function to generate a spending bar chart.
