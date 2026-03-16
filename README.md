# 📋 ClipCopy

A clean, lightweight clipboard utility web app that lets you type or paste text and copy it to your clipboard — preserving every line break, indentation, tab, and number **exactly** as written.

![HTML](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![No Dependencies](https://img.shields.io/badge/dependencies-none-brightgreen?style=flat)

---

## ✨ Features

- **Exact Copy** — preserves all newlines, spaces, tabs, and formatting as-is
- **Live Line Numbers** — line numbers update in real time as you type
- **Live Stats** — shows character and line count in the toolbar
- **Tab Support** — pressing `Tab` inserts a real tab character instead of shifting focus
- **Clear Button** — one click to wipe the editor
- **Toast Notifications** — instant feedback when text is copied or cleared
- **Empty State Warning** — shakes the editor and warns if there's nothing to copy
- **Fallback Copy** — uses `execCommand` for older browser compatibility
- **No Dependencies** — pure HTML, CSS, and JavaScript; no frameworks or libraries needed

---

## 🖥️ Preview

> Light blue & white theme with a code-editor-style textarea featuring line numbers, toolbar stats, and a gradient copy button.

---

## 🚀 Getting Started

### Option 1 — Open directly in browser

Just download `clipboard.html` and open it in any modern browser. No server required.

```bash
# Clone the repository
git clone https://github.com/your-username/your-repo.git

# Navigate into the folder
cd your-repo

# Open in browser (macOS)
open clipboard.html

# Open in browser (Linux)
xdg-open clipboard.html

# Open in browser (Windows)
start clipboard.html
```

### Option 2 — Serve locally

```bash
# Using Python
python -m http.server 8000

# Then visit
http://localhost:8000/clipboard.html
```

---

## 📁 Project Structure

```
your-repo/
└── clipboard.html    # Single self-contained file (HTML + CSS + JS)
```

---

## 🛠️ How It Works

| Step | Action |
|------|--------|
| 1 | User types or pastes text into the editor |
| 2 | Line numbers and stats update live |
| 3 | User clicks **Copy to Clipboard** |
| 4 | `navigator.clipboard.writeText()` copies the raw `textarea.value` |
| 5 | A toast notification confirms the copy |

The key to exact-copy behavior is using `white-space: pre` on the textarea and copying `textarea.value` directly (without `.trim()` or any transformation), so every character — including leading spaces, blank lines, and tab indents — is preserved faithfully.

---

## 🌐 Browser Support

| Browser | Support |
|---------|---------|
| Chrome 66+ | ✅ Full |
| Firefox 63+ | ✅ Full |
| Edge 79+ | ✅ Full |
| Safari 13.1+ | ✅ Full |
| Older browsers | ✅ Fallback via `execCommand` |

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

## 🙌 Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you'd like to change.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/my-feature`)
3. Commit your changes (`git commit -m 'Add my feature'`)
4. Push to the branch (`git push origin feature/my-feature`)
5. Open a Pull Request

---

*Built with ❤️ using vanilla HTML, CSS & JavaScript.*
