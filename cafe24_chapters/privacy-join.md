# PRIVACY JOIN


## Privacy join

```json
Endpoints    GET /api/v2/admin/privacy/join
PUT /api/v2/admin/privacy/join
```

```json
GET /api/v2/admin/privacy/join
PUT /api/v2/admin/privacy/join
```

### Privacy join property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| no | 동의서 번호 |
| name | 동의서명 |
| use | 사용 여부 T: 사용함 F: 사용안함 |
| required | 필수/선택 여부 T : 필수 F : 선택 |
| display | 동의서 표시 화면 JOIN: 회원가입 SIMPLE_ORDER_JOIN: 주문서 간단 회원가입 SHOPPING_PAY_EASY_JOIN: 쇼핑페이 간편가입 |
| content | 동의서 내용 |

### Retrieve privacy policy for signup   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 읽기권한 (mall.read_store) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |

```bash
Retrieve privacy policy for signup        Retrieve privacy policy for signup       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/privacy/join' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "join": [        {            "shop_no": 1,            "no": 1,            "name": "Agreement to Collection and Use of Personal Information (Required)",            "use": "T",            "required": "T",            "display": [                "JOIN",                "SIMPLE_ORDER_JOIN"            ],            "content": "Content of agreement for collection and use of personal information has been modified."        },        {            "shop_no": 1,            "no": 2,            "name": "Agreement to Collection and Use of Personal Information (Optional)",            "use": "F",            "required": "F",            "display": [                "JOIN",                "SHOPPING_PAY_EASY_JOIN"            ],            "content": "This form is provided as a sample to help with shopping mall operation and requires modification according to the type of shopping mall operation."        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/privacy/join' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "join": [        {            "shop_no": 1,            "no": 1,            "name": "Agreement to Collection and Use of Personal Information (Required)",            "use": "T",            "required": "T",            "display": [                "JOIN",                "SIMPLE_ORDER_JOIN"            ],            "content": "Content of agreement for collection and use of personal information has been modified."        },        {            "shop_no": 1,            "no": 2,            "name": "Agreement to Collection and Use of Personal Information (Optional)",            "use": "F",            "required": "F",            "display": [                "JOIN",                "SHOPPING_PAY_EASY_JOIN"            ],            "content": "This form is provided as a sample to help with shopping mall operation and requires modification according to the type of shopping mall operation."        }    ]}
```

### Update privacy policy for signup   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 쓰기권한 (mall.write_store) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 10 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| noRequired최소값: [1] | 동의서 번호 |
| use | 사용 여부   T: 사용함 F: 사용안함 |
| required | 필수/선택 여부   T : 필수 F : 선택 |
| display | 동의서 표시 화면   JOIN: 회원가입 SIMPLE_ORDER_JOIN: 주문서 간단 회원가입 SHOPPING_PAY_EASY_JOIN: 쇼핑페이 간편가입 |
| save_type | 저장 방식   S: 표준 약관 적용 C: 사용자 정의 약관 적용 |
| content | 동의서 내용 |

```bash
Update privacy policy for signup        Update privacy policy for signup       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/privacy/join' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "requests": [        {            "no": 1,            "use": "T",            "display": [                "JOIN",                "SIMPLE_ORDER_JOIN"            ],            "save_type": "C",            "content": "Content of agreement for collection and use of personal information has been modified."        },        {            "no": 2,            "use": "F",            "display": [                "JOIN",                "SHOPPING_PAY_EASY_JOIN"            ],            "save_type": "C",            "content": "This form is provided as a sample to help with shopping mall operation and requires modification according to the type of shopping mall operation."        }    ]}'    Response  Copy     {    "join": [        {            "shop_no": 1,            "no": 1,            "name": "Agreement to Collection and Use of Personal Information (Required)",            "use": "T",            "required": "T",            "display": [                "JOIN",                "SIMPLE_ORDER_JOIN"            ],            "content": "Content of agreement for collection and use of personal information has been modified."        },        {            "shop_no": 1,            "no": 2,            "name": "Agreement to Collection and Use of Personal Information (Optional)",            "use": "F",            "required": "F",            "display": [                "JOIN",                "SHOPPING_PAY_EASY_JOIN"            ],            "content": "This form is provided as a sample to help with shopping mall operation and requires modification according to the type of shopping mall operation."        }    ]}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/privacy/join' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "requests": [        {            "no": 1,            "use": "T",            "display": [                "JOIN",                "SIMPLE_ORDER_JOIN"            ],            "save_type": "C",            "content": "Content of agreement for collection and use of personal information has been modified."        },        {            "no": 2,            "use": "F",            "display": [                "JOIN",                "SHOPPING_PAY_EASY_JOIN"            ],            "save_type": "C",            "content": "This form is provided as a sample to help with shopping mall operation and requires modification according to the type of shopping mall operation."        }    ]}'
```

```json
{    "join": [        {            "shop_no": 1,            "no": 1,            "name": "Agreement to Collection and Use of Personal Information (Required)",            "use": "T",            "required": "T",            "display": [                "JOIN",                "SIMPLE_ORDER_JOIN"            ],            "content": "Content of agreement for collection and use of personal information has been modified."        },        {            "shop_no": 1,            "no": 2,            "name": "Agreement to Collection and Use of Personal Information (Optional)",            "use": "F",            "required": "F",            "display": [                "JOIN",                "SHOPPING_PAY_EASY_JOIN"            ],            "content": "This form is provided as a sample to help with shopping mall operation and requires modification according to the type of shopping mall operation."        }    ]}
```
