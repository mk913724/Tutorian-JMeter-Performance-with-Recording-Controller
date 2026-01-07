
# 📋 Tutorian – Performance Test Cases (Based on Actual JMeter Results)

> **Test Type:** Performance Testing
> 
> **Tool:** Apache JMeter
> 
> **Request Type:** HTTP Request (Web URL, not API)
> 
> **Controller:** Recording Controller
> 
> **Thread Group:** Thread Group 1

---

##  Performance Test Case Table

| TC ID | Feature            | Scenario                                   | Request Type | Method | Load Condition        | Expected Result                    | Actual Result (From JMeter)                   | Status     |
| ----- | ------------------ | ------------------------------------------ | ------------ | ------ | --------------------- | ---------------------------------- | --------------------------------------------- | ---------- |
| TC-01 | Home Page          | Measure home page response time under load | HTTP Request | GET    | 1 user, recorded flow | Response time ≤ 3 sec, no warnings | Multiple samples > 3 sec, high bytes received | Warning |
| TC-02 | All Courses        | Load test course listing page              | HTTP Request | GET    | Sequential requests   | Stable response without delay      | Response time spiked (~5 sec)                 |  Warning |
| TC-03 | Free Classes       | Validate free classes page performance     | HTTP Request | GET    | Recorded navigation   | Page loads normally                | Page loaded within acceptable time            |  Pass     |
| TC-04 | Blog               | Test blog page under traffic               | HTTP Request | GET    | Recorded request      | No response delay                  | Some requests crossed threshold               |  Warning |
| TC-05 | Exams              | Evaluate exams page response               | HTTP Request | GET    | Recorded flow         | Response under threshold           | Page loaded successfully                      |  Pass     |
| TC-06 | Community          | Verify community page stability            | HTTP Request | GET    | Recorded flow         | No performance degradation         | Minor response fluctuation                    |  Warning |
| TC-07 | Contact            | Test contact page load time                | HTTP Request | GET    | Recorded navigation   | Page loads smoothly                | Page loaded successfully                      |  Pass     |
| TC-08 | Privacy Policy     | Measure privacy policy page performance    | HTTP Request | GET    | Single user           | Response ≤ threshold               | Loaded successfully                           |  Pass     |
| TC-09 | Terms & Conditions | Check T&C page response consistency        | HTTP Request | GET    | Sequential requests   | Stable response                    | Warning observed in multiple samples          |  Warning |
| TC-10 | Refund Policy      | Validate refund policy page under load     | HTTP Request | GET    | Sequential requests   | No delay or warning                | High response time & warnings observed        |  Fail     |

---

##  Evidence From JMeter Execution

| Observation             | Evidence                         |
| ----------------------- | -------------------------------- |
| Warning status detected | Multiple samplers show `Warning` |
| High response time      | Samples above 3000–6000 ms       |
| Large response size     | Bytes received unusually high    |
| No API usage            | Pure web HTTP URL requests       |
| No functional failure   | Pages responded but slowly       |

## Bug ↔ Test Case Mapping

| Test Case ID | Bug ID   |
| ------------ | -------- |
| TC-01        | PERF-001 |
| TC-09        | FUNC-002 |
| TC-10        | PERF-003 |
