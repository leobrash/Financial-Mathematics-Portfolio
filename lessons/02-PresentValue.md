# 2. Present Value

[Back to contents](../README.md)

## Summary
- Present Values:
    - Cash Flows: Sequence of payments specified by the amount $C$ and the time $t$. So a sequence of cashflows is denoted $C_1, C_2, \ldots, C_n$ paid at times $t_1, t_2, \ldots, t_n$.
    - Assets & Liabilities: An asset is a positive cash flow & a liability is a negative cash flow.

    - Present Value (PV): The present value $P$ at time $t$ is the amount you must deposit now so at time $t$ you have $P_t$.

    - Discount Factor (D(t)): The discount factor $D(t)$ to time $t$ is the present value of 1 unit of cash at time $t$.

    - Different Present Values and Discount Factors:
        - Compounded Annually: For a nominal rate $r$ and cashflow $C$ paid in $t$ years the present value is $PV = \frac{C}{(1+r)^t}$ with discount factor to $t$ years $D(t) = \frac{1}{(1+r)^t}.$

        - Effective rate: For an effective rate $r_{\text{eff}}$ and cashflow $C$ paid in $t$ years the present value is $PV = \frac{C}{(1+r_{\text{eff}})^t}$ with discount factor to $t$ years $D(t) = \frac{1}{(1+r_{\text{eff}})^t}.$

        - Compounded Monthly: For a monthly compounded rate $r$ and cashflow $C$ paid in $t$ years the present value is $PV = \frac{C}{(1+\frac{r}{12})^{12t}}$ with discount factor to $t$ years $D(t) = \frac{1}{(1+\frac{r}{12})^{12t}}.$

        - Continuously Compounded Rate: For a continuously compounded interest rate $r$ and cashflow $C$ paid in $t$ years the present value is $PV = Ce^{-rt}$ with discount factor to $t$ years $D(t) = e^{-rt}.$

  - Net Present Value (NPV): The sum of the present values of a sequence of cashflows $C_1, C_2, \ldots, C_n$ paid at times $t_1, t_2, \ldots, t_n$. $NPV = \sum_{i=1}^{n} D(t_i) \cdot C_i.$

  - Balanced: Assets and liabilities are balanced if $NPV = 0$.

  - NPV Analysis: $NPV > 0$ suggests investment was good and $NPV < 0$ suggests investment was bad.

- Rates of Return:
    - Amount $P$ which later results in value $P_{\text{final}}$. The return on the investment is the quantity $P_{\text{final}}$. The profit is the difference $P_{\text{final}} - P$. The rate of return is: $R = \frac{P_{\text{final}}-P}{P}.$

    - Equivalent Effective Rate: Standardized equation to compare rates of return. $\left(\frac{P_{\text{final}}}{P}\right)^{1/t}-1.$

    - Annualized Rate of Return: $r = \frac{R}{T}.$

    - Internal Rate of Return (IRR): For a sequence of cashflows $C_0, C_1, \ldots, C_n$ at times $t_0, t_1, \ldots, t_n$. The IRR is the unique rate $r$ that satisfies $C_0 + \frac{C_1}{(1+r)^{t_1}} + \cdots + \frac{C_n}{(1+r)^{t_n}} = 0.$

- Market Risk:
    - Rates fluctuate and change based on a variety of factors.

## My example

Suppose John invests £100 into the S&P 500. His initial investment is now valued at £150. What is the rate of return? 

$$R = \frac{P_{\text{final}}-P}{P} = \frac{150-100}{100} = 0.5 = 50\\%.$$

## Solved exercises

### Exercise 2.1 

Calculate the internal rate of return of an investment that, for an initial £1,000, gives payments of £500 at the end of the second year and £750 at the end of the fourth year.

$$
-1000 + \frac{500}{(1+r)^2} + \frac{750}{(1+r)^4} = 0
$$

Let

$$
x = \frac{1}{(1+r)^2}
$$

Then 

$$ 
-1000 + 500x + 750x^2 = 0 \Rightarrow 3x^2 + 2x - 4 = 0
$$

Using the quadratic formula:

$$
x = \frac{-2 \pm \sqrt{2^2-4(3)(-4)}}{6} \Rightarrow x = \frac{-2 \pm \sqrt{52}}{6} \Rightarrow x = -1.535183758 \ \text{or} \ x= 0.8685170918.
$$

Since $x = \frac{1}{(1+r)^2} > 0$ we only consider the positive branch. 

$$
0.8685170918 = \frac{1}{(1+r)^2} \Rightarrow \frac{1}{0.8685170918} = (1+r)^2 \Rightarrow \sqrt{\frac{1}{0.8685170918}} = 1+r \Rightarrow \sqrt{\frac{1}{0.8685170918}} -1 = r
$$

$$
\Rightarrow r = 0.073 \Rightarrow r = 7.3\%
$$


## Spreadsheet

[02-PresentValue.xlsx](../spreadsheets/02-PresentValue.xlsx): This spreadsheet calculates the NPV and IRR of a series of cash flows over time. The user can enter up to 100 dates and corresponding cash flows in cells A6/B6 through A105/B105. The rate can be adjusted in cell F3. The spreadsheet then calculates present value of each cash flow and the NPV. The user can compare the calculated NPV with Excel functions that do so. The goal is to adjust the rate until the NPV reaches 0. 
