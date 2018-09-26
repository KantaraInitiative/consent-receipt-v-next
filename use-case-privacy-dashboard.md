# Use case: Privacy Dashboard

Author: 
Andrew Hughes

Date: 
2018-09-25

# Actors
* PII Principal (a.k.a. Data Subject)
* Privacy dashboard service provider
* PII Controller (a.k.a. Data Controller)

# Terminology
* Consent Receipt: A JSON/JWT document that conforms to the Kantara Initiative Consent Receipt Specification
* Consented Interaction: An event where the PII Principal has agreed to grant permission for the PII Controller to process the PII Principal's data. 

# Description
A privacy dashboard service provider presents Consent Receipts of Consented Interactions to the PII Principal. The privacy dashboard provides a useable and organized view of the PII Principal's Consented Interactions.

For any Consented Interaction, the privacy dashboard offers actions to the PII Principal to allow automated exercising of the PII Principal's Data Subject Rights. 

For example, in GDPR, Data Subject Rights are: 

1. **Right to information**
This right provides the data subject with the ability to ask a company for information about what personal data (about him or her) is being processed and the rationale for such processing. For example, a customer may ask for the list of processors with whom his or her personal data is shared.

2. **Right to access**
This right provides the data subject with the ability to get access to his or her personal data that is being processed. This request provides the right for data subjects to see or view their own personal data, as well as to request copies of the personal data.

3. **Right to rectification**
This right provides the data subject with the ability to ask for modifications to his or her personal data in case the data subject believes that this personal data is not up to date or accurate.

4. **Right to withdraw consent**
This right provides the data subject with the ability to withdraw a previously given consent for processing of their personal data for a purpose. The request would then require the company to stop the processing of the personal data that was based on the consent provided earlier.

5. **Right to object**
This right provides the data subject with the ability to object to the processing of their personal data. Normally, this would be the same as the right to withdraw consent, if consent was appropriately requested and no processing other than legitimate purposes is being conducted. However, a specific scenario would be when a customer asks that his or her personal data should not be processed for certain purposes while a legal dispute is ongoing in court.

6. **Right to object to automated processing**
This right provides the data subject with the ability to object to a decision based on automated processing. Using this right, a customer may ask for his or her request (for instance, a loan request) to be reviewed manually, because he or she believes that automated processing of his or her loan may not consider the unique situation of the customer.

7. **Right to be forgotten**
Also known as right to erasure, this right provides the data subject with the ability to ask for the deletion of their data. This will generally apply to situations where a customer relationship has ended. It is important to note that this is not an absolute right, and depends on your retention schedule and retention period in line with other applicable laws.

8. **Right for data portability**
This right provides the data subject with the ability to ask for transfer of his or her personal data. As part of such request, the data subject may ask for his or her personal data to be provided back (to him or her) or transferred to another controller. When doing so, the personal data must be provided or transferred in a machine-readable electronic format.


# Outcome
On invoking the data subject right action, the Privacy Dashboard service provider creates a message for transmittal to the Data Controller, indicating that the Data Subject is invoking a Data Subject Right, and that the Data Controller should take appropriate action.
