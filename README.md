

## Goal

How does GPT-3 solve reasoning tasks?


In this library, we provide evidence that GPT-3 uses simple attention patterns to solve reasoning tasks.
Specifically, we show that GPT-3 uses a consistent approach to solve the [LEGO reasoning task](https://arxiv.org/pdf/2206.04301.pdf), regardless of the size, syntax, or scrambling of the input. 
This suggests that GPT-3 has an internal circuit that it consistently uses during this task. 

We hope to reverse-engineer this circuit and make it human-interpretable. 


## Results

We find that GPT-3's performance scales linearly with the length of the hint it is given, on all versions of the LEGO reasoning task that we tested. This suggests that GPT-3 uses the same attention pattern each time it solves the task.

<p align="center">
<img src="images/1.png" alt="12 hints 1" width="300"/>
<img src="images/2.png" alt="12 hints 2" width="300"/>
</p>

<p align="center">
<img src="images/3.png" alt="20 hints 1" width="300"/>
<img src="images/4.png" alt="20 hints 2" width="300"/>
</p>




## Cases


This library tests the following cases:


- Using various problem sizes (12, 16, and 20 variables)

- Adding spaces and commas between tokens

- Using words as variable names

- Padding the equals sign in the hint

- Padding the equals sign in the system of equations


