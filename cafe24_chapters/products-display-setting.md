# PRODUCTS DISPLAY SETTING


## Products display setting

```json
Endpoints    GET /api/v2/admin/products/display/setting
PUT /api/v2/admin/products/display/setting
```

```json
GET /api/v2/admin/products/display/setting
PUT /api/v2/admin/products/display/setting
```

### Products display setting property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| sorting_options | 상품정렬조건 new_product : 신상품 product_name : 상품명 low_price : 낮은가격 high_price : 높은가격 manufacture : 제조사 popular_product : 인기상품 review : 사용후기 hit_count : 조회수 like_count : 좋아요 |

### List all products display setting   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 읽기권한 (mall.read_store) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |

```bash
List all products display setting        List all products display setting       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/products/display/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "product": {        "shop_no": 1,        "sorting_options": [            "new_product",            "product_name",            "low_price",            "high_price",            "manufacture",            "review"        ]    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/products/display/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "product": {        "shop_no": 1,        "sorting_options": [            "new_product",            "product_name",            "low_price",            "high_price",            "manufacture",            "review"        ]    }}
```

### Update a products display setting   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 쓰기권한 (mall.write_store) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| sorting_optionsRequired | 상품정렬조건   new_product : 신상품 product_name : 상품명 low_price : 낮은가격 high_price : 높은가격 manufacture : 제조사 popular_product : 인기상품 review : 사용후기 hit_count : 조회수 like_count : 좋아요 |

```bash
Update a products display setting        Update a products display setting       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/products/display/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "sorting_options": [            "new_product",            "product_name",            "low_price",            "high_price",            "manufacture",            "review"        ]    }}'    Response  Copy     {    "product": {        "shop_no": 1,        "sorting_options": [            "new_product",            "product_name",            "low_price",            "high_price",            "manufacture",            "review"        ]    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/products/display/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "sorting_options": [            "new_product",            "product_name",            "low_price",            "high_price",            "manufacture",            "review"        ]    }}'
```

```json
{    "product": {        "shop_no": 1,        "sorting_options": [            "new_product",            "product_name",            "low_price",            "high_price",            "manufacture",            "review"        ]    }}
```
