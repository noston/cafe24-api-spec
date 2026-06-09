# PRIVACY ORDERS


## Privacy orders

```json
Endpoints    GET /api/v2/admin/privacy/orders
PUT /api/v2/admin/privacy/orders
```

```json
GET /api/v2/admin/privacy/orders
PUT /api/v2/admin/privacy/orders
```

### Privacy orders property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| no | 동의서 번호 |
| name | 동의서명 |
| use | 사용 여부 T: 사용함 F: 사용안함 |
| use_member | 회원 구매 시 사용 여부 T: 사용함 F: 사용안함 |
| use_non_member | 비회원 구매 시 사용 여부 T: 사용함 F: 사용안함 |
| content | 동의서 내용 |

### Retrieve privacy policy for checkout   cafe24

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
Retrieve privacy policy for checkout        Retrieve privacy policy for checkout       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/privacy/orders' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "orders": [        {            "shop_no": 1,            "no": 8,            "name": "Privacy Policy Agreement for Member/Non-member Purchases",            "use": "T",            "use_member": "F",            "use_non_member": "T",            "content": "This sample form is provided to help with shopping mall operations and needs to be modified according to the specific operational characteristics of your shopping mall."        },        {            "shop_no": 1,            "no": 9,            "name": "Agreement for Collection and Use of Personal Identification Information",            "use": "T",            "use_member": null,            "use_non_member": null,            "content": "This form provides guidance for collecting personal identification information such as ID cards and passport numbers for customs clearance when shipping to international destinations."        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/privacy/orders' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "orders": [        {            "shop_no": 1,            "no": 8,            "name": "Privacy Policy Agreement for Member/Non-member Purchases",            "use": "T",            "use_member": "F",            "use_non_member": "T",            "content": "This sample form is provided to help with shopping mall operations and needs to be modified according to the specific operational characteristics of your shopping mall."        },        {            "shop_no": 1,            "no": 9,            "name": "Agreement for Collection and Use of Personal Identification Information",            "use": "T",            "use_member": null,            "use_non_member": null,            "content": "This form provides guidance for collecting personal identification information such as ID cards and passport numbers for customs clearance when shipping to international destinations."        }    ]}
```

### Update privacy policy for checkout   cafe24

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
| use_member | 회원 구매 시 사용 여부   T: 사용함 F: 사용안함 |
| use_non_member | 비회원 구매 시 사용 여부   T: 사용함 F: 사용안함 |
| save_type | 저장 방식   S: 표준 약관 적용 C: 사용자 정의 약관 적용 |
| content | 동의서 내용 |

```bash
Update privacy policy for checkout        Update privacy policy for checkout       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/privacy/orders' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "requests": [        {            "no": 8,            "use": "T",            "use_member": "F",            "use_non_member": "T",            "save_type": "C",            "content": "This sample form is provided to help with shopping mall operations and needs to be modified according to the specific operational characteristics of your shopping mall."        },        {            "no": 9,            "save_type": "C",            "content": "This form provides guidance for collecting personal identification information such as ID cards and passport numbers for customs clearance when shipping to international destinations."        }    ]}'    Response  Copy     {    "orders": [        {            "shop_no": 1,            "no": 8,            "name": "Privacy Policy Agreement for Member/Non-member Purchases",            "use": "T",            "use_member": "F",            "use_non_member": "T",            "content": "This sample form is provided to help with shopping mall operations and needs to be modified according to the specific operational characteristics of your shopping mall."        },        {            "shop_no": 1,            "no": 9,            "name": "Agreement for Collection and Use of Personal Identification Information",            "use": "T",            "use_member": null,            "use_non_member": null,            "content": "This form provides guidance for collecting personal identification information such as ID cards and passport numbers for customs clearance when shipping to international destinations."        }    ]}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/privacy/orders' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "requests": [        {            "no": 8,            "use": "T",            "use_member": "F",            "use_non_member": "T",            "save_type": "C",            "content": "This sample form is provided to help with shopping mall operations and needs to be modified according to the specific operational characteristics of your shopping mall."        },        {            "no": 9,            "save_type": "C",            "content": "This form provides guidance for collecting personal identification information such as ID cards and passport numbers for customs clearance when shipping to international destinations."        }    ]}'
```

```json
{    "orders": [        {            "shop_no": 1,            "no": 8,            "name": "Privacy Policy Agreement for Member/Non-member Purchases",            "use": "T",            "use_member": "F",            "use_non_member": "T",            "content": "This sample form is provided to help with shopping mall operations and needs to be modified according to the specific operational characteristics of your shopping mall."        },        {            "shop_no": 1,            "no": 9,            "name": "Agreement for Collection and Use of Personal Identification Information",            "use": "T",            "use_member": null,            "use_non_member": null,            "content": "This form provides guidance for collecting personal identification information such as ID cards and passport numbers for customs clearance when shipping to international destinations."        }    ]}
```
