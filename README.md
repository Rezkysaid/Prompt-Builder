# PromptCraft — Prompt Builder

Macam Google Translate, tapi untuk prompt: translate prompt mentah / kabur / rojak kepada prompt yang jelas, spesifik dan berstruktur — supaya hasil daripada mana-mana AI (ChatGPT, Claude, Gemini, dll.) jadi jauh lebih bagus.

**Live app:** https://rezkysaid.github.io/Prompt-Builder/

## Ciri-ciri

- 🔁 **Dual-panel macam Google Translate** — prompt asal kiri, prompt enhanced kanan
- 🎛️ **6 mode enhancement** — General, Coding, Creative, Business, Image-Gen, Academic
- ✅ **Annotation** — senarai apa yang ditambah/diubah pada prompt asal (belajar sambil guna)
- 🌐 **Sokong bahasa rojak** — input Melayu, English atau campuran; bahasa output boleh pilih (Auto / MS / EN)
- 🧹 **Intensiti: Kemas je** — pilihan untuk hanya susun ayat jadi kemas dan gramatis tanpa AI tambah konteks/format/andaian sendiri; sesuai bila kau nak AI tafsir sendiri niat prompt kau. Terpakai pada enhance utama dan follow-up sekali
- 🧭 **Wizard "blank tak tahu nak mula?"** — untuk yang stress tak tahu macam mana nak interact dengan AI: jawab 4 soalan klik-klik (nak tolong apa, pasal apa, apa hasil akhir, gaya bahasa) dan app bina prompt permulaan secara automatik — termasuk arahan supaya AI tanya soalan dulu sebelum jawab. Tiada kos API
- 🎴 **Dek kad idea** — 36 topik rawak pelbagai kategori untuk diteroka dengan Claude/ChatGPT/Gemini bila buntu; satu klik terus masuk ke panel input. Bila semua 36 habis, AI pula jana idea baru secara automatik (batch 5 seklik untuk jimat API)
- 🕘 **Sejarah prompt + kegemaran** — disimpan dalam browser (localStorage)
- 📋 Copy, Paste, Swap, Regenerate
- 🧵 **Thread follow-up** — prompt pertama untuk buka chat; lepas tu taip niat follow-up secara kasar dan PromptCraft craft prompt seterusnya yang bersambung dengan yang sebelumnya (tak ulang konteks, merujuk jawapan AI tadi) — sedia untuk paste dalam chat yang sama kat ChatGPT/Claude/Gemini. Seluruh thread disimpan dalam sejarah: klik balik item tu bila-bila dan sambung craft follow-up dengan konteks yang sama
- ↺ **Panggil balik soalan** — teks yang kau taip dalam kotak follow-up auto-simpan (kekal walaupun AI high-demand/limit atau app ditutup); butang "soalan tadi" munculkan balik soalan yang pernah kau taip supaya tak lupa apa yang pernah diajukan
- 📱 **PWA** — boleh install ke home screen (Add to Home Screen), ada offline shell melalui service worker

## Teknikal

- Satu fail `index.html` sahaja — static site, GitHub Pages friendly
- AI engine: Gemini melalui proxy Vercel sedia ada (`muhasabah-app.vercel.app/api/gemini`) — API key kekal selamat di server side, tidak terdedah dalam frontend
