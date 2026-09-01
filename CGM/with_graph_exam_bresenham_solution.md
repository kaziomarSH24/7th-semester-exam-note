# Exam Solution Format: Bresenham's Line Algorithm

**Question:** Scan-convert a line from point $A(8, 5)$ to point $B(12, 8)$ using Bresenham's Line Drawing Algorithm.

---

### Step 1: Initial Calculations

Given points: $(x_1, y_1) = (8, 5)$ and $(x_2, y_2) = (12, 8)$

1.  **Calculate $dx$ and $dy$:**
    *   $dx = x_2 - x_1 = 12 - 8 = 4$
    *   $dy = y_2 - y_1 = 8 - 5 = 3$

2.  **Calculate slope ($m$) and verify condition:**
    *   $m = \frac{dy}{dx} = \frac{3}{4} = 0.75$
    *   Since $0 < m < 1$, we sample at unit $x$ intervals.

3.  **Calculate the three constant parameters:**
    *   **Initial Decision Parameter ($d$):** 
        $d = 2dy - dx = 2(3) - 4 = 6 - 4 = \mathbf{2}$
    *   **Increment for $d < 0$ ($dS$):** 
        $dS = 2dy = 2(3) = \mathbf{6}$
    *   **Increment for $d \ge 0$ ($dT$):** 
        $dT = 2dy - 2dx = 2(3) - 2(4) = 6 - 8 = \mathbf{-2}$

*(Note: In exam, $d$ is sometimes written as $p_k$, and $dT, dS$ as just formula additions. Writing them beforehand saves time and prevents calculation errors).*

---

### Step 2: Calculation Table

Start with the initial point $(8, 5)$ and initial $d = 2$.
*   If $d \ge 0$: $x_{k+1} = x_k + 1$, $y_{k+1} = y_k + 1$, and $d_{new} = d_{old} + dT$
*   If $d < 0$: $x_{k+1} = x_k + 1$, $y_{k+1} = y_k$ (no change), and $d_{new} = d_{old} + dS$

| $k$ | Decision Parameter ($d$) | $x_{k+1}$ | $y_{k+1}$ | Plotted Pixel |
| :---: | :---: | :---: | :---: | :---: |
| 0 | 2 | 8 | 5 | **(8, 5)** |
| 1 | $2 + (-2) = \mathbf{0}$ | 9 | 6 | **(9, 6)** |
| 2 | $0 + (-2) = \mathbf{-2}$ | 10 | 7 | **(10, 7)** |
| 3 | $-2 + 6 = \mathbf{4}$ | 11 | 7 | **(11, 7)** |
| 4 | $4 + (-2) = \mathbf{2}$ | 12 | 8 | **(12, 8)** |

---

### Step 3: Graphical Representation

Plot the calculated pixels on a 2D grid.

```text
  Y
  |
9 |  .   .   .   .   .   .   . 
  |
8 |  .   .   .   .   .   ●   .  (12,8)
  |                 
7 |  .   .   .   ●   ●   .   .  (10,7), (11,7)
  |             
6 |  .   .   ●   .   .   .   .  (9,6)
  |         
5 |  .   ●   .   .   .   .   .  (8,5)
  |     
4 |  .   .   .   .   .   .   . 
  |
0 +----------------------------- X
     7   8   9  10  11  12  13 
```
