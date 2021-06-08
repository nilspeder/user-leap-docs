# Technical Considerations

## Technical Considerations

### Data Security, PII, and GDPR

UserLeap is Privacy Shield certified, PCI DSS compliant, and regularly runs 3rd-party penetration tests to proactively identify possible vulnerabilities. All communication between the UserLeap SDK and the UserLeap backend is done securely over SSL and your data is stored in a database that is encrypted at rest.

UserLeap will not implicitly collect any personally identifiable information \(PII\) about your users. If you wish to send user PII to UserLeap, it must be done explicitly through one of the UserLeap data collection APIs for attributes or events. 

In compliance with GDPR and other data regulatory frameworks, UserLeap offers functionality for data access, erasure, and opt-out for Enterprise customers. Please reach out to your customer service representative to learn more.

### Network Reliability & Retries

The UserLeap SDK has built-in queueing and retry functionality to make it resilient to network disruptions. This helps to ensure that you’re always working the most current user data.

### **Minimum Requirements:** 

TLS

The minimum supported TLS protocol version for communicating with UserLeap services is TLSv1.2\_2019. The following TLS versions are not supported:

* TLSv1
* TLSv1\_2016
* TLSv1.1\_2016
* TLSv1.2\_2018

