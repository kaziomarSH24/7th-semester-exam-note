# SIM Compulsory Part: Lecture 5 & 6 (Short Suggestion)

---

## 📌 Lecture 5: Software Testing Strategies & Debugging
*(Suggested Slides: 2, 5-8, 14-21)*

### 1. What is Testing Strategy? (Slide 2)
**English:** It is a plan for testing. It tells us:
*   What to test and when to test.
*   How much time and effort is needed.
*   **Steps:** Plan $\rightarrow$ Design $\rightarrow$ Execute $\rightarrow$ Evaluate.
**বাংলা সামারি:** সফটওয়্যার টেস্টিংয়ের পুরো প্ল্যানিং বা রোডম্যাপ। কী টেস্ট করব, কখন করব এবং কত সময় লাগবে, সেটাই টেস্টিং স্ট্র্যাটেজি।

### 2. Difference between Verification and Validation (V&V). (Slide 5) 🌟
**English:**
| Verification (Building the product right) | Validation (Building the right product) |
| :--- | :--- |
| Are we writing the code correctly? | Are we making the right product for the customer? |
| Focuses on **design and code**. | Focuses on **customer needs**. |

**বাংলা সামারি:** **Verification** হলো আমি ডিজাইনের নিয়ম মেনে কোড লিখছি কি না। আর **Validation** হলো কাস্টমার আসলে যেটা চেয়েছিল, আমি সেটা বানাচ্ছি কি না।

### 3. Key SQA Activities in V&V. (Slide 6)
**English:**
1. Technical reviews (finding errors early).
2. Quality audits.
3. Performance monitoring.
4. Simulation (virtual testing).
5. Documentation review.

### 4. Organizing for Testing (Slide 7)
**English:**
*   **Psychology:** Developers love to build software. But testing finds bugs in their hard work. So, developers do not like testing.
*   **False ideas (ভুল ধারণা):**
    1. Developers should not test. (False)
    2. Outsiders should test the software. (False)
*   **Reality (সত্যিটা কী):**
    1. Developers and testers must work together.
    2. Testing should start early.

### 5. Testing Strategy for Conventional Software. (Slide 8)
**English:**
1.  **Unit Testing:** Tests one module at a time.
2.  **Integration Testing:** Tests multiple modules together.
3.  **Validation Testing:** Checks if the customer is happy.
4.  **System Testing:** Tests the whole software system.
**💡 Mnemonic:** **UIVS** (ইউ আই ভি এস).

### 6. What is Debugging and its Process? (Slide 14, 15)
**English:** 
*   **Definition:** Debugging means finding and fixing bugs. It is like an art because it needs logic and experience.
*   **Process:**
    1. Run the test.
    2. Find the error (symptom).
    3. Find the real root cause of the error.
    4. Fix the bug.
**বাংলা সামারি:** টেস্টিং শুধু ভুল (bug) খুঁজে বের করে, আর ডিবাগিং সেই ভুলটার আসল কারণ (root cause) খুঁজে বের করে সেটা সলভ করে।

### 7. Why is Debugging Difficult? (Slide 17, 18) 🌟
**English:** 
1. Symptom and root cause can be far away.
2. Fixing one bug can hide another bug.
3. Timing issues can cause errors.
4. Some bugs happen rarely.

### 8. Debugging Strategies. (Slide 19-21)
**English:** 
1.  **Brute Force:** Developers just print variables to find the bug. It is a blind guess and wastes a lot of time. (Least efficient).
2.  **Backtracking:** Developers start from the error line. Then they go backward line-by-line to find the root cause. (Good for small programs).
3.  **Cause Elimination:** Developers use logic. They make a list of possible causes and eliminate the wrong ones step-by-step. (Best method).
**বাংলা সামারি:** Brute Force হলো চোখ বন্ধ করে প্রিন্ট স্টেটমেন্ট দিয়ে ভুল খোঁজা। Backtracking হলো যেখান থেকে এরর এসেছে, সেখান থেকে উল্টো দিকে চেক করা। আর Cause elimination হলো লজিক খাটিয়ে আসল ভুলের কাছে পৌঁছানো।

---

## 📌 Lecture 6: Test Strategies for Conventional Software
*(Suggested Slides: 3, 5, 7-18)*

### 1. What is Unit Testing and its Targets? (Slide 3, 5)
**English:** Unit testing tests a single module. It checks the internal logic of that module.

**💡 Diagram (খাতায় আঁকার জন্য):**
![Unit Testing Diagram](images/media_1789134843024.png)

*   **Targets for Unit Test (কী কী চেক করা হয়):**
    1. **Interface:** Checks if data flows in and out correctly.
    2. **Local data:** Checks if temporary data is saved correctly.
    3. **Boundary:** Checks what happens at maximum and minimum limits.
    4. **Paths:** Runs every single line of code at least once.
    5. **Error handling:** Checks if the software shows correct error messages.

### 2. Drivers and Stubs in Unit Testing. (Slide 7) 🌟
**English:** 
*   **Driver:** A dummy main program. It passes data to the tested module. (Acts like a boss).
*   **Stub:** A dummy worker program. It replaces lower-level modules. (Acts like a worker).
**বাংলা সামারি:** একটা মডিউল টেস্ট করার সময় তার ওপরের লেভেলকে ডাকার জন্য লাগে **Driver**, আর নিচের লেভেল রেডি না থাকলে ডামি হিসেবে লাগে **Stub**। 

### 3. Integration Testing. (Slide 8, 9)
**English:** 
*   **Definition:** It combines unit-tested modules and tests them together.
*   **Two Strategies:** 
    1. **Big Bang:** Combines all modules at once. (Bad idea).
    2. **Incremental:** Combines modules step-by-step. (Good idea).

### 4. Incremental Integration (Top-Down vs Bottom-Up). (Slide 11-14) 🌟
**English:**
| Feature | Top-Down Integration | Bottom-Up Integration |
| :--- | :--- | :--- |
| **Direction** | Goes from top to bottom. | Goes from bottom to top. |
| **Needs** | Needs **Stubs**. | Needs **Drivers**. |
| **Advantage** | Tests major control points early. | Tests lower data processing early. |

**📝 For Broad Question:**

#### A. Top-Down Integration
*   It starts from the main top module.
*   It goes down step-by-step to lower modules.
*   Lower modules are not ready yet.
*   So, we replace lower modules with dummy worker programs called **Stubs**.

**✅ Advantages (সুবিধা):**
1. It tests the main logic (major control points) very early.
2. If there are big design mistakes in the top modules, we can find them quickly.
3. We get a working prototype of the software very early.

**❌ Disadvantages (অসুবিধা):**
1. It needs many Stubs (dummy programs), which wastes development time.
2. Testing for lower-level data processing is delayed.
3. It is hard to observe test outputs from deep within the system.

*   **Diagram:**
![Top-Down Integration](images/media_1789135556717.png)

#### B. Bottom-Up Integration
*   It starts from the lowest-level modules.
*   It goes up step-by-step to the main module.
*   Top modules are not ready yet.
*   So, we replace top modules with dummy boss programs called **Drivers**.

**✅ Advantages (সুবিধা):**
1. It tests lower-level data processing very early.
2. It does not need any Stubs (dummy worker programs).
3. It is much easier to observe test results at the bottom level.

**❌ Disadvantages (অসুবিধা):**
1. It needs many Drivers, which wastes development time.
2. We cannot see a working prototype of the whole system until the end.
3. Big design mistakes in the top modules are found very late.

*   **Diagram:**
![Bottom-Up Integration](images/media_1789135538355.png)

### 5. Sandwich Integration. (Slide 15, 16)
**English:** 
*   It is a mix of Top-Down and Bottom-Up integration.
*   It tests high and low modules together in groups.
*   It minimizes the need for many drivers and stubs.

**💡 Diagram (খাতায় আঁকার জন্য):**
![Sandwich Integration](images/media_1789135599166.png)

### 6. Regression Testing and Smoke Testing. (Slide 17-20) 🌟

#### A. Regression Testing
**English:**
*   **Definition:** It means running old test cases again.
*   **Why do we need it?** When developers add new code or fix a bug, it might accidentally break old working code.
*   **Purpose:** It ensures new changes do not create new errors in the software.
*   **How to do it:** We can run old tests manually, or use automated testing tools to save time.

#### B. Smoke Testing
**English:**
*   **Definition:** It is a daily test for the whole software system.
*   **Process:** Every day, developers combine all new code. Then they run a quick test.
*   **Purpose:** To see if the software crashes immediately. We call these "show-stopper" errors.
*   **Benefits:** 
    1. It finds major errors early.
    2. It saves time for developers.
    3. Managers can easily track daily progress.

**💡 Diagram (খাতায় আঁকার জন্য):**
![Smoke Testing Diagram](images/media_1789135738919.png)

**বাংলা সামারি:** নতুন কোড অ্যাড করার পর পুরোনো কোড নষ্ট হলো কি না, সেটা চেক করাই হলো **Regression Testing**। আর প্রতিদিন পুরো সিস্টেম জোড়া লাগানোর পর অ্যাপটা ক্র্যাশ করছে কি না, সেটা চেক করাই হলো **Smoke Testing**।
