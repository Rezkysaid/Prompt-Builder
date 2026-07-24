# PromptCraft — Prompt Builder

Toolkit ringkas untuk kerja dengan AI: tumbuhkan idea/prompt daripada frasa pendek, ringkaskan jawapan AI yang panjang supaya senang faham, cari idea use-case AI, dan chat AI am — semua dalam satu app kecil.

**Live app:** https://rezkysaid.github.io/Prompt-Builder/

## Tiga mod (toggle atas)

App ada tiga kerja, tukar dengan toggle ikon+teks **✍️ Prompt │ 📖 fahami │ 🧭 ilham**:

- **✍️ Prompt (Seed grower)** — tak ada idea nak taip? Bagi frasa pendek/kasar (contoh: "buat duit dengan ai") dan AI tumbuhkan jadi **5 cadangan prompt penuh** dengan angle berbeza, siap boleh **Copy** dan terus paste ke mana-mana AI tool (ChatGPT/Claude/Gemini). Ada pilihan bahasa output (Auto / MS / EN)
- **📖 Faham Output** — malas/susah baca jawapan panjang dari ChatGPT/Claude/Gemini? Paste jawapan tu masuk sini, app ringkaskan jadi **Intinya (TL;DR) · Poin penting · Apa kau kena buat · Terang simple**, dalam BM santai yang senang telan — siap butang **Dengar** (TTS baca kuat-kuat) & Copy. Tiga alat bantu fokus masa baca: **Fokus** (mod spotlight — blok yang kau tengah baca terang, yang lain jadi kelabu; tap untuk gerak fokus), **Bionik** (bionic reading — bold permulaan tiap perkataan supaya mata lekat & baca laju), dan **checklist** untuk "apa kau kena buat" (tick step yang dah siap, progress nampak). Copy & Dengar tetap ambil teks asal walaupun Bionik on
- **🧭 ilham** — ada AI power tapi tak tau nak buat apa (macam ada Lamborghini tapi tak tau nak pandu ke mana)? Swipe kad use-case AI satu-satu macam Tinder: swipe kanan (menarik) / kiri (skip). Yang kau suka masuk simpanan bawah — tap **"copy idea"** untuk paste ke AI tool kau, atau tap ikon **tong sampah** untuk buang idea yang tak jadi. Deck **tak habis-habis**: lepas kad seed (18 idea) dah nak licin, app auto-minta idea segar dari AI di latar belakang (prefetch), jadi kau boleh swipe tanpa henti. Kalau AI tak dapat dicapai sekejap, ada butang "cuba lagi" / "ulang idea lama". Laju, main-main, zero typing

## Lain-lain

- 📱 **PWA** — boleh install ke home screen (Add to Home Screen), ada offline shell melalui service worker
- 🎨 Reka bentuk hand-made cream-paper, ikon SVG, animasi lembut (hormat `prefers-reduced-motion`)

## Teknikal

- Satu fail `index.html` sahaja — static site, GitHub Pages friendly
- AI engine: DeepSeek V4 (`deepseek-v4-flash`, non-thinking mode) melalui proxy Vercel (`muhasabah-app.vercel.app/api/gemini`) — API key kekal selamat di server side, tidak terdedah dalam frontend. Proxy pulangkan respons dalam bentuk Gemini supaya serasi dengan app lain yang berkongsi endpoint yang sama
