# Managing the Unmanageable (Second Edition)

## Information

| | Book data |
| --- | --- |
| **Title**  | Managing the Unmanageable (Second Edition)|
| **Author** | Mickey W. Mantle & Ron Lichty |
| **Release Date** | Dec 10, 2019 |
| **ISBN** | ISBN-13: 978-0-13-566736-1 |
| **Webpage** | https://managingtheunmanageable.net/ |

## Chapter 9: Managing Successful Software Delivery

### Technical Debt

Collaboration between **Product Owners** and **Development Leaders** are mostly based in the following list:

* Take into account dependencies.
* Enable design to emerge.
* Test architecture.
* Enable early learning.
* Engage in [risk-first development](https://riskfirst.org/) to reduce uncertainty.

But the product backlog is not complete if it has only user stories. The backlog should have *technical items* such as:

* Architectural foundation-building.
* Technical debt pay-down.
* Bug fixes.
* Risk mitigation.

Also, apart from both lists, we should include *functional debt*. This debt should be prioritized by the **Product Owners** based in the business needs. That *functional debt* must be treated as a new user story.

#### Organization

There are two ways of *user stories*, *technical items* and *debt items* organization (maybe more):

* We can create a separate backlog for *technical items* and for *user stories*. We must include each *debt item* in the corresponding backlog.
* We can create a just one backlog that includes both kind of tasks, *technical items* and *user stories*.

#### Identify Technical Debt

First of all, we must identify the *technical debt*. As we mentioned early, we should identify if the debt task is *technical* or *functional*.

* *Technical Debt*: is the result when the *development* team delivers a feature or a piece of code fast not taking into account the detail care, giving priority to the software delivery time versus perfect software. This action, could produces a lack of quality on any of the following aspects:
  * Software Architecture.
  * Code quality.
  * Performance.
  * Test coverage.
  * Team standards alignments.
  * Documentation.
  * ...

* *Functional Debt*: is the result when the *product* team wants to deliver a feature in a partial manner or detects that an old feature could be done in another way that improves the user experience or the business metrics.
