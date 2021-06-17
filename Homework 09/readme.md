## **A/B Testing**
<p align="center">
 <img  width="750" height="345" src="./BIG6_EPL.jpg">
</p>

BADS7105 : CRM Analytics and Intelligence | Homework 9

Topic : A/B Testing 

Data : excel file from questionnaire with gooogle form

### <ins>Explore</ins>

<ins>Supporters</ins>

<p align="center">
 <img  src="./Overall ratio support.png">
</p>

<ins>Frequency of Supporters x Hate </ins>

<p align="center">
 <img  src="./Overall ratio hater.png">
</p>

### <ins>Hypothesis test </ins>
#### Test the fans of each team dislike the other teams differently?

\>>> Chisquare test <<<  

* Arsenal

<p align="left">
 <img width="460" height="300" src="./Overall hate by Arsenal.png">
 
</p>

```diff
------------ ทดสอบสัดส่วนความของต่างของคนที่ชอบเชียร์ทีม -> Arsenal ------------

H0 : แฟนบอลที่เชียร์สโมสร Arsenal มีสัดส่วนในความไม่ชอบทีมอื่นๆใน Big6 ไม่แตกต่างกัน
H1 : แฟนบอลที่เชียร์สโมสร Arsenal มีสัดส่วนในความไม่ชอบทีมอื่นๆใน Big6 แตกต่างกัน
ที่ระดับนัยสำคัญ 0.05

แฟนบอลสโมสร Arsenal มีความไม่ชอบต่อสโมสรใน Big6 แตกต่างกันอย่างมีนัยสำคัญ โดยมีค่า P-Value = 0.015609416100266893

>>>>>>>>> ทีมที่แฟนบอลสโมสร Arsenal ไม่ชอบมากที่สุดคือ Manchester United <<<<<<<<<<
```

<p align="left">
 <img width="460" height="300" src="./Overall hate by Chelsea.png">
 
</p>

```diff
------------ ทดสอบสัดส่วนความของต่างของคนที่ชอบเชียร์ทีม -> Chelsea ------------

H0 : แฟนบอลที่เชียร์สโมสร Chelsea มีสัดส่วนในความไม่ชอบทีมอื่นๆใน Big6 ไม่แตกต่างกัน
H1 : แฟนบอลที่เชียร์สโมสร Chelsea มีสัดส่วนในความไม่ชอบทีมอื่นๆใน Big6 แตกต่างกัน
ที่ระดับนัยสำคัญ 0.05

แฟนบอลสโมสร Chelsea มีความไม่ชอบต่อสโมสรใน Big6 แตกต่างกันอย่างมีนัยสำคัญ โดยมีค่า P-Value = 4.442097828924892e-07

>>>>>>>>> ทีมที่แฟนบอลสโมสร Chelsea ไม่ชอบมากที่สุดคือ Liverpool <<<<<<<<<<
```

<p align="left">
 <img width="460" height="300" src="./Overall hate by Liverpool.png">
 
</p>

```diff
------------ ทดสอบสัดส่วนความของต่างของคนที่ชอบเชียร์ทีม -> Liverpool ------------

H0 : แฟนบอลที่เชียร์สโมสร Liverpool มีสัดส่วนในความไม่ชอบทีมอื่นๆใน Big6 ไม่แตกต่างกัน
H1 : แฟนบอลที่เชียร์สโมสร Liverpool มีสัดส่วนในความไม่ชอบทีมอื่นๆใน Big6 แตกต่างกัน
ที่ระดับนัยสำคัญ 0.05

แฟนบอลสโมสร Liverpool มีความไม่ชอบต่อสโมสรใน Big6 แตกต่างกันอย่างมีนัยสำคัญ โดยมีค่า P-Value = 3.9149319180782143e-28

>>>>>>>>> ทีมที่แฟนบอลสโมสร Liverpool ไม่ชอบมากที่สุดคือ Manchester United <<<<<<<<<<
```

<p align="left">
 <img width="460" height="300" src="./Overall hate by Manchester City.png">
 
</p>

```diff
------------ ทดสอบสัดส่วนความของต่างของคนที่ชอบเชียร์ทีม -> Manchester City ------------

H0 : แฟนบอลที่เชียร์สโมสร Manchester City มีสัดส่วนในความไม่ชอบทีมอื่นๆใน Big6 ไม่แตกต่างกัน
H1 : แฟนบอลที่เชียร์สโมสร Manchester City มีสัดส่วนในความไม่ชอบทีมอื่นๆใน Big6 แตกต่างกัน
ที่ระดับนัยสำคัญ 0.05

แฟนบอลสโมสร Manchester City มีความไม่ชอบต่อสโมสรใน Big6 แตกต่างกันอย่างมีนัยสำคัญ โดยมีค่า P-Value = 0.001598917522052272

>>>>>>>>> ทีมที่แฟนบอลสโมสร Manchester City ไม่ชอบมากที่สุดคือ Liverpool <<<<<<<<<<
```

<p align="left">
 <img width="460" height="300" src="./Overall hate by Manchester United.png">
 
</p>

```diff
------------ ทดสอบสัดส่วนความของต่างของคนที่ชอบเชียร์ทีม -> Manchester United ------------

H0 : แฟนบอลที่เชียร์สโมสร Manchester United มีสัดส่วนในความไม่ชอบทีมอื่นๆใน Big6 ไม่แตกต่างกัน
H1 : แฟนบอลที่เชียร์สโมสร Manchester United มีสัดส่วนในความไม่ชอบทีมอื่นๆใน Big6 แตกต่างกัน
ที่ระดับนัยสำคัญ 0.05

แฟนบอลสโมสร Manchester United มีความไม่ชอบต่อสโมสรใน Big6 แตกต่างกันอย่างมีนัยสำคัญ โดยมีค่า P-Value = 1.1571590660197325e-45

>>>>>>>>> ทีมที่แฟนบอลสโมสร Manchester United ไม่ชอบมากที่สุดคือ Liverpool <<<<<<<<<<
```

<p align="left">
 <img width="460" height="300" src="./Overall hate by Spurs.png">
 
</p>

```diff
------------ ทดสอบสัดส่วนความของต่างของคนที่ชอบเชียร์ทีม -> Spurs ------------

H0 : แฟนบอลที่เชียร์สโมสร Spurs มีสัดส่วนในความไม่ชอบทีมอื่นๆใน Big6 ไม่แตกต่างกัน
H1 : แฟนบอลที่เชียร์สโมสร Spurs มีสัดส่วนในความไม่ชอบทีมอื่นๆใน Big6 แตกต่างกัน
ที่ระดับนัยสำคัญ 0.05

แฟนบอลสโมสร Spurs มีความไม่ชอบต่อสโมสรใน Big6 ไม่แตกต่างกันอย่างมีนัยสำคัญ โดยมีค่า P-Value = 0.17558838731303802
```


ref :

<url>www.soccersuck.com</url>

<url>https://towardsdatascience.com/a-b-testing-with-chi-squared-test-to-maximize-conversions-and-ctrs-6599271a2c31</url>
