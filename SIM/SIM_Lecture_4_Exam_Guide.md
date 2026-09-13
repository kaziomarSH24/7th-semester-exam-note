# SIM Lecture 4 - COCOMO Model (Math Guide) 🌟

## 1. What is COCOMO?
**English:** COCOMO is a math model to estimate **Effort**, **Time**, and **Cost** based on software size (KLOC - Kilo Lines of Code).

## 2. The 3 Categories of Projects (Slide 3, 4)
**English:** Before doing the math, identify the project type:
1. **Organic:** Small and simple projects. (Size: 2-50 KLOC)
2. **Semidetached:** Medium projects. (Size: 51-300 KLOC)
3. **Embedded:** Large and complex projects. (Size: >300 KLOC)

## 3. The Formulas You Need to Memorize! 🧮
**1. Effort (E):** $E = a_1 \times (KLOC)^{a_2}$  (Unit: pm or Person-Months)
**2. Time (T):** $T = 2.5 \times (E)^b$  (Unit: months)
**3. Average Staff Size (People):** $Staff = \frac{Effort}{Time}$  (Unit: persons)
**4. Productivity:** $Productivity = \frac{KLOC}{Effort}$  (Unit: KLOC/PM)

*Note: For **Intermediate COCOMO**, the Effort formula adds an **EAF** (Effort Adjustment Factor). EAF is the multiplication of all given cost drivers.*
*Intermediate Effort:* $E = a_1 \times (KLOC)^{a_2} \times EAF$

## 4. The Magic Table (Must Memorize for Exams!)
| Project Category | $a_1$ (Basic) | $a_1$ (Intermediate) | $a_2$ | $b$ |
| :--- | :--- | :--- | :--- | :--- |
| **Organic** | 2.4 | 3.2 | 1.05 | 0.38 |
| **Semidetached** | 3.0 | 3.0 | 1.12 | 0.35 |
| **Embedded** | 3.6 | 2.8 | 1.20 | 0.32 |

---

## 5. Solved Math Examples (From Slides)

### Example 1: Basic COCOMO (Slide 7)
**Question:** Consider an **embedded** project with **700 KLOC**. Calculate the effort, development time, average staff size, and productivity.
**Solution:**
Since it's "Embedded" and "Basic COCOMO" (no cost drivers given), we use: $a_1 = 3.6$, $a_2 = 1.20$, $b = 0.32$.

1. **Effort (E):**
   $E = 3.6 \times (700)^{1.20} = 9341.58 \text{ pm}$
2. **Time (T):**
   $T = 2.5 \times (9341.58)^{0.32} = 46.61 \text{ months}$
3. **Average Staff Size:**
   $Staff = \frac{9341.58}{46.61} = 200.42 \text{ persons}$
4. **Productivity:**
   $Productivity = \frac{700}{9341.58} = 0.0749 \text{ KLOC/PM}$

### Example 2: Intermediate COCOMO (Slide 12)
**Question:** Consider a project with **250 KLOC**. 
Cost Drivers: Nominal DB (1.00), High memory constraints (1.06), High application experience (0.91), Very low programming experience (1.14), Low dev schedule (1.08). Calculate effort, time, and staff.
**Solution:**
Size is 250 KLOC, which falls under **Semidetached** (51-300 KLOC). So, we use the intermediate values: $a_1 = 3.0$, $a_2 = 1.12$, $b = 0.35$.

1. **Calculate EAF (Multiply all cost drivers):**
   $EAF = 1.00 \times 1.06 \times 0.91 \times 1.14 \times 1.08 = 1.187$
   *(Note: Slides may skip showing 1.187 and just multiply them directly)*
2. **Effort (E):**
   $E = 3.0 \times (250)^{1.12} \times EAF$
   $E = 3.0 \times 485.33 \times 1.187 = 1727.79 \text{ pm}$
3. **Time (T):**
   $T = 2.5 \times (1727.79)^{0.35} = 33.97 \text{ months}$
4. **Average Staff Size:**
   $Staff = \frac{1727.79}{33.97} = 50.86 \text{ persons}$

---
**বাংলা সামারি (কীভাবে ম্যাথ করবেন):** 
COCOMO ম্যাথ করার জন্য আপনাকে শুধু ৩টা জিনিস মাথায় রাখতে হবে: 
১. প্রথমে প্রজেক্টের সাইজ (KLOC) দেখে ক্যাটাগরি (Organic, Semi, Embedded) বের করবেন।
২. ওই ক্যাটাগরির $a_1, a_2, b$ এর মান মুখস্থ টেবিল থেকে বসাবেন।
৩. ক্যালকুলেটরে সূত্র (Effort, Time, Staff) দিয়ে হিসাব করে ফেলবেন! Intermediate এর ক্ষেত্রে শুধু EAF (প্রশ্নে দেওয়া সবগুলো কন্ডিশনের গুণফল) এক্সট্রা গুণ করতে হয় Effort-এর সাথে।

---

## 6. Previous Class Test Solution (Important!)

### Q1. Differentiate between Basic, Intermediate, and Detailed COCOMO. Explain advantages and limitations.
**Answer:**
**Difference:**
1.  **Basic COCOMO:** It calculates software cost and effort based **only on the size** of the program (KLOC). It is used for quick and early estimates.
2.  **Intermediate COCOMO:** It calculates cost based on the size (KLOC) **AND 15 cost drivers** (like team experience, memory constraints). It uses an Effort Adjustment Factor (EAF).
3.  **Detailed COCOMO:** It is the most advanced model. It calculates the impact of cost drivers on **each individual phase** (planning, design, coding, testing) of the project.

**Advantages and Limitations:**
*   **Basic COCOMO:**
    *   *Advantage:* Very simple and fast to calculate.
    *   *Limitation:* Low accuracy because it ignores team skills and hardware constraints.
*   **Intermediate COCOMO:**
    *   *Advantage:* More accurate because it considers 15 real-world cost drivers.
    *   *Limitation:* Estimating the exact value of cost drivers can be subjective/guesswork.
*   **Detailed COCOMO:**
    *   *Advantage:* Highest accuracy as it calculates effort for every single development phase.
    *   *Limitation:* Extremely complex and time-consuming to calculate.

### Q2. Math Problem: Semidetached project with 200 KLOC. Cost Drivers given. Calculate EAF, Effort, Time, Staff.
**Answer:**
**Given Data:**
*   Model Category: **Semidetached**
*   Size (KLOC): **200**
*   Cost Drivers: Reliability (1.15), Memory (1.06), App Exp (0.91), Lang Exp (1.07), Schedule (1.00)

**Constants for Semidetached (Intermediate):**
*   $a_1 = 3.0$
*   $a_2 = 1.12$
*   $b = 0.35$

**Calculations:**
**i. Effort Adjustment Factor (EAF):**
$EAF = 1.15 \times 1.06 \times 0.91 \times 1.07 \times 1.00$
**EAF = 1.187**

**ii. Total Effort (E):**
Formula: $E = a_1 \times (KLOC)^{a_2} \times EAF$
$E = 3.0 \times (200)^{1.12} \times 1.187$
$E = 3.0 \times 373.197 \times 1.187$
**Total Effort (E) = 1329.13 pm**

**iii. Development Time (T):**
Formula: $T = 2.5 \times (E)^b$
$T = 2.5 \times (1329.13)^{0.35}$
$T = 2.5 \times 12.569$
**Development Time (T) = 31.42 months**

**iv. Average Staff Size:**
Formula: $Staff = \frac{Effort}{Time}$
$Staff = \frac{1329.13}{31.42}$
**Average Staff Size = 42.30 Persons (approx 42 Persons)**
