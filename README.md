# 📚 Kutubxona Boshqaruv Tizimi

Kutubxona faoliyatini yuritish uchun to'liq relatsion ma'lumotlar bazasi asosida yaratilgan veb-ilova. Loyiha "Ma'lumotlar bazasini loyihalashtirish" fani doirasida amaliy ko'nikma sifatida ishlab chiqilgan.

🔗 **Demo:** ilovani ochish uchun `index.html` faylini brauzerda ishga tushiring (hech qanday server kerak emas).

## ✨ Imkoniyatlar

- 5 ta bog'langan jadval: **Mualliflar, Adabiyotlar, O'quvchilar, Xodimlar, Ijara**
- Har bir jadval uchun to'liq **CRUD** (qo'shish, ko'rish, tahrirlash, o'chirish)
- Jadvallar orasidagi bog'lanishlar (Foreign Key) — masalan, kitob qo'shishda muallif ro'yxatdan tanlanadi
- Ma'lumotlar brauzer xotirasida (localStorage) saqlanadi
- Mobil qurilmalarga moslashgan (responsive) dizayn
- Tungi/kunduzgi rejimga avtomatik moslashish (dark/light mode)

## 🗂 Ma'lumotlar bazasi tuzilishi

| Jadval | Asosiy maydonlar | Bog'lanish |
|---|---|---|
| Mualliflar | muallif_id (PK), muallif_fish, tugilgan_yili, vafot_etgan_yili | — |
| Adabiyotlar | adabiyot_id (PK), adabiyot_nomi, muallif_id (FK), janri, nashr_yili | Mualliflar → Adabiyotlar (1:N) |
| O'quvchilar | oquvchi_id (PK), oquvchi_fish, manzili, azo_sanasi, toifasi | — |
| Xodimlar | xodim_id (PK), xodim_fish, lavozim | — |
| Ijara | ijara_id (PK), adabiyot_id (FK), oquvchi_id (FK), xodim_id (FK), sanalar | Adabiyotlar/O'quvchilar/Xodimlar → Ijara (1:N) |

To'liq ER-diagramma va normalizatsiya tahlili `Kutubxona_MB_hisobot.docx` faylida keltirilgan.

## 🛠 Texnologiyalar

- HTML5, CSS3 (CSS Variables, responsive grid)
- Vanilla JavaScript (framework'siz)
- Brauzer localStorage API (ma'lumotlarni saqlash)

## 🚀 Ishga tushirish

1. Repozitoriyani yuklab oling yoki klonlang:
   ```bash
   git clone https://github.com/<username>/kutubxona-mb.git
   ```
2. `index.html` faylini istalgan brauzerda oching.
3. Tayyor! Hech qanday o'rnatish yoki server talab qilinmaydi.

### GitHub Pages orqali onlayn joylashtirish

1. Repo Settings → Pages bo'limiga o'ting
2. Source sifatida `main` branch, `/root` papkasini tanlang
3. Bir necha daqiqadan so'ng `https://<username>.github.io/kutubxona-mb/` manzilida ilova ishga tushadi

## 📁 Loyiha tuzilishi

```
kutubxona-mb/
├── index.html      # To'liq ilova (HTML + CSS + JS bitta faylda)
├── README.md       # Loyiha haqida ma'lumot
└── docs/
    └── Kutubxona_MB_hisobot.docx   # Loyihalashtirish hisoboti (ER-diagramma, normalizatsiya)
```

## 👤 Muallif

**Otamurodov Azizbek**
Samarqand davlat universiteti qoshidagi Sun'iy intellekt va raqamli texnologiyalar instituti
Dasturiy injiniring yo'nalishi, 15-guruh

## 📄 Litsenziya

Bu loyiha ta'lim maqsadlarida yaratilgan va MIT litsenziyasi ostida ochiq.
