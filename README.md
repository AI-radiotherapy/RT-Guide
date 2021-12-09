# RT programming guide

Tutorial นี้ทำขึ้นเพื่อแนะนำการเขียนโปรแกรมสำหรับ radiotherapy เบื้องต้น สำหรับระบบ treatment planning (TPS) ของ Varian

TPS ของ varian นั้นจะมี API ที่ชื่อ ESAPI ที่เป็นชุดคำสั่งสำหรับเขียนโปรแกรมติดต่อกับระบบ TPS โดยรองรับภาษา C# และ Python ตัวอย่างโค้ดและ documents สามารถดูได้ที่ [link](https://varianapis.github.io/)

## Index

- [เริ่มต้นเขียนโปรแกรม](#เริ่มต้นเขียนโปรแกรม)
    - [Python](#python)
    - [C#](#c)
- [Library ที่ควรรู้จัก](##2.-library-ที่ควรรู้จัก)
- [การติดต่อกับ TPS และนำข้อมูลออกจากระบบ](#การติดต่อกับ-tps-และนำข้อมูลออกจากระบบ)
- [การ import file และ image processing เบื้องต้น](#file-io-and-image-processing)
- [อื่นๆ](#อื่นๆ)

---

## เริ่มต้นเขียนโปรแกรม

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

### C #

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

## Library ที่ควรรู้จัก

Python

- [Numpy](https://numpy.org/) ใช้สำหรับการคำนวณทางคณิตศาสตร์
- [Matplotlib](https://matplotlib.org/) ใช้สำหรับการ visualize data
- [SimpleITK](https://simpleitk.org/) ใช้สำหรับ image analysis

C#

- TODO

## การติดต่อกับ TPS และนำข้อมูลออกจากระบบ

การเขียนโปรแกรมติดต่อกับ Varian TPS โดยรวมแล้วแนะนำให้อ่านใน [Varian API Book](https://varianapis.github.io/VarianApiBook.pdf) โดยจะสอน ESAPI ทั้งภาษา C# และ Python

ในเรื่องที่ไม่มีใน Varian API Book เช่น

- การ export image (RTDose, CT, ROIs) สามารถดูได้ที่ [link](https://github.com/VarianAPIs/Varian-Code-Samples/blob/master/Eclipse%20Scripting%20API/plugins/Export3D.cs) (C#)
- ตัวอย่างโค้ดอื่นๆ และโค้ดจากงานสัมนาของ Varian สามารถดูได้ที่ [link](https://github.com/VarianAPIs)

## File IO and image processing

part นี้จะพูดถึงการอ่านไฟล์ที่เรา export ออกมาจาก TPS และ image processing เบื้องต้น (จริงๆแล้วใน Varian API Book และ example code จาก Github ของ Varian Developer ที่แนะนำใน Part ก่อน ก็มีตัวอย่างโค้ด image processing อยู่บ้างแล้ว)

Tools เบื้องต้นสำหรับอ่านไฟล์คือ

- [pydicom (python)](https://github.com/pydicom/pydicom) สำหรับอ่านไฟล์ DICOM
- [SimpleITK (python)](https://simpleitk.org/) สำหรับอ่านไฟล์ image อื่นๆ และ image processing [tutorial](http://insightsoftwareconsortium.github.io/SimpleITK-Notebooks/)
- [3D slicer](https://www.slicer.org/) ไฟล์ที่เรานำออกมาบางชนิดที่ไม่สามารถเปิดด้วย Library ด้านบนได้ สามารถเปิดในโปรแกรม 3D slicer เพื่อแปลงไฟล์ให้เป็นแบบที่เราต้องการ

Tools สำหรับ image processing

- [SimpleITK (python)](https://simpleitk.org/) สำหรับอ่านไฟล์ image อื่นๆ และ image processing [tutorial](http://insightsoftwareconsortium.github.io/SimpleITK-Notebooks/)
- [Numpy](https://numpy.org/) ใช้สำหรับการคำนวณทางคณิตศาสตร์
- [Matplotlib](https://matplotlib.org/) ใช้สำหรับการ visualize data

## อื่นๆ

section นี้จะแนะนำ resource อื่นๆที่อาจจะจำเป็นสำหรับการเขียนโปรแกรมหรือทำวิจัยทางด้าน radiotherapy

- [3D slicer](https://www.slicer.org/) เป็น Software สำหรับ medical image analysis ภาษาที่ใช้จะเป็น Python
- [pymedphys](https://github.com/pymedphys/pymedphys) เป็น Python library สำหรับ medical physics
- [matRad](https://e0404.github.io/matRad/) เป็น Software สำหรับ intensity-modulated photon, proton, and carbon ion therapy ภาษาที่ใช้จะเป็น MATLAB
- [Github](https://github.com/) คือเว็บไซด์ที่ใช้ Git ไว้สำหรับการจัดเก็บ code โดยสามารถหา public resources (code, tutorial) ที่คนอื่นได้เปิดไว้ให้เราได้อ่านหรือนำไปใช้ได้ฟรีๆอีกด้วยในบางโปรเจค
