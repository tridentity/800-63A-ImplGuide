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

## Selecting an IAL

Managing the risk assessment process and selecting the assurance level can be challenging. To assist agencies through the process, NIST has built the framework around identity assurance levels summarized in Table 1 and provided selection guidance in SP800-63A. Assurance in a subscriber’s identity is described using one of three Identity Assurance Levels, or IALs. The IAL selection process, as presented in NIST800-63-3, has been illustrated in Figure 2. Broadly categorizing all subsystems at the same level of identity assurance may not be ideal and it should be recognized that systems with different IAL1 and IAL2 or IAL3 compartments may need to be partitioned with respect to their specific identity assurance level requirements, leading the implementations to be done accordingly.

![Figure 2: Selecting an IAL](https://github.com/usnistgov/800-63-3/blob/nist-pages/sp800-63-3/media/IAL_CYOA.png)

**Figure 2:** Selecting an IAL

According to Table 1 the following is true for IAL1:

- There is no requirement of proof for an applicant’s identity.
- Any attributes that are provided in the authentication process are either:
    - Self-asserted, or
    - Should be treated as self-asserted

Table 1 suggests the following for IAL2:

- Identity proofing is required with evidence that:
    - Supports real-world existence of the claimed identity
    - Verifies the association between the applicant and the real-world identity
- Identity proofing can be done in person or remotely
- Attributes may be asserted by CSPs to RPs for verification in support of pseudonymous identity

For IAL3:

- Identity proofing is required to be done in person
- Attributes must be verified by an authorized and trained representative of the CSP
- CSPs may assert attributes to RPs for verification in support of pseudonymous identity

| ***Case Example: IAL Selection without Proofing***|
| --- |
| A free secure messaging service provider offers desktop and smartphone application versions of a product that allows users to send one another encrypted messages via the internet. Users are registered by providing a first and a last name and selecting a unique user name that is connected to an email address through which registration has to be confirmed and account management is done. Secure authentication is done via user name and a custom password.

While building their product architecture, the company consulted SP800-63A and determined that their identity model does not require a user to prove their actual identity. No mechanism will be built to check the veracity of the user’s first and last name, or the associated identity to which the registered email address belongs. It was therefore concluded that their identity proofing requirements are of level IAL1. |

As with the other content in this document the IAL selection guidance is intended to be informative and to complement the existing risk management practices of each agency. It is not intended to supersede or contravene processes and procedures developed at the organizational level. As there are not requirements for identity proofing at IAL 1, hereafter this document focuses on IAL 2 & 3 and the processes for putting into place an operational identity proofing program. 

As seen in the case example, there is no proof requirement until IAL2.

## Determining the Necessary Evidence

Once the identity assurance level for a system or subsystem has been selected, the CSP can determine the evidence required for identity proofing.

Beside the information provided by the applicant during the enrollment process –please note that the word “information” here is intended to convey information provided in the content of an evidence document, and not solely knowledge or the applicant’s say-so, which alone is not sufficient for proofing—, the validation step may also require evidence from an applicant as dictated by the requirements of the CSP. Submitting evidence this way in multiple stages can become burdensome for an applicant. It is important to consider collecting the appropriate evidence up-front to avoid requiring the user to perform multiple interactions in order to establish and account.

There should be a good balance between executing the proofing process and minimizing the burden on the applicant.

## Types of Evidence

Table 2 provides examples of evidence from each category of strength defined in the aforementioned identity evidence quality table in 800-63A.

| **Strength** | **Examples** |
| --- | --- |
| Unacceptable | Library Cards |
| Weak | Organizational Membership Cards<br/>Birth Certificate<br/>Social Security Card |
| Fair | Individual Tax Number<br/>Credit or Debit Card\br Bank Account Statement<br/>Utility Account Statement |
| Strong | Real ID Driver’s License\br State ID |
| Superior | FIPS 201 Compliant Personal Identification Verification Card (PIV, PIV-I, and CAC)<br/>National Passports<br/>Enhanced Driver’s License or Identification |

**Table 2:** Examples of Identity Evidence

Please note that while examples of unacceptable and weak evidence are presented here for the sake of completeness, CSP’s should nevertheless be careful in requiring such documents as identity evidence. CSP’s should also consider birth certificates and social security cards, which contain no visual evidence with which to confirm the applicant’s identity, with special care. Moreover, CSP’s are cautioned to revisit guidance provided earlier with respect to international or common names and the event of a name change while considering evidence for strength.

A CSP can collect an applicant’s social security number as additional information, but two other forms of identification should still be collected to which information in the social security number should still resolve. An example selection of evidence documents for a CSP to consider in an IAL2 process are shown in the following figure.

![Figure 3: Selecting Evidence](https://github.com/usnistgov/800-63-3/tree/nist-pages/sp800-63-3/media/workflow-1-evidence-selection.png)

**Figure 3** Selecting Evidence

Documents signed by digital watermarking (DWM) (such as driver’s license images) can also be used by CSP’s as a piece of strong evidence in identity proofing. Watermarks are embedded in images used in secure identity verification and use applications to verify the rightful owner of an evidence document. Some applications, for instance, use the applicant’s fingerprint information to watermark the image. Training of operators is also important for CSP’s to be able to expect and recognize the presence of a watermark in a piece of evidence that normally carries it, or notice when the watermark is absent for a simple binary fraud checking measure.

Numbers, references and checksums may also be used by CSP’s to validate strong evidence in identity proofing.

Checksums are an application of the traditional digital error-checking mechanism to cryptographic security. As a concept, a checksum is a numerical sum representing the correct digits in a piece of transmitted data, enabling recipients or relaying parties to verify integrity. As a cryptographic application, the checksum is calculated by applying cryptographic algorithms to data in order to generate a hash, which is then used to validate the data. The generated hash is the checksum used for validation and the principle is that unauthorized parties would not be able to change the data without affecting the hash as they would not have visibility into the cryptographic algorithm or algorithms that were originally used by the provider to generate the hash.

Checksums therefore provide a method to validate electronic evidence as well, whereby CSP’s can generate cryptographic checks to associate with documents used as evidence, which are then subject to a check for validation. This method can then be used to validate strong evidence.

Similarly, numbers or references that are associated with identity evidence such as a barcode embedded on the document can be used to validate strong evidence by CSP’s that wish to validate evidence.

It is also important to make the distinction between equipment and knowledge that is the patented intellectual property of a particular vendor and is protected by patent law, and equipment and knowledge (algorithms, workflows, systems) that is proprietary to the vendor, whose internal working mechanisms are not known to outside entities that are not bound by non-disclosure agreements. Measures should be taken to ensure that proprietary systems and equipment produce results that are trusted by the CSP.
