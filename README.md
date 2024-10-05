
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
#### Foydalanuvchini yaratish:

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


#### Foydalanuvchini `/etc/passwd` faylida tekshirish:
```bash
   /etc/passwd
   ```
![img](screen/2.3.png)

