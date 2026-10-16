# Project 2: Personal Finance Tracker

## 1. Loyiha maqsadi

Terminalda ishlaydigan shaxsiy moliya hisoblagichini yarating. Dastur foydalanuvchining daromadlari va xarajatlarini qayd etsin, balansni hisoblasin va oddiy hisobotlar chiqarsin.

Bu loyiha funksiyalar, modullar, `list`, `dict`, sikllar, shartlar, filtrlash va aggregatsiyani amaliyotda mustahkamlaydi.

## 2. Texnik cheklovlar

- Python standart imkoniyatlaridan foydalaning.
- Ma’lumotlarni `list` va `dict` ichida saqlang.
- `class`, tashqi kutubxonalar va haqiqiy ma’lumotlar bazasidan foydalanmang.
- Har bir asosiy operatsiya alohida funksiya bo‘lsin.
- Dastur `main.py` orqali ishga tushsin.
- Hozircha ma’lumotlarni faylga saqlash shart emas.

## 3. Fayllar tuzilmasi

```text
personal_finance_tracker/
├── main.py
├── transactions.py
├── reports.py
├── utils.py
└── database.py
```

Vazifalar:

- `main.py` — menu va dastur oqimini boshqarish.
- `transactions.py` — daromad/xarajat qo‘shish, ko‘rish va o‘chirish.
- `reports.py` — balans, jami daromad, jami xarajat va kategoriyalar bo‘yicha hisobotlar.
- `utils.py` — input tekshirish va formatlash yordamchilari.
- `database.py` — tranzaksiyalar ro‘yxati va keyingi ID kabi ma’lumotlar.

## 4. Ma’lumotlar modeli

Har bir tranzaksiya quyidagi ko‘rinishda bo‘lsin:

```python
{
    "id": 1,
    "type": "expense",
    "amount": 45000,
    "category": "food",
    "description": "Tushlik"
}
```

`type` qiymati faqat `income` yoki `expense` bo‘lishi mumkin. `amount` musbat son bo‘lishi kerak. Pul qiymatlarini hisoblashda float aniqligi bilan bog‘liq muammolardan qochish uchun summalarni butun so‘m ko‘rinishida saqlang.

## 5. Menu talablari

```text
===== PERSONAL FINANCE TRACKER =====
1. Daromad qo‘shish
2. Xarajat qo‘shish
3. Barcha tranzaksiyalarni ko‘rish
4. Tranzaksiyani o‘chirish
5. Joriy balansni ko‘rish
6. Umumiy hisobot
7. Kategoriya bo‘yicha filtrlash
8. Ma’lum summadan yuqori xarajatlarni ko‘rish
0. Chiqish
```

Menu `0` tanlanguncha ishlasin.

## 6. Funksional talablar

### 6.1. Daromad qo‘shish
- Miqdor musbat butun son bo‘lsin.
- Kategoriya va izoh kiritilsin.
- ID avtomatik yaratilishi kerak.
- Tranzaksiya `income` turi bilan saqlansin.

### 6.2. Xarajat qo‘shish
- Miqdor musbat butun son bo‘lsin.
- Kategoriya va izoh kiritilsin.
- Tranzaksiya `expense` turi bilan saqlansin.

### 6.3. Tranzaksiyalarni ko‘rish
- ID, turi, summa, kategoriya va izoh ko‘rsatilsin.
- Ro‘yxat bo‘sh bo‘lsa, mos xabar chiqsin.
- Daromad va xarajat turi foydalanuvchiga aniq ko‘rinsin.

### 6.4. Tranzaksiyani o‘chirish
- ID orqali tranzaksiya topilsin.
- Mavjud bo‘lmagan ID uchun xabar chiqsin.
- Tranzaksiya faqat topilganidan keyin o‘chirilsin.

### 6.5. Joriy balans
Quyidagi formula asosida hisoblang:

`Balans = jami daromad − jami xarajat`

Balansni hisoblash uchun alohida funksiya yozing. Hisoblash kodi menu ichida takrorlanmasin.

### 6.6. Umumiy hisobot
Quyidagilar ko‘rsatilsin:
- Jami daromad.
- Jami xarajat.
- Joriy balans.
- Tranzaksiyalar soni.
- Eng katta xarajat (xarajat mavjud bo‘lsa).

### 6.7. Kategoriya bo‘yicha filtrlash
- Foydalanuvchi kategoriya kiritsin.
- Shu kategoriyadagi tranzaksiyalar ko‘rsatilsin.
- Kategoriya topilmasa, mos xabar chiqsin.
- Qo‘shimcha talab: kategoriya nomini katta-kichik harflarga bog‘liq bo‘lmagan holda taqqoslang.

### 6.8. Ma’lum summadan yuqori xarajatlar
- Foydalanuvchi chegara summasini kiritsin.
- Faqat `expense` turidagi va shu summadan katta tranzaksiyalar chiqarilsin.

## 7. Hisoblash qoidalari

- Daromad summasi musbat bo‘lsin.
- Xarajat summasi musbat bo‘lsin; uni balansdan ayirish hisobot funksiyasida bajarilsin.
- `income` va `expense` turlarini aralashtirib yubormang.
- Bo‘sh ro‘yxatda `max()` kabi operatsiyalarni ishlatishdan oldin holatni tekshiring.
- Hisobot funksiyalari natijani qaytarsin yoki aniq formatda chiqarsin; bir xil hisob-kitobni turli joyda takrorlamang.

## 8. Xatolik holatlari

Quyidagilarni sinab ko‘ring:

- Manfiy yoki nol summa.
- Summa o‘rniga matn kiritish.
- Noto‘g‘ri tranzaksiya turi.
- Mavjud bo‘lmagan ID.
- Bo‘sh kategoriya.
- Hali tranzaksiya kiritilmagan holatda hisobot ochish.
- Xarajatlar bo‘lmaganda eng katta xarajatni aniqlash.

Dastur foydalanuvchining noto‘g‘ri inputi sababli to‘xtab qolmasligi kerak.

## 9. Qabul qilish mezonlari

- [ ] Daromad va xarajat qo‘shiladi.
- [ ] Tranzaksiyalar ro‘yxati ko‘rsatiladi.
- [ ] Tranzaksiya ID orqali o‘chiriladi.
- [ ] Balans formulasi to‘g‘ri ishlaydi.
- [ ] Umumiy hisobot to‘g‘ri hisoblanadi.
- [ ] Kategoriya bo‘yicha filtrlash ishlaydi.
- [ ] Musbat summa tekshiriladi.
- [ ] Kod modullarga ajratilgan va funksiyalar qayta ishlatiladi.

## 10. Qo‘shimcha challenge

1. Tranzaksiyalarni summa bo‘yicha saralash.
2. Eng ko‘p pul sarflangan kategoriyani topish.
3. Faqat daromadlarni yoki faqat xarajatlarni ko‘rsatish.
4. JSON faylga saqlash va qayta yuklash.
5. Ma’lumotlar eksporti uchun oddiy matnli hisobot yaratish.

## 11. Topshirish

Loyihani ishga tushirish yo‘riqnomasi va qisqa demo bilan topshiring. Balans qanday hisoblanishini va hisobotlar qaysi funksiyalarga tayanganini tushuntira oling.
