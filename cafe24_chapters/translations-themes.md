# TRANSLATIONS THEMES


## Translations themes

```json
Endpoints    GET /api/v2/admin/translations/themes
GET /api/v2/admin/translations/themes/{skin_no}
PUT /api/v2/admin/translations/themes/{skin_no}
```

```json
GET /api/v2/admin/translations/themes
GET /api/v2/admin/translations/themes/{skin_no}
PUT /api/v2/admin/translations/themes/{skin_no}
```

### Translations themes property list

| Attribute | Description |
| --- | --- |
| skin_no | 디자인 번호 |
| translations | 번역 정보 |
| skin_code | 디자인 코드 |
| skin_translation | 디자인 번역 정보 |

### Retrieve a list of theme translations   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 번역 읽기권한 (mall.read_translation) |
| 호출건수 제한 | 40 |

```bash
Retrieve a list of theme translations        Retrieve a list of theme translations       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/translations/themes' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "themes": [        {            "skin_no": 3,            "translations": [                {                    "language_code": "en_US",                    "path": "/locale/en_US.json"                },                {                    "language_code": "es_ES",                    "path": "/locale/es_ES.json"                }            ]        },        {            "skin_no": 5,            "translations": [                {                    "language_code": "en_US",                    "path": "/locale/en_US.json"                },                {                    "language_code": "es_ES",                    "path": "/locale/es_ES.json"                }            ]        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/translations/themes' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "themes": [        {            "skin_no": 3,            "translations": [                {                    "language_code": "en_US",                    "path": "/locale/en_US.json"                },                {                    "language_code": "es_ES",                    "path": "/locale/es_ES.json"                }            ]        },        {            "skin_no": 5,            "translations": [                {                    "language_code": "en_US",                    "path": "/locale/en_US.json"                },                {                    "language_code": "es_ES",                    "path": "/locale/es_ES.json"                }            ]        }    ]}
```

### Retrieve a theme translation   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 번역 읽기권한 (mall.read_translation) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| skin_noRequired | 디자인 번호 |
| language_codeRequired | 언어 코드 |

```bash
Retrieve a theme translation        Retrieve a theme translation       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/translations/themes/3?language_code=en_US' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "theme": {        "skin_no": 3,        "skin_code": "skin1",        "skin_translation": {            "language_code": "en_US",            "path": "/locale/en_US.json",            "source": "{\\n    \\\"MEMBER_ID\\\": {\\n        \\\"FIND_YOUR_ID\\\": \\\"Find your ID\\\",\\n        \\\"NAME\\\": \\\"Name\\\",\\n        \\\"EMAIL_ADDRESS\\\": \\\"Email address\\\",\\n        \\\"LOG_IN\\\": \\\"Log in\\\",\\n        \\\"FORGOT_PASSWORD\\\": \\\"Forgot password?\\\"\\n    }\\n}"        }    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/translations/themes/3?language_code=en_US' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "theme": {        "skin_no": 3,        "skin_code": "skin1",        "skin_translation": {            "language_code": "en_US",            "path": "/locale/en_US.json",            "source": "{\\n    \\\"MEMBER_ID\\\": {\\n        \\\"FIND_YOUR_ID\\\": \\\"Find your ID\\\",\\n        \\\"NAME\\\": \\\"Name\\\",\\n        \\\"EMAIL_ADDRESS\\\": \\\"Email address\\\",\\n        \\\"LOG_IN\\\": \\\"Log in\\\",\\n        \\\"FORGOT_PASSWORD\\\": \\\"Forgot password?\\\"\\n    }\\n}"        }    }}
```

### Update a theme translation   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 번역 쓰기권한 (mall.write_translation) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| skin_noRequired | 디자인 번호 |
| skin_translation | 디자인 번역 정보 |
| skin_translation 하위 요소 보기     language_codeRequired언어 코드 sourceRequired소스 코드 |

```bash
Update a theme translation        Update a theme translation       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/translations/themes/3' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "request": {        "skin_translation": {            "language_code": "en_US",            "source": "{\\n    \\\"MEMBER_ID\\\": {\\n        \\\"FIND_YOUR_ID\\\": \\\"Find your ID\\\",\\n        \\\"NAME\\\": \\\"Name\\\",\\n        \\\"EMAIL_ADDRESS\\\": \\\"Email address\\\",\\n        \\\"LOG_IN\\\": \\\"Log in\\\",\\n        \\\"FORGOT_PASSWORD\\\": \\\"Forgot password?\\\"\\n    }\\n}"        }    }}'    Response  Copy     {    "theme": {        "skin_no": 3,        "skin_code": "skin1",        "skin_translation": {            "language_code": "en_US",            "path": "/locale/en_US.json",            "source": "{\\n    \\\"MEMBER_ID\\\": {\\n        \\\"FIND_YOUR_ID\\\": \\\"Find your ID\\\",\\n        \\\"NAME\\\": \\\"Name\\\",\\n        \\\"EMAIL_ADDRESS\\\": \\\"Email address\\\",\\n        \\\"LOG_IN\\\": \\\"Log in\\\",\\n        \\\"FORGOT_PASSWORD\\\": \\\"Forgot password?\\\"\\n    }\\n}"        }    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/translations/themes/3' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "request": {        "skin_translation": {            "language_code": "en_US",            "source": "{\\n    \\\"MEMBER_ID\\\": {\\n        \\\"FIND_YOUR_ID\\\": \\\"Find your ID\\\",\\n        \\\"NAME\\\": \\\"Name\\\",\\n        \\\"EMAIL_ADDRESS\\\": \\\"Email address\\\",\\n        \\\"LOG_IN\\\": \\\"Log in\\\",\\n        \\\"FORGOT_PASSWORD\\\": \\\"Forgot password?\\\"\\n    }\\n}"        }    }}'
```

```json
{    "theme": {        "skin_no": 3,        "skin_code": "skin1",        "skin_translation": {            "language_code": "en_US",            "path": "/locale/en_US.json",            "source": "{\\n    \\\"MEMBER_ID\\\": {\\n        \\\"FIND_YOUR_ID\\\": \\\"Find your ID\\\",\\n        \\\"NAME\\\": \\\"Name\\\",\\n        \\\"EMAIL_ADDRESS\\\": \\\"Email address\\\",\\n        \\\"LOG_IN\\\": \\\"Log in\\\",\\n        \\\"FORGOT_PASSWORD\\\": \\\"Forgot password?\\\"\\n    }\\n}"        }    }}
```
