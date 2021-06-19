## **Voice Analysis**
<p align="center">
 <img  width="500" height="300" src="./shabu-vector-35579589.jpg">
</p>

BADS7105 : CRM Analytics and Intelligence | Homework 9

Topic : Voice Analysis

Data : CustomerReviews.csv

### <ins>Explore</ins>

<ins>Rating of each merchant</ins>

<p >
 <img  src="./Plot_easy.png">
</p>

<ins>important word in review</ins>

<p >
 <img  src="./HM10_VOICE.png">
</p>

### <ins>Flow Process</ins>

<p >
 <img  src="./Flow Process.JPG">
</p>


### <ins>Process</ins>

#### <ins>Label review comment</ins>

<p >
 <img  src="./label_review.JPG">
</p>

Label -> each review relate about -> (Service , Food , Price) or (บริการ , อาหาร , ราคา )

#### <ins>Preparation data</ins>

<p >
 <img  src="./Clean_data.JPG">
</p>

Cleansing -> Cut punctuation / Only Thai x Eng / Tokenize(engine = newmm) then concat with space

#### <ins>Model Result</ins>

<p >
 <img  src="./Plot_Category_acc.png">
</p>

Model Accuracy One vs Rest with SVM Classification

#### <ins>Implement Test</ins>

<p >
 <img  src="./Predict_Imple.JPG">
</p>

Test with 1 review ><
