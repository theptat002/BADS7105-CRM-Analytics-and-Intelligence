## **Product Recommendation**

BADS7105 : CRM Analytics and Intelligence | Homework 7

Topic : Product Recommendation

Data : Customer Preference Survey.xlsx

## <ins>Explore data</ins>


<p>
 <img  width="650" height="345" src="./NUMBER_OF_ACTIVITY.JPG">
</p>

## <ins>Convert data to one-hot encoding</ins>

<p>
 <img  width="600" height="250" src="./Convert_data.JPG">
</p>

## <ins>Get Result</ins>

<p>
 <img   src="./Result_From_Apriori.JPG">
</p>

LIFT ->  lift ratio is the ratio of confidence to expected confidence. Expected confidence is the confidence divided by the frequency of B. The Lift tells us how much better a rule is at predicting the result than just assuming the result in the first place. Greater lift values indicate stronger associations.

<p>
 <img   src="./lift_formula.JPG">
</p>

SUPPORT -> the number of transactions that include items in the {A} and {B} parts of the rule as a percentage of the total number of transactions. It is a measure of how frequently the collection of items occur together as a percentage of all transactions.

<p>
 <img   src="./support_formula.JPG">
</p>

CONFIDENCE -> the confidence of the rule is the ratio of the number of transactions that include all items in {B} as well as the number of transactions that include all items in {A} to the number of transactions that include all items in {A}.

<p>
 <img   src="./confidence_formula.JPG">
</p>

ref : <url>https://infocenter.informationbuilders.com/wf80/index.jsp?topic=%2Fpubdocs%2FRStat16%2Fsource%2Ftopic49.htm</url>

### <ins>Lift x Support</ins>

<p>
 <img   src="./Lift_x_Support.png">
</p>

Example -> We should select activiry ->  low support/high condidence/high lift for recommend user. 

### <ins>Network x with Cosine</ins>

<p>
 <img   src="./networkx_graph.png">
</p>
