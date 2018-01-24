# Introduction

## Purpose

NIST Special Publication 800-63-A Digital Authentication Guideline: Enrollment and Identity Proofing (SP 800-63 or NIST SP 800-63A) provides detailed requirements for enrollment and identity proofing of individuals with which federal identity management systems are expected to comply.

This document provides non-normative guidance to agencies and service providers on possible techniques to implement identity management systems which are aligned with the requirements contained in NIST SP 800-63A. This guide leverages real world examples and illustrative cases to provide practical and actionable guidance to readers. It is complemented by the following additional implementation guides, which, taken in their entirety, provide an end-to-end vision for Federal Identity and Access Management Solutions:

1. Digital Identity Risk Management Implementation Guidance
2. Authentication and Lifecycle Management Implementation Guidance
3. Federation Operations Guidance
4. Federation Implementation Guidance

These documents support the overall vision of NIST SP 800-63-3 by enabling a more comprehensive understanding of what compliant identity solutions could look like in operation. That being said, these documents also do not restrict the manner in which agencies choose to comply with NIST SP 800-63, nor are they intended to restrict agencies from identifying and implementing controls based on an informed and comprehensive risk management process. Just because a technology, control, or process is not mentioned in here does not exclude it from use and does not mean it is non-compliant. 

As technology continues to improve and solutions evolve, agencies are encouraged to explore new techniques and options for mitigating risk, so long as these actions are informed, well documented, and accepted by the appropriate authorities. NIST further encourages readers and implementers to provide feedback and lessons learned to the authors of this document as a way to ensure this guide remains relevant and useful, and to ensure the core Digital Identity Guidelines are updated with new requirements as they are identified. 
## Identity Proofing

Identity proofing is the process by which a Credential Service Provider (CSP) collects and verifies information about a person for the purpose of issuing credentials to that person, as illustrated in Figure 1.

![Figure 1: Individual Identity Proofing Journey](media/figure-1-individual-identity-proofing-journey.png)

**Figure 1:** Individual Identity Proofing Journey

These processes, consistent with the requirements in NIST SP 800-63-3, are intended to help agencies achieve the following objectives:

- **Resolve** a claimed identity to a single, unique identity within the context of the population of users served by the CSP.
- **Validate**
	- that all evidence that is supplied is valid (correct) and genuine (not counterfeit or misappropriated); and
	- that the claimed identity exists in the real world.
- **Verify** that the claimed identity is associated with the real person supplying the identity evidence.

We will discuss identity assurance levels and risk management and the three objectives above in the sections that follow.
