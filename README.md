# PromptCraft — Prompt Builder

Macam Google Translate, tapi untuk prompt: translate prompt mentah / kabur / rojak kepada prompt yang jelas, spesifik dan berstruktur — supaya hasil daripada mana-mana AI (ChatGPT, Claude, Gemini, dll.) jadi jauh lebih bagus.

**Live app:** https://rezkysaid.github.io/Prompt-Builder/

## Empat mod (toggle atas)

App ada empat kerja, tukar dengan toggle ikon+teks **✍️ Prompt │ 📖 fahami │ 🧭 ilham │ 💬 ruang**:

- **Rangka Prompt** — semua ciri di bawah: buat prompt mentah jadi power.
- **📖 Faham Output** — malas/susah baca jawapan panjang dari ChatGPT/Claude/Gemini? Paste jawapan tu masuk sini, app ringkaskan jadi **Intinya (TL;DR) · Poin penting · Apa kau kena buat · Terang simple**, dalam BM santai yang senang telan — siap butang **Dengar** (TTS baca kuat-kuat) & Copy. Tiga alat bantu fokus masa baca: **Fokus** (mod spotlight — blok yang kau tengah baca terang, yang lain jadi kelabu; tap untuk gerak fokus), **Bionik** (bionic reading — bold permulaan tiap perkataan supaya mata lekat & baca laju), dan **checklist** untuk "apa kau kena buat" (tick step yang dah siap, progress nampak). Copy & Dengar tetap ambil teks asal walaupun Bionik on.
- **🧭 ilham** — ada AI power tapi tak tau nak buat apa (macam ada Lamborghini tapi tak tau nak pandu ke mana)? Swipe kad use-case AI satu-satu macam Tinder: swipe kanan (menarik) / kiri (skip). Yang kau suka masuk simpanan bawah — tap **"jom mula dengan ni"** terus power-kan jadi prompt di Rangka Prompt, atau tap ikon **tong sampah** untuk buang idea yang tak jadi. Deck **tak habis-habis**: lepas kad seed (18 idea) dah nak licin, app auto-minta idea segar dari AI di latar belakang (prefetch), jadi kau boleh swipe tanpa henti. Kalau AI tak dapat dicapai sekejap, ada butang "cuba lagi" / "ulang idea lama". Laju, main-main, zero typing.
- **💬 Ruang AI** — ruang chat am, macam guna ChatGPT/Claude terus dalam app ni. Tak berkait prompt: tanya soalan rawak, borak, minta tolong apa-apa. Perbualan berterusan (multi-turn, AI ingat konteks sebelum), disimpan dalam browser (localStorage) supaya tak hilang bila tutup app; ada butang **"chat baru"** untuk mula segar. Guna engine DeepSeek yang sama melalui proxy

## Ciri-ciri (Rangka Prompt)

- 🔁 **Dual-panel macam Google Translate** — prompt asal kiri, prompt enhanced kanan
- 🎛️ **6 mode enhancement** — General, Coding, Creative, Business, Image-Gen, Academic
- ✅ **Annotation** — senarai apa yang ditambah/diubah pada prompt asal (belajar sambil guna)
- 🌐 **Sokong bahasa rojak** — input Melayu, English atau campuran; bahasa output boleh pilih (Auto / MS / EN)
- 🎤 **Voice input** — malas/tak reti menulis? Tekan "Cakap", cakap je dalam BM/rojak dan app transkrip terus jadi teks input (Web Speech API, on-device; butang auto-sembunyi kalau browser tak sokong)
- 🧠 **aku overthinking? (lawan perfeksionis)** — untuk yang beku sebab terlebih fikir "kalau-kalau" sebelum menulis. Butang kecil di panel input; tap bila spiral datang, keluar ayat reframe yang lawan terus kerisauan ("prompt tak perlu perfect — AI pandai teka", "takde gred A, ada 'cukup untuk mula'", "cakap macam biasa je", "'macam mana kalau…' tu tipu otak — cuba je") + butang shuffle & "ok, jom taip" yang fokus balik kotak input
- 🧭 **Pemandu tulis (bila kotak kosong)** — ramai orang beku tengok kotak kosong lepas tu tutup app. Bila kotak kosong, butang **"kepala serabut? jom aku pandu kau tulis"** muncul, buka pemandu **soal-jawab laju**: 3-4 soalan pendek satu-satu (nak buat apa? untuk siapa? bentuk hasil? detail lain?) — kebanyakannya tap chip je, sikit je kena taip. Sambil kau jawab, **prompt tumbuh depan mata** dalam kotak preview (bahagian baru diserlah), jadi kau nampak progress terus. Tekan "guna ni" bila-bila untuk hantar prompt yang dah terbina ke kotak input. Tujuan: turunkan halangan mula sampai tak boleh gagal + bagi momentum
- 💡 **Hint masa taip** — sambil kau taip, app bagi nudge lembut apa yang kurang (untuk siapa? format hasil?) dan bagitau bila prompt dah cukup detail — ngajar kau jadi lebih pandai prompt. Tak muncul dalam mod "Kemas je"
- 🧹 **Intensiti: Kemas je** — pilihan untuk hanya susun ayat jadi kemas dan gramatis tanpa AI tambah konteks/format/andaian sendiri; sesuai bila kau nak AI tafsir sendiri niat prompt kau. Terpakai pada enhance utama dan follow-up sekali
- 💬 **Konteks perbualan** — satu kotak untuk bagitau apa kau tengah bincang dengan AI di tempat lain (ChatGPT/Claude/Gemini) & di mana perbualan tu dah sampai; app suntik konteks ni supaya prompt yang dibuat **berkait & sambung** dengan chat kau di sana, bukan topik baru. Suis on/off, animasi buka/tutup smooth, disimpan dalam browser; tak terpakai dalam mod "Kemas je"
- 🌱 **Seed grower (di atas sekali)** — Rangka Prompt bermula dengan seed grower sebagai titik mula: bagi frasa pendek/kasar (contoh: "buat duit dengan ai") dan AI tumbuhkan jadi 5 cadangan prompt penuh dengan angle berbeza, siap boleh copy atau terus "Guna ni" — ia terus turun ke bahagian **tweak prompt jadi cantik** (enhancer utama) di posisi kedua untuk power-kan lagi
- 🕘 **Sejarah prompt + kegemaran** — disimpan dalam browser (localStorage)
- 📋 Copy, Paste, Swap, Regenerate
- 🖼️ **Kongsi as image** — export prompt yang dah diperbaiki jadi kad gambar cantik berbrand (logo + tagline app) terus dari canvas; guna Web Share API kat mobile (share ke mana-mana app) atau download PNG kat desktop
- 🧵 **Thread follow-up** — prompt pertama untuk buka chat; lepas tu taip niat follow-up secara kasar dan PromptCraft craft prompt seterusnya yang bersambung dengan yang sebelumnya (tak ulang konteks, merujuk jawapan AI tadi) — sedia untuk paste dalam chat yang sama kat ChatGPT/Claude/Gemini. Seluruh thread disimpan dalam sejarah: klik balik item tu bila-bila dan sambung craft follow-up dengan konteks yang sama
- ↺ **Panggil balik soalan** — teks yang kau taip dalam kotak follow-up auto-simpan (kekal walaupun AI high-demand/limit atau app ditutup); butang "soalan tadi" munculkan balik soalan yang pernah kau taip supaya tak lupa apa yang pernah diajukan
- 📱 **PWA** — boleh install ke home screen (Add to Home Screen), ada offline shell melalui service worker

## Teknikal

- Satu fail `index.html` sahaja — static site, GitHub Pages friendly
- AI engine: DeepSeek V4 (`deepseek-v4-flash`, non-thinking mode) melalui proxy Vercel (`muhasabah-app.vercel.app/api/gemini`) — API key kekal selamat di server side, tidak terdedah dalam frontend. Proxy pulangkan respons dalam bentuk Gemini supaya serasi dengan app lain yang berkongsi endpoint yang sama
