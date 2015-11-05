# Replicate Seed Data Program
[source](http://oracleebslearning.blogspot.com/2012/10/replicate-seed-data.html)

**What are the system wide consequences of running the concurrent program Replicate Seed Data and is it safe to run?**  
**What Effects Does Replicate Seed Data Concurrent Request Have On Oracle Applications?**

**Answer:**  
The purpose of the Replicate Seed Data Concurrent Program is to populate the Installed modules seeded values, so that new organizations can use the seeded data.

Whenever new Organizations are created (under the Multi-org Setup, which is mandatory), running Replicate Seed data is a pre-requisite step before you can start working in the newly created organization.

The Replicate Seed Data Concurrent Program can be run for a particular Operating Unit or for all Operating Units (as it is not mandatory parameter) but you cannot run the program for a particular module, for example, Incentive Compensation.

Please reference the Replicate Seed Data step in the Oracle E-Business Suite Multiple Organizations
Implementation Guide for more information.

The concept of the program is that whenever new organizations are created they should be should have seeded data from all relevant modules for normal integration among the modules. The seeded data is basic data needed to perform basic steps when setting up a new organization. 

Running this program will not damage the system because it is providing a new organization with the basic information required to set up the organization. 

**Note:** When running the Replicate Seed Data process ensure no users are logged-in