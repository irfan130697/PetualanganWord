# ⚔️ Word Quest: The Lost Document

Game petualangan edukasi berbasis browser untuk belajar **Microsoft Word untuk Pemula**.
Pemain menjelajahi *Word Kingdom*, melawan monster dan boss, dan menjawab pertanyaan seputar Word untuk menyerang. Tujuan akhirnya adalah mengalahkan **Dark Document Lord** dan meraih gelar **Document Master**.

Materi mengacu pada *Modul Private Microsoft Office, Pertemuan 1: Microsoft Word untuk Pemula*.

## ✨ Fitur

- Peta 2D yang bisa dijelajahi (WASD / tombol panah), 6 wilayah:
  Keyboard Village, Font Forest, Paragraph Canyon, Layout Mountain, Insert Ruins, Save Castle
- Battle bergiliran (Attack, Skill, Item, Escape). Serangan hanya berhasil jika jawaban benar
- Boss berfase di setiap wilayah; Final Boss memiliki 5 fase
- Sistem RPG: level, XP, gold, potion, revive, 11 achievement, dan quest utama serta sampingan
- Progres tersimpan otomatis di `localStorage` (Continue dan Reset Game)
- Satu file HTML, tanpa dependensi, tanpa build, tanpa internet

## 🎮 Cara Bermain

| Aksi | Kontrol |
|---|---|
| Bergerak | `W` `A` `S` `D` atau tombol panah |
| Bicara dengan NPC / buka peti | `E` (atau tombol 🅴 Interaksi) |
| Mulai battle | Dekati monster |
| Quest, inventory, achievement, simpan, reset | Tombol 📜 Menu |

## 🚀 Menjalankan Secara Lokal

Buka `index.html` langsung di browser (klik dua kali). Tidak perlu server.

## 🌐 Deploy ke GitHub Pages

1. Buat repository baru di GitHub, misalnya `word-quest`.
2. Upload `index.html` dan `README.md` ke root repository:
   ```bash
   git init
   git add index.html README.md
   git commit -m "Word Quest: first release"
   git branch -M main
   git remote add origin https://github.com/USERNAME/word-quest.git
   git push -u origin main
   ```
3. Buka **Settings → Pages**.
4. Pada **Build and deployment → Source**, pilih **Deploy from a branch**.
5. Pilih branch **main** dan folder **/ (root)**, lalu klik **Save**.
6. Tunggu 1–2 menit. Game bisa dimainkan di:
   `https://USERNAME.github.io/word-quest/`

## 🛠️ Kustomisasi

Semua ada di `index.html`:

- **Soal**: array `Q` (satu array per wilayah). Format tiap soal: `"pertanyaan|jawaban benar|salah 1|salah 2|salah 3"`. Urutan pilihan diacak otomatis.
- **Monster dan boss**: `MZ` (monster) dan `BZ` (boss).
- **Dialog NPC**: array `NP`. **Cerita pembuka**: array `STORY`.
- **Achievement**: array `ACH`.

## 📚 Catatan

- Progres disimpan di browser pemain (kunci `wq1`). Mengganti browser atau menghapus data situs akan mereset progres.
- Game dirancang untuk layar laptop/desktop dengan keyboard.

## 📄 Lisensi

Bebas dipakai untuk keperluan belajar dan mengajar. Tambahkan file `LICENSE` sesuai kebutuhan, misalnya MIT.
