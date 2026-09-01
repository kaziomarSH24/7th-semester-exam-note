# Section B: Line Drawing Algorithms (Master Exam Note)

এই নোটে আপনার **Section B** এর জন্য DDA এবং Bresenham অ্যালগরিদম থেকে আসতে পারে এমন **৪টি ম্যাথ** একদম পরীক্ষার হুবহু ফরম্যাটে সাজিয়ে দেওয়া হলো। পরীক্ষার আগে শুধু এই একটি ফাইল রিভিশন দিলেই আপনার পুরো Section B কভার হয়ে যাবে!

---

## 🟢 Part 1: DDA Algorithm

### Example 1: DDA Case 1 ($0 < m \le 1$)
**Q:** Scan-convert a line from $A(2, 2)$ to $B(7, 5)$ using DDA.

1.  **Initial Calculations:**
    *   $dx = 7 - 2 = 5$
    *   $dy = 5 - 2 = 3$
    *   $m = \frac{dy}{dx} = \frac{3}{5} = 0.6$
    *   Since $0 < m \le 1$, we sample at unit $x$ intervals.
    *   Formulas: $x_{k+1} = x_k + 1$, $\ y_{k+1} = y_k + m = y_k + 0.6$
    *   Total steps = $dx = 5$

2.  **Calculation Table:**

| k | x | y | Plot Pixel (Round(x), Round(y)) |
| :---: | :---: | :---: | :---: |
| 0 | 2 | 2.0 | **(2, 2)** |
| 1 | 3 | 2.6 | **(3, 3)** |
| 2 | 4 | 3.2 | **(4, 3)** |
| 3 | 5 | 3.8 | **(5, 4)** |
| 4 | 6 | 4.4 | **(6, 4)** |
| 5 | 7 | 5.0 | **(7, 5)** |


### Example 2: DDA Case 2 ($m > 1$)
**Q:** Scan-convert a line from $A(3, 2)$ to $B(2, 7)$ using DDA.

1.  **Initial Calculations:**
    *   $dx = 2 - 3 = -1$
    *   $dy = 7 - 2 = 5$
    *   $m = \frac{dy}{dx} = \frac{5}{-1} = -5$
    *   Since $|m| > 1$, the line is steep. We exchange the $x$ and $y$ axes to sample at unit $y$ intervals.
    *   Formulas: $y_{k+1} = y_k + 1$, $\ x_{k+1} = x_k + \frac{1}{m} = x_k - 0.2$
    *   Total steps = $|dy| = 5$

2.  **Calculation Table:**

| k | y | x | Plot Pixel (Round(x), Round(y)) |
| :---: | :---: | :---: | :---: |
| 0 | 2 | 3.0 | **(3, 2)** |
| 1 | 3 | 2.8 | **(3, 3)** |
| 2 | 4 | 2.6 | **(3, 4)** |
| 3 | 5 | 2.4 | **(2, 5)** |
| 4 | 6 | 2.2 | **(2, 6)** |
| 5 | 7 | 2.0 | **(2, 7)** |

---
---

## 🔵 Part 2: Bresenham's Line Algorithm

### Example 3: Bresenham Case 1 ($0 < m \le 1$)
**Q:** Scan-convert a line from $A(8, 5)$ to $B(12, 8)$ using Bresenham's Algorithm.

1.  **Initial Parameters:**
    *   $dx = 12 - 8 = 4$
    *   $dy = 8 - 5 = 3$
    *   $m = \frac{dy}{dx} = \frac{3}{4} = 0.75$ 
    *   Since $0 < m < 1$, we sample at unit $x$ intervals.

2.  **Decision Constants:**
    *   **$d_{initial}$** $= 2dy - dx = 2(3) - 4 = \mathbf{2}$
    *   **$dS$** (if $d < 0$) $= 2dy = 2(3) = \mathbf{6}$
    *   **$dT$** (if $d \ge 0$) $= 2dy - 2dx = 2(3) - 2(4) = \mathbf{-2}$

3.  **Calculation Table:**
    *   If $d \ge 0$: $x_{k+1} = x_k + 1$, $y_{k+1} = y_k + 1$, and $d_{new} = d_{old} + dT$
    *   If $d < 0$: $x_{k+1} = x_k + 1$, $y_{k+1} = y_k$, and $d_{new} = d_{old} + dS$

| k | d | x | y | Plotted Pixel |
| :---: | :---: | :---: | :---: | :---: |
| 0 | 2 | 8 | 5 | **(8, 5)** |
| 1 | $2 + (-2) = \mathbf{0}$ | 9 | 6 | **(9, 6)** |
| 2 | $0 + (-2) = \mathbf{-2}$ | 10 | 7 | **(10, 7)** |
| 3 | $-2 + 6 = \mathbf{4}$ | 11 | 7 | **(11, 7)** |
| 4 | $4 + (-2) = \mathbf{2}$ | 12 | 8 | **(12, 8)** |


### Example 4: Bresenham Case 2 ($m > 1$)
**Q:** Scan-convert a line from $A(2, 1)$ to $B(5, 8)$ using Bresenham's Algorithm.

1.  **Initial Parameters:**
    *   $dx = 5 - 2 = 3$
    *   $dy = 8 - 1 = 7$
    *   $m = \frac{dy}{dx} = \frac{7}{3} = 2.33$ 
    *   Since $m > 1$, the line is steep. We exchange the $x$ and $y$ axes to sample at unit $y$ intervals.

2.  **Decision Constants (Swapped):** *(Replace $dx$ with $dy$ and vice-versa)*
    *   **$d_{initial}$** $= 2dx - dy = 2(3) - 7 = \mathbf{-1}$
    *   **$dS$** (if $d < 0$) $= 2dx = \mathbf{6}$
    *   **$dT$** (if $d \ge 0$) $= 2dx - 2dy = 2(3) - 2(7) = \mathbf{-8}$

3.  **Calculation Table:**
    *   If $d \ge 0$: $y_{k+1} = y_k + 1$, $x_{k+1} = x_k + 1$, and $d_{new} = d_{old} + dT$
    *   If $d < 0$: $y_{k+1} = y_k + 1$, $x_{k+1} = x_k$, and $d_{new} = d_{old} + dS$

| k | d | y | x | Pixel (x,y) |
| :---: | :---: | :---: | :---: | :---: |
| 0 | -1 | 1 | 2 | **(2,1)** |
| 1 | $-1 + 6 = 5$ | 2 | 2 | **(2,2)** |
| 2 | $5 + (-8) = -3$ | 3 | 3 | **(3,3)** |
| 3 | $-3 + 6 = 3$ | 4 | 3 | **(3,4)** |
| 4 | $3 + (-8) = -5$ | 5 | 4 | **(4,5)** |
| 5 | $-5 + 6 = 1$ | 6 | 4 | **(4,6)** |
| 6 | $1 + (-8) = -7$ | 7 | 5 | **(5,7)** |
| 7 | $-7 + 6 = -1$ | 8 | 5 | **(5,8)** |

---

### Theory for Section B (Short Recap)
**DDA vs Bresenham:**
1.  **Speed:** Bresenham is faster because it uses only integer addition/subtraction. DDA is slower due to floating-point addition and rounding.
2.  **Accuracy:** Bresenham is highly accurate. DDA suffers from rounding errors which can make the line drift slightly for very long lines.
3.  **Operations:** DDA uses division (for slope) and rounding. Bresenham uses simple bit-shifts and basic math.91724

9172491724

9172491724

91724