In this project we develop a Client, Test Harness and a Repository module All modules define services using Windows communication Foundation(WCF) for communication Client module displays a Graphical user interface using Windows Presentation Foundation(WPF), which allows the user to either submit a test request to the Test Harness or query the Repository for the logs. Client creates proxy clients of Test Harness and Repository and uses this proxy objects to communicate with these modules. Client module also defines and hosts a service to accept results from other modules.

Test Harness Module creates and hosts services to accept the test requests. Test Harness module spins a thread which monitors its receiver queue. When there is a message in this queue, it de queues the message, parses it, extracts the xml request , spins a new thread and hands over the xml request to this thread, a temporary directory , whose name is a concatenation of test request user name and current timestamp, is created, test harness module requests the library files from the repository, stores them in this directory, Test harness then creates an application domain for test requests from each user and runs the test driver on the test code in this application domain which isolates its execution.

Repository module creates and hosts services to download and upload files from the Repository. This module spins a separate thread which queues all the request. When there is a message in the queue it de queues the message and either uploads or downloads the files depending on the mesage The users of the Test Harness Are Developers, Managers, Quality Assurance Team, Test Teams, Teaching Assistant and Graders. Developers use the Test Harness to test the functionality of the modules designed by them, they use this to perform Construction test, Integration test and Performance Test. Managers use this to check whether all the requirements are met by the software. Quality Assurance team uses this to run Regression test, Integration test and Quality assurance test, to make sure the product meets the requirements. Graders use this to ascertain the completeness of the project.
