# SHIPPING


## Shipping

```json
Endpoints    GET /api/v2/admin/shipping
PUT /api/v2/admin/shipping
```

```json
GET /api/v2/admin/shipping
PUT /api/v2/admin/shipping
```

### Shipping property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| shipping_method | 배송방법 shipping_01 : 택배 shipping_02 : 빠른등기 shipping_04 : 직접배송 shipping_05 : 퀵배송 shipping_06 : 기타 shipping_07 : 화물배송 shipping_08 : 매장직접수령 shipping_09 : 배송필요 없음 shipping_10 : 고객직접선택 |
| shipping_etc | 기타배송 |
| shipping_type | 국내/해외배송 설정 A : 국내배송 C : 해외배송 B : 국내/해외배송 |
| international_shipping_fee_criteria | 해외 배송비 기준 설정 B : 쇼핑몰 자체 배송비 E : 자동 책정 배송비(EMS) |
| shipping_place | 배송지역 |
| shipping_period | 배송기간 |
| shipping_fee_type | 배송비타입 T : 배송비 무료 R : 고정배송비 사용 M : 구매 금액에 따른 부과 D : 구매 금액별 차등 배송료 사용 W : 상품 무게별 차등 배송료 사용 C : 상품 수량별 차등 배송료 사용 N : 상품 수량에 비례하여 배송료 부과 |
| shipping_fee최대값: [999999999] | 배송비 |
| free_shipping_price최대값: [99999999999999] | 배송비 무료 최소금액 배송비 설정 > 구매 금액에 따른 부과 일 경우 사용 |
| shipping_fee_by_quantity최대값: [999999999] | 상품 수량별 배송비 배송비 설정 > 상품 수량에 비례하여 배송료 부과 일 경우 사용 |
| shipping_rates | 배송비 상세 설정 |
| shipping_fee_criteria | 배송비 청구 기준 주문금액 조건 설정 D : 할인전 정상판매가격 기준(권장) L : 최종 주문(결제)금액 기준 A : 할인 적용 후 결제 금액 기준 R : 최종 실 결제금액 기준 |
| prepaid_shipping_fee | 배송비 선결제 설정 C : 착불 P : 선결제 B : 착불/선결제 |
| product_weight | 상품중량 |
| oversea_shipping_country | 해외배송가능 국가 제한 여부 T : 제한함 F : 제한안함 |
| oversea_shipping_country_list | 배송국가 |
| country_shipping_fee | 배송비 국가별 개별 설정 여부 T : 사용함 F : 사용안함 |
| country_shipping_fee_list | 국가별 배송비 |
| international_shipping_insurance | 해외배송 보험료 T : 사용함 F : 사용안함 |
| return_address | 반품주소 |
| package_volume | 배송규격 |
| wished_delivery_date | 희망배송일 |
| wished_delivery_time | 희망배송시간 |
| hs_code | HS코드 |
| country_hs_code | 국가별 HS 코드 |
| individual_shipping_fee | 상품별 개별배송비 설정 여부 T : 사용함 F : 사용안함 |
| individual_fee_calculation_type | 개별배송비 계산 기준 P : 상품별  I : 품목별 |
| supplier_shipping_fee | 공급사 배송비 사용 여부 T : 사용함 F : 사용안함 |
| supplier_selection | 공급사 배송비 사용 범위 A : 전체 공급사 P : 특정 공급사 |
| applicable_suppliers | 공급사 배송비 사용 공급사 |
| supplier_shipping_calculation | 공급사 배송비 계산 기준 A : 전체 상품금액 합계 S : 대표운영자와 공급사 상품 별도 합계 |
| supplier_regional_surcharge | 공급사 지역별 배송비 A : 대표 운영자의 지역별 배송료를 부과 S : 공급사 관리자 설정에 따라 부과 |
| additional_shipping_fee | 추가 배송비 설정 |
| shipping_company_type | 배송업체 선택 |
| oversea_additional_fee | 해외배송 부가금액 사용여부 T : 사용함 F : 사용안함 |
| oversea_additional_fee_list | 해외배송 부가금액 적용국가 |

### Retrieve shipping / return settings   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 배송 읽기권한 (mall.read_shipping) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |

```bash
Retrieve shipping / return settings        Retrieve shipping / return settings       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/shipping' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "shipping": {        "shop_no": 1,        "shipping_method": "shipping_01",        "shipping_etc": null,        "shipping_type": "C",        "international_shipping_fee_criteria": null,        "shipping_place": null,        "shipping_period": {            "minimum": 3,            "maximum": 7        },        "product_weight": "1.00",        "shipping_fee_type": "D",        "shipping_fee": null,        "free_shipping_price": null,        "shipping_fee_by_quantity": null,        "shipping_rates": [            {                "min_value": "0.00",                "max_value": "10000.00",                "shipping_fee": "2500.00"            },            {                "min_value": "10000.00",                "max_value": "50000.00",                "shipping_fee": "1000.00"            }        ],        "shipping_fee_criteria": "D",        "prepaid_shipping_fee": "P",        "oversea_shipping_country": "T",        "oversea_shipping_country_list": [            {                "country_code": "US"            },            {                "country_code": "JP"            }        ],        "country_shipping_fee": "T",        "country_shipping_fee_list": [            {                "country_code": "US",                "conditional": "price",                "min_value": "1.00",                "max_value": "1000.00",                "shipping_fee": "1000.00"            },            {                "country_code": "JP",                "conditional": "quantity",                "min_value": "1",                "max_value": "3",                "shipping_fee": "1000.00"            }        ],        "international_shipping_insurance": "T",        "return_address": {            "zipcode": "07071",            "ziptype": "KOR",            "address1": "Sindaebang dong Dongjak-gu, Seoul, Republic of Korea",            "address2": "Professional Construction Hall"        },        "package_volume": {            "width": "22",            "length": "19",            "height": "9"        },        "wished_delivery_date": {            "use": "T",            "range": {                "minimum": 1,                "maximum": 3            },            "default": {                "minimum": null,                "use_fast_delivery": "T"            }        },        "wished_delivery_time": {            "use": "T",            "range": [                {                    "start_hour": "08",                    "end_hour": "17"                },                {                    "start_hour": "00",                    "end_hour": "07"                }            ],            "default": {                "range": {                    "start_hour": "08",                    "end_hour": "17"                },                "use_fast_delivery": "F"            }        },        "hs_code": "4203109010",        "country_hs_code": [            {                "hs_code": "61102000",                "country_code": "CHN"            },            {                "hs_code": "392690010",                "country_code": "JPN"            }        ],        "individual_shipping_fee": "F",        "individual_fee_calculation_type": null,        "supplier_shipping_fee": "T",        "supplier_selection": "P",        "applicable_suppliers": [            {                "supplier_code": "S000000A",                "supplier_id": "sampleid1"            },            {                "supplier_code": "S000000B",                "supplier_id": "sampleid2"            }        ],        "supplier_shipping_calculation": "A",        "supplier_regional_surcharge": "A",        "additional_shipping_fee": null,        "shipping_company_type": [            {                "carrier_id": 1,                "is_selected": "F",                "shipping_carrier_code": "0012",                "shipping_type": "A",                "shipping_carrier": "우체국택배"            },            {                "carrier_id": 2,                "is_selected": "F",                "shipping_carrier_code": "0006",                "shipping_type": "B",                "shipping_carrier": "CJ대한통운"            }        ]    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/shipping' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "shipping": {        "shop_no": 1,        "shipping_method": "shipping_01",        "shipping_etc": null,        "shipping_type": "C",        "international_shipping_fee_criteria": null,        "shipping_place": null,        "shipping_period": {            "minimum": 3,            "maximum": 7        },        "product_weight": "1.00",        "shipping_fee_type": "D",        "shipping_fee": null,        "free_shipping_price": null,        "shipping_fee_by_quantity": null,        "shipping_rates": [            {                "min_value": "0.00",                "max_value": "10000.00",                "shipping_fee": "2500.00"            },            {                "min_value": "10000.00",                "max_value": "50000.00",                "shipping_fee": "1000.00"            }        ],        "shipping_fee_criteria": "D",        "prepaid_shipping_fee": "P",        "oversea_shipping_country": "T",        "oversea_shipping_country_list": [            {                "country_code": "US"            },            {                "country_code": "JP"            }        ],        "country_shipping_fee": "T",        "country_shipping_fee_list": [            {                "country_code": "US",                "conditional": "price",                "min_value": "1.00",                "max_value": "1000.00",                "shipping_fee": "1000.00"            },            {                "country_code": "JP",                "conditional": "quantity",                "min_value": "1",                "max_value": "3",                "shipping_fee": "1000.00"            }        ],        "international_shipping_insurance": "T",        "return_address": {            "zipcode": "07071",            "ziptype": "KOR",            "address1": "Sindaebang dong Dongjak-gu, Seoul, Republic of Korea",            "address2": "Professional Construction Hall"        },        "package_volume": {            "width": "22",            "length": "19",            "height": "9"        },        "wished_delivery_date": {            "use": "T",            "range": {                "minimum": 1,                "maximum": 3            },            "default": {                "minimum": null,                "use_fast_delivery": "T"            }        },        "wished_delivery_time": {            "use": "T",            "range": [                {                    "start_hour": "08",                    "end_hour": "17"                },                {                    "start_hour": "00",                    "end_hour": "07"                }            ],            "default": {                "range": {                    "start_hour": "08",                    "end_hour": "17"                },                "use_fast_delivery": "F"            }        },        "hs_code": "4203109010",        "country_hs_code": [            {                "hs_code": "61102000",                "country_code": "CHN"            },            {                "hs_code": "392690010",                "country_code": "JPN"            }        ],        "individual_shipping_fee": "F",        "individual_fee_calculation_type": null,        "supplier_shipping_fee": "T",        "supplier_selection": "P",        "applicable_suppliers": [            {                "supplier_code": "S000000A",                "supplier_id": "sampleid1"            },            {                "supplier_code": "S000000B",                "supplier_id": "sampleid2"            }        ],        "supplier_shipping_calculation": "A",        "supplier_regional_surcharge": "A",        "additional_shipping_fee": null,        "shipping_company_type": [            {                "carrier_id": 1,                "is_selected": "F",                "shipping_carrier_code": "0012",                "shipping_type": "A",                "shipping_carrier": "우체국택배"            },            {                "carrier_id": 2,                "is_selected": "F",                "shipping_carrier_code": "0006",                "shipping_type": "B",                "shipping_carrier": "CJ대한통운"            }        ]    }}
```

### Update store shipping/return settings   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 배송 쓰기권한 (mall.write_shipping) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| shipping_method | 배송방법   shipping_01 : 택배 shipping_02 : 빠른등기 shipping_04 : 직접배송 shipping_05 : 퀵배송 shipping_06 : 기타 shipping_07 : 화물배송 shipping_08 : 매장직접수령 shipping_09 : 배송필요 없음 shipping_10 : 고객직접선택 |
| shipping_etc최대글자수 : [25자] | 기타배송 |
| shipping_type | 국내/해외배송 설정   A : 국내배송 C : 해외배송 B : 국내/해외배송 |
| international_shipping_fee_criteria | 해외 배송비 기준 설정   B : 쇼핑몰 자체 배송비 E : 자동 책정 배송비(EMS) |
| shipping_place | 배송지역 |
| shipping_period | 배송기간 |
| shipping_period 하위 요소 보기     minimum최소 기간 maximum최대 기간 |
| shipping_fee_type | 배송비타입   T : 배송비 무료 R : 고정배송비 사용 M : 구매 금액에 따른 부과 D : 구매 금액별 차등 배송료 사용 W : 상품 무게별 차등 배송료 사용 C : 상품 수량별 차등 배송료 사용 N : 상품 수량에 비례하여 배송료 부과 |
| shipping_fee최대값: [999999999] | 배송비 |
| free_shipping_price최대값: [99999999999999] | 배송비 무료 최소금액 |
| shipping_fee_by_quantity최대값: [999999999] | 상품 수량별 배송비 |
| shipping_rates | 배송비 상세 설정 |
| shipping_rates 하위 요소 보기     min_value조건 최소값 max_value조건 최대값 shipping_fee배송비 |
| shipping_fee_criteria | 배송비 청구 기준 주문금액 조건 설정   D : 할인전 정상판매가격 기준(권장) A : 할인 적용 후 결제 금액 기준 |
| prepaid_shipping_fee | 배송비 선결제 설정   EC 일본, 베트남, 필리핀 버전에서는 사용할 수 없음.   C : 착불 P : 선결제 B : 착불/선결제 |
| product_weight최소값: [0]최대값: [30] | 상품중량 |
| oversea_shipping_country | 해외배송가능 국가 제한 여부   T : 제한함 F : 제한안함 |
| oversea_shipping_country_list | 배송국가 |
| oversea_shipping_country_list 하위 요소 보기     country_code국가코드 |
| country_shipping_fee | 배송비 국가별 개별 설정 여부   EC 일본, 베트남, 필리핀 버전에서는 사용할 수 없음.   T : 사용함 F : 사용안함 |
| country_shipping_fee_list | 국가별 배송비   EC 일본, 베트남, 필리핀 버전에서는 사용할 수 없음. |
| country_shipping_fee_list 하위 요소 보기     country_code국가코드 conditional배송비 책정 조건quantity : 수량 weight : 무게 price : 가격 min_value조건 최소값 max_value조건 최대값 shipping_fee배송비 |
| international_shipping_insurance | 해외배송 보험료   EC 한국 버전에서만 사용할 수 있음.   T : 사용함 F : 사용안함 |
| return_address | 반품주소 |
| return_address 하위 요소 보기     zipcode우편번호 ziptype우편번호 선택 국가 address1기본 주소 address2상세 주소 |
| package_volume | 배송규격 |
| package_volume 하위 요소 보기     width가로 length세로 height높이 |
| individual_shipping_fee | 상품별 개별배송비 설정 여부   T : 사용함 F : 사용안함 |
| individual_fee_calculation_type | 개별배송비 계산 기준   P : 상품별  I : 품목별 |
| additional_shipping_fee글자수 최소: [1자]~최대: [9자]최소: [0]~최대: [999999999] | 추가 배송비 설정 |
| shipping_company_type | 배송업체 선택 |
| shipping_company_type 하위 요소 보기     carrier_id배송사 아이디 is_selected선택여부T: 선택 F: 선택안함 |
| hs_code최대글자수 : [20자] | HS코드 |
| country_hs_code배열 최대사이즈: [29] | 국가별 HS 코드 |
| oversea_additional_fee | 해외배송 부가금액 사용여부   T : 사용함 F : 사용안함 |
| oversea_additional_fee_list배열 최대사이즈: [500] | 해외배송 부가금액 적용국가 |
| oversea_additional_fee_list 하위 요소 보기     country_code국가코드 fee_name부과금액 명칭 min_value조건 최소값 max_value조건 최대값 additional_fee부가금액 unit해외배송 부가금액 단위W : 정액 P : 퍼센트 rounding_unit절사단위F : 절사안함 0 : 1원단위 1 : 10원단위 2 : 100원단위 3 : 1000원단위 rounding_rule절사 방법L : 내림 U : 반올림 C : 올림 |

```bash
Update store shipping/return settings        Update store shipping/return settings Update shipping period of the store Update return address of the store       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/shipping' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "shipping_method": "shipping_01",        "shipping_type": "C",        "shipping_period": {            "minimum": 5,            "maximum": 12        },        "shipping_fee_type": "D",        "shipping_rates": [            {                "min_value": "0.00",                "max_value": "1000.00",                "shipping_fee": "3000.00"            },            {                "min_value": "1000.00",                "max_value": "10000.00",                "shipping_fee": "1500.00"            }        ],        "shipping_fee_criteria": "D",        "product_weight": "5.00",        "oversea_shipping_country": "T",        "oversea_shipping_country_list": [            {                "country_code": "US"            },            {                "country_code": "JP"            }        ],        "country_shipping_fee": "T",        "country_shipping_fee_list": [            {                "country_code": "US",                "conditional": "price",                "min_value": "1.00",                "max_value": "1000.00",                "shipping_fee": "1000.00"            },            {                "country_code": "JP",                "conditional": "quantity",                "min_value": "1",                "max_value": "3",                "shipping_fee": "1000.00"            }        ],        "international_shipping_fee_criteria": "B",        "international_shipping_insurance": "T",        "return_address": {            "zipcode": "07071",            "ziptype": "KOR",            "address1": "Sindaebang dong Dongjak-gu, Seoul, Republic of Korea",            "address2": "Professional Construction Hall"        },        "package_volume": {            "width": "22",            "length": "19",            "height": "9"        },        "individual_shipping_fee": "F",        "additional_shipping_fee": null,        "shipping_company_type": null,        "hs_code": "4303101990",        "country_hs_code": [            {                "hs_code": "430310011",                "country_code": "JPN"            },            {                "hs_code": "43031020",                "country_code": "CHN"            }        ],        "oversea_additional_fee": "T",        "oversea_additional_fee_list": [            {                "country_code": "GH",                "fee_name": "oversea_additional",                "min_value": "0.00",                "max_value": "500000.00",                "additional_fee": "20000.00",                "unit": "W",                "rounding_unit": "F",                "rounding_rule": "L"            }        ]    }}'    Response  Copy     {    "shipping": {        "shop_no": 1,        "shipping_method": "shipping_01",        "shipping_etc": null,        "shipping_type": "C",        "international_shipping_fee_criteria": "B",        "shipping_place": null,        "shipping_period": {            "minimum": 5,            "maximum": 12        },        "shipping_fee_type": "D",        "shipping_rates": [            {                "min_value": "0.00",                "max_value": "1000.00",                "shipping_fee": "3000.00"            },            {                "min_value": "1000.00",                "max_value": "10000.00",                "shipping_fee": "1500.00"            }        ],        "shipping_fee_criteria": "D",        "product_weight": "5.00",        "oversea_shipping_country": "T",        "oversea_shipping_country_list": [            {                "country_code": "US"            },            {                "country_code": "JP"            }        ],        "country_shipping_fee": "T",        "country_shipping_fee_list": [            {                "country_code": "US",                "conditional": "price",                "min_value": "1.00",                "max_value": "1000.00",                "shipping_fee": "1000.00"            },            {                "country_code": "JP",                "conditional": "quantity",                "min_value": "1",                "max_value": "3",                "shipping_fee": "1000.00"            }        ],        "international_shipping_insurance": "T",        "return_address": {            "zipcode": "07071",            "ziptype": "KOR",            "address1": "Sindaebang dong Dongjak-gu, Seoul, Republic of Korea",            "address2": "Professional Construction Hall"        },        "package_volume": {            "width": "22",            "length": "19",            "height": "9"        },        "individual_shipping_fee": "F",        "individual_fee_calculation_type": null,        "additional_shipping_fee": null,        "shipping_company_type": [            {                "carrier_id": 1,                "is_selected": "F",                "shipping_carrier_code": "0012",                "shipping_type": "A",                "shipping_carrier": "우체국택배"            },            {                "carrier_id": 2,                "is_selected": "F",                "shipping_carrier_code": "0006",                "shipping_type": "B",                "shipping_carrier": "CJ대한통운"            }        ],        "hs_code": "4303101990",        "country_hs_code": [            {                "hs_code": "430310011",                "country_code": "JPN"            },            {                "hs_code": "43031020",                "country_code": "CHN"            }        ],        "oversea_additional_fee": "T",        "oversea_additional_fee_list": [            {                "country_code": "GH",                "fee_name": "oversea_additional",                "min_value": "0.00",                "max_value": "500000.00",                "additional_fee": "20000.00",                "unit": "W",                "rounding_unit": "F",                "rounding_rule": "L"            }        ]    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/shipping' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "shipping_method": "shipping_01",        "shipping_type": "C",        "shipping_period": {            "minimum": 5,            "maximum": 12        },        "shipping_fee_type": "D",        "shipping_rates": [            {                "min_value": "0.00",                "max_value": "1000.00",                "shipping_fee": "3000.00"            },            {                "min_value": "1000.00",                "max_value": "10000.00",                "shipping_fee": "1500.00"            }        ],        "shipping_fee_criteria": "D",        "product_weight": "5.00",        "oversea_shipping_country": "T",        "oversea_shipping_country_list": [            {                "country_code": "US"            },            {                "country_code": "JP"            }        ],        "country_shipping_fee": "T",        "country_shipping_fee_list": [            {                "country_code": "US",                "conditional": "price",                "min_value": "1.00",                "max_value": "1000.00",                "shipping_fee": "1000.00"            },            {                "country_code": "JP",                "conditional": "quantity",                "min_value": "1",                "max_value": "3",                "shipping_fee": "1000.00"            }        ],        "international_shipping_fee_criteria": "B",        "international_shipping_insurance": "T",        "return_address": {            "zipcode": "07071",            "ziptype": "KOR",            "address1": "Sindaebang dong Dongjak-gu, Seoul, Republic of Korea",            "address2": "Professional Construction Hall"        },        "package_volume": {            "width": "22",            "length": "19",            "height": "9"        },        "individual_shipping_fee": "F",        "additional_shipping_fee": null,        "shipping_company_type": null,        "hs_code": "4303101990",        "country_hs_code": [            {                "hs_code": "430310011",                "country_code": "JPN"            },            {                "hs_code": "43031020",                "country_code": "CHN"            }        ],        "oversea_additional_fee": "T",        "oversea_additional_fee_list": [            {                "country_code": "GH",                "fee_name": "oversea_additional",                "min_value": "0.00",                "max_value": "500000.00",                "additional_fee": "20000.00",                "unit": "W",                "rounding_unit": "F",                "rounding_rule": "L"            }        ]    }}'
```

```json
{    "shipping": {        "shop_no": 1,        "shipping_method": "shipping_01",        "shipping_etc": null,        "shipping_type": "C",        "international_shipping_fee_criteria": "B",        "shipping_place": null,        "shipping_period": {            "minimum": 5,            "maximum": 12        },        "shipping_fee_type": "D",        "shipping_rates": [            {                "min_value": "0.00",                "max_value": "1000.00",                "shipping_fee": "3000.00"            },            {                "min_value": "1000.00",                "max_value": "10000.00",                "shipping_fee": "1500.00"            }        ],        "shipping_fee_criteria": "D",        "product_weight": "5.00",        "oversea_shipping_country": "T",        "oversea_shipping_country_list": [            {                "country_code": "US"            },            {                "country_code": "JP"            }        ],        "country_shipping_fee": "T",        "country_shipping_fee_list": [            {                "country_code": "US",                "conditional": "price",                "min_value": "1.00",                "max_value": "1000.00",                "shipping_fee": "1000.00"            },            {                "country_code": "JP",                "conditional": "quantity",                "min_value": "1",                "max_value": "3",                "shipping_fee": "1000.00"            }        ],        "international_shipping_insurance": "T",        "return_address": {            "zipcode": "07071",            "ziptype": "KOR",            "address1": "Sindaebang dong Dongjak-gu, Seoul, Republic of Korea",            "address2": "Professional Construction Hall"        },        "package_volume": {            "width": "22",            "length": "19",            "height": "9"        },        "individual_shipping_fee": "F",        "individual_fee_calculation_type": null,        "additional_shipping_fee": null,        "shipping_company_type": [            {                "carrier_id": 1,                "is_selected": "F",                "shipping_carrier_code": "0012",                "shipping_type": "A",                "shipping_carrier": "우체국택배"            },            {                "carrier_id": 2,                "is_selected": "F",                "shipping_carrier_code": "0006",                "shipping_type": "B",                "shipping_carrier": "CJ대한통운"            }        ],        "hs_code": "4303101990",        "country_hs_code": [            {                "hs_code": "430310011",                "country_code": "JPN"            },            {                "hs_code": "43031020",                "country_code": "CHN"            }        ],        "oversea_additional_fee": "T",        "oversea_additional_fee_list": [            {                "country_code": "GH",                "fee_name": "oversea_additional",                "min_value": "0.00",                "max_value": "500000.00",                "additional_fee": "20000.00",                "unit": "W",                "rounding_unit": "F",                "rounding_rule": "L"            }        ]    }}
```
