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

เนื่องจากอยากได้ลักษณะของลุกค้าในแต่ละตัวแปรว่าปกติแล้วลูกค้าจะมีการเกาะกลุ่มกระจุกกันแบบไหนบ้างในแต่ละตัวแปรเลยทำการโยนแต่ละตัวแปรเข้าไปให้ Kmeans ทำการจัดกลุ่มให้กับเราเพื่อใช้ในการอธิบายลักษณะของลูกค้าให้กับเราละกัน

```diff
R -> AVG_DATE_DIFF : ไหนลองให้ Kmeans จัดกลุ่มให้เราซักหน่อยซิโดยใช้ Elbow Curve ในการเลือกตามใน spoil 
```

<details> 
  <summary>Elbow Curve with Fearture -> AVG_DATE_DIFF </summary>
  <p align="center">
    <img  width="460" height="300" src="./Elbow_recen.png">
    
    จิ้มๆเอาตรง 4 ละกัน กำลังหักข้อพอดี 5555
  </p> 
</details>

<details> 
  <summary>จากนั้นก็จัดการ Cluster ด้วย K-means Algorithm ตามจำนวน K ที่เลือก แล้วมาดูผลลัพท์กัน</summary>
  <p align="center">
    <img  src="./Kclus_recen.JPG">
    
    ก็จากผลลัพท์ที่ได้เลยลอง Groupby Data ด้วย Kmeans ที่แบ่งออกมาได้จึงสรุป Label ให้แต่ละกลุ่มออกเป็นดังนี้
    - Cluster 0 : ตั้งชื่อให้ว่าเป็นกลุ่มที่มีลักษณะมาซื้อสินค้าระดับ Quarterly ละกัน
    - Cluster 1 : ตั้งชื่อให้ว่าเป็นกลุ่มที่มีลักษณะมาซื้อสินค้าระดับ Yearly ละกัน
    - Cluster 2 : ตั้งชื่อให้ว่าเป็นกลุ่มที่มีลักษณะมาซื้อสินค้าระดับ Outlier ไปเลยนานๆใช้ทีไม่ดีเลยนะลูกค้ากลุ่มนี้
    - Cluster 3 : ตั้งชื่อให้ว่าเป็นกลุ่มที่มีลักษณะมาซื้อสินค้าระดับ Montly ละกัน กลุ่มนี้น่าจะเป็นกลุ่มลูกค้าที่ดีในแง่ของการมาซื้อของที่ร้าน เนื่องจากมาค่อนข้างบ่อย
    
    ##ลืมบอกไป ลูกค้าที่นำมา Cluster ในกลุ่มตัวแปรนี้จะตัดลูกค้าที่เคยมาซื้อของที่ร้านครั้งเดียวออกนะ กลุ่มนั้นก็จะถูกจำแนกเป็น Come Once ไปแทน
  </p> 
</details>


```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
