Here's a structured report based on the tasks you've provided, organized with subheadings and appropriate descriptions. 

---

# Hisobot

## 1-qism. OTni o'rnatish
Ubuntu 20.04 Server LTS ni GUIsiz o'rnatildi. 

### Qo'shilganlar:
- O'rnatishdan so'ng terminalda bajarilgan buyruq: 
  ```bash
  cat /etc/issue
  ```
- **Skrinshot**: Buyruq chiqishi. (Skrinshotda buyruq natijasi ko'rsatiladi.)

## 2-qism. Foydalanuvchi yaratish
Yangi foydalanuvchi yaratildi va admguruhga qo'shildi.

### Qo'shilganlar:
- Foydalanuvchini yaratish uchun bajargan buyruq:
  ```bash
  sudo adduser yangi_foydalanuvchi
  ```
- Foydalanuvchi ro'yxati:
  ```bash
  cat /etc/passwd
  ```
- **Skrinshotlar**: 
  - Foydalanuvchi yaratish buyruqi natijasi.
  - `cat /etc/passwd` chiqishi.

## 3-qism. OS tarmog'ini sozlash
Tarmoq interfeysi va DHCP sozlamalari amalga oshirildi.

### Qo'shilganlar:
- Foydalanuvchi nomi `foydalanuvchi-1` sifatida belgilandi.
- Tarmoq interfeyslari ro'yxati:
  ```bash
  ip a
  ```
- DHCP kodini dekodlash:
  ```bash
  dhclient
  ```
- **Skrinshotlar**:
  - Tarmoq interfeyslari natijasi.
  - DHCP kodining chiqishi.
  - Ping natijalari (`ping 1.1.1.1` va `ping ya.ru`).

## 4-qism. OS yangilanishi
Tizim paketlari yangilandi va hech qanday yangilanishlar mavjud emasligi tasdiqlandi.

### Qo'shilganlar:
- Yangilash buyruqlari:
  ```bash
  sudo apt update && sudo apt upgrade
  ```
- **Skrinshot**: Yangilanishlar mavjud emasligi haqidagi xabar.

## 5-qism. Sudo buyrug'idan foydalanish
Foydalanuvchiga `sudo` ruxsat berildi va xost nomi o'zgartirildi.

### Qo'shilganlar:
- **Skrinshot**: O'zgartirilgan xost nomi.

## 6-qism. Vaqt xizmatini o'rnatish va sozlash
Vaqt sinxronlash xizmati sozlandi.

### Qo'shilganlar:
- Vaqt mintaqasi:
  ```bash
  timedatectl show
  ```
- **Skrinshot**: Vaqt ko'rsatkichlari.

## 7-qism. Matn muharrirlarini o'rnatish va ulardan foydalanish
VIM matn muharriri o'rnatildi va fayl yaratildi.

### Qo'shilganlar:
- Har bir muharrirdan skrinshotlar:
  - Fayl mazmuni va o'zgarishlarni saqlash uchun nima qilingan.
  - O'zgarishlarni saqlamasdan chiqish uchun nima qilingan.

## 8-qism. SSHD xizmatini o'rnatish va asosiy sozlash
SSHD xizmati o'rnatildi va 2022 portiga tiklandi.

### Qo'shilganlar:
- **Skrinshotlar**:
  - SSHD jarayoni.
  - `netstat -tan` chiqishi.

## 9-qism. Top, htop utilitlarini o'rnatish va ishlatish
Yuqori va htop yordam dasturlari o'rnatildi va ishga tushirildi.

### Qo'shilganlar:
- Hisobotga htop va top buyruqlarining chiqishlari.

## 10-qism. Fdisk yordam dasturidan foydalanish
Fdisk yordamida qattiq disk haqida ma'lumot olindi.

### Qo'shilganlar:
- **Skrinshot**: Fdisk chiqishi.

## 11-qism. df yordam dasturidan foydalanish
Disk maydoni haqida ma'lumot olindi.

### Qo'shilganlar:
- **Skrinshot**: df va df -Th chiqishlari.

## 12-qism. Du yordam dasturidan foydalanish
Disk hajmi haqida ma'lumot olish uchun du yordam dasturi ishlatildi.

### Qo'shilganlar:
- **Skrinshotlar**: Har bir papka hajmi.

## 13-qism. Ncdu yordam dasturini o'rnatish va ishlatish
Ncdu yordam dasturi o'rnatildi va hajm tekshirilmoqda.

### Qo'shilganlar:
- **Skrinshot**: Ncdu chiqishi.

## 14-qism. Tizim jurnallari bilan ishlash
Tizim jurnallari ko'rib chiqildi.

### Qo'shilganlar:
- **Skrinshot**: Oxirgi muvaffaqiyatli kirish vaqtini va foydalanuvchi nomini ko'rsatuvchi jurnallar.

## 15-qism. CRON ish rejalashtiruvchisidan foydalanish
CRON ish rejalashtiruvchisi orqali ish vaqti buyrug'i bajarildi.

### Qo'shilganlar:
- **Skrinshotlar**: CRON ishlar ro'yxati.

### Yakuniy Ish:
Barcha vazifalarni olib tashlash uchun CRON rejalashtiruvchisi tozalandi. 

---

### Izoh:
Barcha skrinshotlar va boshqa qo'shimchalar hisobotda mavjud. Hisobot "src" papkasida `.md` kengaytmali formatda joylashgan.

Umid qilamanki, bu yordam beradi! Agar biror narsani o'zgartirish yoki qo'shish kerak bo'lsa, iltimos xabar bering.