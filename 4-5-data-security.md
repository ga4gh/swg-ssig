# 4.5 Data Security Safeguards #

## 4.5.1 Access Control ##

### Access Control Requirement ###
> Each service provider and service consumer will implement access controls to assure that only authorized individuals and software may access data and services provided through the GA4GH ecosystem, and that each authenticated user (person or entity) is given access to all of and only those data and services to which it has been authorized.


### Access Control Decisions ###
> Access authorizations may be based on organization, individual user, role, location and context (e.g., purpose, authorization time limits)


### Legal and Personal Authorizations ###
> Each service provider and service consumer is responsible for controlling access to genomic and clinical data in accordance with applicable law and the personal authorizations associated with the data.


### Reporting Authorization Policies ###
> Each service provider and service consumer is responsible for assuring that any disclosures of genomic or identifiable clinical data include the personal authorization rules the recipient must enforce with respect to access to, and usage of, those data.

*The work of the Machine-Readable Consent task team and the Registered Access task team is highly relevant here.*


### Policy Transitivity ###
> Each service provider and service consumer with whom genomic or clinical data are shared will control access to and usage of those data in accordance with the personal authorization rules (i.e., consents, permissions) associated with the data


## 4.5.2 Privacy Management ##

### Consent and Policy Persistence ###
> Each data steward is responsible for obtaining the individual authorizations (e.g., consents) required by applicable law and for conveying these authorizations, or a link to these authorizations, along with the associated data.

### User Permissions ###
> The Kantara User Managed Access (UMA) profile[10] of the OAuth 2.0[11] authorization protocol may be useful in mediating access based on user permissions. The UMA profile is available at http://docs.kantarainitiative.org/uma/draft-uma-core.html

### Provenance and Confidentiality ###
> Each data steward is responsible for updating provenance and confidentiality metadata associated with the data under its control, using HL7 FHIR provenance[12] and confidentiality[13] codes.


## 4.5.3 Audit Log Recording and Review ##

### Logging Security Events ###

> Each service provider is responsible for recording and maintaining a log of security- relevant events involving access to or use of resources, data, and services under that entity’s control.

Here "security-relevant events" means lower-level information, such as the fact that a particular user was authenticated, made a particular request, etc. Dixie references ASTM E 2147-01. 

### Required Log Information ###

> For each security-relevant event, the service provider should record the following data elements:[14] user identification, type of event, date and time, success or failure indication, origination of event, name of affected data, system component, or resource.

Consensus was to take a position as to what information should be collected here. Although not normative, we can potentially create interoperability if these suggestions are adopted. 

### Log Retention ###

> Each service provider should retain the audit log history for at least one year, with a minimum of three months immediately available for analysis (for example, online, archived, or restorable from back-up).[14] This best practice should be interpreted within the constraints of applicable jurisdictional law.

Almost nothing we can say here, since this is highly variable by jurisdiction.

### Activity Monitoring ###

> Each service provider is responsible for monitoring activities on the systems under its control to detect potential security breaches and data misuse.

Consensus was to try to define a few events that are global to the GA4GH -- e.g. denial of service, reidentification, etc. Define a syntax for capturing these events. Propose an example of how this could work, e.g. for beacon: maybe a beacon is configured with and endpoint to notify when an event is detected. Start with beacon, then see if we can generalize. 


### Integration with Existing Tools ###

> Service providers’ audit log records should be integratable with existing enterprise security monitoring tools.

Examples logstash/kibana, nagios, monit. Recommendations here.


### Breach Disclosure Policy ###

> Data stewards and their service providers are jointly responsible for implementing the capability to generate an accounting of accesses to and disclosures of data that can be individually identified or associated with the individual.

The Security and Privacy Policy from the REWG has some more detail on this question. Although this requirement is specifically between Data stewards and service providers, it may extend to regulatory authorities, etc. We want to define a syntax / protocol for exposing these. 

## 4.5.4 Data Integrity ##

### Integrity Requirement ###
> Each service provider is responsible for protecting the integrity of genomic and clinical data that it holds, uses, or transmits.

### Checking Integrity ###

> Each service provider that transmits or receives transmissions containing genomic or clinical data will generate a IETF SHA-2 hash function[15] to verify the integrity of the transmission.

### Malware Scanning ###

> Each service provider who offers software will assure that such code is free from malicious software prior to making it available for distribution.


## 4.5.5 Non-repudiation ##

### Content Signatures ###

> Each service provider will have the capability to digitally sign content using a qualified electronic signature, as defined in Directive 1000/03/EC of the European Parliament and of the Council of 13 December 1999 on a Community infrastructure for electronic signatures.[4]

*Presumably for integrity as well as provenance.*


### Software Signatures ###

> GA4GH participants who offer downloadable software will digitally sign the downloadable files using a qualified electronic signature, as defined in Annex II of Directive 1000/03/EC of the European Parliament and of the Council of 13 December 1999 on a Community infrastructure for electronic signatures.[4]
