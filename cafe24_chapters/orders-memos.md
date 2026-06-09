# ORDERS MEMOS


## Orders memos

```json
Endpoints    GET /api/v2/admin/orders/{order_id}/memos
POST /api/v2/admin/orders/{order_id}/memos
PUT /api/v2/admin/orders/{order_id}/memos/{memo_no}
DELETE /api/v2/admin/orders/{order_id}/memos/{memo_no}
```

```json
GET /api/v2/admin/orders/{order_id}/memos
POST /api/v2/admin/orders/{order_id}/memos
PUT /api/v2/admin/orders/{order_id}/memos/{memo_no}
DELETE /api/v2/admin/orders/{order_id}/memos/{memo_no}
```

### Orders memos property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| memo_no | 메모 번호 |
| created_date | 메모 등록일 |
| author_id | 작성자 아이디 |
| ip | 작성자 아이피 |
| use_customer_inquiry | 고객상담 동시등록 여부 T : 사용함 F : 사용안함 |
| attach_type | 등록기준 O : 주문별 P : 품목별 |
| content | 메모 내용 |
| starred_memo | 중요 메모 여부 T : 중요 메모 F : 일반 메모 |
| fixed | 상단고정 여부 T : 사용함 F : 사용안함 |
| product_list | 상품 목록 |
| topic_type | 상담분류 cs_01 : 배송문의 cs_02 : 상품문의 cs_03 : 결제문의 cs_04 : 주문취소 cs_05 : 상품변경 |
| status | 상담결과 F : 처리중 T : 처리완료 |

### Retrieve a list of order memos   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 읽기권한 (mall.read_order) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| order_idRequired주문번호 | 주문번호 |

```bash
Retrieve a list of order memos        Retrieve a list of order memos Retrieve memos with fields parameter       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Create an order memo   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 쓰기권한 (mall.write_order) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| order_idRequired주문번호 | 주문번호 |
| contentRequired최대글자수 : [1000자] | 메모 내용 |
| use_customer_inquiry | 고객상담 동시등록 여부   T : 사용함 F : 사용안함   DEFAULT F |
| topic_type | 상담분류   cs_01 : 배송문의 cs_02 : 상품문의 cs_03 : 결제문의 cs_04 : 주문취소 cs_05 : 상품변경 |
| status | 상담결과   F : 처리중 T : 처리완료 |
| attach_type | 등록기준   O : 주문별 P : 품목별   DEFAULT O |
| starred_memo | 중요 메모 여부   T : 중요 메모 F : 일반 메모   DEFAULT F |
| fixed | 상단고정 여부   T : 사용함 F : 사용안함   DEFAULT F |
| product_list | 상품 목록 |

```bash
Create an order memo        Create an order memo Post an order memo using only content field Try posting an order memo without content field       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Update an order memo   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 쓰기권한 (mall.write_order) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| order_idRequired주문번호 | 주문번호 |
| memo_noRequired | 메모 번호 |
| content최대글자수 : [1000자] | 메모 내용 |
| use_customer_inquiry | 고객상담 동시등록 여부   T : 사용함 F : 사용안함   DEFAULT F |
| topic_type | 상담분류   cs_01 : 배송문의 cs_02 : 상품문의 cs_03 : 결제문의 cs_04 : 주문취소 cs_05 : 상품변경 |
| status | 상담결과   F : 처리중 T : 처리완료 |
| attach_type | 등록기준   O : 주문별 P : 품목별   DEFAULT O |
| starred_memo | 중요 메모 여부   T : 중요 메모 F : 일반 메모   DEFAULT F |
| fixed | 상단고정 여부   T : 사용함 F : 사용안함   DEFAULT F |
| product_list | 상품 목록 |

```bash
Update an order memo        Update an order memo Change memo to attach product code       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Delete an order memo   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 쓰기권한 (mall.write_order) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| order_idRequired주문번호 | 주문번호 |
| memo_noRequired | 메모 번호 |

```bash
Delete an order memo        Delete an order memo       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

## Orders memos

```json
Endpoints    GET /api/v2/admin/orders/memos
```

```json
GET /api/v2/admin/orders/memos
```

### Orders memos property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| memo_no | 메모 번호 |
| order_id | 주문번호 |
| created_date | 메모 등록일 |
| author_id | 작성자 아이디 |
| ip | 작성자 아이피 |
| use_customer_inquiry | 고객상담 동시등록 여부 T : 사용함 F : 사용안함 |
| attach_type | 등록기준 O : 주문별 P : 품목별 |
| content | 메모 내용 |
| starred_memo | 중요 메모 여부 T : 중요 메모 F : 일반 메모 |
| fixed | 상단고정 여부 T : 사용함 F : 사용안함 |
| product_list | 상품 목록 |

### Retrieve a list of admin memos for an order   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 읽기권한 (mall.read_order) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| order_idRequired주문번호 | 주문번호   ,(콤마)로 여러 건을 검색할 수 있다. |
| limit최소: [1]~최대: [500] | 조회결과 최대건수   DEFAULT 10 |
| offset최대값: [8000] | 조회결과 시작위치   DEFAULT 0 |

```bash
Retrieve a list of admin memos for an order        Retrieve a list of admin memos for an order Retrieve memos with fields parameter Retrieve multiple memos Retrieve memos using paging       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/orders/memos?order_id=20200113-0000011' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "memos": [        {            "shop_no": 1,            "memo_no": 13,            "order_id": "20200113-0000011",            "created_date": "2020-01-13T09:53:33+09:00",            "author_id": "sampleid",            "ip": "127.0.0.1",            "use_customer_inquiry": "F",            "attach_type": "P",            "content": "sample memo content",            "starred_memo": "F",            "fixed": "F",            "product_list": [                {                    "product_no": 11,                    "option_code": "000A"                },                {                    "product_no": 12,                    "option_code": "000A"                }            ]        },        {            "shop_no": 1,            "memo_no": 14,            "order_id": "20200113-0000011",            "created_date": "2020-01-14T10:53:41+09:00",            "author_id": "sampleid",            "ip": "127.0.0.1",            "use_customer_inquiry": "F",            "attach_type": "P",            "content": "sample memo content",            "starred_memo": "F",            "fixed": "F",            "product_list": [                {                    "product_no": 11,                    "option_code": "000A"                },                {                    "product_no": 12,                    "option_code": "000A"                }            ]        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/orders/memos?order_id=20200113-0000011' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "memos": [        {            "shop_no": 1,            "memo_no": 13,            "order_id": "20200113-0000011",            "created_date": "2020-01-13T09:53:33+09:00",            "author_id": "sampleid",            "ip": "127.0.0.1",            "use_customer_inquiry": "F",            "attach_type": "P",            "content": "sample memo content",            "starred_memo": "F",            "fixed": "F",            "product_list": [                {                    "product_no": 11,                    "option_code": "000A"                },                {                    "product_no": 12,                    "option_code": "000A"                }            ]        },        {            "shop_no": 1,            "memo_no": 14,            "order_id": "20200113-0000011",            "created_date": "2020-01-14T10:53:41+09:00",            "author_id": "sampleid",            "ip": "127.0.0.1",            "use_customer_inquiry": "F",            "attach_type": "P",            "content": "sample memo content",            "starred_memo": "F",            "fixed": "F",            "product_list": [                {                    "product_no": 11,                    "option_code": "000A"                },                {                    "product_no": 12,                    "option_code": "000A"                }            ]        }    ]}
```
