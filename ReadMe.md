# OLA3/Assignment 3 - Task Service Enhancement: Testing, Code Analysis, and Collaborative Reviews
 - Group name: **TofuBytes** 
 - Members: **Isak, Jamie & Helena**

## Table of Contents

1. [Objective](#objective)
2. [Group Testing & Refinement](#group-testing--refinement)
3. [Code Coverage](#5-code-coverage)
4. [Optional: Code Quality with SonarQube](#6-optional-code-quality-with-sonarqube)
5. [Peer Code Reviews](#7-peer-code-reviews)
6. [Reflections](#9-reflection-software-reviews)
   - [Reflection: Software Reviews](#9-reflection-software-reviews)
   - [Reflection: Testing and Code Quality](#10-reflection-on-testing-and-code-quality)
7. [Deliverables](#deliverables-required-by-the-assignment)
8. [Tools and Technologies](#tools-and-technologies-we-utilized)

## Objective
Refine the **Task Service** with a focus on testing, static code analysis, and peer reviews. Apply code and software review principles to ensure quality, covering both automated and manual review processes.

---

### Group Testing & Refinement
- We made sure to refine our code, and developed unit tests for our validator component and Equivalence Partitioning and Boundary Value Analysis were applied to ensure comprehensive test coverage.
Our unit tests are made based on this data:
- Description length:
  - Valid, too short, too long ( minimum 5, maximum 255)
  - Boundary value: 4-5, 255-256
- Category length:
  - Valid, too short, too long ( minimum 2, maximum 50)
  - Boundary value: 1-2, 50-51
- Deadline:
  - Valid, invalid ( minimum datetime now -1 min, maximum datetime is as long as the calendar can show)
  - Boundary value: now to 1 min ago, now to 1 min in the future

In our `Validator.cs` file and `ValidatorTest.cs`, the validator is tested with the above data.

### 5. Code Coverage
- Code coverage was measured using the built-in code coverage tool in JetBrains Rider, and the results were analyzed to identify areas that need more testing. This was done to ensure that the code is thoroughly tested and that as many code paths as possible are covered. **Our final coverage came out to be 89%.**

### 6. Optional: Code Quality with SonarQube
 - As this was optional, we decided to not prioritize this part of the assignment. We felt that the tools we used were sufficient for our needs, and that we could spend our time more efficiently on other parts of the assignment. That said, we did look into SonarQube, and it seems like a very powerful tool that we might use in the future.

### 7. Peer Code Reviews

We consistently perform code reviews on each other's work. We use GitHub pull requests to review the code, and below are some examples of some reviews we did:

![Code comment 1](Images/codeComment1.png)

![Code comment 2](Images/codeComment2.png)

Especially in this last comment, it's clear that no single person is 'in charge' of the code. Instead, that we always work together to make sure what works, what doesn't.
We always check the code for readability and maintainability, and make sure that the code is up to our standards.

## Reflections 

---

### 9. Reflection: Software Reviews

In relation to functional correctness, the code performs as expected and passes all the test cases. `Validation_test` was added as a way of ensuring our Validation Testing was done using equivalence partitioning and boundary value analysis. 
For equivalence partitioning, the inputs were divided into valid and invalid categories, ensuring that the code handled typical cases within these partitions correctly. 
Additionally, boundary value analysis revealed that the code responds appropriately at the edges of input ranges. However, further testing could be beneficial to expand the test coverage, especially for complex input patterns or extreme edge cases.
We made sure that our software was correct, and that it was easy to maintain. We also made sure that the code was structured in a way that was easy to understand.
The code was made to do what it was supposed to do, and if there were anything that were 'too much' or 'too little', we made sure to fix it.

In relation to best practices, we always try to maintain a clean code structure and follow the coding standards. We make sure to name our methods correctly, so everyone knows what the methods actually do.
We strive to improve documentation, comments is a way we want to reflect that directly in the code.

### 10. Reflection on Testing and Code Quality

For this part of the assignment we went with **Qodana** as our static code analysis tool mostly because it was built into Rider making it easily accessible and more or less was a one-click solution.
  The utilization of Qodana had a significant impact on our project. By scanning our codebase, Qodana identified various issues, no bugs was discovered this time around though. This early detection allowed us to address these problems promptly, preventing them from escalating into more serious issues. The insights provided by Qodana gave us a clear view of the areas that needed improvement, and by using their GUI in the browser it all was clearly presented to us in a nice and really user-friendly way. This helped us to focus on the most critical first(we had 3), and then work our way down to the less severe ones.

Value of code and software reviews:
- Specifically software reviews, helped us understand the importance of teamwork. Sometimes we are too focused on the small things we need to do, without looking at the rest of the code. This is where software reviews come in, and help us see the bigger picture.
    - For instance, initially, we approached the validator tests 3 different ways in the beginning. we were able to compare these different approaches, discuss their merits and drawbacks, and converge on a unified, consistent testing strategy. In a way this also fostered a deeper understanding and alignment among us as a team.

Influence of Equivalence Partitioning and Boundary Value Analysis on test design:
- Equivalence partitioning helped us gather an understanding of what needed to be tested and within what margins. With the combination of the boundary value, we implemented more tests than we would usually, and it also helped us focus more on testing than writing the actual code.
    - Equivalence partitioning helped us identify the major categories of input values, and  boundary values helped us ensure that the boundaries of these categories was tested thoroughly.
 
In general, these practices work together to form a robust safety net that helps identify and address issues early in the development process. By using these techniques early on, we could find and resolve problems before they snowball into larger, more complex issues. This not only leads to higher-quality software but also saves time and effort, reducing the need for extensive debugging later in the development cycle.

---

## Deliverables required by the assignment
- Refined Task Service source code.
- Unit tests with mocks.
- PMD (or FxCop) report.
- JaCoCo (or Coverlet) code coverage report.
- Peer review feedback and any code changes.
- Software review reflection.
- 
- Optional: SonarQube report.

---

## Tools and Technologies we utilized
- **Languages**: C#.
- **Mocking**: Moq (C#).
- **Static Code Analysis**: Qodana & Qodana Cloud .
- **Code Coverage**: Built-in Code Coverage tool in JetBrains Rider.
- **Peer Code Reviews**: GitHub Pull Requests.
- **Documentation**: Markdown.
- **Version Control**: Git & GitHub.
- **IDE**: JetBrains Rider.