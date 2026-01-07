
# **Performance Testing Project: Tutorian Web Application**

This repository contains detailed **performance testing artifacts** for the **Tutorian web application**, demonstrating end-to-end performance evaluation using **Apache JMeter**. The project includes well-structured **test plans, performance test cases, bug reports, and execution summary reports**, covering real-world performance statuses such as **Pass, Failed, and Warning** under different load conditions.

---

## **Table of Contents**

* Project Overview
* Features Tested
* Tools & Technologies
* Folder Structure
* Documentation
* Reports
* How to Use
* Contributing
* License

---

## **Project Overview**

This project focuses on **performance testing of key public pages** of the Tutorian platform, including Home, Courses, Blog, Exams, Community, and Policy pages. The goal is to evaluate **response time, stability, and behavior under load** by simulating real user navigation using **JMeter Recording Controller**.

The project also tracks **performance defects** identified during test execution and classifies them by severity and priority to help improve application reliability and user experience.

---

## **Features Tested**

* Home Page response time under normal load
* Course listing page performance
* Free Classes page stability
* Blog and Community page response consistency
* Exams page load performance
* Contact page accessibility
* Privacy Policy, Terms & Conditions, and Refund Policy page performance
* Sequential and recorded user flow testing
* Warning and failure detection based on response thresholds

---

## **Tools & Technologies**

* **Apache JMeter** – Performance and load testing
* **HTTP/HTTPS Protocol** – Request handling
* **Recording Controller** – Real user navigation simulation
* **GitHub** – Version control and documentation

---

## **Folder Structure**

```
Tutorian-JMeter-Performance-with-Recording-Controller/
│
├── Test_Plan/
│   └── Performance_Test_Plan.md
│
├── Test_Cases/
│   └── Performance_Test_Cases.md
│
├── Bug_Reports/
│   └── Performance_Bug_Report.md
│
├── Reports/
│   └── Summary_Report.md
│
├── JMeter_Scripts/
│   └── Tutorian_Performance_Test.jmx
│
└── README.md
```

---

## **Documentation**

* **Test Plan:** Defines scope, objectives, approach, and environment
* **Test Cases:** Detailed performance test cases with expected and actual results
* **Bug Reports:** Logged performance issues with severity and priority
* **Summary Report:** Overall test execution and defect summary

---

## **Reports**

* Test Execution Summary
* Defects Summary
* JMeter Listener Results
* Performance Analysis Observations
