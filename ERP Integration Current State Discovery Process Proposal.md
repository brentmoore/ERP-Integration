# ERP Integration Current State Discovery Process Proposal
> **Draft**

This document is intended to outline the process of documenting the current state of all integrations impacted by the migration to Workday HR and Finance. Given the number and variety of system integrations involving our existing PeopleSoft HR and Finance systems having a standardized approach to the documentation of the details of each integration is critical in gaining an accurate understanding of the scope of the work of the migration and creating a workable plan for the migration. 

The process for determining the future state of all integrations will be addressed in a separate document.

### Goals of the Effort

This effort is focused on:
- Discovering all points of integration with the existing PeopleSoft HR and Finance systems.
- Capturing sufficient information about the discovered integrations to determine: 
    - If the integration will be necessary with the new Workday system.
    - The best way to support that integration with Workday.
- Gathering sufficient data so that a transition plan for each integration can be created. The actual creation of a transition plan will be a future endeavor.
An added but not primary goal is to provide relevant information discovered to other university strategic efforts, including identity and data. 

### Principles to Follow

There are a number of principles that influence all aspects of this effort. 
1. **Accuracy is everything**. Sufficient research needs to be done to ensure the documentation accurately reflects the current state of the integration. No assumptions should be made as to how the integration functions. Any aspect of the the integration that is not well understood should be highlighted and tracked for further clarification. 
2. **Documentation should be complete and self contained**. Diagrams, combined with textual documentation should be sufficient to describe the integration to the point that it can be understood and a migration plan created. No verbal explanation should be needed.
3. **Documentation is standardized**. Documentation and diagrams should all follow the same standard for the information gathered and diagram styles.
4. **Prefer quick and maintainable diagrams**. The purpose of the diagrams is to convey information. Diagrams that can be created quickly and convey the necessary information are preferred to spending a large amount of time making a diagram "pretty" while not adding pertinent information. 
5. **Gather only what is necessary and sufficient for our purposes**. We need to respect the time of development groups involved in describing the integration. We should only require the information that is necessary for describing the integration and describes it sufficiently for our purposes. Fully documenting every aspect of all integrations between all systems is not the point of this effort. We are only interested in the integrations and data that deal with the migration to Workday of Finance and HR. If we find other integrations that involve identity, SIS, and student financials we should make a note for the teams involved in those efforts and move on. We should be clear about why we are asking for each type of information we require.


### Patterns of Integrations

For this effort an integration is defined as any communication between two systems of interest, regardless of the direction of the flow of information (in or out). So the integrations we need to track are any flow of information (data, events, etc) into and out of the current PeopleSoft HR and Finance systems. 

Not all integrations are the same, but most follow one of a few basic patterns. Each pattern requires a different documentation standard to be sufficiently defined. The number of integration patterns in use will expand over time. The patterns derived from an initial list of the integrations include:

- **Transaction Import** - Standardized data that usually appears as transaction files to be uploaded to the target system. Accounting journal entries and accounts payable / receivable requests fit into this pattern. The target system publishes one or more  standard formats and processes for submitting transactions. 
- **Transaction Export** - Data exported for batch submission to an external system via a flat file. Used to communicate with a number of our external service providers.
- **Data Fetch** - Some systems need specific pieces of information to fulfill their business purpose but do not need or want to store that information. These systems fetch the data as needed from the source system, usually via an API. 
- **Data Update** - Some systems update a small set of data elements in PeopleSoft, usually via an API call or Informatica process. 
- **Data Sync** - Many systems require their own copy of all data necessary for them to fulfill their business purpose. This is particularly true of SaaS and Off the Shelf systems. To support these systems data is replicated between systems and processes are put into place to keep the data synchronized.
- **Initiation of a Business Process** - Activity in a system triggers an action in another system. This is usually accomplished with events combined with data fetches. 


### Process Overview

#### Get a handle on the scope of the problem

We don't really know the number of integrations that must be moved to Workday. The current list of integrations was drawn from a variety of sources and contains duplicates and omissions. There are also number of integrations on the list that are out of scope for the migration of HR and Finance. Until the list is cleaned up we don't really know the scope of work required for the migration. Assigning a small group of knowledgeable engineers to go though the list with the workstream teams to eliminate duplicates and find obvious omissions will greatly help increase the accuracy of the list.

#### Classify each integration into the pattern it fits

Some integration patterns are simple and others are complex. Classifying each integration by pattern allows us to divide the simple integrations (transaction import) from the more complex (data sync) and scope the documentation effort appropriately.

#### Group integrations by development group

Once we have an accurate list of integrations, work can begin on gathering the details of each integration. Contacting each development group with a complete list of the integrations we are interested in documenting, regardless of which workstream they touch, will help in streamlining our interactions with each development group and allow us to be sensitive to their time. 

#### Roadmap the OIT abstraction layer (APIs, Events)

There is a common set of APIs and events that much of campus uses to interact with our ERP systems (Persons API, ChartBlock API, personnel action events, etc). Detailing our roadmap for each of these APIs and events simplifies the responsibility for each dependent integration. Dependent integrations can then simply document the information they use from the API or event and what it is used for.

#### Work with each consuming system's technical representatives to define the interaction in detail

Detailed information about each integration needs to be gathered in order to fully understand how best to migrate the integration. The amount of detail required is dependent upon the pattern the integration follows. 

#### Use the gathered information to create a plan for migration

Once necessary details are in place a migration plan can be created and added to the schedule. Development groups can know what will be expected of them and plan accordingly. 

Specifics about what documentation is required for each integration type is contained in a separate document.
