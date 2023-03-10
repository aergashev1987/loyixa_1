# 11. Lug'at (dict) bilan ishlash 

**Reja:**
<!-- TOC -->
* [1 Elementlardan foydalanish](#1-elementlardan-foydalanish)
    * [Kalitlarini olish](#kalitlarini-olish)
    * [Qiymatlarini olish](#qiymatlarini-olish)
    * [Elementlarni olish](#elementlarni-olish)
    * [Lug'atda kalit borligini tekshirish](#lugatda-kalit-borligini-tekshirish)
* [2 Element o'zgartirish](#2-element-ozgartirish)
* [3 Element qo'shish](#3-element-qoshish)
* [4 Element o'chirish](#4-element-ochirish)
* [5 Tsiklda ishlatilishi](#5-tsiklda-ishlatilishi)
* [6 Lug'atdan nusxa olish](#6-lugatdan-nusxa-olish)
* [7 Ichma-ich lug'at](#7-ichma-ich-lugat)
* [8 Metodlar](#8-metodlar)
<!-- TOC -->

```
key - kalit. {"nomi": "Otabek", "yoshi":23}. Bu yerda kalit "nomi" va "yoshi"
value - qiymat. {"nomi": "Otabek", "yoshi":23}. Bu yerda kalit "Otabek" va 23
```


![](images/dict.png)
```python

```
dict - lug'at ko'rinishida birdan ko'p ma'lumotlarni o'zida saqlaydi. U **kalit** va **qiymat** ko'rinishida ma'lumotlarni saqlaydi. Duplikat kalitlar bo'lmaydi, qiymatlarni o'zgartirsa bo'ladi. 
<br>

- Lug'at - bitta o'zgaruvchida bir nechta elementlarni saqlash uchun ishlatiladi
- Lug'at - tartiblangan (kalit bilan)
- Lug'atda qiymatni o'zgartirsa bo'ladi
- Duplikat kalitlar bo'lmaydi
- Alohida bitta elementidan foydalanish uchun [] belgilariga kalitni yozish bilan bo'ladi

### 1 Elementlardan foydalanish

1. Bo'sh lug'ar e'lon qilish:
```python
toplam = dict()
```
yoki
```python
toplam = {}
```
2. Bo'sh bo'lmagan lug'at e'lon qilish. Talaba haqida ma'lumot:
```python
talaba = {"ismi": "Anvar", "yoshi": 23, "bo'yi": 170}
```
Yuqoridagi kodni qulaylik uchun quyidagicha yozsa bo'ladi
```python
talaba = {
    "ismi": "Anvar", 
    "yoshi": 23, 
    "bo'yi": 170
}
```
2. Bo'sh bo'lmagan lug'at e'lon qilish. Kitob haqida ma'lumot:
```python
kitob = {
    "nomi": "Hadis va Hayot", 
    "beti": 300, 
    "yili": 2020
}
print(kitob)
```

```text
{'nomi': 'Hadis va Hayot', 'beti': 300, 'yili': 2020}
```
3. Bo'sh lug'atga ma'lumot kiritamiz:
```python
kitob = {}
kitob["nomi"] = "Hadis va Hayot" 
kitob["beti"] = 300 
kitob["yili"] =  2020
print(kitob)
```
```text
{'nomi': 'Hadis va Hayot', 'beti': 300, 'yili': 2020}
```
4. Lug'at uzunligini ekranga chiqarish

```python
kitob = {
    "nomi": "Hadis va Hayot", 
    "beti": 300, 
    "yili": 2020
}
print(f"Elementlar soni: {len(kitob)}")
```
```text
Elementlar soni: 3
```
5. Lug'atda turli toifali ma'lumotlarni saqlash
```python
lugat1 = {
    "str": "soz", 
    "bool": True,
    "int": 123,
    "float": 34.2
}
lugat2 = {
    "soz": "str", 
    True: "bool",
    123: "int",
    34.2: "float" 
}
```
```text
{'str': 'soz', 'bool': True, 'int': 123, 'float': 34.2}
{'soz': 'str', True: 'bool', 123: 'int', 34.2: 'float'}
```
Ko'rib turganingizdek turli toifalarni saqlashi mumkin. Xatto list,dict,tuple va boshqalarni ham
6. Murakkab toifali ma'lumotlarni saqlash
```python
lugat = {
    "maktab_raqami": 234,
    "sinflar": [1,2,3,4,5,6,7,8,9]         
}
print(lugat)
```

```text
{'maktab_raqami': 234, 'sinflar': [1, 2, 3, 4, 5, 6, 7, 8, 9]}
```
7. Bitta qiymatni ekranga chiqarish:

```python
kitob = {
    "nomi": "Hadis va Hayot", 
    "beti": 300, 
    "yili": 2020
}
print(f"Kitob nomi: {kitob['nomi']}")
```
Bu yerda agar kalit so'z hato bo'lsa, xatolik ro'y beradi<br>
yoki
```python
kitob = {
    "nomi": "Hadis va Hayot", 
    "beti": 300, 
    "yili": 2020
}
print(f"Kitob nomi: {kitob.get('nomi')}")
```
Bu yerda agar kalit so'z hato bo'lsa, None qaytadi<br>
```text
Kitob nomi: Hadis va Hayot
```
8. Agar meva bozorda bo'lmasa, "bunday meva bozorda yo'q" degan habar chiqsin:
```python
meva = input("Bozordan qaysi mevani qidiryapsiz: ")
bozor = {
    "olma": 5000,
    "nok": 10_000,
    "banan": 20_000,
    "anor": 10_000
}
print(f"Narxi: {bozor.get(meva, 'Bunda meva bozorda yoq')}")
```
```text
Bozordan qaysi mevani qidiryapsiz: olma
Narxi: 5000
```
```text
Bozordan qaysi mevani qidiryapsiz: malina
Narxi: Bunda meva bozorda yoq
```
##### Kalitlarini olish
9. Lug'atdagi hamma kalitlar ro'yxatini qaytarish:
```python
bozor = {
    "olma": 5000,
    "nok": 10_000,
    "banan": 20_000,
    "anor": 10_000
}
print(bozor.keys())
```
```text
dict_keys(['olma', 'nok', 'banan', 'anor'])
```
##### Qiymatlarini olish
10. Lug'atdagi hamma qiymatlar ro'yxatini qaytarish:
```python
bozor = {
    "olma": 5000,
    "nok": 10_000,
    "banan": 20_000,
    "anor": 10_000
}
print(f"Narxlar: {bozor.values()}")
```
##### Elementlarni olish
11. Bozordagi mevalarning ro'yxatini chiqaring:
```python
bozor = {
    "olma": 5000,
    "nok": 10_000,
    "banan": 20_000,
    "anor": 10_000
}
print(f"Bozor mevalari: {bozor.items()}")
```
```text
Bozor mevalari: dict_items([('olma', 5000), ('nok', 10000), ('banan', 20000), ('anor', 10000)])
```
##### Lug'atda kalit borligini tekshirish
12. Olma bozorda borligini tekshiring:
```python
bozor = {
    "olma": 5000,
    "nok": 10_000,
    "banan": 20_000,
    "anor": 10_000
}
if "olma" in bozor:
    print("Meva bozorda bor")
```

### 2 Element o'zgartirish

13. Lug'atdagi qiymatni o'zgartisih:
```python
bozor = {
    "olma": 5000,
    "nok": 10_000,
    "banan": 20_000,
    "anor": 10_000
}
print(f"Bozor mevalari: {bozor}")
bozor["anor"] = 20_000
print(f"Bozor mevalari: {bozor}")
```
```text
Bozor mevalari: {'olma': 5000, 'nok': 10000, 'banan': 20000, 'anor': 10000}
Bozor mevalari: {'olma': 5000, 'nok': 10000, 'banan': 20000, 'anor': 20000}
```

14. Lug'atni o'zlashtirib olgach, anorni narxini 3 barobar oshiring:
```python
bozor = {
    "olma": 5000,
    "nok": 10_000,
    "banan": 20_000,
    "anor": 10_000
}
print(f"Bozor mevalari: {bozor}")
bozor["anor"] *= 3
print(f"Bozor mevalari: {bozor}")
```
```text
Bozor mevalari: {'olma': 5000, 'nok': 10000, 'banan': 20000, 'anor': 10000}
Bozor mevalari: {'olma': 5000, 'nok': 10000, 'banan': 20000, 'anor': 30000}
```
Kalitni ko'rsatgan holda qiymatini o'zgartiramiz
15. talaba = {"ismi": "Anvar", "yoshi": 30} beriglan. Yoshini 20 ga o'zgartiring

```python
talaba = {"ismi": "Anvar", "yoshi": 30}
talaba["yoshi"] = 20
print(talaba)
```
yoki
```python
talaba = {"ismi": "Anvar", "yoshi": 30}
talaba.update({"yoshi": 20})
print(talaba)
```
```text
{'ismi': 'Anvar', 'yoshi': 20}
```
### 3 Element qo'shish
16. Bozor ro'yxatiga yana "malina" va "nok" mevalarini qo'shib yana kalitlar ro'yxatini ekranga chiqaring:
```python
bozor = {
    "olma": 5000,
    "nok": 10_000,
    "banan": 20_000,
    "anor": 10_000
}
print(f"Boshlang'ich lug'at {bozor.keys()}")
bozor["malina"] = 15_000
bozor["nok"] = 21_000
print(f"O'zgargan lug'at: {bozor.keys()}")
```
```text
Boshlang'ich lug'at dict_keys(['olma', 'nok', 'banan', 'anor'])
O'zgargan lug'at: dict_keys(['olma', 'nok', 'banan', 'anor', 'malina'])
```

17. Lug'atga foydalanuvchi tarafidan ma'lumot kiritish:
```python
kitob = {}
kitob["nomi"] = input("Kitob nomini kiriting: ")
kitob["beti"] = int(input("Kitob betini kiriting: "))
kitob["yili"] = int(input("Kitob yilini kiriting: "))
print(kitob)
```
yoki input() funksiyasini birdaniga lug'at ichiga yozamiz 
```python
kitob = {
    "nomi": input("Kitob nomini kiriting: "), 
    "beti": int(input("Kitob betini kiriting: ")),
    "yili": int(input("Kitob yilini kiriting: "))
}
print(kitob)
```
18. 3 so'zdan iborat o'zbekcha inglizcha lug'at bazasini yaratish:

```python
baza = {
    input("Inglizcha so'z kiriting: "): input("Inglizchaga mos o'zbekcha so'z kiriting: "), 
    input("Inglizcha so'z kiriting: "): input("Inglizchaga mos o'zbekcha so'z kiriting: "),
    input("Inglizcha so'z kiriting: "): input("Inglizchaga mos o'zbekcha so'z kiriting: "),
}
print(baza)
```
19. magazin = {"fanta": 7_000, "hurmo": 15_000} berilgan. Magazinga yana quyidagi mahsulotlarni ham qo'shing:<br>
- non - 2000 
- suv - 5000
```python
magazin = {"fanta": 7_000, "hurmo": 15_000}
magazin["non"] = 2_000
magazin["suv"] = 5_000
print(magazin)
```
yoki
```python
magazin = {"fanta": 7_000, "hurmo": 15_000}
magazin.update({"non": 2_000})
magazin.update({"suv": 5_000})
print(magazin)
```
```text
{'fanta': 7000, 'hurmo': 15000, 'non': 2000, 'suv': 5000}
```
### 4 Element o'chirish
- popitem() - ohrigi qo'shilgan elementni o'chirish
- pop() - kalit yordamida elementni o'chirish
- del - o'zgaruvchini yoki elementini xotiradan o'chirish
- clear - barcha elementlarini o'chirish

20. Quyida bozor ro'yxati berilgan ohirgi elementni o'chiring
```python
bozor = {
    "olma": 5000,
    "nok": 10_000,
    "banan": 20_000,
    "anor": 10_000
}
print(f"Avvalgi bozorlik ro'yxati: {bozor}")
element = bozor.popitem()
print(f"Keyingi bozorlik ro'yxati: {bozor}")
print(f"O'chirilgan element: {element}")
```
```text
Avvalgi bozorlik ro'yxati: {'olma': 5000, 'nok': 10000, 'banan': 20000, 'anor': 10000}
Keyingi bozorlik ro'yxati: {'olma': 5000, 'nok': 10000, 'banan': 20000}
O'chirilgan element: ('anor', 10000)
```

21. Quyida bozor ro'yxati berilgan. Ro'yxatdan olmani o'chiring:

```python
bozor = {
    "olma": 5000,
    "nok": 10_000,
    "banan": 20_000,
    "anor": 10_000
}
print(f"Avvalgi bozorlik ro'yxati: {bozor}")
qiymat = bozor.pop("olma")
print(f"Keyingi bozorlik ro'yxati: {bozor}")
print(f"O'chirilgan element narxi: {qiymat}")
```
yoki
```python
bozor = {
    "olma": 5000,
    "nok": 10_000,
    "banan": 20_000,
    "anor": 10_000
}
print(f"Avvalgi bozorlik ro'yxati: {bozor}")
qiymat = bozor["olma"]
del bozor["olma"]
print(f"Keyingi bozorlik ro'yxati: {bozor}")
print(f"O'chirilgan element narxi: {qiymat}")
```
```text
Avvalgi bozorlik ro'yxati: {'olma': 5000, 'nok': 10000, 'banan': 20000, 'anor': 10000}
Keyingi bozorlik ro'yxati: {'nok': 10000, 'banan': 20000, 'anor': 10000}
O'chirilgan element narxi: 5000
```
22. Bozorlik ro'yxatidan hamma elementni o'chiring:
```python
bozor = {
    "olma": 5000,
    "nok": 10_000,
    "banan": 20_000,
    "anor": 10_000
}
print(f"Bozorlik ro'yxati: {bozor}")
bozor.clear()
print(f"O'chirilgan ro'yxat: {bozor}")
```
### 5 Tsiklda ishlatilishi

```text
Bozorlik ro'yxati: {'olma': 5000, 'nok': 10000, 'banan': 20000, 'anor': 10000}
O'chirilgan ro'yxat: {}
```
23. Bozorlik elementlarini hamma kalitlarini alohida satrda ekranga chiqaring:
```python
bozor = {
    "olma": 5000,
    "nok": 10_000,
    "banan": 20_000,
    "anor": 10_000
}
for b in bozor:
    print(b)
```
yoki 
```python
bozor = {
    "olma": 5000,
    "nok": 10_000,
    "banan": 20_000,
    "anor": 10_000
}
for b in bozor.keys():
    print(b)
```

```text
olma
nok
banan
anor
```
24. Bozorlik elementlarini hamma kalitlarini va qiymatlarini alohida satrda ekranga chiqaring:
```python
bozor = {
    "olma": 5000,
    "nok": 10_000,
    "banan": 20_000,
    "anor": 10_000
}
for b in bozor:
    print(f"Mahsulot: {b}, narxi: {bozor[b]}")
```
yoki
```python
bozor = {
    "olma": 5000,
    "nok": 10_000,
    "banan": 20_000,
    "anor": 10_000
}
for kalit, qiymat in bozor.items():
    print(f"Mahsulot: {kalit}, narxi: {qiymat}")
```
```text
Mahsulot: olma, narxi: 5000
Mahsulot: nok, narxi: 10000
Mahsulot: banan, narxi: 20000
Mahsulot: anor, narxi: 10000
```

25. Endi bozorlik elementlarini hamma qiymatlarini alohida satrda ekranga chiqaring:
```python
bozor = {
    "olma": 5000,
    "nok": 10_000,
    "banan": 20_000,
    "anor": 10_000
}
print("Narxlar:")
for qiymat in bozor.values():
    print(qiymat)
```
yoki
```python
bozor = {
    "olma": 5000,
    "nok": 10_000,
    "banan": 20_000,
    "anor": 10_000
}
print("Narxlar:")
for _, qiymat in bozor.items():
    print(qiymat)
```
```text
Narxlar:
5000
10000
20000
10000
```
### 6 Lug'atdan nusxa olish
26. spark = {"brend": "GM","model": "Spark","yili": 2020} berilgan. O'zgaruchini boshqa o'zgaruvchiga ko'chiring, so'ng model va yilini foydalnuvchi kiritishini so'rang, so'ng ikkala modelni chiqaring
```python
spark = {"brend": "GM","model": "Spark","yili": 2020}
moshina = spark
moshina["model"] = input("Moshina modelini kiriting: ")
moshina["yili"] = int(input("Moshina yilini kiriting: "))
print(spark)
print(moshina)
```
```text
Moshina modelini kiriting:  Cobalt
Moshina yilini kiriting:  2022
{'brend': 'GM', 'model': 'Cobalt', 'yili': 2022}
{'brend': 'GM', 'model': 'Cobalt', 'yili': 2022}
```
Yuqoridagi kod **XATO**. Chunki set,dict, list toifalarini boshqa o'zgaruvchiga o'zlashtirganda xotiradan alohida joy ajratilmaydi. Natijada ma'lumot bitta, lekin nomi ikkita bo'lib qoladi. Uning uchun copy() metodidan foydalanamiz:

```python
spark = {"brend": "GM","model": "Spark","yili": 2020}
moshina = spark.copy()
moshina["model"] = input("Moshina modelini kiriting: ")
moshina["yili"] = int(input("Moshina yilini kiriting: "))
print(spark)
print(moshina)
```
```text
Moshina modelini kiriting:  Cobalt
Moshina yilini kiriting:  2022
{'brend': 'GM', 'model': 'Spark', 'yili': 2020}
{'brend': 'GM', 'model': 'Cobalt', 'yili': 2022}
```
### 7 Ichma-ich lug'at
Lug'atlar tarmoqli, ya'ni ichma-ich bo'lishi ham mumkin:
```python
oila = {
  "farzand1" : {
    "ismi" : "Anvar",
    "yili" : 2004,
    "status": "to'ng'ich"
  },
  "farzand2" : {
    "ismi" : "Lola",
    "yili" : 2010,
    "status": "singil"
  },  
    "farzand3" : {
    "ismi" : "Bekzod",
    "yili" : 1990,
    "status": "erka"
  }
}
print(oila)
```
```text
{'farzand1': {'ismi': 'Anvar', 'yili': 2004, 'status': "to'ng'ich"}, 'farzand2': {'ismi': 'Lola', 'yili': 2010, 'status': 'singil'}, 'farzand3': {'ismi': 'Bekzod', 'yili': 1990, 'status': 'erka'}}
```
27. aka, uka, singil degan lug'at toifali o'zgaruvchi yarating. So'ng ularni oila nomli lug'atda birlashtiring:
```python
aka = {
    "ismi" : "Anvar",
    "yili" : 2004,
    "status": "to'ng'ich"
}
singil = {
    "ismi" : "Lola",
    "yili" : 2010,
    "status": "singil"
}
uka = {
    "ismi" : "Bekzod",
    "yili" : 1990,
    "status": "erka"
}
oila = {
    "aka": aka,
    "uka": uka,
    "singil": singil
}
print(oila)
```
```text
{'aka': {'ismi': 'Anvar', 'yili': 2004, 'status': "to'ng'ich"}, 'uka': {'ismi': 'Bekzod', 'yili': 1990, 'status': 'erka'}, 'singil': {'ismi': 'Lola', 'yili': 2010, 'status': 'singil'}}
```

### 8 Metodlar
- a.clear() - a lug'atini bo'shatish
- a.copy() - a lug'atidan nusxa olish
- dict.fromkeys(["a","b"],100) - kalitlari "a" va "b" dan va hammasining qiymati 100 dan iborat lug'at yasab beradi: {"a": 100, "b": 100}   
- a.get(key) - a lug'atidan kaliti *key* ga teng bo'lgan qiymatni qaytaradi
- a.items() - a lug'atining har bir elementini *tuple*ga o'girib, ularning ro'yxatni qaytaradi: dict_items([('a', 100), ('b', 100)])
- a.keys() - a lug'atining kalitlar ro'yxatini qaytaradi: dict_keys(['a', 'b'])
- a.values() - a lug'atining qiymatlar ro'yxatini qaytaradi: dict_keys([1, 2])
- a.pop(key) - a lug'atidan kaliti *key*ga teng bo'lgan elementni o'chiradi
- a.popitem() - a lug'atidan ohiri elementni o'chiradi
- a.setdefault("k",200) - a lug'atidan kaliti *k* ga teng bo'lgan qiymatni qaytaradi, agar unday kalit bo'lmasa 200 ni qaytaradi va a lug'atga {"k": 200} ni ham qo'shib qo'yadi
- a.update({"c":100}) -a to'plamiga element qo'shish 

28. *mevalar* lug'ati berilgan. Undan kaliti banan ga teng bo'lgan element qiymatini qaytar va lug'atga o'zlashtir  
```python
mevalar = {
    "olma": 5_000,
    "nok": 6_000,
    'anor': 10_000
}
print(mevalar)
mevalar.setdefault('banan',10_000)
print(mevalar)

```

29. {"olma": 10_000, "nok": 10_000, "anor": 10_000} lug'atini hosil qiling. Qisqa kod bilan yozing.
```python
mevalar = dict.fromkeys(["olma", "nok", "anor"], 10_000)
print(mevalar)
```
```text
{'olma': 10000, 'nok': 10000, 'anor': 10000}
```