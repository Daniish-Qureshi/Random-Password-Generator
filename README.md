# 🔐 Random Password Generator

A clean and instant Random Password Generator built with pure HTML, CSS, and JavaScript. Generate a strong random password in one click and copy it to clipboard with the copy icon — no signup, no backend, deployed live on Vercel.

## 🌐 Live Demo

🔗 **[random-password-generator-ten-rosy.vercel.app](https://random-password-generator-ten-rosy.vercel.app)**

---

## ✨ Features

- 🎲 **Random Password Generation** — Click "Generate The Password" and instantly get a strong random password
- 📋 **One-Click Copy** — Copy icon button copies the password straight to your clipboard
- 🔡 **Mixed Characters** — Password includes uppercase, lowercase, numbers, and special symbols
- ⚡ **Instant Result** — No page reload, no API call — all client-side
- 📱 **Fully Responsive** — Works on mobile, tablet, and desktop
- 🪶 **Zero Dependencies** — Pure vanilla JavaScript, no libraries needed

---

## 🗂️ Project Structure

```
Random-Password-Generator/
│
├── Assets/
│   ├── copy.png        # Copy to clipboard icon button
│   └── generate.png    # Icon inside the Generate button
│
├── index.html          # Password display field, copy icon, generate button
├── style.css           # Card layout, input box, button styling, responsive
└── script.js           # createPassword() + copyPassword() logic
```

---

## ⚙️ How It Works

```
User clicks "Generate The Password"
              ↓
createPassword() is called
              ↓
JS defines a character set:
  uppercase (A-Z) + lowercase (a-z)
  + numbers (0-9) + symbols (!@#$%^&*)
              ↓
Loop picks random characters using Math.random()
              ↓
Password string displayed in the input field
              ↓
User clicks the copy icon
              ↓
copyPassword() calls navigator.clipboard.writeText()
              ↓
Password is copied to clipboard ✅
```

---

## 🧮 Core Logic

```javascript
function createPassword() {
  const chars =
    "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789!@#$%^&*";
  let password = "";
  for (let i = 0; i < 12; i++) {
    password += chars[Math.floor(Math.random() * chars.length)];
  }
  document.getElementById("Password").value = password;
}

function copyPassword() {
  const password = document.getElementById("Password").value;
  navigator.clipboard.writeText(password);
}
```

---

## 🛠️ Tech Stack

| Technology | Usage |
|------------|-------|
| **HTML5** | Input field, copy icon, generate button |
| **CSS3** | Card layout, password display box, responsive styling |
| **JavaScript (Vanilla)** | `Math.random()`, `navigator.clipboard`, DOM updates |
| **Vercel** | Deployment & hosting |

---

## 💡 Key Concepts Demonstrated

- **`Math.random()` + `Math.floor()`** — Core of random character selection
- **String Concatenation Loop** — Building the password character by character
- **`navigator.clipboard.writeText()`** — Modern Clipboard API for one-click copy
- **Character Set Design** — Combining multiple character types for password strength
- **DOM Manipulation** — Reading and writing to input field value
- **`onclick` Event Handling** — Triggering functions from HTML button attributes

---

## 🔒 Password Strength Breakdown

| Character Type | Example Characters |
|----------------|--------------------|
| Uppercase | `A B C ... Z` |
| Lowercase | `a b c ... z` |
| Numbers | `0 1 2 ... 9` |
| Special Symbols | `! @ # $ % ^ & *` |

> Combining all 4 types significantly increases password entropy, making it much harder to crack.

---

## 🚀 Getting Started

### Run Locally

1. **Clone the repository**
   ```bash
   git clone https://github.com/Daniish-Qureshi/Random-Password-Generator.git
   ```

2. **Navigate into the project folder**
   ```bash
   cd Random-Password-Generator
   ```

3. **Open in browser**
   ```
   Open index.html directly in your browser
   — or use Live Server (VS Code extension)
   ```

> ✅ No API keys, no npm, no setup — just open and generate!

---

## 📱 Responsive Design

| Screen | Behavior |
|--------|----------|
| **Mobile** | Full-width centered card, large generate button |
| **Tablet** | Comfortable card width with padding |
| **Desktop** | Centered card with clean spacing and hover effects |

---

## 👨‍💻 Author

**Danish Qureshi**  
BCA Final Year Student | Full Stack Developer  
📍 Dadri, Uttar Pradesh, India  
🔗 [GitHub — @Daniish-Qureshi](https://github.com/Daniish-Qureshi)  
🌐 [Portfolio](https://danish-qureshi-6ew5.vercel.app)

---

## 📄 License

This project is open source and free to use for **educational & portfolio purposes**.

---

⭐ If you found this useful, give it a **star** on GitHub!
