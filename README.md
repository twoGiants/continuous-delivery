# Continuous Delivery

This is a book summary.

## Chapter 1 The Problem of Delivering Software

Antipattern: Deploying to prod after development is complete. (p. 7)
> **Note:** Integrate testing, deployment, and release activities into the development process. (p. 9)

Antipattern: Manual configuration of prod environmants. (p. 9)
> **Note:** It should not be possible to make manual changes to testing, staging and production environments. Only through an automated process. (p. 10)

## Chapter 2 Configuration Management

_Keep absolutely everyhting in version control:_

- Developers: besides code, tests, database scripts, build and deployment scripts, docs, libraries, config files for app and compiler, collection of tools.
- Ops: info needed to re-create test and prod environments, software stack, OS, DNS zone files, firewall config, etc.
- Analysts: requirements documents.
- Testers: test scripts and procedures.
- Project Managers: release plans, progress charts, risk logs.
- Every member: any file or document related to the project. (p. 33)

In addition to source code and configuration information some store binary images of:

- application servers,
- compilers,
- virtual machines,
- other parts of their toolchain. (p. 34)

Don't keep the binary output of your applications compilation in version control. (p. 35)

### Trunk Based Development

To ensure you don't break the application:

- _First:_ run a commit test suite before each check-in.
- _Second:_ introduce changes incrementally.

Check-in after each incremental change or refactoring => at the very minimum once a day or several times a day. (p. 37)

### Dependencies

Keep a copy of external libraries (and images; added by me) locally or close to be able to reproduce the build. (p. 38)

### Managing Configuration

Treat configuratino of your system the same way you treat you code: Make it subject to proper management and testing. (p. 39)

Everythin that changes between deployments is configuration and should not be baked in or packaged. (p. 42)

Provide configruation information for all applications and environments through the same mechanism. (p. 42)

Keep configuration information specific to each fo your environments in a repository separate from your source code. Keep only the configuration options for your application in the same repository. (p. 43)

### Accessing Configuration

Best is a central service. You can alos use a REST API. (p.44)

### Modeling Configuration

tba

### Testing System Configuration

tba
