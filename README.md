# Python-Country-Capital

## Code

```
import sys
from tkinter import Tk, simpledialog, messagebox

def read_from_file():
    with open('worldCapital.txt', 'r') as file:
        for line in file:
            line = line.rstrip('\n')
            country, capital = line.split('/')
            country = country.capitalize()
            capital = capital.capitalize()
            world_capital[country] = capital
            
def write_to_file(country_name, capital_name):
    with open('worldCapital.txt', 'a') as file:
        file.write('\n')
        file.write(country_name + '/' + capital_name)
        file.close()
        
root = Tk()
root.withdraw()
world_capital = {}
while True:
    read_from_file()
    simpledialog.askstring
    query_country = ''
    query_country = simpledialog.askstring('Country', 'Type the name of a country: ')
    query_country = query_country.capitalize()
    if query_country in world_capital:
        result = world_capital[query_country]
        messagebox.showinfo('Answer','The capital city of ' + query_country + ' is ' + result + '!')
    else:
        new_capital = simpledialog.askstring('Teach me', 'I don\' know the answer. Please teach me. What is the capital city of '+ query_country + '?:')
        messagebox.showinfo('Thanks', 'Thank you for teaching me. I will definitely know it next time!')
        new_capital = new_capital.capitalize()
        write_to_file(query_country, query_capital)
    answer = simpledialog.askstring('Continue', 'Do you want to try again? y/n')
    if answer == 'n':
        messagebox.showinfo('Thanks', 'Thank you for playing!')
        root.destroy()
        sys.exit()
```

## Result

![Fig01](https://github.com/psungg/Python-Country-Capital/blob/main/Images/Fig01.png)

![Fig02](https://github.com/psungg/Python-Country-Capital/blob/main/Images/Fig02.png)

![Fig03](https://github.com/psungg/Python-Country-Capital/blob/main/Images/Fig03.png)

![Fig04](https://github.com/psungg/Python-Country-Capital/blob/main/Images/Fig04.png)

![Fig05](https://github.com/psungg/Python-Country-Capital/blob/main/Images/Fig05.png)

