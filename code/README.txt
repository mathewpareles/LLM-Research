This notebook analyzes GPT's ability to solve LEGO problems (https://arxiv.org/pdf/2206.04301.pdf)

See points 3) and 4) below for results

1) In 'data_iterate.ipynb':

We iterate:

	Generate a LEGO system of equations (SOE) and a hint (HINT) towards solving it

	Define the string concatenation PROMPT = SOE + HINT

	Write the result to the './data' folder

2) In 'analysis.ipynb':

	We pass the various PROMPTs in './data' to GPT-3

	We then analyze the ACCURACY generated text. The graphs are our result

3) Tests:

3.* folders:

	0 0: Do not pad the equals sign '=' with spaces in the SOE, or in the HINT
	...Other folders are named similarly

	*Padding the equals sign in the HINT is very important toward GPT-3 generating the correct result

4.* folders:

	*GPT-3 successfully solves SOEs with many variables named numerically "a13 = -b20"

	*failure: SOE with variables named alphabetically "a = -b"

5.* folders:

	*success: variables whose tokens are spaced, ex. "a 1 0 = -b 7 2"

	*success when using a small SOE: variables whose tokens have commas between them, ex. "a,1,0 = -b,7,2"

6.* folders:
	
	*success: variables that are words, ex "the lazy = - dog"



4) Main question

	What is the underlying attention pattern here (i.e. the "circuit")? Does it generalize to other reasoning tasks?
	

