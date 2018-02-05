# Verification

The goal of identity verification is to confirm and establish a linkage between the claimed identity and the physical, live existence of the person actually presenting the evidence. This can be done by a physical or biometric comparison, or a KBV challenge, or by authenticating the applicant with methods and credentials that are appropriate for the level of assurance.

Table 4-3 in SP800-63A details the verification methods necessary to achieve successful verification at the appropriate levels of strength. The strength of an evidence verification system can be assessed using this information; to achieve proofing at IAL 2, at a minimum, agencies must verify the applicants by a process that is able to achieve a strength of STRONG.

In the following sections we will discuss the identity verification methods listed in Table 4-3 in SP800-63A.

## KBV

This technique presents the applicant with a series of questions to help distinguish the applicant from other known identities. The information in KBV systems can be  obtained from publicly available databases to avoid the leakage of sensitive, non-public information.

KBV systems can also be used in the resolution stage of the identity proofing process. 

Detailed requirements for knowledge based verification have been specified in Section 5.3.2 in SP800-63A. 

The quality and availability of the data used in the KBV process results in varying degrees of confidence and agencies should consider the quality when when making decisions on the utilization and outcome of KBV. The agency should follow a set of fundamental principles in KBV design (The UK government’s [Identity Proofing and Verification (IPV) Operations Manual](https://www.gov.uk/government/uploads/system/uploads/attachment_data/file/383109/IPV_Operations_Manual_v2.3.1_Redacted.pdf) and [Good Practice Guide (GPG) 45](https://www.ncsc.gov.uk/content/files/guidance_files/GPG%2045%20%20-%20validating%20and%20Verifying%20the%20identity%20of%20an%20individual%20-%20issue%202.4%20-%20NCSC%20Web.pdf) have been used as a reference to build the baseline guidance presented in this document):
- Clarity –-process must be clear so that applicant can understand and correctly respond
    - Relevant, sensible, proportionate
    - Carefully constructed, clear, obvious as to what is being asked of the applicant
    - Expectation that owner of claimed identity can reasonably complete process
- Breadth –-process should cover a wide range of information
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
- Sources –-process must use suitable sources
    - Organization that captures or generates original data, not intermediary
    - Data originating from separate acceptance and proofing processes within a source can be considered a separate source
    - Source used for KBV must be independent from applicant
    - Where source of KBV is the proofing organization method delivering to claimed identity and not applicant must be used

Three levels should be considered in evaluating quality of KBV data, as shown in Table 5.

| **KBV Quality** | **Properties of KBV Data** |
| --- | --- |
| Low | Pertinent to claimed identity<br/>Can be researched with little financial commitment and with ease<br/>Source of KBV data protects integrity of KBV data |
| Medium | Pertinent to claimed identity<br/>Can be researched with little financial commitment and with ease<br/>Source of KBV data protects integrity of KBV data<br/>Source of KBV data confirmed claimed identity through a proofing process<br/>KBV data not known or likely to be in public domain<br/>KBV data may be available to others or friends and relations, but not without a financial commitment that would be a deterrent or a time commitment that would noticeably delay the user’s ability to provide correct answer during KBV<br/>Source of KBV data protects confidentiality of KBV data<br/>Where KBV data is a shared secret delivery mechanism is confirmed as linked to claimed identity<br/>Where KBV data is a shared secret delivery mechanism for shared secret means it can reasonably be assumed to have been delivered into possession of claimed identity<br/>KBV data is dynamic |
| High | Pertinent to claimed identity<br/>Can be researched with little financial commitment and with ease<br/>Source of KBV data protects integrity of KBV data<br/>Source of KBV data confirmed claimed identity through a proofing process<br/>KBV data not known or likely to be in public domain<br/>KBV data may be available to others or friends and relations, but not without a financial commitment that would be a deterrent or a time commitment that would noticeably delay the user’s ability to provide correct answer during KBV<br/>Source of KBV data protects confidentiality of KBV data<br/>Where KBV data is a shared secret delivery mechanism is confirmed as linked to claimed identity<br/>Where KBV data is a shared secret delivery mechanism for shared secret means it can reasonably be assumed to have been delivered into possession of claimed identity<br/>KBV data is dynamic<br/>KBV data is no older than 45 days<br/>Where KBV data is a shared secret delivery mechanism for shared secret ensured it was delivered into possession of claimed identity<br/>Source of KBV data confirmed claimed identity in manner that complies with US AML regulations<br/>KBV data not in public domain including any public registers<br/>KBV data not known to others beside owner of claimed identity (and immediate family)<br/>Someone other than claimed identity cannot obtain KBV data without committing either a civil or a criminal offense<br/>Source of KBV data has security practices that prevent unauthorized access, modification or generation of KBV data by insiders, alone or with outside coercion<br/>Source of KBV data is subject to regulation by a statutory or independent body<br/>Source of KBV data is reliable and independent from service providing the proofing |

**Table 5:** KBV Data Quality

In general the distinction between static and dynamic knowledge-based verification is made based on whether the security questions are stored by the agency for later access, or generated as applicable to the end user only using specific information, publicly available or otherwise. Static examples such as mother’s maiden name or previous address would not change over time.
While in a broad sense only dynamic KBV is considered for the purposes of identity proofing, it should be noted that there are risks associated with using publicly available data, as there is with secured data that has the risk of compromise. As a general rule of thumb, data used for KBV needs to be as “secret” as possible. Micro-deposits and transaction codes as a form of dynamic KBV are known to work efficiently.
As a guideline, the following can be adopted by agencies to perform KBV for resolution or verification.
If the agency allows the applicant to suspend and resume the process the applicant should not be able to use this feature to gather information relating to the claimed identity.
If the applicant suspends and resumes the process they should either be presented the same questions as before or given new questions which neither have answers that can be deduced from information provided in the previous questions nor reveal answers to previously asked questions.
If the agency allows the applicant to suspend and resume the process the agency should not reveal whether the applicant correctly answered any of the previous questions.
The agency should only allow the applicant to suspend and resume the process twice, totaling a maximum of three attempts. If the CSP presents the same set of questions upon resumption, further questions should be introduced to prevent attackers from using process to extract information and answer previously given questions.
If the applicant fails to return or fails to complete KBV upon return, KBV should be deemed failed.

## Biometric Capture

Biometrics can play a key role in identity proofing and verification of individuals. This utility can come in multiple stages of the identity proofing process.

In enrollment, agencies can capture biometrics in the form of fingerprints, face, iris images, etc. They can compare requirements with their options to identify which single or multi-modal biometric solution can best respond to their needs and implement the system accordingly.

It is important for agencies to note that biometrics collected for enrollment in one instance without any biometric verification for identity proofing should not later be used as a proofing source.

It is also important to note that local automated verification of an applicant's photo against a picture in evidence supplied remotely (such as the image of a driver's license containing an applicant's picture) is in essense no more secure than a physical comparison of the picture in an applicant's evidence document with the applicant's own image. Because this verification does not utilize the information contained in a reliable background repository, agencies should not treat it as of the same level of strength as biometric verification against a background collection, examples of which will be discussed below.

In many applications, the biometric samples collected upon enrollment automatically trigger open-set identification. Open-set identification is typically defined as the task to determine if someone is in a database and to find the record of the individual in the database. This “defensive” first-line measure upon enrollment performs de-duplication. In other words, the agency's database of identities is surveyed automatically to see if the applicant has an existing identity record. If the deduplication search returns a positive match, agencies should match the attributes in the existing identity and the applicant-provided information to determine and adjudicate any mismatches.

Agencies can also leverage biometrics in the resolution and verification steps as another factor to contribute to the degree of confidence along with other methods such as the fuzzy matching of attributes or knowledge-based verification. Naturally, an agency can only do this if biometric data exists for the applicant in the databases wherein the reference attributes for resolution and verification reside. As an example, if guidelines and regulations governing the use and sharing of biometric data allow it, the biometric samples collected as part of the enrollment of one agency can be submitted for a 1:1 verification by another agency wherein the applicant also has an identity record. In this process the biometrics become another factor, enabling the enrolling agency to resolve and verify the identity with confidence.

Requirements and differences between collection methods such as in-person, virtual in-person or remote also concern the collection of biometric samples for applicants. Presentation attacks are a matter of concern for unproctored collection use cases. Ongoing work, such as [*SOFA-B: Strength of Authentication for Biometrics*](https://pages.nist.gov/SOFA/SOFA.html), provides guidelines for the strength of biometric authentication systems as a balanced function of presentation attack detection abilities, biometric match accuracy and effort (to attack system).

Agencies should also note that different biometric modalities provide varying levels of accuracy, presentation attack vulnerability and ease of collection. Existing literature offers deep insight into the trade-off between accuracy, convenience and other factors of biometric authentication. NIST and other authorities have also conducted and orchestrated standardized tests in order to evaluate performances of biometric algorithms developed by participating vendors. agencies should use these resources as guidelines when considering the use of biometrics in their implementations.

For an IAL3 system, detection mechanisms should be in place to ensure security of the system against presentation attacks if collection is done remotely. Requirements for virtual in-person collection mitigate the risk of presentation attacks for an IAL3 system.  Requirements in 800-63A should be considered for IAL2 systems.

Limiting the number of consecutive unsuccessful verification attempts also helps to protect a system against presentation attacks. For a system without presentation attack detection, the limit can be set to 3 while for systems that employ presentation attack detection, a maximum of 10 consecutive unsuccessful attempts may be allowed.

## Address Confirmation

Agencies may require applicants to confirm their address, as outlined in SP800-63A. This is done in the form of an enrollment code sent by the agency, intended for the applicant to receive at their address of record. Successful provision of the correct code by the applicant to the agency serves to confirm the address provided by the applicant: The address binds the identity to the applicant’s record.

An example is a scannable image or barcode that is unique to the enrollment, mailed to the applicant’s address of record. Successful scanning and verification of this image or barcode by a mobile application provided in the agency’s workflow can be used for address confirmation.
