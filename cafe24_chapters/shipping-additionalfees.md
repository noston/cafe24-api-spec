# SHIPPING ADDITIONALFEES


## Shipping additionalfees

```json
Endpoints    GET /api/v2/admin/shipping/additionalfees
```

```json
GET /api/v2/admin/shipping/additionalfees
```

### Shipping additionalfees property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| oversea_additional_fee | 해외배송 부가금액 사용여부 |
| country_code | 국가코드 |
| fee_name | 부과금액 명칭 |
| min_value | 조건 최소값 |
| max_value | 조건 최대값 |
| additional_fee | 부가금액 |
| unit | 해외배송 부가금액 단위 W : 정액 P : 퍼센트 |
| rounding_unit | 절사단위 F : 절사안함 0 : 1원단위 1 : 10원단위 2 : 100원단위 3 : 1000원단위 |
| rounding_rule | 절사 방법 L : 내림 U : 반올림 C : 올림 |

### Retrieve a list of applicable countries for additional handling fee on international shipping   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 배송 읽기권한 (mall.read_shipping) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| limit최소: [1]~최대: [500] | 조회결과 최대건수   DEFAULT 100 |
| offset최대값: [500] | 조회결과 시작위치   DEFAULT 0 |

```bash
Retrieve a list of applicable countries for additional handling fee on international shipping        Retrieve a list of applicable countries for additional handling fee on international shipping       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/shipping/additionalfees?shop_no=1' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "additionalfees": [        {            "shop_no": 1,            "oversea_additional_fee": "T",            "country_code": "GH",            "fee_name": "oversea_additional",            "min_value": "0.00",            "max_value": "500000.00",            "additional_fee": "20000.00",            "unit": "W",            "rounding_unit": "F",            "rounding_rule": "L"        },        {            "shop_no": 1,            "oversea_additional_fee": "T",            "country_code": "US",            "fee_name": "usa_shipping",            "min_value": "0.00",            "max_value": "1000000.00",            "additional_fee": "30000.00",            "unit": "W",            "rounding_unit": "F",            "rounding_rule": "L"        }    ],    "links": [        {            "rel": "prev",            "href": "https://{mallid}.cafe24api.com/api/v2/admin/shipping/additionalfees?shop_no=1&limit=100&offset=0"        },        {            "rel": "next",            "href": "https://{mallid}.cafe24api.com/api/v2/admin/shipping/additionalfees?shop_no=1&limit=100&offset=200"        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/shipping/additionalfees?shop_no=1' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "additionalfees": [        {            "shop_no": 1,            "oversea_additional_fee": "T",            "country_code": "GH",            "fee_name": "oversea_additional",            "min_value": "0.00",            "max_value": "500000.00",            "additional_fee": "20000.00",            "unit": "W",            "rounding_unit": "F",            "rounding_rule": "L"        },        {            "shop_no": 1,            "oversea_additional_fee": "T",            "country_code": "US",            "fee_name": "usa_shipping",            "min_value": "0.00",            "max_value": "1000000.00",            "additional_fee": "30000.00",            "unit": "W",            "rounding_unit": "F",            "rounding_rule": "L"        }    ],    "links": [        {            "rel": "prev",            "href": "https://{mallid}.cafe24api.com/api/v2/admin/shipping/additionalfees?shop_no=1&limit=100&offset=0"        },        {            "rel": "next",            "href": "https://{mallid}.cafe24api.com/api/v2/admin/shipping/additionalfees?shop_no=1&limit=100&offset=200"        }    ]}
```
