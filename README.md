# Manual Functional Testing — OpenCart E-Commerce Platform

**A self-driven, end-to-end manual QA project** covering the full software testing lifecycle — from requirement exploration through test design, execution, defect reporting, and closure — performed against the public [OpenCart demo store](https://demo.opencart.com/).

**Prepared by:** Tanvir Ahmed | **Testing Type:** Manual, Black-Box Functional Testing | **Application:** OpenCart (open-source e-commerce platform)

---

## 📊 Project at a Glance

| Metric | Result |
|---|---|
| Modules covered | 31 |
| Test scenarios | 31 |
| Test cases designed | 516 |
| Test cases executed | 516 / 516 (100%) |
| Pass rate | 93.8% (484 pass / 32 fail) |
| Unique defects logged | 24 |
| Defect severity split | 13 Major · 9 Minor · 2 Trivial |

Pass rate held consistent (91–95%) across every priority tier — defects were spread across the application rather than concentrated in one area. Full breakdown in the [Test Summary Report](./09-Test-Summary-Report.docx).

---

## 📁 Project Artifacts

| # | Artifact | Description |
|---|---|---|
| 1 | [Project Introduction](./01-Project-Introduction.docx) | Scope, objective, approach, severity/priority scheme |
| 2 | [Understanding & Exploring the Functionality](./02-Understanding-Functionality.docx) | FRS-style notes from exploring the app before test design |
| 3 | [Test Plan](./03-Test-Plan.docx) | Strategy, schedule, roles, risks, entry/exit criteria |
| 4 | [Test Scenarios](./04-Test-Scenarios.xlsx) | 31 high-level scenarios, each prioritized P0–P4 |
| 5 | [Test Cases](./05-Test-Cases.xlsx) | 516 detailed test cases derived from the scenarios |
| 6 | [Requirement Traceability Matrix (RTM)](./06-RTM.xlsx) | Maps every requirement → scenario → test case(s) |
| 7 | [Test Execution Report](./07-Test-Execution.xlsx) | Pass/Fail status and actual result for all 516 cases |
| 8 | [Bug Report](./08-Bug-Report.xlsx) | 24 defects with repro steps, expected vs. actual, severity & priority |
| 9 | [Test Summary & Closure Report](./09-Test-Summary-Report.docx) | Final metrics, defect summary, exit criteria, sign-off |

Each failed test case is cross-referenced to its defect ID, and every defect traces back to the test case(s) that found it — a closed loop from requirement to defect.

---

## 🐛 Notable Defects Found

| ID | Severity | Summary |
|---|---|---|
| BUG-1 | Major | No outbound email is sent for any workflow (registration, password reset, order confirmation, etc.) — highest-impact defect, explains 9 of the 32 failures |
| BUG-3 | Major | No account lockout / rate-limiting after repeated failed logins — allows unlimited brute-force attempts |
| BUG-4 | Major | Password reset links never expire, even after 24+ hours |
| BUG-8 | Major | Adding the same product twice creates a duplicate cart line instead of merging quantities |
| BUG-20 | Major | Reward Points balance after redemption doesn't always match the amount applied at checkout |

*(Full repro steps, expected vs. actual results, and severity/priority for every defect are in the [Bug Report](./08-Bug-Report.xlsx).)*

---

## 🛠️ Approach & Tools

- **Test design techniques:** Equivalence Class Partitioning, Boundary Value Analysis, Error Guessing, Exploratory Testing
- **Coverage per module:** positive (happy-path), negative/boundary, basic security (e.g. SQL-injection input), and UI/navigation checks
- **Environment:** Google Chrome on Windows 10/11; responsive layout spot-checked via browser device-emulation
- **Tools:** Microsoft Excel (Test Scenarios, Test Cases, Execution, Bug Report, RTM), Microsoft Word (Project Introduction, FRS notes, Test Plan, Summary Report), browser DevTools, screenshot capture

## 🚫 Out of Scope

OpenCart Admin back-office panel · performance/load testing · automated test scripting · real payment gateway transactions · native mobile apps

---

## About This Project

This was built independently — outside of any employer or client engagement — to practice and demonstrate a complete manual testing lifecycle for a QA portfolio. Full context and rationale for every decision (scope, entry/exit criteria, risk mitigation) is documented in the [Test Plan](./03-Test-Plan).

**Contact:** [linkedin.com/in/tanvir-ahmed-b88836365](https://www.linkedin.com/in/tanvir-ahmed-b88836365/)
