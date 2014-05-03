## How to ensure software quality (DianDian App) ##

	Huang MingEn (13126083) mingenhuang@gmail.com

This article will take the app of DianDian (点点单词) as the target system. Software quality assurance (SQA) consists of a means of monitoring the software engineering processes and methods used to ensure quality. SQA encompasses the entire software development process, which includes processes such as requirements definition, software design, coding, testing and so on. And we will talk about how to ensure the software quality of the app mainly from the view of testing.

### No Defects != Good Quality ###

Software application quality depends upon a lot more than simply the absence of defects. Consider the consequences of improperly captured business processes, poorly extensible architecture, inflexible code – none are necessarily the result of bugs but all can badly affect end user satisfaction.

### Ensure functional quality ###

- Ensure every line of code executes properly with Unit Testing.

	Unit testing is the process of testing each unit of code in a single component. This form of testing is carried out by the developer as the component is being developed. The developer is responsible for ensuring that each detail of the implementation is logically correct. Unit tests are normally discussed in terms of the type of coverage they provide:
	- Function coverage: Each function/method executed by at least one test case.
	- Statement coverage: Each line of code covered by at least one test case (need more test cases than above).
	- Path coverage: Every possible path through code covered by at least one test case (need plenty of test cases).
	
- Ensure every function produces its expected outcome with Functional Testing.
	
	Functional testing addresses concerns surrounding the correct implementation of functional requirements. Commonly referred to as black box testing, this type of testing requires no knowledge of the underlying implementation.

	Functional test suites are created from requirement use cases, with each scenario becoming a functional test. As a component is implemented, the respective functional test is applied to it after it has been unit tested.

- Ensure all functions combine to deliver the desired business result with System Testing. 
- Ensure new changes did not adversely affect other parts of the system with Regression Testing.
- Ensure the system integrates with and does not adversely affect other enterprise systems with System Integration Testing. 
- Ensure the customer is satisfied with the system with Acceptance Testing.

	Acceptance testing aims to test how well users interact with the system, that it does what they expect and is easy to use. Although it is the final phase of testing before software deployment, the tests themselves should be defined as early as possible.  Early definition ensures customer expectations are set appropriately and confirms for designers that what they are building will satisfy the end user's requirements. To that end, acceptance test cases are developed from user requirements and are validated in conjunction with actual end users of the system. 

### Test early and often ###

Quality should be built in throughout the development life cycle rather than tested in at the end of a project. This is also an important part of the agile development process which we can use when making the app of DianDian(点点单词). We test what we do, whether it’s design, code, or documentation, early and often so that defects are found while the work is still fresh in people’s minds and before the defects can become too deeply embedded in the software.

###	Minimise variation and build in flexibility ###

Any customisation of the software introduces variation which needs to be tested and maintained for every version of the app. Where there is a common need for the same customisation from lots of clients we try to allow for this by building flexibility into the system. This limited and known variation can be accounted for when testing and does not add a huge cost overhead to our development process, while at the same time allowing our clients to change the things they need to.




