# SQA Lecture 1: Final Exam Guide 🎯

এই নোটে পরীক্ষার খাতায় ঠিক যেভাবে **English**-এ লিখতে হবে সেভাবে পয়েন্টগুলো সাজানো হয়েছে এবং সহজে মুখস্থ করার জন্য নিচে **বাংলা অনুবাদ ও শর্টকাট (Mnemonic)** দেওয়া হয়েছে।

---

## 1. What is Software Quality Assurance (SQA)?

**English (Exam Answer):**
Software Quality Assurance (SQA) is a set of activities that ensure processes, procedures, and standards are suitable for the project and implemented correctly. It is an "Umbrella activity" that is applied throughout the software development process.

**বাংলায় বুঝে নিন:**
SQA হলো এমন কিছু কাজের সমষ্টি যা নিশ্চিত করে যে সফটওয়্যার বানানোর রুলস এবং প্রসেসগুলো ঠিকঠাক মানা হচ্ছে। এটি কোনো একটি নির্দিষ্ট ধাপ নয়, বরং পুরো সফটওয়্যার বানানোর সময় ছাতার মতো (Umbrella activity) কাজ করে।

---

## 2. What is Software Quality?

**English (Exam Answer):**
Quality is the ability of a software to meet stated and implied requirements and satisfy users.
Software quality means the degree to which software:
1. Meets functional and non-functional requirements.
2. Is free from defects.
3. Satisfies user expectations.

> [!TIP]
> **💡 Exam Tip (Diagram):** Draw this flowchart if asked about Software Quality:
> **Quality** $\rightarrow$ divides into $\rightarrow$ **Quality of Design** and **Quality of Conformance**

**বাংলায় বুঝে নিন:**
সফটওয়্যার কোয়ালিটি মানে হলো সফটওয়্যারটি কাস্টমারের রিকোয়ারমেন্ট পূরণ করছে, এতে কোনো বাগ (bug/defect) নেই এবং ইউজার এটি ব্যবহার করে সন্তুষ্ট।

---

## 3. Elements of SQA

**💡 Mnemonic (মনে রাখার ট্রিক): "STRESS ER"**

**English (Exam Answer):**
1. **S - Standards:** Ensure IEEE, ISO, or other adopted standards are followed.
2. **T - Testing:** Ensure testing is properly planned and efficiently conducted to find errors.
3. **R - Reviews and Audits:** Perform technical reviews (by engineers) to uncover errors and audits (by SQA personnel) to ensure guidelines are followed.
4. **E - Education:** Sponsor educational programs to improve software engineering practices.
5. **S - Security Management:** Ensure appropriate processes and technology are used for software security.
6. **S - Safety:** Assess the impact of software failure and initiate steps to reduce risk.
7. **E - Error/Defect Analysis:** Collect and analyze error data to understand how they are introduced and eliminate them.
8. **R - Risk Management:** Ensure risk management activities are conducted and contingency plans are established.

**বাংলায় বুঝে নিন:**
সফটওয়্যার কোম্পানির কোয়ালিটি ঠিক রাখতে এই ৮টি কাজ করতে হয়: স্ট্যান্ডার্ড মানা (Standards), টেস্টিং করা (Testing), কোড রিভিউ ও অডিট করা (Reviews), ডেভেলপারদের ট্রেইনিং দেওয়া (Education), সিকিউরিটি ও হ্যাকিং থেকে বাঁচানো (Security), বড় দুর্ঘটনা থেকে সেফ রাখা (Safety), কেন ভুল হলো তা এনালাইসিস করা (Error analysis), এবং বিপদের জন্য প্ল্যান-বি রেডি রাখা (Risk management)।

---

## 4. Garvin's 8 Dimensions of Quality (Very Important 🌟)

**💡 Mnemonic (মনে রাখার ট্রিক): "PF CARS DP"**

> [!TIP]
> **💡 Exam Tip (Diagram):** Draw a staircase diagram with these 8 points from bottom to top!

**English (Exam Answer):**
1. **P - Performance:** Primary operating characteristics (e.g., Response time of an online banking system).
2. **F - Feature:** Additional functionalities beyond basic requirements (e.g., Auto save, dark mode).
3. **C - Conformance:** Degree to which software meets standards and specifications (e.g., Following ISO standards).
4. **A - Aesthetics:** User interface look and feel, visual appeal (e.g., Clean UI design, readable fonts).
5. **R - Reliability:** Probability of failure-free operation over time (e.g., Software runs without crashing).
6. **S - Serviceability:** Ease of maintenance, repair, and speed of fixing bugs (e.g., Fast bug fixes through patches).
7. **D - Durability:** Ability of software to remain useful over time (e.g., Software remains usable after OS updates).
8. **P - Perception:** User's overall impression, influenced by brand reputation (e.g., Trust in Google or Microsoft software).

**বাংলায় বুঝে নিন:**
কোনো সফটওয়্যার কতটা ভালো তা মাপার ৮টি উপায়: স্পিড কেমন (Performance), এক্সট্রা কী সুবিধা আছে (Feature), ইন্টারন্যাশনাল রুলস মানে কি না (Conformance), দেখতে কতটা সুন্দর (Aesthetics), একটানা ক্র্যাশ না করে চলে কি না (Reliability), নষ্ট হলে কত দ্রুত ফিক্স করা যায় (Serviceability), কত বছর টিকে থাকে (Durability), এবং ইউজারের চোখে কোম্পানির ইমেজ কেমন (Perception)।

---

## 5. Key Factors of SQA

**💡 Mnemonic (মনে রাখার ট্রিক): "CPU R ME"** (সিপিইউ আর মি / CPU and Me)

**English (Exam Answer):**
1. **C - Correctness:** Software gives correct results and works according to its requirements.
2. **P - Portability:** Software can run on different systems or platforms with little or no change.
3. **U - Usability:** How easy and user-friendly the software is to use and understand.
4. **R - Reusability:** Software components can be used again in other programs, saving time.
5. **M - Maintainability:** How easily the software can be updated, fixed, or improved.
6. **E - Error Control:** Software can detect and handle errors properly without crashing.

**বাংলায় বুঝে নিন:**
কোয়ালিটির মূল বিষয়গুলো হলো: পিসি থেকে মোবাইলে সহজে চলা (Portability), সহজে ব্যবহার করা (Usability), আগের কোড নতুন প্রজেক্টে ব্যবহার করা (Reusability), পারফেক্ট রেজাল্ট দেওয়া (Correctness), সহজে আপডেট করা (Maintainability), এবং এরর হলে ক্র্যাশ না করে ম্যানেজ করা (Error control)।

---

## 6. How to Achieve SQA? (কীভাবে কোয়ালিটি অর্জন করব?)

**English (Exam Answer):**
1. **Clear and Correct Requirements:** Gather unambiguous requirements and maintain proper SRS.
2. **Well-Defined Development Process:** Follow standard models like Agile or Waterfall.
3. **Apply Quality Assurance (QA):** Process-oriented approach focusing on defect prevention.
4. **Apply Quality Control (QC):** Product-oriented approach focusing on defect detection.
5. **Follow Standards and Models:** Follow ISO 9001 and CMMI process maturity models.
6. **Perform Continuous Testing:** Conduct Unit, Integration, System, and Acceptance testing.
7. **Conduct Reviews and Inspections:** Perform requirement, design, and code reviews.
8. **Skilled Team and Quality Culture:** Employ trained developers and maintain continuous learning.

**বাংলায় বুঝে নিন:**
কোয়ালিটি ভালো করতে হলে: কাস্টমারের রিকোয়ারমেন্ট ক্লিয়ারলি বুঝতে হবে, অ্যাজাইল বা ওয়াটারফলের মতো প্রসেস মানতে হবে, QA ও QC অ্যাপ্লাই করতে হবে, ISO স্ট্যান্ডার্ড ফলো করতে হবে, বারবার টেস্টিং ও কোড রিভিউ করতে হবে এবং কোম্পানিতে একটি এক্সপার্ট টিম থাকতে হবে।
