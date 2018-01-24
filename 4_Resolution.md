# Resolution

The goal of resolution is to use the information provided by the applicant to resolve them to a unique, claimed identity. This process may be started automatically upon submission of biographic information during the enrollment process. Unlike validation and verification, the resolution process is focused on ensuring that the information being provided is representative of a real unique individual that can be distinguished from other records to enable the verification of associated attributes and identity evidence. It, in and of itself, is not intended to provide confidence that the individual presenting the information is who they claim to be.

Agencies and CSPs should take into account factors specific to the populations that they serve, or intend to serve, to help design enrollment and proofing processes to allow for the collection of necessary information to uniquely distinguish between individual users—without collecting unnecessary sensitive information. As SP800-63A emphasizes, effective identity resolution uses the smallest set of attributes necessary to resolve to a unique individual. Where possible non-sensitive information should be added to collection if additional attributes are needed to help differentiate users. For example, a population of former military personnel will provide different details and require different resolution data sources than foreign nationals.

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
Fuzzy matching is effective only when the degree of confidence in the inexact match of a single attribute can be supported by the matching of additional attributes that belong to the same identity. In general fuzzy matching tools involve a sequence of steps that align the attributes for proper matching, compare attributes from each source, and generate a confidence score.

![Figure 4: Fuzzy Matching of Attributes Using Name, Date of Birth and Current Address](media/figure-4-fuzzy-matching.png)
**Figure 4:** Fuzzy Matching of Attributes Using Name, Date of Birth and Current Address

The U.S. Department of Veterans’ Affairs and many large health care organizations use attribute matching systems to perform patient identity matching. These systems vary in costs and complexity and fuzzy matching algorithms consider demographic attributes such as name, date of birth, address and phone number. When comparisons indicate a high statistical likelihood that the records are related, the algorithm declares a match between the two records based on thresholds established by the assurance requirements of the use case. In deterministic cases (such as the algorithm used by the Veterans Health Administration) exact matching of identity and demographic data is performed. 

If a CSP chooses to start the identity proofing process with higher confidence, or in the event an identity cannot be resolved using automated matching algorithms or manual inspection by CSP staff, the CSP may request the applicant participate in a KBV process. KBV is more commonly used in the verification step and a more detailed discussion of this process is provided in that section.
