# EXCHANGEREQUESTS


## Exchangerequests

```json
Endpoints    POST /api/v2/admin/exchangerequests
PUT /api/v2/admin/exchangerequests
```

```json
POST /api/v2/admin/exchangerequests
PUT /api/v2/admin/exchangerequests
```

### Exchangerequests property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| order_id | 주문번호 |
| items | 품주 목록 |
| exchange_request_no | 교환신청번호 |
| undone | 접수거부 여부 |
| order_item_code | 품주코드 |
| additional_payment_gateway_cancel | 추가 PG 취소 |

### Bulk exchange request API   cafe24 youtube

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
| reason_typeRequired | 사유 구분   A:고객변심 E:상품불만족 K:상품불량 J:배송오류 I:기타 |
| reasonRequired최대글자수 : [2000자] | 교환신청 사유 |
| request_pickup | 수거신청 여부   T : 수거신청 F : 직접발송 |
| pickup | 수거지역 상세 |
| pickup 하위 요소 보기     nameRequired이름 phone전화번호 cellphoneRequired휴대전화 zipcode우편번호 address1Required기본 주소 address2Required상세 주소 |
| tracking_no최대글자수 : [40자] | 반품 송장 번호 |
| shipping_company_name최대글자수 : [30자] | 반품 배송업체명 |
| refund_bank_code | 환불 은행 코드 |
| refund_bank_name최대글자수 : [250자] | 환불은행명 |
| refund_bank_account_no | 환불 계좌번호 |
| refund_bank_account_holder최대글자수 : [15자] | 환불계좌 예금주 명의 |
| items | 품주 목록 |
| items 하위 요소 보기     order_item_codeRequired품주코드 quantityRequired수량 |
| exchange_items | 교환상품정보 |
| exchange_items 하위 요소 보기     product_noRequired상품번호 variant_codeRequired상품 품목 코드 quantityRequired수량 |

```bash
Bulk exchange request API        Bulk exchange request API       Request   cURL Java Python Node.js PHP Go  Copy     curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/exchangerequests' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "requests": [        {            "order_id": "20190228-0000011",            "items": [                {                    "order_item_code": "20190228-0000011-01",                    "quantity": 1                },                {                    "order_item_code": "20190228-0000011-02",                    "quantity": 3                }            ],            "exchange_items": [                {                    "product_no": 9,                    "variant_code": "P000000I000B",                    "quantity": 1                },                {                    "product_no": 9,                    "variant_code": "P000000I000A",                    "quantity": 3                }            ],            "request_pickup": null,            "pickup": null,            "tracking_no": null,            "shipping_company_name": null,            "reason_type": "A",            "reason": "Change of mind",            "refund_bank_name": null,            "refund_bank_code": "bank_82",            "refund_bank_account_no": "000000111111",            "refund_bank_account_holder": "John Doe"        },        {            "order_id": "20190228-0000022",            "items": [                {                    "order_item_code": "20190228-0000022-01",                    "quantity": 2                },                {                    "order_item_code": "20190228-0000022-02",                    "quantity": 2                }            ],            "reason_type": "A",            "reason": "Change of mind",            "request_pickup": "T",            "tracking_no": null,            "shipping_company_name": null,            "pickup": {                "name": "John Doe",                "phone": "02-0000-0000",                "cellphone": "010-0000-0000",                "zipcode": "123-456",                "address1": "Sindaebang dong Dongjak-gu, Seoul, Republic of Korea",                "address2": "Professional Construction Hall"            },            "refund_bank_name": null,            "refund_bank_code": "bank_82",            "refund_bank_account_no": "000000111111",            "refund_bank_account_holder": "John Doe"        }    ]}'    Response  Copy     {    "exchangerequests": [        {            "shop_no": 1,            "order_id": "20190228-0000011",            "exchange_request_no": 8,            "items": [                {                    "order_item_code": "20190228-0000011-01",                    "quantity": 1                },                {                    "order_item_code": "20190228-0000011-02",                    "quantity": 3                }            ]        },        {            "shop_no": 1,            "order_id": "20190228-0000022",            "exchange_request_no": 9,            "items": [                {                    "order_item_code": "20190228-0000022-01",                    "quantity": 2                },                {                    "order_item_code": "20190228-0000022-02",                    "quantity": 2                }            ]        }    ]}
```

```bash
curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/exchangerequests' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "requests": [        {            "order_id": "20190228-0000011",            "items": [                {                    "order_item_code": "20190228-0000011-01",                    "quantity": 1                },                {                    "order_item_code": "20190228-0000011-02",                    "quantity": 3                }            ],            "exchange_items": [                {                    "product_no": 9,                    "variant_code": "P000000I000B",                    "quantity": 1                },                {                    "product_no": 9,                    "variant_code": "P000000I000A",                    "quantity": 3                }            ],            "request_pickup": null,            "pickup": null,            "tracking_no": null,            "shipping_company_name": null,            "reason_type": "A",            "reason": "Change of mind",            "refund_bank_name": null,            "refund_bank_code": "bank_82",            "refund_bank_account_no": "000000111111",            "refund_bank_account_holder": "John Doe"        },        {            "order_id": "20190228-0000022",            "items": [                {                    "order_item_code": "20190228-0000022-01",                    "quantity": 2                },                {                    "order_item_code": "20190228-0000022-02",                    "quantity": 2                }            ],            "reason_type": "A",            "reason": "Change of mind",            "request_pickup": "T",            "tracking_no": null,            "shipping_company_name": null,            "pickup": {                "name": "John Doe",                "phone": "02-0000-0000",                "cellphone": "010-0000-0000",                "zipcode": "123-456",                "address1": "Sindaebang dong Dongjak-gu, Seoul, Republic of Korea",                "address2": "Professional Construction Hall"            },            "refund_bank_name": null,            "refund_bank_code": "bank_82",            "refund_bank_account_no": "000000111111",            "refund_bank_account_holder": "John Doe"        }    ]}'
```

```json
{    "exchangerequests": [        {            "shop_no": 1,            "order_id": "20190228-0000011",            "exchange_request_no": 8,            "items": [                {                    "order_item_code": "20190228-0000011-01",                    "quantity": 1                },                {                    "order_item_code": "20190228-0000011-02",                    "quantity": 3                }            ]        },        {            "shop_no": 1,            "order_id": "20190228-0000022",            "exchange_request_no": 9,            "items": [                {                    "order_item_code": "20190228-0000022-01",                    "quantity": 2                },                {                    "order_item_code": "20190228-0000022-02",                    "quantity": 2                }            ]        }    ]}
```

### Reject an exchange request for multiple items   cafe24 youtube

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
Reject an exchange request for multiple items        Reject an exchange request for multiple items       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/exchangerequests' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "requests": [        {            "order_id": "20190228-0000011",            "undone": "T",            "reason_type": "H",            "reason": "out of stocks",            "display_reject_reason": "T",            "reject_reason": "These products are out of stocks. Sorry",            "order_item_code": [                "20190228-0000011-01",                "20190228-0000011-02"            ]        },        {            "order_id": "20190228-0000022",            "undone": "T",            "reason_type": "L",            "reason": null,            "display_reject_reason": "F",            "reject_reason": null,            "order_item_code": [                "20190228-0000022-01",                "20190228-0000022-02"            ]        }    ]}'    Response  Copy     {    "exchangerequests": [        {            "shop_no": 1,            "order_id": "20190228-0000011",            "undone": "T",            "order_item_code": [                "20190228-0000011-01",                "20190228-0000011-02"            ],            "additional_payment_gateway_cancel": {                "success": [                    "20190228-0000011-01",                    "20190228-0000011-02"                ],                "fail": null            }        },        {            "shop_no": 1,            "order_id": "20190228-0000022",            "undone": "T",            "order_item_code": [                "20190228-0000022-01",                "20190228-0000022-02"            ],            "additional_payment_gateway_cancel": {                "success": [                    "20190228-0000022-01",                    "20190228-0000022-02"                ],                "fail": null            }        }    ]}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/exchangerequests' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "requests": [        {            "order_id": "20190228-0000011",            "undone": "T",            "reason_type": "H",            "reason": "out of stocks",            "display_reject_reason": "T",            "reject_reason": "These products are out of stocks. Sorry",            "order_item_code": [                "20190228-0000011-01",                "20190228-0000011-02"            ]        },        {            "order_id": "20190228-0000022",            "undone": "T",            "reason_type": "L",            "reason": null,            "display_reject_reason": "F",            "reject_reason": null,            "order_item_code": [                "20190228-0000022-01",                "20190228-0000022-02"            ]        }    ]}'
```

```json
{    "exchangerequests": [        {            "shop_no": 1,            "order_id": "20190228-0000011",            "undone": "T",            "order_item_code": [                "20190228-0000011-01",                "20190228-0000011-02"            ],            "additional_payment_gateway_cancel": {                "success": [                    "20190228-0000011-01",                    "20190228-0000011-02"                ],                "fail": null            }        },        {            "shop_no": 1,            "order_id": "20190228-0000022",            "undone": "T",            "order_item_code": [                "20190228-0000022-01",                "20190228-0000022-02"            ],            "additional_payment_gateway_cancel": {                "success": [                    "20190228-0000022-01",                    "20190228-0000022-02"                ],                "fail": null            }        }    ]}
```
