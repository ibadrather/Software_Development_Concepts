# Software Development in Agile Environment

## 1. Agile Methodologies:

### 1.1. Scrum:

* Scrum Framework
  * Scrum Roles: Product Owner, Scrum Master, Development Team
  * Scrum Artifacts: Product Backlog, Sprint Backlog, Increment
  * Scrum Events: Sprint, Sprint Planning, Daily Scrum, Sprint Review, Sprint Retrospective
* Scrum Values: Commitment, Courage, Focus, Openness, Respect
* Scrum Metrics: Velocity, Burndown Chart, Burnup Chart

### 1.2. Kanban:

* Kanban Principles
  * Visualize Work
  * Limit Work in Progress (WIP)
  * Manage Flow
  * Make Process Policies Explicit
  * Improve Collaboratively, Evolve Experimentally
* Kanban Board
  * Columns: To Do, In Progress, Done
  * Work Item Types: User Stories, Tasks, Bugs
  * WIP Limits
* Kanban Metrics: Lead Time, Cycle Time, Throughput, Cumulative Flow Diagram

### 1.3. Extreme Programming (XP):

* XP Values: Communication, Simplicity, Feedback, Courage, Respect
* XP Practices:
  * Fine-scale Feedback: Pair Programming, Planning Game, Test-Driven Development (TDD), Whole Team
  * Continuous Process: Continuous Integration, Design Improvement, Small Releases
  * Shared Understanding: Simple Design, System Metaphor, Collective Code Ownership, Coding Standards
  * Programmer Welfare: Sustainable Pace

### 1.4. Lean Software Development:

* Lean Principles:
  * Eliminate Waste
  * Build Quality
  * Create Knowledge
  * Defer Commitment
  * Deliver Fast
  * Respect People
  * Optimize the Whole
* Lean Practices: Just-in-Time (JIT) Production, Kanban, Root Cause Analysis, Set-based Design, Continuous Improvement (Kaizen)

## 2. Agile Principles and Best Practices:

* Agile Manifesto:

  * Individuals and interactions over processes and tools
  * Working software over comprehensive documentation
  * Customer collaboration over contract negotiation
  * Responding to change over following a plan
* Agile Principles:

  * Deliver value early and often
  * Embrace change
  * Focus on user needs
  * Collaborate with stakeholders
  * Empower the team
  * Maintain a sustainable pace
  * Strive for technical excellence
  * Reflect, adapt, and improve

## 3. Agile Project Management Tools:

* Task Management and Collaboration Tools:

  * Jira
  * Trello
  * Asana
  * Monday.com
* Continuous Integration and Continuous Deployment (CI/CD) Tools:

  * Github Actions
  * Jenkins
  * GitLab CI
* Version Control Systems:

  * Git
  * Subversion
* Communication and Documentation Tools:

  * Slack
  * Microsoft Teams
  * Confluence
  * Google Workspace

## 4. Agile Testing:

* Agile Testing Quadrants:

  * Quadrant 1: Technology-Facing Tests that Support the Team (e.g., Unit Tests, Component Tests)
  * Quadrant 2: Business-Facing Tests that Support the Team (e.g., Functional Tests, Story Tests)
  * Quadrant 3: Business-Facing Tests that Critique the Product (e.g., Exploratory Testing, Usability Testing)
  * Quadrant 4: Technology-Facing Tests that Critique the Product (e.g., Performance Testing, Security Testing)
* Test-Driven Development (TDD):

  * Red-Green-Refactor Cycle
    * Write a failing test (Red)
    * Write the minimal code to pass the test (Green)
    * Refactor and improve the code (Refactor)
  * Benefits of TDD: Improved code quality, Faster development, Easier debugging, Better collaboration
* Continuous Integration (CI) and Continuous Deployment (CD):

  * CI: Regularly merging code changes into a central repository, followed by automated builds and tests
  * CD: Automatically deploying the application to production after successful CI
  * CI/CD Benefits: Faster delivery, Reduced risk, Higher quality
* Behavior-Driven Development (BDD):

  * BDD Process:
    * Write user stories with acceptance criteria
    * Create executable specifications using a language like Gherkin
    * Implement the application code to fulfill the specifications
  * BDD Tools: Cucumber, SpecFlow, Behave
* Test Automation:

  * Automated Testing Frameworks and Tools:
    * For Python: pytest, unittest, Selenium WebDriver
    * For JavaScript: Jest, Mocha, Jasmine, Protractor
* Test Automation Best Practices:

  * Write maintainable and reusable test code
  * Prioritize tests based on risk and impact
  * Run automated tests frequently and in parallel
  * Monitor and analyze test results

---

## A. Agile Methodologies:

### A.1. Scrum:

* **Scrum Framework**:

  * Scrum Roles:

    * Product Owner: The Product Owner is responsible for maximizing the value of the product and represents the voice of the customer. They manage the Product Backlog, prioritize items, and ensure that the team understands the requirements.
    * Scrum Master: The Scrum Master is a servant-leader who ensures that the Scrum Team follows the Scrum framework, principles, and practices. They help the team to continuously improve and remove any impediments that hinder the team's progress.
    * Development Team: The Development Team consists of self-organizing, cross-functional professionals who deliver potentially releasable increments of the product at the end of each Sprint. They are responsible for designing, building, and testing the product.
  * Scrum Artifacts:

    * Product Backlog: The Product Backlog is an ordered list of all features, enhancements, and bug fixes that are needed to achieve the product's vision. It is dynamic and evolves as new items are discovered and priorities change.
    * Sprint Backlog: The Sprint Backlog is a subset of the Product Backlog that the Development Team commits to completing during a Sprint. It consists of user stories and tasks, which are broken down and estimated by the team.
    * Increment: The Increment is the sum of all the completed Product Backlog items during a Sprint. It must be potentially releasable, meaning it meets the Definition of Done, which is a shared understanding of what it means for work to be complete.
  * Scrum Events:

    * Sprint: A Sprint is a time-boxed period (usually 2-4 weeks) during which the Scrum Team works to create a potentially releasable Increment. Sprints have a consistent duration and follow one another without breaks.
    * Sprint Planning: Sprint Planning is an event at the beginning of each Sprint where the Scrum Team decides what to work on during the Sprint. The team selects the highest priority items from the Product Backlog and creates a Sprint Backlog.
    * Daily Scrum: The Daily Scrum is a short, daily meeting (15 minutes) where the Development Team synchronizes their work, shares progress, and discusses any impediments. It helps the team to stay on track and adjust their plan as needed.
    * Sprint Review: The Sprint Review is an event held at the end of each Sprint to demonstrate the work done during the Sprint. Stakeholders provide feedback, and the Product Owner may adjust the Product Backlog based on the feedback and current priorities.
    * Sprint Retrospective: The Sprint Retrospective is an event where the Scrum Team reflects on the past Sprint and identifies areas for improvement. They create a plan to implement improvements in the next Sprint.
* **Scrum Values**:

  * Commitment: The team members commit to achieving the goals of the Sprint and delivering a high-quality product.
  * Courage: The team members have the courage to face challenges, make tough decisions, and take responsibility for their work.
  * Focus: The team members focus on the work of the Sprint and prioritize tasks that contribute to the Sprint Goal.
  * Openness: The team members are open about their work, progress, and challenges, fostering transparency and collaboration.
  * Respect: The team members respect each other's skills, opinions, and contributions, creating a positive and supportive work environment.
* **Scrum Metrics**:

  * Velocity: Velocity is a measure of the amount of work a team can complete during a Sprint, typically measured in story points or hours. It helps the team to predict their capacity for future Sprints.
  * Burndown Chart: The Burndown Chart is a visual representation of the remaining work in the Sprint Backlog over time. It shows the progress of the team and helps to identify if the team is on track to complete the work by the end of the Sprint.
  * Burnup Chart: The Burnup Chart is a visual representation of the work completed over time. It shows the cumulative work done and helps to track the progress towards the project's goal or release.

### A.2. Kanban:

* **Kanban Principles**:

  * Visualize Work: Visualizing the work in progress makes it easier to understand the current status, identify bottlenecks, and manage the flow of work. It fosters transparency and promotes better communication among team members.
  * Limit Work in Progress (WIP): By limiting the amount of work in progress, the team can focus on completing tasks and minimize context switching. Limiting WIP helps to identify bottlenecks and improve the overall flow of work.
  * Manage Flow: Optimizing the flow of work through the system is crucial for delivering value to customers quickly and predictably. The team should monitor and adjust their processes to improve the flow of work continually.
  * Make Process Policies Explicit: Clearly defining and documenting the process policies helps the team to understand expectations, follow the process consistently, and identify areas for improvement.
  * Improve Collaboratively, Evolve Experimentally: Continuous improvement is at the heart of Kanban. The team should collaborate to identify areas for improvement and experiment with changes to the process, measuring the results and adapting accordingly.
* **Kanban Board**:

  * Columns: The Kanban Board is divided into columns representing the different stages of the workflow (e.g., To Do, In Progress, Done). Each column may have sub-columns to provide more granularity, such as "In Review" or "Ready for Deployment."
  * Work Item Types: Work items on the Kanban Board can represent various types of work, such as User Stories, Tasks, or Bugs. They are typically represented by cards containing information like the title, description, priority, and assignee.
  * WIP Limits: Work in Progress (WIP) limits are set for each column or sub-column on the Kanban Board to help the team focus on completing tasks and avoid multitasking. The limits should be based on the team's capacity and adjusted as needed.
* **Kanban Metrics**:

  * Lead Time: Lead Time is the total time it takes for a work item to move through the entire workflow, from the moment it is requested until it is completed. It helps the team understand the overall efficiency of their process.
  * Cycle Time: Cycle Time is the amount of time it takes for a work item to move through the workflow from the moment it starts until it is completed. It helps the team understand how long it takes to complete individual tasks and identify areas for improvement.
  * Throughput: Throughput is the number of work items completed within a specific time frame (e.g., per day or per week). It helps the team measure their productivity and track improvements over time.
  * Cumulative Flow Diagram: The Cumulative Flow Diagram (CFD) is a visual representation of the flow of work through the system over time. It shows the amount of work in each stage of the workflow and helps the team identify bottlenecks and trends in their process.

---

## B. Agile Testing:

* **Agile Testing Quadrants**:

  * Quadrant 1: Technology-Facing Tests that Support the Team:

    * Unit Tests: Testing individual functions or methods in isolation to ensure they work as expected. In Python, you can use unittest or pytest libraries to write unit tests.
    * Component Tests: Testing a group of related functions or classes that work together to deliver a specific functionality. These tests often require mocking external dependencies and focus on the correct interaction between internal components.
  * Quadrant 2: Business-Facing Tests that Support the Team:

    * Functional Tests: Testing the application's functionality from the user's perspective, ensuring that the application behaves as expected. In Python, you can use tools like Selenium WebDriver for web applications or Pywinauto for desktop applications.
    * Story Tests: Testing the application against user stories to verify that the implemented features meet the specified acceptance criteria. These tests usually require collaboration between developers, testers, and product owners.
  * Quadrant 3: Business-Facing Tests that Critique the Product:

    * Exploratory Testing: A manual testing technique that involves actively exploring the application to find defects. Testers use their creativity, intuition, and domain knowledge to identify potential issues.
    * Usability Testing: Assessing the application's user interface and overall user experience to ensure it is user-friendly, accessible, and efficient. This testing typically involves real users or user representatives.
  * Quadrant 4: Technology-Facing Tests that Critique the Product:

    * Performance Testing: Evaluating the application's performance under various conditions, such as increased load or high concurrency. In Python, you can use tools like Locust or JMeter for performance testing.
    * Security Testing: Assessing the application's security features and identifying potential vulnerabilities. In Python, you can use tools like Bandit for static code analysis or OWASP ZAP for dynamic security testing.
* **Test-Driven Development (TDD)**:

  * Red-Green-Refactor Cycle:
    * Write a failing test (Red): Create a test that fails because the desired functionality is not yet implemented.
    * Write the minimal code to pass the test (Green): Implement the code required to make the test pass, without worrying about code quality or optimization.
    * Refactor and improve the code (Refactor): Optimize the code, making it more readable, maintainable, and efficient, without affecting its functionality.
  * Benefits of TDD: Improved code quality, Faster development, Easier debugging, Better collaboration
* **Continuous Integration (CI) and Continuous Deployment (CD)**:

  * CI: Regularly merging code changes into a central repository, followed by automated builds and tests. In Python, you can use CI tools like Jenkins, Travis CI, or GitHub Actions to automate the process.
  * CD: Automatically deploying the application to production after successful CI. This process can be set up using tools like Jenkins, GitLab CI/CD, or AWS CodePipeline.
  * CI/CD Benefits: Faster delivery, Reduced risk, Higher quality
* **Test Automation**:

  * Automated Testing Frameworks and Tools:

    * For Python: pytest, unittest (built-in), Selenium WebDriver for web UI testing, Locust for performance testing, Behave for BDD testing.
  * Test Automation Best Practices:

    * Write maintainable and reusable test code: Follow good coding practices, keep tests modular, and use descriptive naming conventions to make the test code easy to understand and maintain.
    * Prioritize tests based on risk and impact: Focus on automating high-priority tests that cover critical functionality or have a higher risk of failure.
    * Run automated tests frequently and in parallel: Schedule tests to run regularly (e.g., on every code commit or nightly) and, if possible, run them in parallel to reduce the overall test execution time.
    * Monitor and analyze test results: Keep track of test results over time, identify trends, and address any issues or improvements needed in the test suite or application code.

---
