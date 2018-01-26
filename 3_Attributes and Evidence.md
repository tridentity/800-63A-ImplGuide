# Attributes and Evidence

Beside the information provided by the applicant –-please note that the word “information” here is intended to convey information provided in the content of an evidence document, and not solely knowledge or the applicant’s say-so, which alone is not sufficient for proofing—-, proofing can also require evidence from an applicant as dictated by the requirements of the CSP. 

Once the identity assurance level for a system or subsystem has been selected, the CSP can determine the attributes and identity evidence required to satisfy their use case.

The first step to proof an individual is to collect the core attributes necessary to establish a unique representation of the individual’s identity for use during the proofing process. The core attributes, regardless of IAL, should be collected in accordance with the requirements identified in SP800-63A. The collection of these core attributes is intended to help the CSP resolve applicants to a single unique entity and to enable the appropriate level of verification and validation to support system risk and meet IAL requirements. Some commonly used core attributes are name, date of birth, address, phone number and e-mail address.

There should be a good balance between executing the proofing process and minimizing the burden on the applicant. 

Submitting evidence in multiple stages can become burdensome for an applicant. It is important to consider collecting the appropriate evidence up-front to avoid requiring the user to perform multiple interactions in order to establish an account.

It is ultimately up to the CSP or agency to determine which biographic information to collect about an applicant. CSPs should take caution in collecting and utilizing a minimally required set of attributes and store attributes on a strictly need-to-know basis. 

## Types of Evidence

Table 2 provides examples of evidence from each category of strength defined in the aforementioned identity evidence quality table in 800-63A.


| **Strength** | **Qualities of Identity Evidence** | **Examples** |
| --- | --- | --- |
| Unacceptable | - No acceptable identity evidence provided. | Library Cards |
| Weak |- The issuing source of the evidence did not perform identity proofing.<br/>- The issuing process for the evidence means that it can reasonably be assumed to have been delivered into the possession of the applicant.<br/>- The evidence contains:<br/>- At least one reference number that uniquely identifies itself or the person to whom it relates.<br/>OR<br/>- The issued identity evidence contains a photograph or biometric template (of any modality) of the person to whom it relates. | Membership or Loyalty Cards<br/>Birth Certificate<br/>Social Security Card |
| Fair |- The issuing source of the evidence confirmed the claimed identity through an identity proofing process.<br/>- The issuing process for the evidence means that it can reasonably be assumed to have been delivered into the possession of the person to whom it relates.<br/>- The evidence:<br/>- contains at least one reference number that uniquely identifies the person to whom it relates.<br/>OR<br/>- contains a photograph or biometric template (any modality) of the person to whom it relates.<br/>OR<br/>- can have ownership confirmed through KBV.<br/>- Where the evidence includes digital information, that information is protected using approved cryptographic or proprietary methods, or both, and those methods ensure the integrity of the information and enable the authenticity of the claimed issuing source to be confirmed.<br/>- Where the evidence includes physical security features, it requires proprietary knowledge to be able to reproduce it.<br/>- The issued evidence is unexpired. | Individual Taxpayer Identification Number<br/>Credit or Debit Card<br/>Bank Account Statement<br/>Utility Account Statement |
| Strong |- The issuing source of the evidence confirmed the claimed identity through written procedures designed to enable it to form a reasonable belief that it knows the real-life identity of the person. Such procedures are subject to recurring oversight by regulatory or publicly-accountable institutions. For example, the Customer Identification Program guidelines established in response to the USA PATRIOT Act of 2001 or the Red Flags Rule, under Section 114 of the Fair and Accurate Credit Transaction Act of 2003 (FACT Act).<br/>- The issuing process for the evidence ensured that it was delivered into the possession of the subject to whom it relates<br/>- The issued evidence contains at least one reference number that uniquely identifies the person to whom it relates.<br/>- The full name on the issued evidence must be the name that the person was officially known by at the time of issuance. Not permitted are pseudonyms, aliases, an initial for surname, or initials for all given names<br/>- The:<br/>- Issued evidence contains a photograph or biometric template (of any modality) of the person to whom it relates.<br/>OR<br/>- Applicant proves possession of an AAL2 authenticator, or equivalent, bound to an IAL2 identity, at a minimum.<br/>- Where the issued evidence includes digital information, that information is protected using approved cryptographic or proprietary methods, or both, and those methods ensure the integrity of the information and enable the authenticity of the claimed issuing source to be confirmed.<br/>- Where the issued evidence contains physical security features, it requires proprietary knowledge and proprietary technologies to be able to reproduce it.<br/>- The evidence is unexpired. | Real ID Driver’s License<br/>State Identification Card |
| Superior |- The issuing source of the evidence confirmed the claimed identity by following written procedures designed to enable it to have high confidence that the source knows the real-life identity of the subject. Such procedures are subject to recurring oversight by regulatory or publicly accountable institutions.<br/>- The issuing source visually identified the applicant and performed further checks to confirm the existence of that person.<br/>- The issuing process for the evidence ensured that it was delivered into the possession of the person to whom it relates.<br/>- The evidence contains at least one reference number that uniquely identifies the person to whom it relates.<br/>- The full name on the evidence must be the name that the person was officially known by at the time of issuance. Not permitted are pseudonyms, aliases, an initial for surname, or initials for all given names.<br/>- The evidence contains a photograph of the person to whom it relates.<br/>- The evidence contains a biometric template (of any modality) of the person to whom it relates.<br/>- The evidence includes digital information, the information is protected using approved cryptographic or proprietary methods, or both, and those methods ensure the integrity of the information and enable the authenticity of the issuing source to be confirmed.<br/>- The evidence includes physical security features that require proprietary knowledge and proprietary technologies to be able to reproduce it.<br/>- The evidence is unexpired. | FIPS 201 Compliant Personal Identification Verification Card (PIV, PIV-I, and CAC)<br/>National Passports<br/>Enhanced Driver’s License or Identification |

**Table 2:** Examples of Identity Evidence

Please note that while examples of unacceptable and weak evidence are presented here for the sake of completeness, CSPs should nevertheless be careful in requiring such documents as identity evidence. Moreover, CSPs are cautioned to review guidance on international or common names and the event of a name change while considering evidence for strength.

A CSP can collect an applicant’s social security number as additional information, but two other forms of identification should still be collected to which information in the social security number should still resolve. An example selection of evidence documents for a CSP to consider in an IAL2 process are shown in the following figure.

![Figure 3: Selecting Evidence](media/workflow-1-evidence-selection.png)

**Figure 3** Selecting Evidence

## Collection Techniques

CSPs may use multiple techniques for collecting attributes and evidence in different media. These pertain to digital or other methods of collection that result in the transmission of information from the applicant to the CSP. As noted earlier, while the processes laid out in this guide suggest multiple phases of collection, it is possible that agencies or CSPs could choose to collect core attributes, additionally required attributes, and evidence during the same event. Multiple techniques may also be combined based on agency requirements, user needs, and the overall approved proofing process flow.

### Digital

The initial information may be captured via an online form directly from the applicant that is being proofed.
In other cases, the CSP may allow the applicant to provide some documents via remote means, such as submitting an image of an identification document like a passport or a driver’s license. This workflow requires the utilization of some form of digital capture, such as a camera or a document scanner. Systems with optical character recognition capabilities that allow fields in a document to be pre-populated upon scanning should also allow the applicant to review and validate the information as correct.

Some of the methods with which a CSP can digitally capture evidence are listed in Table 3.

| **Method** | **Device** | **Information** |
| --- | --- | --- |
| Photo Capture | Camera | This can be used to capture an applicant’s photo or the image of an evidence such as a driver’s license. CSPs can consider pictures at 300 dpi or above to be of sufficient resolution. |
| Document Capture | Scanner | This can capture a document, which is compared against a known template by automated software to extract information. For optical character recognition, scans at high than 300 dpi are typically considered to be of sufficient quality. |
| Barcode | Scanner | Commercial off-the-shelf scanners can capture and extract information from standardized barcodes embedded on identity evidence. |
| UV Light | Lamp/Reader | Certain document features can only be detected under UV light and therefore require specialized equipment for the CSP to validate or otherwise capture information. |

**Table 3** Digital Evidence Capture Methods

Some CSPs may choose to enforce requirements more directly by providing mobile applications for collection –e.g. camera capture functions that provide an overlay and illumination check feature to ensure applicants provide pictures with correct size and brightness. For passport applications, the U.S. Department of State requires the photograph to be submitted physically as a printed picture, but also provides guidelines for applicants that choose to collect and submit their own printed pictures after digitally creating them.

###	In-Person

If a CSP allows in-person registration, it may consider, for efficiency and convenience purposes, executing additional steps in the process, such as evidence validation, at the time of registration. The CSP may provide kiosks to allow applicants to enter their information directly. Alternatively, users may meet with a representative of the CSP to allow them to enter the applicant’s information on their behalf. Note—when this is done it is important the process is conducted in a manner that allows the individual to verify their information has been accurately captured and input into the collection system. Training should be provided for all CSP representatives to ensure that they are aware of organizational and federal policy concerning privacy and user experience.

###	Paper Form

In the event an applicant does not have access to a connected device, is unable to use a computer, or otherwise wishes to submit the biographic information via a non-digital medium, the CSP may offer the option to complete a paper form instead. Written entry of information should be avoided if it is possible to capture information via multiple choice selections and the applicant should be instructed to print clearly to reduce inaccuracies resulting from the interpretation of handwriting. Some organizations require enrollment via paper form only in person while some implementations may allow the applicant to complete the form remotely and mail it in. It is also important to note that in many use cases applicants are asked to fill out a paper form with sensitive personal information and mail it to the requesting organization. Precautions should be taken minimize that risk and maintain transparency by informing the individual of the risks while the paper form is in transit.
