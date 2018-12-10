

# Quality Assurance

Asset Tracker is committed to providing quality service to our consumers.
Our approach to QA and continuous improvement is to utilize the best available tools 
to ensure a well development of target project. We set standards for:

- Alex Flores-Veliz – Project Manager
- Amado Suarez - Project Manager
- Nehemias Miranda –Senior Back End Engineer
- Albert Oviedo –Senior Front End Enginner
- Joan Quintero –Database Administrator
- Manuel De La Rosa –Cloud Infrastructure Engineer
- Edilenso Garcia –Cloud Infrastructure
- Saqeb Alam –Lead Designer
- Shany M. Lajara Contreras –Quality Assurance,

This section describes policies and procedures that will be used to meet 
QA project objectives. 

#### The application is expected to perform the following tasks:

- allow producers (freelancers): 
- to register, upload, and display their assets into the platform.
- to monitor statistics about their own assets.
- to monitor their royalty earnings from the use of their assets
- be able to also become a consumer.

##### Consumers:
- be able to register under a tier subscription.
- download assets as they please as long as it is allowed under their particular subscription and user agreement.

##### Administrators:
- will be able to manage both consumer and producer accounts.
- watch the performance of all users and assets.
- manage payments.



### Design

The application will be built in Ruby on Rails; a development tool which gives web developers a framework, 
providing structure for all the code they write. The Rails framework will help our developers to build a 
website or/and an application for our project and Stripe, software allows individuals and businesses to 
receive payments over the Internet. Stripe provides the technical, fraud prevention, and banking 
infrastructure required to operate on-line payment systems.

Bootstrap and other front-end frameworks might be used. The team will develop the software following 
Agile principles.

### Testing

We want our job to feel accomplishing; we don’t want to get stuck in eternal code-fix cycles, and, 
above all, we don’t want our job to be repetitive and mind numbing. Unfortunately, unless our software 
is testable, we run that risk. Untestable software forces us to work more and harder instead of smarter. 
Testability is a quality attribute including; reliability, maintainability, and usability. 
Observability and controllability are the two keystones of testability.

Black Box Testing is used to do the testing for Quality Assurance because:
- No knowledge of code needed
- No access for the source code
- Use product as user and report

Selenium-WebDriver, also known as Selenium 2.0 will be used to execute tests in the web application and create customized test results.
Selenium-WebDriver was developed to better support dynamic web pages where elements of a page may change without the page itself being reloaded. WebDriver’s goal is to supply a well-designed object-oriented API that provides improved support for modern advanced web-app testing problems.

Why use Selenium-WebDriver?  
-Real-life Interaction: It interacts with page elements in a more realistic way, for example lets say you have a disabled text box on a page you were testing, WebDriver really cannot enter any value in it just as how a real person cannot.
-Speed: WebDriver is really fast since it speaks directly to the browser uses the browser's own engine to control it.
-Browser Support: WebDriver can support the headless HtmlUnit browser.

