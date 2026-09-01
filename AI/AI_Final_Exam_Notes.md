# 🎓 AI Final Exam: Complete Notes & Cheat Sheet

*Generated for Kazi Omar*

---



<!-- ============================================== -->


# 📄 Topic: All Math Formulas Cheatsheet

# AI Exam: Ultimate Formula Cheat Sheet

Here are all the important mathematical formulas you need to solve the math problems in your exam, organized by topic.

---

### 1. K-Means Clustering (Distance Formulas)
Used to find the distance between a data point and a cluster center.

*   **Manhattan Distance (Shortcut):**
    $$Distance = |x_1 - x_2| + |y_1 - y_2| + \dots$$
*   **Euclidean Distance (Actual):**
    $$Distance = \sqrt{(x_1 - x_2)^2 + (y_1 - y_2)^2 + \dots}$$

---

### 2. Confusion Matrix Metrics
Used to evaluate classification models. *(Total $N = TP + TN + FP + FN$)*

*   **Accuracy:** $\frac{TP + TN}{N}$
*   **Precision:** $\frac{TP}{TP + FP}$
*   **Recall / Sensitivity:** $\frac{TP}{TP + FN}$
*   **Specificity:** $\frac{TN}{TN + FP}$
*   **Negative Predictive Value (NPV):** $\frac{TN}{TN + FN}$
*   **F1-Score:** $2 \times \frac{Precision \times Recall}{Precision + Recall}$

---

### 3. Activation Functions
Mathematical functions applied to a neuron's output.

*   **Sigmoid:** $S(x) = \frac{1}{1 + e^{-x}}$
*   **Tanh:** $tanh(x) = \frac{e^x - e^{-x}}{e^x + e^{-x}}$
*   **ReLU:** $f(x) = \max(0, x)$
*   **Softmax:** $f_i(x) = \frac{e^{x_i}}{\sum_{k} e^{x_k}}$

---

### 4. Single Perceptron
Used for basic neuron calculation and updating weights during training.

*   **Perceptron Output (Weighted Sum):**
    $$Sum = (w_1 x_1 + w_2 x_2 + \dots) + \text{bias}$$
*   **Perceptron Weight Update Rule:**
    $$w_{new} = w_{old} + \Delta w$$
    $$\Delta w = \eta \times (t - o) \times x$$
    *(where $\eta$ = Learning Rate, $t$ = Target, $o$ = Output, $x$ = Input)*

---

### 5. Multi-Layer Perceptron & Backpropagation
Used to calculate the errors backward through the network to update weights.

*   **Total Error (Squared Error Function):**
    $$E_{total} = \sum \frac{1}{2}(target - output)^2$$

*   **Error Term for Output Unit ($\delta_k$):**
    $$\delta_k = o_k(1 - o_k)(t_k - o_k)$$
    *(where $o_k$ = actual output, $t_k$ = target output)*

*   **Error Term for Hidden Unit ($\delta_h$):**
    $$\delta_h = o_h(1 - o_h) \sum (w_{h,k} \times \delta_k)$$
    *(where $o_h$ = hidden unit output, $w_{h,k}$ = weight between hidden and output layer)*

*   **Backpropagation Weight Update:**
    $$w_{new} = w_{old} + \Delta w$$
    $$\Delta w = \eta \times \delta_j \times x_{ji}$$
    *(where $\eta$ = Learning Rate, $\delta_j$ = Error term of the unit, $x_{ji}$ = Input from previous unit)*


---



<!-- ============================================== -->


# 📄 Topic: Activation Functions Note

# Short Note: Activation Functions in ANN

### 1. What is an Activation Function?
* It is a mathematical function applied to the output of an artificial neuron.
* It decides whether a neuron should be activated (fired) or not.
* It calculates the weighted sum of inputs and adds a bias to make the final decision.

### 2. Why do we need Activation Functions? (Importance)
* **Introduces Non-linearity:** Without an activation function, a neural network behaves just like a simple linear regression model.
* **Learns Complex Patterns:** It allows the network to learn and solve complex, real-world problems.
* Without it, adding multiple hidden layers is useless, because the output will still be a single linear line.

### 3. Types of Activation Functions

**A. Sigmoid Function:**
* **Formula:** $S(x) = \frac{1}{1 + e^{-x}}$
* It gives an **'S'-shaped** curve.
* The output value is always between **0 and 1**.
* Used mostly for probability and **Binary Classification** (e.g., YES/NO, True/False).

**B. Tanh Function (Hyperbolic Tangent):**
* **Formula:** $tanh(x) = \frac{e^x - e^{-x}}{e^x + e^{-x}}$
* Also gives an 'S'-shaped curve but is centered around zero.
* The output value is between **-1 and 1**.
* It handles negative inputs better by making them strongly negative.

**C. ReLU (Rectified Linear Unit):**
* **Formula:** $f(x) = max(0, x)$
* The **most popular** and widely used function today (mostly in Deep Learning and CNNs).
* **Rule:** 
  * If input is negative ($< 0$), output is **0**.
  * If input is positive ($\ge 0$), output is the **exact same** as the input.
* It solves the vanishing gradient problem and makes learning faster.

**D. Softmax Function:**
* **Formula:** $f_i(x) = \frac{e^{x_i}}{\sum_{k} e^{x_k}}$
* Used in the **final output layer** of a neural network.
* Best for **Multi-Class Classification** (e.g., choosing between Apple, Banana, and Orange).
* It converts raw scores into **probabilities**.
* The sum of all output probabilities is always equal to **1**.


---



<!-- ============================================== -->


# 📄 Topic: Confusion Matrix Note

# Short Note: Confusion Matrix

### 1. What is a Confusion Matrix?
A Confusion Matrix is a $2 \times 2$ table used to evaluate the performance of a classification machine learning model. It compares the model's predicted outputs with the actual real-world values.

### 2. The 4 Key Terms
*   **TP (True Positive):** Model predicted YES, and the actual value was YES. *(Correct Prediction)*
*   **TN (True Negative):** Model predicted NO, and the actual value was NO. *(Correct Prediction)*
*   **FP (False Positive / Type-I Error):** Model predicted YES, but the actual value was NO. *(False Alarm)*
*   **FN (False Negative / Type-II Error):** Model predicted NO, but the actual value was YES. *(Missed Detection)*

### 3. Important Formulas (Based on Slide)
1.  **Accuracy:** $\frac{TP + TN}{TP + TN + FP + FN}$
2.  **Precision:** $\frac{TP}{TP + FP}$
3.  **Sensitivity (Recall):** $\frac{TP}{TP + FN}$
4.  **Specificity:** $\frac{TN}{TN + FP}$
5.  **Negative Predictive Value (NPV):** $\frac{TN}{TN + FN}$
6.  **F1-Score:** $2 \times \frac{Precision \times Sensitivity}{Precision + Sensitivity}$

---

### 4. Mathematical Example (Exam Practice)

**Question:**
An AI model was tested on 100 patients to detect a disease. Calculate all the metrics from the given data:
*   True Positive (TP) = 40
*   True Negative (TN) = 45
*   False Positive (FP) = 5
*   False Negative (FN) = 10

**Solution:**
*Total Data (N)* = $40 + 45 + 5 + 10 = 100$

**1. Accuracy:**
$$= \frac{TP + TN}{Total} = \frac{40 + 45}{100} = \frac{85}{100} = \mathbf{0.85}$$

**2. Precision:**
$$= \frac{TP}{TP + FP} = \frac{40}{40 + 5} = \frac{40}{45} = \mathbf{0.888}$$

**3. Sensitivity (Recall):**
$$= \frac{TP}{TP + FN} = \frac{40}{40 + 10} = \frac{40}{50} = \mathbf{0.80}$$

**4. Specificity:**
$$= \frac{TN}{TN + FP} = \frac{45}{45 + 5} = \frac{45}{50} = \mathbf{0.90}$$

**5. Negative Predictive Value (NPV):**
$$= \frac{TN}{TN + FN} = \frac{45}{45 + 10} = \frac{45}{55} = \mathbf{0.818}$$

**6. F1-Score:**
$$= 2 \times \frac{Precision \times Sensitivity}{Precision + Sensitivity} = 2 \times \frac{0.888 \times 0.80}{0.888 + 0.80} = \mathbf{0.841}$$


---



<!-- ============================================== -->


# 📄 Topic: Perceptron Xor Note

# Short Note: Perceptron & The XOR Problem

### 1. What is a Perceptron?
* A Perceptron is the simplest type of Artificial Neural Network (ANN). It is basically a single artificial neuron.
* **How it works:** It takes inputs, multiplies them by weights, adds them up (weighted sum), and passes the result through an activation function (like a threshold) to generate an output (usually 1 or 0).

### 2. Linear Separability (AND & OR Gates)
* A single Perceptron works by drawing a **single straight line** (called a decision boundary) to separate different classes of data.
* **AND Gate & OR Gate:** In these logic gates, we can easily draw one straight line on a graph to perfectly separate the '1' outputs from the '0' outputs.
* Because they can be separated by a single straight line, they are called **Linearly Separable** problems. A single perceptron can easily solve them.

### 3. The XOR Problem (Why Perceptron Fails)
* **What is XOR?** In an XOR gate, the output is 1 only when the inputs are different (e.g., 0,1 or 1,0). If inputs are the same (0,0 or 1,1), the output is 0.
* **The Problem:** If you plot the XOR data on a graph, the '1's and '0's are positioned diagonally (criss-crossed).
* It is **mathematically impossible** to draw a single straight line that separates the 0s from the 1s. 
* Because it cannot be separated by one line, XOR is called a **Linearly Inseparable** problem. Since a single Perceptron can only draw one line, it **completely fails** to solve the XOR problem.

### 4. The Solution to the XOR Problem
* To solve the XOR problem, we must draw **two or more lines**.
* **Solution:** We need to use a **Multi-Layer Perceptron (MLP)**. By adding "Hidden Layers" between the input and output, the neural network becomes capable of drawing multiple lines and solving complex, non-linear problems like XOR.


---



<!-- ============================================== -->


# 📄 Topic: Backpropagation Note

# Short Note: Backpropagation in ANN

### 1. What is Backpropagation?
* Backpropagation (short for "Backward Propagation of Errors") is the core learning algorithm for training Artificial Neural Networks.
* It is the process by which a neural network calculates its error and sends that error signal backward to fix its internal parameters.

### 2. How does it work? (The 3 Main Steps)
* **Step 1 (Forward Pass):** The input data travels forward through the network's layers, and the network makes a guess or prediction.
* **Step 2 (Calculate Error):** The network compares its prediction with the actual correct answer to find out how wrong it was. This difference is called the **Error** or Loss.
* **Step 3 (Backward Pass & Weight Update):** The error signal is sent backwards from the output layer to the hidden layers. Using an algorithm called **Gradient Descent**, the network updates and adjusts its "Weights" and "Biases" so that the error becomes smaller the next time.

### 3. Why is it Important?
* It is the primary mechanism that allows a neural network to actually **"learn"** from its mistakes.
* Without backpropagation, a neural network would just keep making random guesses forever and its accuracy would never improve. 
* By constantly repeating this forward-and-backward process, the network gradually becomes highly accurate.


---



<!-- ============================================== -->


# 📄 Topic: Backprop Math Steps

# Backpropagation Math (Step-by-Step Chain Rule)

When you need to update a weight connecting the **Hidden Layer to the Output Layer** (e.g., $w_5$ connected to $y1$), you must use the Chain Rule. The calculation is broken down into 3 easy pieces.

### The Main Chain Rule Formula (Example for $w_5$):
$$ \frac{\partial E_{total}}{\partial w_5} = \frac{\partial E_{total}}{\partial y1_{final}} \times \frac{\partial y1_{final}}{\partial y1} \times \frac{\partial y1}{\partial w_5} $$

---

### The 3 Pieces Explained

**Piece 1: The Error Difference (Target vs Actual)**
$$ \frac{\partial E_{total}}{\partial y1_{final}} = -(T_1 - y1_{final}) $$
*(Here, $T_1$ is the Target Value given in the question, and $y1_{final}$ is the output your network calculated).*

**Piece 2: Derivative of Sigmoid (Activation Function)**
$$ \frac{\partial y1_{final}}{\partial y1} = y1_{final}(1 - y1_{final}) $$

**Piece 3: The Input to that Specific Weight**
$$ \frac{\partial y1}{\partial w_5} = H1_{final} $$
*(Look at the graph: $w_5$ is connected to $H1$. So the input coming into $w_5$ is the final value of $H1$).*

---

### Calculating the Error Term (Delta $\delta$)
Sometimes the exam asks you to calculate the "Error" for a specific output node first. This is simply **Piece 1 $\times$ Piece 2**.

*   **Error for Output y1 (Delta y1):**
    $$ y1_{error} = -(T_1 - y1_{final}) \times [y1_{final} \times (1 - y1_{final})] $$

*   **Error for Output y2 (Delta y2):**
    $$ y2_{error} = -(T_2 - y2_{final}) \times [y2_{final} \times (1 - y2_{final})] $$

---

### Final Step: Updating the Weight
Once you have calculated the 3 pieces, multiply them together to find the total gradient, and then update the weight using the Learning Rate ($\eta$).

**1. Multiply the 3 pieces:**
$$ Gradient = Piece 1 \times Piece 2 \times Piece 3 $$

**2. Update the old weight:**
$$ w_5^{(new)} = w_5^{(old)} - (\eta \times Gradient) $$


---



<!-- ============================================== -->


# 📄 Topic: Kmeans Points Solution

# K-means Clustering Solution (2D Points) - Euclidean Method

**Given Data:**
8 Points: $A_1(2,10), A_2(2,5), A_3(8,4), A_4(5,8), A_5(7,5), A_6(6,4), A_7(1,2), A_8(4,9)$

**সূত্র (Euclidean Distance Formula):** 
$Distance = \sqrt{(x_1 - x_2)^2 + (y_1 - y_2)^2}$
*(দশমিকের পর ২ ঘর পর্যন্ত মান দেওয়া হলো যাতে হিসাব বুঝতে সুবিধা হয়)*

---

### 🔹 Iteration 1
**Centers (Seeds):** $C_1$=(2, 10), $C_2$=(5, 8), $C_3$=(1, 2)

| Point | Dist $C_1$ (2, 10) | Dist $C_2$ (5, 8) | Dist $C_3$ (1, 2) | Nearest Cluster |
| :--- | :--- | :--- | :--- | :--- |
| **A1 (2,10)** | **$0.00$** | $\sqrt{13}$ (3.61) | $\sqrt{65}$ (8.06) | **$C_1$** |
| **A2 (2,5)** | $\sqrt{25}$ (5.00) | $\sqrt{18}$ (4.24) | **$\sqrt{10}$ (3.16)** | **$C_3$** |
| **A3 (8,4)** | $\sqrt{36}$ (6.00) | **$\sqrt{25}$ (5.00)** | $\sqrt{53}$ (7.28) | **$C_2$** |
| **A4 (5,8)** | $\sqrt{13}$ (3.61) | **$0.00$** | $\sqrt{52}$ (7.21) | **$C_2$** |
| **A5 (7,5)** | $\sqrt{50}$ (7.07) | **$\sqrt{13}$ (3.61)** | $\sqrt{45}$ (6.71) | **$C_2$** |
| **A6 (6,4)** | $\sqrt{52}$ (7.21) | **$\sqrt{17}$ (4.12)** | $\sqrt{29}$ (5.39) | **$C_2$** |
| **A7 (1,2)** | $\sqrt{65}$ (8.06) | $\sqrt{52}$ (7.21) | **$0.00$** | **$C_3$** |
| **A8 (4,9)** | $\sqrt{5}$ (2.24) | **$\sqrt{2}$ (1.41)** | $\sqrt{58}$ (7.62) | **$C_2$** |

**New Clusters & Centers:**
*   $C_1$: A1 $\Rightarrow$ **New $C_1$ = (2, 10)**
*   $C_2$: A3, A4, A5, A6, A8 $\Rightarrow$ **New $C_2$ = (6, 6)** 
*   $C_3$: A2, A7 $\Rightarrow$ **New $C_3$ = (1.5, 3.5)**

---

### 🔹 Iteration 2
**Centers:** $C_1$=(2, 10), $C_2$=(6, 6), $C_3$=(1.5, 3.5)

| Point | Dist $C_1$ (2, 10) | Dist $C_2$ (6, 6) | Dist $C_3$ (1.5, 3.5) | Nearest Cluster |
| :--- | :--- | :--- | :--- | :--- |
| **A1 (2,10)** | **0.00** | 5.66 | 6.52 | **$C_1$** |
| **A2 (2,5)** | 5.00 | 4.12 | **1.58** | **$C_3$** |
| **A3 (8,4)** | 8.49 | **2.83** | 6.52 | **$C_2$** |
| **A4 (5,8)** | 3.61 | **2.24** | 5.70 | **$C_2$** |
| **A5 (7,5)** | 7.07 | **1.41** | 5.70 | **$C_2$** |
| **A6 (6,4)** | 7.21 | **2.00** | 4.53 | **$C_2$** |
| **A7 (1,2)** | 8.06 | 6.40 | **1.58** | **$C_3$** |
| **A8 (4,9)** | **2.24** | 3.61 | 6.04 | **$C_1$** (Moved!) |

**New Clusters & Centers:**
*   $C_1$: A1, A8 $\Rightarrow$ **New $C_1$ = (3, 9.5)**
*   $C_2$: A3, A4, A5, A6 $\Rightarrow$ **New $C_2$ = (6.5, 5.25)**
*   $C_3$: A2, A7 $\Rightarrow$ **New $C_3$ = (1.5, 3.5)**

---

### 🔹 Iteration 3
**Centers:** $C_1$=(3, 9.5), $C_2$=(6.5, 5.25), $C_3$=(1.5, 3.5)

| Point | Dist $C_1$ (3, 9.5) | Dist $C_2$ (6.5, 5.25) | Dist $C_3$ (1.5, 3.5) | Nearest Cluster |
| :--- | :--- | :--- | :--- | :--- |
| **A1 (2,10)** | **1.12** | 6.54 | 6.52 | **$C_1$** |
| **A2 (2,5)** | 4.61 | 4.51 | **1.58** | **$C_3$** |
| **A3 (8,4)** | 7.43 | **1.95** | 6.52 | **$C_2$** |
| **A4 (5,8)** | **2.50** | 3.13 | 5.70 | **$C_1$** (Moved!) |
| **A5 (7,5)** | 6.02 | **0.56** | 5.70 | **$C_2$** |
| **A6 (6,4)** | 6.26 | **1.35** | 4.53 | **$C_2$** |
| **A7 (1,2)** | 7.76 | 6.39 | **1.58** | **$C_3$** |
| **A8 (4,9)** | **1.12** | 4.51 | 6.04 | **$C_1$** |

**New Clusters & Centers:**
*   $C_1$: A1, A4, A8 $\Rightarrow$ **New $C_1$ = (3.66, 9)**
*   $C_2$: A3, A5, A6 $\Rightarrow$ **New $C_2$ = (7, 4.33)**
*   $C_3$: A2, A7 $\Rightarrow$ **New $C_3$ = (1.5, 3.5)**

### ✅ Conclusion:
Algorithm stops here as no more points will move to a different cluster.


---



<!-- ============================================== -->


# 📄 Topic: Kmeans Solution

# K-means Clustering Solution (Student Dataset)

**Given Data:**
10 Students with 4 Attributes: (Age, Marks1, Marks2, Marks3)
**Initial Centers:** $C_1 = s_1$, $C_2 = s_2$, $C_3 = s_3$
**Distance Metric:** Manhattan Distance ($|x_1 - x_2| + |y_1 - y_2| + |z_1 - z_2| + |w_1 - w_2|$)

---

## 🟢 Iteration 1: Distance Calculation

Calculate the distance from each student to the 3 initial centers.

| Student | Data (Age, M1, M2, M3) | Distance to $C_1$ (18, 73, 75, 57) | Distance to $C_2$ (18, 79, 85, 75) | Distance to $C_3$ (23, 70, 70, 52) | Nearest Cluster |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **$s_1$** | (18, 73, 75, 57) | **0** | 34 | 18 | **$C_1$** |
| **$s_2$** | (18, 79, 85, 75) | 34 | **0** | 52 | **$C_2$** |
| **$s_3$** | (23, 70, 70, 52) | 18 | 52 | **0** | **$C_3$** |
| **$s_4$** | (20, 55, 55, 55) | 42 | 76 | **36** | **$C_3$** |
| **$s_5$** | (22, 85, 86, 87) | 57 | **23** | 67 | **$C_2$** |
| **$s_6$** | (19, 91, 90, 89) | 66 | **32** | 82 | **$C_2$** |
| **$s_7$** | (20, 70, 65, 60) | 18 | 46 | **16** | **$C_3$** |
| **$s_8$** | (21, 53, 56, 59) | 44 | 74 | **40** | **$C_3$** |
| **$s_9$** | (19, 82, 82, 60) | **20** | 22 | 36 | **$C_1$** |
| **$s_{10}$** | (47, 75, 76, 77) | 52 | **44** | 60 | **$C_2$** |

### 📌 Iteration 1 Resulting Clusters:
*   **Cluster 1:** $s_1, s_9$
*   **Cluster 2:** $s_2, s_5, s_6, s_{10}$
*   **Cluster 3:** $s_3, s_4, s_7, s_8$

---

## 🟢 Calculating New Cluster Centers (Means)

We average the values of the students in each cluster to find the new centers.

| Cluster | Members | Age (Avg) | Marks1 (Avg) | Marks2 (Avg) | Marks3 (Avg) | **New Center Coordinates** |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **$C_1$** | $s_1, s_9$ | (18+19)/2 = **18.5** | (73+82)/2 = **77.5** | (75+82)/2 = **78.5** | (57+60)/2 = **58.5** | **(18.5, 77.5, 78.5, 58.5)** |
| **$C_2$** | $s_2, s_5, s_6, s_{10}$ | 106/4 = **26.5** | 330/4 = **82.5** | 337/4 = **84.3** | 328/4 = **82.0** | **(26.5, 82.5, 84.3, 82.0)** |
| **$C_3$** | $s_3, s_4, s_7, s_8$ | 84/4 = **21.0** | 248/4 = **62.0** | 246/4 = **61.5** | 226/4 = **56.5** | **(21.0, 62.0, 61.5, 56.5)** |

---

## 🟢 Iteration 2: Distance Calculation (with New Centers)

Calculate the distances again using the newly found centers.

| Student | Data | Dist to New $C_1$ (18.5, 77.5, 78.5, 58.5) | Dist to New $C_2$ (26.5, 82.5, 84.3, 82) | Dist to New $C_3$ (21, 62, 61.5, 56.5) | Nearest Cluster |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **$s_1$** | (18, 73, 75, 57) | **10.0** | 52.3 | 28.0 | **$C_1$** |
| **$s_2$** | (18, 79, 85, 75) | 25.0 | **19.8** | 62.0 | **$C_2$** |
| **$s_3$** | (23, 70, 70, 52) | 27.0 | 60.3 | **23.0** | **$C_3$** |
| **$s_4$** | (20, 55, 55, 55) | 51.0 | 90.3 | **16.0** | **$C_3$** |
| **$s_5$** | (22, 85, 86, 87) | 47.0 | **13.8** | 79.0 | **$C_2$** |
| **$s_6$** | (19, 91, 90, 89) | 56.0 | **28.8** | 92.0 | **$C_2$** |
| **$s_7$** | (20, 70, 65, 60) | 24.0 | 60.3 | **16.0** | **$C_3$** |
| **$s_8$** | (21, 53, 56, 59) | 50.0 | 86.3 | **17.0** | **$C_3$** |
| **$s_9$** | (19, 82, 82, 60) | **10.0** | 32.3 | 46.0 | **$C_1$** |
| **$s_{10}$** | (47, 75, 76, 77) | 52.0 | **41.3** | 74.0 | **$C_2$** |

### 📌 Iteration 2 Resulting Clusters:
*   **Cluster 1:** $s_1, s_9$
*   **Cluster 2:** $s_2, s_5, s_6, s_{10}$
*   **Cluster 3:** $s_3, s_4, s_7, s_8$

---

### ✅ Conclusion:
As you can see, the clusters in Iteration 2 are **exactly the same** as the clusters in Iteration 1. Since no student moved to a different cluster, the algorithm has converged and we **stop here**.


---

