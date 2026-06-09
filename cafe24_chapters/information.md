# INFORMATION


## Information

```json
Endpoints    GET /api/v2/admin/information
PUT /api/v2/admin/information
```

```json
GET /api/v2/admin/information
PUT /api/v2/admin/information
```

### Information property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| type | 안내 유형 information_type |
| display_mobile | 모바일 표시 여부 T : 표시함 F : 표시안함 |
| use | 사용 여부 T: 사용함 F: 사용안함 |
| content | 안내 내용 |

### Retrieve store policies   cafe24

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
Retrieve store policies        Retrieve store policies       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/information' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "information": [        {            "shop_no": 1,            "type": "PAYMENT",            "display_mobile": "F",            "use": null,            "content": "For high-value payments, the card company may call you to verify the transaction for security purposes."        },        {            "shop_no": 1,            "type": "SHIPPING_INFORMATION",            "display_mobile": null,            "use": "T",            "content": "This guide contains our shipping information provision policy."        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/information' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "information": [        {            "shop_no": 1,            "type": "PAYMENT",            "display_mobile": "F",            "use": null,            "content": "For high-value payments, the card company may call you to verify the transaction for security purposes."        },        {            "shop_no": 1,            "type": "SHIPPING_INFORMATION",            "display_mobile": null,            "use": "T",            "content": "This guide contains our shipping information provision policy."        }    ]}
```

### Update store policies   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 쓰기권한 (mall.write_store) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 8 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| typeRequired | 안내 유형   information_type |
| display_mobile | 모바일 표시 여부   T : 표시함 F : 표시안함 |
| use | 사용 여부   T: 사용함 F: 사용안함 |
| save_type | 저장 방식   S: 표준 안내 적용 C: 사용자 정의 안내 적용 |
| content | 안내 내용 |

```bash
Update store policies        Update store policies       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/information' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "requests": [        {            "type": "PAYMENT",            "display_mobile": "F",            "save_type": "C",            "content": "For high-value payments, the card company may call you to verify the transaction for security purposes."        },        {            "type": "SHIPPING_INFORMATION",            "use": "T",            "save_type": "S"        }    ]}'    Response  Copy     {    "information": [        {            "shop_no": 1,            "type": "PAYMENT",            "display_mobile": "F",            "use": null,            "content": "For high-value payments, the card company may call you to verify the transaction for security purposes."        },        {            "shop_no": 1,            "type": "SHIPPING_INFORMATION",            "display_mobile": null,            "use": "T",            "content": "This is a guide to our shipping information provision policy which explains how we handle your delivery data."        }    ]}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/information' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "requests": [        {            "type": "PAYMENT",            "display_mobile": "F",            "save_type": "C",            "content": "For high-value payments, the card company may call you to verify the transaction for security purposes."        },        {            "type": "SHIPPING_INFORMATION",            "use": "T",            "save_type": "S"        }    ]}'
```

```json
{    "information": [        {            "shop_no": 1,            "type": "PAYMENT",            "display_mobile": "F",            "use": null,            "content": "For high-value payments, the card company may call you to verify the transaction for security purposes."        },        {            "shop_no": 1,            "type": "SHIPPING_INFORMATION",            "display_mobile": null,            "use": "T",            "content": "This is a guide to our shipping information provision policy which explains how we handle your delivery data."        }    ]}
```
