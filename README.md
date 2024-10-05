
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

**[Part 1](#Part-1.-Operatsion-tizimni-o‘rnatish)da yaratilgan foydalanuvchiga sudo komandasini bajarishga ruxsat berish.**
![img](screen/5.0.png)
**Part 2 da yaratilgan foydalanuvchi nomidan OS hostname ni o'zgartirish (sudo yordamida).**
![img](screen/5.1.png)
**sudo — bu yordamchi dastur bo'lib, vaqtinchalik ravishda imtiyozlarni oshirish va tizimni boshqarish vazifalarini bajarishga imkon beradi.**
![img](screen/4..png)
![img](screen/4..png)
![img](screen/4..png)
![img](screen/4..png)

# Simple Bash Utils

Development of Bash text utilities: cat, grep.

The russian version of the task can be found in the repository.

💡 [Tap here](https://new.oprosso.net/p/4cb31ec3f47a4596bc758ea1861fb624) **to leave your feedback on the project**. It's anonymous and will help our team make your educational experience better. We recommend completing the survey immediately after the project.

## Contents

0. [Preamble](#preamble)
1. [Chapter I](#chapter-i) \
   1.1. [Introduction](#introduction)
2. [Chapter II](#chapter-ii) \
   2.1. [Information](#information)
3. [Chapter III](#chapter-iii) \
[Part 1](#part-1-operatsion-tizimni-o‘rnatish) 
   3.1. [Part 1](#part-1-working-with-the-cat-utility)  
   3.2. [Part 2](#part-2-working-with-grep-utility)  
   3.3. [Part 3](#part-3-bonus-implementation-of-some-grep-utility-flags)  
   3.4. [Part 4](#part-4-bonus-implementation-of-grep-utility-flag-combinations)


## Part 1. Working with the cat utility

You need to develop a cat utility:
- Support of all flags (including GNU versions) specified [above](#cat-options)
- The source, header, and build files must be placed in the src/cat/ directory
- The resulting executable file must be placed in the directory src/cat/ and named s21_cat

## Part 2. Working with grep utility

You need to develop the grep utility:
- Support of the following flags: `-e`, `-i`, `-v`, `-c`, `-l`, `-n`
- Only pcre or regex libraries can be used for regular expressions
- The source, header and make files must be placed in the src/grep/ directory
- The resulting executable file must be placed in the directory src/grep/ and named s21_grep

## Part 3. Bonus. Implementation of some grep utility flags

Bonus assignment for extra points. You need to develop the grep utility:
- Support of all flags, including: `-h`, `-s`, `-f`, `-o`
- Only pcre or regex libraries can be used for regular expressions
- The source, header and make files must be placed in the src/grep/ directory
- The resulting executable file must be placed in the directory src/grep/ and named s21_grep

## Part 4. Bonus. Implementation of grep utility flag combinations

Bonus assignment for extra points. You need to develop the grep utility:
- Support of all flags, including their _pair_ combinations (e.g. `-iv`, `-in`)
- Only pcre or regex libraries can be used for regular expressions
- The source, header and make files must be placed in the src/grep/ directory
- The resulting executable file must be placed in the directory src/grep/ and named s21_grep




