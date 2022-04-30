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

n/a

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
In case of our "login"-use-case we are looking at the scenarios "successful login", "empty username", "empty inputs" and "empty session link". 
This way we over all possibilities we could think of. 

### 4.1 Outline of Test Inclusions

we are planning on implementing the following tests during the course of our project:
Backend: Spring Boot Application:

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
|Technique Objective    |  We are going to use JUnit and Mockito to mock code and trigger features   |
|Technique              |  We are going to simulate the input of different strings in the fields "username" and "session code"  |
|Oracles                |    We are looking for a login-token to test the outcome of the authentication| 
|Required Tools         |    Mockito, Spring-Boot, JUnit 5|
|Success Criteria       |   A valid token is returned|
|Special Considerations |    We are using a mock of our database|

#### 5.2.3 User Interface Testing

Angular Tests jasmine (Selenium?) 


|                       | Description                                                         |
|-----------------------|---------------------------------------------------------------------|
|Technique Objective    | ensuring quality and functionality of our frontend. The User Interface is supposed to work like intended and provide all functionalities needed by the user|
|Technique              |  Using Selenium and Jasmine we can test components separately but also control the functionality of groups of components  |
|Oracles                |  We expect all steps of different features to work properly and show up the way we intend them to do   |
|Required Tools         |   We are going to test using Jasmine and Selenium. This way we are covering all possible bugs |
|Success Criteria       |   the frontend has to work as intended. Data exchange and looks need to be tested|
|Special Considerations |   separate tests for presenter and participant may be needed  |

#### 5.2.8 Security and Access Control Testing

|                       | Description                                                         |
|-----------------------|---------------------------------------------------------------------|
|Technique Objective    |We want to find bugs related to security and access control |
|Technique              | we try to detect security issues using automated tests   |
|Oracles                |  We implement tests for successful behaviours and tests that are supposed to create errors. |
|Required Tools         |  JUnit 5, Mockito, SonarCloud, IntelliJ and Github   |
|Success Criteria       |  There are no security related bugs|
|Special Considerations | Testing the security of our system is extremely important. We will review the security tests in a group of at least 3 people|


#### 5.2.11 Installation Testing

The installation tests of our software will not be automated. We will manually install it regularly.

## 6. Entry and Exit Criteria

### 6.1 Test Plan

#### 6.1.1 Test Plan Entry Criteria

Pushing new commits to gitlab will trigger the Github pipeline.
There needs to be a successful installation of LectureFeed

#### 6.1.2 Test Plan Exit Criteria

When all tests pass without throwing an exception. If an exception is thrown we want to be notified.

#### 6.1.3 Suspension and Resumption Criteria

n/a

### 6.2 Test Cycles

##### 6.2.1 Test Cycle Entry Criteria

A mocked database and controller need to be created.  

##### 6.2.2 Test Cycle Exit Criteria

all tests pass correctly. 

##### 6.2.3 Test Cycle Abnormal Termination

Send emails to team LectureFeed

## 7. Deliverables

## 7.1 Test Evaluation Summaries

## Build-Status
[![Build LectureFeed](https://github.com/MaximilianLincks/LectureFeed/actions/workflows/build_main.yml/badge.svg?branch=main)](https://github.com/MaximilianLincks/LectureFeed/actions/workflows/build_main.yml)

[![Coverage](https://sonarcloud.io/api/project_badges/measure?project=MaximilianLincks_LectureFeed&amp;metric=coverage)](https://sonarcloud.io/summary/new_code?id=MaximilianLincks_LectureFeed)

## 7.2 Reporting on Test Coverage

Sonarcloud live-updates our code coverage, quality gate status, 

## 7.3 Perceived Quality Reports

More badges = more fun. 

LectureFeed Repository:

[![Build LectureFeed](https://github.com/MaximilianLincks/LectureFeed/actions/workflows/build_main.yml/badge.svg?branch=main)](https://github.com/MaximilianLincks/LectureFeed/actions/workflows/build_main.yml)

[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=MaximilianLincks_LectureFeed&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=MaximilianLincks_LectureFeed)

[![Duplicated Lines (%)](https://sonarcloud.io/api/project_badges/measure?project=MaximilianLincks_LectureFeed&metric=duplicated_lines_density)](https://sonarcloud.io/summary/new_code?id=MaximilianLincks_LectureFeed)

[![Vulnerabilities](https://sonarcloud.io/api/project_badges/measure?project=MaximilianLincks_LectureFeed&metric=vulnerabilities)](https://sonarcloud.io/summary/new_code?id=MaximilianLincks_LectureFeed)

[![Coverage](https://sonarcloud.io/api/project_badges/measure?project=MaximilianLincks_LectureFeed&amp;metric=coverage)](https://sonarcloud.io/summary/new_code?id=MaximilianLincks_LectureFeed)

[![Lines of Code](https://sonarcloud.io/api/project_badges/measure?project=MaximilianLincks_LectureFeed&metric=ncloc)](https://sonarcloud.io/summary/new_code?id=MaximilianLincks_LectureFeed)

[![Bugs](https://sonarcloud.io/api/project_badges/measure?project=MaximilianLincks_LectureFeed&metric=bugs)](https://sonarcloud.io/summary/new_code?id=MaximilianLincks_LectureFeed)

LectureFeed-web Repository:

[![Nodejs-Build](https://github.com/MaximilianLincks/LectureFeed-Web/actions/workflows/build.yml/badge.svg)](https://github.com/MaximilianLincks/LectureFeed-Web/actions/workflows/build.yml)

[![Duplicated Lines (%)](https://sonarcloud.io/api/project_badges/measure?project=MaximilianLincks_LectureFeed-Web&metric=duplicated_lines_density)](https://sonarcloud.io/summary/new_code?id=MaximilianLincks_LectureFeed-Web)

[![Vulnerabilities](https://sonarcloud.io/api/project_badges/measure?project=MaximilianLincks_LectureFeed-Web&metric=vulnerabilities)](https://sonarcloud.io/summary/new_code?id=MaximilianLincks_LectureFeed-Web)

LectureFeed-Desktop: 

[![Build LectureFeed-Desktop](https://github.com/MaximilianLincks/LectureFeed-Desktop/actions/workflows/build.yml/badge.svg)](https://github.com/MaximilianLincks/LectureFeed-Desktop/actions/workflows/build.yml)

[![Lines of Code](https://sonarcloud.io/api/project_badges/measure?project=MaximilianLincks_LectureFeed-Web&metric=ncloc)](https://sonarcloud.io/summary/new_code?id=MaximilianLincks_LectureFeed-Web)



## 7.4 Incident Logs and Change Requests

We are using YouTrack for change requests. Those will be manually created after receiving notifications about failed tests by Sonarcloud.
GitHub and SonarCloud are logging the build-status

## 7.5 Smoke Test Suite and Supporting Test Scripts

We are non-smokers

## 7.6      Additional Work Products
n/a

### 7.6.1     Detailed Test Results

We only receive a mail with information about if and where the tests failed. SonarCloud and GitHub are providinglogs containing further information 

### 7.6.2     Additional Automated Functional Test Scripts

n/a

### 7.6.3     Test Guidelines
n/a

### 7.6.4     Traceability Matrices
n/a



## 8. Testing Workflow

1) Local testing in the IDE
2) Commit and Push triggers build and test execution in the Github Pipeline
3) Each Pull Request and every push on main-branch triggers the pipeline (build and test)
4) Information about the tests will be sent to team LectureFeed

## 9. Environmental Needs

This section presents the non-human resources required for the Test Plan.

### 9.1 Base System Hardware

The following table sets forth the system resources for the test effort presented in this Test Plan.

| Resource                                                                | Quantity | Name and Type |
|-------------------------------------------------------------------------|----------|---------------|
| CI/CD server                                                            | 1        | GitHub Runner |
| local test machine                                                      |    4     | NoteBook of Viktor, Stefanie, Maximilian, Lukas    |

### 9.2 Base Software Elements in the Test Environment

The following base software elements are required in the test environment for this Test Plan.

| Software Element Name |  Type and Other Notes                        |
|-----------------------|----------------------------------------------|
| IntelliJ              | Test Runner / IDE                            |
| [JUnit 5](https://lecturefeed.wordpress.com/2022/04/29/week-4-2/)               | Unit testing library                         |
| Selenium              | UI testing library                           |
| [Cucumber](https://lecturefeed.wordpress.com/2021/11/07/week-4/)              | human readable test definitions              |

### 9.3 Productivity and Support Tools

The following tools will be employed to support the test process for this Test Plan.

| Tool Category or Type             | Tool Brand Name | Version |
|-----------------------------------|-----------------|---------|
| Project Management                |    YouTrack     | newest  |
| Defect Tracking                   |  SonarCloud     |         |
| Test Coverage Monitor or Profiler |   SonarCloud    |         |
| Test Management                 |  SonarCloud     |         |

### 9.4 Test Environment Configurations

n/a

## 10. Responsibilities, Staffing, and Training Needs

### 10.1 People and Roles

This table shows the staffing assumptions for the test effort.

| Human Resources                          |      |                                                                                                                                                                                                                                                                                   |
|------------------------------------------|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Role                                     |  Minimum Resources Recommended (number of full-time roles allocated)    | Specific Responsbilities or Comments                                                                                                                                                                                                                                              |
| Test Manager                             |   Maximilian   | Provides management oversight. Responsibilities include: planning and logistics agree mission identify motivators acquire appropriate resources present management reporting advocate the interests of test evaluate effectiveness of test effort                                 |
| Test Analyst                             |   Viktor   | Identifies and defines the specific tests to be conducted. Responsibilities include: identify test ideas define test details determine test results document change requests evaluate product quality                                                                             |
| Test Designer                            |   Stefanie   | Defines the technical approach to the implementation of the test effort. Responsibilities include: define test approace define test automation architecture verify test techniques define testability elements structure test implementation                                      |
| Tester                                   |   Lukas   | Implements and executes the tests. Responsibilities include: implement tests and test suites execute test suites log results analyze and recover from test failures document incidents                                                                                            |
| Test System Administrator                |   Maximilian   | Ensurs test environment and assets are managed and maintained. Responsibilities include: administer test management system install and support access to, and recovery of, test environment configurations and test labs                                                          |
| Database Administrator, Database Manager |   Viktor   | Ensures test data (database) environment and assets are managed andmaintained. Responsibilities include: support the administration of test data and test beds (database)                                                                                                         |
| Designer                                 |   Stefanie   | Identifies and defines the operations, attributes, and associations of the test classes. Responsibilities include: defines the test classes required to support testability requirements as defined by the test team                                                              |
| Implementer                              |   Lukas   | Implements and unit tests the test classes and test packages. Responsibilities include: creates the test components required to support testability requirements as defined by the designer                                                                                       |
| Professional photographer for marketing references |   Linus Pust   | takes photos of our team for our weekly blogs. Using his enormous experience in photographing ... people |

### 10.2 Staffing and Training Needs

We learn new testing technologies using references provided by the [website](https://kay.fasten-your-seat-belts.de/) of our professor.

## 11. Iteration Milestones

We want to keep over 20% code coverage.

## 12. Risks, Dependencies, Assumptions, and Constraints

We worked out our risk table in [week 2 of this semester](https://lecturefeed.wordpress.com/2022/04/16/week-2-2/)

| Risk           | Mitigation Strategy |
|----------------|---------------------|
|Inexperienced team  | We share experience and learn new technologies regularily                                                                                           |                                      
|Unexpected workload caused by other lectures                |  We start with the important tasks and try to finish most of our scope before the first exam                   |                                       
|Undefined team workflows  |   Define rules and workflows and make sure everybody knows and follows those                                   
|Users don't have access to a local network or a device       |       Users can access a session on mobile devices. We provide a tutorial for alternative usage other than laptops              |                                       
|Progress not monitored |     We use dashboards and agile boards to track our progress live on youtrack                |                                      
|Lack of special skills required by project     |  Orienting our current scope on the one of last semester                   |                                       
|Unclear responsibilities   | We split our project in subproject with dedicated asignees                    |                                      
|Too many requirements |     We have the option to reduce our scope if we don't finish in time                |                                       
|DHBW closes due to covid  |  Have the technical requirements to keep communicating and working at home                   |                                       
 


## 13. Management Process and Procedures

n/a
