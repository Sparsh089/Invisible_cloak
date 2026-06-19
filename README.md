# 🧥 Invisible Cloak — Harry Potter Style Magic with OpenCV

> "Turn any red cloth into a cloak of invisibility — straight out of Hogwarts, powered by Python."

Ever wanted to vanish into thin air like Harry Potter? This project uses **OpenCV** and a clever color-masking trick to make any **red-colored cloth disappear** from your webcam feed in real time — replaced seamlessly by the background behind you. No green screen studio, no VFX team. Just Python, your webcam, and a red cloth.

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![OpenCV](https://img.shields.io/badge/OpenCV-ComputerVision-green?logo=opencv)
![Status](https://img.shields.io/badge/Magic-Enabled-red)

---

## ✨ How the Magic Works

1. **Capture the background** — The camera first records a few frames of the empty scene (no you, no cloak) to remember what "should" be there.
2. **Detect the red cloak** — Every frame is converted to HSV color space and masked to isolate red pixels (the cloak).
3. **Clean up the mask** — Morphological operations (open + dilate) remove noise so the mask is smooth and solid.
4. **Swap pixels** — Wherever the cloak is detected, the original background is painted in. Everywhere else, the live frame is shown as-is.
5. **Poof!** ✨ — The cloak area blends perfectly with the background, making you (or whatever's under the cloth) disappear.

---

## 🛠️ Tech Stack

- **Python 3**
- **OpenCV** (`cv2`) — video capture, color space conversion, masking
- **NumPy** — array operations and frame flipping

---

## 🚀 Getting Started

### 1. Clone the repo
```bash
git clone https://github.com/<your-username>/Invisible_cloak.git
cd Invisible_cloak
```

### 2. Install dependencies
```bash
pip install opencv-python numpy
```

### 3. Run the magic
```bash
python Invisible_Cloak.py
```

### 4. Cast your spell 🪄
- Step **out of frame** for the first couple of seconds while the background is captured.
- Step back in wearing (or holding up) a **red cloth**.
- Watch yourself vanish in real time!
- Press **`Esc`** to exit the spell.

---

## 🎯 Tips for Best Results

| Tip | Why it matters |
|---|---|
| Use a **plain, solid red** cloth | Reduces false detections and gives cleaner edges |
| Keep the **background static** | The illusion only works if the background doesn't move |
| Ensure **good, even lighting** | Shadows can confuse the HSV color mask |
| Avoid **red objects** in the background | They'll vanish too! (unless that's the look you want 😉) |

---

## 🔮 Future Enhancements

- [ ] Support for **multiple colors** (blue, green cloaks)
- [ ] Auto-recalibration when background changes
- [ ] Save output as a video file
- [ ] Web-based demo using `streamlit` or `flask`

---

## 📜 License

Free to use, modify, and share. Go forth and disappear responsibly. 🧙‍♂️

---

<p align="center"><i>"It is our choices that show what we truly are, far more than our abilities."</i><br>— and apparently, our choice of cloth color.</p>
