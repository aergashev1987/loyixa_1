# 01. Kirish (print, sintaksis, izoh, arifmetik amallar)

**Reja:**
- [Qayatirish uchun](#qayatirish-uchun)
- [0 Terminlar](#0-terminlar)
- [1 Print](#1-print)
  - [1.0 Turlicha ishlatilishi](#10-turlicha-ishlatilishi) 
  - [1.1 ' va " belgilari](#11--va--belgilari)
  - [1.2 Shakllarni ekranga chiqarish](#12-shakllarni-ekranga-chiqarish)
  - [1.3 Ko'p qatorli matnni chiqarish](#13-kop-qatorli-matnni-chiqarish)
  - [1.4 Bir nechta qiymat berish](#14-bir-nechta-qiymat-berish)
  - [1.5 Maxsus belgilar](#15-maxsus-belgilar)
- [2 Arifmetika](#2-arifmetika)
  - [2.1 Sodda amallar (+,-.*,/)](#21-sodda-amallar-)
  - [2.2 Butun qismini olish (//)](#22-butun-qismini-olish-)
  - [2.3 Qoldig'ini olish (%)](#23-qoldigini-olish)
  - [2.4 Darajaga oshirish (**)](#24-darajaga-oshirish)
  - [2.5 Murakkab misollar](#25-murakkab-misollar)
- [3 Izoh](#3-izoh)
  - [3.1 Bir qatorli izoh](#31-bir-qatorli-izoh)
  - [3.2 Ko'p qatorli izoh](#32-kop-qatorli-izoh)
- [4 Xatoliklar bilan ishlash](#4-xatoliklar-bilan-ishlash) 
- [5 Input](#5-input)

### Qayatirish uchun

#### Amallar

| Python | Nomi                        | Misol         | Natija |
|--------|-----------------------------|---------------|--------|
| +      | Qo'shish                    | print(4 + 2)  | 6      |
| -      | Ayirish                     | print(4 - 2)  | 2      |
| *      | Ko'paytirish                | print(4 * 2)  | 8      |     
| /      | Bo'lish                     | print(4 / 2   | 2.0    |
| //     | Bo'lib butun qismini olish  | print(5 // 2) | 2      |
| %      | Bo'lib qoldiq qismini olish | print(5 % 2)  | 1      |
| **     | Darajaga oshirish           | print(3 ** 3) | 27     |

#### Qiymatlar turi

| Qiymat                                     | Turi  | Misol                                            |
|--------------------------------------------|-------|--------------------------------------------------|
| 4                                          | son   | print(4)                                         |
| 10.4                                       | son   | print(10.4)                                      | 
| 'ab'                                       | yozuv | print('ab')                                      |
| "ab"                                       | yozuv | print("ab")                                      |
| """<br>Ismim: Otabek<br>Yoshim 13<br>"""   | yozuv | print("""<br>Ismim: Otabek<br>Yoshim 13<br>""")  |

#### print

| Bitta qiymat                       | Izoh                               | Natija               |
|------------------------------------|------------------------------------|----------------------|
| print(10)                          | son                                | 10                   |
| print('dastur')                    | yozuv                              | dastur               |
| print('yoshim', 13)                | ikkita qiymat: yozuv va son        | yoshim 13 da         |
| print('yoshim', 13, 'da')          | ikkita qiymat: yozuv, son va yozuv | yoshim 13 da         
| print('To'rtburchak yuzi', 23 * 4) | hisoblab natijani chiqarish        | To'rtburchak yuzi 92 |

#### Izoh

| Turi               | Izoh              |
|--------------------|-------------------|
| #                  | Bir qatorli izoh  |
| """ izoh <br/> """ | Ko'p qatorli izoh |

#### Prioritet

| Belgi | Nomi                                    | Tartibi |
|-------|-----------------------------------------|---------|
| ()    | qavs                                    | 1       |
| **    | darajaga oshirish                       | 2       |
| *,/,% | ko'paytirish, bo'lish, qoldig'ini olish | 3       |
| +, -  | qo'shish, ayirish                       | 4       |


### 0 Terminlar

```
qiymat         - 0,1,2, "abc", 'abc', 5.6, """Matn""",True, False
o'zgaruvchi    - son, soz1, _gap, guruh, Alfavit
qiymat turi    - bool(mantiqiy qiymat: True, False). Qiymatlar ma'nosi: True - haqiqat, False - yolg'on 
                 int(butun sonlar): -4, -2, 1, 5, 7 ..
                 float(haqiqiy sonlar): -4.5, 0, 6.6, 9,6 ..
                 str(matn, satr): 'soz', "soz", """soz"""
funksiya       - kodlarni qisqartirish uchun, ma'lum vazifani bajaradigan kodlarni ajratish uchun
print          - qiymatni ekranga chiqaradigan funksiya
input          - foydalanuvchidan qiymat o'qiydigan funksiya
parametr       - def summa(a, b): return a+b. Bu yerda a va b parametr 
argument       - print("Otabek"). Bu yerda "Otabek" argument  
debug          - dasturni xatolikka tekshirish
```

### 1 Print

#### 1.0 Turlicha ishlatilishi
```python
print(1)
print(1,2)
print(1+4)
print('bir' + ' ikki')
print('bir', ' ikki')
print("PC")
print("""Ko'p qatorli matn
1. Print
2. Input""")
print("\" - qo'shtirnoq")
print('" - qo\'shtirnoq')
print("' - birtirnoq")
print('\' - birtirnoq')
print('Birinchi qator\nIkkinchi qator')
print('Birinchi ustun\t\tIkkinchi ustun')
```
#### 1.1 ' va " belgilari

1. Ekranga "Assalom alaykum" yozuvini chiqarish:

Natija:
```text
Assalom alaykum
```

Yechim:
```python
print("Assalom alaykum")
```
yoki
```python    
print('Assalom alaykum')
```

2. Ekranga quyidagi yozuvni chiqarish

Natija:
```text
Mening ismim "Otabek"
```

Yechim:
```python  
print('Mening ismim "Otabek"')
```
yoki
```python  
print("Mening ismim \"Otabek\"")
```
3. Ekranga quyidagi yozuvni chiqarish

Natija:
```text
Men o'qishni a'lo baholar bilan bitirdim 
```

Yechim:
```python  
print("Men o'qishni a'lo baholar bilan bitirdim")
```
yoki
```python  
print('Men o\'qishni a\'lo baholar bilan bitirdim')
```
 
#### 1.2 Shakllarni ekranga chiqarish

1. Ekranga quyidagini chiqaring 

Naija:
```text
***********
*********
*******
*****
***
*
```

Yechim:
```python
print('***********')
print('*********')
print('*******')
print('*****')
print('***')
print('*')
```

2. Ekranga quyidagini chiqaring 

Natija:
```text
 ________________
|                |
|________________|
```

Yechim:
```pycon
print(' ________________')
print('|                |')
print('|________________|')
```

#### 1.3 Ko'p qatorli matnni chiqarish

1. Quyidagi yozuvni ekranga print funksiyasidan bir marta foydalangan holda ekranga chiqarish

Natija:
```text
Bu mening birinchi darsim
Birinchi darsda print ni o'rgandik
```

Yechim:
```python
print("""Bu mening birinchi darsim
Birinchi darsda print ni o'rgandik""")
```

2. Ekranga quyidagini print funksiyasini bir martta ishlatib chiqarish 

Natija:
```text
###########
###########
###########    
###########
```

Yechim:
```python
print('''
###########
###########
###########    
###########
''')
```

#### 1.4 Bir nechta qiymat berish

1. Eni 4 m va bo'yi 5 m bo'lgan to'rtburchak yuzini hisoblab chiqaradigan kod

Natija:
```text
To'rtburchak yuzi:  20
```

Yechim:
```python  
print("To'rtburchak yuzi: ", 4 * 5)
```

2. 2000$ ni necha so'm bo'lishini hisoblab, natijani chiqaradigan dastur (1$ kurs = 10933 so'm deb olamiz) 

Natija:
```text
2000$ = 21866000 
```

Yechim:
```python
print("2000$ = ", 2000 * 10933)
```

#### 1.5 Maxsus belgilar

| №   | Belgi | Vazifasi                   |
|-----|-------|----------------------------|
| 1   | \t    | Tab belgisini qo'yadi      |
| 2   | \n    | Bir qator pastga tushiradi |
| 3   | \\\   | \ belgisi                  |

1. Quyidagi natijani bir marta print funksiyasini ishlatgan holda ekranga chiqaring

Natija:
```text
Ismim:		Otabek
Yoshim:		34
```

Yechim:
```python  
print("Ismim:\t\tOtabek\nYoshim:\t\t34")
```

2. Ekranga quyidagi shaklni chiqaring 

Natija:
```text
     /\
    /  \    
   /    \
  /      \  
 /        \ 
/__________\
```

Yechim:

```python
print('''
     /\\
    /  \\    
   /    \\
  /      \\  
 /        \\ 
/__________\\''')
```

3. Quyidagi natijani \n bilan qatorlarni alohida qilib chiqarish

Natija:

```text
Ismim: Otabek
Yoshim: 30
Kasbim: dasturchi
```

Yechim:

```python
print("Ismim: Otabek\nYoshim: 30\nKasbim: dasturchi")
```

### 2 Arifmetika

#### 2.1 Sodda amallar (+,-.*,/)

1. 10ni 5 ga bo'lib natijani chiqarish

Natija:

```text
2.0
```
Yechim:

```python
print(10 / 5)
```
2. 20ni 15 ga qo'shib natijani chiqarish

Natija:
```text
35
```

Yechim:
```python
print(20 + 15)
```

3. 100dan 45ni ayirib natijani chiqarish

Natija:

```text
55
```

Yechim:
```python
print(100 - 45)
```

4. 18ni 5ga ko'paytirib natijani chiqarish

Natija:

```text
90
```

Yechim:
```python
print(18 * 5)
```

5. 18 * 5 + 10 - 20 / 5 ifodasini hisoblab natijani chiqaradigan dastur yozish

Natija:

```text
96.0
```

Yechim:
```python
print(18 * 5 + 10 - 20 / 5)
```

6. 18 * (5 + 10) / 5 ifodasini hisoblab natijani tushunarli qilib chiqaradigan dastur yozish

Natija:

```text
Natija: 54.0
```

Yechim:
```python
print("Natija: ", 18 * (5 + 10) / 5)
```

#### 2.2 Butun qismini olish (//)

1. 10ni 7ga bo'lib butun qismini chiqarish

Natija:
```text
1
```

Yechim:
```python
print(10 // 7)
```

2. 70 minut nechchi soat bo'lishini hisoblaydigan dastur (1 soat = 60 min)

Natija:
```text
1 soat
```

Yechim:
```python
print(70 // 60, "soat")
```

3. 733 sm nechchi metr ekanligini hisoblaydigan dastur (1 m = 100 sm) 

Natija:
```text
7 m
```

Yechim:
```python
print(733 // 100, "m")
```

#### 2.3 Qoldig'ini olish

1. 10 ni 7 ga bo'lganda necha qoldiq chiqishini hisoblaydigan dastur

Natija:
```text
3
```

Yechim:

```python
print(10 % 7)
```

2. 100 minutda 1 soatu necha minut borligini hisoblaydigan dastur

Natija:
```text
40 minut
```

Yechim:

```python
print(100 % 60, "minut")
```

3. 6100 gm da 6 kg va necha gm borligini hisoblaydigan dastur yozing

Natija:
```text
100 gm
```

Yechim:

```python
print(6100 % 1000, "gm")
``` 

#### 2.4 Darajaga oshirish

1. 3ni 4-darajasini hisoblaydigan dastur. 

Natija:
```text
3ni 4-darajasi 81
```

Yechim:
```python
print("3ni 4-darajasi", 3 ** 4)
```
yoki
```python
print(3 * 3 * 3 * 3)
```
Yuqoridagi ikkala holatda ham natija bir hil bo'ladi.

2. Kvadrati yuzi necha sm ekanligini hisoblovchi dastur. Kvadrat eni a=40 sm. (S = a * a)

Natija:
```text
Kvadrat yuzi: 1600 sm
```

Yechim:
```python
print('Kvadrat yuzi: ', 40 ** 2, "sm")
```

#### 2.5 Murakkab misollar

1. Quyida darajaga oshirish, butun qismini olish kabi amallar ishtirok etgan ifoda berilgan. Shuni hisoblab natijani ekranga tushunarli qilib chiqaradigan dastur

Natija: 
```text
(2 ** 3 + 10 / 5) // 5 = 2.0
```

Yechim:
```python
print("(2 ** 3 + 10 / 5) // 5 = ", (2 ** 3 + 10/5) // 5)
```

### 3 Izoh

#### 3.1 Bir qatorli izoh

1. Aylana yuzini hisoblovchi dastur yozing. Va buni izohga yozib qo'ying

Natija:

```text
157.0
```

Yechim:

 ```python
#aylana yuzi. R=5, Pi=3.14. S = 2*Pi*R*R
print(2 * 3.14 * 5 ** 2)
```

2. 400kunda necha hafta borligini, so'ng 300 min necha soat ekanligini hisoblovchi dasturni **izohlar bilan** yozing.  

Natija:

```text
57
5
```

Yechim:

 ```python
#400 kunda hafta soni
print(400 // 7)
# 300 minutda soatlar soni
print(300 // 60)
```

#### 3.2 Ko'p qatorli izoh

1. Aylana yuzini hisoblovchi dastur yozing. Va buni izohga yozib qo'ying

Natija: 
```text
157.0
```

Yechim:

```python
"""
    aylana yuzi
    pi=3.14
    R=5
    S = 2 * pi * R * R
"""

print(2 * 3.14 * 5 ** 2)
```


### 4 Xatoliklar bilan ishlash

```text
"Dasturning nega o'rganmoqchi?"
```

Yuqoridagi gapga tushundingizmi? Bilaman nima deb yozilganini tushunmadingiz, chunki grammatikada xatolik bor. Huddi shunday dasturlash tilida ham xatoliklar bo'ladi, ularni tushunib olsak, xatolikni bartaraf qilish oson bo'ladi. Bir qancha xatoliklarni ko'rib o'tamiz:

- **SyntaxError**. Kodingizda xatolik borligini bildiradi. Odatda bu jumladan so'ng,  tahminiy qayerda xato borligini ham aytadi. "Perhaps you forgot a comma" degani "Ehtimol siz "," (vergul) belgisini esdan chiqargansiz" degani. Orasiga "+" yoki "," belgisini qo'ysak ishlab ketadi. Qaysi birini qo'yishlik masalaga qarab bo'ladi
- **NameError**. O'zgaruvchi oldindan e'lon qilinmasa, kompyuter uni tanimaydi va mana shunday xatolik beradi. O'zgaruvchi nimaligini keyingi dars ko'ramiz
- **TypeError**. Toifalar bo'yicha xatolik. Masalan sonni so'zga qo'shib bo'lmaydi. Toifalar haqida keyingi darsda o'tamiz
- **IndentationError**: unexpected indent. Python da kodlar bir tekis yoziladi, agar ortiqcha ko'p joy tashlasangiz, mana shunday xatolik chiqadi

<h5>IndentationError</h5>

![](rasmlar/img.png)

<h5>NameError</h5>

![](rasmlar/img_5.png)

<h5>TypeError</h5>

![](rasmlar/img_6.png)

<h5>IndentationError</h5>

![](rasmlar/img_7.png)


1. Quyidagi dasturda xatolik bor. Bu yerdagi kodda + belgisi tushib qolgan

Natija:

```text
4
```

Kod:

```text
print(1 3)
```

Bu xato, aslida bunday bo'lishi kerak

Yechim:

```python
print(1 + 3)
```

2. Qiymat bilan o'zgaruvchini farqi bor

Kod:

```text
print(son)
```

bu xatolik, chunki son hali e'lon qilinmadi, aslida bunday bo'lishi kerak

Yechim:

```python
son = 3
print(son)
```

3. Siz Program so'zini chiqarmoqchisiz, lekin ' yoki " ni esdan chiqardingiz:

Kod:

```text
print(Program)
```

Bu xato kompyuter uni o'zgaruvchi deb o'ylaydi va bundan avvalgi kodlarda shu o'zgaruvchini e'lon qilinganligini tekshiradi, agar topmasa xatolik beradi, aslida

Yechim:

```python
print("Program")
```

yoki

```python
print('Program')
```

4. Sonlar bilan satrni qo'shib bo'lmaydi

Kod:

```text    
print(5 + "5")
```

Bu xato, aslida bunday bo'lishi kerak

Yechim:

```python
print(5 + 5)
```

5. print funksiyasi umuman hamma funksiyalar nomidan so'ng albatta () belgisi bo'ladi.

Kod:

```text
print "Ismim" + " Otabek"
```

Bu xato , aslida bunday bo'lishi kerak edi

Yechim:

```python
print("Ismim" + " Otabek")
```

yoki

```python
print("Ismim Otabek")
```

6. Kodlar bir tekis yozilishi kerak

Kod:

```text
print('Birinchi dars')
   print('Python')
print('Dasturlash asoslari')
```

Bu xato , aslida bunday bo'lishi kerak edi

Yechim:

```python
print('Birinchi dars')
print('Python')
print('Dasturlash asoslari')
```

### 5 Input

#### Turlicha ishlatilishi

```python
input("") # bu foydalanuvchiga umuman tushunarsiz
input("So'z kiriting") #kiritilgan qiymat matnga yopishib qoladi
input("So'z kiriting: ") #shunisi qulay
```


1. Foydalanuvchidan qiymat o'qish uchun input ishlatiladi

Natija:

```text
So'z kiriting: Otabek
```

Yechim:

```python
input("So'z kiriting: ")
```

2. Kiritilgan soz yordamida boshqa jumla yasab ekranga chiqarish

Natija:

```text
Ism kiriting: Otabek
Assalomu alaykum Otabek
```

Yechim:

```python
print("Assalomu alaykum " + input("Ism kiriting: "))
```

3. Foydalanuvchi kiritgan soz uzunligini chiqararamiz:

Natija:

```text
So'z kiriting: Otabek
So'z uzunligi:  6  ta belgidan iborat
```

Yechim:

```python
print("So'z uzunligi: ", len(input("So'z kiriting: ")), " ta belgidan iborat")
```

4. Quyidagi ko'rinishga ega dastur tuzing 

Natija:

```text
Belgi kiriting: !!
Kiritilgan belgini 2 ga ko'paytiramiz, natija: !!!!
```

Yechim: 

```python
print("Kiritilgan belgini 2 ga ko'paytiramiz, natija: " + input("Belgi kiriting: ") * 2)
```

