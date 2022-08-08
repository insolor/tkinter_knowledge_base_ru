# tk.Text
Получение полного текста:

```python
import tkinter as tk

...

value = text.get("1.0", tk.END)
```

[[#Индексы|Индекс]] `1.0` означает- 1-я строка, 0-й символ

Добавление текста в начало:

```python
text.insert("1.0", "Текст")
```

Добавление текста в конец:
```python
text.insert(tk.END, "Текст")
```

Удаление текста полностью:
```python
text.delete("1.0", tk.END)
```

## Индексы
- `"line.column"` - номер строки, номер столбца в тексте (нумерация строк с 1, нумерация столбцов с 0), также поддерживается формат float: `1.0`
- `"line.end"` - ссылка на конец указанной строки
- `tk.INSERT` - позиция текстового курсора
- `tk.CURRENT` - позиция ближайшая к курсору мыши
- `tk.END` - конец текста
- `tk.SEL_FIRST`, `tk.SEL_LAST` - начало, конец выделения;
	получить выделенный текст - `text.get(tk.SEL_FIRST, tk.SEL_LAST)`

См. также https://anzeljg.github.io/rin2/book2/2405/docs/tkinter/text-index.html

## Тэги
Создать тэг с указанием его свойств:
```python
text.tag_config("tag_name", foreground='blue')
```

Удалить тэги из диапазона текста:
```python
text.tag_remove(tag, 1.0, tk.END)
```

Получить все имена тегов:
```python
text.tag_names()
```

Добавление тега тексту:
```python
text.tag_add("tag_name", индекс_начала, индекс_конца)
```

Привязка обработчика событий на тег (например, обработка наведения, клика мышью):
```python
text.tag_bind("link", "<Button-1>", self.open_link)  # Клик левой клавишей мыши
text.tag_bind("link", "<Enter>",  # Наведение курсора мыши на объект ("hower")
                   lambda _: text.config(cursor="hand2"))
text.tag_bind("link", "<Leave>",  # Смещение курсора с объекта 
                   lambda e: text.config(cursor=""))
```
