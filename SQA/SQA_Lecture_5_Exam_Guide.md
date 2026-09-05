# SQA Lecture 5: Final Exam Guide 🎯 (Most Important 🌟)

এই পিডিএফটি পুরো সিলেবাসের সবচেয়ে ইম্পর্টেন্ট অংশ। এখানে মূল ফোকাস হলো **Cleanroom Software Engineering** এবং **Formal Methods** এর ওপর।

---

## 1. Cleanroom Software Engineering কী?

**English (Exam Answer):**
The cleanroom strategy is a software engineering approach that emphasizes building software correctly from the start. It focuses on avoiding mistakes during development rather than testing to find errors later. 
It involves breaking the development process into small parts called "increments", which are developed by small independent teams.

**বাংলা সামারি:** 
সাধারণত আমরা সফটওয়্যার বানানোর পর টেস্ট করে ভুল ধরি। কিন্তু **Cleanroom Strategy** হলো এমন একটা টেকনিক, যেখানে শুরু থেকেই এত নিখুঁতভাবে (ম্যাথমেটিক্যাল রুলস ফলো করে) কোড করা হয় যে, পরে আর কোনো বাগ (bug) থাকেই না! পুরো প্রজেক্টকে ছোট ছোট "Increment" এ ভাগ করে কাজ করা হয়।

---

## 2. Steps of Cleanroom Process Model (🌟 Very Important)

> [!TIP]
> **💡 Exam Tip (Diagram):** আপনার লেকচার ৫-এর **৪ নাম্বার স্লাইডে** "The Cleanroom Process Model" নামে একটা বড় ফিগার আছে। পরীক্ষায় এই প্রশ্নটা আসলে অবশ্যই ফিগারটা আঁকবেন! ফিগারটা মূলত সিঁড়ির মতো— যেখানে **Increment #1, Increment #2, Increment #n** দিয়ে পরপর বক্স করে ধাপগুলো দেখানো হয়েছে। খুব ডিটেইলে না পারলেও অন্তত ২টা ইনক্রিমেন্টের বক্সগুলো খাতায় এঁকে দেবেন। ফুল মার্কস গ্যারান্টিড!

**💡 Mnemonic (মনে রাখার ট্রিক): "IRB FCC SC"** (আইআরবি এফসিসি এসসি)

**English (Exam Answer):**
1. **I - Increment Planning:** Focuses on delivering valuable features to end-users.
2. **R - Requirements Gathering:** Collecting clear and consistent requirements.
3. **B - Box Structure Specification:** Understanding the overall structure using Box models (Black, State, Clear).
4. **F - Formal Design:** Specifying how components interact.
5. **C - Correctness Verification:** Catching issues early in the design phase.
6. **C - Code Generation & Inspection:** Writing code and inspecting to catch errors before execution.
7. **S - Statistical Testing:** Testing based on real user behavior probabilities.
8. **C - Certification:** Certifying that the software is reliable and ready for users.

**বাংলা সামারি:** 
প্রথমে প্ল্যান করা (I), তারপর রিকোয়ারমেন্ট নেওয়া (R), এরপর বক্স ডায়াগ্রাম বানানো (B), ডিজাইন করা (F), সেই ডিজাইনটা ঠিক আছে কি না ভেরিফাই করা (C), কোড লেখা (C), রিয়েল ইউজারের মতো টেস্ট করা (S), এবং সবশেষে সফটওয়্যার রিলিজের জন্য সার্টিফিকেট দেওয়া (C)।

---

## 3. Types of Box Structure Specification (খুবই ইম্পর্টেন্ট 🌟)

**English (Exam Answer):**
1. **Black Box Specification:** Represents the input-output relationship without internal details. Notation: $f(S^*) = R$. 
   *   *Example:* Withdrawing cash from an ATM (you just give input and get output).
2. **State Box Specification:** Explains how a system behaves over time and transitions between states.
   *   *Example:* Traffic lights (Red $\rightarrow$ Green $\rightarrow$ Yellow).
3. **Clear Box Specification:** Provides insight into the underlying procedural design and implementation.
   *   *Example:* Online e-commerce site (how the cart, payment, and checkout logic works internally).

**বাংলা সামারি:** 
*   **Black Box:** শুধু ইনপুট-আউটপুট দেখবে, ভেতরে কী হচ্ছে দেখবে না।
*   **State Box:** সময়ের সাথে সাথে সফটওয়্যার কীভাবে এক অবস্থা (State) থেকে অন্য অবস্থায় যায় তা দেখবে।
*   **Clear Box:** ভেতরের একদম সব কোডিং লজিক ক্লিয়ারলি দেখবে।

---

## 3.5. Box Structure Refinement

**English (Exam Answer):**
Box Structure refinement is a way to breakdown complex software systems into smaller, more manageable parts. 
* It starts with a high-level description of the system's behavior.
* Then it breaks it down into smaller parts that each address a specific aspect of the behavior.
* This process continues until each part is small enough to be easily understood and designed.

**বাংলা সামারি:**
Refinement মানে হলো বিশাল ও জটিল কোনো সফটওয়্যার সিস্টেমকে ভেঙে ছোট ছোট এবং সহজ অংশে ভাগ করা। বড় একটা কাজকে ছোট ছোট অংশে ভাগ করতে থাকলে একসময় সেটা বোঝা এবং ডিজাইন করা খুব সহজ হয়ে যায়।

## 3.6. Cleanroom Design

**English (Exam Answer):**
Cleanroom design is an approach that emphasizes building correctness into software as it is being developed. It has two main parts:

1. **Design Refinement:** Breaking down the high-level functional specification into smaller, detailed components called subfunctions.
   * *Example:* A Banking Application includes features like (a) Account Creation, (b) Deposits, (c) Withdrawals, and (d) Transfers.
2. **Design Verification:** Ensuring that the refined software design is correct and meets the functional specifications using formal methods and mathematical proofs.

**বাংলা সামারি:**
কোড লেখার আগে ডিজাইনটাকে দুই ধাপে ভাগ করা হয়। প্রথমে বড় কাজকে ছোট ছোট ফিচারে ভাঙা হয় (যেমন ব্যাংকিং অ্যাপকে ডিপোজিট, উইথড্র এসব ফিচারে ভাগ করা), যাকে বলে **Refinement**। এরপর ম্যাথ বা লজিক দিয়ে চেক করা হয় যে এই ডিজাইনটা আসলেই কাজ করবে কি না, যাকে বলে **Verification**।

---

## 3.7. Cleanroom Testing

**English (Exam Answer):**
1. **Cleanroom Testing:** Creating test cases based on the software's design and code to find errors (includes unit, integration, and system tests).
2. **Statistical Use Testing:** Understanding user interactions, assigning probabilities to those interactions, and creating test cases based on those probabilities.

**বাংলা সামারি:**
Cleanroom-এ সাধারণ টেস্টিংয়ের পাশাপাশি **Statistical Use Testing** করা হয়। এর মানে হলো, ইউজার বাস্তবে কোন ফিচারে বেশি ক্লিক করবে বা কোন কাজটা বেশি করবে, তার প্রবাবিলিটি (Probability) বা সম্ভাবনা হিসাব করে সেই অনুযায়ী টেস্ট করা।

---

## 4. Cleanroom Certification Process

**English (Exam Answer):**
Certification implies that the software has achieved a specific level of reliability.
**Steps:**
1. **Create Usage Scenarios:** Describe how users interact.
2. **Specify a Usage Profile:** Determine the probability of each scenario.
3. **Generate Test Cases:** Create tests covering different user interactions.
4. **Execute Tests & Record Data:** Identify defects and assess reliability.
5. **Compute & Certify Reliability:** Using Sampling model, Component model, and Certification model.

**বাংলা সামারি:**
সফটওয়্যারটি বাজারে ছাড়ার জন্য 'সার্টিফিকেট' দেওয়ার প্রসেস:
১. ইউজার অ্যাপে ঢুকে কী কী করতে পারে তা চিন্তা করা (Scenarios)।
২. কোন কাজটা ইউজার বেশি করবে তার পার্সেন্টেজ/সম্ভাবনা বের করা (Profile)।
৩. সেই পার্সেন্টেজ অনুযায়ী টেস্ট কেস বানানো (Test cases)।
৪. টেস্ট রান করে দেখা এবং কোনো ভুল পেলে রেকর্ড করা (Execute & Record)।
৫. সবশেষে মডেলিং বা ম্যাথ ব্যবহার করে সফটওয়্যারের কোয়ালিটি সার্টিফাই করা (Certify)।

---

## 5. Advantages & Disadvantages of Cleanroom Strategy

**English (Exam Answer):**

**Advantages (সুবিধা):**
1. **Defect Prevention:** Prevents errors early, leading to better software performance. *(ভুল হওয়ার আগেই আটকে দেয়, ফলে পারফরম্যান্স ভালো হয়)*
2. **Less Testing & Rework:** Reduces the need for extensive testing and fixing bugs later. *(যেহেতু শুরুতেই সব চেক করা হয়, তাই পরে গিয়ে বারবার টেস্ট করা বা ঠিক করার দরকার হয় না)*
3. **Uses Formal Methods:** Reduces defects by using mathematical methods to verify design correctness. *(ম্যাথ বা লজিক দিয়ে চেক করার কারণে ভুল হওয়ার চান্স কমে যায়)*

**Disadvantages (অসুবিধা):**
1. **Time Consuming:** Takes a lot of time and effort to implement. *(অনেক বেশি সময় ও পরিশ্রম লাগে)*
2. **Not for All Projects:** May not be suitable for every type of software project. *(সব ধরনের প্রজেক্টে এই টেকনিক খাটানো যায় না)*
3. **Needs Extra Training:** Requires additional training and expertise, which increases the cost. *(ডেভেলপারদের স্পেশাল ম্যাথমেটিক্যাল ট্রেনিং দিতে হয়, ফলে খরচ বাড়ে)*

---

## 6. Important Concepts in Formal Methods (🌟 Very Important)

**💡 Mnemonic (মনে রাখার ট্রিক): "POS DIP"** (পস ডিপ - ধরুন দোকানে গিয়ে POS মেশিনে কার্ড DIP বা পাঞ্চ করছেন)

**English (Exam Answer):**
1. **P - Precondition:** Requirements that must be satisfied *before* an operation. *(কোনো কাজ শুরু করার আগের শর্ত)*
2. **O - Operation:** An action that reads or writes data within the system. *(সিস্টেমের ভেতরে কোনো কাজ করা)*
3. **S - State:** The stored data of a system at any point in time. *(সিস্টেমের বর্তমান অবস্থা বা ডাটা)*
4. **D - Data Invariant:** Ensuring that certain properties hold true at all times, even as the system changes state. *(এমন একটা রুল বা শর্ত যেটা কখনোই ভাঙবে না)*
5. **I - Invariant:** A condition that doesn't change during an operation. *(কাজের সময় যে রুলস অপরিবর্তিত থাকে)*
6. **P - Postcondition:** Specifies the effects *after* an operation. *(কাজ শেষ হওয়ার পরের অবস্থা)*

---

## 7. Formal Specification Languages (FSL)

**What is FSL? (English Exam Answer):**
It is a formal language that uses **math and logic** to design secure software. It is mostly used in high-risk projects like airplanes or hospital machines, where mistakes are not allowed.

**Three Main Components of FSL (Traffic Light Example):**

1. **Syntax (The writing format):** It defines how the rules are written.
   * *Example:* A traffic light has 3 states: Red, Yellow, and Green.
2. **Semantics (The actual meaning):** It defines the meaning behind the symbols or words.
   * *Example:* Red means "Stop", Green means "Go", and Yellow means "Wait".
3. **Relations (The connection):** It describes how different parts interact with each other based on rules.
   * *Example:* Only one light can turn ON at a time. After Red, Green MUST turn ON.

---

## 8. Types of FSL (OCL and Z)

**1. Object Constraint Language (OCL):**
Used with UML to specify constraints on objects.
*Key Aspects:*
*   **Invariants:** Conditions that must hold true for a class.
*   **Preconditions & Postconditions:** Conditions before and after an operation.
*   **Guard Conditions:** Constraints that must be satisfied for a specific event.
*   **Derived Attributes:** Attributes computed based on other attributes.

**2. Z Specification Language:**
Uses mathematical symbols (sets, predicates) and breaks systems into smaller parts called **"schemas"** (like pieces of a puzzle).

---

## 9. Advantages & Disadvantages of FSL

**Advantages:**
1. Provides a precise and unambiguous description. *(একদম নিখুঁত বর্ণনা দেয়)*
2. Catches errors early in the design process. *(শুরুতেই ভুল ধরে ফেলে)*
3. Improves communication between stakeholders. *(সবার মধ্যে বোঝাপড়া ভালো হয়)*
4. Verifies correctness using constraints. *(সঠিকভাবে কাজ করবে কি না তা শিওর করে)*

**Disadvantages:**
1. Complex and difficult to learn (requires math). *(শেখা খুব কঠিন)*
2. Time-consuming. *(অনেক সময় লাগে)*
3. Not suitable for all domains/systems. *(সব প্রজেক্টে খাটানো যায় না)*
