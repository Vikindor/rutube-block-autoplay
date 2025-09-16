# Rutube - Block Autoplay

Userscript that prevents videos on **Rutube** from starting automatically.  
Works both on regular video pages and embedded players.

## ✨ Features
- Stops autoplay on Rutube video pages.
- Disables autoplay in embedded Rutube players.
- Overrides the native `video.play()` method to block the first automatic play attempt.

## 🔧 Installation
1. Install [Tampermonkey](https://www.tampermonkey.net/) (or another userscript manager).
2. Install the script from one of the mirrors:
   - [GreasyFork](https://greasyfork.org/en/scripts/544729-rutube-block-autoplay/)
   - [OpenUserJS](https://openuserjs.org/scripts/Vikindor/Rutube_-_Block_Autoplay)
   - Or [install directly from this repository](./Rutube_-_Block_Autoplay.js).

## ⚙️ How it works
- The script waits until a `<video>` element appears.
- It forces `autoplay` to `false` and removes the `autoplay` attribute.
- On the first call to `video.play()`, it rejects the promise to prevent autoplay.  
  Any further manual play calls will work normally.

---

Made to keep Rutube quiet until *you* decide to press play.