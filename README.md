# PromptCraft — Prompt Builder

Macam Google Translate, tapi untuk prompt: translate prompt mentah / kabur / rojak kepada prompt yang jelas, spesifik dan berstruktur — supaya hasil daripada mana-mana AI (ChatGPT, Claude, Gemini, dll.) jadi jauh lebih bagus.

**Live app:** https://rezkysaid.github.io/Prompt-Builder/

## Ciri-ciri

- 🔁 **Dual-panel macam Google Translate** — prompt asal kiri, prompt enhanced kanan
- 🎛️ **6 mode enhancement** — General, Coding, Creative, Business, Image-Gen, Academic
- ✅ **Annotation** — senarai apa yang ditambah/diubah pada prompt asal (belajar sambil guna)
- 🌐 **Sokong bahasa rojak** — input Melayu, English atau campuran; bahasa output boleh pilih (Auto / MS / EN)
- 🎴 **Dek kad idea** — 36 topik rawak pelbagai kategori untuk diteroka dengan Claude/ChatGPT/Gemini bila buntu; satu klik terus masuk ke panel input
- 🕘 **Sejarah prompt + kegemaran** — disimpan dalam browser (localStorage)
- 📋 Copy, Paste, Swap, Regenerate
- 📱 **PWA** — boleh install ke home screen (Add to Home Screen), ada offline shell melalui service worker

## Teknikal

- Satu fail `index.html` sahaja — static site, GitHub Pages friendly
- AI engine: Gemini melalui proxy Vercel sedia ada (`muhasabah-app.vercel.app/api/gemini`) — API key kekal selamat di server side, tidak terdedah dalam frontend
