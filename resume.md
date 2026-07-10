# Friedrich "Fred" Clausen
## Contact Details

* Traditional
    * <ftclausen@gmail.com>
* Online Identities
    * [Github](https://github.com/ftclausen) (https://github.com/ftclausen)
    * [LinkedIn](http://www.linkedin.com/in/friedrichclausen) (http://www.linkedin.com/in/friedrichclausen)
    * [ServerFault](http://serverfault.com/users/127243/fred-clausen) (http://serverfault.com/users/127243/fred-clausen)
    * [SuperUser](http://superuser.com/users/164635/fred-clausen) (http://superuser.com/users/164635/fred-clausen)
    * [StackOverflow](http://stackoverflow.com/users/1300307/fred-clausen) (http://stackoverflow.com/users/1300307/fred-clausen)
    * [Math StackExchange](https://math.stackexchange.com/users/109665/friedrich-fred-clausen) (https://math.stackexchange.com/users/109665/friedrich-fred-clausen)

## What I Can Offer

I love enabling productivity. For example:

- Giving developers solid, continuous pipelines to see their work build and
deployed with low friction. Modifying products to support these goals as needed.
- Giving first-responders consistently deployed infra with enough observability (but not too much) to get to the bottom of issues quickly.
- Contributing to SRE efforts to bring software engineering rigour to infrastructure management e.g. quick
feedback during dev, testing, keep things DRY, APIs first, and having awareness of the full stack from OSI layer 1 to 7
- Thus enabling customers to have highly available and performant platforms to get their work done.

I enjoy working at the interfaces between domains.

## Proficiency Summary

My proficiencies cover the following areas (see following sections for more details)

* **Development productivity/Support** - Contributing to build engineering tasks such as
    build system code, build job runners, and Continuous Integration (CI)
    systems management.
* **Infrastructure Code and Orchestration** - A combination of configuration management and tool
    development in various languages to support 
    automated infrastructure and application management. This includes using
    container orchestration tools like Kubernetes (K8s) combined with AWS CDK (mainly Typescript and Python) and/or Terraform.
* **Application Administration** - Supporting applications with regard to
    provisioning, performance tuning, observability, and troubleshooting using metrics and log analysis.
* **Systems Administration and Networking** - While classic "System Administration" has been supplanted (for the
better) by SRE and similar, the infrastructural lessons I learned there serve me well. That experience enables me to
quickly hone in on potential areas of investigation or how a stack might fit together. As well has handy troubleshooting
skills like packet sniffing and strace.

## A note on 
## Proficiency Details

### Continuous Integration / Continuous Deployment (CI/CD)

This overlaps somewhat with the developer productivity sphere and my main areas has been:

* **Job Runners**
    * Jenkins - Fully automated, version controlled Jenkins management using Kubernetes compute for jobs
        * Docker containers defined in Git to manage versioning and plugin installation. No manual plugin installs.
        * JobDSL to define the creation and structure of jobs (e.g. parameters, schedule, etc)
        * Per-project, in-repo Jenkinsfiles (mainly Groovy based) to define job logic specific to each project
        * Organisation shared libraries (Groovy) for certain common operations (e.g. scheduling JNLP pods)
    * GitHub Actions
        * Create custom actions for PR hygiene e.g. check for tickets, branch age, etc.
        * Per-project workflows for building, publishing, tests and so on
    * AWS CodePipeline/CodeBuild
        * Define buildspec.yaml files to perform similar tasks to GitHub workflows
* **Developer productivity**
    * Build Systems
       * Gradle - Single step 

### Infrastructure Code

    * AWS CDK (Cloud Development Kit) - Define infrastructure, usually in Typescript or Python to manage software stacks
      from within the application's repo
    * Terraform - Define infrastructure with declarative Terraform, usually for shared infrastructure

### Software
    * Scripting - I have used the languages below for areas such as configuration management, 
                  general automation and monitoring.
        * Bash
        * Ruby
        * Python
        * Perl
    * Groovy - Used in the context of Gradle
    * Java - I have written small Java services for "glue" integration services
        and also modest product contributions to support better build
        integration.
    * Testing - Unit tests JUnit in the context of Groovy and Java

* **Containers and Container Orchestration**
    * Containers - Create, update and run Docker containers mostly in the
        context of continuous integration and deployment. Create and maintain
        tooling to streamline and automate container creation tailored to
        support development workflows.
    * Orchestration - Define deployment specs for Kubernetes and Mesos/Marathon
        to support both building, testing and deploying applications.
    * CI/CD - Integrate container creation and deployment with Jenkins to fully
        automate building, testing and deployment when code is committed to
        revision control.

* **Configuration Management** - I am using configuration management to affect fully
                                 automatic and consistent environments. This
                                 allows me to manage systems and applications at
                                 scale.
    * General - Working with other departments on a common code base - deciding
                conventions and areas of responsibility. Writing documentation
                and providing internal training for colleagues.
    * Chef - Create/manage cookbooks, create data bags, custom Ohai plugins,
             environment management, converting legacy scripts into
             Cookbooks, Chef server and client management, node bootstrap.
    * Puppet - Create/manage modules, create and use Facter facts, Puppet server
               and node services, node bootstrap. 

* **Version Control Systems** 
    * Git - Configuration management repositories, in-house code
            repositories.
    * Subversion - Checkout and build legacy code bases.


* **Testing**
    * Configuration management
        * Unit Testing - Chefspec and Rspec
        * Integration Testing - Test Kitchen with Serverspec

### Application Administration

* **Java**
    * JVM - Installation, upgrade considerations and tuning for the type of application.
    * Tomcat - Web application deployment, security and integration with other
middleware.
    * ActiveMQ - Installation, tuning and troubleshooting.

* **Supporting Services and Tools**
    * Apache - Integration with backend apps, tuning and security.
    * Authentication - LDAP, Shibboleth (SAML2) single-sign-on
    * Package Management - Red Hat (RPM) and Debian (.deb) packages
    * Documentation
        * Wiki based, e.g. Atlassian Confluence, MediaWiki.
        * Markdown documents.
        * Diagrams - OmniGraffle, ASCII generators for simple diagrams close to code, Cloud tools like Miro

* **Databases**
    * AWS RDS - Provision below database engines in AWS via Terraform or CDK with sensible alerting.
    * PostgresSQL - Installation and configuration
    * MySQL - Installation, user creation, backup & recovery, replication, clustering
    * Oracle - Installation, configuration and tuning of SGA sizes. Alert log monitoring.
    * SQL - SQL queries focused on monitoring and troubleshooting.

* **Monitoring and Metrics**
    * Prometheus - Kubernetes metrics auto-discovery, custom scraping configuration
    * JMX - Monitor with some kind of intermediate layer like Prometheus JMX exporter or Jmxterm
    * Other legacy/specialised - Nagios, SNMP, Cacti, Munin.
    * Ad-Hoc experiments with RRDTool

### Systems Administration and Networking

* **Unix-like Systems**
    * Linux - Red Hat, Debian, Ubuntu
    * Solaris
    * BSD - OpenBSD, FreeBSD
    * OS X
* **Security**
    * VPN - OpenVPN, Linux IPsec (Kame + Racoon)
    * Firewalls - IPtables and OpenBSD packet filter
    * Implement security best practices
    * Network audits with Nmap.
    * OpenSSL - Create and inspect certificates
    * Linux PAM
* **Networking**
    * OSI Model understanding
    * TCP/IP theories and configuration
    * Basic Cisco IOS usage
    * Knowledge of switching concepts (VLANs and spanning tree)
    * General understand of routing protocols.
* **Virtualisation**
    * Xen - Red Hat and Citrix
    * VMware
    * VirtualBox
* **High-availability**
    * LVS (Linux Virtual Server) Loadbalancer
    * Heartbeat
* **Systems Provisioning**
    * Red Hat kickstart
    * Debian FAI
* **File Serving**
    * NFS
    * CIFS (Samba)
    * Webdav
* **Storage**
    * RAID Concepts and configuration on common controllers
    * Linux software raid
    * Linux Logical Volume Manager (LVM)
    * Disk encryption with LUKS
* **Commonly Run Services**
    * DNS - ISC Bind
    * OpenSSH
    * DHCP - ISC dhcpd

## Spoken languages

* English - Native speaker
* Dutch - Conversational speaker

## Experience

### Anthology (Formerly Blackboard)

#### Platform Engineer, CI/CD, Infra as Code (Staff Platform Engineer) - January 2020 to Present
Location: Remote in NSW, Australia

Work on projects to streamline our infrastructure, applications, and processes to not only automate but view our platform and applications as single system. Thus:

 - Everything is API first
 - In keeping with the above point, modify our core applications to better support automation
 - Use AWS and other facilities where appropriate, we want to differentiate in our app not reinvent the wheel
 - Deploy Infrastructure with awareness of other systems and APIs. Use AWS CDK and Terraform to define all infrastructure thus ensuring we have controlled release, accountability, and change history.

In addition to the above:

- Maintain our CI/CD infrastructure consisting of Jenkins code (JobDSL, Jenkinsfile Groovy DSL)
- Maintain Gradle based build systems (Groovy based)
- Handle SRE related escalations

#### Build and Release Engineer - October 2015 to January 2020
Location: Remote in NSW, Australia

In this role I'm working to 

Infrastructure:

* Deploy Microservices via AWS CDK (Cloud Development Kit)
* Migrate Microservices from Terraform to AWS CDK
* Deploy Microservices via Terraform

CI/CD Tasks:

* Extend our existing Gradle build system
* Ensure reproducible builds
* Use container orchestration tools like Kubernetes to deploy services
* Support the Jenkins pipeline and integrate with Kubernetes for scalable builds
* Create releases

#### Infrastructure Automation Developer - October 2014 to Present
Location: Sydney, Australia

In my role as an Automation Developer I am responsible for writing 
infrastructure (and supporting) code to allow Blackboard to fully 
automatically deploy our product offerings on both public cloud providers
such as AWS as well as private cloud environments running on Openstack.

This role also encompassed build engineering tasks such as implementing
Gradle build system code (build file DSL and Gradle plugins) as well as
modifying the main product (Java) to support semantic versioning.

#### Web Applications Administrator - July 2011 to October 2014
Location: Amsterdam, The Netherlands

As a Web Applications Administrator in the Web Tech team my 
responsibilities include ensuring the stability and performance 
of the Blackboard Managed Hosting applications; this involves 
tasks such as tuning and root cause analysis.

My other responsibilities revolve around improvement initiatives
primarily focussed on improving the level of automation within the
managed hosting departments.

### Marktplaats/eBay
#### Systems/Applications Administrator (Freelance) - March 2010 to May 2011
Location: Amsterdam, The Netherlands

Together with the rest of the site operations team I was responsible for 
ensuring the availability and performance of the Marktplaats, an eBay subsidiary, 
web applications. Additionally I worked embedded within a development team to 
provide operations support for the development efforts. Such as managing the test
infrastructure, setting up monitoring, interfacing with the operations/networking
departments and production deployments.

### IPSoft
#### Systems Administrator - April 2009 to March 2010
Location: Amsterdam, The Netherlands

My responsibilities at IPSoft were to provide systems administration services
to the client base, both on-site and remotely, while actively working to refine 
existing processes and knowledge with regards to the management of client systems

### TomTom
#### Systems Administrator (Freelance) - February 2008 to April 2009
Location: Amsterdam, The Netherlands

At TomTom I was the infrastructural lead on projects, which entailed 
working with both the development and operational teams, to ensure 
a smooth transitioning from a project in development to a production service.

### Telfort (formerly Tiscali) Internet
#### Systems Administrator (Initially freelance then permanent) - March 2005 to December 2007
Location: Utrecht, The Netherlands

Here I was part of the team managing the core ISP infrastructure and 
also taking on improvement initiatives to further the level of automation
and systems consistency.

### New Zealand Holiday - August 2004 to March 2005
Extended backpacking trip to New Zealand. 

### Xinit Systems
#### Professional Services Engineer - July 2003 to August 2004
Location: London, UK

My responsibilities were providing professional Linux support 
services to customers and also managing the Xinit internal 
infrastructure.

### Unique Broadcasting Company
#### System Administrator - November 2001 to June 2003
Location: London, UK

I supported the backend servers powering their digital radio
support services. I also worked with the development team to
manage their testing infrastructure and ensure smooth production 
deployments.

### Frontwire Ltd.
#### Systems Administrator - January 2001 to July 2001
Location: London, UK

At Frontwire I was the backend systems administrator and 
also supported the employee workstations.

### Red Hat Europe
#### Linux Technical Support - June 2000 to November 2000
Location: Guildford, UK

I provided first line technical support for Red Hat Linux
which entailed helping customers install and use the product.

