# pi_monte_carlo
Simple python program to estimate the value of pi using a classic monte-carlo simulation.

**Monte-Carlo Methods** <br />
A monte-carlo method relies on random sampling to derive a numerical result.

**Monte-Carlo Method for finding π** <br />
In this well-known approach, the value of π is estimated using a random number function which generates a number between 0 and 1.
Consider a circle of radius **r** which is placed inside a square with length **2r**; both the circle and square are centred at the origin.

<!-- ![pi_monte_carlo](https://user-images.githubusercontent.com/78542843/118504789-bdbdc100-b723-11eb-889b-a7ee2f7acc9c.png) -->
<img src="https://user-images.githubusercontent.com/78542843/118504789-bdbdc100-b723-11eb-889b-a7ee2f7acc9c.png" width="250" height="250">

If we were to pick a set of co-ordinates at random in the picture above, then the probability of our co-ordinates falling inside the circle is given by the area of the circle divided by the area of the square, i.e. **P(inside circle) = πr^2/(2r)^2**.
The random number function affords a method for generating random co-ordiantes.
Therefore, for a sample of **n** random co-ordinates, we can expect the ratio of co-ordinates falling inside the circle **(m)** to the total number of co-ordinates **(n)** to tend towards the probability **P(inside circle)**.
n.b. A large value of **n > 1000** is necessary to acquire a reasonably accurate estimation of **π**.

<br />
In fact, it is only necessary to consider a single quadrant of the picture above as πr^2/(2r)^2=(1/4)(πr^2)/r^2.
Calling the random number function twice generates an (x,y) co-ordinate for the upper-right quadrant of the square.
If we do this **n** times, counting how many times the co-ordinates fall inside the circle **m**, we can compute the probability **P(inside circle) = m/n**.
Given **P(inside circle) = πr^2/(2r)^2**, we can re-arrange the expression to find **π** like so π = 4(m/n).
