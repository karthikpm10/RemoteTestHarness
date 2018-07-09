The biggest concern when developing a software is to make sure that the software meets the requirements and functions as expected. To do so, the software has to be tested as and when its developed. Complex real time software projects are often developed by hundreds of people and each developer is responsible for implementing certain modules. Each of the modules should be tested thoroughly before inserting them to the final build. As and when changes are made to these modules these tests should be re-run. As there are so many packages the only way to make this intensive testing practical is to automate the process. In this project we develop a Test Harness which is an automated test tool that runs specified tests on multiple packages and records the status of the test. Test Harness accepts test requests from the users, test requests are of the xml type, they contain details about the test code and test drivers. Test harness then creates an application domain for test requests from each user and runs the test driver on the test code in this application domain which isolates its execution
