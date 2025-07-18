## จองรถส่งสินค้าหน่อย

บริษัท ModCom Express มีรถตู้อยู่ 3 คันที่พนักงานสามารถนำไปใช้สำหรับจัดส่งสินค้าแบบด่วนพิเศษใส่ไข่ได้ โดยรถตู้คันที่หนึ่ง สอง และสาม มีรหัสประจำรถว่า A B และ C ตามลำดับ ข้อกำหนดในการนำไปใช้มีอยู่ว่าพนักงานจะต้องทำการจองรถก่อน โดยคำสั่งจองจะต้องระบุจำนวนวันที่จะใช้  
จากนั้นผู้จองจะได้รถตู้ที่ว่างให้ใช้เร็วที่สุดเท่าที่หาได้จากหนึ่งในสามคันนั้น

ในกรณีที่มีรถตู้ว่างให้ใช้เร็วที่สุดมากกว่าหนึ่งคันและ A ว่างให้ใช้เร็วที่สุด A จะถูกเลือกก่อน B และ C (เป็นไปได้ว่าจะว่างให้ใช้เร็วที่สุดพร้อมกันทั้งสามคัน หรือแค่สองคันซึ่งเป็น A กับ B หรือ A กับ C ก็ได้) ถ้า A ไม่ได้ว่างให้ใช้เร็วที่สุด แต่เป็น B กับ C ที่ว่างให้ใช้ได้เร็วที่สุดพร้อมกันทั้งคู่ รถ B จะถูกเลือกก่อน C นอกจากนี้การจองจะให้ความสำคัญกับคำสั่งจองที่มาก่อนเสมอ สำหรับการจองแต่ละครั้ง ผู้จองจะได้รับคำตอบกลับมาว่าจะได้ใช้รถคันใด ซึ่งมีเกณฑ์การเลือกรถเป็นไปตามที่อธิบายไว้ก่อนหน้า

จงเขียนโปรแกรมที่รับจำนวนคำสั่งจอง N และคำสั่งจองทั้ง N คำสั่ง จากนั้นคำนวณว่ารถคันใดจะถูกนำไปใช้กับคำสั่งจองแต่ละคำสั่ง โดยหากเป็นรถ A โปรแกรมจะพิมพ์ข้อความว่า A และขึ้นบรรทัดใหม่ ถ้าเป็นรถ B หรือ C ก็จะพิมพ์ผลลัพธ์ออกมาในลักษณะเดียวกัน

---

## ข้อมูลนำเข้า (Input)

- บรรทัดแรกระบุจำนวนคำสั่งจองเป็นจำนวนเต็มบวก N โดยที่ 1 ≤ N ≤ 10,000  
- บรรทัดที่ 2 ถึง N + 1 ระบุคำสั่งจองเรียงตามลำดับการขอ (บรรทัดที่มาก่อนหมายถึงขอจองก่อน) ในแต่ละบรรทัดประกอบด้วยเลขจำนวนเต็มบวกหนึ่งตัวคือ t โดยที่ 1 ≤ t ≤ 15 (นั่นคือจองรถตู้ได้ครั้งละ 1 ถึง 15 วัน)

---

## ข้อมูลส่งออก (Output)

- มีทั้งหมด N บรรทัด โดยแต่ละบรรทัดระบุว่ารถคันใดจะถูกนำไปใช้กับคำสั่งจองแต่ละคำสั่ง โดยผลลัพธ์เรียงตามลำดับคำสั่งจอง

---

## ตัวอย่างกรณีทดสอบ

| Input                                    | Output                               |
| ---------------------------------------- | ------------------------------------ |
| 6<br>3<br>1<br>2<br>2<br>2<br>1          | A<br>B<br>C<br>B<br>C<br>A           |
| 6<br>1<br>2<br>2<br>1<br>1<br>3          | A<br>B<br>C<br>A<br>A<br>B           |
| 7<br>2<br>2<br>1<br>1<br>1<br>3<br>1     | A<br>B<br>C<br>C<br>A<br>B<br>C      |

---

## คำอธิบายเพิ่มเติม

ในส่วนตรงนี้จะเป็นคำอธิบายของตัวอย่าง Testcase ที่ 1 เพื่อให้เห็นรูปแบบการทำงานตามโจทย์

| Input                                    | Output                               |
| ---------------------------------------- | ------------------------------------ |
| 6<br>3<br>1<br>2<br>2<br>2<br>1          | A<br>B<br>C<br>B<br>C<br>A           |

- บรรทัดที่ 1: เลข 6 ในคือจำนวนคำสั่งจองที่จะต้องคำนวณ
- บรรทัดที่ 2: เลข 3 คือจำนวนวันที่จะใช้รถ เนื่องจากในตอนแรกรถทุกคันว่างหมดจึงเลือกใช้รถ A ตรงนี้ควรจำไว้ด้วยว่ารถ A จะว่างใช้อีกทีในวันที่ 4
- บรรทัดที่ 3: เลข 1 คือจำนวนวันที่จะใช้รถ เนื่องจากตอนนี้รถที่ว่างใช้ได้เร็วที่สุดคือ B และ C จึงเลือก B ก่อน เช่นเดิมจำไว้ด้วยว่า B จะว่างใช้อีกทีในวันที่ 2
- บรรทัดที่ 4: เลข 2 คือจำนวนวันที่จะใช้รถ เนื่องจากตอนนี้รถที่ว่างใช้ได้เร็วที่สุดคือ C จึงเลือก C เช่นเดิมจำไว้ด้วยว่า C จะว่างใช้อีกทีในวันที่ 3
- บรรทัดที่ 5: เลข 2 คือจำนวนวันที่จะใช้รถ เนื่องจากตอนนี้รถที่ว่างใช้ได้เร็วที่สุดคือ B จึงเลือก B เช่นเดิมจำไว้ด้วยว่า B จะว่างใช้อีกทีในวันที่ 2 + 2 = 4
- บรรทัดที่ 6: เลข 2 คือจำนวนวันที่จะใช้รถ เนื่องจากตอนนี้รถที่ว่างใช้ได้เร็วที่สุดคือ C จึงเลือก C เช่นเดิมจำไว้ด้วยว่า C จะว่างใช้อีกทีในวันที่ 3 + 2 = 5
- บรรทัดที่ 7: เลข 1 คือจำนวนวันที่จะใช้รถ เนื่องจากตอนนี้รถที่ว่างใช้ได้เร็วที่สุดคือ A และ B จึงเลือก A

---