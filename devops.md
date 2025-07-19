# DevOps Tools - Multiple Choice Questions (MCQ)

## Table of Contents
1. [Ansible](#ansible)
2. [Puppet](#puppet)
3. [Nagios](#nagios)
4. [Terraform](#terraform)
5. [Git](#git)
6. [Maven](#maven)

---

## Ansible

### Question 1
What is Ansible primarily used for?
a) Database management
b) Configuration management and automation
c) Web development
d) Network monitoring

**Answer: b) Configuration management and automation**

### Question 2
Which file format does Ansible use for playbooks?
a) JSON
b) XML
c) YAML
d) INI

**Answer: c) YAML**

### Question 3
What is an Ansible inventory file used for?
a) Storing playbook templates
b) Defining host groups and variables
c) Logging execution results
d) Managing user credentials

**Answer: b) Defining host groups and variables**

### Question 4
Which Ansible module is used to copy files to remote hosts?
a) file
b) template
c) copy
d) fetch

**Answer: c) copy**

### Question 5
What does "idempotent" mean in the context of Ansible?
a) Operations can be performed only once
b) Operations produce the same result regardless of how many times they're executed
c) Operations must be performed in a specific order
d) Operations require administrator privileges

**Answer: b) Operations produce the same result regardless of how many times they're executed**

### Question 6
Which command is used to run an Ansible playbook?
a) ansible-run
b) ansible-play
c) ansible-playbook
d) ansible-execute

**Answer: c) ansible-playbook**

### Question 7
What is an Ansible role?
a) A user permission level
b) A reusable collection of tasks, variables, and handlers
c) A type of inventory file
d) A network protocol

**Answer: b) A reusable collection of tasks, variables, and handlers**

### Question 8
Which Ansible module is used for package management on Ubuntu/Debian systems?
a) yum
b) apt
c) package
d) dnf

**Answer: b) apt**

---

## Puppet

### Question 9
What language is primarily used to write Puppet manifests?
a) Ruby
b) Python
c) Puppet DSL (Domain Specific Language)
d) JavaScript

**Answer: c) Puppet DSL (Domain Specific Language)**

### Question 10
What is the default port for Puppet Master?
a) 8080
b) 8140
c) 9090
d) 443

**Answer: b) 8140**

### Question 11
In Puppet, what is a "catalog"?
a) A list of available modules
b) A compiled set of resources for a specific node
c) A user manual
d) A backup configuration

**Answer: b) A compiled set of resources for a specific node**

### Question 12
Which Puppet resource type is used to manage files?
a) package
b) service
c) file
d) user

**Answer: c) file**

### Question 13
What is Facter in Puppet?
a) A testing framework
b) A system inventory tool that gathers facts about nodes
c) A deployment tool
d) A monitoring service

**Answer: b) A system inventory tool that gathers facts about nodes**

### Question 14
Which command is used to apply Puppet manifests locally?
a) puppet run
b) puppet execute
c) puppet apply
d) puppet deploy

**Answer: c) puppet apply**

### Question 15
What is PuppetDB used for?
a) Storing user credentials
b) Storing catalogs, facts, and reports
c) Managing puppet modules
d) Network configuration

**Answer: b) Storing catalogs, facts, and reports**

### Question 16
In Puppet, what does "ensure => present" typically mean?
a) The resource should be created if it doesn't exist
b) The resource should be deleted
c) The resource should be backed up
d) The resource should be monitored

**Answer: a) The resource should be created if it doesn't exist**

---

## Nagios

### Question 17
What type of monitoring system is Nagios?
a) Log management
b) Network and infrastructure monitoring
c) Code quality analysis
d) Database performance monitoring

**Answer: b) Network and infrastructure monitoring**

### Question 18
What is the main configuration file for Nagios Core?
a) nagios.ini
b) nagios.conf
c) nagios.cfg
d) nagios.config

**Answer: c) nagios.cfg**

### Question 19
Which Nagios state indicates that a service is functioning normally?
a) WARNING
b) CRITICAL
c) OK
d) UNKNOWN

**Answer: c) OK**

### Question 20
What is NRPE in Nagios?
a) Nagios Remote Plugin Executor
b) Network Resource Performance Evaluator
c) Node Reporting and Processing Engine
d) Notification and Reporting Protocol Extension

**Answer: a) Nagios Remote Plugin Executor**

### Question 21
Which file format is used for Nagios configuration files?
a) JSON
b) XML
c) Plain text with specific syntax
d) YAML

**Answer: c) Plain text with specific syntax**

### Question 22
What is the purpose of Nagios plugins?
a) To extend the web interface
b) To perform actual monitoring checks
c) To manage user accounts
d) To handle database connections

**Answer: b) To perform actual monitoring checks**

### Question 23
Which Nagios object is used to define what to monitor?
a) Host
b) Service
c) Contact
d) All of the above

**Answer: d) All of the above**

### Question 24
What does NSClient++ do in a Nagios environment?
a) Provides Linux monitoring capabilities
b) Enables Windows monitoring
c) Manages network switches
d) Handles email notifications

**Answer: b) Enables Windows monitoring**

---

## Terraform

### Question 25
What type of tool is Terraform?
a) Configuration management
b) Infrastructure as Code (IaC)
c) Continuous integration
d) Container orchestration

**Answer: b) Infrastructure as Code (IaC)**

### Question 26
Which language does Terraform use for configuration files?
a) JSON
b) YAML
c) HCL (HashiCorp Configuration Language)
d) XML

**Answer: c) HCL (HashiCorp Configuration Language)**

### Question 27
What file extension do Terraform configuration files typically use?
a) .tf
b) .terraform
c) .hcl
d) .config

**Answer: a) .tf**

### Question 28
Which command is used to initialize a Terraform working directory?
a) terraform start
b) terraform init
c) terraform begin
d) terraform setup

**Answer: b) terraform init**

### Question 29
What does "terraform plan" do?
a) Creates infrastructure
b) Destroys infrastructure
c) Shows what actions Terraform will take
d) Validates configuration syntax

**Answer: c) Shows what actions Terraform will take**

### Question 30
Where does Terraform store state information by default?
a) In the cloud provider
b) In a local file called terraform.tfstate
c) In a database
d) In memory only

**Answer: b) In a local file called terraform.tfstate**

### Question 31
What is a Terraform provider?
a) A hosting service
b) A plugin that enables interaction with APIs of cloud providers
c) A user account
d) A configuration template

**Answer: b) A plugin that enables interaction with APIs of cloud providers**

### Question 32
Which command applies Terraform configuration changes?
a) terraform execute
b) terraform run
c) terraform apply
d) terraform deploy

**Answer: c) terraform apply**

---

## Git

### Question 33
What type of version control system is Git?
a) Centralized
b) Distributed
c) Local only
d) Server-based

**Answer: b) Distributed**

### Question 34
Which command is used to create a new Git repository?
a) git create
b) git new
c) git init
d) git start

**Answer: c) git init**

### Question 35
What does "git clone" do?
a) Copies files locally
b) Creates a backup
c) Creates a local copy of a remote repository
d) Duplicates a branch

**Answer: c) Creates a local copy of a remote repository**

### Question 36
Which command shows the current status of the working directory?
a) git info
b) git status
c) git state
d) git check

**Answer: b) git status**

### Question 37
What does "git add ." do?
a) Adds all changes to the staging area
b) Creates a new branch
c) Commits all changes
d) Pushes changes to remote

**Answer: a) Adds all changes to the staging area**

### Question 38
Which command is used to create and switch to a new branch simultaneously?
a) git branch -new
b) git checkout -b
c) git switch -create
d) git branch -switch

**Answer: b) git checkout -b**

### Question 39
What does "git merge" do?
a) Splits a branch
b) Combines changes from different branches
c) Deletes a branch
d) Renames a branch

**Answer: b) Combines changes from different branches**

### Question 40
Which file is used to specify files that Git should ignore?
a) .gitignore
b) .ignore
c) gitignore.txt
d) .git-exclude

**Answer: a) .gitignore**

---

## Maven

### Question 41
What is Apache Maven primarily used for?
a) Web server management
b) Java project build management and dependency management
c) Database administration
d) Network monitoring

**Answer: b) Java project build management and dependency management**

### Question 42
What is the name of Maven's main configuration file?
a) build.xml
b) maven.xml
c) pom.xml
d) config.xml

**Answer: c) pom.xml**

### Question 43
What does POM stand for in Maven?
a) Project Object Model
b) Package Object Manager
c) Project Organization Model
d) Program Object Module

**Answer: a) Project Object Model**

### Question 44
Which Maven command compiles the source code?
a) mvn build
b) mvn compile
c) mvn make
d) mvn run

**Answer: b) mvn compile**

### Question 45
What is Maven's default directory structure for source code?
a) src/java
b) source/main
c) src/main/java
d) main/src/java

**Answer: c) src/main/java**

### Question 46
Which Maven phase runs unit tests?
a) compile
b) test
c) verify
d) validate

**Answer: b) test**

### Question 47
What is a Maven repository?
a) A code versioning system
b) A storage location for project artifacts and dependencies
c) A testing framework
d) A deployment server

**Answer: b) A storage location for project artifacts and dependencies**

### Question 48
Which command creates a new Maven project from an archetype?
a) mvn create
b) mvn new
c) mvn archetype:generate
d) mvn project:create

**Answer: c) mvn archetype:generate**

### Question 49
What is the Maven Central Repository?
a) A local storage for projects
b) A default remote repository containing common libraries
c) A backup system
d) A development environment

**Answer: b) A default remote repository containing common libraries**

### Question 50
Which Maven command packages the compiled code into a distributable format?
a) mvn build
b) mvn package
c) mvn deploy
d) mvn install

**Answer: b) mvn package**

---

## Answer Key Summary

| Question | Answer | Question | Answer | Question | Answer | Question | Answer |
|----------|--------|----------|--------|----------|--------|----------|--------|
| 1 | b | 13 | b | 25 | b | 37 | a |
| 2 | c | 14 | c | 26 | c | 38 | b |
| 3 | b | 15 | b | 27 | a | 39 | b |
| 4 | c | 16 | a | 28 | b | 40 | a |
| 5 | b | 17 | b | 29 | c | 41 | b |
| 6 | c | 18 | c | 30 | b | 42 | c |
| 7 | b | 19 | c | 31 | b | 43 | a |
| 8 | b | 20 | a | 32 | c | 44 | b |
| 9 | c | 21 | c | 33 | b | 45 | c |
| 10 | b | 22 | b | 34 | c | 46 | b |
| 11 | b | 23 | d | 35 | c | 47 | b |
| 12 | c | 24 | b | 36 | b | 48 | c |
| | | | | | | 49 | b |
| | | | | | | 50 | b |

---

*This study guide covers fundamental concepts and common scenarios for each tool. Practice with hands-on experience is recommended alongside studying these questions.*
