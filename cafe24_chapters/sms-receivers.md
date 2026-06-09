# SMS RECEIVERS


## Sms receivers

```json
Endpoints    GET /api/v2/admin/sms/receivers
```

```json
GET /api/v2/admin/sms/receivers
```

### Sms receivers property list

| Attribute | Description |
| --- | --- |
| no | 번호 |
| recipient_type | 수신자 구분 |
| supplier_name | 공급사명 |
| supplier_id | 공급사 아이디 |
| user_name | 운영자명 |
| user_id | 운영자 아이디 |
| manager_name | 담당자명 |
| cellphone | 휴대전화 |

### Retrieve a SMS recipient   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 알림 읽기권한 (mall.read_notification) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| recipient_type | 수신자 구분   ALL:전체 S:공급사 A:운영자 |
| supplier_name | 공급사명 |
| supplier_id | 공급사 아이디 |
| user_name | 운영자명 |
| user_id | 운영자 아이디 |
| manager_name | 담당자명 |
| cellphone모바일 | 휴대전화 |
| offset최대값: [8000] | 조회결과 시작위치   DEFAULT 0 |
| limit최소: [1]~최대: [100] | 조회결과 최대건수   DEFAULT 10 |

```bash
Retrieve a SMS recipient        Retrieve a SMS recipient       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/sms/receivers' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "receivers": [        {            "no": 1,            "recipient_type": "S",            "supplier_name": "Oliver Johnson",            "supplier_id": "supplier1",            "user_name": null,            "user_id": null,            "manager_name": "James Anderson",            "cellphone": "010-1234-5678"        },        {            "no": 2,            "recipient_type": "A",            "supplier_name": null,            "supplier_id": null,            "user_name": "Henrry",            "user_id": "admin1",            "manager_name": "John Doe",            "cellphone": "010-2345-6789"        }    ],    "links": [        {            "rel": "next",            "href": "https://{mallid}.cafe24api.com/api/v2/sms/receivers?limit=10&offset=10"        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/sms/receivers' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "receivers": [        {            "no": 1,            "recipient_type": "S",            "supplier_name": "Oliver Johnson",            "supplier_id": "supplier1",            "user_name": null,            "user_id": null,            "manager_name": "James Anderson",            "cellphone": "010-1234-5678"        },        {            "no": 2,            "recipient_type": "A",            "supplier_name": null,            "supplier_id": null,            "user_name": "Henrry",            "user_id": "admin1",            "manager_name": "John Doe",            "cellphone": "010-2345-6789"        }    ],    "links": [        {            "rel": "next",            "href": "https://{mallid}.cafe24api.com/api/v2/sms/receivers?limit=10&offset=10"        }    ]}
```
