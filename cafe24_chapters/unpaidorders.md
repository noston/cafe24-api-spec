# UNPAIDORDERS


## Unpaidorders

```json
Endpoints    GET /api/v2/admin/unpaidorders
```

```json
GET /api/v2/admin/unpaidorders
```

### Unpaidorders property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 DEFAULT 1 |
| order_id | 주문번호 |
| order_item_code | 품주코드 |
| order_date | 주문일 |
| buyer_name | 주문자 이름 |
| billing_name | 입금자명 |
| bank_code | 은행코드 bank_code |
| bank_name | 은행명 |
| unpaid_amount | 미입금 금액 |
| accounts | 계좌번호 |
| payment_method | 결제수단 cash : 무통장 icash : 가상계좌 |
| settle_type | 결제타입 S: 기본결제 E: 추가결제 |
| payment_no | 결제번호 |

### Retrieve unpaid orders   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 읽기권한 (mall.read_order) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| start_dateRequired날짜 | 검색 시작일 |
| end_dateRequired날짜 | 검색 종료일 |
| payment_method | 결제수단   ,(콤마)로 여러 건을 검색할 수 있다.   cash : 무통장 icash : 가상계좌 |
| settle_type | 결제타입   S: 기본결제 E: 추가결제 |
| limit최소: [1]~최대: [500] | 조회결과 최대건수   DEFAULT 10 |
| offset최대값: [15000] | 조회결과 시작위치   DEFAULT 0 |
| order | 정렬 순서   asc : 순차정렬 desc : 역순 정렬   DEFAULT desc |

```bash
Retrieve unpaid orders        Retrieve unpaid orders       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/unpaidorders?start_date=2025-06-06&end_date=2025-07-06&payment_method=cash,icash&settle_type=S' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "unpaidorders": [        {            "shop_no": 1,            "order_id": "20250604-0000023",            "order_item_code": [                "20250604-0000023-01",                "20250605-0000023-02"            ],            "order_date": "2025-06-04T12:30:00+09:00",            "buyer_name": "John Doe",            "billing_name": "John Doe",            "bank_code": "bank_001",            "bank_name": "Kakao Bank",            "unpaid_amount": "1000",            "accounts": "123456",            "payment_method": "cash",            "settle_type": "S",            "payment_no": 2        },        {            "shop_no": 1,            "order_id": "20250604-0000024",            "order_item_code": [                "20210101-0000024-03",                "20210101-0000024-04"            ],            "order_date": "2025-06-04T12:30:00+09:00",            "buyer_name": "John Doe",            "billing_name": "John Doe124",            "bank_code": "bank_005",            "bank_name": "Shinhan Bank",            "unpaid_amount": "2000",            "accounts": "54321",            "payment_method": "icash",            "settle_type": "E",            "payment_no": 3        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/unpaidorders?start_date=2025-06-06&end_date=2025-07-06&payment_method=cash,icash&settle_type=S' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "unpaidorders": [        {            "shop_no": 1,            "order_id": "20250604-0000023",            "order_item_code": [                "20250604-0000023-01",                "20250605-0000023-02"            ],            "order_date": "2025-06-04T12:30:00+09:00",            "buyer_name": "John Doe",            "billing_name": "John Doe",            "bank_code": "bank_001",            "bank_name": "Kakao Bank",            "unpaid_amount": "1000",            "accounts": "123456",            "payment_method": "cash",            "settle_type": "S",            "payment_no": 2        },        {            "shop_no": 1,            "order_id": "20250604-0000024",            "order_item_code": [                "20210101-0000024-03",                "20210101-0000024-04"            ],            "order_date": "2025-06-04T12:30:00+09:00",            "buyer_name": "John Doe",            "billing_name": "John Doe124",            "bank_code": "bank_005",            "bank_name": "Shinhan Bank",            "unpaid_amount": "2000",            "accounts": "54321",            "payment_method": "icash",            "settle_type": "E",            "payment_no": 3        }    ]}
```
