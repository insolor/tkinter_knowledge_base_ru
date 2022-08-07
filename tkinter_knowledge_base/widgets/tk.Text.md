# tk.Text
Получение полного текста:

```python
import tkinter as tk

...

value = text.get("1.0", tk.END)
```

Индекс `1.0` - 1-я строка, 0-й символ

Добавление текста в начало:

```python
text.insert("1.0", "Текст")
```

Добавление текста в конец:
```python
text.insert(tk.END, "Текст")
```
