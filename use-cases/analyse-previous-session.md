#Use-Case Specification: analyzing a session

# 1 analyzing a session

## 1.1 Brief Description
The Moderator uploads a session and is shown data about the session.

# 2 Flow of Events
## 2.1 Basic Flow
- Moderator starts LectureFeed application
- Moderator opens analyze-session menu
- Moderator uploads session-data
- Data is shown

### 2.1.1 Activity Diagram


### 2.1.2 Mock-up


### 2.1.3 Narrative

```gherkin
Feature: analyze session

  Scenario: analyze session 
    Given I started the LectureFeed application
    And I open the analyze-session menu
    When I upload mockup-Session.csv
    And I press the "analyze Session" button   
    Then am shown the data collected during the session
```

## 2.2 Alternative Flows
The session-data includes errors and cannot be analyzed. A error message is shown.

# 3 Special Requirements
(n/a)

# 4 Preconditions
A session is finished, saved and downloaded.

# 5 Postconditions
After analyzing a session the data can be analyzed again. Nothing is changed

# 6 Extension Points
(n/a)

