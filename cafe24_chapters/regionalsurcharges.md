# REGIONALSURCHARGES


## Regionalsurcharges

```json
Endpoints    GET /api/v2/admin/regionalsurcharges
PUT /api/v2/admin/regionalsurcharges
```

```json
GET /api/v2/admin/regionalsurcharges
PUT /api/v2/admin/regionalsurcharges
```

### Regionalsurcharges property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| use_regional_surcharge | 지역별 배송비 사용여부 T : 사용함 F : 사용안함 |
| region_setting_type | 지역 설정 방식 A : 간편 설정 N : 지명 설정 Z : 우편번호 설정 |
| regional_surcharge_list | 지역별 배송비 목록 |
| jeju_surcharge_amount | 제주 추가 배송비 |
| remote_area_surcharge_amount | 도서산간 추가 배송비 |

### Retrieve shipping zone rates settings   cafe24

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
Retrieve shipping zone rates settings        Retrieve shipping zone rates settings       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/regionalsurcharges' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "regionalsurcharge": {        "shop_no": 1,        "use_regional_surcharge": "T",        "region_setting_type": "Z",        "regional_surcharge_list": [            {                "regional_surcharge_no": 1,                "region_name": "Gyeonggi-do",                "surcharge_region_name": null,                "country_code": null,                "start_zipcode": "11750",                "end_zipcode": "11750",                "regional_surcharge_amount": "2200.00"            },            {                "regional_surcharge_no": 2,                "region_name": "Seoul",                "surcharge_region_name": null,                "country_code": null,                "start_zipcode": "05200",                "end_zipcode": "05200",                "regional_surcharge_amount": "1000.00"            }        ],        "jeju_surcharge_amount": null,        "remote_area_surcharge_amount": null    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/regionalsurcharges' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "regionalsurcharge": {        "shop_no": 1,        "use_regional_surcharge": "T",        "region_setting_type": "Z",        "regional_surcharge_list": [            {                "regional_surcharge_no": 1,                "region_name": "Gyeonggi-do",                "surcharge_region_name": null,                "country_code": null,                "start_zipcode": "11750",                "end_zipcode": "11750",                "regional_surcharge_amount": "2200.00"            },            {                "regional_surcharge_no": 2,                "region_name": "Seoul",                "surcharge_region_name": null,                "country_code": null,                "start_zipcode": "05200",                "end_zipcode": "05200",                "regional_surcharge_amount": "1000.00"            }        ],        "jeju_surcharge_amount": null,        "remote_area_surcharge_amount": null    }}
```

### Update regional surcharges   cafe24

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
| use_regional_surcharge | 지역별 배송비 사용여부   T : 사용함 F : 사용안함 |
| region_setting_type | 지역 설정 방식   A : 간편 설정 N : 지명 설정 Z : 우편번호 설정 |
| jeju_surcharge_amount최소: [0]~최대: [999999999] | 제주 추가 배송비 |
| remote_area_surcharge_amount최소: [0]~최대: [999999999] | 도서산간 추가 배송비 |

```bash
Update regional surcharges        Update regional surcharges       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/regionalsurcharges' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "use_regional_surcharge": "T",        "region_setting_type": "A",        "jeju_surcharge_amount": "0.00",        "remote_area_surcharge_amount": "0.00"    }}'    Response  Copy     {    "regionalsurcharge": {        "shop_no": 1,        "use_regional_surcharge": "T",        "region_setting_type": "A",        "jeju_surcharge_amount": "0.00",        "remote_area_surcharge_amount": "0.00"    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/regionalsurcharges' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "use_regional_surcharge": "T",        "region_setting_type": "A",        "jeju_surcharge_amount": "0.00",        "remote_area_surcharge_amount": "0.00"    }}'
```

```json
{    "regionalsurcharge": {        "shop_no": 1,        "use_regional_surcharge": "T",        "region_setting_type": "A",        "jeju_surcharge_amount": "0.00",        "remote_area_surcharge_amount": "0.00"    }}
```
