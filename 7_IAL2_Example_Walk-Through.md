# IAL2 Example Walkthrough

Assuming that IAL2 is selected for a particular use, let us walk through the identity proofing steps for an application case wherein a provider offers services through a mobile device.

## Evidence Selection

The agency e-mails applicants to inform them that enrollment can be done remotely using its secure mobile application through which the service or solution is delivered.

The landing page of the application instructs the applicant to login or sign-up using email. A new applicant is instructed to provide either:

1.	Full name, address, DOB and a photograph of their US passport’s ID page, OR
2.	Full name, address, DOB, a photograph of their Driver’s License, the ABA/routing number and account number for a bank account and the name, number, expiration date and security code for a credit card.

![Figure 4: Mobile Application's Document Instructions Page](media/workflow-2-instructions.png)

**Figure 4:** Mobile Application's Document Instructions Page

The applicant is told explicitly that the passport and driver’s license images will be used for identity verification only, and once verified, document images will be deleted and not retained by the agency.

The agency then requests, as shown in Figure 4, a picture of the applicant’s passport to be uploaded using the mobile application, or a picture of their driver’s license in addition to credit card and bank account information. The applicant also providers full name, address and date of birth for registration. These tasks, as shown on the mobile application, are illustrated in Figure 5.

![Figure 5: Document Capture](media/workflow-3-enrollment.png)

**Figure 5:** Document Capture

Once document capture is finished, the applicant is advised to await a confirmation message.

## Resolution

The agency proceeds to resolve all core attributes collected from the applicant into a single identity. In the case of paper/in-person applications some of the resolution steps may require human intervention.

In our IAL2 example, the agency can leverage identity document image verification software to obtain the full name, address and DOB for an applicant from the image of their driver’s license or passport that they received via the app. Once attribute information is produced from the document image, the agency has two or more sets of attributes for the applicant –one from the application entries provided by the applicant, and one or more from the document(s).

The agency can then run a matching algorithm, as depicted in the following figure, to obtain a similarity score that reflects the extent to which the different sets of identity attributes resolve, and, comparing this against a threshold, decide success or failure.

![Figure 6: Resolution](https://github.com/usnistgov/800-63A-ImplGuide/blob/master/media/workflow-4-resolution.png)

**Figure 6:** Resolution

## Validation

To validate the identity the agency must examine the documents collected from the applicant. Automated software (or an operator) will first check the security features on the document that has been uploaded by the applicant using the mobile application – holograms, secure inks and other devices – to check that it is genuine. Second, the agency will also validate the personalized information on the card – name, date of birth, address, driver’s license or passport number, account number – and make sure that the information in the documents is valid. An example is illustrated in Figure 7, where an automated system that uses the picture of the applicant's passport to extract information and physical security features to validate the evidence in terms of both the features and the information.

![Figure 7: Validation](https://github.com/usnistgov/800-63A-ImplGuide/blob/master/media/workflow-5-validation.png)

**Figure 7:** Validation

## Verification

The agency completes the identity proofing process by verification. In this step, the identity of the actual individual applying is verified for a match against the individual whose identity information is built using resolution and validation of the documents provided. A general outline for the verification process has been shown in the following figure. In our example, the agency uses the mobile application to perform face verification of the individual which compares a face image submitted by the applicant in the final stage of identity proofing against face images in the background records of the applicant’s driver’s license or passport. Please note that this would be equivalent to a physical check if the applicant's picture taken by the mobile app is compared simply to the image on the identity document; strong or superior biometric verification would require the verification of the applicant' face image against an image (or template thereof) retained in the background repository by the state department of motor vehicles or the Department of State. For enhanced security, the agency can in addition use the bank account information provided by the applicant to submit two micro deposits of less than $1 each, and then ask the applicant to complete the final verification step by providing the micro deposit amounts in cents, appended into a 4-digit sequence. Upon successful verification the agency will issue credentials to the applicant, who can subsequently start using the service.

![Figure 8: Verification](https://github.com/usnistgov/800-63A-ImplGuide/blob/master/media/workflow-5-verification.png)

**Figure 8:** Verification
