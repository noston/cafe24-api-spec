# DISCOUNTCODES


## Discountcodes

```json
Endpoints    GET /api/v2/admin/discountcodes
GET /api/v2/admin/discountcodes/{discount_code_no}
POST /api/v2/admin/discountcodes
PUT /api/v2/admin/discountcodes/{discount_code_no}
DELETE /api/v2/admin/discountcodes/{discount_code_no}
```

```json
GET /api/v2/admin/discountcodes
GET /api/v2/admin/discountcodes/{discount_code_no}
POST /api/v2/admin/discountcodes
PUT /api/v2/admin/discountcodes/{discount_code_no}
DELETE /api/v2/admin/discountcodes/{discount_code_no}
```

### Discountcodes property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| discount_code_no | 할인코드 번호 |
| discount_code_name | 할인코드 이름 |
| discount_code | 할인코드 |
| available_start_date | 시작일 |
| available_end_date | 종료일 |
| available_product_type | 할인코드 적용범위 할인코드의 적용범위가 A(전체상품) 일 경우 할인코드적용 상품(available_product) 및 할인코드적용 분류(available_category) 는 입력 필요 없음할인코드의 적용범위가 P(특정상품) 일 경우 할인코드적용 상품(available_product) 은 필수 입력 할인코드의 적용범위가 C(특정분류) 일 경우 할인코드적용 분류(available_category)는 필수 입력 A : 전체상품 P : 특정상품 C : 특정분류 |
| created_date | 혜택 등록일 |
| available_issue_count | 최대 발급 횟수 |
| issued_count | 발급된 수량 |
| discount_value | 할인 값 |
| discount_truncation_unit | 절사 단위 C : 0.01단위 B : 0.1단위 F : 절사안함 O : 1원단위 T : 10원단위 M : 100원단위 H : 1000원 단위 |
| discount_max_price | 혜택 최대 금액 |
| available_product | 특정상품 리스트 할인코드 적용범위(available_product_type)가 P(특정상품) 의 경우 상품번호를 배열로 입력한다. |
| available_category | 특정분류 리스트 할인코드 적용범위(available_product_type)가 C(특정분류) 의 경우 분류번호를 배열로 입력한다. |
| available_min_price | 이용 주문 최소 금액 |
| available_user | 사용가능 대상 |
| max_usage_per_user | 회원당 사용가능 횟수 |

### Retrieve a list of discount codes   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 프로모션 읽기권한 (mall.read_promotion) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| discount_code_name | 할인코드 이름 |
| discount_code | 할인코드 |
| search_date_type | available_start_date : 시작일 available_end_date : 종료일 created_date : 등록일   available_start_date : 시작일  available_end_date : 종료일  created_date : 등록일 |
| start_date날짜 | 검색 시작일 |
| end_date날짜 | 검색 종료일 |
| offset최대값: [8000] | 조회결과 시작위치   DEFAULT 0 |
| limit최소: [1]~최대: [100] | 조회결과 최대건수   DEFAULT 10 |
| sort | 정렬 순서 값   discount_code_name : 혜택이름  discount_code : 할인코드  created_date : 등록시간  available_start_date : 시작시간 available_end_date : 종료시간   DEFAULT created_date |
| order | 정렬 순서   asc : 순차정렬 desc : 역순 정렬   DEFAULT desc |

```bash
Retrieve a list of discount codes        Retrieve a list of discount codes       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/discountcodes' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "discountcodes": [        {            "shop_no": 1,            "discount_code_no": 1,            "discount_code": "DISCOUNT1",            "discount_code_name": "123456",            "available_product_type": "P",            "available_start_date": "2024-09-10T11:10:34+09:00",            "available_end_date": "2024-09-20T13:10:34+09:00",            "created_date": "2019-12-13T10:10:10:34+09:00",            "issued_count": 30,            "available_issue_count": 100        },        {            "shop_no": 1,            "discount_code_no": 2,            "discount_code": "DISCOUNT2",            "discount_code_name": "123456",            "available_product_type": "P",            "available_start_date": "2024-09-10T11:10:34+09:00",            "available_end_date": "2024-09-20T13:10:34+09:00",            "created_date": "2019-12-13T10:10:10:34+09:00",            "issued_count": 30,            "available_issue_count": 100        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/discountcodes' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "discountcodes": [        {            "shop_no": 1,            "discount_code_no": 1,            "discount_code": "DISCOUNT1",            "discount_code_name": "123456",            "available_product_type": "P",            "available_start_date": "2024-09-10T11:10:34+09:00",            "available_end_date": "2024-09-20T13:10:34+09:00",            "created_date": "2019-12-13T10:10:10:34+09:00",            "issued_count": 30,            "available_issue_count": 100        },        {            "shop_no": 1,            "discount_code_no": 2,            "discount_code": "DISCOUNT2",            "discount_code_name": "123456",            "available_product_type": "P",            "available_start_date": "2024-09-10T11:10:34+09:00",            "available_end_date": "2024-09-20T13:10:34+09:00",            "created_date": "2019-12-13T10:10:10:34+09:00",            "issued_count": 30,            "available_issue_count": 100        }    ]}
```

### Retrieve a discount code   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 프로모션 읽기권한 (mall.read_promotion) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| discount_code_noRequired최소값: [1] | 할인코드 번호 |

```bash
Retrieve a discount code        Retrieve a discount code       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/discountcodes/23?shop_no=1' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "discountcode": {        "shop_no": 1,        "discount_code_no": 23,        "discount_code": "DISCOUNT1",        "discount_code_name": "discount for customer",        "discount_value": 10,        "discount_truncation_unit": "M",        "discount_max_price": 10000,        "available_start_date": "2024-09-10T11:10:34+09:00",        "available_end_date": "2024-09-20T13:10:34+09:00",        "available_product_type": "P",        "available_product": [            10,            12        ],        "available_category": null,        "available_min_price": 1000,        "available_issue_count": 1000,        "available_user": "A",        "max_usage_per_user": 3    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/discountcodes/23?shop_no=1' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "discountcode": {        "shop_no": 1,        "discount_code_no": 23,        "discount_code": "DISCOUNT1",        "discount_code_name": "discount for customer",        "discount_value": 10,        "discount_truncation_unit": "M",        "discount_max_price": 10000,        "available_start_date": "2024-09-10T11:10:34+09:00",        "available_end_date": "2024-09-20T13:10:34+09:00",        "available_product_type": "P",        "available_product": [            10,            12        ],        "available_category": null,        "available_min_price": 1000,        "available_issue_count": 1000,        "available_user": "A",        "max_usage_per_user": 3    }}
```

### Create a discount code   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 프로모션 쓰기권한 (mall.write_promotion) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| discount_codeRequired최소글자수 : [1자]최대글자수 : [35자] | 할인코드 |
| discount_code_nameRequired글자수 최소: [1자]~최대: [50자] | 할인코드 이름 |
| discount_valueRequired최소값: [1]최대값: [99] | 할인 값 |
| discount_truncation_unitRequired | 절사 단위   C : 0.01단위 B : 0.1단위 F : 절사안함 O : 1원단위 T : 10원단위 M : 100원단위 H : 1000원 단위 |
| discount_max_priceRequired최소값: [1]최대값: [999999999] | 혜택 최대 금액 |
| available_start_dateRequired날짜 | 시작일 |
| available_end_dateRequired날짜 | 종료일 |
| available_product_type | 할인코드 적용범위   할인코드의 적용범위가 A(전체상품) 일 경우 할인코드적용 상품(available_product) 및 할인코드적용 분류(available_category) 는 입력 필요 없음할인코드의 적용범위가 P(특정상품) 일 경우 할인코드적용 상품(available_product) 은 필수 입력 할인코드의 적용범위가 C(특정분류) 일 경우 할인코드적용 분류(available_category)는 필수 입력 A : 전체상품 P : 특정상품 C : 특정분류   DEFAULT A |
| available_product | 특정상품 리스트   할인코드 적용범위(available_product_type)가 P(특정상품) 의 경우 상품번호를 배열로 입력한다. |
| available_category | 특정분류 리스트   할인코드 적용범위(available_product_type)가 C(특정분류) 의 경우 분류번호를 배열로 입력한다. |
| available_min_price최대값: [999999999] | 이용 주문 최소 금액   DEFAULT 0 |
| available_issue_count최대값: [10000] | 최대 발급 횟수   DEFAULT 0 |
| available_user | 사용가능 대상   M : 회원 A : 전체   DEFAULT A |
| max_usage_per_user최대값: [999] | 회원당 사용가능 횟수   DEFAULT 0 |

```bash
Create a discount code        Create a discount code       Request   cURL Java Python Node.js PHP Go  Copy     curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/discountcodes' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "discount_code": "DISCOUNT1",        "discount_code_name": "discount for customer",        "discount_value": 10,        "discount_truncation_unit": "M",        "discount_max_price": 10000,        "available_start_date": "2036-10-05 11:10:34",        "available_end_date": "2036-10-20 13:10:34",        "available_product_type": "P",        "available_product": [            9,            10        ],        "available_category": null,        "available_min_price": 1000,        "available_issue_count": 1000,        "available_user": "A",        "max_usage_per_user": 3    }}'    Response  Copy     {    "discountcode": {        "shop_no": 1,        "discount_code_no": 23,        "discount_code": "DISCOUNT1",        "discount_code_name": "discount for customer",        "discount_value": 10,        "discount_truncation_unit": "M",        "discount_max_price": 10000,        "available_start_date": "2036-10-05T11:10:34+09:00",        "available_end_date": "2036-10-20T13:10:34+09:00",        "available_product_type": "P",        "available_product": [            9,            10        ],        "available_category": null,        "available_min_price": 1000,        "available_issue_count": 1000,        "available_user": "A",        "max_usage_per_user": 3    }}
```

```bash
curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/discountcodes' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "discount_code": "DISCOUNT1",        "discount_code_name": "discount for customer",        "discount_value": 10,        "discount_truncation_unit": "M",        "discount_max_price": 10000,        "available_start_date": "2036-10-05 11:10:34",        "available_end_date": "2036-10-20 13:10:34",        "available_product_type": "P",        "available_product": [            9,            10        ],        "available_category": null,        "available_min_price": 1000,        "available_issue_count": 1000,        "available_user": "A",        "max_usage_per_user": 3    }}'
```

```json
{    "discountcode": {        "shop_no": 1,        "discount_code_no": 23,        "discount_code": "DISCOUNT1",        "discount_code_name": "discount for customer",        "discount_value": 10,        "discount_truncation_unit": "M",        "discount_max_price": 10000,        "available_start_date": "2036-10-05T11:10:34+09:00",        "available_end_date": "2036-10-20T13:10:34+09:00",        "available_product_type": "P",        "available_product": [            9,            10        ],        "available_category": null,        "available_min_price": 1000,        "available_issue_count": 1000,        "available_user": "A",        "max_usage_per_user": 3    }}
```

### Update a discount code   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 프로모션 쓰기권한 (mall.write_promotion) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| discount_code_noRequired최소값: [1] | 할인코드 번호 |
| discount_code최소글자수 : [1자]최대글자수 : [35자] | 할인코드 |
| discount_code_nameRequired글자수 최소: [1자]~최대: [50자] | 할인코드 이름 |
| discount_value최소값: [1]최대값: [99] | 할인 값 |
| discount_truncation_unit | 절사 단위   C : 0.01단위 B : 0.1단위 F : 절사안함 O : 1원단위 T : 10원단위 M : 100원단위 H : 1000원 단위 |
| discount_max_price최소값: [1]최대값: [999999999] | 혜택 최대 금액 |
| available_start_date날짜 | 시작일 |
| available_end_date날짜 | 종료일 |
| available_product_type | 할인코드 적용범위   할인코드의 적용범위가 A(전체상품) 일 경우 할인코드적용 상품(available_product) 및 할인코드적용 분류(available_category) 는 입력 필요 없음할인코드의 적용범위가 P(특정상품) 일 경우 할인코드적용 상품(available_product) 은 필수 입력 할인코드의 적용범위가 C(특정분류) 일 경우 할인코드적용 분류(available_category)는 필수 입력 A : 전체상품 P : 특정상품 C : 특정분류 |
| available_product | 특정상품 리스트   할인코드 적용범위(available_product_type)가 P(특정상품) 의 경우 상품번호를 배열로 입력한다. |
| available_category | 특정분류 리스트   할인코드 적용범위(available_product_type)가 C(특정분류) 의 경우 분류번호를 배열로 입력한다. |
| available_min_price최대값: [999999999] | 이용 주문 최소 금액 |
| available_issue_count최대값: [10000] | 최대 발급 횟수 |
| available_user | 사용가능 대상   M : 회원 A : 전체 |
| max_usage_per_user최대값: [999] | 회원당 사용가능 횟수 |

```bash
Update a discount code        Update a discount code       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/discountcodes/23' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "discount_code": "DISCOUNT1",        "discount_code_name": "discount for customer",        "discount_value": 10,        "discount_truncation_unit": "M",        "discount_max_price": 10000,        "available_start_date": "2036-09-10 11:10:34",        "available_end_date": "2036-09-20 13:10:34",        "available_product_type": "P",        "available_product": [            9,            10        ],        "available_category": null,        "available_min_price": 1000,        "available_issue_count": 1000,        "available_user": "A",        "max_usage_per_user": 3    }}'    Response  Copy     {    "discountcode": {        "shop_no": 1,        "discount_code_no": 23,        "discount_code": "DISCOUNT1",        "discount_code_name": "discount for customer",        "discount_value": 10,        "discount_truncation_unit": "M",        "discount_max_price": 10000,        "available_start_date": "2036-09-10T11:10:34+09:00",        "available_end_date": "2036-09-20T13:10:34+09:00",        "available_product_type": "P",        "available_product": [            9,            10        ],        "available_category": null,        "available_min_price": 1000,        "available_issue_count": 1000,        "available_user": "A",        "max_usage_per_user": 3    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/discountcodes/23' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "discount_code": "DISCOUNT1",        "discount_code_name": "discount for customer",        "discount_value": 10,        "discount_truncation_unit": "M",        "discount_max_price": 10000,        "available_start_date": "2036-09-10 11:10:34",        "available_end_date": "2036-09-20 13:10:34",        "available_product_type": "P",        "available_product": [            9,            10        ],        "available_category": null,        "available_min_price": 1000,        "available_issue_count": 1000,        "available_user": "A",        "max_usage_per_user": 3    }}'
```

```json
{    "discountcode": {        "shop_no": 1,        "discount_code_no": 23,        "discount_code": "DISCOUNT1",        "discount_code_name": "discount for customer",        "discount_value": 10,        "discount_truncation_unit": "M",        "discount_max_price": 10000,        "available_start_date": "2036-09-10T11:10:34+09:00",        "available_end_date": "2036-09-20T13:10:34+09:00",        "available_product_type": "P",        "available_product": [            9,            10        ],        "available_category": null,        "available_min_price": 1000,        "available_issue_count": 1000,        "available_user": "A",        "max_usage_per_user": 3    }}
```

### Delete a discount code   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 프로모션 쓰기권한 (mall.write_promotion) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| discount_code_noRequired최소값: [1] | 할인코드 번호 |

```bash
Delete a discount code        Delete a discount code       Request   cURL Java Python Node.js PHP Go  Copy     curl -X DELETE \  'https://{mallid}.cafe24api.com/api/v2/admin/discountcodes/23' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "discountcode": {        "discount_code_no": 23    }}
```

```bash
curl -X DELETE \  'https://{mallid}.cafe24api.com/api/v2/admin/discountcodes/23' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "discountcode": {        "discount_code_no": 23    }}
```
