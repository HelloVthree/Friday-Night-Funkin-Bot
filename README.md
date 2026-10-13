# FNF Python Bot (`BotFNF1.py`)

A simple Python automation script designed to play Friday Night Funkin' by detecting specific pixel colors on the screen and simulating key presses (`A`, `W`, `S`, `D`).

---

## Prerequisites

Make sure you have Python installed on your system. You will also need to install a couple of external Python libraries (`pyautogui` and `pynput`) for controlling the keyboard and reading screen pixels.

Open your terminal or command prompt and run:

```bash
pip install pyautogui pynput
```

---

## Configuration Note (Important!)

This script relies on **hardcoded screen coordinates and color values**:
* **Coordinates:** `(1115, 206)`, `(1285, 206)`, `(1437, 206)`, `(1596, 206)`
* **Colors:** RGB tuples like `(194, 75, 153)`, etc.

Because these coordinates depend heavily on your monitor's resolution, window size, and game layout, **you will likely need to adjust these numbers** in `BotFNF1.py` to match your specific setup.

---

## How to Run

1. Open your terminal or command prompt in the folder containing `BotFNF1.py`.
2. Start your game of Friday Night Funkin' and position the game window so that the pixel check locations match your script coordinates.
3. Run the script using Python:
   ```bash
   python BotFNF1.py
   ```
4. The console will print `started`, and the bot will begin monitoring those pixel areas and pressing keys automatically.

> **Disclaimer:** Since the infinite loop (`while True:`) has no built-in keyboard listener to stop it gracefully, you may need to force-quit your terminal or move your mouse rapidly to a corner of the screen (triggering PyAutoGUI's failsafe) to stop the script.
