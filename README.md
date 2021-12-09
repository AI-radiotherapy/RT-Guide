# RT programming guide

Tutorial นี้ทำขึ้นเพื่อแนะนำการเขียนโปรแกรมสำหรับ radiotherapy เบื้องต้น สำหรับระบบ treatment planning (TPS) ของ Varian

TPS ของ varian นั้นจะมี API ที่ชื่อ ESAPI ที่เป็นชุดคำสั่งสำหรับเขียนโปรแกรมติดต่อกับระบบ TPS โดยรองรับภาษา C# และ Python ตัวอย่างโค้ดและ documents สามารถดูได้ที่ https://varianapis.github.io/


## Index

0. [เริ่มต้นเขียนโปรแกรม](#เริ่มต้นเขียนโปรแกรม)
    - [Python](#python)
    - [C#](#c)
1. [การติดต่อกับ TPS และนำข้อมูลออกจากระบบ](#การติดต่อกับ-tps-และนำข้อมูลออกจากระบบ)
2. [การอ่านไฟล์ข้อมูล](#การอ่านไฟล์ข้อมูล)
3. [Dosimetry เบื้องต้น](#dosimetry-เบื้องต้น)

---

## 1. เริ่มต้นเขียนโปรแกรม

พื้นฐานการเขียนโปรแกรมที่ควรมีในแต่ละภาษาส่วนมากจะคล้ายกัน ต่างกันแค่ syntax (โครงสร้างภาษา) เรื่องที่ควรรู้คือ

- Variables และชนิดของ variables
- Array or Lists
- Operator
- Conditional statement (if/else)
- Loop (For loop/while loop)
- Functions
- การใช้ library/modules
- Classes/Objects (เรื่องนี้อาจจะข้ามไปก่อนได้ แต่ถ้ารู้จะเข้าใจการเขียนโปรแกรมได้ไวขึ้น แนะนำว่าถ้าข้ามไปแล้วพอเขียนโปรแกรมไปสักพักให้กลับมาอ่านใหม่)

การเรียนเขียนโปรแกรมจะไปได้ไวขึ้นถ้าเราฝึกเขียนไปด้วย resources หลักๆจะมีหนังสือ วิดีโอ และ interactive website ซึ่งผมแนะนำ interactive website เนื่องจากไม่ต้อง set โปรแกรมในเครื่องตัวเองเหมาะสำหรับคนเรียนครั้งแรก หรือแล้วแต่ถนัด

### Python

ภาษาไทย

- [Kong Ruksiam Youtube](https://www.youtube.com/playlist?list=PLltVQYLz1BMBwqJysYnoEKWXUvqusJpgN) สอนตั้งแต่การติดตั้ง Python จนถึง Functions
- [marcuscode](http://marcuscode.com/lang/python) บทความสอน Python ภาษาไทย

ภาษาอังกฤษ

- [w3schools](https://www.w3schools.com/python) เป็น interactive website
- [Sololearn](https://www.sololearn.com/home) มีทั้ง ios และ android app แบบ interactive
- [FreeCodeCamp](https://www.youtube.com/watch?v=rfscVS0vtbw) youtube
- [Reddit learning resources](https://www.reddit.com/r/learnpython/wiki/index#wiki_new_to_python.3F) รวม tutorials สำหรับ python lists นี้บางแหล่งอาจจะเกินพื้นฐานไปบ้าง

### C#

ภาษาไทย

- [Kong Ruksiam Youtube](https://www.youtube.com/playlist?list=PLEE74DyIkwEm84UiA8fRGvJSecZaHZ9KY) สอนพื้นฐานครบ อาจจะขาดเรื่องการติดตั้งโปรแกรม
- [CBSknowledgeNET Youtube](https://www.youtube.com/playlist?list=PLFBv5UmF33FwhFnHXTNNQEq7uFop4v0i2) สอนตั้งแต่ติดตั้งโปรแกรม

ภาษาอังกฤษ

- [Microsoft tutorials](https://docs.microsoft.com/en-us/dotnet/csharp/tour-of-csharp/tutorials/) เป็น interactive website
- [w3schools](https://www.w3schools.com/cs/index.php) เป็น interactive website
- [Sololearn](https://www.sololearn.com/home) มีทั้ง ios และ android app แบบ interactive
- [FreeCodeCamp](https://www.youtube.com/watch?v=GhQdlIFylQ8) youtube
- [Caleb Curry](https://www.youtube.com/playlist?list=PL_c9BZzLwBRIXCJGLd4UzqH34uCclOFwC) youtube
- [Microsoft video](https://dotnet.microsoft.com/en-us/learn/csharp)

## 2. การติดต่อกับ TPS และนำข้อมูลออกจากระบบ

Guideline การ

## 3. การอ่านไฟล์ข้อมูล

## 4. Dosimetry เบื้องต้น
