## **Segmentation**

Homework 6 รายวิชา BADS7105 : CRM Analytics and Intelligence 

Topic : Segmentation 

Data : Supermarket

### <ins>Explore</ins>

  ข้อมูลที่นำมาใช้จะเป็นข้อมูลที่อยู่ในรูปของ Transaction นะครับจะเป็นราย Basket Id (เดาว่าคือคีย์ของแต่ละ Bill นะ ><)

<p align="center">
 <img  src="./Explore_Pic_01.JPG">
</p>

ข้อมูลมาจะมี Feature ประกอบด้วย CUST_CODE , SHOP_DATE , BASKET_ID , BASKET_TYPE , C_PRO_CODE , QTY , AMT

```diff
- !!! C_PRO_CODE  : จำนวน Product Code ที่อยู่ในแต่ละบิล 

- !!! BASKET_TYPE : คาดการณ์ว่าเป็นประเภทของ SHOP 
```
ลองทำ Scatter Plot ดูความแตกต่างระหว่าง QTY กับ AMT โดยใช้สีแยกในแต่ละ BASKET TYPE ดูหน่อยว่าแตกต่างมั้ย

<p align="center">
 <img  width="460" height="300" src="./SCATTER_OVERALL.png">
</p>

อื้มม ก็พอจะเห็นว่าในแต่ละประเภทของ SHOP นั้นมีความแตกต่างกันอยู่ ฉะนั้น Segmentation ที่เราจะทำก็คงต้องสามารถอธิบายประเภทของร้านค้าพวกนี้ได้ด้วย(ละมั้ง)

<!-- ![table](./Explore_Pic_01.JPG) -->

### <ins>Create Feature for represent behavior</ins>

  เริ่มต้นด้วยการคิดอะไรไม่ออกก็ลองมองไปที่ RFM ก่อนเลย แต่ใน RFM นั้นผมว่าจะลองบิดตัวแปรบางตัวเช่น F นั้นเปลี่ยนเป็น ความหลากหลายในการซื้อสินค้าแทน
- R -> Recency | AVG_DATE_DIFF : แทนด้วยจำนวนวันเฉลี่ยที่ลูกค้าจะมาซื้อของที่ร้าน เช่น นาย B จะมาซื้อของทุกๆ 30 วัน เป็นต้น
- V -> Variety | C_PRO_CODE : ตัวแปรนี้จะเป็นความหลากหลายของสินค้าที่ลุกค้าเข้ามาซื้อต่อ Transaction ที่เกิดขึ้น
- M -> Monetary | AVG_TTL_AMT : Ticket size ต่อ transaction ของลูกค้า 
```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
