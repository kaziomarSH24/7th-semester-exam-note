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
1.  **Brute Force:** Blindly using print statements to find bugs. (Not efficient).
2.  **Backtracking:** Going backward from the error line to find the root cause. (Good for small programs).
3.  **Cause Elimination:** Using logic to eliminate wrong causes until you find the real cause. (Best method).
**বাংলা সামারি:** Brute Force হলো চোখ বন্ধ করে প্রিন্ট স্টেটমেন্ট দিয়ে ভুল খোঁজা। Backtracking হলো যেখান থেকে এরর এসেছে, সেখান থেকে উল্টো দিকে চেক করা। আর Cause elimination হলো লজিক খাটিয়ে আসল ভুলের কাছে পৌঁছানো।

---

## 📌 Lecture 6: Test Strategies for Conventional Software
*(Suggested Slides: 3, 5, 7-18)*

### 1. What is Unit Testing and its Targets? (Slide 3, 5)
**English:** Unit testing tests a single module. It checks the internal logic of that module.

**💡 Diagram (খাতায় আঁকার জন্য):**
![Unit Testing Diagram](images/media_1789134843024.png)

*   **Targets for Unit Test (কী কী চেক করা হয়):**
    1. **Interface:** Checks data flow in and out.
    2. **Local data:** Checks temporary data.
    3. **Boundary:** Checks the limit values.
    4. **Paths:** Runs all code lines at least once.
    5. **Error handling:** Checks error responses.

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
*   Starts from the main top module and goes down.
*   Lower modules are replaced with **Stubs**.
*   **Diagram:**
![Top-Down Integration](images/media_1789135556717.png)

#### B. Bottom-Up Integration
*   Starts from the lowest modules and goes up.
*   Top modules are replaced with **Drivers**.
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
*   **Definition:** Running old tests again. 
*   **Purpose:** It ensures new code does not break old code.

#### B. Smoke Testing
**English:**
*   **Definition:** A daily test for the whole build.
*   **Purpose:** It checks if the software crashes immediately (show-stopper errors).
*   **Benefits:** Finds major errors early and tracks daily progress.

**💡 Diagram (খাতায় আঁকার জন্য):**
![Smoke Testing Diagram](images/media_1789135738919.png)

**বাংলা সামারি:** নতুন কোড অ্যাড করার পর পুরোনো কোড নষ্ট হলো কি না, সেটা চেক করাই হলো **Regression Testing**। আর প্রতিদিন পুরো সিস্টেম জোড়া লাগানোর পর অ্যাপটা ক্র্যাশ করছে কি না, সেটা চেক করাই হলো **Smoke Testing**।
