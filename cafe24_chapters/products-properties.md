# PRODUCTS PROPERTIES


## Products properties

```json
Endpoints    GET /api/v2/admin/products/properties
POST /api/v2/admin/products/properties
PUT /api/v2/admin/products/properties
```

```json
GET /api/v2/admin/products/properties
POST /api/v2/admin/products/properties
PUT /api/v2/admin/products/properties
```

### Products properties property list

| Attribute | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호 |
| properties | 항목 속성 |
| property | 항목 속성 |

### Retrieve fields for product details   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 읽기권한 (mall.read_product) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |

```bash
Retrieve fields for product details        Retrieve fields for product details       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/products/properties' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "product": {        "shop_no": 1,        "properties": [            {                "key": "product_name",                "name": "Product Name",                "display": "F",                "font_type": "N",                "font_size": 13,                "font_color": "#000000"            },            {                "key": "manufacturer_name",                "name": "Manufacturer",                "display": "T",                "font_type": "N",                "font_size": 14,                "font_color": "#333333"            }        ]    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/products/properties' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "product": {        "shop_no": 1,        "properties": [            {                "key": "product_name",                "name": "Product Name",                "display": "F",                "font_type": "N",                "font_size": 13,                "font_color": "#000000"            },            {                "key": "manufacturer_name",                "name": "Manufacturer",                "display": "T",                "font_type": "N",                "font_size": 14,                "font_color": "#333333"            }        ]    }}
```

### Create a field for product details page   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 쓰기권한 (mall.write_product) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| property | 항목 속성 |
| property 하위 요소 보기     multishop_display_names Array    multishop_display_names 하위 요소 보기     shop_no멀티쇼핑몰 번호Required name항목명 표시텍스트Required    display항목 표시여부DEFAULT F display_name항목명 표시설정T : 사용함 F : 사용안함DEFAULT T font_type글자 타입N : 보통(Normal) B : 굵게(Bold) I : 기울임(Italic) D : 굵게 기울임(Bold Italic)DEFAULT N font_size글자 크기DEFAULT 12 font_color글자 색상DEFAULT #555555 exposure_group_type표시 대상 타입A: 전체 M: 회원DEFAULT A |

```bash
Create a field for product details page        Create a field for product details page       Request   cURL Java Python Node.js PHP Go  Copy     curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/products/properties' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "request": {        "property": {            "multishop_display_names": [                {                    "shop_no": 1,                    "name": "Custom Property1"                },                {                    "shop_no": 2,                    "name": "Custom Property2"                }            ],            "display": "T",            "display_name": "T",            "font_type": "N",            "font_size": 13,            "font_color": "#000000",            "exposure_group_type": "M"        }    }}'    Response  Copy     {    "product": {        "property": {            "key": "custom_option1",            "multishop_display_names": [                {                    "shop_no": 1,                    "name": "Custom Property1"                },                {                    "shop_no": 2,                    "name": "Custom Property2"                }            ],            "display": "T",            "display_name": "T",            "font_type": "N",            "font_size": 13,            "font_color": "#000000",            "exposure_group_type": "M"        }    }}
```

```bash
curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/products/properties' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "request": {        "property": {            "multishop_display_names": [                {                    "shop_no": 1,                    "name": "Custom Property1"                },                {                    "shop_no": 2,                    "name": "Custom Property2"                }            ],            "display": "T",            "display_name": "T",            "font_type": "N",            "font_size": 13,            "font_color": "#000000",            "exposure_group_type": "M"        }    }}'
```

```json
{    "product": {        "property": {            "key": "custom_option1",            "multishop_display_names": [                {                    "shop_no": 1,                    "name": "Custom Property1"                },                {                    "shop_no": 2,                    "name": "Custom Property2"                }            ],            "display": "T",            "display_name": "T",            "font_type": "N",            "font_size": 13,            "font_color": "#000000",            "exposure_group_type": "M"        }    }}
```

### Update fields for product details   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 쓰기권한 (mall.write_product) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| properties | 항목 속성 |
| properties 하위 요소 보기     keyRequired항목코드 name항목명 표시텍스트 display항목 표시여부 font_type글자 타입N : 보통(Normal) B : 굵게(Bold) I : 기울임(Italic) D : 굵게 기울임(Bold Italic) font_size글자 크기 font_color글자 색상 |

```bash
Update fields for product details        Update fields for product details       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/products/properties' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "properties": [            {                "key": "product_name",                "name": "Product Name",                "display": "F",                "font_type": "N",                "font_size": 13,                "font_color": "#000000"            },            {                "key": "manufacturer_name",                "name": "Manufacturer",                "display": "T",                "font_type": "N",                "font_size": 14,                "font_color": "#333333"            }        ]    }}'    Response  Copy     {    "product": {        "shop_no": 1,        "properties": [            {                "key": "product_name",                "name": "Product Name",                "display": "F",                "font_type": "N",                "font_size": 13,                "font_color": "#000000"            },            {                "key": "manufacturer_name",                "name": "Manufacturer",                "display": "T",                "font_type": "N",                "font_size": 14,                "font_color": "#333333"            }        ]    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/products/properties' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "properties": [            {                "key": "product_name",                "name": "Product Name",                "display": "F",                "font_type": "N",                "font_size": 13,                "font_color": "#000000"            },            {                "key": "manufacturer_name",                "name": "Manufacturer",                "display": "T",                "font_type": "N",                "font_size": 14,                "font_color": "#333333"            }        ]    }}'
```

```json
{    "product": {        "shop_no": 1,        "properties": [            {                "key": "product_name",                "name": "Product Name",                "display": "F",                "font_type": "N",                "font_size": 13,                "font_color": "#000000"            },            {                "key": "manufacturer_name",                "name": "Manufacturer",                "display": "T",                "font_type": "N",                "font_size": 14,                "font_color": "#333333"            }        ]    }}
```
