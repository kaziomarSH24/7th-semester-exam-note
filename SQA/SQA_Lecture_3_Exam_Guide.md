# SQA Lecture 3: Final Exam Guide 🎯

এই লেকচারটি মূলত **সফটওয়্যার টেস্টিং (Testing)** এবং **Verification & Validation** নিয়ে। 

---

## 1. Steps for Software Testing Strategies

**English (Exam Answer):**
1. **Define Testing Objectives:** Clearly state what testing aims to achieve (e.g., Effectiveness, Failure detection, Cost of defects).
2. **Understand Users:** Identify user categories, create profiles, and use *use cases* to see how users interact.
3. **Develop a Test Plan:** Focus on Rapid-Cycle Testing to quickly identify improvements and help testers work efficiently.
4. **Build Robust Software:** Software should detect its own errors and support automated/regression testing.

**বাংলা সামারি:** 
সফটওয়্যার টেস্টিংয়ের ৪টা ধাপ: প্রথমে টেস্টিংয়ের **উদ্দেশ্য (Objectives)** ঠিক করতে হবে (কেন টেস্ট করছি)। এরপর **ইউজারদের (Users)** বুঝতে হবে তারা কীভাবে অ্যাপ চালাবে। তারপর একটা দ্রুত **টেস্ট প্ল্যান (Plan)** বানাতে হবে। আর সবশেষে এমন **মজবুত সফটওয়্যার (Robust)** বানাতে হবে যেন সে নিজের ভুল নিজেই ধরতে পারে।

---

## 2. Common Testing Strategies (টেস্টিংয়ের প্রকারভেদ)
*(এগুলো শুধু রিডিং পড়লেই মনে থাকবে, কারণ এগুলো আমরা সবসময়ই শুনি)*

**English & বাংলা সামারি:**
1. **Black Box (অদৃশ্য/লুকায়িত) Testing:** Tests functionality without looking at internal code. *(ভিতরের কোড না দেখেই শুধু ইনপুট-আউটপুট চেক করা)*
2. **White Box (দৃশ্যমান/স্বচ্ছ) Testing:** Tests internal code structure and logic. *(ভিতরের কোড লাইন-বাই-লাইন চেক করা)*
3. **Unit (একক/ক্ষুদ্রতম অংশ) Testing:** Tests individual components. *(সফটওয়্যারের ছোট ছোট পার্ট বা বাটন আলাদা করে টেস্ট করা)*
4. **Integration (একত্রীকরণ/জোড়া লাগানো) Testing:** Tests how different components work together. *(পার্টগুলো জোড়া লাগানোর পর একসাথে কাজ করে কি না দেখা)*
5. **Functional (কার্যকারিতা) Testing:** Checks if functional requirements are met. *(সফটওয়্যারটি কাস্টমারের চাওয়া অনুযায়ী কাজ করছে কি না)*
6. **System (সম্পূর্ণ সিস্টেম) Testing:** Tests the complete system against specified requirements. *(পুরো রেডি সফটওয়্যারটাকে একসাথে টেস্ট করা)*
7. **Acceptance (গ্রহণযোগ্যতা) Testing:** Ensures software meets customer expectations. *(কাস্টমার বা ইউজার নিজে চালিয়ে দেখে পছন্দ হলো কি না)*
8. **Regression (আপডেটের প্রভাব/পশ্চাদপসরণ) Testing:** Tests after changes to ensure no new defects are introduced. *(আপডেট দেওয়ার পর পুরনো ফিচারে কোনো সমস্যা হলো কি না চেক করা)*
9. **Performance (কর্মক্ষমতা/গতি) Testing:** Measures speed, scalability, and stability. *(সফটওয়্যার কতটা স্পিডে কাজ করে বা একসাথে কতজন ইউজার নিতে পারে)*
10. **Security (নিরাপত্তা) Testing:** Identifies vulnerabilities. *(সফটওয়্যার হ্যাক হওয়ার চান্স আছে কি না চেক করা)*

---

## 3. Verification & Validation (V&V) - Very Important 🌟

> [!WARNING]
> **💡 Exam Tip:** Verification এবং Validation এর পার্থক্য পরীক্ষায় প্রায়ই আসে। এই দুইটা ডায়লগ অবশ্যই নীল/কালো কলম দিয়ে হাইলাইট করে লিখবেন:
> Verification $\rightarrow$ "Are we building the product right?"
> Validation $\rightarrow$ "Are we building the right product?"

### **A. Verification**
**English (Exam Answer):**
The process of checking whether the software is being built correctly according to specifications and design documents.
*   **Focus:** Process
*   **Asks:** “Are we building the product right?”
*   **Example:** Checking if the login module follows the design document and coding standards.

**বাংলা সামারি:** 
সফটওয়্যারটা ডিজাইন বা প্ল্যান অনুযায়ী ঠিকঠাক কোডিং করা হচ্ছে কি না, সেটা চেক করাই হলো ভেরিফিকেশন। (ধরুন, আপনি বিরিয়ানির রেসিপি দেখে ধাপে ধাপে ঠিকমতো রাঁধছেন কি না, সেটা চেক করা)।

### **B. Validation**
**English (Exam Answer):**
The process of checking whether the software meets the user’s needs and performs its intended functions in the real world.
*   **Focus:** Product
*   **Asks:** “Are we building the right product?”
*   **Example:** After the app is built, ensuring that customers can successfully transfer money.

**বাংলা সামারি:** 
ফাইনাল সফটওয়্যারটা ইউজারের আসল কাজে লাগছে কি না, সেটা চেক করাই হলো ভ্যালিডেশন। (ধরুন, বিরিয়ানি রান্না শেষে খেয়ে দেখা যে স্বাদটা আসলেই বিরিয়ানির মতো হয়েছে কি না)।

---

## 4. Criteria for Completing Testing (টেস্টিং কখন শেষ হবে?)

**💡 Mnemonic (মনে রাখার ট্রিক): "ABC GAPS"** (এবিসি গ্যাপস)

**English (Exam Answer):**
1. **A - All Test Cases Executed:** Every planned test case has been run.
2. **B - Bugs (Defects) Fixed and Verified:** All critical and major defects have been resolved.
3. **C - Coverage Achieved:** Required functional and code coverage goals are satisfied.
4. **G - Goals Met:** Performance, security, and reliability standards are met.
5. **A - Acceptance Criteria Met:** Software meets the requirements and user expectations.
6. **P - Priority Defects Zero:** No high-priority defects remaining (only minor bugs may remain).
7. **S - Stakeholder Approval:** Testing completion is formally approved by the QA team.

**বাংলা সামারি:** 
টেস্টিং শেষ করার জন্য: সব টেস্ট রান করতে হবে (**A**ll tests), বড় সব বাগ ফিক্স করতে হবে (**B**ugs), ফুল কোড কভার করতে হবে (**C**overage), সিকিউরিটি ও স্পিডের গোল পূরণ হতে হবে (**G**oals), ইউজারের সব রিকোয়ারমেন্ট পূরণ হতে হবে (**A**cceptance), কোনো বড় ডেনজারাস বাগ থাকা যাবে না (**P**riority), এবং সবার শেষে বসের সাইন বা অ্যাপ্রুভাল লাগবে।
