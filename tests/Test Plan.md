# Test Plan Template

## Table of contents

- [1. Introduction](#1-introduction)
  * [1.1 Purpose](#11-purpose)
  * [1.2 Scope](#12-scope)
  * [1.3 Intended Audience](#13-intended-audience)
  * [1.4 Document Terminology and Acronyms](#14-document-terminology-and-acronyms)
  * [1.5  References](#15--references)
  * [1.6 Document Structure](#16-document-structure)
- [2. Evaluation Mission and Test Motivation](#2-evaluation-mission-and-test-motivation)
  * [2.1 Background](#21-background)
  * [2.2 Evaluation Mission](#22-evaluation-mission)
  * [2.3 Test Motivators](#23-test-motivators)
- [3. Target Test Items](#3-target-test-items)
- [4. Outline of Planned Tests](#4-outline-of-planned-tests)
  * [4.1 Outline of Test Inclusions](#41-outline-of-test-inclusions)
  * [4.2 Outline of Other Candidates for Potential Inclusion](#42-outline-of-other-candidates-for-potential-inclusion)
  * [4.3 Outline of Test Exclusions](#43-outline-of-test-exclusions)
- [5. Test Approach](#5-test-approach)
  * [5.1 Initial Test-Idea Catalogs and Other Reference Sources](#51-initial-test-idea-catalogs-and-other-reference-sources)
  * [5.2 Testing Techniques and Types](#52-testing-techniques-and-types)
    + [5.2.1 Data and Database Integrity Testing](#521-data-and-database-integrity-testing)
    + [5.2.2 Functional Testing](#522-functional-testing)
    + [5.2.3 Business Cycle Testing](#523-business-cycle-testing)
    + [5.2.4 User Interface Testing](#524-user-interface-testing)
    + [5.2.5 Performance Profiling](#525-performance-profiling)
    + [5.2.6 Load Testing](#526-load-testing)
    + [5.2.7 Stress Testing](#527-stress-testing)
    + [5.2.8 Volume Testing](#528-volume-testing)
    + [5.2.9 Security and Access Control Testing](#529-security-and-access-control-testing)
    + [5.2.10 Failover and Recovery Testing](#5210-failover-and-recovery-testing)
    + [5.2.11 Configuration Testing](#5211-configuration-testing)
    + [5.2.12 Installation Testing](#5212-installation-testing)
- [6. Entry and Exit Criteria](#6-entry-and-exit-criteria)
  * [6.1 Test Plan](#61-test-plan)
    + [6.1.1 Test Plan Entry Criteria](#611-test-plan-entry-criteria)
    + [6.1.2 Test Plan Exit Criteria](#612-test-plan-exit-criteria)
    + [6.1.3 Suspension and Resumption Criteria](#613-suspension-and-resumption-criteria)
  * [6.2 Test Cycles](#62-test-cycles)
      - [6.2.1 Test Cycle Entry Criteria](#621-test-cycle-entry-criteria)
      - [6.2.2 Test Cycle Exit Criteria](#622-test-cycle-exit-criteria)
      - [6.2.3 Test Cycle Abnormal Termination](#623-test-cycle-abnormal-termination)
- [7. Deliverables](#7-deliverables)
- [7.1 Test Evaluation Summaries](#71-test-evaluation-summaries)
- [7.2 Reporting on Test Coverage](#72-reporting-on-test-coverage)
- [7.3 Perceived Quality Reports](#73-perceived-quality-reports)
- [7.4 Incident Logs and Change Requests](#74-incident-logs-and-change-requests)
- [7.5 Smoke Test Suite and Supporting Test Scripts](#75-smoke-test-suite-and-supporting-test-scripts)
- [7.6      Additional Work Products](#76------additional-work-products)
  * [7.6.1     Detailed Test Results](#761-----detailed-test-results)
  * [7.6.2     Additional Automated Functional Test Scripts](#762-----additional-automated-functional-test-scripts)
  * [7.6.3     Test Guidelines](#763-----test-guidelines)
  * [7.6.4     Traceability Matrices](#764-----traceability-matrices)
- [8. Testing Workflow](#8-testing-workflow)
- [9. Environmental Needs](#9-environmental-needs)
  * [9.1 Base System Hardware](#91-base-system-hardware)
  * [9.2 Base Software Elements in the Test Environment](#92-base-software-elements-in-the-test-environment)
  * [9.3 Productivity and Support Tools](#93-productivity-and-support-tools)
  * [9.4 Test Environment Configurations](#94-test-environment-configurations)
- [10. Responsibilities, Staffing, and Training Needs](#10-responsibilities--staffing--and-training-needs)
  * [10.1 People and Roles](#101-people-and-roles)
  * [10.2 Staffing and Training Needs](#102-staffing-and-training-needs)
- [11. Iteration Milestones](#11-iteration-milestones)
- [12. Risks, Dependencies, Assumptions, and Constraints](#12-risks--dependencies--assumptions--and-constraints)
- [13. Management Process and Procedures](#13-management-process-and-procedures)

## 1. Introduction

### 1.1 Purpose

The purpose of the Iteration Test Plan is to gather all of the information necessary to plan and control the test effort for a given iteration. It describes the approach to testing the software.
This Test Plan for Vaultionizer supports the following objectives:

- Identifies the items that should be targeted by the tests.
- Identifies the motivation for and ideas behind the test areas to be covered.
- Outlines the testing approach that will be used.
- Identifies the required resources and provides an estimate of the test efforts.

### 1.2 Scope

Unit Tests are testing the functionality, performance and reliability of authentification inside LectureFeed.

### 1.3 Intended Audience

For all that are interested in the structure and testing architecture inside the LectureFeed-project. For example our professor and other course members. 
Feel free to express your interest as an non-involved person.

### 1.4 Document Terminology and Acronyms



| Abbr | Abbreviation                        |
|------|-------------------------------------|
| API  | Application Programmable Interface  |
| JSON | JavaScript Object Notation          |
| CI   | Continuous Integration              |
| CD   | Continuous Delivery/Deployment      |
| n/a  | not applicable                      |
| SRS  | Software Requirements Specification |
| tbd  | to be determined                    |
| UML  | Unified Modeling Language           |
| DHBW | Duale Hochschule Baden-Württemberg  |
| UI   | User Interface                      |
| VC   | Version Control                     |
| TDD  | Test Driven Development             |

### 1.5  References



| Title                                                                   | Date       | Publishing organization   |
| ------------------------------------------------------------------------|:----------:| ------------------------- |
| [Blog](lecturefeed.wordpress.com/)                                      | Apr. 2022  |                  |
| [GitHub Repository]()                                                   | Apr. 2022  |                  |
| [Use Cases](https://github.com/MaximilianLincks/LectureFeed-Docs/tree/main/use-cases) | Apr. 2022  |    |
| [Test Plan](./TestPlan.md)                                              | Apr. 2022  |                  |
| [SRS](../README.md)                                                     | Apr. 2022  |                  |
| [SAD](../Architecture.md)                                               | Apr. 2022  |                  |

### 1.6 Document Structure

<!--[This subsection outlines what the rest of the Test Plan contains and gives an introduction to how the rest of the document is organized. This section may be eliminated if a Table of Contents is used.]-->
//TODO

## 2. Evaluation Mission and Test Motivation

The use-case that is supposed to be tested is "login". Authentification is a key functionality in our application. Ensuring the reliability, functionality and stability as well as the performance of this important feature helps ensuring the sustained quality of our code. 
The whole project benefits of high quality in automated tests. Regular development of tests enables us to use test-driven development and ensures consistent quality.

### 2.1 Background

The login of our application is solved using a username and a session key which is used to connect users. 
There is no password. This is the easiest way for users to get into a session and recognize each other by usernames.

Testing serves to ensure that the written code does what it is intended to do. It also prevents future code changes to break existing functionality unnoticed. In the context of integration it can also prevent broken software states to be merged into secured VC branches

### 2.2 Evaluation Mission

We are eager to find important problems and bugs which could be for example a error caused by wrong input. 
Verifying high standards in our software whilst testing the features promised by the tested code. 
This way we are raising the quality of our product. 

### 2.3 Test Motivators

We want to ensure the funcitonality of our use-cases.

## 3. Target Test Items

We save our unit tests inside the repository where our application is saved.

## 4. Outline of Planned Tests

We are planning on covering as many use-cases as possible. 
In case of our "login"-use-case we are looking at the scenarios "successfull login", "empty username", "empty inputs" and "empty session link". 
This way we over all possibilities we could think off. 

### 4.1 Outline of Test Inclusions

we are planning on implementing the following tests during the course of our project:
*Backend: Spring Boot Application*:

- Unit testing
- Integration testing
- Api testing

The tests themself will not be tested and will not account into code coverage.

### 4.2 Outline of Other Candidates for Potential Inclusion

Testing the functionalities of the participiant as well as the presenter may cause the need of different tests for different environments. 
This will require further investigation.

### 4.3 Outline of Test Exclusions

We are not going to do Database tests.

## 5. Test Approach

Our tests are supposed to be working, stable tests with accurate descriptions. We are trying to achieve useful scenarios. 
We want to test the coorporation between different components and dynamic change of data using integration tests.
We also need to test the functionality of our naviation in the UI. This is going to be implemented using Selenium. There will be different tests for participiant- and presenterview.
Unit Tests are going to be used to test different components one at a time. 

### 5.1 Initial Test-Idea Catalogs and Other Reference Sources

Our SRS is going to provide the informaiton about use-cases that require testing. 
Furthermore we have designed UML-diagrams that explaing our use-cases in more detail.

### 5.2 Testing Techniques and Types

#### 5.2.1 Functional Testing

The functionality of our software will be tested using mostly Unit-Tests 

|                       | Description                                                         |
|-----------------------|---------------------------------------------------------------------|
|Technique Objective    |  We are going to use JUnit to mock code and trigger features   |
|Technique              |  We are going to simulate the input of different strings in the fields "username" and "session code"  |
|Oracles                |    |;[Outline one or more strategies that can be used by the technique to accurately observe the outcomes of the test. The oracle combines elements of both the method by which the observation can be mad, and the characteristics of specific outcome that indicate probable success or failure. Ideally, oracles will be self-verifying, allowing automated tests to make an initial assessment of test pass or failure, however, be careful to mitigate the risks inherent in automated results determination.]
|Required Tools         |    |;[The technique requires the following tools:; Test Script Automation Tool; base configuration imager and restorer; backup and recovery tools; installation-monitoring tools (registry, hard disk, CPU, memory, and so on); data-generation tools]
|Success Criteria       |   |;[The technique supports the testing of:; all key use-case scenarios; all key features ]
|Special Considerations |    |;[Identify or describe those items or issues (internal or external) that impact the implementation and execution of function test.]

#### 5.2.2 Business Cycle Testing

<!--[Business Cycle Testing should emulate the activities performed on the  Project Name  over time. A period should be identified, such as one year, and transactions and activities that would occur during a year's period should be executed. This includes all daily, weekly, and monthly cycles, and events that are date-sensitive, such as ticklers.]-->

|                       | Description                                                         |
|-----------------------|---------------------------------------------------------------------|
|Technique Objective    |  |;[Exercise target-of-test and background processes according to required business models and schedules to observe and log target behavior.]   
|Technique              |  |;[Testing will simulate several business cycles by performing the following:; The tests used for target-of-test's function testing will be modified or enhanced to increase the number of times each function is executed to simulate several different users over a specified period.; All time or date-sensitive functions will be executed using valid and invalid dates or time periods.; All functions that occur on a periodic schedule will be executed or launched at the appropriate time.; Testing will include using valid and invalid data to verify the following:; The expected results occur when valid data is used.;The appropriate error or warning messages are displayed when invalid data is used.;Each business rule is properly applied.]   |
|Oracles                |   |;[Outline one or more strategies that can be used by the technique to accurately observe the outcomes of the test. The oracle combines elements of both the method by which the observation can be made, and the characteristics of specific outcome that indicate probable success or failure. Ideally, oracles will be self-verifying, allowing automated tests to make an initial assessment of test pass or failure, however, be careful to mitigate the risks inherent in automated results determination.]  |
|Required Tools         |   |;[The technique requires the following tools:; Test Script Automation Tool; base configuration imager and restorer; backup and recovery tools; data-generation tools]  |
|Success Criteria       |  |;[The technique supports the testing of all critical business cycles.]   |
|Special Considerations |   |;[System dates and events may require special support activities.; A business model is required to identify appropriate test requirements and procedures.]  |

#### 5.2.3 User Interface Testing

<!--[User Interface (UI) testing verifies a user's interaction with the software. The goal of UI testing is to ensure that the UI provides the user with the appropriate access and navigation through the functions of the target-of-test. In addition, UI testing ensures that the objects within the UI function as expected and conform to corporate, or industry, standards.]-->

|                       | Description                                                         |
|-----------------------|---------------------------------------------------------------------|
|Technique Objective    |  |;[Exercise the following to observe and log standards conformance and target behavior:; Navigation through the target-of-test reflecting business functions and requirements, including window-to-window, field-to- field, and use of access methods (tab keys, mouse movements, accelerator keys).; Window objects and characteristics can be exercised-such as menus, size, position, state, and focus.]   |
|Technique              |  |;[Create or modify tests for each window to verify proper navigation and object states for each application window and object.]   |
|Oracles                |  |;[Outline one or more strategies that can be used by the technique to accurately observe the outcomes of the test. The oracle combines elements of both; the method by which the observation can be made and the characteristics of specific outcome that indicate probable success or failure. Ideally, oracles will be self-verifying, allowing automated tests to make an initial assessment of test pass or failure, however, be careful to mitigate the risks inherent in automated results determination.]   |
|Required Tools         |   |;[The technique requires the Test Script Automation Tool.]  |
|Success Criteria       |   |;[The technique supports the testing of each major screen or window that will be used extensively by the end user.]  |
|Special Considerations |   |;[Not all properties for custom and third party objects can be accessed.]  |

#### 5.2.4 Performance Profiling

<!--[Performance profiling is a performance test in which response times, transaction rates, and other time-sensitive requirements are measured and evaluated. The goal of Performance Profiling is to verify performance requirements have been achieved. Performance profiling is implemented and executed to profile and tune a target-of-test's performance behaviors as a function of conditions, such as workload or hardware configurations.-->

<!--Note: Transactions in the following table refer to "logical business transactions". These transactions are defined as specific use cases that an actor of the system is expected to perform using the target-of-test, such as add or modify a given contract.]-->

|                       | Description                                                         |
|-----------------------|---------------------------------------------------------------------|
|Technique Objective    |   |;[Exercise behaviors for designated functional transactions or business functions under the following conditions to observe and log target behavior and application performance data:; normal anticipated workload; anticipated worst-case workload]  |
|Technique              |   |;[Use Test Procedures developed for Function or Business Cycle Testing.; Modify data files to increase the number of transactions or the scripts to increase the number of iterations that occur in each transaction.; Scripts should be run on one machine (best case is to benchmark single user, single transaction) and should be repeated with multiple clients (virtual or actual, see Special Considerations below).]  |
|Oracles                |  	|;[Outline one or more strategies that can be used by the technique to accurately observe the outcomes of the test. The oracle combines elements of both the method by which the observation can be made and the characteristics of specific outcome that indicate probable success or failure. Ideally, oracles will be self-verifying, allowing automated tests to make an initial assessment of test pass or failure, however, be careful to mitigate the risks inherent in automated results determination.]   |
|Required Tools         |   |;[The technique requires the following tools:; Test Script Automation Tool; an application performance profiling tool, such as Rational Quantify; installation-monitoring tools (registry, hard disk, CPU, memory, and so on; resourse-constraining tools; for example, Canned Heat]  |
|Success Criteria       |  |;[The technique supports testing:; Single Transaction or single user: Successful emulation of the transaction scripts without any failures due to test implementation problems.; Multiple transactions or multiple users: Successful emulation of the workload without any failures due to test implementation problems.]   |
|Special Considerations |  |;[Comprehensive performance testing includes having a background workload on the server.; There are several methods that can be used to perform this, including:; "Drive transactions" directly to the server, usually in the form of Structured Query Language (SQL) calls.; Create "virtual" user load to simulate many clients, usually several hundred. Remote Terminal Emulation tools are used to accomplish this load. This technique can also be used to load the network with "traffic".; Use multiple physical clients, each running test scripts, to place a load on the system.; Performance testing should be performed on a dedicated machine or at a dedicated time. This permits full control and accurate measurement.; The databases used for Performance Testing should be either actual size or scaled equally.]   |


#### 5.2.5 Load Testing

<!--[Load testing is a performance test that subjects the target-of-test to varying workloads to measure and evaluate the performance behaviors and abilities of the target-of-test to continue to function properly under these different workloads. The goal of load testing is to determine and ensure that the system functions properly beyond the expected maximum workload. Additionally, load testing evaluates the performance characteristics, such as response times, transaction rates, and other time-sensitive issues.-->

<!--[Note: Transactions in the following table refer to "logical business transactions". These transactions are defined as specific functions that an end user of the system is expected to perform using the application, such as add or modify a given contract.]-->

|                       | Description                                                         |
|-----------------------|---------------------------------------------------------------------|
|Technique Objective    |  |;[Exercise designated transactions or business cases under varying workload conditions to observe and log target behavior and system performance data.] |
|Technique              |  |;[Use Transaction Test Scripts developed for Function or Business Cycle Testing as a basis, but remember to remove unnecessary interactions and delays.; Modify data files to increase the number of transactions or the tests to increase the number of times each transaction occurs.; Workloads should include—for example, daily, weekly, and monthly—peak loads.; Workloads should represent both average as well as peak loads.; Workloads should represent both instantaneous and sustained peaks.; The workloads should be executed under different Test Environment Configurations.]   |
|Oracles                |  |;[Outline one or more strategies that can be used by the technique to accurately observe the outcomes of the test. The oracle combines elements of both the method by which the observation can be made and the characteristics of specific outcome that indicate probable success or failure. Ideally, oracles will be self-verifying, allowing automated tests to make an initial assessment of test pass or failure, however, be careful to mitigate the risks inherent in automated results determination.]   |
|Required Tools         |   |;[The technique requires the following tools:; Test Script Automation Tool; Transaction load scheduling and control tool; installation-monitoring tools (registry, hard disk, CPU, memory, and so on); resource-constraining tools; for example, Canned Heat; data-generation tools]  |
|Success Criteria       |  |;[The technique supports the testing of Workload Emulation, which is the successful emulation of the workload without any failures due to test implementation problems.]   |
|Special Considerations |  |;[Load testing should be performed on a dedicated machine or at a dedicated time. This permits full control and accurate measurement.; The databases used for load testing should be either actual size or scaled equally.]   |


#### 5.2.6 Stress Testing

<!--[Stress testing is a type of performance test implemented and executed to understand how a system fails due to conditions at the boundary, or outside of, the expected tolerances. This typically involves low resources or competition for resources. Low resource conditions reveal how the target-of-test fails that is not apparent under normal conditions. Other defects might result from competition for shared resources, like database locks or network bandwidth, although some of these tests are usually addressed under functional and load testing.-->

<!--Note: References to transactions in the following table refer to logical business transactions.-->

|                       | Description                                                         |
|-----------------------|---------------------------------------------------------------------|
|Technique Objective    |   |;[Exercise the target-of-test functions under the following stress conditions to observe and log target behavior that identifies and documents the conditions under which the system fails to continue functioning properly:; little or no memory available on the server (RAM and persistent storage space); maximum actual or physically capable number of clients connected or simulated; multiple users performing the same transactions against the same data or accounts; "overload" transaction volume or mix (see Performance Profiling above)]  |
|Technique              |   |;[Use tests developed for Performance Profiling or Load Testing.; To test limited resources, tests should be run on a single machine, and RAM and persistent storage space on the server should be reduced or limited.; For remaining stress tests, multiple clients should be used, either running the same tests or complementary tests to produce the worst-case transaction volume or mix.]  |
|Oracles                |  |;[Outline one or more strategies that can be used by the technique to accurately observe the outcomes of the test. The oracle combines elements of both the method by which the observation can be made and the characteristics of specific outcome that indicate probable success or failure. Ideally, oracles will be self-verifying, allowing automated tests to make an initial assessment of test pass or failure, however, be careful to mitigate the risks inherent in automated results determination.]   |
|Required Tools         |  |;[The technique requires the following tools:; Test Script Automation Tool; Transaction load scheduling and control tool; installation-monitoring tools (registry, hard disk, CPU, memory, and so on; resource-constraining tools; for example, Canned Heat; data-generation tools]   |
|Success Criteria       |  |;[The technique supports the testing of Stress Emulation. The system can be emulated successfully in one or more conditions defined as stress conditions, and an observation of the resulting system state, during and after the condition has been emulated, can be captured.]   |
|Special Considerations |  |;[Stressing the network may require network tools to load the network with messages or packets.; The persistent storage used for the system should temporarily be reduced to restrict the available space for the database to grow.; Synchronize the simultaneous clients accessing of the same records or data accounts.]   |


#### 5.2.7 Volume Testing

<!--Volume testing subjects the target-of-test to large amounts of data to determine if limits are reached that cause the software to fail. Volume testing also identifies the continuous maximum load or volume the target-of-test can handle for a given period. For example, if the target-of-test is processing a set of database records to generate a report, a Volume Test would use a large test database, and would check that the software behaved normally and produced the correct report.-->-->

|                       | Description                                                         |
|-----------------------|---------------------------------------------------------------------|
|Technique Objective    ||;  [Stressing the network may require network tools to load the network with messages or packets.; The persistent storage used for the system should temporarily be reduced to restrict the available space for the database to grow.; Synchronize the simultaneous clients accessing of the same records or data accounts.]   |
|Technique              ||;  [Use tests developed for Performance Profiling or Load Testing.; Multiple clients should be used, either running the same tests or complementary tests to produce the worst-case transaction volume or mix (see Stress Testing) for an extended period.; Maximum database size is created (actual, scaled, or filled with representative data), and multiple clients are used to run queries and report transactions simultaneously for extended periods.]]   |
|Oracles                ||;   [Outline one or more strategies that can be used by the technique to accurately observe the outcomes of the test. The oracle combines elements of both the method by which the observation can be made and the characteristics of specific outcome that indicate probable success or failure. Ideally, oracles will be self-verifying, allowing automated tests to make an initial assessment of test pass or failure, however, be careful to mitigate the risks inherent in automated results determination.]  |
|Required Tools         ||;   [The technique requires the following tools:; Test Script Automation Tool; Transaction load scheduling and control tool; installation-monitoring tools (registry, hard disk, CPU, memory, and so on; resource-constraining tools; for example, Canned Heat; data-generation tools]  |
|Success Criteria       ||;  	[The technique supports the testing of Volume Emulation. Large quantities of users, data, transactions, or other aspects of the system use under volume can be successfully emulated and an observation of the system state changes over the duration of the volume test can be captured.]   |
|Special Considerations ||;  [What period of time would be considered an acceptable time for high volume conditions, as noted above?]   |


#### 5.2.8 Security and Access Control Testing

<!--Security and Access Control Testing focuses on two key areas of security:; Application-level security, including access to the Data or Business Functions; System-level Security, including logging into or remotely accessing to the system; Based on the security you want, application-level security ensures that actors are restricted to specific functions or use cases, or they are limited in the data that is available to them. For example, everyone may be permitted to enter data and create new accounts, but only managers can delete them. If there is security at the data level, testing ensures that "user type one" can see all customer information, including financial data, however, "user type two" only sees the demographic data for the same client.; System-level security ensures that only those users granted access to the system are capable of accessing the applications and only through the appropriate gateways.-->

|                       | Description                                                         |
|-----------------------|---------------------------------------------------------------------|
|Technique Objective    ||;  [Exercise the target-of-test under the following conditions to observe and log target behavior:; Application-level Security: an actor can access only those functions or data for which their user type is provided permissions.; System-level Security: only those actors with access to the system and applications are permitted to access them].   |
|Technique              ||;  [Application-level Security: Identify and list each user type and the functions or data for which each type has permissions.; Create tests for each user type and verify each permission by creating transactions specific to each user type.; Modify user type and rerun tests for same users. In each case, verify those additional functions or data are correctly available or denied.; System-level Access: See Special Considerations below.]   |
|Oracles                ||;  [Outline one or more strategies that can be used by the technique to accurately observe the outcomes of the test. The oracle combines elements of both the method by which the observation can be made and the characteristics of specific outcome that indicate probable success or failure. Ideally, oracles will be self-verifying, allowing automated tests to make an initial assessment of test pass or failure, however, be careful to mitigate the risks inherent in automated results determination.] |
|Required Tools         ||;  [The technique requires the following tools:; Test Script Automation Tool; "Hacker" security breach and probing tools; OS Security Administration tools]   |
|Success Criteria       ||;  [The technique supports the testing of the appropriate functions or data affected by security settings can be tested for each known actor type.]   |
|Special Considerations ||; [Access to the system must be reviewed or discussed with the appropriate network or systems administrator. This testing may not be required as it may be a function of network or systems administration.]


#### 5.2.9 Failover and Recovery Testing



<!--Failover and recovery testing ensures that the target-of-test can successfully failover and recover from a variety of hardware, software, or network malfunctions with undue loss of data or data integrity]-->

<!--For those systems that must be kept running, failover testing ensures that when a failover condition occurs, the alternate or backup systems properly "take over" for the failed system without any loss of data or transactions.; Recovery testing is an antagonistic test process in which the application or system is exposed to extreme conditions, or simulated conditions, to cause a failure, such as device Input/Output (I/O) failures, or invalid database pointers and keys. Recovery processes are invoked, and the application or system is monitored and inspected to verify proper application, or system, and data recovery has been achieved.-->

|                       | Description                                                         |
|-----------------------|---------------------------------------------------------------------|
|Technique Objective    |  |;[Simulate the failure conditions and exercise the recovery processes (manual and automated) to restore the database, applications, and system to a desired, known state. The following types of conditions are included in the testing to observe and log behavior after recovery:; power interruption to the client; power interruption to the server; communication interruption via network servers; interruption, communication, or power loss to DASD (Dynamic Access Storage Devices) and DASD controllers; incomplete cycles (data filter processes interrupted, data synchronization processes interrupted); invalid database pointers or keys; invalid or corrupted data elements in database]  |
|Technique              |  |;[The tests already created for Function and Business Cycle testing can be used as a basis for creating a series of transactions to support failover and recovery testing, primarily to define the tests to be run to test that recovery was successful.; Power interruption to the client: power down the PC.; Power interruption to the server: simulate or initiate power down procedures for the server.; Interruption via network servers: simulate or initiate communication loss with the network (physically disconnect communication wires or power down network servers or routers).; Interruption, communication, or power loss to DASD and DASD controllers: simulate or physically eliminate communication with one or more DASDs or DASD controllers.; Once the above conditions or simulated conditions are achieved, additional transactions should be executed and upon reaching this second test point state, recovery procedures should be invoked.; Testing for incomplete cycles utilizes the same technique as described above except that the database processes themselves should be aborted or prematurely terminated.; Testing for the following conditions requires that a known database state be achieved. Several database fields, pointers, and keys should be corrupted manually and directly within the database (via database tools). Additional transactions should be executed using the tests from Application Function and Business Cycle Testing and full cycles executed.]   |
|Oracles                |  |;[Outline one or more strategies that can be used by the technique to accurately observe the outcomes of the test. The oracle combines elements of both the method by which the observation can be made and the characteristics of specific outcome that indicate probable success or failure. Ideally, oracles will be self-verifying, allowing automated tests to make an initial assessment of test pass or failure, however, be careful to mitigate the risks inherent in automated results determination.]  |
|Required Tools         |  |;[The technique requires the following tools:; base configuration imager and restorer; installation-monitoring tools (registry, hard disk, CPU, memory, and so on; backup and recovery tools]  |
|Success Criteria       |  |;[The technique supports the testing of:; One of more simulated disasters involving one or more combinations of the application, database, and system.; One or more simulated recoveries involving one or more combinations of the application, database, and system to a known desired state.  ] |
|Special Considerations |  |;[Recovery testing is highly intrusive. Procedures to disconnect cabling (simulating power or communication loss) may not be desirable or feasible. Alternative methods, such as diagnostic software tools may be required.; Resources from the Systems (or Computer Operations), Database, and Networking groups are required.; These tests should be run after hours or on an isolated machine.]  |


#### 5.2.10 Configuration Testing

<!--[Configuration testing verifies the operation of the target-of-test on different software and hardware configurations. In most production environments, the particular hardware specifications for the client workstations, network connections, and database servers vary. Client workstations may have different software loaded (for example, applications, drivers, and so on) and, at any one time, many different combinations may be active using different resources.]-->

|                       | Description                                                         |
|-----------------------|---------------------------------------------------------------------|
|Technique Objective    |   |;[Exercise the target-of-test on the required hardware and software configurations to observe and log target behavior under different configurations and identify changes in configuration state.]  |
|Technique              |   |;[Use Function Test scripts.; Open and close various non-target-of-test related software, such as the Microsoft Excel and Word applications, either as part of the test or prior to the start of the test.; Execute selected transactions to simulate actors interacting with the target-of-test and the non-target-of-test software.; Repeat the above process, minimizing the available conventional memory on the client workstation.]  |
|Oracles                |   |;[Outline one or more strategies that can be used by the technique to accurately observe the outcomes of the test. The oracle combines elements of both the method by which the observation can be made and the characteristics of specific outcome that indicate probable success or failure. Ideally, oracles will be self-verifying, allowing automated tests to make an initial assessment of test pass or failure, however, be careful to mitigate the risks inherent in automated results determination.]  |
|Required Tools         |   |;[The technique requires the following tools:; base configuration imager and restorer; installation-monitoring tools (registry, hard disk, CPU, memory, and so on ] |
|Success Criteria       |   |;[The technique supports the testing of one or more combinations of the target test items running in expected, supported deployment environments.]  |
|Special Considerations |   |;[What non-target-of-test software is needed, is available, and is accessible on the desktop?; What applications are typically used?; What data are the applications running; for example, a large spreadsheet opened in Excel or a 100-page document in Word?; The entire systems' netware, network servers, databases, and so on, also need to be documented as part of this test.]  |


#### 5.2.11 Installation Testing

<!--[Installation testing has two purposes. The first is to ensure that the software can be installed under different conditions (such as a new installation, an upgrade, and a complete or custom installation) under normal and abnormal conditions. Abnormal conditions include insufficient disk space, lack of privilege to create directories, and so on. The second purpose is to verify that, once installed, the software operates correctly. This usually means running a number of tests that were developed for Function Testing.]-->

|                       | Description                                                         |
|-----------------------|---------------------------------------------------------------------|
|Technique Objective    |   |;[Exercise the installation of the target-of-test onto each required hardware configuration under the following conditions to observe and log installation behavior and configuration state changes:; new installation: a new machine, never installed previously with Project Name; update: a machine previously installed Project Name, same version; update: a machine previously installed Project Name, older version]  |
|Technique              |   |;[Develop automated or manual scripts to validate the condition of the target machine.; new: never installed; same or older version already installed; Launch or perform installation..; Using a predetermined subset of Function Test scripts, run the transactions.]  |
|Oracles                |   |;[Outline one or more strategies that can be used by the technique to accurately observe the outcomes of the test. The oracle combines elements of both the method by which the observation can be made and the characteristics of specific outcome that indicate probable success or failure. Ideally, oracles will be self-verifying, allowing automated tests to make an initial assessment of test pass or failure, however, be careful to mitigate the risks inherent in automated results determination.]  |
|Required Tools         |   |;[The technique requires the following tools:; base configuration imager and restorer; installation-monitoring tools (registry, hard disk, CPU, memory, and so on ] |
|Success Criteria       |   |;[The technique supports the testing of the installation of the developed product in one or more installation configurations.]  |
|Special Considerations |   |;[What transactions should be selected to comprise a confidence test that application has been successfully installed and no major software components are missing?]  |


## 6. Entry and Exit Criteria

### 6.1 Test Plan

#### 6.1.1 Test Plan Entry Criteria

n/a

#### 6.1.2 Test Plan Exit Criteria

n/a

#### 6.1.3 Suspension and Resumption Criteria

n/a

### 6.2 Test Cycles

##### 6.2.1 Test Cycle Entry Criteria

n/a

##### 6.2.2 Test Cycle Exit Criteria

n/a

##### 6.2.3 Test Cycle Abnormal Termination

n/a


## 7. Deliverables

## 7.1 Test Evaluation Summaries

n/a

## 7.2 Reporting on Test Coverage

<!--[Provide a brief outline of both the form and content of the reports used to measure the extent of testing, and indicate how frequently they will be produced. Give an dication as to the method and tools used to record, measure, and report on the extent of testing.]-->

## 7.3 Perceived Quality Reports

n/a

## 7.4 Incident Logs and Change Requests

<!--[Provide a brief outline of both the method and tools used to record, track, and manage test incidents, associated change requests, and their status.]-->

## 7.5 Smoke Test Suite and Supporting Test Scripts

n/a

## 7.6      Additional Work Products
n/a

### 7.6.1     Detailed Test Results
n/a

### 7.6.2     Additional Automated Functional Test Scripts
<!--[These will be either a collection of the source code files for automated test scripts, or the repository of both source code and compiled executables for test scripts maintained by the test automation product.]-->

### 7.6.3     Test Guidelines
n/a

### 7.6.4     Traceability Matrices
n/a



## 8. Testing Workflow

<!--[Provide an outline of the workflow to be followed by the test team in the development and execution of this Test Plan.
The specific testing workflow that you will use should be documented separately in the project's Development Case. It should explain how the project has customized the base RUP test workflow (typically on a phase-by-phase basis). In most cases, we recommend you place a reference in this section of the Test Plan to the relevant section of the Development Case. It might be both useful and sufficient to simply include a diagram or image depicting your test workflow.
More specific details of the individual testing tasks are defined in a number of different ways, depending on project culture; for example:
* defined as a list of tasks in this section of the Test Plan, or in an accompanying appendix
* defined in a central project schedule (often in a scheduling tool such as Microsoft Project)
* documented in individual, "dynamic" to-do lists for each team member, which are usually too detailed to be placed in the Test Plan
* documented on a centrally located whiteboard and updated dynamically
* not formally documented at all
Based on your project culture, you should either list your specific testing tasks here or provide some descriptive text explaining the process your team uses to handle detailed task planning and provide a reference to where the details are stored, if appropriate.
For Master Test Plans, we recommend avoiding detailed task planning, which is often an unproductive effort if done as a front-loaded activity at the beginning of the project. A Master Test Plan might usefully describe the phases and the number of iterations, and give an indication of what types of testing are generally planned for each Phase or Iteration.
Note: Where process and detailed planning information is recorded centrally and separately from this Test Plan, you will have to manage the issues that will arise from having duplicate copies of the same information. To avoid team members referencing out-of-date information, we suggest that in this situation you place the minimum amount of process and planning information within the Test Plan to make ongoing maintenance easier and simply reference the "Master" source material.]
-->
## 9. Environmental Needs

<!--[This section presents the non-human resources required for the Test Plan.]-->

### 9.1 Base System Hardware

<!--[The specific elements of the test system may not be fully understood in early iterations, so expect this section to be completed over time. We recommend that the system simulates the production environment, scaling down the concurrent access and database size, if and where appropriate.]-->

The following table sets forth the system resources for the test effort presented in this Test Plan.

| Resource                                                                | Quantity | Name and Type |
|-------------------------------------------------------------------------|----------|---------------|
| Database Server                                                         |          |               |
| - Network or Subnet                                                     |          | TBD           |
| - Server Name                                                           |          | TBD           |
| - Database Name                                                         |          | TBD           |
| Client Test PCs                                                         |          |               |
| - Include special configuration requirements                            |          | TBD           |
| Test Repository                                                         |          |               |
| - Network or Subnet                                                     |          | TBD           |
| - Server Name                                                           |          | TBD           |
| Test Development PCs                                                    |          | TBD           |

### 9.2 Base Software Elements in the Test Environment

The following base software elements are required in the test environment for this Test Plan.

<!--[These are examples!]-->

| Software Element Name |  Type and Other Notes                        |
|-----------------------|----------------------------------------------|
| Android Studio        | Test Runner / IDE                            |
| IntelliJ              | Test Runner / IDE                            |
| JUnit 4               | Unit testing library                         |
| Espresso              | UI testing library                           |
| Cucumber              | human readable test definitions              |

<!--[These are examples!]-->

### 9.3 Productivity and Support Tools

The following tools will be employed to support the test process for this Test Plan.

| Tool Category or Type             | Tool Brand Name | Vendor or In-house | Version |
|-----------------------------------|-----------------|--------------------|---------|
| Test Management                   |                 |                    |         |
| Defect Tracking                   |                 |                    |         |
| ASQ Tool for functional testing   |                 |                    |         |
| ASQ Tool for performance testing  |                 |                    |         |
| Test Coverate Monitor or Profiler |                 |                    |         |
| Project Management                |                 |                    |         |
| DBMS tools                        |                 |                    |         |

### 9.4 Test Environment Configurations

The following Test Environment Configurations need to be provided and supported for this project.

| Configuration Name                | Description | Implemented in Physical Configuration |
|-----------------------------------|-------------|---------------------------------------|
| Average user configuration        |             |                                       |
| Minimal configuration supported   |             |                                       |
| Visually and mobility challenged  |             |                                       |
| International Double Byte OS      |             |                                       |
| Network installation (not client) |             |                                       |

## 10. Responsibilities, Staffing, and Training Needs

### 10.1 People and Roles

This table shows the staffing assumptions for the test effort.

| Human Resources                          |                                                                         |                                                                                                                                                                                                                                                                                   |
|------------------------------------------|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Role                                     | Minimum Resources Recommended (number of full-time roles allocated)     | Specific Responsbilities or Comments                                                                                                                                                                                                                                              |
| Test Manager                             |                                                                         | Provides management oversight. Responsibilities include: planning and logistics agree mission identify motivators acquire appropriate resources present management reporting advocate the interests of test evaluate effectiveness of test effort                                 |
| Test Analyst                             |                                                                         | Identifies and defines the specific tests to be conducted. Responsibilities include: identify test ideas define test details determine test results document change requests evaluate product quality                                                                             |
| Test Designer                            |                                                                         | Defines the technical approach to the implementation of the test effort. Responsibilities include: define test approace define test automation architecture verify test techniques define testability elements structure test implementation                                      |
| Tester                                   |                                                                         | Implements and executes the tests. Responsibilities include: implement tests and test suites execute test suites log results analyze and recover from test failures document incidents                                                                                            |
| Test System Administrator                |                                                                         | Ensurs test environment and assets are managed and maintained. Responsibilities include: administer test management system install and support access to, and recovery of, test environment configurations and test labs                                                          |
| Database Administrator, Database Manager |                                                                         | Ensures test data (database) environment and assets are managed andmaintained. Responsibilities include: support the administration of test data and test beds (database)                                                                                                         |
| Designer                                 |                                                                         | Identifies and defines the operations, attributes, and associations of the test classes. Responsibilities include: defines the test classes required to support testability requirements as defined by the test team                                                              |
| Implementer                              |                                                                         | Implements and unit tests the test classes and test packages. Responsibilities include: creates the test components required to support testability requirements as defined by the designer                                                                                       |

### 10.2 Staffing and Training Needs

<!--This section outlines how to approach staffing and training the test roles for the project.-->

<!--[The way to approach staffing and training will vary from project to project. If this section is part of a Master Test Plan, you should indicate at what points in the project lifecycle different skills and numbers of staff are needed. If this is an Iteration Test Plan, you should focus mainly on where and what training might occur during the Iteration. Give thought to your training needs, and plan to schedule this based on a Just-In-Time (JIT) approach—there is often a temptation to attend training too far in advance of its usage when the test team has apparent slack. Doing this introduces the risk of the training being forgotten by the time it's needed. Look for opportunities to combine the purchase of productivity tools with training on those tools, and arrange with the vendor to delay delivery of the training until just before you need it. If you have enough headcount, consider having training delivered in a customized manner for you, possibly at your own site. The test team often requires the support and skills of other team members not directly part of the test team. Make sure you arrange in your plan for appropriate availability of System Administrators, Database Administrators, and Developers who are required to enable the test effort.]-->

## 11. Iteration Milestones

We want to keep over 20% code coverage.

## 12. Risks, Dependencies, Assumptions, and Constraints

| Risk                                    | Mitigation Strategy                                           | Contingency (Risk is realized)                                                                              |
|-----------------------------------------|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Prerequisite Entry Criteria is not met. |  Tester  will define the prerequisites that must be met before Load Testing can start.  Customer  will endeavor to meet prerequisites indicated by  Tester .          | meet outstanding prerequisites consider Load Test Failure                                                   |
| Test data proves to be inadequate.      |  Customer  will ensure a full set of suitable and protected test data is available. br/  Tester  will indicate what is required and will verify suitability of test data. | redefine test data review Test Plan and modify Components (that is, scripts) consider Load Test Failure |
| Database requires a refresh.            |  System Administrator  will endeavor to ensure that the Database is regularly refreshed as required by the  Tester .                                                      | restore data and restart clear Database                                                                     |

## 13. Management Process and Procedures

n/a
