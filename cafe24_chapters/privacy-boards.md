# PRIVACY BOARDS


## Privacy boards

```json
Endpoints    GET /api/v2/admin/privacy/boards
PUT /api/v2/admin/privacy/boards
```

```json
GET /api/v2/admin/privacy/boards
PUT /api/v2/admin/privacy/boards
```

### Privacy boards property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| no | 동의서 번호 |
| name | 동의서명 |
| use | 사용 여부 T: 사용함 F: 사용안함 |
| content | 동의서 내용 |

### Retrieve privacy policy for posting on board   cafe24

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
Retrieve privacy policy for posting on board        Retrieve privacy policy for posting on board       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/privacy/boards' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "boards": [        {            "shop_no": 1,            "no": 10,            "name": "Privacy Policy Agreement for Guest Board Posts",            "use": "F",            "content": "This sample form is provided to help with shopping mall operations and needs to be modified according to the specific operational characteristics of your shopping mall before application."        },        {            "shop_no": 1,            "no": 11,            "name": "Privacy Policy Agreement for Guest Bulk Order Inquiry",            "use": "F",            "content": "This sample form is provided to help with shopping mall operations and needs to be modified according to the specific operational characteristics of your shopping mall before application."        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/privacy/boards' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "boards": [        {            "shop_no": 1,            "no": 10,            "name": "Privacy Policy Agreement for Guest Board Posts",            "use": "F",            "content": "This sample form is provided to help with shopping mall operations and needs to be modified according to the specific operational characteristics of your shopping mall before application."        },        {            "shop_no": 1,            "no": 11,            "name": "Privacy Policy Agreement for Guest Bulk Order Inquiry",            "use": "F",            "content": "This sample form is provided to help with shopping mall operations and needs to be modified according to the specific operational characteristics of your shopping mall before application."        }    ]}
```

### Update privacy policy for posting on board   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 쓰기권한 (mall.write_store) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 2 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| noRequired최소값: [1] | 동의서 번호 |
| use | 사용 여부   T: 사용함 F: 사용안함 |
| save_type | 저장 방식   S: 표준 약관 적용 C: 사용자 정의 약관 적용 |
| content | 동의서 내용 |

```bash
Update privacy policy for posting on board        Update privacy policy for posting on board       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/privacy/boards' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "requests": [        {            "no": 10,            "use": "F",            "save_type": "C",            "content": "This sample form is provided to help with shopping mall operations and needs to be modified according to the specific operational characteristics of your shopping mall before application."        },        {            "no": 11,            "use": "F",            "save_type": "C",            "content": "This sample form is provided to help with shopping mall operations and needs to be modified according to the specific operational characteristics of your shopping mall before application."        }    ]}'    Response  Copy     {    "boards": [        {            "shop_no": 1,            "no": 10,            "name": "Privacy Policy Agreement for Guest Board Posts",            "use": "F",            "content": "This sample form is provided to help with shopping mall operations and needs to be modified according to the specific operational characteristics of your shopping mall before application."        },        {            "shop_no": 1,            "no": 11,            "name": "Privacy Policy Agreement for Guest Bulk Order Inquiry",            "use": "F",            "content": "This sample form is provided to help with shopping mall operations and needs to be modified according to the specific operational characteristics of your shopping mall before application."        }    ]}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/privacy/boards' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "requests": [        {            "no": 10,            "use": "F",            "save_type": "C",            "content": "This sample form is provided to help with shopping mall operations and needs to be modified according to the specific operational characteristics of your shopping mall before application."        },        {            "no": 11,            "use": "F",            "save_type": "C",            "content": "This sample form is provided to help with shopping mall operations and needs to be modified according to the specific operational characteristics of your shopping mall before application."        }    ]}'
```

```json
{    "boards": [        {            "shop_no": 1,            "no": 10,            "name": "Privacy Policy Agreement for Guest Board Posts",            "use": "F",            "content": "This sample form is provided to help with shopping mall operations and needs to be modified according to the specific operational characteristics of your shopping mall before application."        },        {            "shop_no": 1,            "no": 11,            "name": "Privacy Policy Agreement for Guest Bulk Order Inquiry",            "use": "F",            "content": "This sample form is provided to help with shopping mall operations and needs to be modified according to the specific operational characteristics of your shopping mall before application."        }    ]}
```
