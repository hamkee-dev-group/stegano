# 🕵️‍♀️ Invisible Steganography Tool (HTML + JS)

This is a simple web-based steganography utility that lets you **hide messages invisibly inside plain text** using Unicode zero-width characters.

The entire app is built in pure HTML, CSS, and JavaScript — **no backend, no dependencies, no build system**.

---

## ✨ Features

- ✅ Encode a hidden message invisibly inside any visible text
- ✅ Decode and extract hidden messages from encoded text
- ✅ User-friendly web interface with two clean sections: **Encode** and **Decode**
- ✅ Copy-paste support for easy message sharing
- ✅ 100% client-side – your data never leaves your browser

---

## 🚀 How It Works

The tool uses two invisible Unicode characters:

| Bit | Unicode Character        | Code Point |
|-----|--------------------------|------------|
| 0   | Zero Width Space         | `U+200B`   |
| 1   | Zero Width Non-Joiner    | `U+200C`   |

These are inserted invisibly after characters in your carrier text to encode the binary representation of a hidden message.

---

## 📦 Usage

1. Open the `index.html` file in any modern browser
2. Navigate to the **Encode** tab:
   - Paste or type a **carrier text**
   - Enter the **message to hide**
   - Click `Encode`
   - Copy the encoded result using the `Copy` button
3. To reveal a hidden message:
   - Switch to the **Decode** tab
   - Paste the encoded text into the input box
   - Click `Decode` to reveal the original hidden message

---

## 🛡️ Security & Privacy

This is a **client-side only** tool. Everything runs locally in your browser.  
No data is ever sent over the network.

---

## 🛠️ Technical Notes

- Hidden messages are converted to binary (UTF-8) and embedded using zero-width characters.
- Remaining bits (if the carrier text is shorter than needed) are appended at the end.
- The tool works best in plaintext editors that **preserve Unicode characters**.
