# Software Quality Assurance (SQA) - Full Course Notes
**Course Teacher:** Md. Didar Ahmed

---

## LECTURE 1: Introduction to SQA

### Software Quality Assurance (SQA)
Software Quality Assurance (SQA) is simply a way to assure quality in the software. It is the set of activities that ensure processes, procedures as well as standards are suitable for the project and implemented correctly. It is a process that works parallel to Software Development. Software Quality Assurance is a kind of Umbrella activity that is applied throughout the software process.

### Quality
Quality is the ability of a product or service to meet stated and implied requirements and satisfy users.
In software context (SQA) Software quality is the degree to which software:
* Meets functional and non-functional requirements
* Conforms to standards
* Is free from defects
* Satisfies user expectations

### Elements of SQA
* **Standards:** The IEEE, ISO, and other standards organizations have produced a broad array of software engineering standards and related documents. The job of SQA is to ensure that standards that have been adopted are followed.
* **Reviews and audits:** Technical reviews are a quality control activity performed by software engineers. Their intent is to uncover errors. Audits are a type of review performed by SQA personnel.
* **Testing:** Software Testing is a quality control function that has one primary goal to find errors.
* **Error/defect collection and analysis:** SQA collects and analyses error and defect data to better understand how errors are introduced.
* **Education:** A key contributor to improvement is education of software engineers, their managers, and other stakeholders.
* **Security management:** SQA ensures that appropriate process and technology are used to achieve software security.
* **Safety:** SQA may be responsible for assessing the impact of software failure and for initiating those steps required to reduce risk.
* **Risk management:** The SQA organization ensures that risk management activities are properly conducted and that risk-related contingency plans have been established.

### Dimension of Software Quality - Garvin's Dimensions Of Quality
David A. Garvin proposed eight dimensions of quality, which are widely used to evaluate product and software quality.
1. **Performance:** Primary operating characteristics of the software. How well the software performs its intended functions.
2. **Feature:** Additional functionalities beyond basic requirements. Enhancements that attract users.
3. **Reliability:** Probability of failure-free operation over time. Consistency and stability.
4. **Conformance:** Degree to which software meets standards and specifications. Compliance with requirements.
5. **Durability:** Ability of software to remain useful over time. Resistance to obsolescence.
6. **Serviceability:** Ease of maintenance, repair, and updates. Speed of fixing bugs.
7. **Aesthetics:** User interface look and feel. Visual appeal and user experience.
8. **Perception:** User’s overall impression of quality. Influenced by brand reputation and experience.

### How to Achieve SQA?
* **Clear and Correct Requirements:** Gather complete and unambiguous requirements, Validate requirements with stakeholders, Maintain a proper SRS.
* **Use a Well-Defined Development Process:** Follow standard models (Waterfall, Agile, Spiral), Define roles, responsibilities, and workflows, Ensure process discipline.
* **Apply Quality Assurance (QA):** Process-oriented approach, Focus on defect prevention.
* **Apply Quality Control (QC):** Product-oriented approach, Focus on defect detection.
* **Perform Continuous Testing:** Unit testing, Integration testing, System testing, Acceptance testing.
* **Conduct Reviews and Inspections:** Requirement reviews, Design reviews, Code reviews.
* **Follow Standards and Models:** ISO 9001, ISO/IEC 25010, CMMI.
* **Skilled Team and Quality Culture:** Trained developers and testers, Management commitment to quality, Continuous learning.

### Key Factors of SQA
* **Software Portability:** Portability means the software can run on different systems or platforms with little or no change.
* **Software Usability:** Usability refers to how easy and user-friendly the software is to use and understand.
* **Software Reusability:** Reusability means software components can be used again in other programs or projects, saving time and effort.
* **Software Correctness:** Correctness means the software gives correct results and works according to its requirements.
* **Software Maintainability:** Maintainability refers to how easily the software can be updated, fixed, or improved.
* **Software Error Control:** Error control means the software can detect and handle errors properly without crashing.

---

## LECTURE 3: Software Testing Strategies & V&V

### Software Testing Strategies
* **Specify Requirements Clearly:** Objectives of testing such as effectiveness (achieve the target), failure detection (inability to fulfill requirements), and cost of defects.
* **Define Testing Objectives:** Effectiveness, Failure detection, Cost of defects.
* **Understand Users:** Identify user categories and create profiles. Use use cases to see how users interact with the software.
* **Develop a Test Plan:** Focus on Rapid-Cycle Testing to quickly identify improvements.
* **Build Robust Software:** Software should be able to detect its own errors. Support automated and regression testing to check for side effects after changes.

### Common Testing Strategies
* **Black Box Testing:** Tests software functionality without looking at internal code.
* **White Box Testing:** Tests internal code structure and logic.
* **Unit Testing:** Tests individual components or units to ensure they work correctly.
* **Integration Testing:** Tests how different components work together as a system.
* **Functional Testing:** Checks if functional requirements are met.
* **System Testing:** Tests the complete system against specified requirements.
* **Acceptance Testing:** Ensures software meets customer or end-user expectations.
* **Regression Testing:** Tests after changes to ensure no new defects are introduced.
* **Performance Testing:** Measures speed, scalability, and stability of the software.
* **Security Testing:** Identifies vulnerabilities and checks security requirements.

### Verification & Validation
**Verification:**
The process of checking whether the software is being built correctly according to specifications and design documents.
* **Focus:** Process
* **Asks:** “Are we building the product right?”
* **Example:** A team is developing an online banking app. During verification, they check if the login module follows the design document and meets coding standards.

**Validation:**
The process of checking whether the software meets the user’s needs and performs its intended functions in the real world.
* **Focus:** Product
* **Asks:** “Are we building the right product?”
* **Example:** After the online banking app is built, users try it. Validation ensures that customers can successfully transfer money, check balance, and pay bills as intended.

### Criteria for Completing Testing
1. **All Test Cases Executed:** Every planned test case has been run.
2. **Defects Fixed and Verified:** All critical and major defects have been resolved and re-tested.
3. **Acceptance Criteria Met:** Software meets the requirements and user expectations.
4. **No High-Priority Defects Remaining:** Only minor or low-priority defects, if any, remain.
5. **Test Coverage Achieved:** Required functional and code coverage goals are satisfied.
6. **Performance and Security Goals Met:** Software meets performance, security, and reliability standards.
7. **Stakeholder Approval:** Testing completion is formally approved by QA team and project stakeholders.

---

## LECTURE 4: Testing Types

### Black Box Testing
Black Box Testing is a software testing method where the tester checks the functionality of an application without knowing or looking at the internal code. You give inputs (like a user), observe the outputs/behaviour, and verify whether it matches the requirements.
* **Think:** “I don’t care how it works inside — I only care if it works correctly.”
* **Example:** ATM Machine (Insert card $\rightarrow$ enter PIN $\rightarrow$ withdraw money). Login Page (Valid/Invalid credentials).

### White Box Testing
White Box Testing is a testing method where the tester checks the internal code, logic, and structure of a program. Here the tester knows how the system works inside and designs tests to cover code paths, conditions, loops, and statements.
* **Think:** “I will test the code from inside.”
* **Main Techniques:**
  * Statement Coverage: every line runs at least once
  * Branch/Decision Coverage: every true/false decision runs
  * Path Coverage: all possible paths run
  * Loop Testing: tests loops (0 times, 1 time, many times)

### Gray Box Testing
Gray Box Testing is a software testing technique that is a combination of Black Box and White Box testing. The tester has partial knowledge of the internal system (such as database schema, APIs) but tests the software mainly from the user’s point of view.
* **Think:** “I know a little about inside, but I test like a user”

### Unit Testing
Unit Testing is a software testing technique where individual units or components of a program (such as a function, method, or class) are tested independently to verify that they work correctly.
* **Think:** “Test the smallest piece of code first”

### Integration Testing
Integration Testing is a level of software testing where multiple modules are combined and tested as a group to verify their interaction. "It focuses on interfaces and communication between modules".
* **Example:** Online Shopping System (Module 1: Login $\rightarrow$ Module 2: Cart $\rightarrow$ Module 3: Payment).

### Performance Testing
Performance Testing is a type of software testing that evaluates how well an application performs under expected and peak workloads.
**Types of Performance Testing:**
1. **Load Testing:** Checks how the system works under normal expected users.
2. **Stress Testing:** Checks what happens when the system is pushed beyond its limit.
3. **Spike Testing:** Checks how the system reacts to sudden increase in users.
4. **Soak Testing:** Checks system performance under continuous load for a long time.
5. **Endurance Testing:** Checks if the system can run for a long time without failure.
6. **Volume Testing:** Checks system performance with large amount of data.
7. **Scalability Testing:** Checks if the system can grow with more users.

---

## LECTURE 5: Formal Modeling and Verification

### Introduction
Formal modeling and verification methods use specialized techniques to ensure software quality from the start. These methods are different from typical reviews and testing, which only start after the software has been developed.
1. **Cleanroom Software Engineering:** It focuses on avoiding mistakes during the development process. It requires precise, error-free practices from the beginning.
2. **Formal Methods:** Formal methods use mathematics to create and verify software systems.

### Cleanroom Strategy
The cleanroom strategy is a software engineering approach that emphasizes building software correctly from the start. It involves breaking the development process into small parts, called “increments”, which are developed by small independent teams.

### Elements of Cleanroom Process Model
1. **Increment Planning:** Ensures each increment focuses on delivering valuable features.
2. **Requirements Gathering:** Collects and documents specific requirements.
3. **Box Structure Specification:** Helps understand the overall structure and relationships.
4. **Formal Design:** Specifies how each component interacts.
5. **Correctness Verification:** Catches potential issues early in development.
6. **Code Generation and Inspection:** Ensures code accurately reflects the design.
7. **Statistical Testing:** Identifies potential issues like performance bottlenecks.
8. **Certification:** Provides confidence that software increment is reliable and ready.

### Types of Box Structure Specification
1. **Black Box Specification:** Represents the input-output relationship without considering internal details. Notation: f(S*) = R.
2. **State Box Specification:** Helps explain how a software system behaves over time.
3. **Clear Box Specification:** Helps in understanding how the system processes inputs to produce outputs (procedural design).

### Cleanroom Design
Cleanroom design is an approach to software development that emphasizes the Need to build correctness into software as it is being developed.
1. **Design Refinement:** Breaking down high level functional specification into subfunctions.
2. **Design Verification:** Ensuring the refined software design is correct using formal methods and mathematical proofs.

### Cleanroom Testing
* **Statistical Use testing:** Understanding user interactions, assigning probabilities to those interactions, creating test cases based on those probabilities.

### Certification Process
Certification implies that the software components or the entire system have achieved a specific level of reliability.
1. **Create Usage Scenarios:** Describe how users interact with the software.
2. **Specify a usage profile:** Determine probability of each scenario.
3. **Generate test cases:** Create a representative sample of test cases.
4. **Execute tests and Record Failure Data:** Assess its reliability.
5. **Compute and Certify Reliability:** Using Sampling Model, Component Model, and Certification Model.

### Formal Methods & Concepts
Formal methods are a set of mathematical and logical techniques used to specify, design, and verify software systems.
* **Data Invariant:** Ensuring that certain properties hold true at all times.
* **State:** Stored data at any point in time.
* **Operation:** Action that reads or writes data within the system.
* **Invariant:** A condition that doesn't change during an operation.
* **Precondition:** Requirements that must be satisfied in order for an operation to be performed.
* **Postcondition:** Specifies the effects of the operation on the system’s state.

### Formal Specification Languages (FSL)
The main goal of using a formal specification language is to ensure the correctness, reliability and robustness of the system being designed. Often used in safety-critical systems.
Components:
1. **Syntax:** Specific manner in which rules are written down.
2. **Semantics:** Meaning behind the symbols, notations, or words.
3. **Relations:** Describe the rules themselves and how different parts should behave.

**Object Constraint Language (OCL):**
A formal language used to specify constraints on objects in a system (part of UML).
Key Aspects: Invariants, Preconditions and Postconditions, Guard Conditions, Derived Attributes.

**Z Specification Language:**
Uses a well-defined set of symbols based on mathematical concepts (sets, predicates, functions). Breaks down a system into smaller parts called "schemas".
