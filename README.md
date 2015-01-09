# prototype-microservices-architecture-dotne
A prototype architecture for a microservices extension of an legacy closed ERP system

## Overview of the document
The following document will provide a base framework architecture for the extension of the current Shipping company ERP system.
The current state of the system, at the time of the writing of this document, was a single close sourced monolithic application deployed on top of a DB2 database. The current ERP system provides all the base functions required by the shipping organization, but it lacks some fundamental features and it’s the desire of the company to extend it with more manageable and extensible system.
On top of the basic ERP operations the current system relies on several third party data providers which provide various types of data sources (XML feeds, manual downloads and web services) with real time (or as close as possible) information about various shipping statues of ships and containers currently an route around the world (detailed description of third party shipping providers can be found in the requirements document).
The ERP extension architecture document will focus on providing an architectural framework used to solve the following technical and process problems:
1.	Unified system wide event logging (who what and where inside the entire system)
2.	Unified third party data retrieval and processing system
3.	Unified system event generation based on data changes inside the original ERP system
4.	Framework for extending the original system with application silos based on event generation and loose core system integration based on published core system web services and message queues.
5.	Management system for all integration components (e.g. custom built ETL systems)
6.	General DevOPS strategy for managing and deploying applications

The document will be organize into the following sections:
- General architectural principles
- High level architecture model
- Specific architectural models
- Framework utilization guidelines
