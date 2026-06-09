# CUSTOMERGROUPS


## Customergroups

```json
Endpoints    GET /api/v2/admin/customergroups
GET /api/v2/admin/customergroups/count
GET /api/v2/admin/customergroups/{group_no}
```

```json
GET /api/v2/admin/customergroups
GET /api/v2/admin/customergroups/count
GET /api/v2/admin/customergroups/{group_no}
```

### Customergroups property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| group_no | 회원등급번호 |
| group_name | 회원등급명 |
| group_description | 회원 등급설명 |
| group_icon | 회원등급 아이콘 |
| benefits_paymethod | 혜택 결제조건 A : 모든 결제 B : 현금 결제(무통장) C : 현금 결제 외 모든 결제 |
| buy_benefits | 구매시 할인/적립 혜택 F : 혜택없음 D : 구매금액 할인 M : 적립금 지급 P : 할인/적립 동시 적용 |
| ship_benefits | 배송비 혜택 T : 배송비무료설정 F : 배송비무료설정안함 |
| product_availability | 상품별 할인 중복설정 P : 상품별 가격할인만 적용 M : 회원등급별 가격할인만 적용 A : 둘다적용 |
| discount_information | 구매금액 할인설정 |
| points_information | 적립금 지급설정 |
| mobile_discount_information | 모바일 추가 할인설정 |
| mobile_points_information | 모바일 추가 적립금설정 |
| discount_limit_information | 할인 제한설정 멀티쇼핑몰에서 등급별 할인 혜택 제한 사용 시 등급 별로 적용되는 할인 혜택 제한 설정 및 최대 할인 한도 정보.  멀티쇼핑몰에서 등급별 할인 혜택 제한을 사용하지 않거나, buy_benefits(구매 시 할인/적립 혜택)이 F(혜택없음) 또는 M(적립금 지급)일 경우 null로 반환  discount_limit_type(할인 혜택 제한 설정)  - A : 제한없음 - B : 할인금액 제한 - C : 할인횟수 제한 discount_amount_limit(최대 할인금액 한도) : discount_limit_type이 B가 아닐 경우 null number_of_discount_limit(최대 할인횟수 한도) : discount_limit_type이 C가 아닐 경우 null로 반환. |

### Retrieve a list of customer tiers   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 회원 읽기권한 (mall.read_customer) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| group_no | 회원등급번호   ,(콤마)로 여러 건을 검색할 수 있다. |
| group_name최대글자수 : [20자] | 회원등급명   ,(콤마)로 여러 건을 검색할 수 있다. |

```bash
Retrieve a list of customer tiers        Retrieve a list of customer tiers Retrieve customergroups with fields parameter Retrieve a specific customergroups with group_no parameter Retrieve multiple customergroups       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/customergroups' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "customergroups": [        {            "shop_no": 1,            "group_no": 1,            "group_name": "Standard Membership",            "group_description": "Group information",            "group_icon": "https://{domain}/web/bbs_member_icon/member/1457000663.png",            "benefits_paymethod": "A",            "buy_benefits": "D",            "ship_benefits": "F",            "product_availability": "A",            "discount_information": {                "amount_product": "100000.00",                "amount_discount": "100.00",                "discount_unit": "P",                "truncation_unit": "10",                "max_discount": "10.00"            },            "points_information": {                "amount_product": "100000.00",                "amount_discount": "20.00",                "discount_unit": "P",                "truncation_unit": "100",                "max_discount": "100.00"            },            "mobile_discount_information": {                "amount_product": "100000.00",                "amount_discount": "20.00",                "discount_unit": "P",                "truncation_unit": "100",                "max_discount": "100.00"            },            "mobile_points_information": {                "amount_product": "100000.00",                "amount_discount": "20.00",                "discount_unit": "P",                "truncation_unit": "100",                "max_discount": "100.00"            },            "discount_limit_information": {                "discount_limit_type": "B",                "discount_amount_limit": "100000.00",                "number_of_discount_limit": null            }        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/customergroups' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "customergroups": [        {            "shop_no": 1,            "group_no": 1,            "group_name": "Standard Membership",            "group_description": "Group information",            "group_icon": "https://{domain}/web/bbs_member_icon/member/1457000663.png",            "benefits_paymethod": "A",            "buy_benefits": "D",            "ship_benefits": "F",            "product_availability": "A",            "discount_information": {                "amount_product": "100000.00",                "amount_discount": "100.00",                "discount_unit": "P",                "truncation_unit": "10",                "max_discount": "10.00"            },            "points_information": {                "amount_product": "100000.00",                "amount_discount": "20.00",                "discount_unit": "P",                "truncation_unit": "100",                "max_discount": "100.00"            },            "mobile_discount_information": {                "amount_product": "100000.00",                "amount_discount": "20.00",                "discount_unit": "P",                "truncation_unit": "100",                "max_discount": "100.00"            },            "mobile_points_information": {                "amount_product": "100000.00",                "amount_discount": "20.00",                "discount_unit": "P",                "truncation_unit": "100",                "max_discount": "100.00"            },            "discount_limit_information": {                "discount_limit_type": "B",                "discount_amount_limit": "100000.00",                "number_of_discount_limit": null            }        }    ]}
```

### Retrieve a count of customer tiers   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 회원 읽기권한 (mall.read_customer) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호.   DEFAULT 1 |
| group_no | 회원등급번호   시스템이 회원등급에 부여한 번호.   ,(콤마)로 여러 건을 검색할 수 있다. |
| group_name최대글자수 : [20자] | 회원등급명   회원등급을 만들 당시 지정한 회원등급의 이름.   ,(콤마)로 여러 건을 검색할 수 있다. |

```bash
Retrieve a count of customer tiers        Retrieve a count of customer tiers       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/customergroups/count' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "count": 1}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/customergroups/count' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "count": 1}
```

### Retrieve a customer tier   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 회원 읽기권한 (mall.read_customer) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호.   DEFAULT 1 |
| group_noRequired | 회원등급번호   시스템이 회원등급에 부여한 번호. |

```bash
Retrieve a customer tier        Retrieve a customer tier Retrieve a customergroup with fields parameter       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/customergroups/1' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "customergroup": {        "shop_no": 1,        "group_no": 1,        "group_name": "Standard Membership",        "group_description": "Group information",        "group_icon": "https://{domain}/web/bbs_member_icon/member/1457000663.png",        "benefits_paymethod": "A",        "buy_benefits": "D",        "ship_benefits": "F",        "product_availability": "A",        "discount_information": {            "amount_product": "100000.00",            "amount_discount": "100.00",            "discount_unit": "P",            "truncation_unit": "10",            "max_discount": "10.00"        },        "points_information": {            "amount_product": "100000.00",            "amount_discount": "20.00",            "discount_unit": "P",            "truncation_unit": "100",            "max_discount": "100.00"        },        "mobile_discount_information": {            "amount_product": "100000.00",            "amount_discount": "20.00",            "discount_unit": "P",            "truncation_unit": "100",            "max_discount": "100.00"        },        "mobile_points_information": {            "amount_product": "100000.00",            "amount_discount": "20.00",            "discount_unit": "P",            "truncation_unit": "100",            "max_discount": "100.00"        },        "discount_limit_information": {            "discount_limit_type": "B",            "discount_amount_limit": "100000.00",            "number_of_discount_limit": null        }    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/customergroups/1' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "customergroup": {        "shop_no": 1,        "group_no": 1,        "group_name": "Standard Membership",        "group_description": "Group information",        "group_icon": "https://{domain}/web/bbs_member_icon/member/1457000663.png",        "benefits_paymethod": "A",        "buy_benefits": "D",        "ship_benefits": "F",        "product_availability": "A",        "discount_information": {            "amount_product": "100000.00",            "amount_discount": "100.00",            "discount_unit": "P",            "truncation_unit": "10",            "max_discount": "10.00"        },        "points_information": {            "amount_product": "100000.00",            "amount_discount": "20.00",            "discount_unit": "P",            "truncation_unit": "100",            "max_discount": "100.00"        },        "mobile_discount_information": {            "amount_product": "100000.00",            "amount_discount": "20.00",            "discount_unit": "P",            "truncation_unit": "100",            "max_discount": "100.00"        },        "mobile_points_information": {            "amount_product": "100000.00",            "amount_discount": "20.00",            "discount_unit": "P",            "truncation_unit": "100",            "max_discount": "100.00"        },        "discount_limit_information": {            "discount_limit_type": "B",            "discount_amount_limit": "100000.00",            "number_of_discount_limit": null        }    }}
```
