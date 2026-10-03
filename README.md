# Keypad

Typing on a [wedgie](https://wedgie.dev): a PIN pad and a keyboard, both on one grid.

- Joystick: move. **A** (or press the joystick in): type the key. **Y**: delete (on an empty box: cancel).
- **X**: done. **B**: caps (keyboard only).
- The PIN pad finishes by itself on the last digit.

The app runs one, then the other, and shows what you typed.

## From your own app

Copy `keypad/keypad.py` into your app as `<yourmod>_keypad.py` (app files must start with your mod), then:

```python
from mymod_keypad import pin, text
code = pin(lcd, "Enter PIN", 4)     # "1234", or None if cancelled
name = text(lcd, "Name it")         # "my wallet", or None
```

`pin()` reads only real button presses by default: a computer on USB can't type a PIN.

No saves. MIT.
