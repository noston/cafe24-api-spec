# CANCELLATIONREQUESTS


## Cancellationrequests

```json
Endpoints    POST /api/v2/admin/cancellationrequests
PUT /api/v2/admin/cancellationrequests
```

```json
POST /api/v2/admin/cancellationrequests
PUT /api/v2/admin/cancellationrequests
```

### Cancellationrequests property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| order_id | 주문번호 |
| items | 품주 목록 |
| undone | 접수거부 여부 |
| order_item_code | 품주코드 |

### Create a cancellation request for multiple items   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 쓰기권한 (mall.write_order) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 100 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| order_idRequired | 주문번호 |
| reason_typeRequired | 취소사유 구분   A:고객변심B:배송지연G:서비스불만족I:기타 |
| reasonRequired최대글자수 : [2000자] | 취소사유 |
| refund_bank_code | 환불 은행 코드   환불 방식(refund_method)이 현금(T)일 경우 필수  refund_bank_code   해당 쇼핑몰이 EC Korea 쇼핑몰일 경우 필수 환불수단(refund_method)이 "현금(T)"일 때만 사용 가능 오픈마켓/네이버페이 주문을 취소할 경우 사용 불가 |
| refund_bank_name최대글자수 : [250자] | 환불은행명 |
| refund_bank_account_no | 환불 계좌번호 |
| refund_bank_account_holder최대글자수 : [15자] | 환불계좌 예금주 명의 |
| items | 품주 목록 |
| items 하위 요소 보기     order_item_codeRequired품주코드 quantityRequired수량 |

```bash
Create a cancellation request for multiple items        Create a cancellation request for multiple items       Request   cURL Java Python Node.js PHP Go  Copy     curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/cancellationrequests' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "requests": [        {            "order_id": "20190228-0000011",            "reason_type": "A",            "reason": "Change of mind",            "refund_bank_code": "bank_82",            "refund_bank_account_no": "000000111111",            "refund_bank_account_holder": "John Doe",            "items": [                {                    "order_item_code": "20190228-0000011-01",                    "quantity": 2                },                {                    "order_item_code": "20190228-0000011-02",                    "quantity": 3                }            ]        },        {            "order_id": "20190228-0000022",            "reason_type": "A",            "reason": "Change of mind",            "refund_bank_code": "bank_82",            "refund_bank_account_no": "000000111111",            "refund_bank_account_holder": "John Doe",            "items": [                {                    "order_item_code": "20190228-0000022-01",                    "quantity": 1                },                {                    "order_item_code": "20190228-0000022-02",                    "quantity": 2                }            ]        }    ]}'    Response  Copy     {    "cancellationrequests": [        {            "shop_no": 1,            "order_id": "20190228-0000011",            "items": [                {                    "order_item_code": "20190228-0000011-01",                    "quantity": 2                },                {                    "order_item_code": "20190228-0000011-02",                    "quantity": 3                }            ]        },        {            "shop_no": 1,            "order_id": "20190228-0000022",            "items": [                {                    "order_item_code": "20190228-0000022-01",                    "quantity": 1                },                {                    "order_item_code": "20190228-0000022-02",                    "quantity": 2                }            ]        }    ]}
```

```bash
curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/cancellationrequests' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "requests": [        {            "order_id": "20190228-0000011",            "reason_type": "A",            "reason": "Change of mind",            "refund_bank_code": "bank_82",            "refund_bank_account_no": "000000111111",            "refund_bank_account_holder": "John Doe",            "items": [                {                    "order_item_code": "20190228-0000011-01",                    "quantity": 2                },                {                    "order_item_code": "20190228-0000011-02",                    "quantity": 3                }            ]        },        {            "order_id": "20190228-0000022",            "reason_type": "A",            "reason": "Change of mind",            "refund_bank_code": "bank_82",            "refund_bank_account_no": "000000111111",            "refund_bank_account_holder": "John Doe",            "items": [                {                    "order_item_code": "20190228-0000022-01",                    "quantity": 1                },                {                    "order_item_code": "20190228-0000022-02",                    "quantity": 2                }            ]        }    ]}'
```

```json
{    "cancellationrequests": [        {            "shop_no": 1,            "order_id": "20190228-0000011",            "items": [                {                    "order_item_code": "20190228-0000011-01",                    "quantity": 2                },                {                    "order_item_code": "20190228-0000011-02",                    "quantity": 3                }            ]        },        {            "shop_no": 1,            "order_id": "20190228-0000022",            "items": [                {                    "order_item_code": "20190228-0000022-01",                    "quantity": 1                },                {                    "order_item_code": "20190228-0000022-02",                    "quantity": 2                }            ]        }    ]}
```

### Reject a cancellation request for multiple items   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 쓰기권한 (mall.write_order) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 100 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| order_idRequired | 주문번호 |
| order_item_codeRequired | 품주코드 |
| undoneRequired | 접수거부 여부   T : 접수거부함 |
| reason_type | 사유 구분   A:고객변심B:배송지연J:배송오류C:배송불가지역L:수출/통관 불가D:포장불량E:상품 불만족F:상품정보상이K:상품불량G:서비스불만족H:품절I:기타 |
| reason최대글자수 : [2000자] | 사유 |
| display_reject_reason | 주문상세내역 노출설정   T : 노출함 F : 노출안함   DEFAULT F |
| reject_reason최대글자수 : [2000자] | 거부 사유 |

```bash
Reject a cancellation request for multiple items        Reject a cancellation request for multiple items       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/cancellationrequests' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "requests": [        {            "order_id": "20190228-0000011",            "undone": "T",            "reason_type": "I",            "display_reject_reason": "T",            "reject_reason": "Already been producing customized products.",            "order_item_code": [                "20190228-0000011-01",                "20190228-0000011-02"            ]        },        {            "order_id": "20190228-0000022",            "undone": "T",            "reason_type": "I",            "order_item_code": [                "20190228-0000022-01",                "20190228-0000022-02"            ]        }    ]}'    Response  Copy     {    "cancellationrequests": [        {            "shop_no": 1,            "order_id": "20190228-0000011",            "undone": "T",            "order_item_code": [                "20190228-0000011-01",                "20190228-0000011-02"            ]        },        {            "shop_no": 1,            "order_id": "20190228-0000022",            "undone": "T",            "order_item_code": [                "20190228-0000022-01",                "20190228-0000022-02"            ]        }    ]}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/cancellationrequests' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "requests": [        {            "order_id": "20190228-0000011",            "undone": "T",            "reason_type": "I",            "display_reject_reason": "T",            "reject_reason": "Already been producing customized products.",            "order_item_code": [                "20190228-0000011-01",                "20190228-0000011-02"            ]        },        {            "order_id": "20190228-0000022",            "undone": "T",            "reason_type": "I",            "order_item_code": [                "20190228-0000022-01",                "20190228-0000022-02"            ]        }    ]}'
```

```json
{    "cancellationrequests": [        {            "shop_no": 1,            "order_id": "20190228-0000011",            "undone": "T",            "order_item_code": [                "20190228-0000011-01",                "20190228-0000011-02"            ]        },        {            "shop_no": 1,            "order_id": "20190228-0000022",            "undone": "T",            "order_item_code": [                "20190228-0000022-01",                "20190228-0000022-02"            ]        }    ]}
```
