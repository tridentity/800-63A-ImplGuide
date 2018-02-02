# Validation 
The goal of identity validation is to collect from the applicant the most appropriate identity evidence (for example, a passport or driver’s license) and determine its authenticity and accuracy. Identity validation is made up of two process steps: confirming the evidence is genuine and authentic, and confirming the data contained on the identity evidence is valid, current, and related to an actual, live individual. Regardless of level - steps must be taken to validate the evidence to prevent an attacker from fraudulently completing the identity proofing process by presenting forged or modified evidence. 

## Validation Techniques

At IAL 2, agencies may allow applicants to present evidence digitally to facilitate remote proofing. Evidence presented in this manner will often be examined visually to determine if it appears fraudulent, counterfeit, or otherwise modified. The collection of evidence and validation of their authenticity may occur at the same time.

| **Example** |
| --- |
| If  an applicant provides a digital image of their driver’s license, the system accepting that image may be able to automatically read the ID number or barcode and perform a lookup in the issuing state’s motor vehicles department to confirm its authenticity. |

Agencies should also examine the evidence visually. Techniques for remote validation should be comparable to in-person validation. Table 5-2 in SP800-63A describe methods for validating identity evidence at each strength.  

The validation process consists of two steps as we mentioned earlier: determining whether the evidence is genuine and checking if it is valid. Accordingly, agency may use the following techniques to validate evidence in identity proofing:

- Determining whether the evidence is genuine
    - Examination of the security features of a physical document
        - Ultraviolet desktop light and magnifier
        - Inspection equipment that can assist in identifying forgeries or counterfeit documents
    - Physical document containing cryptographically protected information
        - Reading the embedded chip with a compatible reader
        - Comparing the retrieved information with personal and evidence details on the document
        - Confirming the digital signature
        - Validating the signing key
        - Confirming the correctness of the signing key with respect to evidence type and source
    - Electronic evidence containing cryptographically protected information
        - Confirming the electronic signature is correct
        - Validating the signing key
        - Validating the checksum
        - Confirming the correctness of the signing key with respect to evidence type and source
- Checking if the identity evidence is valid
    - Confirming the accuracy of information including name, address, DOB with the issuing source
    - Confirming information from a machine-readable passport
    - Confirming information from a machine-readable driver’s license    
    
Agencies can leverage physical and digital security features to validate identity evidence. Examples of security features are provided in Table 3.

| **Feature** | **Advantages** |
| --- | --- |
| Holographic Security Threads | Highly complex production processes make documents tough to counterfeit. |
| Secure Ink | Durable and reliable bonding provides resistance against tampering and forgery. |
| Dynamic Fluorescent Feature | Dynamic response generated in UV light at varying distances from the source is hard to duplicate by attackers. |
| Ghost Image | Image duplicating applicant photo or other feature generated with UV ink can only be seen under UV light. |
| Integrated Circuit with PKI Protection | Asymmetric cryptography protects data content. |
| Digital Watermark | Documents signed by digital watermarking (DWM) (such as driver’s license images) can also be used by agencies as a piece of strong evidence in identity proofing. Watermarks are embedded in images used in secure identity verification and use applications to verify the rightful owner of an evidence document. Some applications, for instance, use the applicant’s fingerprint information to watermark the image. |
| Barcodes | Barcode embedded on the document can be used to carry data and validate strong evidence by agencies that wish to validate evidence. |
| Checksums | As a cryptographic application, the checksum is calculated by applying cryptographic algorithms to data in order to generate a hash, which is then used to validate the data. The generated hash is the checksum used for validation and the principle is that unauthorized parties would not be able to change the data without affecting the hash as they would not have visibility into the cryptographic algorithm or algorithms that were originally used by the provider to generate the hash. Checksums therefore provide a method to validate electronic evidence as well, whereby agencies can generate cryptographic checks to associate with documents used as evidence, which are then subject to a check for validation. This method can then be used to validate strong evidence. |

**Table 3:** Physical and Digital Security Features

Training of operators is also important for agencies to be able to expect and recognize the presence of a validating feature in a piece of evidence that normally carries it, and utilize specific knowledge or equipment to validate.

It is also important to make the distinction between equipment and knowledge that is the patented intellectual property of a particular vendor and is protected by patent law, and equipment and knowledge (algorithms, workflows, systems) that is proprietary to the vendor, whose internal working mechanisms are not known to outside entities that are not bound by non-disclosure agreements. Measures should be taken to ensure that proprietary systems and equipment produce results that are trusted by the agency.

## Validation Strength

When validating - agencies must do so consistent with the level of strength appropriate based on the strengh of the evidence. For example, a piece of evidence characterized as being "strong" evidence must be validated at the same level of strength. NIST SP 800-63A provides the following requirements for achieving different validation strengths:  

|Strength|Method(s) performed by the agency|
|:---:|:------------------------------|
|Unacceptable|- Evidence validation was not performed, or validation of the evidence failed.|
|Weak|- All personal details from the evidence have been confirmed as valid by comparison with information held or published by an authoritative source.|
|Fair| - The evidence:<br>&nbsp;&nbsp;&nbsp;&nbsp;- details have been confirmed as valid by comparison with information held or published by the issuing source or authoritative source(s).<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**OR**<br>&nbsp;&nbsp;&nbsp;&nbsp;- has been confirmed as genuine using appropriate technologies, confirming the integrity of physical security features and that the evidence is not fraudulent or inappropriately modified.<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**OR** <br>&nbsp;&nbsp;&nbsp;&nbsp;- The evidence has been confirmed as genuine by trained personnel. <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**OR** <br>&nbsp;&nbsp;&nbsp;&nbsp;- The issued evidence has been confirmed as genuine by confirmation of the integrity of cryptographic security features.|
|Strong| - The evidence has been confirmed as genuine:<br>&nbsp;&nbsp;&nbsp;&nbsp;- using appropriate technologies, confirming the integrity of physical security features and that the evidence is not fraudulent or inappropriately modified. <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**OR**<br>&nbsp;&nbsp;&nbsp;&nbsp;- by trained personnel and appropriate technologies, confirming the integrity of the physical security features and that the evidence is not fraudulent or inappropriately modified.<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**OR**<br>&nbsp;&nbsp;&nbsp;&nbsp;- by confirmation of the integrity of cryptographic security features.<br><br> - All personal details and evidence details have been confirmed as valid by comparison with information held or published by the issuing source or authoritative source(s).|
|Superior| - The evidence has been confirmed as genuine by trained personnel and appropriate technologies including the integrity of any physical and cryptographic security features.<br><br> - All personal details and evidence details from the evidence have been confirmed as valid by comparison with information held or published by the issuing source or authoritative source(s).|
