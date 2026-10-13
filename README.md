# Portal Layanan Akademik (Pertemuan 5)

Halaman web client semantik, responsif, dan aksesibel. Tanpa JavaScript.

- **Demo:** https://kevinpelamonia.github.io/Layanan-Akademik/
- **Repo:** https://github.com/KevinPelamonia/Layanan-Akademik

## Keputusan desain
- **Semantik:** `header`, `nav`, `main`, `section`, `article` (4 kartu), `form`, `footer`; heading h1 → h2 → h3 berurutan.
- **Mobile-first:** CSS dasar satu kolom; breakpoint 40em (2 kolom) dan 64em (4 kolom) karena konten mulai lapang.
- **Form:** label terasosiasi (`for`/`id`), `fieldset`+`legend` untuk radio, `type=email`, `required`, `minlength`, `pattern`, `autocomplete`, `<button type="submit">`.
- **Aksesibilitas:** skip link, `:focus-visible` jelas, kontras tinggi, `aria-describedby` hanya untuk teks bantuan, ARIA minimal (native-first).
- **Gambar:** `img/logo.svg` dekoratif (nama portal sudah ada di teks `h1`), maka `alt=""`.

## Bukti pengujian DevTools (isi dan simpan screenshot di `evidence/`)
| Pemeriksaan | Cara | Hasil | File bukti |
|---|---|---|---|
| Responsive 360px | F12 → Ctrl+Shift+M, lebar 360 | tidak ada scroll horizontal | evidence/01-360.png |
| Responsive 768px | lebar 768 | kartu 2 kolom | evidence/02-768.png |
| Responsive 1280px | lebar 1280 | kartu 4 kolom | evidence/03-1280.png |
| Elements/CSS | Inspect kartu, lihat Grid badge & box model | | evidence/04-elements.png |
| Network | Reload (Ctrl+R), cek status resource | semua 200, tanpa 404 | evidence/05-network.png |
| Accessibility | Tab "Accessibility" / Lighthouse | tree: landmark & label terbaca | evidence/06-a11y.png |
| Keyboard | Tekan Tab dari awal halaman | fokus terlihat di semua kontrol | evidence/07-focus.png |
| Validasi email | Isi `abc` lalu kirim | browser menolak | evidence/08-email.png |

## Catatan temuan
Tulis 2–3 temuan debugging nyata Anda di sini (mis. masalah overflow, kontras, atau resource 404 dan cara memperbaikinya).
