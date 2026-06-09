# PAYMENTGATEWAY


## Paymentgateway

```json
Endpoints    POST /api/v2/admin/paymentgateway
PUT /api/v2/admin/paymentgateway/{client_id}
DELETE /api/v2/admin/paymentgateway/{client_id}
```

```json
POST /api/v2/admin/paymentgateway
PUT /api/v2/admin/paymentgateway/{client_id}
DELETE /api/v2/admin/paymentgateway/{client_id}
```

### Paymentgateway property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| partner_id | PG사 발급 가맹점 ID |
| client_id | 앱 클라이언트 ID |
| additional_information | 추가 정보 |
| membership_fee_type | 가입비 분류 PRE : 선불 PAD : 후불 FREE : 무료 |
| service_limit_type | 서비스 제한 A : 회원/비회원 제한 없음 M : 회원만 제공 |
| review_status | 심사상태 AWAITING_PAYMENT : 결제대기 PENDING_REVIEW : 심사대기 APPROVED : 심사완료 |
| review_date | 심사일자 |

### Create a Payment Gateway   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 쓰기권한 (mall.write_store) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| partner_idRequired최대글자수 : [50자] | PG사 발급 가맹점 ID |
| additional_information배열 최대사이즈: [5] | 추가 정보 |
| additional_information 하위 요소 보기     key추가항목 키 value추가항목 값 |
| membership_fee_type최대글자수 : [4자] | 가입비 분류   PRE : 선불 PAD : 후불 FREE : 무료 |
| service_limit_type최대글자수 : [1자] | 서비스 제한   A : 회원/비회원 제한 없음 M : 회원만 제공   DEFAULT A |
| review_status | 심사상태   AWAITING_PAYMENT : 결제대기 PENDING_REVIEW : 심사대기 APPROVED : 심사완료   DEFAULT AWAITING_PAYMENT |

```bash
Create a Payment Gateway        Create a Payment Gateway Create a payment gateway by using only required fields Try creating a payment gateway with same client id       Request   cURL Java Python Node.js PHP Go  Copy     curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/paymentgateway' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "partner_id": "partner1",        "additional_information": [            {                "key": "version",                "value": "s1.6"            },            {                "key": "hash_code",                "value": "aXKB4Pe"            }        ],        "membership_fee_type": "FREE",        "service_limit_type": "A",        "review_status": "AWAITING_PAYMENT"    }}'    Response  Copy     {    "paymentgateway": {        "shop_no": 1,        "partner_id": "partner1",        "client_id": "t9v2be4eYDif11NVvHbSsG",        "additional_information": [            {                "key": "version",                "value": "s1.6"            },            {                "key": "hash_code",                "value": "aXKB4Pe"            }        ],        "membership_fee_type": "FREE",        "service_limit_type": "A",        "review_status": "AWAITING_PAYMENT",        "review_date": "2025-04-23 10:00:00"    }}
```

```bash
curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/paymentgateway' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "partner_id": "partner1",        "additional_information": [            {                "key": "version",                "value": "s1.6"            },            {                "key": "hash_code",                "value": "aXKB4Pe"            }        ],        "membership_fee_type": "FREE",        "service_limit_type": "A",        "review_status": "AWAITING_PAYMENT"    }}'
```

```json
{    "paymentgateway": {        "shop_no": 1,        "partner_id": "partner1",        "client_id": "t9v2be4eYDif11NVvHbSsG",        "additional_information": [            {                "key": "version",                "value": "s1.6"            },            {                "key": "hash_code",                "value": "aXKB4Pe"            }        ],        "membership_fee_type": "FREE",        "service_limit_type": "A",        "review_status": "AWAITING_PAYMENT",        "review_date": "2025-04-23 10:00:00"    }}
```

### Update a Payment Gateway   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 쓰기권한 (mall.write_store) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| client_idRequired최대글자수 : [50자] | 앱 클라이언트 ID |
| partner_id최대글자수 : [50자] | PG사 발급 가맹점 ID |
| additional_information배열 최대사이즈: [5] | 추가 정보 |
| additional_information 하위 요소 보기     key추가항목 키 value추가항목 값 |
| membership_fee_type최대글자수 : [4자] | 가입비 분류   PRE : 선불 PAD : 후불 FREE : 무료 |
| service_limit_type최대글자수 : [1자] | 서비스 제한   A : 회원/비회원 제한 없음 M : 회원만 제공   DEFAULT A |
| review_status | 심사상태   AWAITING_PAYMENT : 결제대기 PENDING_REVIEW : 심사대기 APPROVED : 심사완료 |

```bash
Update a Payment Gateway        Update a Payment Gateway Update subscription fee type Update pg-issued store id(partner id)       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/paymentgateway/t9v2be4eYDif11NVvHbSsG' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "partner_id": "partner1",        "additional_information": [            {                "key": "version",                "value": "s1.6"            },            {                "key": "hash_code",                "value": "aXKB4Pe"            }        ],        "membership_fee_type": "FREE",        "service_limit_type": "A",        "review_status": "PENDING_REVIEW"    }}'    Response  Copy     {    "paymentgateway": {        "shop_no": 1,        "partner_id": "partner1",        "client_id": "t9v2be4eYDif11NVvHbSsG",        "additional_information": [            {                "key": "version",                "value": "s1.6"            },            {                "key": "hash_code",                "value": "aXKB4Pe"            }        ],        "membership_fee_type": "FREE",        "service_limit_type": "A",        "review_status": "PENDING_REVIEW",        "review_date": "2025-04-23 10:00:00"    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/paymentgateway/t9v2be4eYDif11NVvHbSsG' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "partner_id": "partner1",        "additional_information": [            {                "key": "version",                "value": "s1.6"            },            {                "key": "hash_code",                "value": "aXKB4Pe"            }        ],        "membership_fee_type": "FREE",        "service_limit_type": "A",        "review_status": "PENDING_REVIEW"    }}'
```

```json
{    "paymentgateway": {        "shop_no": 1,        "partner_id": "partner1",        "client_id": "t9v2be4eYDif11NVvHbSsG",        "additional_information": [            {                "key": "version",                "value": "s1.6"            },            {                "key": "hash_code",                "value": "aXKB4Pe"            }        ],        "membership_fee_type": "FREE",        "service_limit_type": "A",        "review_status": "PENDING_REVIEW",        "review_date": "2025-04-23 10:00:00"    }}
```

### Delete a Payment Gateway   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 쓰기권한 (mall.write_store) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| client_idRequired최대글자수 : [50자] | 앱 클라이언트 ID |

```bash
Delete a Payment Gateway        Delete a Payment Gateway       Request   cURL Java Python Node.js PHP Go  Copy     curl -X DELETE \  'https://{mallid}.cafe24api.com/api/v2/admin/paymentgateway/t9v2be4eYDif11NVvHbSsG' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "paymentgateway": {        "shop_no": 1,        "client_id": "t9v2be4eYDif11NVvHbSsG"    }}
```

```bash
curl -X DELETE \  'https://{mallid}.cafe24api.com/api/v2/admin/paymentgateway/t9v2be4eYDif11NVvHbSsG' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "paymentgateway": {        "shop_no": 1,        "client_id": "t9v2be4eYDif11NVvHbSsG"    }}
```
