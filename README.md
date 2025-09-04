# Animated Lightbulb Pixel Art 💡

A charming pixel art animation of a lightbulb that turns on and off with flickering light rays, created using **Python** and **OpenCV**.  

This project was developed as an **activity for COE190 – Emerging Technologies in Computer Engineering**.

---

## 📖 Description
This project creates a simple animated lightbulb using pixel art techniques. The animation cycles through three states:

1. **Off state** – A grayscale lightbulb  
2. **On state** – A bright yellow illuminated lightbulb  
3. **Flickering state** – The lightbulb with animated light rays that flicker around it  

The animation runs in a continuous loop, displaying the lightbulb turning on, flickering with rays, and then turning off again.

---

## ✨ Features
- **Pixel Art Style** – Hand-crafted 19×28 pixel grid artwork  
- **Smooth Animation** – Scaled up 20× for clear visibility (380×560 final resolution)  
- **Color Gradients** – Multiple shades of yellow for the "on" state and various grays for the "off" state  
- **Dynamic Light Rays** – Animated rays that flicker around the illuminated bulb  
- **Continuous Loop** – Seamless animation cycle  

---

## ⚙️ Requirements
- Python 3.x  
- OpenCV (`cv2`)  
- NumPy  

---

## 🛠 Installation
1. Clone or download this project.  
2. Install the required dependencies:  

```bash
pip install opencv-python numpy
```

---

## ▶️ Usage
Run the script:

```bash
python Jadman_art.py
```

The animation window will open and begin the lightbulb animation cycle.

---

## 🎮 Controls
- **ESC** or **Q** → Quit the animation
- The window automatically cycles through the animation states

---

## ⏱ Animation Timing
- **Off state** → 1 second
- **On state** → 0.5 seconds
- **Flickering with rays** → 6 flickers at 200ms each (1.2 seconds total)

---

## 🧩 How It Works
The animation uses a grid-based approach where each "pixel" in the art is represented by a number in a 2D array:

- `0` → Transparent/background (black)
- `1–6` → Different colors/shades used for the lightbulb and base

### 🔑 Key Components
- **Canvas Setup** – Creates a 380×560 white canvas (19×28 grid scaled by 20)
- **Color Palette** – Defines shades of yellow for the "on" state and grays for the "off" state
- **Pixel Drawing** – `draw_pixel()` function scales individual pixels to 20×20 rectangles
- **Animation States:**
  - `draw_off_light()` → Renders grayscale bulb
  - `draw_on_light()` → Renders illuminated bulb
  - `draw_rays()` → Adds flickering rays

---

## 🔍 Explanation of Pixel Scaling & Animation

### 🎨 Pixel Scaling
Pixel art is originally defined on a tiny grid (19×28 in this case). To make it visible on screen:

- Each "pixel" is scaled up by a factor (e.g., 20×).
- So instead of a single point, each pixel becomes a 20×20 block on the canvas.
- This ensures the artwork retains its blocky retro style while being clearly visible.

### 🎬 Animation
The animation is created by:

1. **Drawing frames** – Each state of the bulb (off, on, rays) is drawn separately.
2. **Timing control** – `cv2.waitKey()` is used to control how long each frame is displayed.
   - Example: 1000 ms for "off", 500 ms for "on", 200 ms per flicker.
3. **Looping** – The program continuously cycles through these frames, creating a smooth looping animation.
4. **Flicker effect** – Light rays are drawn and erased in quick succession to simulate natural flickering.

---

## 🎨 Customization
- **Colors** – Modify BGR color values at the top of the file
- **Timing** – Adjust `cv2.waitKey()` values to speed up or slow down the animation
- **Scaling** – Change the `scale` variable for larger/smaller pixels
- **New States** – Add new pixel art arrays and drawing functions

---

## 🌈 Color Palette
- **Yellow tones** – `dark_yellow`, `bright_yellow`, `mid_yellow`
- **Gray tones** – `dark_gray` to `super_light_gray`
- **Background** – Black (transparent), White (canvas)

---

## 📂 File Structure
```
Jadman_art.py    # Main animation script
README.md        # Project documentation
```

---

## 👤 Author
Created by **Jadman** – A simple pixel art animation project for **COE190 – Emerging Technologies in Computer Engineering**.

---

## 📜 License
This project is open source and available for personal and educational use.

---

✨ **Enjoy watching the lightbulb come to life!** 💡
