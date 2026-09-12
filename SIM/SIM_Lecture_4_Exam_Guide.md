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
