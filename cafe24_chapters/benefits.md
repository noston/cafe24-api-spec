# BENEFITS


## Benefits

```json
Endpoints    GET /api/v2/admin/benefits
GET /api/v2/admin/benefits/count
GET /api/v2/admin/benefits/{benefit_no}
POST /api/v2/admin/benefits
PUT /api/v2/admin/benefits/{benefit_no}
DELETE /api/v2/admin/benefits/{benefit_no}
```

```json
GET /api/v2/admin/benefits
GET /api/v2/admin/benefits/count
GET /api/v2/admin/benefits/{benefit_no}
POST /api/v2/admin/benefits
PUT /api/v2/admin/benefits/{benefit_no}
DELETE /api/v2/admin/benefits/{benefit_no}
```

### Benefits property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호 |
| benefit_no | 혜택번호 혜택이 생성된 경우 부여되는 고유 번호 |
| use_benefit | 진행여부 |
| benefit_name최대글자수 : [255자] | 혜택명 |
| benefit_division | 혜택 유형 해당 혜택의 유형으로, 할인과 증정으로 구분됨 |
| benefit_type | 혜택 상세유형 해당 혜택의 상세유형  할인 : 기간할인, 재구매할인, 대량구매할인, 회원할인, 신규상품할인, 배송비할인 증정 : 사은품증정, 1+N 이벤트 |
| use_benefit_period | 혜택 기간 설정 해당 혜택이 적용되는 기간을 설정했는지 여부 |
| benefit_start_date날짜 | 혜택 시작일 혜택이 적용되는 기간을 설정한 경우, 해당 혜택이 시작되는 일시 |
| benefit_end_date날짜 | 혜택 종료일 혜택이 적용되는 기간을 설정한 경우, 해당 혜택이 종료되는 일시 |
| platform_types | 혜택 사용범위 해당 혜택이 적용되는 범위 (PC, 모바일, 플러스앱) |
| use_group_binding | 참여대상 설정 해당 혜택이 적용되는 대상을 설정 (회원+비회원, 비회원, 회원) |
| customer_group_list | 회원 등급 참여대상을 회원으로 설정한 경우, 참여가 가능한 회원등급을 설정 |
| product_binding_type | 상품 범위 해당 혜택이 적용되는 상품의 범위  전체상품 : 전체 상품에 혜택 적용 특정상품 : 선택한 특정 상품에 대해서만 혜택 적용 제외상품 : 선택한 특정 상품에 대해서만 혜택 적용 제외 상품분류 : 선택한 상품 분류에 속한 상품에 대해서만 혜택 적용 |
| use_except_category | 상품분류 혜택제외 특정 상품분류에 대해 혜택 적용을 제외함 (각 유형별로 설정 가능여부가 다름)  기간할인 : 전체상품, 특정상품인 경우 설정 가능 신규상품할인 : 전체상품인 경우 설정 가능  그 외 할인 및 증정유형에서는 설정 불가 |
| available_coupon | 쿠폰 사용범위 쿠폰이 있는 경우, 쿠폰을 중복하여 사용할 수 있는지 여부 |
| icon_url | 아이콘 URL 혜택이 적용되는 상품명에 아이콘이 노출되도록 아이콘 등록 |
| created_date | 혜택 등록일 해당 혜택이 등록된 일시 |
| repurchase_sale | 재구매 할인 설정 혜택의 상세유형이 재구매 할인인 경우 그와 관련한 상세 설정 |
| bulk_purchase_sale | 대량구매 수량 설정 혜택의 상세유형이 대량구매 할인인 경우 그와 관련한 상세 설정 |
| member_sale | 회원 할인 설정 혜택의 상세유형이 회원 할인인 경우 그와 관련한 상세 설정 |
| period_sale | 기간 할인 설정 혜택의 상세유형이 기간 할인인 경우 그와 관련한 상세 설정 하위 요소가 입력되어야 정상적인 등록이 가능함 |
| new_product_sale | 신규상품할인 설정 혜택의 상세유형이 신규상품 할인인 경우 그와 관련한 상세 설정 하위 요소가 입력되어야 정상적인 등록이 가능함 |
| shipping_fee_sale | 배송비 할인 설정 혜택의 상세유형이 배송비 할인인 경우 그와 관련한 상세 설정 하위 요소가 입력되어야 정상적인 등록이 가능함 |
| gift | 사은품 설정 혜택의 상세유형이 사은품 증정인 경우 그와 관련한 상세 설정 하위 요소가 입력되어야 정상적인 등록이 가능함 |
| gift_product_bundle | 1+N 이벤트 설정 혜택의 상세유형이 1+N 이벤트인 경우 그와 관련한 상세 설정 하위 요소가 입력되어야 정상적인 등록이 가능함 |

### Retrieve a list of customer benefits   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 프로모션 읽기권한 (mall.read_promotion) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호   DEFAULT 1 |
| use_benefit | 진행여부   T : 진행함 F : 진행안함 |
| benefit_name | 혜택명 |
| benefit_type | 혜택 상세유형   해당 혜택의 상세유형   DP : 기간할인 DR : 재구매할인 DQ : 대량구매할인 DM : 회원할인 DN : 신규상품할인 DV : 배송비할인 PG : 사은품  PB : 1+N 이벤트 |
| period_type | 혜택 기간 타입   R : 혜택 등록일 S : 혜택 시작일 E : 혜택 종료일 |
| benefit_start_date날짜 | 검색 시작일 |
| benefit_end_date날짜 | 검색 종료일 |
| platform_types | 혜택 사용범위   ,(콤마)로 여러 건을 검색할 수 있다.   P : PC 쇼핑몰 M : 모바일쇼핑몰 A : 브랜드앱 |
| offset최대값: [8000] | 조회결과 시작위치   DEFAULT 0 |
| limit최소: [1]~최대: [100] | 조회결과 최대건수   DEFAULT 10 |

```bash
Retrieve a list of customer benefits        Retrieve a list of customer benefits Retrieve benefits with fields parameter Retrieve benefits using paging Retrieve a specific benefits with benefit_name parameter Retrieve multiple benefits       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/benefits' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "benefits": [        {            "shop_no": 1,            "benefit_no": 3,            "use_benefit": "T",            "benefit_name": "Group Sale",            "benefit_division": "P",            "benefit_type": "PG",            "use_benefit_period": "T",            "benefit_start_date": "2018-12-04T00:00:00+09:00",            "benefit_end_date": "2018-12-04T23:55:00+09:00",            "platform_types": [                "P",                "M"            ],            "use_group_binding": "M",            "customer_group_list": [                1,                8,                9            ],            "product_binding_type": "A",            "use_except_category": "T",            "icon_url": "https://{domain}/web/upload/benefit/benefit_shop1_4975395c0f0de82b254843.gif",            "available_coupon": "T",            "repurchase_sale": null,            "bulk_purchase_sale": null,            "member_sale": null        },        {            "shop_no": 1,            "benefit_no": 2,            "use_benefit": "T",            "benefit_name": "New Product Sale",            "benefit_division": "D",            "benefit_type": "DN",            "use_benefit_period": null,            "benefit_start_date": null,            "benefit_end_date": null,            "platform_types": [                "P",                "M"            ],            "use_group_binding": "N",            "customer_group_list": [],            "product_binding_type": "E",            "use_except_category": "F",            "icon_url": "https://{domain}/web/upload/benefit/benefit_shop1_8376295c0fcd29hb22h893.gif",            "available_coupon": "T",            "repurchase_sale": null,            "bulk_purchase_sale": null,            "member_sale": null        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/benefits' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "benefits": [        {            "shop_no": 1,            "benefit_no": 3,            "use_benefit": "T",            "benefit_name": "Group Sale",            "benefit_division": "P",            "benefit_type": "PG",            "use_benefit_period": "T",            "benefit_start_date": "2018-12-04T00:00:00+09:00",            "benefit_end_date": "2018-12-04T23:55:00+09:00",            "platform_types": [                "P",                "M"            ],            "use_group_binding": "M",            "customer_group_list": [                1,                8,                9            ],            "product_binding_type": "A",            "use_except_category": "T",            "icon_url": "https://{domain}/web/upload/benefit/benefit_shop1_4975395c0f0de82b254843.gif",            "available_coupon": "T",            "repurchase_sale": null,            "bulk_purchase_sale": null,            "member_sale": null        },        {            "shop_no": 1,            "benefit_no": 2,            "use_benefit": "T",            "benefit_name": "New Product Sale",            "benefit_division": "D",            "benefit_type": "DN",            "use_benefit_period": null,            "benefit_start_date": null,            "benefit_end_date": null,            "platform_types": [                "P",                "M"            ],            "use_group_binding": "N",            "customer_group_list": [],            "product_binding_type": "E",            "use_except_category": "F",            "icon_url": "https://{domain}/web/upload/benefit/benefit_shop1_8376295c0fcd29hb22h893.gif",            "available_coupon": "T",            "repurchase_sale": null,            "bulk_purchase_sale": null,            "member_sale": null        }    ]}
```

### Retrieve a count of customer benefits   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 프로모션 읽기권한 (mall.read_promotion) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호   DEFAULT 1 |
| use_benefit | 진행여부   T : 진행함 F : 진행안함 |
| benefit_name | 혜택명 |
| benefit_type | 혜택 상세유형   해당 혜택의 상세유형   DP : 기간할인 DR : 재구매할인 DQ : 대량구매할인 DM : 회원할인 DN : 신규상품할인 DV : 배송비할인 PG : 사은품  PB : 1+N 이벤트 |
| period_type | 혜택 기간 타입   R : 혜택 등록일 S : 혜택 시작일 E : 혜택 종료일 |
| benefit_start_date날짜 | 검색 시작일 |
| benefit_end_date날짜 | 검색 종료일 |
| platform_types | 혜택 사용범위   ,(콤마)로 여러 건을 검색할 수 있다.   P : PC 쇼핑몰 M : 모바일쇼핑몰 A : 브랜드앱 |

```bash
Retrieve a count of customer benefits        Retrieve a count of customer benefits       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/benefits/count' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "count": 3}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/benefits/count' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "count": 3}
```

### Retrieve a customer benefit   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 프로모션 읽기권한 (mall.read_promotion) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| benefit_noRequired | 혜택번호   혜택이 생성된 경우 부여되는 고유 번호 |

```bash
Retrieve a customer benefit        Retrieve a customer benefit Retrieve a benefit with fields parameter       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/benefits/3' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "benefit": {        "shop_no": 1,        "benefit_no": 3,        "use_benefit": "T",        "benefit_name": "Sample Benefit",        "benefit_division": "D",        "benefit_type": "DP",        "use_benefit_period": "T",        "benefit_start_date": "2019-01-01T12:00:00+09:00",        "benefit_end_date": "2019-01-31T12:00:00+09:00",        "platform_types": [            "P",            "M"        ],        "use_group_binding": "M",        "customer_group_list": [            8,            9        ],        "product_binding_type": "P",        "use_except_category": "T",        "available_coupon": "T",        "icon_url": "https://{domain}/web/upload/benefit/benefit_shop1_4975395c0f0de82b254843.gif",        "created_date": "2019-01-01T12:00:00+09:00",        "period_sale": {            "product_list": [                17,                25,                29            ],            "add_category_list": null,            "except_category_list": [                168,                175,                177            ],            "discount_purchasing_quantity": null,            "discount_value": "10.00",            "discount_value_unit": "P",            "discount_truncation_unit": "O",            "discount_truncation_method": "U"        },        "repurchase_sale": null,        "bulk_purchase_sale": null,        "member_sale": null,        "new_product_sale": null,        "shipping_fee_sale": null,        "gift": null,        "gift_product_bundle": null    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/benefits/3' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "benefit": {        "shop_no": 1,        "benefit_no": 3,        "use_benefit": "T",        "benefit_name": "Sample Benefit",        "benefit_division": "D",        "benefit_type": "DP",        "use_benefit_period": "T",        "benefit_start_date": "2019-01-01T12:00:00+09:00",        "benefit_end_date": "2019-01-31T12:00:00+09:00",        "platform_types": [            "P",            "M"        ],        "use_group_binding": "M",        "customer_group_list": [            8,            9        ],        "product_binding_type": "P",        "use_except_category": "T",        "available_coupon": "T",        "icon_url": "https://{domain}/web/upload/benefit/benefit_shop1_4975395c0f0de82b254843.gif",        "created_date": "2019-01-01T12:00:00+09:00",        "period_sale": {            "product_list": [                17,                25,                29            ],            "add_category_list": null,            "except_category_list": [                168,                175,                177            ],            "discount_purchasing_quantity": null,            "discount_value": "10.00",            "discount_value_unit": "P",            "discount_truncation_unit": "O",            "discount_truncation_method": "U"        },        "repurchase_sale": null,        "bulk_purchase_sale": null,        "member_sale": null,        "new_product_sale": null,        "shipping_fee_sale": null,        "gift": null,        "gift_product_bundle": null    }}
```

### Create a customer benefit   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 프로모션 쓰기권한 (mall.write_promotion) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호   DEFAULT 1 |
| shop_no | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호 |
| use_benefitRequired | 진행여부   T : 진행함 F : 진행안함 |
| benefit_nameRequired최대글자수 : [255자] | 혜택명 |
| benefit_divisionRequired | 혜택 유형   해당 혜택의 유형으로, 할인과 증정으로 구분됨   D : 할인 P : 증정 |
| benefit_typeRequired | 혜택 상세유형   해당 혜택의 상세유형   DP : 기간할인 DR : 재구매할인 DQ : 대량구매할인 DM : 회원할인 DN : 신규상품할인 DV : 배송비할인 PG : 사은품  PB : 1+N 이벤트 |
| use_benefit_period | 혜택 기간 설정   해당 혜택이 적용되는 기간을 설정할지 여부  사용함으로 설정하는 경우, 혜택 시작일과 종료일을 입력해야 함   T : 사용함 F : 사용안함 |
| benefit_start_date날짜 | 혜택 시작일   혜택이 적용되는 기간을 설정한 경우, 해당 혜택이 시작되는 일시 |
| benefit_end_date날짜 | 혜택 종료일   혜택이 적용되는 기간을 설정한 경우, 해당 혜택이 종료되는 일시 |
| platform_typesRequired | 혜택 사용범위   해당 혜택이 적용되는 범위   P : PC 쇼핑몰 M : 모바일쇼핑몰 A : 브랜드앱 |
| use_group_binding | 참여대상 설정   해당 혜택이 적용되는 대상을 설정   A : 회원 + 비회원 N : 비회원 M : 회원 |
| customer_group_list | 회원 등급   참여대상을 회원으로 설정한 경우, 참여가 가능한 회원등급을 설정 |
| product_binding_type | 상품 범위   해당 혜택이 적용되는 상품의 범위   A : 전체상품 P : 특정상품 E : 제외상품 C : 상품분류 |
| use_except_category | 상품분류 혜택제외   특정 상품분류에 대해 혜택 적용을 제외함 (각 유형별로 설정 가능여부가 다름)  기간할인 : 전체상품, 특정상품인 경우 설정 가능 신규상품할인 : 전체상품인 경우 설정 가능  그 외 할인 및 증정유형에서는 설정 불가   T : 사용함 F : 사용안함 |
| available_coupon | 쿠폰 사용범위   쿠폰이 있는 경우, 쿠폰을 중복하여 사용할 수 있는지 여부   T : 모든 쿠폰 사용가능 F : 모든 쿠폰 사용제한 |
| period_sale | 기간 할인 설정   혜택의 상세유형이 기간 할인인 경우 그와 관련한 상세 설정 하위 요소가 입력되어야 정상적인 등록이 가능함  할인 금액(discount_value_unit)이 비율(P)인 경우 할인 반올림 단위(discount_truncation_unit), 할인 단위 처리(discount_truncation_method) 필수 입력  할인 금액(discount_value_unit)이 금액(W)인 경우 discount_purchasing_quantity 필수 입력 |
| period_sale 하위 요소 보기     product_list상품 목록 add_category_list상품 분류 except_category_list제외 분류 discount_purchasing_quantity할인 구매수량T : 구매수량에 따라 F : 구매수량에 관계없이 discount_value할인 값 discount_value_unit할인 기준P : 비율 W : 금액 discount_truncation_unit할인 반올림 단위F : 절사안함 C : 0.01 B : 0.1 O : 1 T : 10 M : 100 H : 1000 discount_truncation_method할인 단위 처리L : 내림 U : 반올림 C : 올림 |
| repurchase_sale | 재구매 할인 설정   혜택의 상세유형이 재구매 할인인 경우 그와 관련한 상세 설정 |
| repurchase_sale 하위 요소 보기     product_list상품 목록 purchase_item_type구매 횟수 설정P : 상품 I : 품목 purchase_timesRequired구매횟수 제한 수량 discount_purchasing_quantity할인 구매수량T : 구매수량에 따라 F : 구매수량에 관계없이 discount_value할인 값 discount_value_unit할인 기준P : 비율 W : 금액 discount_truncation_unit할인 반올림 단위F : 절사안함 C : 0.01 B : 0.1 O : 1 T : 10 M : 100 H : 1000 discount_truncation_method할인 단위 처리L : 내림 U : 반올림 C : 올림 |
| bulk_purchase_sale | 대량구매 수량 설정   혜택의 상세유형이 대량구매 할인인 경우 그와 관련한 상세 설정 |
| bulk_purchase_sale 하위 요소 보기     product_list상품 목록 bulk_purchase_item_type대량구매 수량 설정P : 상품 I : 품목DEFAULT P bulk_purchase_begin_quantityRequired구매수량 제한 (n 이상) bulk_purchase_limit_quantityRequired구매수량 제한 (n 미만) discount_purchasing_quantity할인 구매수량T : 구매수량에 따라 F : 구매수량에 관계없이 discount_value할인 값 discount_value_unit할인 기준P : 비율 W : 금액 discount_truncation_unit할인 반올림 단위F : 절사안함 C : 0.01 B : 0.1 O : 1 T : 10 M : 100 H : 1000 discount_truncation_method할인 단위 처리L : 내림 U : 반올림 C : 올림 |
| member_sale | 회원 할인 설정   혜택의 상세유형이 회원 할인인 경우 그와 관련한 상세 설정 |
| member_sale 하위 요소 보기     product_list상품 목록 discount_purchasing_quantity할인 구매수량T : 구매수량에 따라 F : 구매수량에 관계없이 discount_value할인 값 discount_value_unit할인 기준P : 비율 W : 금액 discount_truncation_unit할인 반올림 단위F : 절사안함 C : 0.01 B : 0.1 O : 1 T : 10 M : 100 H : 1000 discount_truncation_method할인 단위 처리L : 내림 U : 반올림 C : 올림 |
| gift | 사은품 설정   혜택의 상세유형이 사은품 증정인 경우 그와 관련한 상세 설정 하위 요소가 입력되어야 정상적인 등록이 가능함 |
| gift 하위 요소 보기     product_list상품 목록 add_category_list상품 분류 offer_only_first첫 구매 여부T : 사용함 F : 사용안함 first_purchase_type첫 구매 기준O : 주문기준 D : 배송완료 기준 use_unlimited_price최대가격 제한여부T : 사용함 F : 사용안함 purchase_start_price구매가격 제한 (n 이상) purchase_limit_price구매가격 제한 (n 미만) gift_product_list Array    gift_product_list 하위 요소 보기     product_no상품번호Required gift_point차감 점수Required max_count최대 선택 수량 |
| new_product_sale | 신규상품할인 설정   혜택의 상세유형이 신규상품 할인인 경우 그와 관련한 상세 설정 하위 요소가 입력되어야 정상적인 등록이 가능함  할인 금액(discount_value_unit)이 비율(P)인 경우 할인 반올림 단위(discount_truncation_unit), 할인 단위 처리(discount_truncation_method) 필수 입력  할인 금액(discount_value_unit)이 금액(W)인 경우 discount_purchasing_quantity 필수 입력 |
| new_product_sale 하위 요소 보기     product_list상품 목록 add_category_list상품 분류 except_category_list제외 분류 new_product_date_typeRequired신상품 설정 기준일I : 상품 등록일 U : 상품 최종 수정일 V : 상품 최종 진열일 new_product_dayRequired신상품 설정 값 new_product_term_typeRequired신상품 설정 단위D : 일 H : 시간 discount_purchasing_quantity할인 구매수량T : 구매수량에 따라 F : 구매수량에 관계없이 discount_valueRequired할인 값 discount_value_unit할인 기준P : 비율 W : 금액 discount_truncation_unit할인 반올림 단위F : 절사안함 C : 0.01 B : 0.1 O : 1 T : 10 M : 100 H : 1000 discount_truncation_method할인 단위 처리L : 내림 U : 반올림 C : 올림 |
| shipping_fee_sale | 배송비 할인 설정   혜택의 상세유형이 배송비 할인인 경우 그와 관련한 상세 설정 하위 요소가 입력되어야 정상적인 등록이 가능함 |
| shipping_fee_sale 하위 요소 보기     product_list상품 목록 use_purchase_price_condition금액 기준 사용여부T : 사용함 F : 사용안함 total_purchase_price금액 제한 include_regional_shipping_rate지역별배송비 포함여부값T : 포함 F : 미포함 |
| gift_product_bundle | 1+N 이벤트 설정   혜택의 상세유형이 1+N 이벤트인 경우 그와 관련한 상세 설정 하위 요소가 입력되어야 정상적인 등록이 가능함 |
| gift_product_bundle 하위 요소 보기     product_list상품 목록 product_bundle_typeRequired혜택 설정P : 상품 I : 품목 product_bundle_countRequired추가 상품 수량 |
| icon_url | 아이콘 URL   혜택이 적용되는 상품명에 아이콘이 노출되도록 아이콘 등록 |

```bash
Create a customer benefit        Create a customer benefit Trying to create a promotion without benefit_type Create a promotion of period discount Create a promotion of new product discount Create a promotion of shipping fee discount Create a promotion of gift Create a promotion of 1+N gift       Request   cURL Java Python Node.js PHP Go  Copy     curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/benefits' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "use_benefit": "T",        "benefit_name": "Sample Benefit",        "benefit_division": "D",        "benefit_type": "DP",        "use_benefit_period": "T",        "benefit_start_date": "2019-01-01T12:00:00+09:00",        "benefit_end_date": "2019-01-31T12:00:00+09:00",        "platform_types": [            "P",            "M"        ],        "use_group_binding": "M",        "customer_group_list": [            8,            9        ],        "product_binding_type": "P",        "use_except_category": "T",        "available_coupon": "T",        "icon_url": "iVBORw0KGgoAAAANSUhEUgAAAAoAAAAKCAYAAACNMs+9AAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAAAJcEhZcwAADsMAAA7DAcdvqGQAAAAXSURBVChTY1BQdvhPDB5ViBdTW6HDfwA+dpbJG+7kLwAAAABJRU5ErkJggg==\\n",        "period_sale": {            "product_list": [                17,                25,                29            ],            "except_category_list": [                168,                175,                177            ],            "discount_value": "10.00",            "discount_value_unit": "P",            "discount_truncation_unit": "O",            "discount_truncation_method": "U"        }    }}'    Response  Copy     {    "benefit": {        "shop_no": 1,        "benefit_no": 3,        "use_benefit": "T",        "benefit_name": "Sample Benefit",        "benefit_division": "D",        "benefit_type": "DP",        "use_benefit_period": "T",        "benefit_start_date": "2019-01-01T12:00:00+09:00",        "benefit_end_date": "2019-01-31T12:00:00+09:00",        "platform_types": [            "P",            "M"        ],        "use_group_binding": "M",        "customer_group_list": [            8,            9        ],        "product_binding_type": "P",        "use_except_category": "T",        "available_coupon": "T",        "icon_url": "https://{domain}/web/upload/benefit/benefit_shop1_3648075d918c2c5ecae6.10781112.png",        "created_date": "2019-01-01T12:00:00+09:00",        "period_sale": {            "product_list": [                17,                25,                29            ],            "add_category_list": null,            "except_category_list": [                168,                175,                177            ],            "discount_purchasing_quantity": null,            "discount_value": "10.00",            "discount_value_unit": "P",            "discount_truncation_unit": "O",            "discount_truncation_method": "U"        },        "repurchase_sale": null,        "bulk_purchase_sale": null,        "member_sale": null,        "new_product_sale": null,        "shipping_fee_sale": null,        "gift": null,        "gift_product_bundle": null    }}
```

```bash
curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/benefits' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "use_benefit": "T",        "benefit_name": "Sample Benefit",        "benefit_division": "D",        "benefit_type": "DP",        "use_benefit_period": "T",        "benefit_start_date": "2019-01-01T12:00:00+09:00",        "benefit_end_date": "2019-01-31T12:00:00+09:00",        "platform_types": [            "P",            "M"        ],        "use_group_binding": "M",        "customer_group_list": [            8,            9        ],        "product_binding_type": "P",        "use_except_category": "T",        "available_coupon": "T",        "icon_url": "iVBORw0KGgoAAAANSUhEUgAAAAoAAAAKCAYAAACNMs+9AAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAAAJcEhZcwAADsMAAA7DAcdvqGQAAAAXSURBVChTY1BQdvhPDB5ViBdTW6HDfwA+dpbJG+7kLwAAAABJRU5ErkJggg==\\n",        "period_sale": {            "product_list": [                17,                25,                29            ],            "except_category_list": [                168,                175,                177            ],            "discount_value": "10.00",            "discount_value_unit": "P",            "discount_truncation_unit": "O",            "discount_truncation_method": "U"        }    }}'
```

```json
{    "benefit": {        "shop_no": 1,        "benefit_no": 3,        "use_benefit": "T",        "benefit_name": "Sample Benefit",        "benefit_division": "D",        "benefit_type": "DP",        "use_benefit_period": "T",        "benefit_start_date": "2019-01-01T12:00:00+09:00",        "benefit_end_date": "2019-01-31T12:00:00+09:00",        "platform_types": [            "P",            "M"        ],        "use_group_binding": "M",        "customer_group_list": [            8,            9        ],        "product_binding_type": "P",        "use_except_category": "T",        "available_coupon": "T",        "icon_url": "https://{domain}/web/upload/benefit/benefit_shop1_3648075d918c2c5ecae6.10781112.png",        "created_date": "2019-01-01T12:00:00+09:00",        "period_sale": {            "product_list": [                17,                25,                29            ],            "add_category_list": null,            "except_category_list": [                168,                175,                177            ],            "discount_purchasing_quantity": null,            "discount_value": "10.00",            "discount_value_unit": "P",            "discount_truncation_unit": "O",            "discount_truncation_method": "U"        },        "repurchase_sale": null,        "bulk_purchase_sale": null,        "member_sale": null,        "new_product_sale": null,        "shipping_fee_sale": null,        "gift": null,        "gift_product_bundle": null    }}
```

### Update a customer benefit   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 프로모션 쓰기권한 (mall.write_promotion) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호   DEFAULT 1 |
| benefit_noRequired | 혜택번호   혜택이 생성된 경우 부여되는 고유 번호 |
| use_benefit | 진행여부   T : 진행함 F : 진행안함 |
| benefit_name최대글자수 : [255자] | 혜택명 |
| use_benefit_period | 혜택 기간 설정   해당 혜택이 적용되는 기간을 설정할지 여부   T : 사용함 F : 사용안함 |
| benefit_start_date날짜 | 혜택 시작일   혜택이 적용되는 기간을 설정한 경우, 해당 혜택이 시작되는 일시  혜택 시작일을 수정하고자 하는 경우, use_benefit_period 파라미터를 반드시 선언해야 함 |
| benefit_end_date날짜 | 혜택 종료일   혜택이 적용되는 기간을 설정한 경우, 해당 혜택이 종료되는 일시  혜택 종료일을 수정하고자 하는 경우, use_benefit_period 파라미터를 반드시 선언해야 함 |
| platform_types | 혜택 사용범위   해당 혜택이 적용되는 범위   P : PC 쇼핑몰 M : 모바일쇼핑몰 A : 브랜드앱 |
| use_group_binding | 참여대상 설정   해당 혜택이 적용되는 대상을 설정   A : 회원 + 비회원 N : 비회원 M : 회원 |
| customer_group_list | 회원 등급   참여대상을 회원으로 설정한 경우, 참여가 가능한 회원등급을 설정  회원 등급을 수정하고자 하는 경우, use_group_binding 파라미터를 반드시 선언해야 함 |
| product_binding_type | 상품 범위   해당 혜택이 적용되는 상품의 범위  상품 범위가 P,E,C 인 경우 기존에 설정된 상품 또는 분류를 수정하고자 하는 경우 product_binding_type 파라미터를 반드시 선언해야 함   A : 전체상품 P : 특정상품 E : 제외상품 C : 상품분류 |
| use_except_category | 상품분류 혜택제외   특정 상품분류에 대해 혜택 적용을 제외함 (각 유형별로 설정 가능여부가 다름)  기간할인 : 전체상품, 특정상품인 경우 설정 가능 신규상품할인 : 전체상품인 경우 설정 가능  그 외 할인 및 증정유형에서는 설정 불가  기존에 설정된 제외 분류를 수정하고자 하는 경우, use_except_category 파라미터를 반드시 선언해야 함   T : 사용함 F : 사용안함 |
| available_coupon | 쿠폰 사용범위   쿠폰이 있는 경우, 쿠폰을 중복하여 사용할 수 있는지 여부   T : 모든 쿠폰 사용가능 F : 모든 쿠폰 사용제한 |
| period_sale | 기간 할인 설정   혜택의 상세유형이 기간 할인인 경우 그와 관련한 상세 설정 하위 요소가 입력되어야 정상적인 수정이 가능함  할인 금액(discount_value_unit)이 비율(P)인 경우 할인 반올림 단위(discount_truncation_unit), 할인 단위 처리(discount_truncation_method) 필수 입력  할인 금액(discount_value_unit)이 금액(W)인 경우 discount_purchasing_quantity 필수 입력 |
| period_sale 하위 요소 보기     product_list상품 목록 add_category_list상품 분류 except_category_list제외 분류 discount_purchasing_quantity할인 구매수량T : 구매수량에 따라 F : 구매수량에 관계없이 discount_value할인 값 discount_value_unit할인 기준P : 비율 W : 금액 discount_truncation_unit할인 반올림 단위F : 절사안함 C : 0.01 B : 0.1 O : 1 T : 10 M : 100 H : 1000 discount_truncation_method할인 단위 처리L : 내림 U : 반올림 C : 올림 |
| gift | 사은품 설정   혜택의 상세유형이 사은품 증정인 경우 그와 관련한 상세 설정 하위 요소가 입력되어야 정상적인 수정이 가능함 |
| gift 하위 요소 보기     product_list상품 목록 add_category_list상품 분류 offer_only_first첫 구매 여부T : 사용함 F : 사용안함 first_purchase_type첫 구매 기준O : 주문기준 D : 배송완료 기준 use_unlimited_price최대가격 제한여부T : 사용함 F : 사용안함 purchase_start_price구매가격 제한 (n 이상) purchase_limit_price구매가격 제한 (n 미만) gift_product_list Array    gift_product_list 하위 요소 보기     product_no상품번호 gift_point차감 점수 max_count최대 선택 수량 |
| gift_product_bundle | 1+N 이벤트 설정   혜택의 상세유형이 1+N 이벤트인 경우 그와 관련한 상세 설정 하위 요소가 입력되어야 정상적인 수정이 가능함 |
| gift_product_bundle 하위 요소 보기     product_list상품 목록 product_bundle_count추가 상품 수량 |
| new_product_sale | 신규상품할인 설정   혜택의 상세유형이 신규상품 할인인 경우 그와 관련한 상세 설정 하위 요소가 입력되어야 정상적인 수정이 가능함  할인 금액(discount_value_unit)이 비율(P)인 경우 할인 반올림 단위(discount_truncation_unit), 할인 단위 처리(discount_truncation_method) 필수 입력  할인 금액(discount_value_unit)이 금액(W)인 경우 discount_purchasing_quantity 필수 입력 |
| new_product_sale 하위 요소 보기     product_list상품 목록 add_category_list상품 분류 except_category_list제외 분류 new_product_date_type신상품 설정 기준일I : 상품 등록일 U : 상품 최종 수정일 V : 상품 최종 진열일 new_product_day신상품 설정 값 new_product_term_type신상품 설정 단위D : 일 H : 시간 discount_purchasing_quantity할인 구매수량T : 구매수량에 따라 F : 구매수량에 관계없이 discount_value할인 값 discount_value_unit할인 기준P : 비율 W : 금액 discount_truncation_unit할인 반올림 단위F : 절사안함 C : 0.01 B : 0.1 O : 1 T : 10 M : 100 H : 1000 discount_truncation_method할인 단위 처리L : 내림 U : 반올림 C : 올림 |
| shipping_fee_sale | 배송비 할인 설정   혜택의 상세유형이 배송비 할인인 경우 그와 관련한 상세 설정 하위 요소가 입력되어야 정상적인 수정이 가능함 |
| shipping_fee_sale 하위 요소 보기     product_list상품 목록 use_purchase_price_condition금액 기준 사용여부T : 사용함 F : 사용안함 total_purchase_price금액 제한 include_regional_shipping_rate지역별배송비 포함여부값T : 포함 F : 미포함 |
| icon_url | 아이콘 URL   혜택이 적용되는 상품명에 아이콘이 노출되도록 아이콘 등록 (빈 값으로 요청 시, 기존에 등록된 아이콘 삭제됨) |

```bash
Update a customer benefit        Update a customer benefit Update target participants of benefits to member only Update discount rates of the benefits to 15%       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/benefits/3' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "use_benefit": "T",        "benefit_name": "Sample Benefit",        "use_benefit_period": "T",        "benefit_start_date": "2019-01-01T12:00:00+09:00",        "benefit_end_date": "2019-01-31T12:00:00+09:00",        "platform_types": [            "P",            "M"        ],        "use_group_binding": "M",        "customer_group_list": [            8,            9        ],        "product_binding_type": "P",        "use_except_category": "T",        "available_coupon": "T",        "icon_url": "iVBORw0KGgoAAAANSUhEUgAAAAoAAAAKCAYAAACNMs+9AAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAAAJcEhZcwAADsMAAA7DAcdvqGQAAAAXSURBVChTY1BQdvhPDB5ViBdTW6HDfwA+dpbJG+7kLwAAAABJRU5ErkJggg==\\n",        "period_sale": {            "product_list": [                17,                25,                29            ],            "except_category_list": [                168,                175,                177            ],            "discount_value": "10.00",            "discount_value_unit": "P",            "discount_truncation_unit": "O",            "discount_truncation_method": "U"        }    }}'    Response  Copy     {    "benefit": {        "shop_no": 1,        "benefit_no": 3,        "use_benefit": "T",        "benefit_name": "Sample Benefit",        "benefit_division": "D",        "benefit_type": "DP",        "use_benefit_period": "T",        "benefit_start_date": "2019-01-01T12:00:00+09:00",        "benefit_end_date": "2019-01-31T12:00:00+09:00",        "platform_types": [            "P",            "M"        ],        "use_group_binding": "M",        "customer_group_list": [            8,            9        ],        "product_binding_type": "P",        "use_except_category": "T",        "available_coupon": "T",        "icon_url": "https://{domain}/web/upload/benefit/benefit_shop1_3648075d918c2c5ecae6.10781112.png",        "created_date": "2019-01-01T12:00:00+09:00",        "period_sale": {            "product_list": [                17,                25,                29            ],            "add_category_list": null,            "except_category_list": [                168,                175,                177            ],            "discount_purchasing_quantity": null,            "discount_value": "10.00",            "discount_value_unit": "P",            "discount_truncation_unit": "O",            "discount_truncation_method": "U"        },        "repurchase_sale": null,        "bulk_purchase_sale": null,        "member_sale": null,        "new_product_sale": null,        "shipping_fee_sale": null,        "gift": null,        "gift_product_bundle": null    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/benefits/3' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "use_benefit": "T",        "benefit_name": "Sample Benefit",        "use_benefit_period": "T",        "benefit_start_date": "2019-01-01T12:00:00+09:00",        "benefit_end_date": "2019-01-31T12:00:00+09:00",        "platform_types": [            "P",            "M"        ],        "use_group_binding": "M",        "customer_group_list": [            8,            9        ],        "product_binding_type": "P",        "use_except_category": "T",        "available_coupon": "T",        "icon_url": "iVBORw0KGgoAAAANSUhEUgAAAAoAAAAKCAYAAACNMs+9AAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAAAJcEhZcwAADsMAAA7DAcdvqGQAAAAXSURBVChTY1BQdvhPDB5ViBdTW6HDfwA+dpbJG+7kLwAAAABJRU5ErkJggg==\\n",        "period_sale": {            "product_list": [                17,                25,                29            ],            "except_category_list": [                168,                175,                177            ],            "discount_value": "10.00",            "discount_value_unit": "P",            "discount_truncation_unit": "O",            "discount_truncation_method": "U"        }    }}'
```

```json
{    "benefit": {        "shop_no": 1,        "benefit_no": 3,        "use_benefit": "T",        "benefit_name": "Sample Benefit",        "benefit_division": "D",        "benefit_type": "DP",        "use_benefit_period": "T",        "benefit_start_date": "2019-01-01T12:00:00+09:00",        "benefit_end_date": "2019-01-31T12:00:00+09:00",        "platform_types": [            "P",            "M"        ],        "use_group_binding": "M",        "customer_group_list": [            8,            9        ],        "product_binding_type": "P",        "use_except_category": "T",        "available_coupon": "T",        "icon_url": "https://{domain}/web/upload/benefit/benefit_shop1_3648075d918c2c5ecae6.10781112.png",        "created_date": "2019-01-01T12:00:00+09:00",        "period_sale": {            "product_list": [                17,                25,                29            ],            "add_category_list": null,            "except_category_list": [                168,                175,                177            ],            "discount_purchasing_quantity": null,            "discount_value": "10.00",            "discount_value_unit": "P",            "discount_truncation_unit": "O",            "discount_truncation_method": "U"        },        "repurchase_sale": null,        "bulk_purchase_sale": null,        "member_sale": null,        "new_product_sale": null,        "shipping_fee_sale": null,        "gift": null,        "gift_product_bundle": null    }}
```

### Delete a customer benefit   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 프로모션 쓰기권한 (mall.write_promotion) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호   DEFAULT 1 |
| benefit_noRequired | 혜택번호   혜택이 생성된 경우 부여되는 고유 번호 |

```bash
Delete a customer benefit        Delete a customer benefit       Request   cURL Java Python Node.js PHP Go  Copy     curl -X DELETE \  'https://{mallid}.cafe24api.com/api/v2/admin/benefits/3' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "benefit": {        "shop_no": 1,        "benefit_no": 3    }}
```

```bash
curl -X DELETE \  'https://{mallid}.cafe24api.com/api/v2/admin/benefits/3' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "benefit": {        "shop_no": 1,        "benefit_no": 3    }}
```
