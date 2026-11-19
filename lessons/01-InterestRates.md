# 1. Interest rates

[Back to contents](../README.md)

## Summary

# Week 1: Interest Rates
- Interest Rates:
    - Principal ($P$ or $P_0$): Initial amount invested or borrowed.
    - Future Value ($P_t$ or $P_1$): Amount received at the end of investment, the principal plus interest.
    - Return: Future Value $-$ Principal, quantity earned in interest.
    - Percentage Return: $R = \frac{P_t - P}{P}.$
    - Nominal Interest Rate ($r$): Stated interest rate.
    - Simple Interest: Interest is calculated on original principal: $P_t = P(1+rt),$ where $t$ is the time in years.
    - Compound Interest: Interest is added to the principal, meaning future interest is calculated on previously accumulated interest periodically: $P_t = \left(1+\frac{r}{n}\right)^{nt}P,$ where $n$ is the number of compounding periods per year. For example, $n=1$ is compounded annually, $n=2$ is compounded semi-annually, $n=12$ is compounded monthly, etc.
    - Compounding Effective Rate ($r_{eff}$): Standardizes nominal interest rates with different compounding frequencies. $r_{\text{eff}} = \left(1+\frac{r}{n}\right)^n - 1.$
    - Continuously Compounded Interest: Interest is compounded at an infinite frequency, periods are incredibly small. $P_t = Pe^{rt}.$
    - Continuously Compounding Effective Rate ($r_{eff}$): $r_{\text{eff}} = e^r - 1.$
- Variable Interest Rates:
    - Instantaneous Interest Rate: A continuously compounded rate where the interest rate $r$ at time $t$ is equal to $r = r(t)$.
    - Instantaneous Interest Rate on $P$: $P_t = P e^{\int_0^t r(u)du}.$
    - Yield Curve: The average value of $r(t)$ on the interval $(0,t)$: $\bar{r}(t) = \frac{1}{t}\int_0^t r(u)du.$     
    - It follows $P_t = P e^{\bar{r}(t)t}.$
    - Effective Rate expressed in terms of the yield curve: $r_{\text{eff}}(t) = e^{\bar{r}(t)} - 1.$
- Inflation:
    - Prices increasing as a whole over time.
    - Real Interest Rate ($r_a$): $r_a = \frac{r-r_{\text{inf}}}{1+r_{\text{inf}}}.$

## My example
Bank A charges a 16% nominal rate compounded semi-annually whereas Bank B charges a 16% nominal rate compounded continuously. Which bank offers a better deal?

- Bank A: $r_{\text{eff}} = \left(1+\frac{0.16}{2}\right)^2 - 1 = 0.1664.$
- Bank B:$r_{\text{eff}} = e^{0.16}-1 = 0.1735.$
- We conclude that Bank A offers a better deal. 

## Solved exercises

### Exercise 1.8
Consider a deposit of \$1 that accrues a nominal interest rate of 100% compounded $n$ times a year. Calculate how much money you will have in the bank in one year as $n$ tends to infinity.

$$P(n) = \left(1+\frac{1}{n}\right)^n.$$

Taking the limit of $P(n)$ as $n$ approaches infinity:

$$\lim_{n\to\infty} P(n) = \lim_{n\to\infty}\left(1+\frac{1}{n}\right)^n = Pe^{r} = 1e^{1} = e.$$

### Exercise 1.11

From Capinski & Zastawniak, \*Mathematics for Finance: An Introduction to Financial Engineering\*.

In 1626 Peter Minuit, governor of the colony of New Netherland, bought the island of Manhattan from Native Americans paying with beads, cloth, and trinkets worth $24. Find the value of this sum in year 2026 at 5% compounded

(a) continuously, and
(b) annually. 

(a) 
$$P(t) = Pe^{rt} = P(400) = 24e^{0.05(400)} = 11643964700.$$

(b)
$$P(t) = P(1+r)^{t} = 24(1+0.05)^{400} = 7176800430.$$

## Spreadsheet

[01-InterestRates.xlsx](../spreadsheets/01-InterestRates.xlsx): what it
does, which cells to change and what to look at.
