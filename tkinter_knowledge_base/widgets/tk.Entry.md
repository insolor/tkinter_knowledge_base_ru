# tk.Entry

Получение значения:
```python
value = entry.get()
```

Вставка значения:
```python
entry.insert(0, "text")  # вставка в начало
entry.insert(tk.END, "text")  # вставка в конец
```

Удаление:
```python
entry.delete(0, tk.END)  # Удаление по диапазону индексов
entry.delete(0)  # Удаление от указанного индекса до конца
```

Удаление последнего символа:
```python
entry.delete(len(entry.get()) - 1)
# или
entry.delete(entry.index(tk.END) - 1)
```
Второй вариант by [@rdbende](https://github.com/rdbende), взят отсюда: [r/learnpython: How do you delete the last character you typed in entry box tkinter](https://www.reddit.com/r/learnpython/comments/ngdkmk/comment/gyyl6dk/?utm_source=share&utm_medium=web2x&context=3)

Замена текста (через очистку / вставку):
```python
entry.delete(0)
entry.insert(0, "text")
```

Замена текста через использование привязанной переменной `StringVar`:
```python
entry_var = tk.StringVar()
entry = tk.Entry(textvariable=entry_var)

...

entry_var.set("text")
```
