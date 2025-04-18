**Entry Criteria vs Exit Criteria** are two key components in software testing that define the conditions under which a phase or activity can begin (entry) and end (exit).

### **Entry Criteria:**

- **Definition:** Entry criteria are the conditions that must be met before a particular testing phase or activity can begin.
- **Purpose:** They ensure that the testing phase starts only when the necessary preparations and prerequisites are in place.
- **Examples:**
    
    - Test plan is approved.
    - Test environment is set up.
    - Test cases are designed and reviewed.
    - Test data is available.
    - The build or version of the software is stable and ready for testing.

### **Exit Criteria:**

- **Definition:** Exit criteria are the conditions that must be met for a testing phase or activity to be considered complete and for the next phase to begin.
- **Purpose:** They define when the testing can stop, ensuring that the necessary testing has been completed and all required objectives have been met.
- **Examples:**
    
    - All planned test cases have been executed.
    - Critical defects have been fixed or deferred.
    - Test results have been reviewed and documented.
    - Test coverage is complete.
    - No high-priority defects remain unresolved


### **Document Requirements for Entry Criteria:**

1. **Test Plan:**
    
    - A detailed document outlining the scope, objectives, test cases, testing methods, resources, and schedule for the testing phase.
        
    - Confirms the availability of all necessary test environments and data.
        
2. **Test Environment Setup Documentation:**
    
    - A checklist or report that confirms the test environment (software, hardware, and network setup) is ready and available for testing.
        
    - Includes details about the version of the application, configurations, and any dependencies.
        
3. **Test Cases and Test Scripts:**
    
    - Documents containing the test cases to be executed.
        
    - For manual testing, the test cases should be written, reviewed, and approved.
        
    - For automation, the scripts should be developed and ready for execution.
        
4. **Test Data:**
    
    - A document listing the data sets required for testing (e.g., specific inputs, datasets for functional, boundary, and performance testing).
        
    - Includes test data validation to ensure it's accurate and complete.
        
5. **Software Build / Version Notes:**
    
    - A record detailing the version of the application or software build that will be tested, along with its release notes.
        
    - Ensures that testing is performed on the correct version.
        
6. **Risk Assessment / Mitigation Plan:**
    
    - A document identifying potential risks in the testing phase (e.g., lack of resources, unstable build) and how those risks will be mitigated.
        
7. **Resource Availability:**
    
    - Documentation confirming that required resources (testers, tools, hardware, etc.) are available to begin testing.
        

---

### **Document Requirements for Exit Criteria:**

1. **Test Execution Report:**
    
    - A document that details the results of test executions, including the number of test cases run, passed, failed, blocked, and skipped.
        
    - Should include logs and screenshots (if necessary) to demonstrate test results.
        
2. **Defect Report:**
    
    - A detailed list of defects discovered during testing, including their severity, status (open/closed), and resolution (fixed or deferred).
        
    - May include defect logs, details on retests, and fix validation.
        
3. **Test Coverage Summary:**
    
    - A document that summarizes the test coverage (e.g., functionality, security, performance) and verifies that the planned tests have been completed.
        
    - May include traceability matrices linking requirements to test cases.
        
4. **Test Case Execution Status:**
    
    - A list showing the status of all executed test cases (pass/fail), and whether they met the expected outcomes.
        
    - Includes any deviations from the original test case plan.
        
5. **Test Completion Report:**
    
    - A final report summarizing the testing process, highlighting achievements, areas of concern, and whether exit criteria were met.
        
    - Includes a summary of all executed tests and the overall quality of the application.
        
6. **Risk Mitigation and Residual Risk Report:**
    
    - A document identifying any unresolved issues or risks that were encountered during testing.
        
    - Details the plan for addressing those issues (e.g., fixing defects in later releases).
        
7. **Approval of Deliverables:**
    
    - Sign-off documents from key stakeholders (e.g., product owners, project managers) indicating that all exit criteria are met and the testing phase is complete.
        

---

### **Summary of Documentation:**

- **Entry Criteria** documentation typically focuses on test readiness (plan, environment, test data, test cases, and risk assessment).
    
- **Exit Criteria** documentation focuses on tracking the completion of testing (execution results, defect status, test coverage, and final reports).