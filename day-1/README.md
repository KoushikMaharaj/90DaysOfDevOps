# Introduction to DevOps

- ### What is DevOps?
  DevOps is a methodology in the software development and IT industry. Used as a set of practices and tools, DevOps integrates and automates the work of software development (Dev) and IT operations (Ops) as a means for improving and shortening the systems development life cycle.
- ### Importance/Benefits of DevOps
  - Continuous delivery of software
  - Better collaboration between teams
  - Easy deployment
  - Better efficiency and scalability
  - Errors are fixed at the initial stage
  - More security
  - Less manual intervention (which means fewer chances of error)
- ### What is Automation, Scaling, Infrastructure?

  - #### Automation in DevOps

    Automation is a critical component of DevOps. It involves automating the entire software delivery process, from code creation to testing, deployment, and monitoring. Automation enables teams to eliminate manual tasks, reduce errors, and deliver software faster.

  - #### Scaling in DevOps

    Scaling is another critical component of DevOps. It involves designing and implementing systems that can handle increased load and traffic. Scaling enables teams to deliver software that can handle a high volume of users and traffic

  - #### Infrastructure in DevOps
    Infrastructure is a key component of DevOps. It involves designing and managing the hardware and software required to run applications and services. Infrastructure can be physical, such as servers and networks, or virtual, such as cloud-based servers and networks.

- ### DevOps Life Cycles
  - #### Source Code Management
    In this phase, the business owners and software development team discuss project goals and create a plan. Programmers then design and code the application, using tools like Git to store the application code.
  - #### Continuous Build and Test
    This phase deals with building tools, like Maven and Gradle, then taking code from different repositories and combining them to build the complete application. The application is then tested using automation testing tools, like Selenium and JUnit, to ensure software quality
  - #### Continuous Integration
    When the testing is complete, new features are integrated automatically to the existing codebase
  - #### Continuous Deployment
    Here, the application is packaged after being released and deployed from the development server to the production server. Once the software is deployed, operations teams perform tasks, such as configuring servers and provisioning them with the required resources
  - #### Continuous Monitoring
    Monitoring allows IT organizations to identify issues of specific releases and understand the impact on end-users
  - #### Software Released
    After all the phases are completed and the software meets the user’s requirement, it is released into the market.
- ### Tools Required in DevOps

  1. #### Git
     Git is a distributed version control tool used to manage source code.
  2. #### Package Manager

     Package manager is a tool that helps software developers to easily share and utilise software libraries and manage dependencies. There are different package managers available in the market. Famous amongst them are:

     - maven for java
     - npm for nodejs
     - pip for python etc…

  3. #### Selenium
     Selenium is an open-source automation tool that is used to test web applications, mainly for regression and functional testing. Regression testing is the process to make sure that the older programming still works with the new changes. Functional testing ensures that the application has adequately satisfied the requirements.
  4. #### Continuous Integration tool
     CI tool helps to automate continuous development, testing, and deployment of newly created codes. Tools like Jenkins, ArgoCD, GoCD etc…
  5. #### Docker
     Docker is an OS-level virtualization software platform that enables developers and IT administrators to create, deploy and run applications and all their dependencies in a Docker container. A Docker Container is an executable package of an application and its dependencies together.
  6. #### Kubernetes (k8s)
     Kubernetes (K8s) is an open source system to deploy, scale, and manage containerized applications anywhere.
  7. #### Ansible
     Ansible is a configuration management tool allowing applications to be deployed automatically in a variety of environments.
  8. #### Monitoring tool
     Monitoring tool is used to monitor systems, servers, networks, and storage infrastructure. Tools like grafana, nagios etc…

[Next Day →](../day-2/README.md)