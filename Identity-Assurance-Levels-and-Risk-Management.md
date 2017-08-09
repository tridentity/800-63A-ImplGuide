# Identity Assurance Levels and Risk Management

NIST SP 800-63A divides identity proofing requirements into three different assurance levels: Identity Assurance Levels, or IALs, 1, 2 and 3. At each level the document describes unique requirements for the processes, techniques, and approaches that may be taken by agencies and organizations, with increasing levels of stringency. These levels align with the Levels of Assurance, or LOA’s, in Office of Management and Budget’s Memorandum M-04-04, *E-Authentication Guidance for Federal Agencies*, which outlines overall identity assurance levels based on risk and potential impacts of a system compromise to the agency and users. This alignment and SP 800-63A’s descriptions of assurance levels have been outlined in Table 1.

| SP 800-63 IAL | Description | OMB M04-04 LOA |
| ------------- | ----------- | -------------- |
| IAL1 | There is no requirement for an applicant’s identity to be proven. Any attributes provided in conjunction with the authentication process are self-asserted or should be treated as self-asserted. | LOA 1 |
| IAL2 | The claimed identity is proven with evidence that supports the real world existence of the claimed identity and identifies and verifies the person to whom the claimed identity belongs. IAL 2 introduces the need for either remote or in-person identity proofing. Attributes MAY be asserted by CSPs to RPs in support of pseudonymous identity with verified attributes. | LOA 2 & 3 |
| IAL3 | In-person identity proofing is required. Identifying attributes must be verified by an authorized and trained representative of the CSP. As with IAL 2, attributes MAY be asserted by CSPs to RPs in support of pseudonymous identity with verified attributes. | LOA 4 |

**Table 1:** Identity Assurance Levels in SP 800-63A and OMB M-04-04

Agencies and service providers building or acquiring identity solutions are expected to conduct a thorough risk assessment of their systems –including assessments of both privacy and security risks-- and understand the risks associated with the resources, data, and applications being accessed via a specific identity management solution. This document does not provide guidance on how to conduct these risk assessment, but readers can find further information in resources such as the aforementioned M-04-04; NIST Special Publication 800-53, *Security and Privacy Controls for Federal Information Systems and Organizations*; or Federal Information Processing Standards publication 199, *Standards for Security Categorization of Federal Information and Information Systems*. 

Additionally, agencies and service providers are expected to employ appropriately tailored security controls from the moderate baseline of security controls defined in NIST SP800-53 or equivalent industry standard and ensure that the minimum assurance requirements associated with the moderate baseline are satisfied.

## Selecting and IAL

Managing the risk assessment process and selecting the assurance level can be challenging. To assist agencies through the process, NIST has built the framework around identity assurance levels summarized in Table 1 and provided selection guidance in SP800-63A. Assurance in a subscriber’s identity is described using one of three Identity Assurance Levels, or IALs. The IAL selection process, as presented in NIST800-63-3, has been illustrated in Figure 2. Broadly categorizing all subsystems at the same level of identity assurance may not be ideal and it should be recognized that systems with different IAL1 and IAL2 or IAL3 compartments may need to be partitioned with respect to their specific identity assurance level requirements, leading the implementations to be done accordingly.

![Figure 2: Selecting an IAL](https://github.com/usnistgov/800-63-3/blob/nist-pages/sp800-63-3/media/IAL_CYOA.png)

**Figure 2:** Selecting an IAL
