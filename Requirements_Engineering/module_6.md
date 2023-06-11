# Module 6: Requirements Validation and Verification

## Topic 1: Understanding Validation and Verification

**Validation** and **Verification** are vital parts of Requirements Engineering. Validation answers the question "Are we building the right product?", focusing on user requirements and needs. On the other hand, Verification addresses the question "Are we building the product right?", meaning it's about confirming the system meets specified requirements.

### Case Study:
Consider a software project to create an e-commerce application. Verification checks if all features specified in the requirements (such as login functionality, shopping cart, payment gateway integration, etc.) are implemented correctly. Validation, in contrast, will consider if the implemented system fulfills the business needs (like user-friendly interface, secure payment method, efficient delivery tracking system, etc.).

## Topic 2: Techniques for Requirements Verification
Verification techniques ensure that requirements are correct, complete, feasible, and testable. They include:

**Reviews**: Requirements are examined critically to find any errors, ambiguities, omissions, or inconsistencies. It can be a peer review, a team review, or an expert review.

**Prototyping**: An initial model of the system is built to verify if the system can be developed and to discover any issues early.

**Model Checking**: Models of the system (like UML diagrams) are checked against certain properties.

**Test Case Generation**: Creating test cases based on the requirements. If a test case cannot be created for a requirement, then that requirement might be unverifiable.

### Example:
Consider the requirement: "The system should respond quickly to user input". In a review, we might discover that this requirement is ambiguous (what does "quickly" mean?) and untestable (how do we test "quickly"?). It should be revised to something like: "The system should respond to user input within 1 second."

## Topic 3: Techniques for Requirements Validation
Validation techniques ensure that the system being developed will satisfy the user's needs. Techniques include:

**User Feedback**: Direct feedback from users or stakeholders provides valuable information on whether the requirements meet their needs.

**Prototyping**: Like in verification, prototyping allows users to interact with a model of the system, helping validate if the system meets their expectations.

**Acceptance Tests**: These are tests based on user requirements. If the system passes these tests, it's valid.


### Example:
For our e-commerce application, we can create a prototype for the shopping cart feature and have potential users interact with it. Their feedback can help us validate if our shopping cart implementation will meet user needs and expectations.

## Topic 4: Managing Changes in Requirements
Requirements change for a variety of reasons: users change their minds, business environments evolve, laws and regulations update, etc. Change is inevitable, and managing change is essential to successful Requirements Engineering.

**Change Control Process**: When a change is proposed, it should be evaluated for its impact on the system, cost, schedule, and feasibility. Changes must be approved before being incorporated.

**Traceability**: Maintaining a traceability matrix helps in understanding the impact of changes. It links requirements to their source (like user needs) and to other entities (like system components, test cases).

**Version Control**: Changes should be tracked using version control tools. Each version of the requirements should be stored and tagged appropriately.


### Case Study:
Consider that after our e-commerce site is half developed, a new law mandates extra security checks for online payments. We need to manage this change. We assess the impact of the change, estimate its cost and time, and once approved, incorporate it into our requirements. With a traceability matrix and version control, we can efficiently track and implement this change.

By understanding validation and verification processes in detail, one can ensure that requirements are effectively captured, articulated, and implemented to meet user needs and expectations.

