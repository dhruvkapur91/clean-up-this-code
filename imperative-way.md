
# Imperative Way
- Write a **characterization test** to find out what the function below does.
- What are some of the code smells you identify?
- Once you understand it, try simplifying it. There are probably multiple ways in which it can happen. Why not try some collection APIs in Python to achieve that?

```python
	INTEGER = "Integer"

    def token(self, text, current_position):
        current_char = text[current_position]

        digits = ""
        next_position = current_position

        while current_char.isdigit():
            digits += current_char
            next_position += 1
            if next_position < len(text):
                current_char = text[next_position]
            else:
                break 

        token = (INTEGER, int(digits))
        return (token, next_position)

```