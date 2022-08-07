# ttk.Combobox
Создание:

```python
combo = Combobox(w, values=["value 1", "value 2"], state="readonly")
```

Установить значение (по индексу):

```python
combo.current(1)
```

Событие изменения значения:

```python
def on_change_selection(event):
    if combo.get() == "value 1":
        # Если выбрана 1, то выполнить какое-то действие
        print(1)

combo.bind("<<ComboboxSelected>>", on_change_selection)
```
