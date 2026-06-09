# CUSTOMERS PROPERTIES


## Customers properties

```json
Endpoints    GET /api/v2/admin/customers/properties
PUT /api/v2/admin/customers/properties
```

```json
GET /api/v2/admin/customers/properties
PUT /api/v2/admin/customers/properties
```

### Customers properties property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| type | 회원가입항목 유형 |
| properties | 항목 |

### View account signup fields   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 회원 읽기권한 (mall.read_customer) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| type | 회원가입항목 유형   join:회원가입 항목 edit:회원정보 수정 항목   DEFAULT join |

```bash
View account signup fields        View account signup fields       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/customers/properties' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "customer": {        "shop_no": 1,        "type": "join",        "properties": [            {                "key": "sms_agree",                "name": "SMS subscription",                "use": "T",                "required": "T"            },            {                "key": "email_agree",                "name": "Email subscription",                "use": "T",                "required": "T"            }        ]    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/customers/properties' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "customer": {        "shop_no": 1,        "type": "join",        "properties": [            {                "key": "sms_agree",                "name": "SMS subscription",                "use": "T",                "required": "T"            },            {                "key": "email_agree",                "name": "Email subscription",                "use": "T",                "required": "T"            }        ]    }}
```

### Edit account signup fields   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 회원 쓰기권한 (mall.write_customer) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| typeRequired | 회원가입항목 유형   join:회원가입 항목 edit:회원정보 수정 항목 |
| properties | 항목 |
| properties 하위 요소 보기     key항목키 use일반 회원가입 사용여부T:사용 F:사용안함 required필수입력여부T:필수 F:선택 |

```bash
Edit account signup fields        Edit account signup fields       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/customers/properties' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "type": "join",        "properties": [            {                "key": "sms_agree",                "use": "T"            },            {                "key": "birthday",                "use": "T",                "required": "T"            }        ]    }}'    Response  Copy     {    "customer": {        "shop_no": 1,        "type": "join",        "properties": [            {                "key": "sms_agree",                "name": "SMS subscription",                "use": "T",                "required": "T"            },            {                "key": "birthday",                "name": "Date of birth",                "use": "T",                "required": "T"            }        ]    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/customers/properties' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "type": "join",        "properties": [            {                "key": "sms_agree",                "use": "T"            },            {                "key": "birthday",                "use": "T",                "required": "T"            }        ]    }}'
```

```json
{    "customer": {        "shop_no": 1,        "type": "join",        "properties": [            {                "key": "sms_agree",                "name": "SMS subscription",                "use": "T",                "required": "T"            },            {                "key": "birthday",                "name": "Date of birth",                "use": "T",                "required": "T"            }        ]    }}
```
