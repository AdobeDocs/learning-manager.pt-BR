---
description: Saiba mais sobre as APIs não conectadas para desenvolver a interface sem periféricos.
jcr-language: en_us
title: APIs não conectadas
source-git-commit: 21e2a4a5e73fcbddb64e0afec0a896b315e38688
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 0%

---

# APIs não conectadas

Saiba mais sobre as APIs do Adobe Learning Manager, que fornecem dados para a experiência sem periféricos ou não conectada neste artigo.
API de pesquisa pública

## API de pesquisa pública

### Filtrar dados usando ES público

A API de pesquisa pública permite obter os dados de filtro que podem ser usados com a API de pesquisa básica para filtrar os cursos. Esta API fornece todos os filtros que podem ser usados na API de pesquisa.

**Exemplo de curva**

Use o método GET para fazer a seguinte solicitação. Substitua &lt;Base_URL> pelo URL base no comando curl abaixo. Você pode encontrar o &lt;Base_URL> na página do conector de acesso a dados de treinamento.

```
curl --location '<Base_URL>/filterableData'
```

**Exemplo de resposta**

```
{
    "terms": {
        "loSkillLevels": [
            "1"
        ],
        "catalogNames": [
            "Default Catalog"
        ],
"catalogLabelIds": [
            "0000_1111"
        ],
        "loType": [
            "course"
        ],
        "availability": [
            "waitlistAvailable",
            "seatAvailable"
        ],
        "loSkillNames": [
            "General"
        ],
        "tags": [
            "course_tag"
        ],
        "authors": [
            "author_1"        
]
    },
    "range": {
        "duration": [
            "0"
        ],
        "dateCreated": [
            "2024-06-13T04:32:17.000Z"
        ],
        "price": [
            "0.0"
        ],
        "sessionEndTime": [
            "2024-06-18T20:30:00.000Z"
        ],
        "averageRating": [
            "0.0"
        ],
        "sessionStartTime": [
            "2024-06-18T19:30:00.000Z"
        ],
        "publishDate": [
            "2024-06-13T04:32:51.000Z"
        ],
        "ratingsCount": [
            "0"
        ]
    },
    "term": {}
}
```

**Opções de filtro**

| Opções | Descrição |
| --- | --- |
| `loSkillLevels` | O nível de proficiência necessário para se inscrever no curso. |
| `catalogNames` | Lista de nomes de catálogo disponíveis. |
| `loType` | Tipos de objetos de aprendizado disponíveis. |
| `availability` | A disponibilidade de vagas e a disponibilidade de listas de espera. |
| `loSkillNames` | Os nomes das habilidades adicionados aos objetos de aprendizado. |
| `tags` | As tags associadas aos objetos de aprendizado. |
| `authors` | O nome do autor dos objetos de aprendizado |
| `duration` | A duração dos objetos de aprendizado. |
| `dateCreated` | A data de criação do objeto de aprendizado. |
| `sessionEndTime` | A hora em que a sessão foi encerrada. |
| `averageRating` | A classificação por estrelas média dos objetos de aprendizado. |
| `sessionStartTime` | A hora em que a sessão foi iniciada. |
| `publishDate` | A data de publicação do objeto de aprendizado. |
| `ratingsCount` | O número de contagens de classificações do objeto de aprendizado. |

### API de pesquisa

A API de pesquisa pública permite obter dados de pesquisa básica usando os dados fornecidos.

**Exemplo de Ondulação**

Use o método POST para fazer a seguinte solicitação. Substitua &lt;Base_URL> pelo URL base no comando curl abaixo. Você pode encontrar o &lt;Base_URL> na página do conector de acesso a dados de treinamento.

```
curl --location '<Base_URL>/search?size=1000' \
--header 'content-type: application/json' 

--data '{
   "query": "",
   
    "sort": {
        "name": "publishDate",
        "order": "desc"
    },
    "lang": [
        "en-US"
    ],
    "filters": {
        "terms": {
            "loType": [
                "course",
                "learningProgram",
                "certification"
            ],
            "availability": [
                "seatAvailable",
                "waitlistAvailable"
            ]
        },
        "term": {
            "enrollmentDeadlinePassed": "true"
        },
        "range": {
                "dateCreated": [
                    {
                        "gte": "2024-05-02T02:48:51.000Z"
                    }
                ],
            "sessionStartTime": [
                {
                   "gte": "2024-06-18T19:30:00.000Z"
                }
            ],
            "sessionEndTime": [
                {
                   "lte": "2024-06-20T09:30:00.000Z"     
                }
            ]
        }
    }
}'
```

**Exemplo de resposta da chamada de API**

```
{
    "results": [
        {
            "loId": "course:11332313",
            "loType": "course",
            "tags": [
                "course_tag"
            ],
            "authors": [
                "author1",
                "author2"
            ],
            "status": "Published",
            "duration": 0,
            "publishDate": "2024-06-13T04:32:51.000Z",
            "dateCreated": "2024-06-13T04:32:17.000Z",
            "name": "vc coursse to check ",
            "averageRating": 0.0,
            "ratingsCount": 0,
            "loSkillNames": [
                "General"
            ],
            "loSkillLevels": [
                "1"
            ],
            "loInstances": [
                {
                    "id": "14346696",
                    "name": "Default Instance",
                    "status": "Active",
                    "price": 0.0
                }
            ],
            "catalogInfo": [
                {
                    "id": "37779",
                    "name": "Default Catalog"
                }
            ]
        }
    ],
    "request": {
        "query": "",
        "filters": {
            "terms": {
                "loType": [
                    "course",
                    "learningProgram",
                    "certification"
                ],
                "loSkillNames": [
                    "General"
                ],
                "deliveryType": [],
                "availability": [
                    "seatAvailable",
                    "waitlistAvailable"
                ]
            },
            "term": {
                "enrollmentDeadlinePassed": "true"
            },
            "range": {
                "dateCreated": [
                    {
                        "gte": "2024-05-02T02:48:51.000Z"
                    }
                ],
                "sessionStartTime": [
                    {
                        "gte": "2024-06-18T19:30:00.000Z"
                    }
                ],
                "sessionEndTime": [
                    {
                        "lte": "2024-06-20T09:30:00.000Z"
                    }
                ]
            }
        },
        "sort": {
            "name": "publishDate",
            "order": "desc"
        },
        "lang": [
            "en-US"
        ]
    },
    "self": "<Base_URL>/search?page=0&size=1000",
    "count": 1
}
```

**Opções de classificação na API de Pesquisa**

Você pode selecionar as seguintes opções de classificação a serem aplicadas aos resultados.

| Opções | Descrição |
| --- | --- |
| `duration` | A duração do objeto de aprendizado. |
| `publishDate` | A data de publicação do objeto de aprendizado. |
| `dateCreated` | A data de criação do objeto de aprendizado. |
| `name_en` | O nome do objeto de aprendizado. |
| `averageRating` | Classificação de estrelas média fornecida pelos alunos. |
| `ratingsCount` | O número de contagens de classificações do objeto de aprendizado. |
| `relevance(default)` | Os dados relevantes são baseados nas palavras-chave de pesquisa. |

### Obter dados do objeto de aprendizado usando a API de pesquisa pública

A API pública de objeto de aprendizado ES permite obter a lista de tipos e IDs de objetos de aprendizado disponíveis na interface sem periféricos.

**Exemplo de curva**

Use o método GET para fazer a seguinte solicitação. Substitua &lt;Base_URL> pelo URL base no comando curl abaixo. Você pode encontrar o &lt;Base_URL> na página do conector de acesso a dados de treinamento.

```
curl --location '<Base_URL>/learningObjectIds'
```

**Exemplo de resposta para a chamada de API**

```
{
    "loIds": [
        "course:1132800",
"certification:126009",
"learningProgram:104433"
    ]
}
```

## API de resumo do curso

A API de resumo do curso permite recuperar informações detalhadas sobre um curso específico.

**Exemplo de curva**

Use o método GET para fazer a seguinte solicitação. Substitua &lt;Base_URL> pelo URL base no comando curl abaixo. Você pode encontrar o &lt;Base_URL> na página do conector de acesso a dados de treinamento. Substitua &lt;Course_ID> pela ID específica do curso.

```
curl --location '<Base_URL>/loSummary?loId=course%3A<Course_ID>'
```

**Exemplo de resposta da chamada de API**

```
{
    "results": [
        {
            "instanceId": "14336686",
            "courseId": "11312313",
            "accountId": "44355",
            "seatConsumed": 1,
            "seatLimit": 1,
            "waitlistLimit":1,
            "waitlistCount": 1,
            "seatAvailable": false,
            "waitlistAvailable": false
        }
    ],
    "count": 1
}
```

>[!NOTE]
>
>Se um curso tiver várias instâncias, você obterá detalhes para todas as instâncias.

## API JSON CDN para detalhes do curso

A API JSON CDN permite recuperar as informações completas do curso sobre um curso específico.

**Exemplo de curva para o curso**

Use o método GET para fazer a seguinte solicitação. Substitua &lt;CDN_path> pelo URL base no comando de curvas abaixo. Você pode encontrar o &lt;CDN_path> na página do conector de acesso a dados de treinamento. Substitua &lt;Course_ID> pela ID específica do curso.

```
curl --location '<CDN_path_URL>/course/<Course_ID>.json'
```

**Exemplo de curva para caminho de aprendizado e certificação**

```
curl --location '<CDN_path_URL>/learningProgram/<LearningProgram_ID>.json'
```

```
curl --location '<CDN_path_URL>/ certification /<Certification_ID>.json'
```

**Exemplo de resposta da chamada de API**

```
{
    "data": {
        "id": "course:11342313",
        "type": "learningObject",
        "attributes": {
            "authorNames": [
                "author1",
                "author2"
            ],
            "dateCreated": "2024-06-13T04:32:17.000Z",
            "datePublished": "2024-06-13T04:32:51.000Z",
            "dateUpdated": "2024-06-13T04:32:51.000Z",
            "duration": 0,
            "effectiveModifiedDate": "2024-06-13T04:32:51.000Z",
            "effectivenessIndex": 0,
            "enrollmentType": "Self Enroll",
            "hasOptionalLoResources": false,
            "hasPreview": false,
            "isExternal": false,
            "isMqaEnabled": false,
            "isPrerequisiteEnforced": false,
            "isSubLoOrderEnforced": false,
            "loResourceCompletionCount": 1,
            "loType": "course",
            "moduleResetEnabled": false,
            "state": "Published",
            "tags": [
                "course_tag"
            ],
            "unenrollmentAllowed": true,
            "localizedMetadata": [
                {
                    "description": "",
                    "locale": "en-US",
                    "name": "vc coursse to check "
                }
            ],
            "rating": {
                "averageRating": 0,
                "ratingsCount": 0
            }
        },
        "relationships": {
            "authors": {
                "data": [
                    {
                        "id": "13138897",
                        "type": "user"
                    }
                ]
            },
            "instances": {
                "data": [
                    {
                        "id": "course:11332313_14336696",
                        "type": "learningObjectInstance"
                    }
                ]
            },
            "skills": {
                "data": [
                    {
                        "id": "course:11332313_237719",
                        "type": "learningObjectSkill"
                    }
                ]
            }
        }
    },
    "included": [
        {
            "id": "237719",
            "type": "skill",
            "attributes": {
                "name": "General",
                "state": "Active"
            },
            "relationships": {
                "levels": {
                    "data": [
                        {
                            "id": "237719_1",
                            "type": "skillLevel"
                        }
                    ]
                }
            }
        },
        {
            "id": "course:11312313",
            "type": "learningObject",
            "attributes": {
                "authorNames": [
                    "m 41",
                    "rae"
                ],
                "dateCreated": "2024-06-13T04:32:17.000Z",
                "datePublished": "2024-06-13T04:32:51.000Z",
                "dateUpdated": "2024-06-13T04:32:51.000Z",
                "duration": 0,
                "effectiveModifiedDate": "2024-06-13T04:32:51.000Z",
                "effectivenessIndex": 0,
                "enrollmentType": "Self Enroll",
                "hasOptionalLoResources": false,
                "hasPreview": false,
                "isExternal": false,
                "isMqaEnabled": false,
                "isPrerequisiteEnforced": false,
                "isSubLoOrderEnforced": false,
                "loResourceCompletionCount": 1,
                "loType": "course",
                "moduleResetEnabled": false,
                "state": "Published",
                "tags": [
                    "course_tag"
                ],
                "unenrollmentAllowed": true,
                "localizedMetadata": [
                    {
                        "description": "",
                        "locale": "en-US",
                        "name": "course name "
                    }
                ],
                "rating": {
                    "averageRating": 0,
                    "ratingsCount": 0
                }
            },
            "relationships": {
                "authors": {
                    "data": [
                        {
                            "id": "13128897",
                            "type": "user"
                        }
                    ]
                },
                "instances": {
                    "data": [
                        {
                            "id": "course:11312313_14336696",
                            "type": "learningObjectInstance"
                        }
                    ]
                },
                "skills": {
                    "data": [
                        {
                            "id": "course:11312313_237719",
                            "type": "learningObjectSkill"
                        }
                    ]
                }
            }
        },
        {
            "id": "course:11312313_14336696_12034506_0",
            "type": "learningObjectResource",
            "attributes": {
                "externalReporting": false,
                "isExpiredSubmission": false,
                "loResourceType": "Content",
                "multipleAttemptEnabled": false,
                "previewEnabled": false,
                "resourceType": "Virtual Classroom",
                "submissionEnabled": false,
                "localizedMetadata": [
                    {
                        "description": "",
                        "locale": "en-US",
                        "name": "vc session"
                    }
                ]
            },
            "relationships": {
                "learningObject": {
                    "data": {
                        "id": "course:11312313",
                        "type": "learningObject"
                    }
                },
                "resources": {
                    "data": [
                        {
                            "id": "course:11312313_14336696_12034506_0_resource",
                            "type": "resource"
                        }
                    ]
                }
            }
        },
        {
            "id": "course:11312313_237719",
            "type": "learningObjectSkill",
            "attributes": {
                "credits": 1,
                "learningObjectId": "course:11312313"
            },
            "relationships": {
                "skillLevel": {
                    "data": {
                        "id": "237719_1",
                        "type": "skillLevel"
                    }
                }
            }
        },
        {
            "id": "13128897",
            "type": "user",
            "attributes": {
                "avatarUrl": "https://abccontents.adobe.com/public/images/default_user_avatar.svg",
                "binUserId": "1f8c01aa-7f58-42e9-bc40-11537eb6498d",
                "email": "manjusha+41re@adobetest.com",
                "enrollOnClick": false,
                "gamificationEnabled": true,
                "lastLoginDate": "2024-06-13T04:23:45.000Z",
                "name": "m 41",
                "pointsEarned": 0,
                "pointsRedeemed": 0,
                "preferredResolution": "AUTO",
                "profile": "admin",
                "roles": [
                    "Learner",
                    "Admin",
                    "Author",
                    "Instructor",
                    "Integration Admin"
                ],
                "state": "ACTIVE",
                "userType": "Internal"
            },
            "relationships": {
                "account": {
                    "data": {
                        "id": "44355",
                        "type": "account"
                    }
                }
            }
        },
        {
            "id": "course:11312313_14336696_12034506_0_resource",
            "type": "resource",
            "attributes": {
                "avatarUrls": [
                    "https://abccontents.adobe.com/public/images/default_user_avatar.svg"
                ],
                "completionDeadline": "2024-06-18T20:30:00.000Z",
                "contentType": "Virtual Classroom",
                "dateStart": "2024-06-18T19:30:00.000Z",
                "desiredDuration": 3600,
                "hasQuiz": false,
                "hasToc": false,
                "instructorNames": [
                    "instructor1"
                ],
                "isDefault": true,
                "locale": "en-US",
                "location": "http://google.com",
                "name": "vc session",
                "onlyQuiz": false,
                "reportingType": "NONE"
            }
        },
        {
            "id": "course:11312313_14336696",
            "type": "learningObjectInstance",
            "attributes": {
                "dateCreated": "2024-06-13T04:32:18.000Z",
                "isDefault": true,
                "isFlexible": false,
                "state": "Active",
                "localizedMetadata": [
                    {
                        "locale": "en-US",
                        "name": "Default Instance"
                    }
                ],
                "seatConsumed": 0,
                "waitlistCount": 0
            },
            "relationships": {
                "learningObject": {
                    "data": {
                        "id": "course:11312313",
                        "type": "learningObject"
                    }
                },
                "loResources": {
                    "data": [
                        {
                            "id": "course:11312313_14336696_12034506_0",
                            "type": "learningObjectResource"
                        }
                    ]
                }
            }
        },
        {
            "id": "237719_1",
            "type": "skillLevel",
            "attributes": {
                "level": "1",
                "maxCredits": 1,
                "name": "Level 1"
            },
            "relationships": {
                "skill": {
                    "data": {
                        "id": "237719",
                        "type": "skill"
                    }
                }
            }
        }
    ]
}
```
