# PRODUCTS CUSTOMPROPERTIES


## Products customproperties

```json
Endpoints    GET /api/v2/admin/products/{product_no}/customproperties
PUT /api/v2/admin/products/{product_no}/customproperties/{property_no}
DELETE /api/v2/admin/products/{product_no}/customproperties/{property_no}
```

```json
GET /api/v2/admin/products/{product_no}/customproperties
PUT /api/v2/admin/products/{product_no}/customproperties/{property_no}
DELETE /api/v2/admin/products/{product_no}/customproperties/{property_no}
```

### Products customproperties property list

| Attribute | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호 |
| custom_properties | 자체 정의 속성 |

### Retrieve user-defined properties by product   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 읽기권한 (mall.read_product) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| product_noRequired | 상품번호 |

```bash
Retrieve user-defined properties by product        Retrieve user-defined properties by product       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Update user-defined properties by product   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 쓰기권한 (mall.write_product) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| product_noRequired | 상품번호 |
| property_noRequired | 자체 정의 속성 번호 |
| shop_no최소값: [1] | 멀티쇼핑몰 번호 |
| property_value | 자체 정의 속성 값 |

```bash
Update user-defined properties by product        Update user-defined properties by product       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Delete user-defined properties by product   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 쓰기권한 (mall.write_product) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| product_noRequired | 상품번호 |
| property_noRequired | 자체 정의 속성 번호 |

```bash
Delete user-defined properties by product        Delete user-defined properties by product       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

## Products customproperties

```json
Endpoints    GET /api/v2/admin/products/customproperties
POST /api/v2/admin/products/customproperties
PUT /api/v2/admin/products/customproperties/{property_no}
DELETE /api/v2/admin/products/customproperties/{property_no}
```

```json
GET /api/v2/admin/products/customproperties
POST /api/v2/admin/products/customproperties
PUT /api/v2/admin/products/customproperties/{property_no}
DELETE /api/v2/admin/products/customproperties/{property_no}
```

### Products customproperties property list

| Attribute | Description |
| --- | --- |
| custom_properties | 자체 정의 속성 |

### Retrieve user-defined properties   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 읽기권한 (mall.read_product) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |

```bash
Retrieve user-defined properties        Retrieve user-defined properties       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/products/customproperties' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "products": {        "custom_properties": [            {                "property_no": 1001,                "property_name": "Color"            },            {                "property_no": 1002,                "property_name": "Size"            }        ]    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/products/customproperties' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "products": {        "custom_properties": [            {                "property_no": 1001,                "property_name": "Color"            },            {                "property_no": 1002,                "property_name": "Size"            }        ]    }}
```

### Create user-defined properties   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 쓰기권한 (mall.write_product) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| custom_properties | 자체 정의 속성 |
| custom_properties 하위 요소 보기     property_nameRequired자체 정의 속성 이름 |

```bash
Create user-defined properties        Create user-defined properties       Request   cURL Java Python Node.js PHP Go  Copy     curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/products/customproperties' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "request": {        "custom_properties": [            {                "property_name": "Color"            },            {                "property_name": "Size"            }        ]    }}'    Response  Copy     {    "product": {        "custom_properties": [            {                "property_no": 1001,                "property_name": "Color"            },            {                "property_no": 1002,                "property_name": "Size"            }        ]    }}
```

```bash
curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/products/customproperties' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "request": {        "custom_properties": [            {                "property_name": "Color"            },            {                "property_name": "Size"            }        ]    }}'
```

```json
{    "product": {        "custom_properties": [            {                "property_no": 1001,                "property_name": "Color"            },            {                "property_no": 1002,                "property_name": "Size"            }        ]    }}
```

### Update user-defined properties   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 쓰기권한 (mall.write_product) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| property_noRequired | 자체 정의 속성 번호 |
| property_nameRequired최대글자수 : [250자] | 자체 정의 속성 이름 |

```bash
Update user-defined properties        Update user-defined properties       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/products/customproperties/1001' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "request": {        "property_name": "Volumn"    }}'    Response  Copy     {    "product": {        "custom_properties": [            {                "property_no": 1001,                "property_name": "Volumn"            },            {                "property_no": 1002,                "property_name": "Size"            }        ]    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/products/customproperties/1001' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "request": {        "property_name": "Volumn"    }}'
```

```json
{    "product": {        "custom_properties": [            {                "property_no": 1001,                "property_name": "Volumn"            },            {                "property_no": 1002,                "property_name": "Size"            }        ]    }}
```

### Delete user-defined properties   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 쓰기권한 (mall.write_product) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| property_noRequired | 자체 정의 속성 번호 |

```bash
Delete user-defined properties        Delete user-defined properties       Request   cURL Java Python Node.js PHP Go  Copy     curl -X DELETE \  'https://{mallid}.cafe24api.com/api/v2/admin/products/customproperties/1001' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "product": {        "custom_properties": [            {                "property_no": 1002,                "property_name": "Size"            }        ]    }}
```

```bash
curl -X DELETE \  'https://{mallid}.cafe24api.com/api/v2/admin/products/customproperties/1001' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "product": {        "custom_properties": [            {                "property_no": 1002,                "property_name": "Size"            }        ]    }}
```
