### Typing Monkey Game


```python
import random
import keyboard
from colorama import Fore, Style, init
import time

init(autoreset=True)  # Auto-reset color after each print

def load_quotes(file_path):
    with open(file_path, 'r') as f:
        lines = [line.strip() for line in f if line.strip()]
    return lines

def typing_test(text):
    print(Fore.WHITE + "\n" + text + "\n")
    typed = ""
    idx = 0

    while idx < len(text):
        key = keyboard.read_event()
        if key.event_type != keyboard.KEY_DOWN:
            continue

        char = key.name
        if char == 'space':
            char = ' '
        elif char == 'enter':
            break
        elif len(char) > 1:
            continue  # skip shift, ctrl, etc.

        expected = text[idx]
        if char == expected:
            print(Fore.GREEN + char, end="", flush=True)
        else:
            print(Fore.RED + char, end="", flush=True)

        typed += char
        idx += 1

    print(Style.RESET_ALL + "\n\n✅ Test complete.")

if __name__ == "__main__":
    quotes = load_quotes("quotes.txt")
    quote = random.choice(quotes)
    print("⌨️  Typing Test - Type the following line:\n")
    time.sleep(1)
    typing_test(quote)

```