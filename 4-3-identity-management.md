# 4.3 Identity Management #

## Service Authentication ##

Here is a quotation from the Security Framework:

> • Each data and application service exposed within the GA4GH ecosystem will have the capability to electronically authenticate its fully qualified domain name using a server certificate or, within the EU, a qualified electronic signature, as defined in Annex II of Directive 1000/03/EC of the European Parliament and of the Council of 13 December 1999 on a Community infrastructure for electronic signatures.[4]

... and this section would elaborate on these requirements, providing recommendations e.g. for obtaining certificates, possibly configuring common web server software with these certs, etc.


## User Authentication ##
> • Each service provider will authenticate the identity of individuals and software accessing data and services under that provider’s control.


## Identity Providers ##
> • Data and application service providers are encouraged to externalize authentication and authorization to trusted identity providers.


## Identity Proofing and Levels of Assurance ##

> • The level of assurance to which individual identities will be established (i.e., identity proofing) and authenticated will be consistent with the level of risk associated with the actions to be performed by that individual. Suggested levels of assurance are defined in the US National Institute of Standards and Technology (NIST) Special Publication (SP) - 2,[5] as shown in Figure 2 below; each LOA comprises a unified set of identity proofing, authentication, and token protection attributes. (Note that NIST SP 800-63-2 is under revision.)

*Reproduce the table from Figure 2 here?*

## Federated Identities ##

> • Service providers may choose to federate authenticated identities and service authorizations using either OASIS Security Assertion Markup Language (SAML) V2.0,[6] or OAuth 2.0[7] with OpenID Connect.[8]

The Software Security Task Team has done some substantial work here already. This is where we document the findings and recommendations.
