<img style="width:100%;" src="images/datasecurity-main.png">

What is InsightLake Data Security?
-----------
Enterprises today are storing large amount of data in data lakes and data stores to gain insights. At the same time regulations like GDPR, Sarbanes-Oxley, HIPAA, Basel III are forcing companies to protect sensitive data sets and conduct regular audits. Non compliance can lead to legal action, reputation damage and business loss.

This poses a big challenge for enterprises to manage data access security and data loss in a central and easy manner.

<img style="width:100%;" src="images/datasecurity.png">

Insight Lake Security Manager solves this problem by allowing companies to manage security and monitoring of data assets (files, databases), which are present in cloud or on-premise centrally. It enables security administrators to discover datasets, profile to find sensitive information and define access policies easily with rich set of rules. It allows seamless migration by not requiring any change in existing applications and tools. It captures comprehensive audit logs to provide great detail about the access.

### Discover --> Profile Sensitive Info --> Enforce Access & Protection Policies

## Following are the main features provided by Security Manager:

* Discover data assets continuously and identify gaps and sensitive information
* DCAP - Data Centric Audit & Protection
* Cloud (AWS, GCP, Azure) and on-premise support
* Protection for many data assets relational DBs, File systems, Hadoop, MPP DBs etc.
* Monitor access rights regularly
* Monitor queries and alerting based on policies
* Protect data assets by modifying queries or blocking access
* Protect unstructured data and mask/obfuscate sensitive information on Docs (PDF, Word, Text), Images etc.
* Apply ML/DL models to discover information
* Integration with metadata and governance policies
* Using APIs and workflow tokenize data (One way hash, FPE - Format preserving encryption)
* Comprehensive audit logs
* Integration with external SEIMs like Splunk, LogRythm, InsightLake Cyber Security
* Integration with Sentry & Ranger

## Supported Data Assets - Cloud & On-Premise
Security Manager solution allows companies to monitor and protect variety of data assets. Following data areas are protected.

* Database
* Files
* Big Data
* SAS - Software-as-a-Service
* IAAS - Infrastructure-as-a-Service

<img style="width:100%;" src="images/datasecurity-scope.jpeg">

* Hadoop Distributions - Cloudera (CDH), Hortonworks (HDP), MapR, EMR
* Relational Databases - MySQL, Oracle, PostgreSQL
* File System - S3, GCS, Azure Blob, HDFS
* Hadoop Data Store - Hive, Impala, SparkSQL, SOLR
* MPP Databases - Redshift, Big Query, Vertica, Teradata

## Discover Sensitive Information
Security Manager solution provides asset discovery feature, which identifies what types of data stores present in a given network. Rich data profiling of data sets provides fine grain details about the sensitivity of data elements. Discovery feature allows creation of security policies for identified sensitive data elements like alerting, masking, blocking etc. Data discovery can be easily automated to provide continuous monitoring of sensitive elements.

## Data Discovery
Periodic jobs to automatically discover data assets

## Data Profiling
Ad-hoc and periodic jobs to profile data store and identify sensitive information.

## Logical Data Types

* BASIC - Name, Email Address, Phone, SSN
* PCI - Credit Card

## Compliance Domains

* BASIC
* GDPR
* PCI
* HIPAA

## Central Policy Manager

<img style="width:100%;" src="images/policy-tab/data-location-policy.png">

Security Manger provides an interactive policy manager UI, which allows security admins to manage enterprise data assets from one place. They can explore data assets, monitor them, create policies, check audit logs and see dashboards.

## Applications and data domains
Security Manager integrates with Metadata and Governance solutions and provides insights through a hierarchy of business unit, application, data domain and user.

## Manage users

<img style="width:100%;" src="images/setting-tab/user-page.png">

Security Manager allows companies to import or provision users manually. Users can be easily imported from AD systems. AD integration allows automatic policy handling for users who are removed from AD on their termination.

## Monitor Access Rights
Security Manager allows security admins to monitor user access rights based on user roles. It allows them to identify if excess rights are given to a user whose role doesn't permit them. For example a developer is given drop table rights on production will be a security gap. Monitoring of access rights can be done periodically and alerts could be provisioned. From the interactive UI and dashboards security admins can monitor and explore access rights easily.

## Security Agents
Security agents are the main actors, they load policies from central policy server, monitor traffic, apply policies, generate alerts, modify queries for data protection and block access.

<img style="width:100%;" src="images/agent-tab/agent-page.png">

Security agents are divided in two types:

### Monitoring Agent
These agents listen to the data access traffic in sniffing mode and apply policies to generate alerts and audit logs. They can't block the data connection or modify queries.

### Proxy Agent
These agents sits in middle of the traffic, they apply policies to alert, generate audit logs, block access and modify queries.

## Security Policies - Monitor & Protect
Enterprises can utilize rich set of policy rules to control access to data. Rules include: Coarse Grain Permissions - allow, deny Allow or deny data set joins Fine grain masking Data filtering Location Based Access Metadata Attributes

## Rich Rules
Enterprises can utilize rich set of policy rules to control access to data. Rules include:

<img style="width:100%;" src="images/policy-tab/data-location-policy.png">

* Coarse Grain Permissions - allow, deny
* Allow or deny data set joins
* Fine grain masking
* Data filtering
* Location Based Access
* Metadata Attributes

## Comprehensive Audit
Security manager captures provides comprehensive audit of data assets as well operational policies. It provides :

<img style="width:100%;" src="images/audit-tab/audit-page.png">

Data access logs - captures details about user, data store, location, time, original query and modified queries by policies.
Policy changes logs - captures user, time and policy changes

Audit logs can be pushed to an enterprise based event handling systems or exported to big data based systems.


## Data Protection APIs & Workflow
Protect your data using DLP APIs to mask or encrypt in real time or batch mode. Security manager provides tokenization features to encrypt data using one way hash or FPE (Format Preserving Encryption).

## Security Dashboards

<img style="width:100%;" src="images/security-dashboard-page.png">

Analyze and monitor all enterprise data assets using security dashboards

Following dashboards are provided:

Agents Dashboard
How agents are performing - number of connections, requests
Uptime
CPU, Memory
Access Rights Dashboard
Number of roles assigned, approved, rejected, in review
Dormant users
Users with direct access
Permissions distribution by users
Top users with more rights
User Access Dashboard
User requests
Top users
Access by location, time, IP, OS, Source, application, user group
AD Login/Logout
Top data stores with many access, users
Top data stores access which are most dormant
Queries Dashboard
Requests - hourly, weekday, weekly distributions
Top queries
Query type distributions
Sensitive queries - count, who queried, time, what db etc..
Number of records in response
Admin Dashboard
Type of admin queries - create, modify, drop etc
Sensitive queries - drop and truncate
Schema changes
Other governance activities

To learn more, check out [http://insightlake.com/data-security.html](http://insightlake.com/data-security.html)

## Endpoints
<img style="width:100%;" src="images/monitor-tab/endpoint-page.png">

## Assign Policy
<img style="width:100%;" src="images/assign-policy-tab/assign-policy.png">

## Onboard 
<img style="width:100%;" src="images/onboard-tab/onboard-page.png">


Installation
------
* Download or clone the repository. 
* Run bin/insightlake command.
* Open browser with URL as http://localhost:8080/
* Change configuration in /conf folder to set different ports
* By default H2 database is used, you can change the database details in jdbc.properties file

Installation using docker 
------
* Download or clone the repository. 
* cd /docker
* Run `docker-compose -f docker-compose.yaml up --build`
* Open browser with URL as http://localhost:8080/
* While creating Data Location use below credentials  

        * username : root
        * password : password
        * URL :  jdbc:mysql://mysql:3306/


License
------
InsightLake Data Security is a commercial product but distributed to be used freely. Please contact contact@insightlake.com for details.

Getting Help
----------

You can get help easily :
Community - Google Groups
Slack Channel
Twitter
Facebook
Email: contact@insightlake.com
