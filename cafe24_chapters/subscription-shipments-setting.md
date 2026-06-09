# SUBSCRIPTION SHIPMENTS SETTING


## Subscription shipments setting

```json
Endpoints    GET /api/v2/admin/subscription/shipments/setting
POST /api/v2/admin/subscription/shipments/setting
PUT /api/v2/admin/subscription/shipments/setting/{subscription_no}
DELETE /api/v2/admin/subscription/shipments/setting/{subscription_no}
```

```json
GET /api/v2/admin/subscription/shipments/setting
POST /api/v2/admin/subscription/shipments/setting
PUT /api/v2/admin/subscription/shipments/setting/{subscription_no}
DELETE /api/v2/admin/subscription/shipments/setting/{subscription_no}
```

### Subscription shipments setting property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| subscription_no | 정기배송 상품설정 번호 |
| subscription_shipments_name | 정기배송 상품설정 명 |
| product_binding_type | 정기배송 상품 설정 A : 전체상품 P : 개별상품 C : 상품분류 |
| one_time_purchase | 1회구매 제공여부 T : 제공함 F : 제공안함 |
| product_list | 적용 상품 |
| category_list | 적용 분류 |
| use_discount | 정기배송 할인 사용여부 T : 사용함 F : 사용안함 |
| discount_value_unit | 할인 기준 P : 할인율 W : 할인 금액 |
| discount_values | 할인 값 |
| related_purchase_quantity | 구매수량 관계 여부 T : 구매수량에 따라 F : 구매수량에 관계없이 |
| subscription_shipments_cycle_type | 배송주기 제공여부 T : 사용함 F : 사용안함 |
| subscription_shipments_cycle | 배송주기 1W : 1주 2W : 2주 3W : 3주 4W : 4주 1M : 1개월 2M : 2개월 3M : 3개월 4M : 4개월 5M : 5개월 6M : 6개월 1Y : 1년 |
| subscription_shipments_count_type | 정기배송 횟수 설정 T : 사용함 F : 사용안함 |
| subscription_shipments_count | 정기배송 횟수 2 : 2회 3 : 3회 4 : 4회 6 : 6회 8 : 8회 10 : 10회 12 : 12회 |
| use_order_price_condition | 혜택제공금액기준 사용여부 T : 사용함 F : 사용안함 |
| order_price_greater_than | 혜택제공금액기준 제공 기준금액 |
| include_regional_shipping_rate | 지역별배송비 포함여부 T : 포함 F : 미포함 |
| shipments_start_date최소값: [1]최대값: [30] | 배송시작일 설정 |
| change_option | 옵션 변경 가능 여부 T : 사용함 F : 사용안함 |

### Retrieve a list of subscription products   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 읽기권한 (mall.read_store) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| subscription_no | 정기배송 상품설정 번호 |

```bash
Retrieve a list of subscription products        Retrieve a list of subscription products Retrieve setting with fields parameter Retrieve a specific setting with subscription_no parameter       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/subscription/shipments/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "shipments": [        {            "shop_no": 1,            "subscription_no": 70,            "subscription_shipments_name": "SHIRTS SUBSCRIPTION SHIPMENTS",            "product_binding_type": "P",            "one_time_purchase": "T",            "product_list": [                11,                13            ],            "category_list": null,            "use_discount": "T",            "discount_value_unit": "P",            "discount_values": [                {                    "delivery_cycle": 1,                    "discount_amount": 10                },                {                    "delivery_cycle": 5,                    "discount_amount": 20                }            ],            "subscription_shipments_cycle_type": "T",            "subscription_shipments_cycle": [                "1M",                "2M"            ],            "subscription_shipments_count_type": "T",            "subscription_shipments_count": [                4,                6,                8,                10            ],            "use_order_price_condition": "T",            "order_price_greater_than": "25000.00",            "include_regional_shipping_rate": "F",            "shipments_start_date": 3,            "change_option": "F"        },        {            "shop_no": 1,            "subscription_no": 71,            "subscription_shipments_name": "SHIRTS SUBSCRIPTION SHIPMENTS",            "product_binding_type": "P",            "one_time_purchase": "T",            "product_list": [                11,                13            ],            "category_list": null,            "use_discount": "T",            "discount_value_unit": "P",            "discount_values": [                {                    "delivery_cycle": 1,                    "discount_amount": 10                },                {                    "delivery_cycle": 5,                    "discount_amount": 20                }            ],            "subscription_shipments_cycle_type": "T",            "subscription_shipments_cycle": [                "1M",                "2M"            ],            "subscription_shipments_count_type": "T",            "subscription_shipments_count": [                4,                6,                8,                10            ],            "use_order_price_condition": "T",            "order_price_greater_than": "25000.00",            "include_regional_shipping_rate": "F",            "shipments_start_date": 3,            "change_option": "T"        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/subscription/shipments/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "shipments": [        {            "shop_no": 1,            "subscription_no": 70,            "subscription_shipments_name": "SHIRTS SUBSCRIPTION SHIPMENTS",            "product_binding_type": "P",            "one_time_purchase": "T",            "product_list": [                11,                13            ],            "category_list": null,            "use_discount": "T",            "discount_value_unit": "P",            "discount_values": [                {                    "delivery_cycle": 1,                    "discount_amount": 10                },                {                    "delivery_cycle": 5,                    "discount_amount": 20                }            ],            "subscription_shipments_cycle_type": "T",            "subscription_shipments_cycle": [                "1M",                "2M"            ],            "subscription_shipments_count_type": "T",            "subscription_shipments_count": [                4,                6,                8,                10            ],            "use_order_price_condition": "T",            "order_price_greater_than": "25000.00",            "include_regional_shipping_rate": "F",            "shipments_start_date": 3,            "change_option": "F"        },        {            "shop_no": 1,            "subscription_no": 71,            "subscription_shipments_name": "SHIRTS SUBSCRIPTION SHIPMENTS",            "product_binding_type": "P",            "one_time_purchase": "T",            "product_list": [                11,                13            ],            "category_list": null,            "use_discount": "T",            "discount_value_unit": "P",            "discount_values": [                {                    "delivery_cycle": 1,                    "discount_amount": 10                },                {                    "delivery_cycle": 5,                    "discount_amount": 20                }            ],            "subscription_shipments_cycle_type": "T",            "subscription_shipments_cycle": [                "1M",                "2M"            ],            "subscription_shipments_count_type": "T",            "subscription_shipments_count": [                4,                6,                8,                10            ],            "use_order_price_condition": "T",            "order_price_greater_than": "25000.00",            "include_regional_shipping_rate": "F",            "shipments_start_date": 3,            "change_option": "T"        }    ]}
```

### Create a subscription payment rule   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 쓰기권한 (mall.write_store) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| subscription_shipments_nameRequired최대글자수 : [255자] | 정기배송 상품설정 명 |
| product_binding_typeRequired | 정기배송 상품 설정   A : 전체상품 P : 개별상품 C : 상품분류 |
| one_time_purchase | 1회구매 제공여부   T : 제공함 F : 제공안함   DEFAULT T |
| product_list배열 최대사이즈: [10000] | 적용 상품 |
| category_list배열 최대사이즈: [1000] | 적용 분류 |
| use_discountRequired | 정기배송 할인 사용여부   T : 사용함 F : 사용안함 |
| discount_value_unit | 할인 기준   P : 할인율 W : 할인 금액 |
| discount_values배열 최대사이즈: [40] | 할인 값   discount_value_unit이 P일 경우 최대값 : 100 discount_value_unit이 W일 경우 최대값 : 99999999999999 |
| discount_values 하위 요소 보기     delivery_cycleRequired적용회차 discount_amountRequired할인 값 |
| related_purchase_quantity | 구매수량 관계 여부   T : 구매수량에 따라 F : 구매수량에 관계없이 |
| subscription_shipments_cycle_typeRequired | 배송주기 제공여부   T : 사용함 F : 사용안함 |
| subscription_shipments_cycleRequired | 배송주기   1W : 1주 2W : 2주 3W : 3주 4W : 4주 1M : 1개월 2M : 2개월 3M : 3개월 4M : 4개월 5M : 5개월 6M : 6개월 1Y : 1년 |
| subscription_shipments_count_type | 정기배송 횟수 설정   T : 사용함 F : 사용안함 |
| subscription_shipments_count배열 최대사이즈: [7] | 정기배송 횟수   2 : 2회 3 : 3회 4 : 4회 6 : 6회 8 : 8회 10 : 10회 12 : 12회 |
| use_order_price_conditionRequired | 혜택제공금액기준 사용여부   T : 사용함 F : 사용안함 |
| order_price_greater_than최대값: [99999999999999] | 혜택제공금액기준 제공 기준금액 |
| include_regional_shipping_rate | 지역별배송비 포함여부   T : 포함 F : 미포함 |
| shipments_start_date최소값: [1]최대값: [30] | 배송시작일 설정   DEFAULT 3 |
| change_option | 옵션 변경 가능 여부   T : 사용함 F : 사용안함   DEFAULT F |

```bash
Create a subscription payment rule        Create a subscription payment rule       Request   cURL Java Python Node.js PHP Go  Copy     curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/subscription/shipments/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "subscription_shipments_name": "SHIRTS SUBSCRIPTION SHIPMENTS",        "product_binding_type": "P",        "one_time_purchase": "T",        "product_list": [            11,            13        ],        "category_list": null,        "use_discount": "T",        "discount_value_unit": "P",        "discount_values": [            {                "delivery_cycle": 1,                "discount_amount": 10            },            {                "delivery_cycle": 5,                "discount_amount": 20            }        ],        "subscription_shipments_cycle_type": "T",        "subscription_shipments_cycle": [            "1M",            "2M"        ],        "subscription_shipments_count_type": "T",        "subscription_shipments_count": [            4,            6,            8,            10        ],        "use_order_price_condition": "T",        "order_price_greater_than": "25000.00",        "include_regional_shipping_rate": "F",        "shipments_start_date": 3,        "change_option": "F"    }}'    Response  Copy     {    "shipment": {        "shop_no": 1,        "subscription_no": 70,        "subscription_shipments_name": "SHIRTS SUBSCRIPTION SHIPMENTS",        "product_binding_type": "P",        "one_time_purchase": "T",        "product_list": [            11,            13        ],        "category_list": null,        "use_discount": "T",        "discount_value_unit": "P",        "discount_values": [            {                "delivery_cycle": 1,                "discount_amount": 10            },            {                "delivery_cycle": 5,                "discount_amount": 20            }        ],        "subscription_shipments_cycle_type": "T",        "subscription_shipments_cycle": [            "1M",            "2M"        ],        "subscription_shipments_count_type": "T",        "subscription_shipments_count": [            4,            6,            8,            10        ],        "use_order_price_condition": "T",        "order_price_greater_than": "25000.00",        "include_regional_shipping_rate": "F",        "shipments_start_date": 3,        "change_option": "F"    }}
```

```bash
curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/subscription/shipments/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "subscription_shipments_name": "SHIRTS SUBSCRIPTION SHIPMENTS",        "product_binding_type": "P",        "one_time_purchase": "T",        "product_list": [            11,            13        ],        "category_list": null,        "use_discount": "T",        "discount_value_unit": "P",        "discount_values": [            {                "delivery_cycle": 1,                "discount_amount": 10            },            {                "delivery_cycle": 5,                "discount_amount": 20            }        ],        "subscription_shipments_cycle_type": "T",        "subscription_shipments_cycle": [            "1M",            "2M"        ],        "subscription_shipments_count_type": "T",        "subscription_shipments_count": [            4,            6,            8,            10        ],        "use_order_price_condition": "T",        "order_price_greater_than": "25000.00",        "include_regional_shipping_rate": "F",        "shipments_start_date": 3,        "change_option": "F"    }}'
```

```json
{    "shipment": {        "shop_no": 1,        "subscription_no": 70,        "subscription_shipments_name": "SHIRTS SUBSCRIPTION SHIPMENTS",        "product_binding_type": "P",        "one_time_purchase": "T",        "product_list": [            11,            13        ],        "category_list": null,        "use_discount": "T",        "discount_value_unit": "P",        "discount_values": [            {                "delivery_cycle": 1,                "discount_amount": 10            },            {                "delivery_cycle": 5,                "discount_amount": 20            }        ],        "subscription_shipments_cycle_type": "T",        "subscription_shipments_cycle": [            "1M",            "2M"        ],        "subscription_shipments_count_type": "T",        "subscription_shipments_count": [            4,            6,            8,            10        ],        "use_order_price_condition": "T",        "order_price_greater_than": "25000.00",        "include_regional_shipping_rate": "F",        "shipments_start_date": 3,        "change_option": "F"    }}
```

### Update subscription products   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 쓰기권한 (mall.write_store) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| subscription_noRequired | 정기배송 상품설정 번호 |
| subscription_shipments_name최대글자수 : [255자] | 정기배송 상품설정 명 |
| product_binding_type | 정기배송 상품 설정   A : 전체상품 P : 개별상품 C : 상품분류 |
| one_time_purchase | 1회구매 제공여부   T : 제공함 F : 제공안함 |
| product_list배열 최대사이즈: [10000] | 적용 상품 |
| category_list배열 최대사이즈: [1000] | 적용 분류 |
| use_discount | 정기배송 할인 사용여부   T : 사용함 F : 사용안함 |
| discount_value_unit | 할인 기준   P : 할인율 W : 할인 금액 |
| discount_values배열 최대사이즈: [40] | 할인 값 |
| discount_values 하위 요소 보기     delivery_cycleRequired적용회차 discount_amountRequired할인 값 |
| related_purchase_quantity | 구매수량 관계 여부   T : 구매수량에 따라 F : 구매수량에 관계없이 |
| subscription_shipments_cycle_type | 배송주기 제공여부   T : 사용함 F : 사용안함 |
| subscription_shipments_cycle | 배송주기   1W : 1주 2W : 2주 3W : 3주 4W : 4주 1M : 1개월 2M : 2개월 3M : 3개월 4M : 4개월 5M : 5개월 6M : 6개월 1Y : 1년 |
| subscription_shipments_count_type | 정기배송 횟수 설정   T : 사용함 F : 사용안함 |
| subscription_shipments_count배열 최대사이즈: [7] | 정기배송 횟수   2 : 2회 3 : 3회 4 : 4회 6 : 6회 8 : 8회 10 : 10회 12 : 12회 |
| use_order_price_condition | 혜택제공금액기준 사용여부   T : 사용함 F : 사용안함 |
| order_price_greater_than최대값: [99999999999999] | 혜택제공금액기준 제공 기준금액 |
| include_regional_shipping_rate | 지역별배송비 포함여부   T : 포함 F : 미포함 |
| shipments_start_date최소값: [1]최대값: [30] | 배송시작일 설정 |
| change_option | 옵션 변경 가능 여부   T : 사용함 F : 사용안함 |

```bash
Update subscription products        Update subscription products       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/subscription/shipments/setting/72' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "subscription_shipments_name": "SHIRTS SUBSCRIPTION SHIPMENTS MODIFY",        "product_binding_type": "P",        "one_time_purchase": "T",        "product_list": [            11,            13        ],        "use_discount": "T",        "discount_value_unit": "P",        "discount_values": [            {                "delivery_cycle": 1,                "discount_amount": 10            },            {                "delivery_cycle": 5,                "discount_amount": 20            }        ],        "subscription_shipments_cycle_type": "T",        "subscription_shipments_cycle": [            "3M",            "5M"        ],        "subscription_shipments_count_type": "T",        "subscription_shipments_count": [            4,            6,            8,            10        ],        "use_order_price_condition": "T",        "order_price_greater_than": "30000.00",        "include_regional_shipping_rate": "F",        "shipments_start_date": 3,        "change_option": "F"    }}'    Response  Copy     {    "shipment": {        "shop_no": 1,        "subscription_no": 72,        "subscription_shipments_name": "SHIRTS SUBSCRIPTION SHIPMENTS MODIFY",        "product_binding_type": "P",        "one_time_purchase": "T",        "product_list": [            11,            13        ],        "use_discount": "T",        "discount_value_unit": "P",        "discount_values": [            {                "delivery_cycle": 1,                "discount_amount": 10            },            {                "delivery_cycle": 5,                "discount_amount": 20            }        ],        "subscription_shipments_cycle_type": "T",        "subscription_shipments_cycle": [            "3M",            "5M"        ],        "subscription_shipments_count_type": "T",        "subscription_shipments_count": [            4,            6,            8,            10        ],        "use_order_price_condition": "T",        "order_price_greater_than": "30000.00",        "include_regional_shipping_rate": "F",        "shipments_start_date": 3,        "change_option": "F"    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/subscription/shipments/setting/72' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "subscription_shipments_name": "SHIRTS SUBSCRIPTION SHIPMENTS MODIFY",        "product_binding_type": "P",        "one_time_purchase": "T",        "product_list": [            11,            13        ],        "use_discount": "T",        "discount_value_unit": "P",        "discount_values": [            {                "delivery_cycle": 1,                "discount_amount": 10            },            {                "delivery_cycle": 5,                "discount_amount": 20            }        ],        "subscription_shipments_cycle_type": "T",        "subscription_shipments_cycle": [            "3M",            "5M"        ],        "subscription_shipments_count_type": "T",        "subscription_shipments_count": [            4,            6,            8,            10        ],        "use_order_price_condition": "T",        "order_price_greater_than": "30000.00",        "include_regional_shipping_rate": "F",        "shipments_start_date": 3,        "change_option": "F"    }}'
```

```json
{    "shipment": {        "shop_no": 1,        "subscription_no": 72,        "subscription_shipments_name": "SHIRTS SUBSCRIPTION SHIPMENTS MODIFY",        "product_binding_type": "P",        "one_time_purchase": "T",        "product_list": [            11,            13        ],        "use_discount": "T",        "discount_value_unit": "P",        "discount_values": [            {                "delivery_cycle": 1,                "discount_amount": 10            },            {                "delivery_cycle": 5,                "discount_amount": 20            }        ],        "subscription_shipments_cycle_type": "T",        "subscription_shipments_cycle": [            "3M",            "5M"        ],        "subscription_shipments_count_type": "T",        "subscription_shipments_count": [            4,            6,            8,            10        ],        "use_order_price_condition": "T",        "order_price_greater_than": "30000.00",        "include_regional_shipping_rate": "F",        "shipments_start_date": 3,        "change_option": "F"    }}
```

### Delete subscription products   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 쓰기권한 (mall.write_store) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| subscription_noRequired | 정기배송 상품설정 번호 |

```bash
Delete subscription products        Delete subscription products       Request   cURL Java Python Node.js PHP Go  Copy     curl -X DELETE \  'https://{mallid}.cafe24api.com/api/v2/admin/subscription/shipments/setting/15' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "shipment": {        "shop_no": 1,        "subscription_no": 15    }}
```

```bash
curl -X DELETE \  'https://{mallid}.cafe24api.com/api/v2/admin/subscription/shipments/setting/15' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "shipment": {        "shop_no": 1,        "subscription_no": 15    }}
```
