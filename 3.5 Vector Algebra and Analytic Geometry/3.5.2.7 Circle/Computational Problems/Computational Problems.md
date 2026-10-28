


## Calculations and Plotting

### 3. Parametric Representation of the Circle



#### Exercise 1: Parametric trace and Cartesian check.

> [!question]
> Fix $C=(x_0,y_0)=(2,-1)$ and $R=3$. Plot the parametric curve  
> $x(t)=x_0+R\cos t,\ y(t)=y_0+R\sin t$ for $t\in[0,2\pi]$. On the same axes, draw the level set $(x-x_0)^2+(y-y_0)^2=R^2$ (e.g., via a contour). Numerically evaluate $(x(t)-x_0)^2+(y(t)-y_0)^2$ at 200 uniform $t$\-samples and report the maximum absolute deviation from $R^2$.

#### Exercise 2: Periodicity and phase shifts.

> [!question]
> Plot $t\mapsto(x(t),y(t))$ for $t\in[-\pi,3\pi]$. Mark points at $t=\{0,\frac{\pi}{2},\pi,\frac{3\pi}{2},2\pi\}$ and again at $t+2\pi$. Verify visually and numerically that the positions repeat with period $2\pi$. Repeat with a phase-shifted parametrization $x_\phi(t)=x_0+R\cos(t+\phi),\ y_\phi(t)=y_0+R\sin(t+\phi)$ and confirm it is merely a re-labeling of the same curve.

#### Exercise 3: Orientation via signed area.

> [!question]
> Using $t\in[0,2\pi]$, compute the line integral $\frac12\int_0^{2\pi}\bigl(x\,y'-y\,x'\bigr)\,dt$ numerically (e.g., trapezoidal rule) and show it equals $+\pi R^2$ to numerical tolerance. Reverse the parameter direction by plotting $t\mapsto(x(-t),y(-t))$ and verify that the integral changes sign, confirming counterclockwise orientation for increasing $t$.

#### Exercise 4: Tangent orthogonality to the radius.

> [!question]
> At $t_0=\frac{\pi}{3}$, compute the point $P$, the radius vector $r=(x(t_0)-x_0,\ y(t_0)-y_0)$, and the velocity $v=(x'(t_0),y'(t_0))=(-R\sin t_0, R\cos t_0)$. Plot the circle and draw both $r$ and $v$ as arrows anchored at $P$. Numerically evaluate $r\cdot v$ and report the value (it should be zero within floating-point error).

#### Exercise 5: Tangent line from the parametrization.

> [!question]
> Form the tangent line at $t_0$ in point–direction form $L(\lambda)=P+\lambda v$. Convert it to scalar form and simplify it to $(x-x_0)\cos t_0+(y-y_0)\sin t_0=R$. Plot this line together with the circle and visually verify first-order contact at $P$ (zoom in to see quadratic departure).

#### Exercise 6: Constant speed and arc length linearity.

> [!question]
> Compute $v(t)=\sqrt{x'(t)^2+y'(t)^2}$ over $t\in[0,2\pi]$ and plot $v(t)$. It should be flat at $R$. Then approximate arc length $s(t)=\int_0^t v(\tau)\,d\tau$ numerically and overlay it with the straight line $R\,t$. Report the maximum absolute difference.

#### Exercise 7: Unit-speed reparametrization.

> [!question]
> Define $s=Rt$ and plot $x(s)=x_0+R\cos(s/R),\ y(s)=y_0+R\sin(s/R)$ for $s\in[0,2\pi R]$. Numerically differentiate with respect to $s$ to obtain $(dx/ds,dy/ds)$ and verify that its norm is identically $1$. On the same figure, show equally spaced $s$ samples along the curve to illustrate uniform spacing by arc length.

#### Exercise 8: Curvature $1/R$ from derivatives.

> [!question]
> Evaluate $\kappa(t)=\dfrac{|x'y''-y'x''|}{(x'^2+y'^2)^{3/2}}$ on a dense grid in $t$. Plot $\kappa(t)$ and confirm it is flat at $1/R$. As an independent check, estimate curvature from discrete samples using a three-point formula and compare the two curves.

#### Exercise 9: Chords, central angles, and arc length.

> [!question]
> For $t_1=0$ and $t_2=\theta$ with $\theta$ ranging from $0$ to $\pi$, compute the chord length $\| (x(t_2),y(t_2))-(x(t_1),y(t_1))\|$ and the arc length $R\,|t_2-t_1|$. Plot both as functions of $\theta$ and verify the identity $\text{chord}=2R\sin(\theta/2)$ and the linear arc-length relation.

#### Exercise 10: Mapping points to parameters with $\operatorname{}atan2$.

> [!question]
> Sample 40 points on the circle at random angles $t\sim \mathcal{U}[0,2\pi)$. For each point, recover $\hat t=\operatorname{atan2}(y-y_0, x-x_0)$. Plot the original angle $t$ against $\hat t$ (unwrapped to avoid $2\pi$ discontinuities) and report the maximum absolute error.

#### Exercise 11: Uniform in angle vs. uniform in arc length (visual artifact).

> [!question]
> Place $N=24$ markers at uniform $t_k=2\pi k/N$ and on a second copy of the same circle place markers at uniform arc-length spacing (which is the same set because $s\propto t$). Now repeat on an ellipse $(x,y)=(x_0+a\cos t,\ y_0+b\sin t)$ for $a\neq b$, and show that uniform $t$ is no longer uniform in arc length. Plot both to highlight why circles are special.

#### Exercise 12: Rigid motions preserve the parametrization structure.

> [!question]
> Choose a rotation matrix $Q$ and translation $T$. Plot $X(t)=Q\,[C+R(\cos t,\sin t)] + T$ and show it coincides with a circle of radius $R$ centered at $QC+T$. Numerically check that $\|X(t)- (QC+T)\|=R$ on a grid of $t$.

#### Exercise 13: Tangent–normal decomposition of a vector field.

> [!question]
> Define a vector field along the circle, $w(t)=\alpha(t)\,\hat t(t)+\beta(t)\,\hat n(t)$, where $\hat t=(x',y')/\| (x',y')\|$ and $\hat n$ is the outward unit normal $((x-x_0),(y-y_0))/R$. Choose smooth scalars $\alpha,\beta$ (e.g., $\alpha=1+0.5\cos t,\ \beta=0.5\sin t$). Plot several $w(t)$ arrows and visually confirm that the tangential part moves along the circle while the normal part points radially.

#### Exercise 14: Numerical robustness near cardinal angles.

> [!question]
> Zoom into neighborhoods of $t\in\{0,\frac{\pi}{2},\pi,\frac{3\pi}{2}\}$. Plot the tangent line computed two ways—via the parametric direction vector and via the implicit gradient of $F(x,y)=(x-x_0)^2+(y-y_0)^2-R^2$. Report condition numbers or observed numerical instability (if any) and discuss how using the parametric form avoids division by a small slope.



### 4. Equation of the Circle in Polar Coordinates




#### Exercise 1: Law of cosines → polar equation, then overlay

> [!question]
> Pick parameters $(\rho_0,\varphi_0,R)=(2,\,\pi/6,\,3)$. Derive
> 
> $$\rho^2-2\rho\rho_0\cos(\varphi-\varphi_0)+\rho_0^2=R^2$$
> 
> from the law of cosines. Plot the locus two ways on the same axes: (i) as a polar curve by solving for $\rho(\varphi)$ and sampling $\varphi$; (ii) as the Cartesian circle with center $(x_0,y_0)=(\rho_0\cos\varphi_0,\rho_0\sin\varphi_0)$. Verify numerical coincidence.

#### Exercise 2: Recover the polar equation from Cartesian substitution

> [!question]
> Start from $(x-x_0)^2+(y-y_0)^2=R^2$ and substitute $x=\rho\cos\varphi,\ y=\rho\sin\varphi$, $x_0=\rho_0\cos\varphi_0,\ y_0=\rho_0\sin\varphi_0$. Simplify using $\cos\varphi\cos\varphi_0+\sin\varphi\sin\varphi_0=\cos(\varphi-\varphi_0)$. Plot the resulting polar curve and overlay the Cartesian circle to confirm equivalence.

####  Exercise 3: Rotational transparency

> [!question]
> Fix $(\rho_0,\varphi_0,R)=(2,\,\pi/4,\,1.5)$. Plot $\rho(\varphi)$ and then plot the curve after adding a common angle $\alpha=\pi/5$ to both $\varphi$ and $\varphi_0$. In Cartesian coordinates, confirm that both plots are identical sets (same circle, merely rotated parametrization).

####  Exercise 4: Specialization to center on the polar axis

> [!question]
> Set $\varphi_0=0$ and choose $(\rho_0,R)=(3,2)$. Plot the curve given by $\rho^2-2\rho\rho_0\cos\varphi+\rho_0^2=R^2$. On the same figure, plot the Cartesian circle with center $(\rho_0,0)$ and radius $R$. Mark the nearest and farthest points from the pole and verify $\rho_{\min}=|\rho_0-R|$, $\rho_{\max}=\rho_0+R$.

####  Exercise 5: Touching the pole and the canonical form $\rho=2R\cos\varphi$

> [!question]
> Impose the “through the pole” condition $\rho=0$ to get $\rho_0=R$. With $R=2$, plot $\rho=2R\cos\varphi$ and the corresponding Cartesian circle centered at $(R,0)$. Zoom near the pole and draw the tangent line there; verify it is perpendicular to the polar axis.

####  Exercise 6: Signed radius vs. $\rho\ge 0$ convention

> [!question]
> For $\rho=2R\cos\varphi$ with $R=2$, make two plots: (i) allow signed $\rho$ and $\varphi\in[-\pi,\pi]$; (ii) restrict to $\rho\ge 0$. On (ii), show the curve covers only $|\varphi|\le \pi/2$. Then map the “missing” half via $(\rho,\varphi)\mapsto(-\rho,\varphi+\pi)$ and demonstrate that the union matches (i).

####  Exercise 7: Two branches of $\rho(\varphi)$ and visibility

> [!question]
> Solve the quadratic in $\rho$:
> 
> $$\rho(\varphi)=\rho_0\cos\Delta \pm \sqrt{R^2-\rho_0^2\sin^2\Delta},\quad \Delta=\varphi-\varphi_0.$$
> 
> For $(\rho_0,\varphi_0,R)=(3,\pi/6,2)$, plot both “$+$” and “$-$” branches in Cartesian coordinates, coloring them differently. Identify the angular interval where the square root is real and interpret the two branches as front/back intersections of the ray at angle $\varphi$ with the circle.

####  Exercise 8: Visibility mask as a function of $\Delta$

> [!question]
> With $(\rho_0,R)=(3,2)$, plot the indicator of reality $\chi(\Delta)=\mathbf{1}\{R^2-\rho_0^2\sin^2\Delta\ge 0\}$ over $\Delta\in[-\pi,\pi]$. Mark the endpoints where $|\sin\Delta|=R/\rho_0$. Overlay the corresponding rays in the plane and verify that outside this angular sector, rays from the pole miss the circle.

####  Exercise 9: Numerical stability—direct $\cos(\Delta)$ vs expanded products

> [!question]
> Pick $\varphi_0=1.200$ rad and $\varphi=\varphi_0+\epsilon$ with $\epsilon$ as small as $10^{-8}$. Compute $\cos(\varphi-\varphi_0)$ two ways: directly, and via $\cos\varphi\cos\varphi_0+\sin\varphi\sin\varphi_0$. Compare relative errors and then propagate them into $\rho(\varphi)$. Plot error vs $\epsilon$ on log–log axes and comment on cancellation.

####  Exercise 10: Back-out the Cartesian parameters from polar data

> [!question]
> Choose five random triples $(\rho_0,\varphi_0,R)$. For each, compute $(x_0,y_0)$, plot the Cartesian circle, and overlay the polar curve generated from the general equation. Label each with its $(x_0,y_0)$ and $R$. Confirm that the reconstruction works uniformly across orientations.

####  Exercise 11: Edge cases—center at the pole, and large radius

> [!question]
> (a) Set $\rho_0=0$ and show the polar equation reduces to $\rho=R$. Plot this circle and verify constant $\rho$.  
> (b) Fix $\rho_0=1$ and let $R\to\infty$. On a fixed window, plot the portion of the circle and show it approaches a straight line orthogonal to the ray at angle $\varphi_0$. Quantify the deviation by plotting the curvature estimate along the visible arc.

####  Exercise 12: Intersections of rays with the circle

> [!question]
> Fix $(\rho_0,\varphi_0,R)=(2.5,\pi/3,1.5)$. For a grid of $\varphi$, solve the quadratic for $\rho$ and keep the real, nonnegative solutions. Plot the rays $\rho$ vs $\varphi$ in polar axes, placing markers at intersections. In Cartesian space, overlay the same intersections on the circle and connect each to the pole with a straight segment to visualize “front/back” hits.

####  Exercise 13: Extremal $\rho$ and geometric meaning

> [!question]
> For $\varphi_0=0$, differentiate $\rho(\varphi)$ with respect to $\varphi$ and find critical points. Show they occur at $\varphi=0,\pi$ with values $\rho_{\max}=\rho_0+R$ and $\rho_{\min}=|\rho_0-R|$. Plot $\rho(\varphi)$ and mark these extrema; interpret them as the farthest and nearest points of the circle from the pole.

####  Exercise 14: Tangent at the pole via polar differentiation

> [!question]
> In the touching case $R=\rho_0$ with $\varphi_0=0$, start from $\rho=2R\cos\varphi$. Convert to Cartesian and differentiate to obtain the slope at the pole. Plot the circle and the tangent line, and numerically confirm perpendicularity to the polar axis by measuring the angle between the axis direction and the tangent.

####  Exercise 15: Polar sampling vs Cartesian uniformity

> [!question]
> Sample $\varphi_k=\varphi_0+k\,\Delta$ uniformly and compute the corresponding points on the circle from the polar equation. In Cartesian coordinates, visualize the chord lengths between successive samples and compare them to the constant arc length $R\Delta$. Confirm uniform angular sampling yields uniform arc spacing only when the center is at the pole ($\rho_0=0$).



### 5. Tangent (and Normal) to a Circle




#### Exercise 1 — Gradient is normal (numeric check).

> [!question]
> Take $C=(2,-1)$, $R=3$, $F(x,y)=(x-2)^2+(y+1)^2-9$. Sample ten angles $t_k=2\pi k/10$. For each $P_k=(x_k,y_k)=(2+3\cos t_k,\,-1+3\sin t_k)$, compute $\nabla F(P_k)=(2(x_k-2),\,2(y_k+1))$ and the unit tangent from the parametrization $T_k=(-\sin t_k,\,\cos t_k)$. Plot the circle, draw $\nabla F(P_k)$ and $T_k$ as arrows at $P_k$, and report the dot products $\nabla F(P_k)\cdot T_k$ (they should be ≈0).

#### Exercise 2 — Tangent via the normal-line formula (expanded algebra).

> [!question]
> With the same circle and a specific point $P=(x_1,y_1)=(5,-1)$ (i.e., $t=0$), derive the tangent using  
> $\nabla F(P)\cdot\big((x,y)-P\big)=0$  
> to obtain $(x_1-2)(x-x_1)+(y_1+1)(y-y_1)=0$. Simplify to the center–point form $(x-2)(x_1-2)+(y+1)(y_1+1)=9$. Plot the circle and this line; zoom in to see second-order contact.

#### Exercise 3 — Origin special case and slope.

> [!question]
> Switch to $C=(0,0)$, $R=3$. For $P=(x_1,y_1)=(3/2,\,3\sqrt{3}/2)$, compute the tangent $x\,x_1+y\,y_1=R^2$ and extract its slope. Verify numerically that it equals $-x_1/y_1$. On the plot, show the radius $OP$, the tangent line, and annotate both slopes.

#### Exercise 4 — Implicit differentiation check.

> [!question]
> For general $C=(x_0,y_0)$, differentiate $F(x,y)=0$ to obtain  
> $2(x-x_0)+2(y-y_0)\,y'(x)=0$.  
> Evaluate at $P=(x_1,y_1)$ on the circle and compute $y'(x_1)=-(x_1-x_0)/(y_1-y_0)$. Compare this value to the slope read off from your plotted tangent in Exercise 2 at a non-cardinal point.

#### Exercise 5 — Tangent from the translated implicit form.

> [!question]
> Take the implicit circle $x^2+y^2+2mx+2ny+q=0$ with $(m,n,q)=(-2,1,\,2^2+(-1)^2-3^2)=( -2, 1, -4)$. At $P=(5,-1)$, compute the tangent  
> $x x_1+y y_1+m(x+x_1)+n(y+y_1)+q=0$.  
> Plot this line and the circle; confirm it matches the line from Exercise 2.

#### Exercise 6 — Perpendicularity of tangent and radius (vector test).

> [!question]
> Pick three angles $t=\pi/6,\;2\pi/5,\;7\pi/6$. For each $t$, form the radius vector $r=(x(t)-x_0,\;y(t)-y_0)$ and a direction vector of the tangent $v=(-R\sin t,\;R\cos t)$. Compute and tabulate $r\cdot v$. Overlay $r$ and $v$ as arrows at the same point on your plot.

#### Exercise 7 — Tangency as double intersection (discriminant).

> [!question]
> For the circle in Exercise 1 and a line $y=px+r$, substitute into $(x-2)^2+(y+1)^2=9$ to get a quadratic in $x$. Derive the discriminant $\Delta(p,r)$. Choose $(p,r)$ so that $\Delta>0$ (secant), $\Delta=0$ (tangent), and $\Delta<0$ (no intersection), plot the three lines, and mark intersection(s). For the tangent case, verify the quadratic has a repeated root.

#### Exercise 8 — Distance-from-center characterization.

> [!question]
> For a generic line $ax+by+c=0$, compute the perpendicular distance $d=\frac{|a x_0+b y_0+c|}{\sqrt{a^2+b^2}}$. Show numerically on several examples that the line is tangent iff $d=R$. Plot a small family of lines with varying $c$ crossing from secant to external and highlight the tangent where $d=R$.

#### Exercise 9 — Normal line through $C$.

> [!question]
> At $t=\pi/3$ on the circle of Exercise 1, compute the normal line (line through $C$ and $P$). Plot the normal and tangent together, compute their slopes, and verify they are negative reciprocals (handle vertical/horizontal cases correctly). Draw a small right angle marker at the intersection to emphasize orthogonality.

#### Exercise 10 — Agreement with the parametric tangent line.

> [!question]
> Using $x(t)=x_0+R\cos t,\;y(t)=y_0+R\sin t$, form the tangent at $t_0$ in point–direction form $L(\lambda)=P+\lambda(-R\sin t_0,\,R\cos t_0)$. Convert to the scalar equation $(x-x_0)\cos t_0+(y-y_0)\sin t_0=R$. For three different $t_0$, plot these lines and confirm they coincide with the gradient-based tangents.

#### Exercise 11 — Envelope of tangents (visualization).

> [!question]
> Sweep $t$ over $[0,2\pi]$ and plot a sparse bundle of tangent lines at angles $t_k$. Show that their common envelope is exactly the circle. To avoid overplot clutter, draw short tangent segments centered at the contact point and fade them outward.

#### Exercise 12 — Tangent at cardinal points (numerical stability).

> [!question]
> Evaluate tangents at $P=(x_0\pm R,y_0)$ and $P=(x_0, y_0\pm R)$. Confirm they are vertical or horizontal as appropriate. In code, compute slopes both from implicit differentiation and as $-x_1/y_1$ in the origin-centered case; comment on numerical stability when denominators are near zero and show how to branch to a vertical/horizontal representation.

#### Exercise 13 — Fitting a tangent from two near points (finite differences).

> [!question]
> Numerically approximate the tangent at $t_0$ by secants through $P_\pm=(x(t_0\pm h),y(t_0\pm h))$ with small $h$. Plot the secant for decreasing $h$ and show convergence to the analytic tangent line. Track the angle error vs $h$ on a log–log plot.

#### Exercise 14 — Reflection law with respect to the normal (applied check).

> [!question]
> Let a unit incoming direction $u$ strike the circle at $P$. Compute the outward unit normal $n=\frac{(x_1-x_0,\;y_1-y_0)}{R}$ and the reflected direction $u_{\text{out}}=u-2(u\cdot n)\,n$. Plot a short incoming ray segment, the normal, and the outgoing segment at $P$. Numerically verify equality of incidence and reflection angles relative to $n$.

#### Exercise 15 — Tangent in translated implicit coordinates (random trials).

> [!question]
> Generate random $(m,n,q)$ corresponding to real circles (ensure $m^2+n^2-q>0$). For random points $P$ on each circle, compute the tangent using  
> $x x_1+y y_1+m(x+x_1)+n(y+y_1)+q=0$  
> and overlay on the plot. Also recover $(x_0,y_0),R$ by completing the square and verify that the center–point tangent $(x-x_0)(x_1-x_0)+(y-y_0)(y_1-y_0)=R^2$ matches exactly.



