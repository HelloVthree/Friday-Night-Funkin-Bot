# FNF Python Bot (`FNF_bot_V2.py`)

A simple Python automation script designed to play Friday Night Funkin' by detecting specific pixel colors on the screen and simulating key presses (`A`, `W`, `S`, `D`).

![](Images/Image_dashboard.png)


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

![](Images/Image_arrow.png)

Because these coordinates depend heavily on your monitor's resolution, window size, and game layout, **you will likely need to adjust these numbers** in `BotFNF1.py` to match your specific setup.

## ⚠️ Important Limitations (Why it might fail)

* **Does Not Support Hold Notes:** This script only performs short taps (`press_A`, `press_W`, `press_S`, `press_D`) with a fixed 0.05-second press duration. If a song or chart requires you to **hold** a note down, this script will let go immediately, causing you to miss/fail the hold note.
* **Fails on Different Color Codes:** The bot relies on exact hardcoded RGB color tuples (e.g., `(194, 75, 153)` for A, `(18, 250, 5)` for W, etc.). If you play a level, mod, or song that uses **different note colors**, custom charts, or changing UI themes, the script will completely fail to recognize the notes.

---

## How to Run

1. Open your terminal or command prompt in the folder containing `FNF_bot_V2.py`.
2. Start your game of Friday Night Funkin' and position the game window so that the pixel check locations match your script coordinates.
3. Run the script using Python:
   ```bash
   python FNF_bot_V2.py
   ```
4. The console will print `started`, and the bot will begin monitoring those pixel areas and pressing keys automatically.

> **Disclaimer:** Since the infinite loop (`while True:`) has no built-in keyboard listener to stop it gracefully, you may need to force-quit your terminal or move your mouse rapidly to a corner of the screen (triggering PyAutoGUI's failsafe) to stop the script.
