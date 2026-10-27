# 🏕️ The Pi Academy: Florida Coding Camp Volunteer Training Manual

Welcome to **The Pi Academy**! Thank you for volunteering your time to mentor middle school students (ages 10–13 / grades 6–8) at our Florida youth coding camp.

This manual serves as the companion guide to the interactive training portal (`volunteer_training.html`).

---

## 🏛️ Module 1: Who is The Pi Academy?

### High-Level Mission & Vision ([www.thepiacademy.org](https://www.thepiacademy.org))
The Pi Academy is a non-profit organization dedicated to closing the digital divide and igniting computer science passion in young learners. We provide hands-on, high-engagement STEM camps that turn middle schoolers from passive screen users into creative programmers, game developers, robotics engineers, and problem solvers.

### Why Middle School?
Research shows that ages 10–13 are the formative years where students form their identities around STEM. By putting real microcomputers (Raspberry Pi), programmable drones, robotics, and game engines into their hands, we demystify technology and build lasting self-efficacy.

### ⭐ The Golden Rule for All Volunteers
> **"Never take the mouse or keyboard away from a camper."**
* Our core teaching pedagogy is **guided discovery**.
* If a student encounters an error or gets stuck, guide their eyes and fingers with questions:
  * *"What line number does the red error message point to?"*
  * *"Let's look at the end of that line together—do you see any missing quotes or parentheses?"*
  * *"What do you think happens if we change that variable?"*
* When a student types the solution themselves and sees it work, their confidence surges.

---

## ⏰ Module 2: The Camp Day Breakdown

The Florida camp runs for **5 hours total (4 hours of active seat time)** for ~15 middle school students:

| Time / Block | Camp Activity | Volunteer Responsibilities |
| :--- | :--- | :--- |
| **Hour 1 (45 min)** | **Welcome & Raspbian OS Exploration**<br>Peripherals unboxing, connecting monitors/mice, desktop tour, coding icebreaker. | Greet campers, ensure power (CanaKit 5V) and micro-HDMI cables are snug, guide first-time mouse and desktop navigation. |
| *15 min Break* | Snack & beverage break. | Sanitize surfaces, check hardware readiness. |
| **Hour 2 (60 min)** | **Scratch Programming**<br>Block-based programming, loops, conditionals, events, creating an interactive story. | Circulate room, encourage creative sprite choices, help connect logic blocks. |
| *30 min Lunch* | Pizza lunch break! 🍕 | Connect with campers, build team camaraderie, discuss their favorite video games and interests. |
| **Hour 3 (60 min)** | **Python & GoPiGo Robotics Intro**<br>Python in Thonny IDE, connecting to GoPiGo rover, driving forward, backward, turns. | Keep battery packs secure, clear floor paths, assist with Python syntax. |
| *15 min Break* | Snack & beverage break. | Reset drone batteries and clean floor courses. |
| **Hour 4 (60 min)** | **Interactive Station Rotations**<br>Specialized small-group stations: Drones, Pizza Delivery, Web Dev, Turtle Race, GoPiGo courses. | Staff assigned station, guide hands-on coding, manage pacing, challenge fast finishers. |
| **Hour 5 (45 min)** | **Wrap-up, Project Showcase & Demos**<br>Students show favorite projects to peers/parents, Q&A, certificates, next steps. | Help students prepare demo screens, cheer and applaud every camper, assist with teardown. |

---

## 🎪 Station-by-Station Volunteer Guides

---

### 🚁 Station 1: Drone Station (Tello EDU)

* **What it is**: An autonomous flight challenge where campers program a DJI Tello EDU drone using DroneBlocks on an iPad to fly from Table A to Table B.
* **Core Goals**:
  * Sequence commands in an exact algorithm.
  * Use physical tape measurements (inches) as code parameters.
  * Understand that climb blocks (`Fly Up 20 inches`) are additive above takeoff hover.
  * Debug flights based on observed landing drift.
* **The 4-Block Sequence**:
  1. `Takeoff` (firmware-controlled hover)
  2. `Fly Up • 20 inches` (additional climb)
  3. `Fly Forward • [Measured] inches` (e.g. 120 inches between table centers)
  4. `Land` (descends vertically to Table B)
* **Volunteer Duties & Safety (2 Volunteers Recommended)**:
  * **Volunteer A**: Oversees code creation on iPad.
  * **Volunteer B**: Supervises flight area, enforces safety boundaries, holds DroneBlocks abort control.
  * **Guided Access**: Connect iPad to `TELLO-xxxxxx` Wi-Fi, then triple-click top button to lock into DroneBlocks with Guided Access before handing to students.
  * **Safety Rule**: **Never let any camper reach for or catch a flying drone.** Wait until propellers stop completely.
  * **Student Roles**: Assign *Measurer*, *Programmer*, and *Observer*. Rotate roles each flight!

---

### 🍕 Station 2: Pizza Delivery Game (Pygame)

* **Repository**: [`The-Pi-Academy/pizza-delivery-game`](https://github.com/The-Pi-Academy/pizza-delivery-game)
* **What it is**: A medieval pizza delivery 2D platformer written in Python. The player attacks with a breadstick sword and fires pizza slices into delivery ovens using a pizza cannon. Levels 2 & 3 are intentionally impossible without editing code!
* **Core Goals**:
  * Demystify game development (Game Loop, physics, 2D vectors, collision).
  * Learn by breaking and modding Python code.
* **Launch Instructions**:
  ```bash
  cd ~/thepiacademy/pizza-delivery-game
  source venv/bin/activate
  python run.py
  ```
* **Volunteer Guide for Helping Campers**:
  * **Developer Mode (`M` key)**: Pressing `M` toggles an on-screen grid with exact (X, Y) coordinates. Remind campers: Pygame's origin (0,0) is top-left!
  * **Level 2 Wall**: Have campers open `levels/Level2.py` and delete line 21 (`tilemap.add_range(5, GROUND_Y, 5, 0, S)`) to open a path.
  * **Level 2 Pit Gap**: Add a platform bridge using: `tilemap.add_range(20, GROUND_ROW, 60, GROUND_ROW, G)`.
  * **Level 3 Jetpack & Gas Cans**: Add fuel cans by adding: `GasCan(15, -5)`.
  * **Emergency Fix ("We broke the game!")**: If syntax errors crash Python, run:
    ```bash
    git restore pathTo/MyFile.py   # or git reset --hard
    ```

---

### 💻 Station 3: Simple Website (HTML / CSS / JavaScript)

* **Repository**: [`The-Pi-Academy/simple-website`](https://github.com/The-Pi-Academy/simple-website)
* **What it is**: A self-contained, single-file (`index.html`) web development lab.
* **Core Goals**:
  * Understand the 3 pillars of the web:
    * **HTML**: The Skeleton (headings, paragraphs, buttons)
    * **CSS**: The Clothing (colors, backgrounds, fonts)
    * **JavaScript**: The Brains (button click events, DOM updates)
  * Introduce browser developer tools (Right-Click → *Inspect*).
* **Volunteer Progression**:
  1. Open `index.html` side-by-side in VS Code/Thonny and Chromium.
  2. Change `<h1>` to their own name (e.g., *"Maya's Florida Coding Hub"*). Save (`Ctrl+S`), reload browser (`Ctrl+R`).
  3. Change the `<style>` block: modify background colors, borders, and fonts.
  4. Teach *Inspect Element* on the browser.
  5. Edit the `<script>` tag at the bottom to alter button behavior.

---

### 🐢 Station 4: Turtle Race (Python Turtle Graphics)

* **Repository**: [`The-Pi-Academy/turtle-race`](https://github.com/The-Pi-Academy/turtle-race)
* **What it is**: An 11-racer animated competition comparing hardcoded code (`01-original.py`) with clean, modular code (`02-improved.py`).
* **Core Goals**:
  * Understand "Working Code" vs. "Well-Architected Code".
  * Learn how **Lists** store collections of data (e.g. `colors = [...]`).
  * Learn how **Functions** eliminate repetitive code.
  * See configurable variables in action.
* **Launch Instructions**:
  ```bash
  cd ~/thepiacademy/turtle-race
  python3 race.py    # or python3 02-improved.py
  ```
* **Volunteer Talking Points**:
  * Use the **LEGO analogy**: stacking random blocks stands up, but interlocking bricks allow you to build towers.
  * Challenge campers to add their favorite color (e.g., `'gold'`) to the `colors` list. Watch how the program dynamically creates an extra lane, draws numbered tracks, and celebrates the winner!

---

### 🤖 Station 5: GoPiGo Obstacle Course *(Robotics)*

* **What it is**: Physical robotic rover navigation through a taped or foam maze on the floor using Python motor control.
* **Core Goals**:
  * Program wheel speed, duration, and turn angles.
  * Use ultrasonic distance sensors to detect walls before crashing.
* **Volunteer Duties**:
  * Maintain safe floor boundaries and check battery levels.
  * Guide campers to measure course distances with tape measures before guessing motor seconds.
* *(Note: Specific course layout and API commands will be detailed once course dimensions are provided).*

---

### 📷 Station 6: GoPiGo Pi Photo *(Computer Vision & Camera)*

* **What it is**: Interfacing the Raspberry Pi Camera module mounted on GoPiGo to take snapshots, apply filters, or detect targets.
* **Core Goals**:
  * Understand digital cameras, preview windows, and image capture via Python.
  * Trigger photos through code commands or sensor interrupts.
* **Volunteer Duties**:
  * Verify camera ribbon cables are firmly seated.
  * Help campers find and view their saved photo files in the file manager.
* *(Note: Specific camera scripts and filter exercises will be detailed once finalized).*

---

## 🏆 Day 1 Volunteer Checklist

Before campers arrive:
1. [ ] Reviewed the Golden Rule: **Never touch the camper's keyboard or mouse**.
2. [ ] Reviewed the 5-hour camp schedule and station transitions.
3. [ ] Tested Guided Access and flight abort on the Drone Station iPad.
4. [ ] Know the Developer Mode shortcut (`M` key) in the Pizza Delivery Game.
5. [ ] Know how to run `git reset --hard` if a game script gets mangled.
6. [ ] Excited to encourage, inspire, and celebrate every Florida camper! 🎉
