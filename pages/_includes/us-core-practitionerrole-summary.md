#### Summary of the Mandatory Requirements 

1.  One practitioner in `PractitionerRole.practitioner`
1.  One organization in `PractitionerRole.organization`
1.  One practitioner role code in `PractitionerRole.code` which has an [extensible]({{ site.data.fhir.path }}/terminologies.html#extensible) binding to:
    -    [NUCC - Classification](http://www.fhir.org/guides/argonaut/pd/ValueSet-provider-role.html) value set **Need to ask Argonauts**
1.  One practitioner specialty code in `PractitionerRole.specialty` which has an [extensible]({{ site.data.fhir.path }}/terminologies.html#extensible) binding to:
    -    [NUCC - Specialization](http://www.fhir.org/guides/argonaut/pd/ValueSet-provider-specialty.html) value set **Need to ask Argonauts**
1.  One reference to a location in `PractitionerRole.location`
1.  At least one contact using either 'PractitionerRole.telecom' OR or reference to an Endpoint Resource in  `PractitionerRole.endpoint`
  