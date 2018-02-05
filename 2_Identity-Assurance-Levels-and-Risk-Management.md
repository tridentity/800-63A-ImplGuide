# Identity Assurance Levels and Risk Management

[NIST SP 800-63A](https://pages.nist.gov/800-63-3/sp800-63a.html) divides identity proofing requirements into three Identity Assurance Levels. At each level the document describes unique requirements for the processes, techniques, and approaches that may be taken by agencies and organizations, with increasing levels of stringency.

Per [800-63-3](https://pages.nist.gov/800-63-3/), agencies are required to conduct a thorough risk assessment of their systems –including assessments of both privacy and security risks -- and understand the risks associated with the resources, data, and applications being accessed via a specific identity management solution. This document does not provide guidance on how to conduct these risk assessment, but readers can find further information in resources such as [NIST Special Publication 800-37, Guide for Applying the Risk Management Framework to Federal Information Systems](http://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-37r1.pdf); [NIST Special Publication 800-53, Security and Privacy Controls for Federal Information Systems and Organizations](http://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-53r4.pdf); or [Federal Information Processing Standards Publication 199, Standards for Security Categorization of Federal Information and Information Systems](http://nvlpubs.nist.gov/nistpubs/FIPS/NIST.FIPS.199.pdf).

Additionally, agencies and service providers are expected to employ appropriately tailored security controls from the moderate baseline of security controls defined in NIST SP800-53 or equivalent industry standard and ensure that the minimum assurance requirements associated with the moderate baseline are satisfied.

## Selecting an IAL

NIST SP 800-63-3 includes a sample process flow for selection of identity assurance levels. Assurance in a subscriber’s identity is described using one of three IALs. The IAL selection process, as presented in NIST800-63-3, has been illustrated in Figure 2.

![Figure 2: Selecting an IAL](https://github.com/usnistgov/800-63-3/blob/nist-pages/sp800-63-3/media/IAL_CYOA.png)

**Figure 2:** Selecting an IAL

**IAL 1:** There is no requirement of proof for an applicant’s identity and any attributes that are provided in the authentication process are either self-asserted, or should be treated as self-asserted.

**IAL 2:** Identity proofing is required with evidence that supports real-world existence of the claimed identity and verifies the association between the applicant and the real-world identity. Identity proofing can be done in person or remotely and attributes may be asserted by agencies to RPs for verification in support of pseudonymous identity.

**IAL 3:** Identity proofing is required to be done in person; attributes must be verified by an authorized and trained representative of the agency, and agencies may assert attributes to RPs for verification in support of pseudonymous identity.

In some system architectures, a single IAL for the entire system may not be sufficient to mitigate risk effectively. In these instances  the proper course of action would be to identify and isolate components of the system and determine individual component assurance levels. Similarly, users and operators of a system may have varying levels of access and authorization requirements necessitating different IALs based on privileges, access levels, or authorizations. Agencies should consider the selection of IALs based on the context of specific systems, applications, and user bases --rather than attempting to implement a general set of proofing controls. 
