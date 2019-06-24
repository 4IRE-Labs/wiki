# GDPR Compliance Audit

## Basics

In essence, GDPR is a strict data privacy code that holds companies responsible for securing the data they store and process.

Securing primary systems is one thing— we know all the cybersecurity cliches about endpoints and perimeters. GDPR, however, is solely focused on data, which means that any surface over which that data passes must be protected from exposure, even if it’s in the hands of a vendor. Vendors in this sense include both managed services, like outsourced IT, and hosted services, like cloud servers and storage. The enterprise technology ecosystem has evolved to include a complex interrelationship of hosted and managed services, in addition to traditional on-premise network and data center architectures— all of these must be factored into GDPR compliance [\*upguard.com](https://www.upguard.com/blog/vendor-risk-the-hidden-challenge-of-gdpr-compliance).

## Addressing risks in GDPR

If your business operates in EU and you choose a software development vendor you want to be sure that this vendor will share the responsibility for security of your users' data.

In 4irelabs we take care of GDPR risks and we have a process that can guarantee that during our development and operational processes we perform technical and organizational measures regarding the data security.

During the development process, we take care of the encryption of the user's personal data.

* No passwords in plain-text
* No unencrypted documents stored in the infrastructure 
* We provide reports on-demand regarding what personal data is stored and where it's stored
* We watch that the right to be forgotten is performed
* We give you the report of what database rows and documents on hard drives and in cloud storages are deleted when a user requested it.
* We take care of how our developers access the data on infrastructure by using advanced logging and auditing tools. 

When you need to host some important data \(eg. legal documents\), we can use additional instruments that can guarantee advanced logging and security, like AWS or GCP KMS. We also can maintain such systems on your on-premise infrastructure.

## Access to data

All our developers who have access to the infrastructure or to the production database or cloud storage buckets use 2-factor authentication. Decryption and encryption of any personal data are stored in the special logging tools that you can audit.

## Security audits

We're open for external security audits and take responsibility for fixing critical security issues found.

## Communication of a personal data breach to the data subject

In case of security breach found, 4ire labs team fixes the issue ASAP no more than 1 week and notify all users whose data is affected.

## Process

This policy is applied to the projects where a customer wants to make 4irelabs to be responsible for GDPR compliance as a vendor.

A project manager or consultant on the project must ensure that all point from the checklist is executed. In other cases, the person responsible for the project must negotiate additional SoW with the customer to be compliant with GDPR and be able to execute responsibilities described in the GDPR document. PM or consultant must create the document that describes all the points from the checklist and technical and organizational measures regarding the data security. The part of the document with organizational measures must be signed off by partners and customer and included in the annex.

* [Checklist](https://4irelabs.atlassian.net/wiki/spaces/SP/pages/6258698/GDPR+Draft#Checklist)
* [Technical and organizational measures regarding data security](https://4irelabs.atlassian.net/wiki/spaces/SP/pages/6258698/GDPR+Draft#Technical-and-organizational-measures-regarding-data-security)
  * [The right to rectification, portability, and to be forgotten](https://4irelabs.atlassian.net/wiki/spaces/SP/pages/6258698/GDPR+Draft#The-right-to-rectification,-portability,-and-to-be-forgotten)
  * [Access to data](https://4irelabs.atlassian.net/wiki/spaces/SP/pages/6258698/GDPR+Draft#Access-to-data)
  * [Communication of a personal data breach to the data subject](https://4irelabs.atlassian.net/wiki/spaces/SP/pages/6258698/GDPR+Draft#Communication-of-a-personal-data-breach-to-the-data-subject)
* [Example of the GDPR document](https://4irelabs.atlassian.net/wiki/spaces/SP/pages/6258698/GDPR+Draft#Example-of-the-GDPR-document)

### Checklist <a id="Checklist"></a>

1. All servers which process users personal data are located in the EU \(not including GB\).
2. All data is backed app at least 1 time per week.
3. All user’s personal data stored in the database is described in the separate document. Fields that are considered as sensitive are marked as “Deleted after the right to be forgotten”
4. Personal data stored on the cloud storages or physical storages is encrypted
5. All access keys or other information that can be used to access the infrastructure or 3rd party services or encryption keys are stored in a secure place. Access to this information is given only to people who need it
6. All 3rd party providers integrated into the project are GDPR compliant
7. Right to be forgotten is implemented and available to users
8. Users passwords are stored as hashes in the database
9. Audit trail of who and when had access to sensitive personal data is updating and stored somewhere in the secure place
10. Employees who have access to the infrastructure or to the place where personal data is stored have their own keys and use 2FA.

### Technical and organizational measures regarding data security <a id="Technical-and-organizational-measures-regarding-data-security"></a>

#### The right to rectification, portability, and to be forgotten <a id="The-right-to-rectification,-portability,-and-to-be-forgotten"></a>

A user always can rectify his personal data in the account at the website. There is also a button “delete account” that could be used to delete all data about a user on the website. The data that will be deleted is described in the appropriate section. All user’s documents will be also deleted from the cloud storage. All user’s documents can be downloaded from the website if the user wants to reuse them.

However, if there is no possibility to get some data using the built-in website functions the user could write a request to get this data using the feedback form or using the contact info provided on the website. The 4irelabs support team will handle this request in 2 weeks period.

#### Access to data <a id="Access-to-data"></a>

The engineers in charge of production applications are controlled each time they access the production environments. A centralized role management system is used to define and control engineer access to production services. 2-factor authentication is used to access the production environment. Engineers issue short-time tokens using google authenticator to get access to the production environment.

#### Communication of a personal data breach to the data subject <a id="Communication-of-a-personal-data-breach-to-the-data-subject"></a>

In case of security breach found, the smart-agreements team must fix the issue ASAP no more than 1 week and notify all users whose data is affected.

### Example of the GDPR document <a id="Example-of-the-GDPR-document"></a>

[https://docs.google.com/document/d/19PwxIqyypI2-h8SPzUDXOabMeGm6EJbzkK3mdjQR\_\_U/edit?usp=sharing](https://docs.google.com/document/d/19PwxIqyypI2-h8SPzUDXOabMeGm6EJbzkK3mdjQR__U/edit?usp=sharing)

## Conclusion

At first, you can treat GDPR compliance as something scary, but with an experienced vendor whom you can believe, you can transform it into a good competitive advantage of your business.

For more information please contact our sales department.

