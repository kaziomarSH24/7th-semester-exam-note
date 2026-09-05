# SQA Lecture 4: Final Exam Guide 🎯

এই লেকচারটি টেস্টিংয়ের কিছু গুরুত্বপূর্ণ প্রকারভেদ (Black Box, White Box, Performance) নিয়ে একদম বিস্তারিত। 

---

## 1. The 3 Main "Box" Testing (খুবই ইম্পর্টেন্ট 🌟)

### **A. Black Box Testing**
**English (Exam Answer):**
Testing software functionality without looking at internal code. The tester gives inputs, observes outputs, and verifies if it matches requirements.
*   **Think:** "I don't care how it works inside — I only care if it works correctly."
*   **Example:** Testing an ATM machine (insert card $\rightarrow$ pin $\rightarrow$ withdraw money). You don't know the internal ATM code.

**বাংলা সামারি:** 
ভেতরের কোড না দেখেই শুধু ইউজার হিসেবে ইনপুট দিয়ে আউটপুট চেক করা। (যেমন: এটিএম বুথে টাকা তোলা)।

### **B. White Box Testing**
**English (Exam Answer):**
Testing internal code, logic, and structure of a program. The tester knows how the system works inside and designs tests to cover code paths and conditions.
*   **Think:** "I will test the code from inside."
*   **Example:** A developer tests the internal `if/else` logic of a login module.

> [!WARNING]
> **💡 Exam Tip:** White Box Testing এর ৪টা টেকনিকের নাম পরীক্ষায় আসতে পারে: 
> 1. Statement Coverage (সব লাইন রান করা)
> 2. Branch/Decision Coverage (সব if/else চেক করা)
> 3. Path Coverage (সব রাস্তা চেক করা)
> 4. Loop Testing (লুপ চেক করা)

**বাংলা সামারি:** 
ভেতরের কোড (If/Else, Loop) খুলে লাইন-বাই-লাইন চেক করা। 

### **C. Gray Box Testing**
**English (Exam Answer):**
A combination of Black Box and White Box testing. The tester has partial knowledge of the internal system (like DB schema or APIs) but tests from a user's point of view.
*   **Think:** "I know a little about inside, but I test like a user."
*   **Example:** Transferring money via UI (Black box) and then checking the Database to see if the balance updated (White box).

**বাংলা সামারি:** 
ভেতরের একটু-আধটু খবর (যেমন ডাটাবেস) জানা থাকে, কিন্তু টেস্ট করা হয় বাইরের ইউজার ইন্টারফেস থেকে। 

---

## 2. Unit vs Integration Testing

**1. Unit Testing:** 
Testing individual units or components (like a single function or class) independently.
*   **Example:** Testing only the `isValidPassword()` function. 

**2. Integration Testing:** 
Combining multiple modules and testing them as a group to verify their interaction.
*   **Example:** Testing if `Login` $\rightarrow$ `Cart` $\rightarrow$ `Payment` works correctly together. 

---

## 3. Types of Performance Testing (🌟 Very Important)

Performance Testing হলো সফটওয়্যার কতটা স্পিডে এবং কতটা লোড বা প্রেশার নিতে পারে তা চেক করা। এর ৭টি প্রকারভেদ আছে।

**💡 Mnemonic (মনে রাখার ট্রিক): "LESS SVS"** (লেস এসভিএস)

**English (Exam Answer):**
1. **L - Load Testing:** Checks how the system works under normal expected users. *(স্বাভাবিক ইউজার আসলে কেমন চলে, যেমন ১০০০ জন একসাথে শপিং করলে)*
2. **E - Endurance Testing:** Checks if the system can run for a long time without failure. *(টানা অনেক দিন বা অনেক ঘণ্টা চালালে ক্র্যাশ করে কি না)*
3. **S - Stress Testing:** Checks what happens when the system is pushed beyond its limit. *(লিমিটের চেয়ে বেশি ইউজার, যেমন ৫০,০০০ জন একসাথে ঢুকলে কী হয়)*
4. **S - Spike Testing:** Checks how the system reacts to a sudden increase in users. *(হঠাৎ করে ইউজার বেড়ে গেলে, যেমন ফ্ল্যাশ সেলের সময়)*
5. **S - Soak Testing:** Checks performance under continuous load for a long time to find memory leaks. *(টানা ২৪-৪৮ ঘণ্টা ওয়েবসাইট চালিয়ে দেখা স্লো হয়ে যায় কি না)*
6. **V - Volume Testing:** Checks system performance with a large amount of data. *(ডাটাবেসে মিলিয়ন মিলিয়ন ডাটা থাকলে কেমন রেসপন্স করে)*
7. **S - Scalability Testing:** Checks if the system can grow with more users. *(১০০০ থেকে ইউজার ১০,০০০ এ বাড়ালে হ্যান্ডেল করতে পারে কি না)*

**বাংলা সামারি:** 
*   **Load:** নরমাল লোডে চেক করা।
*   **Stress:** লিমিট পার করে প্রেশার দেওয়া।
*   **Spike:** হঠাৎ ইউজার বাড়িয়ে দেওয়া।
*   **Soak / Endurance:** অনেকক্ষণ টানা চালিয়ে দেখা।
*   **Volume:** বিশাল ডাটা দিয়ে চেক করা। 
*   **Scalability:** ইউজার বাড়লে সিস্টেম নিজেকে বড় করতে পারে কি না।
