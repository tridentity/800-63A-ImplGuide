# Verification

The goal of identity verification is to confirm and establish a linkage between the claimed identity and the physical, live existence of the person actually presenting the evidence. This can be done by a physical or biometric comparison, or a KBV challenge, or by authenticating the applicant with methods and credentials that are appropriate for the level of assurance.

The following table presents the verification methods that should be considered to achieve a given level of strength of fair or above. The requirements for these levels have been outlined in Table 5-3 in SP800-63A.

| **Strength** | **Method** | **Description** |
| --- | --- | --- |
| Superior | Biometric Verification | Comparison against strongest piece of evidence, remote or in-person |
| Strong | In-Person Physical Verification | Physical comparison to photograph against strongest piece of evidence done in person: Operator compares submitted evidence with applicant in-person |
| Strong | Remote Physical Verification | Physical comparison to photograph against strongest piece of evidence done remotely: Operator compares submitted evidence with applicant via remote video or remotely submitted image |
| Fair | Knowledge-Based Verification | Comparison of challenge response provided by applicant against known information, remote or in-person |

**Table 4: Verification Methods and Strengths**

In the following subsections we will offer implementation considerations for these verification methods.

## Biometric Verification

Biometrics can play a key role in identity proofing and verification of individuals. This utility can come in multiple stages in identity management systems. In this section, we will provide considerations for implementing biometric verification in identity proofing.

Biometric verification of an applicant can be done using two main methodologies.

In one, biometrics collected from the applicant is matched against trusted data sources and repositories if guidelines and regulations governing the use and sharing of biometric data allow it, i.e. the biometric samples collected as part of the enrollment of one agency can be submitted for a 1:1 verification by another agency wherein the applicant also has an identity record. This can be fingerprint, face or iris image of an applicant, supplied during identity proofing for verification. The agency collecting the biometrics then submits the image or images to the trusted data sources that contain biometric information on the applicant to verify the applicant’s provided identity.

In the second approach, biometrics collected from the applicant is matched against biometrics present in identity evidence provided by the applicant. The matching is done in a similar way to the process described above, while the reference biometrics (e.g. fingerprint or face) in this case is stored as a template on the evidence document.

It is important to note that a verification process wherein an agency collects face biometrics from an applicant, and then matches it against face biometrics extracted anew from the photo identification evidence provided by the applicant is not considered strong biometric verification against a trusted data source and should be treated as equivalent to a physical verification of the applicant’s identity for proofing.

Agencies should follow the guidance of NIST Special Publication 800-63B, Section 5.2.3 for requirements on match accuracy, rate limiting, presentation attack detection (PAD) and template protection or revokability when implementing biometric verification systems for identity proofing. Presentation attacks are a matter of concern for unproctored collection use cases. Ongoing work, such as SOFA-B: Strength of Authentication for Biometrics, provides guidelines for the strength of biometric authentication systems as a balanced function of presentation attack detection abilities, biometric match accuracy and effort (to attack system).

Agencies can capture biometrics in the form of fingerprints, face, iris images, etc. They can compare requirements with their options to identify which single or multi-modal biometric solution can best respond to their needs and implement the system accordingly. Agencies should also note that different biometric modalities provide varying levels of accuracy, presentation attack vulnerability and ease of collection. Existing literature offers deep insight into the trade-off between accuracy, convenience and other factors of biometric authentication. NIST and other authorities have also conducted and orchestrated standardized tests in order to evaluate performances of biometric algorithms developed by participating vendors. Agencies should use these resources as guidelines when considering the use of biometrics in their implementations. The following table outlines some considerations for some of the high-accuracy biometric modalities in verification.

| **Biometric Modality** | **Verification Considerations**|
| --- | --- |
| Fingerprint | Commonly used in many applications, including authentication integration with chip cards. Fingerprint readers are widely available, including those that are interoperable with systems used for generating typical chip card identity evidence examples that agencies can choose to use. |
| Iris | Not as broadly available as fingerprints, but also very accurate. Specialized capture devices needed and image acquisition issues have largely been mitigated in the current state of the art. Device costs have also come down significantly, though the ability to find a trusted background source that can match an applicant's iris biometrics to their own reference gallery is limited. |
| Face | While still quite accurate, face biometrics is far more vulnerable to capture issues such as ambient lighting conditions. On the flipside, a photograph being the most ubiquitous component of identity evidence, opportunities to match an applicant's face biometrics against a trusted background source are abundant. |

**Table 5:** Biometric Modalities and Verification Considerations

Requirements and differences between collection methods such as in-person, virtual in-person or remote also concern the collection of biometric samples for applicants. 

### In-person Biometric Verification

### Remote Biometric Verification

For an IAL3 system, detection mechanisms should be in place to ensure security of the system against presentation attacks if collection is done remotely. Requirements for virtual in-person collection mitigate the risk of presentation attacks for an IAL3 system. Requirements in 800-63A should be considered for IAL2 systems.

## Physical Verification

Agencies can perform physical verification of an applicant by comparing the applicant to a photograph or against the strongest piece of evidence provided to support the claimed identity. As noted in 63A, guidance in [NIST Special Publication 800-63B, Section 5.2.3](https://pages.nist.gov/800-63-3/sp800-63b.html#biometric_use) should be followed for the requirements for physical verification. As mentioned earlier, biometric verification that is done locally (i.e. biometrics captured on device matched against biometrics stored on device) or biometric verification done by matching biometrics provided by applicant against biometrics present in evidence provided by the applicant should be considered of no greater strength than that of physical verification of applicant against evidence. Physical verification can be done in person or via a shared video session with the applicant, or by means of a remote submission of evidence by the applicant.

## KBV

This technique presents the applicant with a series of questions to help distinguish the applicant from other known identities. While it is preferred that information in KBV systems are obtained from publicly available databases to counter fraud attempts due to leakage of sensitive, non-public information from compromised data sources, this also means that KBV cannot properly secure the identity proofing process against attackers that have compiled all publicly available information about an applicant. That is why KBV is generally designated at a level of fair in 63A, as specified in [Section 5.3.2](https://pages.nist.gov/800-63-3/sp800-63a.html#sec5). 

KBV systems can also be used in the resolution stage of the identity proofing process. 

The quality and availability of the data used in the KBV process results in varying degrees of confidence and agencies should consider the quality when when making decisions on the utilization and outcome of KBV. The UK government’s [Identity Proofing and Verification (IPV) Operations Manual](https://www.gov.uk/government/uploads/system/uploads/attachment_data/file/383109/IPV_Operations_Manual_v2.3.1_Redacted.pdf) and [Good Practice Guide (GPG) 45](https://www.ncsc.gov.uk/content/files/guidance_files/GPG%2045%20%20-%20validating%20and%20Verifying%20the%20identity%20of%20an%20individual%20-%20issue%202.4%20-%20NCSC%20Web.pdf) have been used as a reference to build the baseline considerations presented in this document. Accordingly, the agency should follow a set of fundamental principles in KBV design:
- **Clarity:** Process must be clear so that applicant can understand and correctly respond.
    - Relevant, sensible, proportionate
    - Carefully constructed, clear, obvious as to what is being asked of the applicant
    - Expectation that owner of claimed identity can reasonably complete process
- **Breadth:** Process should cover a wide range of information.
    - Based on a range of information and not one single source
    - Covering different evidence categories
    - Security –process must protect claimed identity from impersonation
    - Constructed so that loss or theft would not provide required information to pass
    - Must not be used where it is known or likely to be in the public domain
    - Multiple choice answers must be plausible and not easily guessed
    - Multiple questions should not be answering one another
    - Answers cannot be researched from public domain or social media
    - Must minimize risk of impersonation by close family member
    - Answers to multiple questions should not have been provided to applicant earlier in workflow
    - Must not reveal personal information that has not been provided by applicant
- **Sources:** Process must use suitable sources.
    - Organization that captures or generates original data, not intermediary
    - Data originating from separate acceptance and proofing processes within a source can be considered a separate source
    - Source used for KBV must be independent from applicant
    - Where source of KBV is the proofing organization method delivering to claimed identity and not applicant must be used

In general the distinction between static and dynamic knowledge-based verification is made based on whether the security questions are stored by the agency for later access, or generated as applicable to the end user only using specific information, publicly available or otherwise. Static examples such as mother’s maiden name or previous address would not change over time. Two types of dynamic KBV should be considered for identity proofing, as listed in Table 6.

| **Dynamic KBV Type** | **Description** |
| --- | --- |
| Quiz-based | In this approach, a series of questions is asked to the applicant from a pool of available information. The sequence of the questions is not static and is impacted by the applicant's answers. A scoring mechanism can be used to evaluate an applicant's performance and return a KBV verification outcome, based on the number and sequence of correct and incorrect answers and an applicant's pausing/resumption of the process. |
| Micro Deposit | In this approach, one or more microdeposits are made into a bank account provided by the applicant and the amounts are used to verify the applicant's identity. Please note that in some cases it may not be possible to verify an applicant's identity using ACH (routing and account number) information without paying for third-party verification services and agencies looking to bind an applicant's identity to bank account information should consider this while evaluating a KBV option for verification. |

**Table 6: Dynamic KBV Types**

Dynamic KBV should be considered over static for the purposes of identity proofing.

## Address Confirmation

Agencies may also require applicants to confirm their address, as outlined in SP800-63A for remote and in-person implementations wherein a proofing notice or an enrollment code can be sent to the applicant's address of record. Successful provision of the correct code by the applicant to the agency serves to confirm the address provided by the applicant: The address binds the identity to the applicant’s record. The following table includes different types of addresses that can be used for confirmation.

| **Address Type** | **Notes** |
| --- | --- |
| Physical Mail | This is the address of record for an applicant that can be used by the agency to mail a notice of proofing or an enrollment code. While using an address for verification in KBV is vulnerable to attacks leveraging an array of public address registers, physical address use for notices or codes in proofing can be compromised if the applicant's mail is intercepted. |
| Electronic Mail | This is a an email address provided by the applicant which can be used for notification or verification of enrollment codes. |
| Phone | A phone number can be used as an address to confirm an applicant in scenarios such as automated phone calls that complete proofing upon responses to voice prompts, or the verification of enrollment codes by the applicant if the number and the phone verification are used in conjunction with a physical or electronic delivery mechanism. |

**Table 7: Address Types Used for Confirmation**

The enrollment or notification of proofing code can be a verifiable sequence of digits or numbers to be provided by the applicant when prompted, or a scannable image or barcode contained within the notice that can scanned by the mobile application used by the applicant as included in the agency's workflow.
