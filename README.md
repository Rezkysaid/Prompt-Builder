# PromptCraft — Input Builder

Toolkit ringkas untuk kerja dengan AI. Kau tulis **input** — bukan "prompt" — sebab perkataan tu bagi tekanan supaya menulis elok-elok dulu. Tulis je macam kau fikir, bersepah pun tak apa; app yang susunkan.

**Live app:** https://rezkysaid.github.io/Prompt-Builder/

## Dua mod (toggle atas)

- **✍️ Input** — tiga langkah bersambung, dari kabur terus ke prompt siap:
  - **Terokai sudut** — tak jelas apa sebenarnya kau nak bincang? Taip **satu kata kunci** je (contoh: "harga diri") dan AI bukakan jadi **8 sudut perbincangan konkrit** — soalan yang bermain dalam kepala, situasi harian yang menyakitkan, punca/akar, salah faham biasa, langkah praktikal, dan sudut yang jarang terfikir. Tap yang kena dengan hati, dia jatuh ke kotak benih. Tekan **"lagi sudut"** untuk batch baru (AI elak ulang yang dah dipapar)
  - **Tulis mentah-mentah je** — kerja utama app ni. Tulis bersepah, separuh siap, bercampur BM-English pun tak apa. App tukarkan jadi **prompt berstruktur** ikut elemen prompt engineering berkesan: **peranan · konteks · tugas · kekangan · format output · kriteria berjaya** — dan hanya yang bahan kau betul-betul perlukan. Niat asal kau dikekalkan; app tak reka fakta, dan kalau ada benda penting yang betul-betul hilang dia tinggalkan **[kurungan siku]** untuk kau isi. Bawah hasil ada nota **"apa yang app tambah"** — setiap satu namakan elemen mana yang dimasukkan, supaya lama-lama kau nampak coraknya sendiri. Siap butang **Copy** dan **"cuba versi lain"**
    - **Mula ayat** — halaman kosong susah dilawan, jadi ni **ayat yang dah bermula, tinggal kau habiskan** ("Aku stuck kat…", "Tolong susun fikiran aku pasal…"). Disusun ikut **keadaan kepala kau** — *kepala kosong · kepala serabut · tersekat · nak faham · nak siapkan · nak dilawan* — sebab orang yang buntu tak fikir "aku nak belajar", dia fikir "aku serabut". Tap satu, dia jatuh ke kotak dengan **kursor menunggu betul-betul kat tempat kau sambung**. Tap lagi satu, masuk baris baru. Statik & serta-merta, tiada tunggu AI
  - **Bagi benih je** — tak ada idea langsung? Taip frasa pendek ("buat duit dengan ai") dan AI tumbuhkan jadi **5 prompt penuh** dengan angle berbeza-beza, siap boleh Copy. Ada pilihan bahasa output (Auto / MS / EN)

- **🧭 ilham** — ada AI power tapi tak tau nak buat apa? Swipe kad use-case AI macam Tinder: kanan (menarik) / kiri (skip). Yang kau suka masuk simpanan bawah — tap **"copy idea"** atau ikon tong sampah untuk buang. Deck ni **100% dari AI, takde idea simpanan/default langsung** — setiap kali kau buka tab ilham, app terus tarik idea segar secara real time. Deck **tak habis-habis**: bila kad tinggal sikit, app auto-minta batch baru di latar belakang. Kalau AI tak dapat dicapai, ada butang "cuba lagi" (bukan spinner tersangkut)

## Lain-lain

- 📱 **PWA** — boleh install ke home screen, ada offline shell melalui service worker
- 🎨 Reka bentuk hand-made cream-paper, ikon SVG, animasi lembut (hormat `prefers-reduced-motion`)

## Teknikal

- Satu fail `index.html` sahaja — static site, GitHub Pages friendly
- AI engine: DeepSeek V4 (`deepseek-v4-flash`, non-thinking mode) melalui proxy Vercel (`muhasabah-app.vercel.app/api/gemini`) — API key kekal selamat di server side, tidak terdedah dalam frontend. Proxy pulangkan respons dalam bentuk Gemini supaya serasi dengan app lain yang berkongsi endpoint yang sama
