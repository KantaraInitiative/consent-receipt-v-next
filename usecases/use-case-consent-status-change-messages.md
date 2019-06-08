# Use Case: Consent Status Change Messages


Author: 
Andrew Hughes

Date: 
2018-09-25

# Actors
* Consent Management Platform
* PII Controller front end systems
* PII Controller back end systems
* PII Principal

# Terminology

# Description
The PII Principal interacts with the PII Controller front end systems. The PII Controller front end systems offer services to the PII Principal. PII Controller front end systems use a Consent Management Platform to provide privacy notices, inform the PII Principal of purposes for collection and processing of PII, create consent receipts, communicate consent changes to other systems and to assist in servicing consent-related requests. 

In an enterprise deployment of a Consent Management Platform, the Consent Management Platform must communicate consent status changes to all affected PII Controller back end systems.

After a consent event occurs, the Consent Management Platform records relevant details and creates a Consent Receipt. Either the PII Controller systems or the Consent Management Platform communicates with PII Controller back end systems to inform them to make configuration changes as a result of the consent event. 

The systems use the Consent Receipt specification data structure to communicate.

When a change to the PII Principal consent status occurs, such as withdrawl, modification or time limit, the Consent Management Platform communicates with PII Controller back end systems to inform them to make configuration changes as a result of the status change.

The systems use the Consent Receipt specification data structure to communicate.


# Outcome
The Consent Receipt Specification is used to inform PII Controller systems of changes to PII Principal consent status.
