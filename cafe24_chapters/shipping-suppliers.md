# SHIPPING SUPPLIERS


## Shipping suppliers

```json
Endpoints    GET /api/v2/admin/shipping/suppliers/{supplier_id}
PUT /api/v2/admin/shipping/suppliers/{supplier_id}
```

```json
GET /api/v2/admin/shipping/suppliers/{supplier_id}
PUT /api/v2/admin/shipping/suppliers/{supplier_id}
```

### Shipping suppliers property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| supplier_id | 공급사 아이디 |
| supplier_code | 공급사 코드 |
| shipping_method | 배송방법 shipping_01 : 택배 shipping_02 : 빠른등기 shipping_04 : 직접배송 shipping_05 : 퀵배송 shipping_06 : 기타 shipping_07 : 화물배송 shipping_08 : 매장직접수령 shipping_09 : 배송필요 없음 |
| shipping_etc최대글자수 : [25자] | 기타배송 배송방법(shipping_method)이 shipping_06(기타) 일 때 기타 배송 정보 |
| shipping_type | 국내/해외배송 설정 A : 국내배송 C : 해외배송 B : 국내/해외배송 |
| shipping_place최대글자수 : [127자] | 배송지역 |
| shipping_start_date최소값: [1]최대값: [100] | 배송기간 시작일 |
| shipping_end_date최소값: [1]최대값: [100] | 배송기간 종료일 |
| shipping_fee_type | 배송비타입 T : 배송비 무료 R : 고정배송비 사용 M : 구매 금액에 따른 부과 D : 구매 금액별 차등 배송료 사용 W : 상품 무게별 차등 배송료 사용 C : 상품 수량별 차등 배송료 사용 N : 상품 수량에 비례하여 배송료 부과 |
| free_shipping_price최소값: [0]최대값: [999999999] | 배송비 무료 최소금액 배송비타입(shipping_fee_type)이 "M(구매 금엑에 따른 부과)" 일 때 배송비를 무료로 만들기 위한 기준 금액 |
| shipping_fee최소값: [0]최대값: [999999999] | 배송비 배송비타입(shipping_fee_type)이 "R(고정배송비 사용)"이거나 "M(구매 금액에 따른 부과)"일 때 배송비 금액 |
| shipping_fee_by_quantity최소값: [0]최대값: [999999999] | 상품 수량별 배송비 배송비타입(shipping_fee_type)이 "N(상품 수량에 비례하여 배송료 부과)"일 때 수량별 배송비 금액 |
| shipping_rates배열 최대사이즈: [50] | 배송비 상세 설정 |
| prepaid_shipping_fee | 배송비 선결제 설정 C : 착불 P : 선결제 B : 착불/선결제 |
| shipping_fee_by_product | 상품별 개별 배송료 설정 T : 사용함 F : 사용안함 |
| product_weight최소값: [0]최대값: [30] | 상품중량 |
| hscode최대글자수 : [20자] | HS코드 |
| country_hscode배열 최대사이즈: [50] | 국가별 HS 코드 |
| oversea_shipping_country | 해외배송가능 국가 제한 여부 T : 제한함 F : 제한안함 |
| oversea_shipping_country_list | 배송국가 |

### Retrieve a supplier's shipping settings   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 공급사 정보 읽기권한 (mall.read_supply) |
| 호출건수 제한 | 30 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| supplier_idRequired | 공급사 아이디 |

```bash
Retrieve a supplier's shipping settings        Retrieve a supplier's shipping settings Retrieve a shipping supplier with fields parameter       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/shipping/suppliers/sampleid' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "supplier": {        "shop_no": 1,        "supplier_id": "sampleid",        "supplier_code": "S000000A",        "shipping_method": "shipping_01",        "shipping_etc": null,        "shipping_type": "B",        "shipping_place": "A Region.",        "shipping_start_date": 3,        "shipping_end_date": 7,        "shipping_fee_type": "C",        "free_shipping_price": null,        "shipping_fee": null,        "shipping_fee_by_quantity": null,        "shipping_rates": [            {                "shipping_rates_min": "0.00",                "shipping_rates_max": "30000.00",                "shipping_fee": "3000.00"            },            {                "shipping_rates_min": "30000.00",                "shipping_rates_max": "50000.00",                "shipping_fee": "2500.00"            }        ],        "prepaid_shipping_fee": "P",        "shipping_fee_by_product": "T",        "product_weight": "1.00",        "hscode": "0101211000",        "country_hscode": [            {                "country_code": "JPN",                "hscode": "010121100"            },            {                "country_code": "CHN",                "hscode": "01022100"            }        ],        "oversea_shipping_country": "T",        "oversea_shipping_country_list": [            {                "country_code": "US"            },            {                "country_code": "JPN"            }        ]    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/shipping/suppliers/sampleid' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "supplier": {        "shop_no": 1,        "supplier_id": "sampleid",        "supplier_code": "S000000A",        "shipping_method": "shipping_01",        "shipping_etc": null,        "shipping_type": "B",        "shipping_place": "A Region.",        "shipping_start_date": 3,        "shipping_end_date": 7,        "shipping_fee_type": "C",        "free_shipping_price": null,        "shipping_fee": null,        "shipping_fee_by_quantity": null,        "shipping_rates": [            {                "shipping_rates_min": "0.00",                "shipping_rates_max": "30000.00",                "shipping_fee": "3000.00"            },            {                "shipping_rates_min": "30000.00",                "shipping_rates_max": "50000.00",                "shipping_fee": "2500.00"            }        ],        "prepaid_shipping_fee": "P",        "shipping_fee_by_product": "T",        "product_weight": "1.00",        "hscode": "0101211000",        "country_hscode": [            {                "country_code": "JPN",                "hscode": "010121100"            },            {                "country_code": "CHN",                "hscode": "01022100"            }        ],        "oversea_shipping_country": "T",        "oversea_shipping_country_list": [            {                "country_code": "US"            },            {                "country_code": "JPN"            }        ]    }}
```

### Update a supplier's shipping settings   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 공급사 정보 쓰기권한 (mall.write_supply) |
| 호출건수 제한 | 30 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| supplier_idRequired | 공급사 아이디 |
| shipping_method | 배송방법   shipping_01 : 택배 shipping_02 : 빠른등기 shipping_04 : 직접배송 shipping_05 : 퀵배송 shipping_06 : 기타 shipping_07 : 화물배송 shipping_08 : 매장직접수령 shipping_09 : 배송필요 없음 |
| shipping_etc최대글자수 : [25자] | 기타배송   배송방법(shipping_method)이 shipping_06(기타) 일 때 기타 배송 정보 |
| shipping_type | 국내/해외배송 설정   EC 베트남, 필리핀 버전에서는 사용할 수 없음.   A : 국내배송 C : 해외배송 B : 국내/해외배송 |
| shipping_place최대글자수 : [127자] | 배송지역 |
| shipping_start_date최소값: [1]최대값: [100] | 배송기간 시작일 |
| shipping_end_date최소값: [1]최대값: [100] | 배송기간 종료일 |
| shipping_fee_type | 배송비타입   T : 배송비 무료 R : 고정배송비 사용 M : 구매 금액에 따른 부과 D : 구매 금액별 차등 배송료 사용 W : 상품 무게별 차등 배송료 사용 C : 상품 수량별 차등 배송료 사용 N : 상품 수량에 비례하여 배송료 부과 |
| free_shipping_price최소값: [0]최대값: [999999999] | 배송비 무료 최소금액   배송비타입(shipping_fee_type)이 "M(구매 금엑에 따른 부과)" 일 때 배송비를 무료로 만들기 위한 기준 금액 |
| shipping_fee최소값: [0]최대값: [999999999] | 배송비   배송비타입(shipping_fee_type)이 "R(고정배송비 사용)"이거나 "M(구매 금액에 따른 부과)"일 때 배송비 금액 |
| shipping_fee_by_quantity최소값: [0]최대값: [999999999] | 상품 수량별 배송비   배송비타입(shipping_fee_type)이 "N(상품 수량에 비례하여 배송료 부과)"일 때 수량별 배송비 금액 |
| shipping_rates배열 최대사이즈: [50] | 배송비 상세 설정 |
| shipping_rates 하위 요소 보기     shipping_rates_min배송비 - 배송비 부과 기준 하한값 shipping_rates_max배송비 - 배송비 부과 기준 상한값 shipping_fee배송비 |
| prepaid_shipping_fee | 배송비 선결제 설정   EC 베트남, 필리핀 버전에서는 사용할 수 없음.   C : 착불 P : 선결제 B : 착불/선결제 |
| shipping_fee_by_product | 상품별 개별 배송료 설정   T : 사용함 F : 사용안함 |
| product_weight최소값: [0]최대값: [30] | 상품중량 |
| hscode최대글자수 : [20자] | HS코드 |
| country_hscode배열 최대사이즈: [24] | 국가별 HS 코드 |
| country_hscode 하위 요소 보기     country_code국가코드 hscodeHS코드 |

```bash
Update a supplier's shipping settings        Update a supplier's shipping settings Update international shipping setting for the supplier Update shipping rates to charge according to purchase amount(free shipping if you buy above 10000) Update shipping rates to charge per purchase amount Update shipping rates to charge by product weight Update shipping rates to charge per purchase quantity Update shipping rates to charge per quantity       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/shipping/suppliers/sampleid' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "shipping_method": "shipping_01",        "shipping_type": "B",        "shipping_place": "A Region.",        "shipping_start_date": 3,        "shipping_end_date": 7,        "shipping_fee_type": "D",        "shipping_rates": [            {                "shipping_rates_min": "0.00",                "shipping_rates_max": "30000.00",                "shipping_fee": "3000.00"            },            {                "shipping_rates_min": "30000.00",                "shipping_rates_max": "50000.00",                "shipping_fee": "2500.00"            }        ],        "prepaid_shipping_fee": "P",        "shipping_fee_by_product": "T",        "product_weight": "1.00",        "hscode": "0101211000",        "country_hscode": [            {                "country_code": "JPN",                "hscode": "010121100"            },            {                "country_code": "CHN",                "hscode": "01022100"            }        ]    }}'    Response  Copy     {    "supplier": {        "shop_no": 1,        "supplier_id": "sampleid",        "supplier_code": "S000000A",        "shipping_method": "shipping_01",        "shipping_etc": null,        "shipping_type": "B",        "shipping_place": "A Region.",        "shipping_start_date": 3,        "shipping_end_date": 7,        "shipping_fee_type": "D",        "free_shipping_price": null,        "shipping_fee": null,        "shipping_fee_by_quantity": null,        "shipping_rates": [            {                "shipping_rates_min": "0.00",                "shipping_rates_max": "30000.00",                "shipping_fee": "3000.00"            },            {                "shipping_rates_min": "30000.00",                "shipping_rates_max": "50000.00",                "shipping_fee": "2500.00"            }        ],        "prepaid_shipping_fee": "P",        "shipping_fee_by_product": "T",        "product_weight": "1.00",        "hscode": "0101211000",        "country_hscode": [            {                "country_code": "JPN",                "hscode": "010121100"            },            {                "country_code": "CHN",                "hscode": "01022100"            }        ]    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/shipping/suppliers/sampleid' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "shipping_method": "shipping_01",        "shipping_type": "B",        "shipping_place": "A Region.",        "shipping_start_date": 3,        "shipping_end_date": 7,        "shipping_fee_type": "D",        "shipping_rates": [            {                "shipping_rates_min": "0.00",                "shipping_rates_max": "30000.00",                "shipping_fee": "3000.00"            },            {                "shipping_rates_min": "30000.00",                "shipping_rates_max": "50000.00",                "shipping_fee": "2500.00"            }        ],        "prepaid_shipping_fee": "P",        "shipping_fee_by_product": "T",        "product_weight": "1.00",        "hscode": "0101211000",        "country_hscode": [            {                "country_code": "JPN",                "hscode": "010121100"            },            {                "country_code": "CHN",                "hscode": "01022100"            }        ]    }}'
```

```json
{    "supplier": {        "shop_no": 1,        "supplier_id": "sampleid",        "supplier_code": "S000000A",        "shipping_method": "shipping_01",        "shipping_etc": null,        "shipping_type": "B",        "shipping_place": "A Region.",        "shipping_start_date": 3,        "shipping_end_date": 7,        "shipping_fee_type": "D",        "free_shipping_price": null,        "shipping_fee": null,        "shipping_fee_by_quantity": null,        "shipping_rates": [            {                "shipping_rates_min": "0.00",                "shipping_rates_max": "30000.00",                "shipping_fee": "3000.00"            },            {                "shipping_rates_min": "30000.00",                "shipping_rates_max": "50000.00",                "shipping_fee": "2500.00"            }        ],        "prepaid_shipping_fee": "P",        "shipping_fee_by_product": "T",        "product_weight": "1.00",        "hscode": "0101211000",        "country_hscode": [            {                "country_code": "JPN",                "hscode": "010121100"            },            {                "country_code": "CHN",                "hscode": "01022100"            }        ]    }}
```
