# Validation 
The goal of identity validation is to collect from the applicant the most appropriate identity evidence (for example, a passport or driver’s license) and determine its authenticity, validity, and accuracy. Identity validation is made up of two process steps: confirming the evidence is genuine and authentic, and confirming the data contained on the identity evidence is valid, current, and related to an actual, live individual. Identity evidence has qualities that make it suitable for proofing at different IALs. Table 5-1 in SP800-63A describes the properties of evidence and qualities that define their strength ratings. Please review SP800-63A Section 4.4.1.2 for evidence requirements at IAL 2. 

For reference, the current IAL 2 proofing requirements are:
- One (1) piece of SUPERIOR or STRONG evidence if the issuing source of the evidence, during its identity proofing event, confirmed the claimed identity by collecting two (2) or more forms of SUPERIOR or STRONG evidence; OR
- Two (2) pieces of STRONG evidence; OR 
- One (1) piece of STRONG evidence plus two (2) pieces of ADEQUATE evidence

In comparison, the IAL 3 proofing requirements, provided in Section 4.5.2 of the same document, are:

- Two (2) or more pieces of SUPERIOR evidence; OR
- One (1) piece of SUPERIOR evidence and one (1) piece of STRONG evidence if the issuing source of the evidence confirmed during its identity proofing event the claimed identity by collecting two (2) or more forms of SUPERIOR or STRONG evidence; OR
- Two (2) pieces of STRONG evidence plus one (1) piece of ADEQUATE evidence

In some cases, a driver’s license may constitute a single piece of definitive evidence. This would be a result of the assurance level requirements of the identity proofing process of the driver’s license in question. We have provided in Appendix  9.1 the driver’s license application document requirements for several REAL ID-compliant and extension states. An example, Maryland, is also provided below. The flowchart developed using the state’s website shows that applicants can provide the state Motor Vehicle Administration a U.S. Birth Certificate and a Social Security Card, a combination allowed by the ruleset. These requirements indicate that a driver’s license is obtained using two pieces of weak evidence for proofing and it therefore should not considered as a definitive piece of evidence in a CSP’s identity proofing process.

CSP’s should start with REAL-ID compliances of states and assess requirements more specifically in order to determine if a driver’s license is acceptable for their desired identity level of assurance. Additionally, at any given time, most, if not all, states have more than one type of driver’s license in circulation, not all of which adhere to the same identity proofing requirements. This should also be taken into account while considering states’ driver’s licenses as evidence.

| **Example** |
| --- |
| The State of Maryland is among the list of states that are [REAL ID-compliant](https://www.dhs.gov/real-id/maryland).<br/>For new driver’s license applicants, Maryland initially checks to see if the applicant has “legally changed [their] name due to marriage or a court order.”<br/>Then, the state requests one of the following from applicants for “[p]roof of [a]ge and [i]dentity:” U.S. Birth Certificate, U.S. Passport, Consular Report of Birth Abroad, Permanent Resident Card, Certificate of Naturalization, Certificate of Citizenship, etc.<br/>Further, Maryland requires “[p]roof of [s]ocial [s]ecurity” by asking the applicant to provide an original social security card, a W-2 form, or other acceptable document that shows the applicant’s complete name and social security number.<br/>The applicants are instructed to bring these two documents to the state’s Motor Vehicle Administration.<br/>The strength ratings in SP800-63A indicate that while the State of Maryland can complete identity proofing for an applicant with one piece of superior evidence and one piece of fair evidence, it is also possible for an applicant to go through the proofing process without any photo identification, supplying a birth certificate and a social security card, since the first set of required documents that the applicant can select from includes both superior and fair evidence. |

## Techniques for Collection

Per SP 800-63A section 4.5.1.5, CSPs should perform proofing in-person, however at IAL 2, remote proofing is allowable. Collection techniques should meet or exceed criteria to ensure secure high-quality data that is acceptable for validation in identity proofing. In what follows, we will provide examples of criteria that CSP’s should observe.

Secure transmission of data is a typical concern and systems used by CSP’s should adopt baseline security controls. CSP’s should follow the guidance of documents such as NIST Special Publication 800-53 Revision 4, *Security and Privacy Controls for Federal Information Systems and Organizations (Appendix F)*, which presents a “catalog of security controls that provides a range of safeguards and countermeasures for organizations and information systems.”

Camera resolution is a typical criterion in collecting images for identity proofing. It is important to note that camera resolution alone may not suffice as a criterion for image quality. Without further instructions specifying the size of the person’s face, hands, eye region, finger, etc., even the highest-resolution camera can result in images that are of insufficient quality despite best efforts and common sense of the collector. The example provided earlier for the U.S. Department of State’s passport application process is a useful guideline in providing specifications for capture.

Ambient lighting conditions are also an important factor to consider while collecting data. Despite the ability of most modern camera equipment to adjust settings such as contrast or brightness automatically, unproctored collection may result in excessive ambient light and overexposure in outdoor settings, or dark, underexposed images if taken under low light, e.g. behind a computer desk. CSP’s should consider lighting conditions when collecting images or issuing instructions for collecting images.
CSP’s should also consider other criteria such as the field of view and image obfuscation when developing collection techniques for identity proofing.

### In-Person Collection

In-person collection of evidence provides the CSP the opportunity to physically inspect the evidence for authenticity. Evidence should be physically presented to the CSP for examination during validation and digital image(s) of the evidence should be captured for use during the remainder of the proofing process.

### Virtual In-Person

Virtual in-person remote identity person proofing process that employs physical, technical and procedural measures that provide sufficient confidence that the remote session can be considered equivalent to a physical, in-person identity proofing encounter. Requirements for virtual in-person proofing can be found in section 5.3.3.2 of SP 800-63A. 

An example is the use of video communications over the internet to proof an individual’s identity. This can be used by a CSP to ensure that the applicant presents the evidence in real-time to the collector and and to capture the evidence (e.g. still picture/snapshot containing an image of the document) for proofing.

### Remote Collection

If evidence is presented digitally, the imaging quality should be high enough to allow for the visual validation of the information presented on the evidence. The imaging should also be clear and unobstructed to allow the CSP to use validation techniques similar to those used in-person.

## Validation Techniques

At IAL 2, CSP’s may allow applicants to present evidence digitally to facilitate remote proofing. Evidence presented in this manner will often be examined visually to determine if it appears fraudulent, counterfeit, or otherwise modified. The collection of evidence and validation of their authenticity may occur at the same time.

| **Example** |
| --- |
| If  an applicant provides a digital image of their driver’s license, the system accepting that image may be able to automatically read the ID number or barcode and perform a lookup in the issuing state’s motor vehicles department to confirm its authenticity. |

CSP’s should also examine the evidence visually. Techniques for remote validation should be comparable to in-person validation. Table 5-2 in SP800-63A describe methods for validating identity evidence at each strength.  

The validation process consists of two steps as we mentioned earlier: determining whether the evidence is genuine and checking if it is valid. Accordingly, CSP’s may use the following techniques to validate evidence in identity proofing:

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
    - Confirming the accuracy of information including name, address, DoB with the issuing source
    - Confirming information from a machine-readable passport
    - Confirming information from a machine-readable driver’s license    
    
CSPs can leverage physical and digital security features to validate identity evidence. Examples of security features are provided in Table 3.

| **Feature** | **Advantages** |
| --- | --- |
| Holographic Security Threads | Highly complex production processes make documents tough to counterfeit. |
| Secure Ink | Durable and reliable bonding provides resistance against tampering and forgery. |
| Dynamic Fluorescent Feature | Dynamic response generated in UV light at varying distances from the source is hard to duplicate by attackers. |
| Ghost Image | Image duplicating applicant photo or other feature generated with UV ink can only be seen under UV light. |
| Integrated Circuit with PKI Protection | Asymmetric cryptography protects data content. |
| Digital Watermark | Documents signed by digital watermarking (DWM) (such as driver’s license images) can also be used by CSPs as a piece of strong evidence in identity proofing. Watermarks are embedded in images used in secure identity verification and use applications to verify the rightful owner of an evidence document. Some applications, for instance, use the applicant’s fingerprint information to watermark the image. |
| Barcodes | Barcode embedded on the document can be used to carry data and validate strong evidence by CSPs that wish to validate evidence. |
| Checksums | As a cryptographic application, the checksum is calculated by applying cryptographic algorithms to data in order to generate a hash, which is then used to validate the data. The generated hash is the checksum used for validation and the principle is that unauthorized parties would not be able to change the data without affecting the hash as they would not have visibility into the cryptographic algorithm or algorithms that were originally used by the provider to generate the hash. Checksums therefore provide a method to validate electronic evidence as well, whereby CSP’s can generate cryptographic checks to associate with documents used as evidence, which are then subject to a check for validation. This method can then be used to validate strong evidence. |

**Table 3:** Physical and Digital Security Features

Training of operators is also important for CSP’s to be able to expect and recognize the presence of a validating feature in a piece of evidence that normally carries it, and utilize specific knowledge or equipment to validate.

It is also important to make the distinction between equipment and knowledge that is the patented intellectual property of a particular vendor and is protected by patent law, and equipment and knowledge (algorithms, workflows, systems) that is proprietary to the vendor, whose internal working mechanisms are not known to outside entities that are not bound by non-disclosure agreements. Measures should be taken to ensure that proprietary systems and equipment produce results that are trusted by the CSP.

### Example: Validation

To validate the identity the CSP must examine the documents collected during enrollment. Automated software (or an operator) will first check the security features on the document that has been uploaded by the applicant using the mobile application – holograms, secure inks and other devices – to check that it is genuine. Second, the CSP will also validate the personalized information on the card – name, date of birth, address, driver’s license or passport number, account number – and make sure that the information in the documents is valid.

