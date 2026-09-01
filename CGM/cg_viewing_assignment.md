# 3D Viewing Transformation

**Given:**
*   $P_0$ (VRP) = $(6, 8, 7)$
*   $P_{ref}$ (Look-at) = $(2, 3, 1)$
*   $V$ (View-up) = $(0, 1, 0)$

---

### (a) Unit Vectors $n, u, v$

**1. Normal Vector ($n$):**
$$N = P_0 - P_{ref} = (6-2,\ 8-3,\ 7-1) = (4,\ 5,\ 6)$$
$$|N| = \sqrt{4^2 + 5^2 + 6^2} = \sqrt{77} \approx 8.775$$
$$n = \frac{N}{|N|} = \left(\frac{4}{8.775},\ \frac{5}{8.775},\ \frac{6}{8.775}\right) = \mathbf{(0.456,\ 0.570,\ 0.684)}$$

**2. Right Vector ($u$):**
$$U = V \times N = \begin{vmatrix} i & j & k \\ 0 & 1 & 0 \\ 4 & 5 & 6 \end{vmatrix} = (6,\ 0,\ -4)$$
$$|U| = \sqrt{6^2 + 0^2 + (-4)^2} = \sqrt{52} \approx 7.211$$
$$u = \frac{U}{|U|} = \left(\frac{6}{7.211},\ \frac{0}{7.211},\ \frac{-4}{7.211}\right) = \mathbf{(0.832,\ 0.000,\ -0.555)}$$

**3. True Up Vector ($v$):**
$$V_{actual} = N \times U = \begin{vmatrix} i & j & k \\ 4 & 5 & 6 \\ 6 & 0 & -4 \end{vmatrix} = (-20,\ 52,\ -30)$$
$$|V_{actual}| = \sqrt{(-20)^2 + 52^2 + (-30)^2} = \sqrt{4004} \approx 63.277$$
$$v = \frac{V_{actual}}{|V_{actual}|} = \left(\frac{-20}{63.277},\ \frac{52}{63.277},\ \frac{-30}{63.277}\right) = \mathbf{(-0.316,\ 0.822,\ -0.474)}$$

---

### (b) Transformation Matrix $M = R \cdot T$

According to the viewing transformation formula:
$$M = \begin{pmatrix} u_x & u_y & u_z & 0 \\ v_x & v_y & v_z & 0 \\ n_x & n_y & n_z & 0 \\ 0 & 0 & 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & 0 & 0 & -x_0 \\ 0 & 1 & 0 & -y_0 \\ 0 & 0 & 1 & -z_0 \\ 0 & 0 & 0 & 1 \end{pmatrix} = \begin{pmatrix} u_x & u_y & u_z & dx \\ v_x & v_y & v_z & dy \\ n_x & n_y & n_z & dz \\ 0 & 0 & 0 & 1 \end{pmatrix}$$

First, calculate $dx, dy, dz$:
*   $dx = -P_0 \cdot u = -(6 \times 0.832 + 8 \times 0.000 + 7 \times -0.555) = -(4.992 + 0 - 3.885) = \mathbf{-1.107}$
*   $dy = -P_0 \cdot v = -(6 \times -0.316 + 8 \times 0.822 + 7 \times -0.474) = -(-1.896 + 6.576 - 3.318) = \mathbf{-1.362}$
*   $dz = -P_0 \cdot n = -(6 \times 0.456 + 8 \times 0.570 + 7 \times 0.684) = -(2.736 + 4.560 + 4.788) = \mathbf{-12.084}$

Now put the values directly into the final matrix:
$$M = \mathbf{\begin{pmatrix} 0.832 & 0.000 & -0.555 & -1.107 \\ -0.316 & 0.822 & -0.474 & -1.362 \\ 0.456 & 0.570 & 0.684 & -12.084 \\ 0 & 0 & 0 & 1 \end{pmatrix}}$$

---

### (c) Transform Point $Q = (2, 3, 1)$

$$Q_{view} = M \cdot Q = \begin{pmatrix} 0.832 & 0.000 & -0.555 & -1.109 \\ -0.316 & 0.822 & -0.474 & -1.359 \\ 0.456 & 0.570 & 0.684 & -12.080 \\ 0 & 0 & 0 & 1 \end{pmatrix} \begin{pmatrix} 2 \\ 3 \\ 1 \\ 1 \end{pmatrix} = \mathbf{\begin{pmatrix} 0.000 \\ 0.000 \\ -8.775 \\ 1 \end{pmatrix}}$$

**Interpretation:**
The coordinates $(0, 0, -8.775)$ mean the point is in the exact center of the camera's view. The $n$-axis value $-8.775$ is exactly the negative distance from the camera to the look-at point.

---

### (d) Justifications

**1. If $V = (0, 5, 0)$:** 
The frame would **not** change. $(0,5,0)$ points in the same direction as $(0,1,0)$. Normalization will divide out the magnitude of 5, keeping the $u$ and $v$ unit vectors identical to before.

**2. If $V$ is parallel to view direction ($n$):** 
The cross product ($V \times n$) would result in a zero vector $(0,0,0)$. We cannot normalize a zero vector, meaning the camera loses its left/right orientation, and the coordinate system fails completely.
---
---

## Example 2: View Coordinate System (VCS) Calculation

**Question 1:** Define the View Coordinate System (VCS) and state the roles of the three input parameters, Eye position, Look-at point, and Up vector, in setting up a camera.
**Answer:**
*   **View Coordinate System (VCS):** This is the camera's local coordinate system (defined by $u, v, n$ axes). It represents how the camera views the 3D world.
*   **Roles of parameters:**
    1.  **Eye position ($P_0$):** Defines the exact location where the camera is placed in the world.
    2.  **Look-at point ($P_{ref}$):** Defines the target point the camera is looking at or focusing on.
    3.  **Up vector ($V$):** Defines the "upward" direction for the camera, establishing its orientation (so the picture doesn't come out upside down).

**Question 2:** Find the VCS coordinates of the point $A(1, 0.5, 1)$ for the following camera setup: Eye: $(2, 2, 3)$ | Look-at: $(2, 1, 1)$ | Up: $(0, 1, 0)$. Show the computation of the axis vectors $n, u, v$, the translation of $A$, and the final view coordinates.

**Step 1: Normal Vector ($n$)**
$$
N = Eye - Look\_at = (2-2,\ 2-1,\ 3-1) = (0, 1, 2)
$$
$$
|N| = \sqrt{0^2 + 1^2 + 2^2} = \sqrt{5}
$$
$$
n = \frac{N}{|N|} = \left(0,\ \frac{1}{\sqrt{5}},\ \frac{2}{\sqrt{5}}\right)
$$

**Step 2: Right Vector ($u$)**
$$
U = V \times N = \begin{vmatrix} i & j & k \\ 0 & 1 & 0 \\ 0 & 1 & 2 \end{vmatrix} = (2, 0, 0)
$$
$$
|U| = \sqrt{2^2} = 2
$$
$$
u = \frac{U}{|U|} = \left(\frac{2}{2},\ 0,\ 0\right) = \mathbf{(1, 0, 0)}
$$

**Step 3: True Up Vector ($v$)**
$$
V_{actual} = N \times U = (0, 1, 2) \times (2, 0, 0) = (0, 4, -2)
$$
$$
|V_{actual}| = \sqrt{0^2 + 4^2 + (-2)^2} = \sqrt{20} = 2\sqrt{5}
$$
$$
v = \frac{V_{actual}}{|V_{actual}|} = \left(0,\ \frac{4}{2\sqrt{5}},\ \frac{-2}{2\sqrt{5}}\right) = \mathbf{\left(0,\ \frac{2}{\sqrt{5}},\ \frac{-1}{\sqrt{5}}\right)}
$$

**Step 4: Translation of A relative to the eye**
$$
A_{translated} = A - Eye = (1 - 2,\ 0.5 - 2,\ 1 - 3) = \mathbf{(-1,\ -1.5,\ -2)}
$$

**Step 5: Final View Coordinates**
$$
A_{view} = \begin{pmatrix} u_x & u_y & u_z \\ v_x & v_y & v_z \\ n_x & n_y & n_z \end{pmatrix} \times \begin{pmatrix} A_{tx} \\ A_{ty} \\ A_{tz} \end{pmatrix}
$$
$$
A_{view} = \begin{pmatrix} 1 & 0 & 0 \\ 0 & 2/\sqrt{5} & -1/\sqrt{5} \\ 0 & 1/\sqrt{5} & 2/\sqrt{5} \end{pmatrix} \begin{pmatrix} -1 \\ -1.5 \\ -2 \end{pmatrix}
$$
*   $x_{view} = 1(-1) + 0 + 0 = -1$
*   $y_{view} = 0 + \frac{2}{\sqrt{5}}(-1.5) + \frac{-1}{\sqrt{5}}(-2) = \frac{-3}{\sqrt{5}} + \frac{2}{\sqrt{5}} = \frac{-1}{\sqrt{5}}$
*   $z_{view} = 0 + \frac{1}{\sqrt{5}}(-1.5) + \frac{2}{\sqrt{5}}(-2) = \frac{-1.5}{\sqrt{5}} - \frac{4}{\sqrt{5}} = \frac{-5.5}{\sqrt{5}}$

**Final Answer:**
VCS coordinates of point $A$ is **$\left(-1,\ \frac{-1}{\sqrt{5}},\ \frac{-5.5}{\sqrt{5}}\right)$** or approximately **$(-1,\ -0.447,\ -2.460)$**.