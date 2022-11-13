Добавление элементов по одному:
```python
listbox.insert(0, "В начало")
listbox.insert(tk.END, "В конец")
```
Добавление списка:
```python
list_variable = tk.Variable()
listbox = tk.Listbox(listvariable=list_variable)
list_vairable.set(("Первый", "Второй", "Третий"))
```
