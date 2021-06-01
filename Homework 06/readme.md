## **Segmentation**

Homework 6 รายวิชา BADS7105 : CRM Analytics and Intelligence 

Topic : Segmentation 

Data : Supermarket

### <ins>Explore</ins>
ข้อมูลที่นำมาใช้จะเป็นข้อมูลที่อยู่ในรูปของ Transaction นะครับจะเป็นราย Basket Id (เดาว่าคือคีย์ของแต่ละ Bill นะ ><)
![chart](./Explore_Pic_01.JPG)





เริ่มต้นด้วยการสร้างตัวแปรขึ้นมาง่ายๆ 3 แง่มาตรฐานของการทำ Cluster เลยนั่นก็คือ R/F/M โดยที่ให้ลักษณะของแต่ละตัวแปลคือ
- R -> Recency | AVG_DATE_DIFF : แทนด้วยจำนวนวันเฉลี่ยที่ลูกค้าจะมาซื้อของที่ร้าน เช่น นาย B จะมาซื้อของทุกๆ 30 วัน เป็นต้น
- V -> Variety | C_PRO_CODE : ตัวแปรนี้จะเป็นความหลากหลายของสินค้าที่ลุกค้าเข้ามาซื้อต่อ Transaction ที่เกิดขึ้น
- M -> Monetary | AVG_TTL_AMT : Ticket size ต่อ transaction ของลูกค้า
