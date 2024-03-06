# How does GPT Solve Equations?



This repository analyzes GPT-3's ability to solve reasoning problems when provided a hint. We find that GPT-3's performance scales linearly with the length of the hint when solving the LEGO reasoning task (https://arxiv.org/pdf/2206.04301.pdf). 


This suggests that at no point does GPT-3 "understand" the task, and that GPT is simply using simple Induction Heads and other simple circuits to produce a response. We hope to find the exact attention pattern that GPT-3 is using to solve this task.




## Results

Here are plots of our results. This is strong evidence that performance scales linearly with the length of the hint. 

<p align="center">
<img src="images/1.png" alt="12 hints 1" width="300"/>
<img src="images/2.png" alt="12 hints 2" width="300"/>
</p>

<p align="center">
<img src="images/3.png" alt="20 hints 1" width="300"/>
<img src="images/4.png" alt="20 hints 2" width="300"/>
</p>


We considered various metrics of correctness (whether the model gave the correct answer verbatim or whether it gave the correct value) and various measurements of accuracy (the number of values correct, the location of the first incorrect response), and they all have a roughly linear relationship between the hint size and GPT-3's accuracy.




## Cases



We tested these cases:


- Using various problem sizes (12, 16, and 20 variables)

- Adding spaces and commas between tokens

- Using words as variable names

- Padding the equals sign in the hint

- Padding the equals sign in the system of equations


