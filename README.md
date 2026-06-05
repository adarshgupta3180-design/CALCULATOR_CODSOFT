# Pro Calculator

A professional-grade, modern desktop calculator application written in Python using the `tkinter` GUI framework. This project follows industry-standard software engineering practices, including modular design, visual micro-interactions, JSON persistence, error handling, and a full unit test suite.

It is designed to resemble a premium desktop utility (such as macOS Calculator or Windows Dark Mode Calculator) suitable for internship project submissions.

---

## 🌟 Key Features

- **Core Mathematical Operations:** Supports Addition, Subtraction, Multiplication, Division, Decimal numbers, Percentage, and Unary Square Roots.
- **Dynamic Font Scaling:** The display automatically scales down its font size as you type larger numbers, preventing text truncation or layout breakages.
- **Robust Mathematical Engine:** Implements correct mathematical order of operations (MDAS) and resolves float arithmetic inaccuracies (e.g. `0.1 + 0.2 = 0.3`).
- **Rich Visual Aesthetics:** Styled with a premium HSL-based dark palette, flat design aesthetics, clear grid spacing, and mouse hover states.
- **Persistent Calculation History:** Displays a scrollable history sidebar which loads past logs from a persistent `history.json` file. Clicking a history item restores its value, and history can be cleared.
- **Full Keyboard Support:** Standard numbers and operator keys are bound to calculator inputs.
- **Micro-Interactions:** Typing on the physical keyboard triggers a visual flash animation on the UI buttons to provide immediate feedback.
- **Error Handling:** Gracefully handles invalid operations like division by zero or square root of negative numbers with clear visual messages (e.g. `"Cannot divide by zero"`).
- **Responsive Layout:** The grid structure adjusts dynamically to window resizing, ensuring a pixel-perfect display at any size.

---

## 📁 Professional Folder Structure

```text
calculator/
│
├── calculator/
│   ├── __init__.py
│   ├── config.py          # Colors, fonts, layout, and keyboard bindings
│   ├── engine.py          # State machine and mathematical calculation logic
│   ├── storage.py         # JSON serialization/deserialization of history log
│   │
│   └── gui/
│       ├── __init__.py
│       ├── app.py         # Main window coordinator and event listener
│       ├── display.py     # Dual-line output screen with auto font scaling
│       ├── keypad.py      # Flat interactive grid of buttons
│       └── history_panel.py # Sidebar display showing calculation history
│
├── tests/
│   ├── __init__.py
│   └── test_engine.py     # Unit test suite verifying core engine logic
│
├── README.md              # Detailed documentation
├── requirements.txt       # Dependencies listing (standard library + dev tools)
├── run.py                 # Convenience script to launch the app
└── history.json           # Local persistent JSON history database (auto-generated)
```

---

## 🚀 Installation & Running

### Prerequisites

- **Python 3.8 or higher** (Python comes packaged with `tkinter` on Windows and macOS).

### 1. Download/Clone the Project
Navigate to the root directory where the files are located:
```bash
cd d:/CODSOFT/CALCULATOR
```

### 2. Run the Application
You can run the application by executing the convenience script `run.py` at the root directory:
```bash
python run.py
```
*(On Windows systems where Python is configured with the launcher shortcut, you can also run `py run.py` or double-click `run.py` in your File Explorer).*

---

## ⌨️ Keyboard Shortcuts

| Keyboard Key | Calculator Action |
| :--- | :--- |
| `0` - `9` | Appends digits |
| `.` | Appends decimal |
| `+`, `-` | Addition, Subtraction |
| `*`, `/` | Multiplication, Division |
| `%` | Computes percentage |
| `Enter` or `=` | Evaluates expression |
| `Backspace` | Removes last digit |
| `Escape` | Clears all |

---

## 🧪 Running Automated Tests

A comprehensive unit test suite is included to verify the state machine and edge cases (division by zero, decimal precision, percent logic, negative square roots).

To run the tests, execute:
```bash
python -m unittest discover -s tests
```
*(or `py -m unittest discover -s tests`)*
