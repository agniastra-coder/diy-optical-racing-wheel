# 🏎️ DIY Optical-Encoder Sim Racing Wheel & HID Controller

A custom-built sim-racing steering wheel and paddle-shifter controller engineered using an optical mouse sensor, microswitches, and a Python virtual-gamepad feeder (`ViGEmBus` / `vJoy`) for *BeamNG.drive* and *Car Parking Multiplayer 2*.

![Hardware Setup]

https://github.com/user-attachments/assets/ea0613c6-beee-4aec-bf5a-b80843b3ce39


---

### ⚙️ How It Works
1. **Optical Steering Axis:** Tracks rotational wheel movement via a high-DPI optical mouse sensor mounted to the steering shaft.
2. **HID Device Isolation:** Separates the wheel's raw mouse input stream from the primary desktop mouse so cursor movement never interferes with gameplay.
3. **Virtual Gamepad Translation (`wheel-script.py`):** Captures raw X-axis optical deltas in real time, applies dynamic sensitivity curves, smoothing, and auto-centering logic, and feeds them into a virtual Xbox 360 controller via **ViGEmBus**.
4. **Tactile Paddle Shifters:** Microswitch-based upshift/downshift paddles wired for crisp, zero-debounce gear changes.

---

### 🛠️ Tech Stack & Hardware
* **Software:** Python (`vgamepad` / `ViGEmBus`, `inputs` / raw HID APIs), C++ (Arduino firmware)
* **Hardware:** Optical Mouse Sensor, Microswitches, Arduino Uno, Custom Mechanical Housing
* **Tested On:** Windows 11 (*BeamNG.drive*, *Car Parking Multiplayer 2*)

---

### 🚀 Setup & Usage
1. Install the **ViGEmBus** driver (Windows) and required Python packages:
   ```bash
   pip install vgamepad inputs
