<div align="center">

# 🌀 Spinning Circle Login

A modern login UI with an animated ring of ticks that spins around the card on submit.

**Vanilla HTML · CSS · JavaScript — zero dependencies**

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)

</div>

---

## 📸 Preview

A dark-themed login card centered inside a radial ring of glowing tick marks. The ring stays still while the user types, then spins on submit to simulate a loading state.

> 💡 Add a screenshot or GIF here: `![preview](https://raw.githubusercontent.com/shirinmohajeri/Spinning-Circle-Login/refs/heads/main/Spinning%20Circle%20Login.jpg)`

---

## ✨ Features

- **Floating label inputs** — labels shrink and float above the field on focus/fill (Email & Password)
- **Animated tick ring** — a CSS-driven circular ring made of individual tick marks positioned with `transform` and CSS custom properties (`--i`)
- **Submit-triggered animation** — the ring is paused by default and only spins while the login request is "in progress," toggled via a `loading` class on form submit
- **Pill-shaped inputs & button** with a soft blue glow theme
- **Fully responsive centering** using Flexbox

---

## 🛠️ Tech Stack

| Layer | Details |
|---|---|
| Markup | HTML5 |
| Styling | CSS3 — custom properties, keyframe animations, `:focus-within` / `:not(:placeholder-shown)` |
| Behavior | Vanilla JavaScript — form submit handling |

---

## ⚙️ How It Works

- Each tick (`<span class="tick">`) is placed around the ring using a rotation formula: **360° ÷ number of ticks**
- A `tick-pulse` keyframe animation staggers the opacity of each tick with `animation-delay`, creating a sweeping glow effect
- On form submit, JavaScript adds a `.loading` class to the container, setting `animation-play-state: running` on the ticks — removed again once the (simulated) login process completes

### Quick Reference — Tick Count vs. Rotation Angle

| Total Ticks | Degree per Tick |
|:---:|:---:|
| 12 | 30deg |
| 16 | 22.5deg |
| 24 | 15deg |
| 36 | 10deg |
| 48 | 7.5deg |

> ⚠️ Above ~36 ticks, reduce `.tick` width (e.g. `2px`) to avoid overlap.

---

## 🚀 Getting Started

```bash
git clone https://github.com/shirinmohajeri/spinning-login.git
```

Then just open `index.html` in your browser — no build step, no dependencies.

---

## 📁 Project Structure

```
spinning-login/
├── index.html
├── style.css
└── README.md
```

---

## 🎨 Customization

| Want to change... | Edit this |
|---|---|
| Ring size | `margin-top` and `transform-origin` in `.tick` |
| Number of ticks | Add/remove `.tick` spans + recalculate angle (`360 / count`) |
| Tick thickness/length | `width` and `height` in `.tick` |
| Color theme | `#60a5fa` / `#3b82f6` blue accents |
| Spin trigger | JS `submit` event listener (currently simulated with `setTimeout`) |

---

## 👤 Author

**Shirin Mohajeri**
[GitHub](https://github.com/shirinmohajeri) · [LinkedIn](https://www.linkedin.com/in/shirin-mohajeri)
