# English Grammar Quiz — Level 2

Kuis grammar interaktif untuk siswa SMA (Kurikulum Merdeka), materi **Level 2 — Penguasaan Verba & Struktur Kalimat** (oleh Mr. Fio).

Struktur & kode aplikasi identik dengan Level 1 — yang berbeda hanya **topik dan soal** (`data/quiz-data.json`).

## 10 Topik (masing-masing 10 soal pilihan ganda)

1. Tense Mastery
2. Modal Verbs
3. Conditionals
4. Passive Voice
5. Adjective Clause
6. Reported Speech
7. Gerund & Infinitive
8. Comparison
9. Causative
10. Question Tags

Tiap soal punya sistem **kunci jawaban** (lock-to-reveal) dengan penjelasan Bahasa Indonesia, lalu hasil & nilai otomatis tersimpan. Tersedia juga **Admin panel** (login admin) untuk melihat & mengelola nilai.

## Struktur folder

```
grammar-quiz-level2/
├── index.html          ← buka file ini
├── css/
│   └── styles.css
├── js/
│   └── app.js
├── data/
│   └── quiz-data.json  ← materi Level 2 (ubah di sini untuk ganti soal)
├── LICENSE
└── README.md
```

## Cara menjalankan

Karena `index.html` memuat `data/quiz-data.json` lewat `fetch`, jalankan via server (bukan klik file langsung):

```bash
# dari dalam folder grammar-quiz-level2
python -m http.server 8000
# buka http://localhost:8000
```

### Publish ke GitHub Pages
1. Buat repo baru, upload **semua isi** folder ini.
2. Settings → Pages → Source: branch `main`, folder `/ (root)`.
3. Kuis live di `https://<username>.github.io/<repo>/`.

## Mengubah soal

Edit `data/quiz-data.json`. Setiap soal berformat:

```json
{
  "id": "tense_001",
  "question": "...",
  "options": ["A", "B", "C", "D"],
  "correctAnswer": 2,
  "explanation": "..."
}
```

`correctAnswer` memakai indeks 0 (0 = opsi pertama).

---
Berbasis aplikasi Grammar Quiz Level 1: https://github.com/pyem23/grammar-quiz1
