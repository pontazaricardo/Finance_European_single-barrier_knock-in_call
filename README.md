# Finance_European_single-barrier_knock-in_call

This is a CRR binomial tree program that prices European single-barrier knock-in calls on a dividend-paying stock, and also determines the relative error based on the call price using the [Black-Scholes model](https://en.wikipedia.org/wiki/Black%E2%80%93Scholes_model). 

![demo](/images/pics/demo.gif)

## Notes

Let *c1* be the price from the tree program and *c2* be the price from the Black-Scholes model. The relative error will be 100[(*c1* -*c2*)/*c2*] (%)

## Inputs and outputs

For this project, we have:
1. **Inputs:** *S* (stock price), *X* (strike price), *H* (barrier, smaller than *S*), *t* (years), *s* (volatility in %), *r* (interest rate in %), *q* (dividend yield in %), and *n* (number of periods).
2. **Output:** Price *c1* from the tree program, price *c2* from the Black-Scholes model and the relative error.

## Usage
In MatLab, just run the given file.

## Example
1. Suppose *S* = 95, *X* = 100, *H* = 90, *t* = 1 (year), *s* = 25 (%), *r* = 15 (%), *q* = 5 (%), and *n* = 192:
	1. The price given by the tree is *c1*=5.3840.
	2. The price given by the Black-Scholes model is *c2*=5.3844.
	3. The relative error is -0.0083%.
	
2. Suppose *S* = 95, *X* = 100, *H* = 90, *t* = 1 (year), *s* = 25 (%), *r* = 15 (%), *q* = 5 (%), and *n* = 193:
	1. The price given by the tree is *c1*=4.1270.
	2. The price given by the Black-Scholes model is *c2*=5.3844.
	3. The relative error is -23.3527%.