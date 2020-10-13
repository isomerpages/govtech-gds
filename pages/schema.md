---
title: Schema
permalink: /schema/
---

```json
{
    "id": "TEST001",
    "name": "HealthCert",
    "$template": {
        "name": "HealthCert_v1.0",
        "type": "EMBEDDED_RENDERER",
        "url": "https://render.openattestation.io"
    },
    "issuers": [
        {
            "name": "IssuerCompanyName",
            "documentStore": "0x0B209E53aaae5E9744d70509b74d66358df0bb27",
            "network": "ETHEREUM",
            "identityProof": {
                "type": "DNS-TXT",
                "location": "ropstore.openattestation.io"
            }
        }
    ],
    "fhirVersion": "4.0.1",
    "fhirBundle": {
        "resourceType": "Bundle",
        "type": "collection",
        "entry": [
            {
                "resourceType": "Patient",
                "extension": [
                    {
                        "url": "http://hl7.org/fhir/StructureDefinition/patient-nationality",
                        "code": {
                            "text": "SG"
                        }
                    }
                ],
                "identifier": [
                    {
                        "type": "PPN",
                        "value": "E7831177G"
                    },
                    {
                        "type": {
                            "text": "NRIC"
                        },
                        "value": "S9098989Z"
                    }
                ],
                "name": [
                    {
                        "text": "Tan Chen Chen"
                    }
                ],
                "gender": "female",
                "birthDate": "1990-01-15"
            },
            {
                "resourceType": "Specimen",
                "type": {
                    "coding": [
                        {
                            "system": "http://snomed.info/sct",
                            "code": "258500001",
                            "display": "Nasopharyngeal swab"
                        }
                    ]
                },
                "collection": {
                    "collectedDateTime": "2020-09-27T06:15:00Z"
                }
            },
            {
                "resourceType": "Observation",
                "identifier": [
                    {
                        "value": "123456789",
                        "type": "ACSN"
                    }
                ],
                "code": {
                    "coding": [
                        {
                            "system": "http://loinc.org",
                            "code": "94531-1",
                            "display": "Reverse transcription polymerase chain reaction (rRT-PCR) test"
                        }
                    ]
                },
                "valueCodeableConcept": {
                    "coding": [
                        {
                            "system": "http://snomed.info/sct",
                            "code": "260385009",
                            "display": "Negative"
                        }
                    ]
                },
                "effectiveDateTime": "2020-09-28T06:15:00Z",
    “status”: “final”,
                "performer": {
                    "name": [
                        {
                            "text": "Dr Michael Lim"
                        }
                    ]
                },
                "qualification": [
                    {
                        "identifier": "MCR 123214",
                        "issuer": "MOH"
                    }
                ]
            },
            {
                "resourceType": "Organization",
                "name": "MacRitchie Medical Clinic",
                "type": "Licensed Healthcare Provider",
                "endpoint": {
                    "address": "https://www.macritchieclinic.com.sg"
                },
                "contact": {
                    "telecom": [
                        {
                            "system": "phone",
                            "value": "+6563113111"
                        }
                    ],
                    "address": {
                        "type": "work",
                        "use": "physical",
                        "text": "MacRitchie Hospital Thomson Road Singapore 123000"
                    }
                }
            },
            {
                "resourceType": "Organization",
                "name": "MacRitchie Laboratory",
                "type": "Accredited Laboratory",
                "contact": {
                    "telecom": [
                        {
                            "system": "phone",
                            "value": "+6562711188"
                        }
                    ],
                    "address": {
                        "type": "work",
                        "use": "physical",
                        "text": "2 Thomson Avenue 4 Singapore 098888"
                    }
                }
            }
        ]
    }
}
```
