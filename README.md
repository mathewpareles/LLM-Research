


This library tests GPT-3's reasoning ability on the LEGO reasoning task (https://arxiv.org/pdf/2206.04301.pdf).


We find evidence that GPT-3 uses a consistent attention pattern to solve the LEGO reasoning task. We hope to reverse-engineer this attention pattern and make it human-interpretable.


## Results

We find that performance scales linearly with the length of the hint, suggesting that GPT-3 consistently uses the same attention pattern across many versions of the LEGO reasoning task.

<p align="center">
<img src="images/1.png" alt="12 hints 1" width="300"/>
<img src="images/2.png" alt="12 hints 2" width="300"/>
</p>

<p align="center">
<img src="images/3.png" alt="20 hints 1" width="300"/>
<img src="images/4.png" alt="20 hints 2" width="300"/>
</p>


We considered various metrics of correctness (whether the model gave the correct answer verbatim or whether it gave the correct value) and various measurements of accuracy (the number of values correct, the location of the first incorrect response), and they all have a striking linear relationship between the hint size and GPT-3's accuracy.




## Cases


This library tests the following cases:


- Using various problem sizes (12, 16, and 20 variables)

- Adding spaces and commas between tokens

- Using words as variable names

- Padding the equals sign in the hint

- Padding the equals sign in the system of equations


