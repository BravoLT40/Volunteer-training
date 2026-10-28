# 🏕️ The Pi Academy: Florida Coding Camp Volunteer Training Manual

Welcome to **The Pi Academy**! Thank you for volunteering your time to mentor middle school students (ages 10–13 / grades 6–8) at our Florida youth coding camp.

This manual serves as the companion guide to the interactive training portal (`volunteer_training.html`).

---

## 🏛️ Module 1: Who is The Pi Academy?

### High-Level Mission & Goals ([www.thepiacademy.org](https://www.thepiacademy.org))
* **Mission:** To empower underrepresented youth to pursue careers in technology by providing accessible, engaging, and culturally relevant coding education and mentorship.
* **Goals:** To inspire and equip underrepresented youth to become the next generation of tech leaders and innovators, driving positive change in our community and beyond.

### The Flagship Program (Ages 10–13)
The **Raspberry Pi Youth Coding Camp** is The Pi Academy's flagship program for middle school students. We teach students how to transition from passive consumers of tech to creative programmers, hardware makers, and problem solvers.
* **Take-Home Tech:** Every camper takes home a complete Raspberry Pi computer desktop—including a monitor, keyboard, and mouse—so they can continue learning and creating beyond camp.

### 🤝 Your Role as a Mentor: Creating Belonging
Volunteers are mentors who show every student that they belong in STEM:
* **Learn names & ask about interests:** Connect coding concepts to things they love (gaming, sports, art, music, community).
* **Connect activities to real tech careers:** Highlight how camp skills power robotics, game dev, cybersecurity, and web engineering.
* **Foster genuine belonging:** Ensure every student leaves thinking: *"I can do this, and there is a place for me in technology."*

### ⭐ Hands-On Mentoring: Let Campers Lead
> **"Let campers lead whenever possible. Use questions and hints to help them work through coding challenges. When direct assistance is needed, explain what you are doing, ask permission before taking control, and return control promptly."**
* **Learning Challenge vs. Technical Issue:** Distinguish between a learning challenge (bugs, typos, logic hurdles—guide through questions) and a technical blocker (dropped Wi-Fi, hardware disconnect—step in transparently with permission to fix the blocker so they can keep participating).

---

## 🍓 Module 2: An Introduction to Raspberry Pi

* **Instructor Resource**: [View or Download the Raspberry Pi Instructor Guide](https://drive.google.com/file/d/1d0jFbc3oOhCBlEKkXcG-2RKTL-tpBdtu/view?usp=sharing) (PDF)
* **What is a Raspberry Pi**: A small, credit-card sized single-board computer with processor, memory, USB ports, and HDMI output. Allows campers to learn both software (programming) and hardware (electronics).
* **Station Hardware Checklist**:
  * Raspberry Pi 4 or 5 board
  * 32GB MicroSD Card (the Pi's "hard drive" containing the OS and user files)
  * Official USB-C power supply (minimum 3A for Pi 4, 5A for Pi 5)
  * Monitor with micro-HDMI to HDMI cable (always connect to **HDMI0**, closest to the USB-C power port)
  * USB Keyboard and Mouse
  * Protective case / cooling
* **Setup & Boot Steps**:
  1. *Flash OS*: Use **Raspberry Pi Imager** on computer → Select device & 64-bit Raspberry Pi OS.
  2. *Pre-configure Settings (Gear icon)*: Set username/password (avoid default `pi/raspberry`) and configure camp Wi-Fi.
  3. *Connect Peripherals First*: MicroSD card, micro-HDMI into HDMI0, keyboard, mouse.
  4. *Power On*: Plug in power supply last. The board powers on automatically into the desktop.
* **Key Volunteer Troubleshooting**:
  * *Black screen*: Verify micro-HDMI is in **HDMI0** (not HDMI1) and power supply is firmly seated.
  * *Rainbow icon / Lightning bolt*: Low voltage warning! Power supply does not supply adequate current (needs 3A/5A).
  * *"Command not found"*: Linux terminal commands are strictly case-sensitive. Check spelling or update with `sudo apt update`.
  * *Wi-Fi issues*: Check network icon in top-right taskbar or reboot the board.

---

## ⏰ Module 3: The Camp Day Breakdown

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

* **Instructor Resource**: [View or Download the Drone Station Instructor Guide](https://drive.google.com/file/d/1UVqs8tgtNY4hx84DvPaDvKj8sgua7sPZ/view?usp=drive_link) (PDF)
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

* **Instructor Resource**: [View or Download the Pizza Delivery Game Lesson Plan](https://drive.google.com/file/d/1ixqBf37FoFb550ygyyUYX42IoUYgnn62/view?usp=sharing) (PDF)
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

* **Instructor Resource**: [View or Download the Simple Website Lesson Plan](https://drive.google.com/file/d/19TgsjZD--jXBhG-piWo6UkMxyPPtps7b/view?usp=sharing) (PDF)
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

* **Instructor Resource**: [View or Download the Turtle Race Lesson Plan](https://drive.google.com/file/d/1Uhr-kBBBcE6Sw1SUIUrXFXjiN_31nCfV/view?usp=sharing) (PDF)
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
1. [ ] Reviewed Mentoring Guideline: **Let campers lead whenever possible** (ask permission before touching mouse/keyboard, explain actions, return control promptly).
2. [ ] Verified Raspberry Pi hardware: Micro-HDMI connected to **HDMI0**, official 3A/5A power, and SD cards seated.
3. [ ] Reviewed the 5-hour camp schedule and station transitions.
4. [ ] Tested Guided Access and flight abort on the Drone Station iPad.
5. [ ] Know the Developer Mode shortcut (`M` key) in the Pizza Delivery Game.
6. [ ] Know how to run `git restore` or `git reset --hard` if game code crashes.
7. [ ] Excited to encourage, inspire, and celebrate every Florida camper! 🎉
