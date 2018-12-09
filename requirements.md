 

**Software Requirements Specification for AssetTracker**

Version 1.0 


Team 5

10/01/2018

------




[TOC]
- [1.    Introduction](#1----introduction)
  * [1.1    Purpose](#11----purpose)
  * [1.2    Document Conventions](#12----document-conventions)
  * [1.3    Intended Audience and Reading Suggestions](#13----intended-audience-and-reading-suggestions)
  * [1.4    Product Scope](#14----product-scope)
  * [1.5    References](#15----references)
- [2.    Overall Description](#2----overall-description)
  * [2.1    Product Perspective](#21----product-perspective)
  * [2.2    Product Functions](#22----product-functions)
  * [2.3    User Classes and Characteristics](#23----user-classes-and-characteristics)
  * [2.4    Operating Environment](#24----operating-environment)
  * [2.5    Design and Implementation Constraints](#25----design-and-implementation-constraints)
  * [2.6    User Documentation](#26----user-documentation)
  * [2.7    Assumptions and Dependencies](#27----assumptions-and-dependencies)
- [3.    External Interface Requirements](#3----external-interface-requirements)
  * [3.1    User Interfaces](#31----user-interfaces)
  * [3.2    Hardware Interfaces](#32----hardware-interfaces)
  * [3.3    Software Interfaces](#33----software-interfaces)
  * [3.4    Communications Interfaces](#34----communications-interfaces)
- [4.    System Features](#4----system-features)
  * [4.1    System Feature 1](#41----system-feature-1)
  * [4.2    System Feature 2 (and so on)](#42----system-feature-2--and-so-on-)
- [5.    Other Nonfunctional Requirements](#5----other-nonfunctional-requirements)
  * [5.1    Performance Requirements](#51----performance-requirements)
  * [5.2    Safety Requirements](#52----safety-requirements)
  * [5.3    Security Requirements](#53----security-requirements)
  * [5.4    Software Quality Attributes](#54----software-quality-attributes)
  * [5.5    Business Rules](#55----business-rules)
- [6.    Other Requirements](#6----other-requirements)



**Revision History**

| **Name** | **Date** | **Reason For   Changes** | **Version** |
| -------- | -------- | ------------------------ | ----------- |
|          |          |                          |             |
|          |          |                          |             |

 

 




# 1.    Introduction

## 1.1    Purpose 

AssetTracker is a marketplace for virtual reality assets. This platform will allow producers to upload their assets and consumers to access and download them. The platform is subscription based and consumers will have a tiered subscription model. This platform will have administrators that will have access to statistics and data about the whole system and its users.

## 1.2    Document Conventions

This project, as discussed with the client, will be developed with agile principles and frequent cyclical iterations with the client will be needed where the design or the focus at that particular stage might be re-determined.

**Some definitions:**

**Consumers**: Clients who will pay a subscription to be allowed to download and use the assets available in the marketplace.

**Producers**: Freelancers affiliated to the platform which create the assets and make them available to the consumers.

## 1.3    Intended Audience and Reading Suggestions

This document is intended to be read by our developers, the project manager, testers, documentation writers, and the client.

## 1.4    Product Scope

AssetTracker is a great tool to convert a tedious operation into a fully functioning marketplace. It facilitates the process of adding producers and keep track of their sales. Producers (and consumers) can have their own profile and collection page with variety of products. Administrators can easily monitor the overall operation.

## 1.5    References

This project looked at the following resources for guidance and inspiration:

[Active Admin](https://activeadmin.info/) 

[Agile Best Practices](https://linchpinseo.com/the-agile-method/)

[Ebay Architecture](https://www.slideshare.net/tcng3716/ebay-architecture)

[Design and Implementation of E-Commerce Site
for Online Shopping](https://opus.govst.edu/cgi/viewcontent.cgi?article=1079&context=capstones) 

[Heroku Architecture](https://devcenter.heroku.com/categories/heroku-architecture)

[Rails](https://guides.rubyonrails.org/)





# 2.    Overall Description

## 2.1    Product Perspective

AssetTracker is a Virtual Reality Assets marketplace. This project allows viewing various products available, enables registered users to purchase desired products instantly.

This project provides an easy access to Administrators to keep track of all activities inside the whole system. 

## 2.2    Product Functions

AssetTracker is a marketplace for Virtual Reality assets. Instead of designing all of your assets yourself, this platform allows you to buy/lease assets from creators around the country.

The marketplace will allow producers to register, upload, and display their assets into the platform. They will also be able to monitor statistics about their own assets. They also will be able to monitor their royalty earnings from the use of their assets.

Consumers will be able to register under a tiered subscription and download assets as they please as long as it is allow under their particular subscription.

Administrators will be able to manage both consumer and producers accounts, watch the performance of all users and assets, and manage payments.

**Diagram Needed - WIP** 

## 2.3    User Classes and Characteristics

This system has three type of users: producers, consumers, and administrators. Administrators need advance access to the system and can only be created by a super-administrator. However, all three type of users are critical to the well being of the business. 

Producers who will register, upload, and display their assets into the platform. They will also be able to monitor statistics about their own assets. They also will be able to monitor their royalty earnings from the use of their assets.

Consumers will be able to register under a tiered subscription and download assets as they please as long as it is allow under their particular subscription.

Administrators will be able to manage both consumer and producers accounts, watch the performance of all users and assets, and manage payments.

## 2.4    Operating Environment

This project will be launched as a containerized web application hosted in a cloud platform. Docker will be used for the containerization part and Heroku as the cloud platform.

## 2.5    Design and Implementation Constraints

The application will be build in Ruby on Rails and Stripe will be used to process the payments, and it will use a Postgres database. Bootstrap and other front-end frameworks might be used. The team will develop the software following Agile principles.

A post-delivery service agreement with the client is on the table but has not been determined yet.

## 2.6    User Documentation

A user manual for all users will be delivered at the final stage in the form of a help page or subdomain within the application. User Manual will explain how hidden features within the application work, such as Databases, creating tables, inserting and/or updating tables and fetching data. 

## 2.7    Assumptions and Dependencies

<List any assumed factors (as opposed to known facts) that could affect the requirements stated in the SRS. These could include third-party or commercial components that you plan to use, issues around the development or operating environment, or constraints. The project could be affected if these assumptions are incorrect, are not shared, or change. Also identify any dependencies the project has on external factors, such as software components that you intend to reuse from another project, unless they are already documented elsewhere (for example, in the vision and scope document or the project plan).>



This projects assumes that the assets will be able to be stored as BLOBS in the Postgres database. If this is not possible, we might have to use Amazon S3 or other solutions to store the assets. This could cause a significant delay in the delivery of the project.

This project assumes that the administrators will be the ones setting subscription prices.

This project assumes the client will provide us with all of the metrics that he would like being monitored in the system and agrees that some metrics might not be possible to track or could cause significant delays and/or affect the budget.

This project also assumes single level administrators without  different privilege levels among them.

# 3.    External Interface Requirements

## 3.1    User Interfaces

<Describe the logical characteristics of each interface between the software product and the users. This may include sample screen images, any GUI standards or product family style guides that are to be followed, screen layout constraints, standard buttons and functions (e.g., help) that will appear on every screen, keyboard shortcuts, error message display standards, and so on. Define the software components for which a user interface is needed. Details of the user interface design should be documented in a separate user interface specification.>

## 3.2    Hardware Interfaces

<Describe the logical and physical characteristics of each interface between the software product and the hardware components of the system. This may include the supported device types, the nature of the data and control interactions between the software and the hardware, and communication protocols to be used.>

## 3.3    Software Interfaces

<Describe the connections between this product and other specific software components (name and version), including databases, operating systems, tools, libraries, and integrated commercial components. Identify the data items or messages coming into the system and going out and describe the purpose of each. Describe the services needed and the nature of communications. Refer to documents that describe detailed application programming interface protocols. Identify data that will be shared across software components. If the data sharing mechanism must be implemented in a specific way (for example, use of a global data area in a multitasking operating system), specify this as an implementation constraint.>

## 3.4    Communications Interfaces

<Describe the requirements associated with any communications functions required by this product, including e-mail, web browser, network server communications protocols, electronic forms, and so on. Define any pertinent message formatting. Identify any communication standards that will be used, such as FTP or HTTP. Specify any communication security or encryption issues, data transfer rates, and synchronization mechanisms.>

# 4.    System Features

<This template illustrates organizing the functional requirements for the product by system features, the major services provided by the product. You may prefer to organize this section by use case, mode of operation, user class, object class, functional hierarchy, or combinations of these, whatever makes the most logical sense for your product.>

## 4.1    System Feature 1

<Don’t really say “System Feature 1.” State the feature name in just a few words.>

4.1.1      Description and Priority

<Provide a short description of the feature and indicate whether it is of High, Medium, or Low priority. You could also include specific priority component ratings, such as benefit, penalty, cost, and risk (each rated on a relative scale from a low of 1 to a high of 9).>

4.1.2      Stimulus/Response Sequences

<List the sequences of user actions and system responses that stimulate the behavior defined for this feature. These will correspond to the dialog elements associated with use cases.>

4.1.3      Functional Requirements

<Itemize the detailed functional requirements associated with this feature. These are the software capabilities that must be present in order for the user to carry out the services provided by the feature, or to execute the use case. Include how the product should respond to anticipated error conditions or invalid inputs. Requirements should be concise, complete, unambiguous, verifiable, and necessary. Use “TBD” as a placeholder to indicate when necessary information is not yet available.>

 

<Each requirement should be uniquely identified with a sequence number or a meaningful tag of some kind.>

 

REQ-1:    

REQ-2:    

## 4.2    System Feature 2 (and so on)

# 5.    Other Nonfunctional Requirements

## 5.1    Performance Requirements

<If there are performance requirements for the product under various circumstances, state them here and explain their rationale, to help the developers understand the intent and make suitable design choices. Specify the timing relationships for real time systems. Make such requirements as specific as possible. You may need to state performance requirements for individual functional requirements or features.>

## 5.2    Safety Requirements

<Specify those requirements that are concerned with possible loss, damage, or harm that could result from the use of the product. Define any safeguards or actions that must be taken, as well as actions that must be prevented. Refer to any external policies or regulations that state safety issues that affect the product’s design or use. Define any safety certifications that must be satisfied.>

## 5.3    Security Requirements

<Specify any requirements regarding security or privacy issues surrounding use of the product or protection of the data used or created by the product. Define any user identity authentication requirements. Refer to any external policies or regulations containing security issues that affect the product. Define any security or privacy certifications that must be satisfied.>

## 5.4    Software Quality Attributes

<Specify any additional quality characteristics for the product that will be important to either the customers or the developers. Some to consider are: adaptability, availability, correctness, flexibility, interoperability, maintainability, portability, reliability, reusability, robustness, testability, and usability. Write these to be specific, quantitative, and verifiable when possible. At the least, clarify the relative preferences for various attributes, such as ease of use over ease of learning.>

## 5.5    Business Rules

<List any operating principles about the product, such as which individuals or roles can perform which functions under specific circumstances. These are not functional requirements in themselves, but they may imply certain functional requirements to enforce the rules.>

# 6.    Other Requirements

<Define any other requirements not covered elsewhere in the SRS. This might include database requirements, internationalization requirements, legal requirements, reuse objectives for the project, and so on. Add any new sections that are pertinent to the project.>

Appendix A: Glossary

<Define all the terms necessary to properly interpret the SRS, including acronyms and abbreviations. You may wish to build a separate glossary that spans multiple projects or the entire organization, and just include terms specific to a single project in each SRS.>

Appendix B: Analysis Models

## Figure 1.2 in "TABLE VRAssets"
![Image of Table_Assets](https://github.com/AmadoSuarez/AssetTracker/blob/database_joan/Table_assets.png)
 **Visit TABLE VRAssets to learn more.**
---
<Optionally, include any pertinent analysis models, such as data flow diagrams, class diagrams, state-transition diagrams, or entity-relationship diagrams.>

Appendix C: To Be Determined List

<Collect a numbered list of the TBD (to be determined) references that remain in the SRS so they can be tracked to closure.>
