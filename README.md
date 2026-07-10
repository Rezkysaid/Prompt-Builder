# PromptCraft — Prompt Builder

Macam Google Translate, tapi untuk prompt: translate prompt mentah / kabur / rojak kepada prompt yang jelas, spesifik dan berstruktur — supaya hasil daripada mana-mana AI (ChatGPT, Claude, Gemini, dll.) jadi jauh lebih bagus.

**Live app:** https://rezkysaid.github.io/Prompt-Builder/

## Dua mod (toggle atas)

App ada tiga kerja, tukar dengan toggle **✍️ Rangka Prompt │ 📖 Faham Output │ 🧭 Coach Socratic**:

- **Rangka Prompt** — semua ciri di bawah: buat prompt mentah jadi power.
- **📖 Faham Output** — malas/susah baca jawapan panjang dari ChatGPT/Claude/Gemini? Paste jawapan tu masuk sini, app ringkaskan jadi **Intinya (TL;DR) · Poin penting · Apa kau kena buat · Terang simple**, dalam BM santai yang senang telan — siap butang **Dengar** (TTS baca kuat-kuat) & Copy.
- **🧭 Coach Socratic** — ada AI power tapi tak tau nak buat apa (macam ada Lamborghini tapi tak tau nak pandu ke mana)? Coach tanya soalan reflektif satu-satu, gali sampai faham kau, lepas tu cadang 2-3 hala tuju konkrit yang kau boleh terus buat dengan AI (tap "jom mula" terus masuk Rangka Prompt). Ada butang **"cukup — bagi cadangan"** untuk skip, dan penjagaan rehat: nudge lembut kalau sesi lebih sejam + butang **"aku rasa serabut"** bila-bila. Setiap sembang auto-disimpan dalam **"sembang lama"** (localStorage) — klik untuk pulih & refer balik, padam individu.

## Ciri-ciri (Rangka Prompt)

- 🔁 **Dual-panel macam Google Translate** — prompt asal kiri, prompt enhanced kanan
- 🎛️ **6 mode enhancement** — General, Coding, Creative, Business, Image-Gen, Academic
- ✅ **Annotation** — senarai apa yang ditambah/diubah pada prompt asal (belajar sambil guna)
- 🌐 **Sokong bahasa rojak** — input Melayu, English atau campuran; bahasa output boleh pilih (Auto / MS / EN)
- 🎤 **Voice input** — malas/tak reti menulis? Tekan "Cakap", cakap je dalam BM/rojak dan app transkrip terus jadi teks input (Web Speech API, on-device; butang auto-sembunyi kalau browser tak sokong)
- ✍️ **Cadangan permulaan ayat** — stuck kat perkataan pertama? Bila kotak kosong, app tunjuk chips rawak cara nak mula ("Terangkan…", "Tolong aku…", "Macam ni weh…", "Sebenarnya…", "Aku nak cerita…"); tap satu, ia isi permulaan dan kau sambung je. Ada butang shuffle untuk cadangan lain, dan bila semua cadangan biasa dah dilihat, butang "AI bagi" muncul untuk minta AI jana pembuka baru
- 💡 **Hint masa taip** — sambil kau taip, app bagi nudge lembut apa yang kurang (untuk siapa? format hasil?) dan bagitau bila prompt dah cukup detail — ngajar kau jadi lebih pandai prompt. Tak muncul dalam mod "Kemas je"
- 🧹 **Intensiti: Kemas je** — pilihan untuk hanya susun ayat jadi kemas dan gramatis tanpa AI tambah konteks/format/andaian sendiri; sesuai bila kau nak AI tafsir sendiri niat prompt kau. Terpakai pada enhance utama dan follow-up sekali
- 💬 **Konteks perbualan** — satu kotak untuk bagitau apa kau tengah bincang dengan AI di tempat lain (ChatGPT/Claude/Gemini) & di mana perbualan tu dah sampai; app suntik konteks ni supaya prompt yang dibuat **berkait & sambung** dengan chat kau di sana, bukan topik baru. Suis on/off, animasi buka/tutup smooth, disimpan dalam browser; tak terpakai dalam mod "Kemas je"
- 🖼️ **Gambar rujukan** — lampirkan gambar masa rangka prompt (butang "Gambar" di panel input); AI (Gemini 3.5, multimodal) tengok gambar tu dan masukkan butiran visualnya ke dalam prompt supaya tak payah teka. Gambar di-resize kecil dulu (≤1024px) untuk laju; boleh enhance walau kotak teks kosong
- 🌱 **Seed grower** — malas taip panjang? Bagi frasa pendek/kasar (contoh: "buat duit dengan ai") dan AI tumbuhkan jadi 5 cadangan prompt penuh dengan angle berbeza, siap boleh copy atau terus "Guna ni" untuk power-kan lagi
- 🕘 **Sejarah prompt + kegemaran** — disimpan dalam browser (localStorage)
- 📋 Copy, Paste, Swap, Regenerate
- 🖼️ **Kongsi as image** — export prompt yang dah diperbaiki jadi kad gambar cantik berbrand (logo + tagline app) terus dari canvas; guna Web Share API kat mobile (share ke mana-mana app) atau download PNG kat desktop
- 🧵 **Thread follow-up** — prompt pertama untuk buka chat; lepas tu taip niat follow-up secara kasar dan PromptCraft craft prompt seterusnya yang bersambung dengan yang sebelumnya (tak ulang konteks, merujuk jawapan AI tadi) — sedia untuk paste dalam chat yang sama kat ChatGPT/Claude/Gemini. Seluruh thread disimpan dalam sejarah: klik balik item tu bila-bila dan sambung craft follow-up dengan konteks yang sama
- ↺ **Panggil balik soalan** — teks yang kau taip dalam kotak follow-up auto-simpan (kekal walaupun AI high-demand/limit atau app ditutup); butang "soalan tadi" munculkan balik soalan yang pernah kau taip supaya tak lupa apa yang pernah diajukan
- 📱 **PWA** — boleh install ke home screen (Add to Home Screen), ada offline shell melalui service worker

## Teknikal

- Satu fail `index.html` sahaja — static site, GitHub Pages friendly
- AI engine: Gemini melalui proxy Vercel sedia ada (`muhasabah-app.vercel.app/api/gemini`) — API key kekal selamat di server side, tidak terdedah dalam frontend
