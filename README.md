# Python Challenge 1
Interactive ordering system from a food truck menu.  
Users can select items from a menu and request any quantity of them. The application will show an itemized bill for all items ordered.

## Notes
Using string multiplication and subtracting string lengths is certainly one way to get a string to have a constant length.  
```
items = ['apple', 'banana', 'pineapple', 'strawberry']
for item in items:
    item_len = len(item)
    filler = ' ' * (20 - item_len)
    print(f'{item}{filler}[end]')

>>> apple               [end]
>>> banana              [end]
>>> pineapple           [end]
>>> strawberry          [end]
```  
But a much cleaner way is to use Python's built-in string method 'ljust' (left justify).  
Code learned from [W3Schools - Python String ljust() Method](https://www.w3schools.com/python/ref_string_ljust.asp)
```
items = ['apple', 'banana', 'pineapple', 'strawberry']
for item in items:
    print(f'{item.ljust(20, " ")}[end]')

>>> apple               [end]
>>> banana              [end]
>>> pineapple           [end]
>>> strawberry          [end]  
```

Same exact result, and all we had to pass were the string, the final string length we want, and the filler character, and Python does the rest. No need to explicitly do multiplication or subtraction.
