# Resolution

The goal of this step is to use the information provided by the applicant to resolve them to a unique, claimed identity. Considerations should be taken for individuals with common names, originating from populous areas, and geographies outside of the United States. This process may be started automatically upon submission of biographic information during the enrollment process. Unlike validation and verification, the resolution process is focused on ensuring that the information being provided is representative of a real unique individual that can be distinguished from other records to enable the verification of associated attributes and identity evidence. It, in and of itself, is not intended to provide confidence that the individual presenting the information is who they claim to be. 

The overall resolution process provided by FIPS PUB 201, *Personal Identity Verification of Federal Employees and Contractors*, can be used as a guideline at the IAL3 level. IAL2 applications have less stringent identity proofing requirements (such as the relaxed IAL3 requirement of in-person presentation) and CSP’s should design their identity proofing process accordingly using the requirements in 800-63A.

Agencies and CSPs should take into account factors specific to the populations that they serve, or intend to serve, to help design enrollment and proofing processes to allow for the collection of necessary information to uniquely distinguish between individual users—without collecting unnecessary sensitive information.  As SP800-63A emphasizes, effective identity resolution uses the smallest set of attributes necessary to resolve to a unique individual. Where possible non-sensitive information should be added to collection if additional attributes are needed to help differentiate users. For example, a population of former military personnel will provide different details and require different resolution data sources than foreign nationals.

| ***Example: Name Changes*** |
| --- |
| It should also be pointed out that not all individuals continue carrying the same legal name throughout their lifetime. Marriage is but one way the name of a person can change legally; another event that may result in a name change is a sex change, which may also result in a change in the self-identification of the individual’s gender, from male to female, or female to male, or female or male, to unknown or undefined. CSP’s should be aware of the possible complications that could be introduced in the proofing process due to these changes and take explicit steps to utilize the evidence documenting the name or gender change to ensure that the provided information resolves into a unique identity. |

Name changes frequently take place due to marriage, divorce or personal preference. When an applicant states that their name has changed and presents formal evidence of such change, the CSP should resolve the identity accordingly. The requirements and procedural guidelines in FIPS PUB 201 can be followed by CSP’s to issue a new credential in the event of a name change. 

A new credential can be issued by the CSP if the applicant presents evidence of name change in the form of a marriage certificate, divorce decree, judicial recognition or other mechanism as permitted by State law or regulation. The identity proofing process needs to be repeated if the CSP does not maintain a chain-of-trust record for the individual or if the reissuance process was not started before the expiration of the old credential. If biometrics have been collected to enroll the individual, a 1:1 biometric comparison of the applicant can be used to reconnect them to the chain of trust, following minimum accuracy requirements specified in NIST SP800-76, Biometric Specifications for Personal Identity Verification. In this case, while a successful match should in the release of a new credential to the applicant, an unsuccessful match or unavailability of data for a biometric comparison should require that applicant provide identity source documents as determined by the IAL level of the process and that the attending operator inspect them and verify the applicant against the face image on record. 

Sets and combinations of core and supplemental attributes provide varying levels of effectiveness, sensitivity, availability and reliability. An assessment of such metrics for core and supplemental identity attributes, e.g. name, address, date and place of birth, mother’s maiden name and gender, can be found in NASPO-IDPV-60 by the American Security Products Organization’s Identity Proofing and Verification (IDPV) working group (NASPO-IDPV-60. Establishment of Core Identity Attribute Sets and Supplemental Identity Attributes, Report of the IDPV Identity Resolution Project, Feb. 17, 2014). Organizations that seek a balance between these metrics and the necessity of the attributes in their selection process in order for their identity proofing design to adhere to their assurance level requirements may use such guidelines.

Additional attributes may also exist in special data sets that are proprietary or private, requiring the collection of more than biographic information.

To reduce inaccuracies and increase efficiency of the resolution process, CSPs have historically employed knowledge based verification (KBV) or matching algorithms. We will examine the two in the following subsections.

## Matching Algorithms

Matching algorithms produce a match outcome based on a comparison of personal information and proofing data and provide a degree or level of confidence for the match outcome which needs to be taken into account by the CSP when relying on the match algorithm’s certainty for identity proofing decisions. Fuzzy matching algorithms perform contextual comparisons between fields of identity records and take into account factors such as name changes, misspellings, typographical errors, nicknames, variants, phonetic similarities and special characters and produce match outcomes that would otherwise not be captured in an exact comparison. 

The uniqueness of the individual and the information presented impact the complexity of the resolution process. Statistically common names may require uniqueness beyond even Date of Birth, given the commonality of the name. 

| ***Example: Fuzzy Matching of Names*** |
| --- |
| A fuzzy matching algorithm may help the resolution of an identity record belonging to James A. Aldrin and data belonging to Jim Alvin Aldren to the same individual with a certain degree of confidence by taking into account that “Jim” is a variant of “James”, “A” is the first initial of “Alvin” and “Aldrin” could possibly have been misspelled as “Aldren,” if other data such as address, date of birth and place of birth all match. |

Another issue which requires close attention is the varying frequency of names across different languages and cultures. Compounding this complexity is the phonetic transformation of names from alphabets like Hangul (Korea), Hiragana (Japan), the Cyrillic and Arabic alphabets into English, which can frequently result in individuals with different names in their countries of origin having their names “translated” into identical names in English. 

| ***Example: Common Last Names*** |
| --- |
| South Korea is a nation of approximately 50 million (2013). [As of the year 2000], a total of roughly 300 family names were in use in Korea and 54 percent of the population had one of the top five most commonly used family names. (*Source:* [Everything you ever wanted to know about Korean surnames](http://www.korea.net/NewsFocus/Culture/view?articleId=75090) Jacco Zwetsloot. KOREA.net, Aug. 12, 2009) |

It is also important to note that measures should be taken to prevent applicants from intentionally or accidentally undergoing the proofing process to obtain multiple credentials.

CSP’s should take care to check for uniqueness during registration. Fuzzy matching of attributes, if employed, also needs to be carefully assessed. Considerations should be made by the CSP as to the confidence level associated with the outcome of a fuzzy match in terms of its applicability to the requirements of the specific level of assurance of the process. 

Fuzzy matching is effective only when the degree of confidence in the inexact match of a single attribute can be supported by the matching of additional attributes that belong to the same identity. The following table can be used as a guideline for CSP’s to consider when using fuzzy matching to resolve identities. As an example if two of the attributes listed below have a confidence score of 95% and the third is at 100%, the total confidence level is just over 90%; if all three are at 95% overall confidence falls to 86% and if all three are above 98.5% overall confidence exceeds 95.5%.

<table><tbody><tr>
<td><table><tbody>
<tr><th>Attribute</th><th>Check</th><th>Rule</th></tr>
<tr><td>Name</td><td><ol><li>Align all fields.<li>Match with replacements, abbreviations.<li>Produce overall score as %.</ol></td><td rowspan=3>Multiply scores, compare to 90%.</td></tr>
<tr><td>Date of Birth</td><td><ol><li>Check using correct order.<li>Check using wrong order.<li>Produce overall score as %.</ol></td></tr>
<tr><td>Current Address</td><td><ol><li>Standardize address.<li>Match.<li>Produce scores as %. </ol></td></tr>
</tbody><table>

**Table 4:** Fuzzy Matching of Attributes Using Name, Date of Birth and Current Address

Accurate matching of attributes can be a requirement with immediate life-and-death consequences; the U.S. Department of Veterans’ Affairs and many large health care organizations use attribute matching systems to perform patient identity matching. These systems vary in costs and complexity and fuzzy matching algorithms consider demographic attributes such as name, date of birth, address and phone number. When comparisons indicate a high statistical likelihood that the records are related, the algorithm declares a match between the two records based on thresholds established by the assurance requirements of the use case. In deterministic cases (such as the algorithm used by the Veterans Health Administration) exact matching of identity and demographic data is performed. In general all fuzzy matching tools involve a similar sequence of steps:

- Import the data
- Align the data fields for proper matching of attributes
- Specify match weights for fields
- Run match algorithm to generate scores for each record pair
- Calculate overall score using weights, compare to a threshold and generate list of candidates
- List match candidates for editing and review

## KBV

If a CSP chooses to start the identity proofing process with higher confidence, or in the event an identity cannot be resolved using automated matching algorithms or manual inspection by CSP staff, the CSP may request the applicant participate in a Knowledge Based Verification process. This technique presents the applicant with a series of questions to help distinguish the applicant from other known identities. The information in KBV systems can be  obtained from publicly available databases to avoid the leakage of sensitive, non-public information.

KBV systems are also commonly used in the verification stage of the identity proofing process. 

Detailed requirements for knowledge based verification have been specified in Section 5.3.2 in SP800-63A. 

The quality and availability of the data used in the KBV process results in varying degrees of confidence and CSP’s should consider the quality when when making decisions on the utilization and outcome of KBV. The CSP should follow a set of four fundamental principles in KBV design (The UK government’s [Identity Proofing and Verification (IPV) Operations Manual](https://www.gov.uk/government/uploads/system/uploads/attachment_data/file/383109/IPV_Operations_Manual_v2.3.1_Redacted.pdf) and [Good Practice Guide (GPG) 45](https://www.ncsc.gov.uk/content/files/guidance_files/GPG%2045%20%20-%20validating%20and%20Verifying%20the%20identity%20of%20an%20individual%20-%20issue%202.4%20-%20NCSC%20Web.pdf) have been used as a reference to build the baseline guidance presented in this document):
- Clarity –process must be clear so that applicant can understand and correctly respond
    - Relevant, sensible, proportionate
    - Carefully constructed, clear, obvious as to what is being asked of the applicant
    - Expectation that owner of claimed identity can reasonably complete process
- Breadth –process should cover a wide range of information
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
- Sources –process must use suitable sources
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

In general the distinction between static and dynamic knowledge-based verification is made based on whether the security questions are stored by the CSP for later access, or generated as applicable to the end user only using specific information, publicly available or otherwise. Static examples such as mother’s maiden name or previous address would not change over time.
While in a broad sense only dynamic KBV is considered for the purposes of identity proofing, it should be noted that there are risks associated with using publicly available data, as there is with secured data that has the risk of compromise. As a general rule of thumb, data used for KBV needs to be as “secret” as possible. Micro-deposits and transaction codes as a form of dynamic KBV are known to work efficiently.
As a guideline, the following can be adopted by CSP’s to perform KBV for resolution or verification.
If the CSP allows the applicant to suspend and resume the process the applicant should not be able to use this feature to gather information relating to the claimed identity.
If the applicant suspends and resumes the process they should either be presented the same questions as before or given new questions which neither have answers that can be deduced from information provided in the previous questions nor reveal answers to previously asked questions.
If the CSP allows the applicant to suspend and resume the process the CSP should not reveal whether the applicant correctly answered any of the previous questions.
The CSP should only allow the applicant to suspend and resume the process twice, totaling a maximum of three attempts. If the CSP presents the same set of questions upon resumption, further questions should be introduced to prevent attackers from using process to extract information and answer previously given questions.
If the applicant fails to return or fails to complete KBV upon return, KBV should be deemed failed.
To calculate the KBV score for the applicant’s answers to a series of questions, let us use the scoring table shown in Table 6.

**Table 6:** KBV Scoring Profile

