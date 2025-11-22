---
{"dg-publish":true,"dg-path":"Petroleum Engineering/how to convert mmbtu to boe.md","permalink":"/petroleum-engineering/how-to-convert-mmbtu-to-boe/","updated":"2025-09-04"}
---



This conversion depends on the premise of finding the energy content of one barrel of oil. See [[Areas/Petroleum Engineering/BOE is used to compare different forms of energy#^a61fc7\|BOE is used to compare different forms of energy#^a61fc7]]. For example, if we assume 1 boe contains 6 mmbtu (with the assumption of 1000 btu/scf), the conversion is simply multiply or divide.
$$
	\begin{align*}
		1 \space boe &= 6000 \space scf = 6 \times 10^{6} \space btu\\
		&= 6 \space mmbtu
	\end{align*}
	$$



### Thermal-Equivalent and Price-Equivalent Conversion

#### Thermal Equivalent Conversion
Let’s assume we have 100 Bscf of gas which has GHV of 1000 btu/scf
$$
\begin{align*}
	100 \space Bscf &= 100 \space Bscf \space \cdot 1000\frac{btu}{scf}\\
	&= 100,000 \space BBtu = 100,000,000 \space MMbtu\\\\
	&= 100,000,000 MMbtu \div 6 \frac{MMbtu}{boe}\\
	&= 16,666,667 \space boe = 16.667 \space MMboe
\end{align*}
$$


#### Price Equivalent Conversion
In price equivalent conversion, the factor is derived by dividing oil price to the gas price – getting the number MMbtu per bbl. In thermal conversion factor it is represented by $\frac{5.8 MMbtu}{bbl}$. However for price equivalent, the input variable is price denoted by $\frac{\$}{MMbtu \space or \space bbl}$. In order to get the factor, the calculation is as per below

let’s assume oil price of $70 per bbl and gas price of $4.5 per mmbtu}
$$

\begin{aligned}
	CF
	&= \frac{\$70/bbl}{\$4.5/mmbtu} \space \text{... and if we focus on the unit movement only ...}\\
	&= \frac{\frac{\$}{bbl}}{\frac{\$}{mmbtu}} = \frac{\$}{bbl}\times\frac{mmbtu}{\$} = \frac{mmbtu}{bbl}
\end{aligned}

$$




### Practical guide to convert prices USD/mmbtu ↔ USD/boe

Assume that we have 1 boe of gas with 1 boe is equivalent to 5.8 mmbtu. If gas price is USD4.5/mmbtu, that would mean for 5.8 mmbtu the price 4.5 x 5.8 = 26.1/boe. Here’s the calculation
$$
\begin{align}
1boe &= 5.8mmbtu\\
&= 5.8 mmbtu \times 4.5 \frac{USD}{mmbtu}\\
&= 26.1 USD\\\\
& \therefore \space \text{price is 5.8/mmbtu or 26.1/boe}
\end{align}
$$

- Quick rule of thumb is to get price in USD/boe is `USD/mmbtu × Conversion Factor` e.g. 6USD/mmbtu × 5.8mmbtu/boe
- Price in BOE should be higher i.e. USD 3/mmbtu = USD 18 per BOE (assume CF of 6)

## References
- [[journals/2022/04/2022-04-08#^ef7c77\|2022-04-08#^ef7c77]]