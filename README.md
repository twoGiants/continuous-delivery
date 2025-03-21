# Continuous Delivery

This is a book summary.

## Chapter 1 The Problem of Delivering Software

Antipattern: Deploying to prod after development is complete.
> **Note:** Integrate testing, deployment, and release activities into the development process.

Antipattern: Manual configuration of prod environmants.
> **Note:** It should not be possible to make manual changes to testing, staging and production environments. Only through an automated process.

## Chapter 2 Configuration Management

_Keep absolutely everyhting in version control:_

- Developers: besides code, tests, database scripts, build and deployment scripts, docs, libraries, config files for app and compiler, collection of tools.
- Ops: info needed to re-create test and prod environments, software stack, OS, DNS zone files, firewall config, etc.
- Analysts: requirements documents.
- Testers: test scripts and procedures.
- Project Managers: release plans, progress charts, risk logs.
- Every member: any file or document related to the project.

In addition to source code and configuration information some store binary images of:

- application servers,
- compilers,
- virtual machines,
- other parts of their toolchain.

Don't keep the binary output of your applications compilation in version control.

### Trunk Based Development

To ensure you don't break the application:

- _First:_ run a commit test suite before each check-in.
- _Second:_ introduce changes incrementally.

Check-in after each incremental change or refactoring => at the very minimum once a day or several times a day.

