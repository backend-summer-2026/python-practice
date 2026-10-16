# Project 1: Library Management System

## 1. Loyiha maqsadi

Terminal orqali ishlaydigan kutubxona boshqaruv tizimini yarating. Dastur kitoblar ro‘yxatini yuritishi, kitoblarni qidirishi va kitob berish/qaytarish jarayonlarini boshqarishi kerak.

Bu loyiha orqali `function`, `module`, `list`, `dict`, `if/elif/else`, `while`, `for`, input tekshirish va CRUD amaliyotlari mustahkamlanadi.

## 2. Texnik cheklovlar

- Python standart imkoniyatlaridan foydalaning.
- Ma’lumotlarni hozircha `list` va `dict` ichida saqlang.
- `class`, tashqi kutubxonalar va haqiqiy ma’lumotlar bazasidan foydalanmang.
- Har bir asosiy amal alohida funksiya bo‘lsin.
- Dastur `main.py` orqali ishga tushsin.
- Ma’lumotlar dastur yopilganda yo‘qolishi mumkin.

## 3. Fayllar tuzilmasi

```text
library_management/
├── main.py
├── books.py
├── utils.py
└── database.py
```

Vazifalar:

- `main.py` — menu va dastur oqimini boshqarish; tegishli modullardagi funksiyalarni chaqirish.
- `books.py` — kitoblarni qo‘shish, ko‘rish, tahrirlash, o‘chirish, qidirish, berish va qaytarish.
- `utils.py` — inputni tekshirish va qayta ishlatish mumkin bo‘lgan yordamchi funksiyalar.
- `database.py` — boshlang‘ich `books` ro‘yxati va `next_book_id` kabi ma’lumotlarni saqlash.

## 4. Ma’lumotlar modeli

Har bir kitob quyidagi maydonlarga ega bo‘lsin:

```python
{
    "id": 1,
    "title": "Clean Code",
    "author": "Robert C. Martin",
    "year": 2008,
    "available": True
}
```

`id` takrorlanmasligi kerak. `available=True` kitob kutubxonada mavjudligini, `False` esa kitob berilganini anglatadi.

## 5. Menu talablari

Dastur quyidagi menyuni ko‘rsatsin:

```text
===== LIBRARY MANAGEMENT =====
1. Barcha kitoblarni ko‘rish
2. Kitob qo‘shish
3. Kitob ma’lumotlarini tahrirlash
4. Kitobni o‘chirish
5. Kitob qidirish
6. Kitobni foydalanuvchiga berish
7. Kitobni qaytarish
8. Mavjud kitoblarni ko‘rish
9. Berilgan kitoblarni ko‘rish
0. Chiqish
```

Menu foydalanuvchi `0` ni tanlamaguncha takrorlanishi kerak.

## 6. Funksional talablar

### 6.1. Kitoblarni ko‘rish
- Barcha kitoblarni tartibli ko‘rsating.
- Kitoblar yo‘q bo‘lsa, tushunarli xabar chiqaring.
- Har bir kitobning ID, nomi, muallifi, yili va holati ko‘rsatilsin.

### 6.2. Kitob qo‘shish
- Kitob nomi va muallifi bo‘sh bo‘lmasin.
- Yil butun son bo‘lsin.
- ID avtomatik berilsin.
- Yangi kitob dasturdagi ro‘yxatga qo‘shilsin.

### 6.3. Kitobni tahrirlash
- Foydalanuvchi kitob ID sini kiritsin.
- ID topilmasa, xatolik xabari chiqsin.
- Nom, muallif yoki yilni yangilash mumkin bo‘lsin.
- Foydalanuvchi bo‘sh qiymat kiritsa, eski qiymatni saqlab qolish imkoniyatini ko‘rib chiqing.

### 6.4. Kitobni o‘chirish
- ID orqali kitob topilsin va o‘chirilsin.
- Topilmagan ID uchun dastur to‘xtab qolmasin.
- Qo‘shimcha talab: kitob hozir foydalanuvchiga berilgan bo‘lsa, uni o‘chirishga ruxsat bermang.

### 6.5. Kitob qidirish
- Nom yoki muallif bo‘yicha qidirish.
- Katta-kichik harflar farq qilmasin.
- Qidiruv natijasi bir nechta kitobni qaytarishi mumkin.

### 6.6. Kitob berish
- ID orqali kitob topilsin.
- Faqat mavjud kitob berilsin.
- Kitob berilganda `available=False` bo‘lsin.
- Allaqachon berilgan kitobni ikkinchi marta berishga ruxsat berilmasin.

### 6.7. Kitobni qaytarish
- Faqat berilgan kitob qaytarilsin.
- Qaytarilganda `available=True` bo‘lsin.
- Kitob allaqachon mavjud bo‘lsa, mos xabar chiqsin.

## 7. Yordamchi funksiyalar

`utils.py` ichida zaruratga qarab quyidagi vazifalar uchun funksiyalar yozing:

- Butun son kiritilishini tekshirish.
- Bo‘sh matnni rad etish.
- Kitobni ID orqali topishga yordam berish.
- Kitob ma’lumotlarini chiroyli formatda chiqarish.

Bir xil tekshiruv kodini bir nechta joyda takrorlamang.

## 8. Xatolik holatlari

Quyidagi vaziyatlarni sinab ko‘ring:

- Kitoblar ro‘yxati bo‘sh.
- Foydalanuvchi menu uchun noto‘g‘ri qiymat kiritadi.
- ID o‘rniga matn kiritiladi.
- Mavjud bo‘lmagan ID kiritiladi.
- Bo‘sh nom yoki muallif kiritiladi.
- Kitobni ikki marta berishga urinish.
- Mavjud kitobni qaytarishga urinish.

Dastur bunday vaziyatlarda to‘xtab qolmasligi kerak.

## 9. Qabul qilish mezonlari

- [ ] Dastur `main.py` orqali ishga tushadi.
- [ ] Menu to‘g‘ri ishlaydi.
- [ ] Qo‘shish, ko‘rish, tahrirlash va o‘chirish ishlaydi.
- [ ] Qidiruv katta-kichik harflarni hisobga olmaydi.
- [ ] Kitob berish va qaytarish holatlari to‘g‘ri boshqariladi.
- [ ] Kod modullarga mantiqan ajratilgan.
- [ ] Har bir asosiy operatsiya funksiyada yozilgan.
- [ ] Noto‘g‘ri input dastur qulashiga olib kelmaydi.

## 10. Qo‘shimcha challenge

Asosiy talablar bajarilgach:

1. Kitoblarni nomi bo‘yicha saralash.
2. Muallif bo‘yicha filtrlash.
3. Umumiy, mavjud va berilgan kitoblar sonini chiqarish.
4. Ma’lumotlarni JSON faylga saqlash va dastur ochilganda qayta yuklash.

## 11. Topshirish

Loyihani ishga tushirish yo‘riqnomasi bilan birga topshiring. Har bir modulning vazifasini va asosiy funksiyalarning nima ish bajarishini og‘zaki tushuntirishga tayyor bo‘ling.
