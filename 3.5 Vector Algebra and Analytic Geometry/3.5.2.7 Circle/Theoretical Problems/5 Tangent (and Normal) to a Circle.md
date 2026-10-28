
### 5 Tangent (and Normal) to a Circle



#### Exercise 1 - Gradient is normal to the level set

> [!question]
> Start with $F(x, y)=\left(x-x_0\right)^2+\left(y-y_0\right)^2-R^2$. Prove directly (using a directional derivative along a differentiable path on $F=0$ ) that $\nabla F$ is orthogonal to every tangent direction of the level set, hence normal to the circle at all points.
> 




#### Exercise 2 - Tangent line via the normal-line formula

> [!question]
> At $P=\left(x_1, y_1\right)$ on the circle, write the tangent as $\nabla F(P) \cdot((x, y)-P)=0$. Expand this to obtain
> 
> $$
> \left(x_1-x_0\right)\left(x-x_1\right)+\left(y_1-y_0\right)\left(y-y_1\right)=0
> $$
> 
> and then rearrange it into the center-point form
> 
> $$
> \left(x-x_0\right)\left(x_1-x_0\right)+\left(y-y_0\right)\left(y_1-y_0\right)=R^2 .
> $$
> 
> 
> Make clear where the identity $\left(x_1-x_0\right)^2+\left(y_1-y_0\right)^2=R^2$ is used.

#### Exercise 3 - Origin-centered special case

> [!question]
> Specialize Exercise 2 to $C=(0,0)$. Show that the tangent at $P=\left(x_1, y_1\right)$ is $x x_1+y y_1=R^2$. Explain geometrically why this is a dot product condition "position $\cdot$ radius $=R^2$ ".



#### Exercise 4 - Slope of the tangent as negative reciprocal

> [!question]
> Assuming $x_1 \neq 0$ and $y_1 \neq 0$, compute the slope of the radius $C P$ and use perpendicularity to derive the tangent slope $-x_1 / y_1$ (origin case) or, in general,
> 
> $$
> \left.\frac{d y}{d x}\right|_P=-\frac{x_1-x_0}{y_1-y_0} .
> $$
> 
> 
> Handle the horizontal/vertical exceptional cases separately and justify the limits.





#### Exercise 5 - Tangent from the translated implicit form

> [!question]
> Take the general implicit circle $x^2+y^2+2 m x+2 n y+q=0$. Using $F(x, y)=x^2+y^2+2 m x+ 2 n y+q$ and $\nabla F(P) \cdot((x, y)-P)=0$, derive
> 
> $$
> x x_1+y y_1+m\left(x+x_1\right)+n\left(y+y_1\right)+q=0
> $$
> 
> 
> Then verify the same formula by completing the square to find the center and applying the center-point form.

#### Exercise 6 - Agreement with the parametric method

> [!question]
> Parameterize the circle as $x(t)=x_0+R \cos t, y(t)=y_0+R \sin t$. Show that the tangent at $t=t_0$ is the line through $P=\left(x\left(t_0\right), y\left(t_0\right)\right)$ with direction vector $\left.\left(x^{\prime}, y^{\prime}\right)\right|_{t_0}=\left(-R \sin t_0, R \cos t_0\right)$. Convert this direction equation to the scalar equation of Exercise 2 and confirm they coincide.

#### Exercise 7 - Implicit differentiation check

> [!question]
> Differentiate $F(x, y)=0$ implicitly to obtain $2\left(x-x_0\right)+2\left(y-y_0\right) y^{\prime}(x)=0$. Evaluate at $P$ to recover
> 
> $$
> y^{\prime}\left(x_1\right)=-\frac{x_1-x_0}{y_1-y_0}
> $$
> 
> and reconcile with the slope you obtained in Exercises 3-4.



#### Exercise 8 - Tangency as double intersection

> [!question]
> Intersect the circle with its tangent line at $P$. Show that the resulting quadratic (in a line parameter) has a double root at $P$. Conclude that the discriminant vanishes and interpret this as "order-two contact," distinguishing tangency from secant intersection.




#### Exercise 9 - Distance-from-center characterization

> [!question]
> Prove that a line $\ell$ is tangent to the circle iff the (perpendicular) distance from the center $C$ to $\ell$ equals $R$. Derive this both (i) by discriminant of "circle $\cap$ line" and (ii) by projecting the radius onto the line's normal.

#### Exercise 10 - Normal line through $C$

> [!question]
> Show that the normal line at $P$ is the line $C P$. Write its equation in slope-intercept form when $x_1 \neq x_0$, and handle the vertical case $x=x_1$ when $x_1=x_0$. Verify that the tangent and normal are perpendicular by checking the product of their slopes (including the vertical/horizontal cases).

#### Exercise 11 - Alternative algebraic forms of the tangent

> [!question]
> In the origin-centered case, express the tangent at $P=\left(x_1, y_1\right)$ equivalently as
> 
> $$
> \operatorname{det}\left(\begin{array}{ccc}
> x & y & 1 \\
> x_1 & y_1 & 1 \\
> -x_1 & -y_1 & R^2
> \end{array}\right)=0
> $$
> 
> and show this expands to $x x_1+y y_1=R^2$. Explain how the third row encodes the circle's quadratic relation at $P$.



#### Exercise 12 - Reflection law via the normal (optional application check)

> [!question]
> Assume a ray hits the circle at $P$. Using the normal line $C P$, prove that the angle of incidence equals the angle of reflection if reflection is defined with respect to the normal. Reduce the statement to a vector equality using decomposition into components parallel and orthogonal to the normal.



#### Exercise 13 - Stability under rigid motions

> [!question]
> Let $Q$ be a $2 \times 2$ orthogonal matrix and $T \in \mathbb{R}^2$. Apply the change of variables $(x, y) \mapsto Q(x, y)+T$ to $F(x, y)=0$ and to the tangent equation at $P$. Show that "circle + tangent at $P$ " carries to "circle + tangent at $Q P+T^{\prime \prime}$, preserving perpendicularity.

