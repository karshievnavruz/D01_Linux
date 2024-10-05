
1.[Part 1](#part-1-operatsion-tizimni-ornatish)
2.[Part 2](#part-2-foydalanuvchini-yaratish)
3.[Part 3](#part-3-tarmoqni-sozlash)
4.[Part 4](#part-4-os-yangilash)
5.[Part 5](#part-5-sudo-komandasi-foydalanish)
6.[Part 6](#part-6-vaqt-xizmatini-ornatish-va-sozlash)
7.[Part 7](#part-7matn-muharrirlarini-ornatish-va-ishlatish)
8.[Part 8]()
9.[Part 9](#)
10.[Part 10](#)
11.[Part 11](#)
12.[Part 12](#)
13.[Part 13](#)


## Part 1. Operatsion tizimni o‘rnatish


Ubuntu 20.04 Server LTS ni GUI (grafik interfeys) siz o'rnating. (VirtualBox dan foydalaning).

Ubuntu versiyasini quyidagi buyruq orqali tekshiring:
```bash
cat /etc/issue
```
### Natija:

![img](screen/1.png)

## Part 2. Foydalanuvchini yaratish

O'rnatish jarayonida yaratilgan foydalanuvchidan boshqa yangi foydalanuvchini yaratishingiz kerak. 
Foydalanuvchi adm guruhiga qo'shilishi kerak.

Yangi foydalanuvchi cat `/etc/passwd` buyruqining chiqishida ko'rinishi kerak:

   ```bash
   cat /etc/passwd
   ```

### Natija:         
**Foydalanuvchini yaratish:**

Terminalni oching va foydalanuvchi yaratish uchun quyidagi buyruqni bajaring 
(foydalanuvchi nomi sifatida masalan, `newuser` deb yozing):
```bash
   sudo adduser newuser
   ```
![img](screen/2.0.png)
![img](screen/2.1.png)



Keyin foydalanuvchini adm guruhiga qo'shish uchun quyidagi buyruqni bajaring:
```bash
   sudo usermod -aG adm newuser
   ```
![img](screen/2.2.png)


**Foydalanuvchini `/etc/passwd` faylida tekshirish:**
```bash
   /etc/passwd
   ```
![img](screen/2.3.png)

## Part 3. Tarmoqni sozlash

### Natija:

***Mashinaning nomini user-1 qilib o'rnating .**

![img](screen/3.0.png)
![img](screen/3.1.png)

**Hozirgi joylashuvingizga mos vaqt zonasini o'rnating.**
![img](screen/3.2.png)
```bash
sudo timedatectl set-timezone Asia/Tashkent
   ```

**Konsol buyrug‘i yordamida tarmoq interfeyslari nomlarini chiqarish.**
![img](screen/3.3.png)
Eng asosiy virtual interfeyslaridan biri - `lo`. Bu lokal interfeys bo'lib, dasturlarga ushbu kompyuterga murojaat qilish imkonini beradi. 

**Konsol buyrug'i yordamida siz ishlayotgan qurilmaning IP manzilini DHCP serveridan oling.**

**O'rnatish**.
![img](screen/3.4.png)

**Konsol buyrug'i yordamida siz ishlayotgan qurilmaning IP manzilini DHCP serveridan oling.**

![img](screen/3.5.png)

**DHCP — bu dinamik host konfiguratsiya protokoli (Dynamic Host Configuration Protocol) bo'lib, u IT-infrastrukturada har bir yangi qurilmaning tarmoq parametrlarini avtomatik ravishda belgilaydi.**


**Tashqi IP manzilini (ip) va ichki IP manzilini (gw) — ya'ni, standart IP manzilini ekranga chiqarish.**
![img](screen/3.6.png)

**Statik (qo'lda belgilangan, DHCP serveridan olinmagan) IP, gw va DNS sozlamalarini o'rnating (masalan, 1.1.1.1 yoki 8.8.8.8 kabi ochiq DNS serverlardan foydalaning).**
![img](screen/3.7.png)
![img](screen/3.8.png)
![img](screen/3.9.png)
![img](screen/3.10.png)

**Qayta yoqilgandan so'ng.**
![img](screen/3.11.png)
![img](screen/3.12.png)
![img](screen/3.13.png)


## Part 4. OS yangilash

**Sistemani paketlarini vazifani bajarish paytidagi oxirgi versiyasiga yangilang.**
![img](screen/4.0.png)
![img](screen/4.1.png)
## Part 5. Sudo komandasi foydalanish

**[Part 1](#part-1-operatsion-tizimni-ornatish)da yaratilgan foydalanuvchiga sudo komandasini bajarishga ruxsat berish.**
![img](screen/5.0.png)

**[Part 2](#part-2-foydalanuvchini-yaratish) da yaratilgan foydalanuvchi nomidan OS hostname ni o'zgartirish (sudo yordamida).**
![img](screen/5.1.png)
**sudo — bu yordamchi dastur bo'lib, vaqtinchalik ravishda imtiyozlarni oshirish va tizimni boshqarish vazifalarini bajarishga imkon beradi.**
## Part 6. Vaqt xizmatini o'rnatish va sozlash

**Avtomatik vaqtni sinxronizatsiya qilish xizmatini sozlash.**
![img](screen/4..png)

**Quyidagi buyruqning natijasida NTPSynchronized=yes bo'lishi kerak: `timedatectl show`.**
![img](screen/4..png)

## Part 7.Matn muharrirlarini o'rnatish va ishlatish.
**VIM matn muharririni o‘rnating (+ istalgan ikkitasini tanlang: NANO, MCEDIT, JOE va boshqalar).**
![img](screen/4..png)

![img](screen/4..png)
