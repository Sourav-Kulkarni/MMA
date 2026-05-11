# ⚔️ Kali Training Documentation

Personal MkDocs-powered training journal for Filipino Martial Arts (Kali / Arnis / Eskrima).

---

## Prerequisites

- Python 3.8 or higher
- pip (Python package manager)

Check your versions:

```bash
python --version
pip --version
```

---

## Installation

### 1. Clone or download this project

```bash
git clone <your-repo-url>
cd kali-training
```

### 2. (Recommended) Create a virtual environment

```bash
python -m venv venv

# Activate on Linux/macOS
source venv/bin/activate

# Activate on Windows
venv\Scripts\activate
```

### 3. Install all dependencies

```bash
pip install -r requirements.txt
```

---

## Running Locally

```bash
mkdocs serve
```

Then open your browser at: **http://127.0.0.1:8000**

The site auto-reloads when you edit any file — great for live editing during training prep.

---

## Building for Static Deployment

```bash
mkdocs build
```

Output goes to the `site/` folder. You can host this on GitHub Pages, Netlify, or any static host.

### GitHub Pages (one command)

```bash
mkdocs gh-deploy
```

---

## Project Structure

```
kali-training/
├── docs/
│   ├── index.md                  # Home / dashboard
│   ├── fundamentals/
│   │   ├── index.md              # Fundamentals overview
│   │   ├── stances.md            # Fighting stances & footwork
│   │   ├── grips.md              # Weapon grips
│   │   └── striking-angles.md   # The 12 angles of attack
│   ├── weapons/
│   │   ├── index.md              # Weapons overview
│   │   ├── single-stick.md      # Single olisi / baston
│   │   ├── double-stick.md      # Doble olisi
│   │   └── knife.md              # Daga (knife)
│   ├── drills/
│   │   ├── index.md              # Drills overview
│   │   ├── sinawali.md           # Sinawali weaving patterns
│   │   ├── sombrada.md           # Sombrada flow drills
│   │   └── sparring.md          # Sparring protocols
│   ├── conditioning/
│   │   ├── index.md              # Conditioning overview
│   │   ├── warmup.md             # Warm-up routine
│   │   ├── strength.md           # Strength & power training
│   │   └── recovery.md          # Recovery & injury prevention
│   └── resources/
│       ├── index.md              # Resources & references
│       ├── glossary.md           # Kali terminology glossary
│       └── lineage.md            # System lineage & history
├── overrides/                    # MkDocs theme overrides
├── docs/stylesheets/
│   └── extra.css                 # Custom styles
├── mkdocs.yml                    # MkDocs configuration
├── requirements.txt              # Python dependencies
└── README.md                     # This file
```

---

## Adding GIFs / Visual Aids

Place your GIFs inside `docs/assets/gifs/` and reference them in any markdown file:

```markdown
![Angle 1 Strike](../assets/gifs/angle1-strike.gif)
```

**Tips for low-resource, high-framerate GIFs:**
- Use [Gifski](https://gif.ski/) for high quality at small file sizes
- Target 15–24 fps for smooth motion
- Keep dimensions at 480–640px wide
- Use [ffmpeg](https://ffmpeg.org/) to convert video clips:

```bash
ffmpeg -i clip.mp4 -vf "fps=20,scale=480:-1:flags=lanczos,split[s0][s1];[s0]palettegen[p];[s1][p]paletteuse" output.gif
```

---

## Editing Tips

- All content is plain **Markdown** — edit any `.md` file in `docs/`
- Use **admonition blocks** for tips, warnings, and notes (see existing pages for examples)
- Use **tabbed content** to separate beginner / advanced variants of techniques
- The site supports **search** out of the box — every technique is instantly findable

---

## License

Personal use. Train hard. 🥋
