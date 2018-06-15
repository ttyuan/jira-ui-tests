# katalon-studio-samples
## JIRA UI TESTS
The **jira-ui-tests** is a testing project with examples of performing UI functional automation test on JIRA Web Application using Katalon Studio. The examples in this project are various from simple to advance tests:
### Contains
#### Simple examples
- Create test case with hard coding test data
- Create test case with hard coding encrypted test data
- Create test case with test data from GlobalVariable (Profiles)
- Create test dase with data-driven approach

#### Advance examples
- Follow [Page Object Design Pattern](https://www.seleniumhq.org/docs/06_test_design_considerations.jsp#page-object-design-pattern) 
- Test cases are set up to be reusable
- Test steps are readable with BDD mindset

### Test scenarios
#### Story: Login feature
     User story
         As a Jira user, I would like to be able to login the Jira system, so that I could manage Jira tickets.
     
     Feature: Login 
         Scenario: Login successfully
          Given The Login page is loaded successfully
          When I login the system with a valid account
          Then The Dashboard Page is loaded successfully

         Scenario Outline: Login successfully
          Given The Login page is loaded successfully
          When I login the system with valid <username> and <password>
          Then The Dashboard Page is loaded successfully
         Examples:
          | username | password  |
          |	tom      | jira@2018 |
          |	jerry    | jira@2019 |
          
#### Story: Create ticket
     User story
         As a Jira user, I would like to be able to create a new ticket, so that I could manage my tasks.

     Feature: Create ticket
         Scenario Outline: Create ticket successfully
          Given I login the system with a valid account
          When I create a new ticket with below information
          Then the ticket is created successfully
         Examples:
          | project | issueType | priority | summary |
          |         |           |          |         |
          |         |           |          |         |
