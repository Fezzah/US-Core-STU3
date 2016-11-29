

### General Security Considerations

US-Core transactions often make use of patient-specific information which could be exploited by malicious actors resulting in exposure of patient data. For this reason, all US-Core transactions must be secured appropriately with access to limited authorized individuals, data protected in transit, and appropriate audit measures taken.

Implementers should be aware of the [security considerations] associated with FHIR transactions, particularly those related to:

-   [Communications]
-   [Authentication]
-   [Authorization/Access Control]
-   [Audit Logging]
-   [Digital Signatures]
-   [Security Labels]
-   [Narrative]

For the purposes of US-Core, security conformance requirements are as follows:


- Systems SHALL establish a risk analysis and management regime that conforms with HIPAA security regulatory requirements. In addition US Federal systems SHOULD conform with the risk management and mitigation requirements defined in NIST 800 series documents. This SHOULD include security category assignment in accordance with NIST 800-60 vol. 2 Appendix D.14. The coordination of risk management and the related security and privacy controls – policies, administrative practices, and technical controls – SHALL be defined in the Business Associate Agreements.
- Systems SHALL reference a single time source to establish a common time base for security auditing, as well as clinical data records, among computing systems. The selected time service SHOULD be documented in the Business Associate Agreements.
- Systems SHALL use the [AuditEvent] resource to capture audit logs of the various transactions. Systems SHOULD capture as many AuditEvent resource data elements as appropriate based on local policies. The following events SHOULD trigger an audit event:
   -   Every successful and unsuccessful Resource Request (GET, READ, vREAD etc.)and corresponding Response.
   -   Every Authentication and Authorization request
   -   Security decisions related to consent, digital signatures, data release and security labelling of returned resources



-   Systems SHALL use TLS version 1.2 or higher for all transmissions not taking place over a secure network connection.
    (Using TLS even within a secured network environment is still encouraged to provide defense in depth.) US Federal systems SHOULD conform with FIPS PUB 140-2.
-   Systems SHALL conform to [FHIR Communications] requirements.
-   For Authentication and Authorization, Systems SHALL use the [Smart On FHIR ![]] OAuth2 profiles. NOTE: The Smart On FHIR specifications include the required OAuth2 scopes for enabling security decisions.
-   Systems SHOULD implement requirements from [FHIR Security Labels] to provide information on the type and sensitivity of data.
-   Systems SHALL implement consent requirements per their state, local, and institutional policies. The Business Associate Agreements SHOULD document systems mutual consent requirements. US-Core actors SHALL ensure that any necessary consent records exist and are reviewed prior to each exchange of patient-identifiable healthcare information. This verification should be logged in the same manner as other transactions, as discussed above under [General Security Considerations].
-   Systems SHOULD track the provenance meta data of a resource using[FHIR Provenance] resource and associated requirements.
-   Systems MAY implement the [FHIR Digital Signatures] and provide feedback on it’s appropriateness for US-Core transactions.
-   Systems MAY protect the confidentiality of data at rest via encryption and associated access controls. The policies and methods used are outside the scope of this specification.


  [FHIR Communications]: %7B%7Bsite.data.fhir.path%7D%7Dsecurity.html#http
  [Smart On FHIR]: http://fhir-docs.smarthealthit.org/argonaut-dev/authorization/backend-services/
  [FHIR Security Labels]: %7B%7Bsite.data.fhir.path%7D%7Dsecurity-labels.html
  [General Security Considerations]: #general
  [FHIR Provenance]: %7B%7Bsite.data.fhir.path%7D%7Dprovenance.html
  [FHIR Digital Signatures]: %7B%7Bsite.data.fhir.path%7D%7Dsecurity.html#digital%20signatures

  [security considerations]: %7B%7Bsite.data.fhir.path%7D%7Dsecurity.html
  [Communications]: %7B%7Bsite.data.fhir.path%7D%7Dsecurity.html#http
  [Authentication]: %7B%7Bsite.data.fhir.path%7D%7Dsecurity.html#authentication
  [Authorization/Access Control]: %7B%7Bsite.data.fhir.path%7D%7Dsecurity.html#authorization/access%20control
  [Audit Logging]: %7B%7Bsite.data.fhir.path%7D%7Dsecurity.html#audit%20logging
  [Digital Signatures]: %7B%7Bsite.data.fhir.path%7D%7Dsecurity.html#digital%20signatures
  [Security Labels]: %7B%7Bsite.data.fhir.path%7D%7Dsecurity-labels.html
  [Narrative]: %7B%7Bsite.data.fhir.path%7D%7Dsecurity.html#narrative
  [AuditEvent]: %7B%7Bsite.data.fhir.path%7D%7Dauditevent.html
