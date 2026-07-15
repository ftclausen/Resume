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
* **Inter Team Conventions** - I try to establish a "paved road" that can make the lives of developers easier so they
    can focus on their value add. For example: shared CI/CD libraries/GitHub actions.

## A note on AI / LLM / ML

Since the advent of generative AI, I now use AI or ML of some kind in most of the topics in the rest of this resume.
Rather than mention it in each section, here are some examples:

* Code generation with agents like Claude Code, OpenCode, GitHub Copilot CLI
* Providing tools (direct and via MCPs) for agents to use to inspect (read-only) the state of a system when exploring or
  troubleshooting.
* Use ML tools like word embeddings to triage log files more quickly. I.e. find related log entries to give more context.
* Adversarial code reviews between multiple LLMs to produce better quality work before the first human gets to look at a
  PR.
* Selecting the best model for the job i.e. summarisation and basic exploration with smaller models and deep
  troubleshooting with larger models. Same criteria for multi-agent systems like oh-my-opencode

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
       * Gradle - Single step builds managing all dependencies automatically.
    * Configure above job runners to give enough information to developers for self-help troubleshooting
    * Empower developers to take ownership of their pipelines

### Infrastructure Code

* AWS CDK (Cloud Development Kit) - Define infrastructure, usually in Typescript or Python to manage software stacks
  from within the application's repo
* Terraform - Define infrastructure with declarative Terraform, usually for shared infrastructure not specific to a
  single project.

### Software Development

My main software development efforts have been support CI/CD, infra code, and modifying applications/services for
deployment, observability or to improve reliability. I use whichever language the project calls for; most of my
experience has been with:

- Java and Groovy: Gradle, Jenkins, and Java based applications
- Python: AWS Cloud Development Kit (CDK) code, Python based microservices
- Typescript: Custom GitHub actions, AWS CDK
- Ruby: Chef code

And, of course, Bash which is ubiquitous. Everything from quick command-line loops to custom deployment wrappers
performing the "last mile" of customisation.

#### Testing

I always try and write my code to testable whether it is for Infra or a running service. I usually use what is common
for a given language e.g.  Junit (Java), Spock (Groovy), RSpec (Ruby).

### Observability

* Grafana and Prometheus for mostly Kubernetes related deployments
* AWS CloudWatch for native AWS services
* New Relic for application specific insights
* Experience with older tools like Nagios, RRDTool, Cacti, etc.

### Container Orchestration

This pervades the topics above and touches product life-cycles from local testing all the way through to production.

* Local
  * Plain Docker for quick testing
  * Docker compose and local K8s stacks for more complete testing but with a quick feedback loop.
* CI/CD
  * Jenkins pipelines backed by elastic Kubernetes instances on AWS EKS (Elastic Kubernetes Service)
  * Longer lived developer deployments to demo and QA
* Deployment environments
  * In addition to Kubernetes, using services like AWS ECS (Elastic Container Service) for prod deployments

And common build pipelines using CDK or a common container build job to make images available for deployments.

### Performance

Getting an app deployed is no good if it does not perform. My main avenues for investigating perf issues are:

* JVM metrics such as Garbage Collection, heap usage, etc.
* Services like New Relic to look for longer term trends and comparisons
* Built-in metrics that AWS provide and creating dashboards for easy review
* System metrics like IO wait, memory, CPU usage.

Some exposure to modifying Java apps to use finer grained locking (e.g. striped locking) and avoiding locks where possible e.g.
checking caches first prior to trying to lock.

### Version Control Systems

Git is an integral part to all of the above and a core part of my day-to-day work.

### Databases

* AWS RDS - Provision below database engines in AWS via Terraform or CDK with sensible alerting.
* PostgresSQL & MySQL - Installation, user creation, backup & recovery, replication, clustering
* SQL - SQL queries focused on monitoring and troubleshooting.

### Identity and Service Providers

I have mostly configured these for internal use by QA teams:

* Shibboleth IdP
* Shibboleth SP (Service Provider) with Apache and custom SP tools
* Central Authentication Service (CAS)
* OpenLDAP as a backing source of identity details

### Networking

Understanding of networking fundamentals such as:

* TCP/IP theories and configuration
* OSI Model
* Knowledge of switching concepts like VLANs
* General understanding of routing protocols
* VPN - OpenVPN, Linux IPsec (Kame + Racoon)
* Firewalls - Packet filtering
* Network audits with Nmap.
* OpenSSL - Create and inspect certificates
* DHCP
* DNS servers like dnsmasq and Bind
* Network file systems like NFS, CIFS (SMB)

### Storage

#### AWS

* Elastic Block Store
* Storage Gateway
* S3

#### Linux

* RAID Concept
* Linux software raid
* Linux Logical Volume Manager (LVM)

### OS Experience

I find the command-line most comfortable (and enjoyable) and mostly work in Unix-like environments. Specifically, every service I work on
runs in a Linux-derived runtime of some sort. I am also familiar with Linux base level services like systemd, legacy
init, PAM, etc.

## Spoken languages

* English - Native speaker
* Dutch - Conversational speaker

## Experience

### Blackboard

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

