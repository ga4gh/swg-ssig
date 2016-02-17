# 4.10 Service Supplier Security #

> Entities that offer data and application services within the GA4GH ecosystem are encouraged to implement architectural assurances that their services can be relied upon to perform their functions as advertised, while resisting malicious attack, adapting to changes, continuing to operate through unanticipated disruptions, and recovering from interruptions and outages. Architectural safeguards include design principles that contribute to the trustworthiness of systems and networks, including but not limited to ability of a system or network to protect the confidentiality and integrity of genomic and clinical data, the availability of data and services, and the privacy of individuals whose data are shared.

> All data, application, and infrastructure service providers to the GA4GH community are responsible for implementing appropriate architectural assurances that will enable them to provide a high level of service expectations, as described in each service provider’s service level agreement (SLAs). These expectations include:

> ● Availability – the ability of the service to perform its functions over a specified period of time, generally expressed as the proportion of time that a service is actually available within an agreed-upon time period. Availability is assured through architectural and design features, and operational procedures that enhance reliability, maintainability, serviceability, and security.

> ● Scalability (or elasticity) – Genomic and clinical data stores should be capable of expanding as the volume of data continues to grow, while protecting the confidentiality, integrity, and availability of data and application services.

> ● Infrastructure security – security features and processes provided as part of the data or application service offering GA4GH service providers and user organizations should assure that their infrastructure, operating systems, and database management systems isolate applications and datasets to prevent interference from other processes and side-channel attacks. A “least privileges” approach should be used to harden execution environments.

> Data stewards should assure that their service suppliers offer the levels of availability, scalability, and infrastructure security necessary to protect the data entrusted to them. Similarly, service consumers should assure that data and application services they use are trustworthy.
