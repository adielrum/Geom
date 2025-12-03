### 1. Numerical Differentiation (Hampiran Turunan)
These formulas approximate derivatives using discrete data points with a step size of $h$.

**Basic Definition via Taylor Series**
* **First Derivative Approximation:** $f^{\prime}(a)\approx\frac{f(a+h)-f(a)}{h}$ with error $O(h)$.

**Finite Difference Formulas (Beda Hingga)**
* **Forward Difference (Beda Maju) - First Derivative:**
    * $O(h)$: $f_{0}^{\prime}\approx\frac{f_{1}-f_{0}}{h}$.
    * $O(h^2)$: $f_{0}^{\prime}=\frac{-3f_{0}+4f_{1}-f_{2}}{2h}$.
* **Forward Difference - Second Derivative:**
    * $f_{0}^{\prime\prime}=\frac{2f_{0}-5f_{1}+4f_{2}-f_{3}}{h^{2}}$.
* **Backward Difference (Beda Mundur) - First Derivative:**
    * $O(h)$: Not explicitly listed as a standalone formula but implied as the reverse of forward.
    * $O(h^2)$: $f_{0}^{\prime}=\frac{f_{-2}-4f_{-1}+3f_{0}}{2h}$.
* **Backward Difference - Second Derivative:**
    * $f_{0}^{\prime\prime}=\frac{-f_{-3}+4f_{-2}-5f_{-1}+2f_{0}}{h^{2}}$.
* **Central Difference (Beda Pusat) - First Derivative:**
    * $O(h^2)$: $f_{0}^{\prime}=\frac{f_{1}-f_{-1}}{2h}$.
    * $O(h^4)$: $f_{0}^{\prime}=\frac{-f_{2}+8f_{1}-8f_{-1}+f_{-2}}{12h}$.
* **Central Difference - Second Derivative:**
    * $O(h^2)$: $f_{0}^{\prime\prime}=\frac{f_{1}-2f_{0}+f_{-1}}{h^{2}}$.
    * $O(h^4)$: $f_{0}^{\prime\prime}=\frac{-f_{2}+16f_{1}-30f_{0}+16f_{-1}-f_{-2}}{12h^{2}}$.

---

### 2. Numerical Integration (Pengintegralan Numerik)
Approximating $\int_{a}^{b}f(x)dx$ using Newton-Cotes and other methods.

**Newton-Cotes Formulas**
* **Trapezoid Rule:** $\int_{a}^{b}f(x)dx\approx\frac{h}{2}(f_{0}+f_{1})$.
    * **Composite Trapezoid:** $\int_{a}^{b}f(x)dx\approx\frac{h}{2}(f_{0}+2f_{1}+2f_{2}+\cdot\cdot\cdot+2f_{n-1}+f_{n})$.
    * **Error:** $E=-\frac{(b-a)^{3}}{12n^{2}}f^{\prime\prime}(c)$.
* **Simpson's 1/3 Rule:** $\int_{a}^{b}f(x)dx\approx\frac{h}{3}(f_{0}+4f_{1}+f_{2})$.
    * **Composite Simpson 1/3:** $\frac{h}{3}(f_{0}+4f_{1}+2f_{2}+4f_{3}+\cdot\cdot\cdot+2f_{n-2}+4f_{n-1}+f_{n})$.
    * **Error:** $E=-\frac{(b-a)^{5}}{180n^{4}}f^{(4)}(c)$.
* **Simpson's 3/8 Rule:** $\int_{a}^{b}f(x)dx\approx\frac{3h}{8}(f_{0}+3f_{1}+3f_{2}+f_{3})$.
* **Boole's Rule:** $\int_{a}^{b}f(x)dx\approx\frac{2h}{45}(7f_{0}+32f_{1}+12f_{2}+32f_{3}+7f_{4})$.

**Recursive and Romberg Integration**
* **Recursive Trapezoid:** $T_{k}:=\frac{T_{k-1}}{2}+h_{k}(f_{1}+f_{3}+f_{5}+\cdot\cdot\cdot+f_{2^{k}-1})$.
* **Recursive Simpson:** $S_{k}:=\frac{4T_{k}-T_{k-1}}{3}$.
* **Romberg Integration (General):** $R_{j,k}:=\frac{4^{k}R_{j,k-1}-R_{j-1,k-1}}{4^{k}-1}$.
    * Specific forms: Simpson $S_j$ is $O(h^4)$; Boole $B_j$ is $O(h^6)$ via $B_{j}:=\frac{4^{2}S_{j}-S_{j-1}}{15}$.

**Gauss-Legendre Integration**
* **Transformation to :** $\int_{a}^{b}f(t)dt\approx\frac{b-a}{2}\sum_{k=1}^{n}w_{n,k}f(\frac{a+b}{2}+\frac{b-a}{2}x_{n,k})$.
* **2-Point Formula:** $G_{2}(f)=f(-\sqrt{\frac{1}{3}})+f(\sqrt{\frac{1}{3}})$ (weights $w=1$).
* **3-Point Formula:** $G_{3}(f)=\frac{1}{9}(5f(-\sqrt{\frac{3}{5}})+8f(0))+5f(\sqrt{\frac{3}{5}}))$.

---

### 3. Ordinary Differential Equations (ODEs) - Initial Value Problems
Solving $y^{\prime}=f(t,y)$, $y(t_{0})=y_{0}$.

**One-Step Methods**
* **Euler's Method:** $y_{k+1}=y_{k}+hf(t_{k},y_{k})$ (Error $O(h)$).
* **Heun's Method (Predictor-Corrector):**
    * Predictor: $p_{k+1}\approx y_{k}+h~f(t_{k},y_{k})$.
    * Corrector: $y_{k+1}\approx y_{k}+\frac{h}{2}$.
* **Taylor Series Method:** $y(t_{k}+h)=y(t_{k})+y^{\prime}(t_{k})h+y^{\prime\prime}(t_{k})\frac{h^{2}}{2}+\cdot\cdot\cdot$ (Using higher derivatives of $f$).
* **Runge-Kutta Order 4 (RK4):**
    * $y_{1}=y_{0}+\frac{h}{6}(f_{1}+2f_{2}+2f_{3}+f_{4})$.
    * $f_{1}=f(t_{0},y_{0})$.
    * $f_{2}=f(t_{0}+\frac{1}{2}h,y_{0}+\frac{h}{2}f_{1})$.
    * $f_{3}=f(t_{0}+\frac{1}{2}h,y_{0}+\frac{h}{2}f_{2})$.
    * $f_{4}=f(t_{0}+h,y_{0}+hf_{3})$.

**Multi-Step Methods (Predictor-Corrector)**
* **Adams-Bashforth-Moulton:**
    * Predictor: $p_{k+1}=y_{k}+\frac{h}{24}(-9f_{k-3}+37f_{k-2}-59f_{k-1}+55f_{k})$.
    * Corrector: $y_{k+1}=y_{k}+\frac{h}{24}(f_{k-2}-5f_{k-1}+19f_{k}+9f_{k+1})$.
* **Milne-Simpson:**
    * Predictor: $p_{k+1}=y_{k-3}+\frac{4h}{3}(2f_{k-2}-f_{k-1}+2f_{k})$.
    * Corrector: $y_{k+1}=y_{k-1}+\frac{h}{3}(f_{k-1}+4f_{k}+f_{k+1})$.
* **Hamming:**
    * Predictor: Same as Milne-Simpson.
    * Corrector: $y_{k+1}=\frac{1}{8}(9y_{k}-y_{k-2})+\frac{3h}{8}(-f_{k-1}+2f_{k}+f_{k+1})$.

**Systems of ODEs**
* **Euler System:** $x_{k+1}\approx x_{k}+h f(t_{k},x_{k},y_{k})$ and $y_{k+1}\approx y_{k}+h g(t_{k},x_{k},y_{k})$.
* **RK4 System:** Extension of RK4 calculating $f_{1..4}$ and $g_{1..4}$ based on both $x$ and $y$.

---

### 4. ODEs - Boundary Value Problems (Masalah Nilai Batas)
Solving $x^{\prime\prime}=p(t)x^{\prime}(t)+q(t)x(t)+r(t)$ with $x(a)=\alpha, x(b)=\beta$.

* **Finite Difference Method:**
    * $(-\frac{h}{2}p_{j}-1)x_{j-1}+(2+h^{2}q_{j})x_{j}+(\frac{h}{2}p_{j}-1)x_{j+1}=-h^{2}r_{j}$.
* **Linear Shooting Method:**
    * Decompose into two IVPs:
        1.  $u^{\prime\prime}=p(t)u^{\prime}+q(t)u+r(t)$, $u(a)=\alpha, u'(a)=0$.
        2.  $v^{\prime\prime}=p(t)v^{\prime}+q(t)v$, $v(a)=0, v'(a)=1$.
    * Solution: $x(t)=u(t)+\frac{\beta-u(b)}{v(b)}v(t)$.

---

### 5. Partial Differential Equations (Persamaan Diferensial Parsial)
Solving the Heat Equation $u_{t}=cu_{xx}$.

* **Forward Time Central Space (FTCS) - Explicit:**
    * $u_{i}^{j+1}=ru_{i-1}^{j}+(1-2r)u_{i}^{j}+ru_{i+1}^{j}$ where $r=\frac{ck}{h^{2}}$.
    * Stability condition: $r<\frac{1}{2}$ or $\Delta t<\frac{\Delta x^{2}}{2c}$.
* **Backward Time Central Space (BTCS) - Implicit:**
    * $u_{i}^{j-1}=-ru_{i-1}^{j}+(1+2r)u_{i}^{j}-ru_{i+1}^{j}$ where $r=\frac{ck}{h^{2}}$.
* **Crank-Nicolson Method:**
    * $-ru_{i-1}^{j+1}+(1+2r)u_{i}^{j+1}-ru_{i+1}^{j+1}=ru_{i-1}^{j}+(1-2r)u_{i}^{j}+ru_{i+1}^{j}$.
    * Note: Here, $r=\frac{ck}{2h^{2}}$.