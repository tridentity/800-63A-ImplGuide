# Verification

The goal of identity verification is to confirm and establish a linkage between the claimed identity and the physical, live existence of the person actually presenting the evidence. This can be done by a physical or biometric comparison, or a KBV challenge, or by authenticating the applicant with methods and credentials that are appropriate for the level of assurance.

Table 4-3 in SP800-63A details the verification methods necessary to achieve successful verification at the appropriate levels of strength. The strength of an evidence verification system can be assessed using this information; to achieve proofing at IAL 2, at a minimum, the applicant must be verified by a process that is able to achieve a strength of STRONG. 

In the following sections we will discuss the identity verification methods listed in Table 4-3 in SP800-63A.

## KBV

This technique utilizes a series of questions to help distinguish the applicant from other known identities in order to perform verification in identity proofing. Please see earlier discussion in Section 4.2 for more information.

## Biometric Capture

Biometrics can play a key role in identity proofing and verification of individuals. This utility can come in multiple stages of the identity proofing process.

In enrollment, CSP’s can capture biometrics in the form of fingerprints, face, iris images, etc. They can compare requirements with their options to identify which single or multi-modal biometric solution can best respond to their needs and implement the system accordingly.

It is important for CSP’s to note that biometrics collected for enrollment in one instance without any biometric verification for identity proofing should not later be used as a proofing source.

In many applications, the biometric samples collected upon enrollment automatically trigger open-set identification. Open-set identification is typically defined as the task to determine if someone is in a database and to find the record of the individual in the database. This “defensive” first-line measure upon enrollment performs de-duplication. In other words, the CSP’s database of identities is surveyed automatically to see if the applicant has an existing identity record. If the deduplication search returns a positive match, CSP’s should match the attributes in the existing identity and the applicant-provided information to determine and adjudicate any mismatches.

CSP’s can also leverage biometrics in the resolution and verification steps as another factor to contribute to the degree of confidence along with other methods such as the fuzzy matching of attributes or knowledge-based verification. Naturally, a CSP can only do this if biometric data exists for the applicant in the databases wherein the reference attributes for resolution and verification reside. As an example, if guidelines and regulations governing the use and sharing of biometric data allow it, the biometric samples collected as part of the enrollment of one CSP can be submitted for a 1:1 verification by another CSP wherein the applicant also has an identity record. In this process the biometrics become another factor, enabling the enrolling CSP to resolve and verify the identity with confidence.

Requirements and differences between collection methods such as in-person, virtual in-person or remote also concern the collection of biometric samples for applicants. Presentation attacks are a matter of concern for unproctored collection use cases. Ongoing work, such as [*SOFA-B: Strength of Authentication for Biometrics*](https://pages.nist.gov/SOFA/SOFA.html), provides guidelines for the strength of biometric authentication systems as a balanced function of presentation attack detection abilities, biometric match accuracy and effort (to attack system).

CSP’s should also note that different biometric modalities provide varying levels of accuracy, presentation attack vulnerability and ease of collection. Existing literature offers deep insight into the trade-off between accuracy, convenience and other factors of biometric authentication. NIST and other authorities have also conducted and orchestrated standardized tests in order to evaluate performances of biometric algorithms developed by participating vendors. CSP’s should use these resources as guidelines when considering the use of biometrics in their implementations.

For an IAL3 system, detection mechanisms should be in place to ensure security of the system against presentation attacks if collection is done remotely. Requirements for virtual in-person collection mitigate the risk of presentation attacks for an IAL3 system.  Requirements in 800-63A should be considered for IAL2 systems.

Limiting the number of consecutive unsuccessful verification attempts also helps to protect a system against presentation attacks. For a system without presentation attack detection, the limit can be set to 3 while for systems that employ presentation attack detection, a maximum of 10 consecutive unsuccessful attempts may be allowed.

## Address Confirmation

CSP’s may require applicants to confirm their address, as outlined in SP800-63A. This is done in the form of an enrollment code sent by the CSP, intended for the applicant to receive at their address of record. Successful provision of the correct code by the applicant to the CSP serves to confirm the address provided by the applicant: The address binds the identity to the applicant’s record.

An example is a scannable image or barcode that is unique to the enrollment, mailed to the applicant’s address of record. Successful scanning and verification of this image or barcode by a mobile application provided in the CSP’s workflow can be used for address confirmation.
