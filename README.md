## Contents
1.[Part 1](#part-1-operatsion-tizimni-ornatish)

2.[Part 2](#part-2-foydalanuvchini-yaratish)

3.[Part 3](#part-3-tarmoqni-sozlash)

4.[Part 4](#part-4-os-yangilash)

5.[Part 5](#part-5-sudo-komandasi-foydalanish)

6.[Part 6](#part-6-vaqt-xizmatini-ornatish-va-sozlash)

7.[Part 7](#part-7matn-muharrirlarini-ornatish-va-ishlatish)

8.[Part 8](#part-8sshd-xizmatini-ornatish-va-asosiy-sozlash)

9.[Part 9](#part-9top-va-htop-utilitalarini-ornatish-va-ishlatish)

10.[Part 10](#part-10fdisk-utilitasidan-foydalanish)

11.[Part 11](#part-11df-utilitasidan-foydalanish)

12.[Part 12](#part-12du-utilitasidan-foydalanish)

13.[Part 13](#part-13ncdu-utilitasini-ornatish-va-undan-foydalanish)

14.[Part 14](#part-14tizim-jurnalari-bilan-ishlash)

15.[Part 15](#part-15cron-ish-rejalashtiruvchisi)


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
![img](screen/7.0.png)

**Har uchta tanlangan muharrirni ishlatib, test_X.txt faylini yarating, bunda X fayl yaratilgan muharrir nomi bo'ladi. Fayl ichiga o'zingizning taxallusingizni yozing va faylni o'zgartirishlarni saqlagan holda yoping.**
![img](screen/7.1.png)

vim7

#### Chiqish:esc+:wq

nano
![img](screen/7.2.png)

#### Chiqish: control+o+x

mcedit
![img](screen/7.3.png)

Chiqish: f2+f10

***Har uchta tanlangan muharrirni ishlatib, faylni tahrirlash uchun oching, faylni tahrirlang va taxallus o‘rniga "21 School 21" qatorini yozing, so‘ngra faylni o‘zgartirishlarsiz yoping. vim**

![img](screen/7.4.png)
#### Chiqish:q!

nano
![img](screen/7.5.png)
Chiqish: control+x

mcedit
![img](screen/7.6.png)

#### Chiqish: f10

**Har uchta tanlangan muharrirda faylni yana bir bor tahrirlab chiqing (oldingi qadamga o‘xshash tarzda), so'ngra fayl mazmunida so‘zlarni qidirish va ularni boshqa so‘zga almashtirish funksiyalarini o‘rganing.**

#### vim Qidirish
![img](screen/7.7.png)

#### O'rnini bosish
![img](screen/7.8.png)

**/-Qidirish**

**nano Qidirish**
![img](screen/7.9.png)

#### O'rnini bosish - ``control/``
![img](screen/7.10.png)
![img](screen/7.11.png)

#### Qidirish ``control w``

``mcedit``

#### Qidirish -f7
![img](screen/7.12.png)
![img](screen/7.13.png)

#### Qidirish -f4
![img](screen/7.14.png)
![img](screen/7.15.png)
![img](screen/7.16.png)


## Part 8.SSHD xizmatini o'rnatish va asosiy sozlash 

**SSHd xizmatini o'rnatish.**

**Repository yangilanishi.**
![img](screen/8.0.png)

#### SSH o'rnatish
![img](screen/8.1.png)
#### OpenSSH o'rnatish
![img](screen/8.2.png)

#### Tizim yuklanayotganda xizmatni avtomatik ishga tushirishni qo'shish.
![img](screen/8.2.png)

#### SSH holati.
![img](screen/8.3.png)
#### SSHd xizmatini 2022-portga qayta sozlash:

![img](screen/8.4.png)

#### SSH-ni o'zgarishlarni saqlash uchun qayta ishga tushirish
![img](screen/8.5.png)
#### `ps` buyrug'idan foydalanib, sshd jarayonining mavjudligini ko'rsatish uchun kalitlarni tanlash kerak.
![img](screen/8.6.png)

`-tan:`

`t-TCP `protokoli bo'yicha

`a`- Barcha ulanishlar va kutilayotgan portlarni ko'rsatish.

`n`- Manzillar va port raqamlarini raqamli formatda ko'rsatish.

Ustunlar:

`Recv-Q `- Ushbu tugunda/kompyuterda qabul qilish navbatlarida turgan so'rovlar soni

`Send-Q` - Ushbu tugunda/kompyuterda jo'natish navbatlarida turgan so'rovlar soni

`Local Address` - Mahalliy soketning manzili va port raqami

`Foreign Address` - Uzoq soket manzili va port raqami

`State `- Soketning holati

Agar manzil sifatida 0.0.0.0 ko'rsatilgan bo'lsa, bu "har qanday manzil" degan ma'noni anglatadi, ya'ni bu ulanishda ushbu kompyuterda mavjud bo'lgan barcha IP-manzillar ishlatilishi mumkin.
![img](screen/8.7.png)

**-tps -aux | grep sshd** chiqishi:

- **ps** — sizning serveringizda hozirgi jarayonlarning ro'yxatini jadval ko'rinishida chiqaradi.
  
- **a** — fon jarayonlaridan tashqari barcha jarayonlarni tanlaydi.
  
- **u** — foydalanuvchi jarayonlarini tanlaydi.
  
- **x** — ps ga sizga tegishli barcha jarayonlarni ro'yxatga olishni buyuradi.



## Part 9.Top va Htop utilitalarini o'rnatish va ishlatish

**top va htop yordamchilarini o'rnating va ishga tushiring**

`top`
![img](screen/9.0.png)

`uptime`
![img](screen/9.1.png)
**Avtorizatsiyadan o'tgan foydalanuvchilar soni**
![img](screen/9.2.png)

**Tizimning umumiy yuklanishi**
![img](screen/9.3.png)
**Umumiy jarayonlar soni**
![img](screen/9.4.png)
**CPU yuklanishi**
![img](screen/9.5.png)
**Xotira yuklanishi**
![img](screen/9.6.png)
**Eng ko'p xotira egallovchi jarayonning PID raqami**
![img](screen/9.7.png)
**Eng ko'p protsessor vaqti sarflovchi jarayonning ``pid``si**
![img](screen/9.8.png)
**htop PID bo'yicha saralangan**
![img](screen/9.9.png)
**PERCENT_CPU** 
![img](screen/9.10.png)
**PERCENT_MEM**
![img](screen/9.11.png)
**TIME**
![img](screen/9.12.png)
**sshd jarayoni uchun filtrlash**
![img](screen/9.13.png)
**Qidiruv yordamida topilgan syslog jarayoni bilan**
![img](screen/9.14.png)
**`hostname`, soat va ``uptime`` chiqishini qo'shgan holda**
![img](screen/9.15.png)

## Part 10.Fdisk utilitasidan foydalanish

**fdisk -l buyrug'ini ishga tushirish.**
![img](screen/10.0.png)
### Ism
![img](screen/10.1.png)
**Hajmi 8.25 GB** 

**Sektorlar soni 88541755744**
![img](screen/10.0.png)

## Part 11.Df utilitasidan foydalanish

## Part 12.Du utilitasidan foydalanish

## Part 13.Ncdu utilitasini o'rnatish va undan foydalanish

## Part 14.Tizim jurnalari bilan ishlash

## Part 15.CRON ish rejalashtiruvchisi 