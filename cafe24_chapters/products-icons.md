# PRODUCTS ICONS


## Products icons

```json
Endpoints    GET /api/v2/admin/products/{product_no}/icons
POST /api/v2/admin/products/{product_no}/icons
PUT /api/v2/admin/products/{product_no}/icons
DELETE /api/v2/admin/products/{product_no}/icons/{code}
```

```json
GET /api/v2/admin/products/{product_no}/icons
POST /api/v2/admin/products/{product_no}/icons
PUT /api/v2/admin/products/{product_no}/icons
DELETE /api/v2/admin/products/{product_no}/icons/{code}
```

### Products icons property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| use_show_date | 표시기간 사용 여부 T : 사용함 F : 사용안함 |
| show_start_date | 표시기간 시작 일자 |
| show_end_date | 표시기간 종료 일자 |
| image_list | 상품 아이콘 리스트 |
| code | 상품 아이콘 코드 |

### Retrieve a list of product icons   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 읽기권한 (mall.read_product) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| product_noRequired | 상품번호 |

```bash
Retrieve a list of product icons        Retrieve a list of product icons Retrieve icons with fields parameter       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Set icons for a product   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 쓰기권한 (mall.write_product) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| product_noRequired | 상품번호 |
| image_listRequired배열 최대사이즈: [5] | 상품 아이콘 리스트 |
| image_list 하위 요소 보기     codeRequired상품 아이콘 코드 |

```bash
Set icons for a product        Set icons for a product Try selecting product icons without image_list field Set an icon to a product by using only required fields Try setting an icon to a product by without using image_list fields       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Update product icons   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 쓰기권한 (mall.write_product) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| product_noRequired | 상품번호 |
| use_show_date | 표시기간 사용 여부   T : 사용함 F : 사용안함 |
| show_start_date날짜 | 표시기간 시작 일자 |
| show_end_date날짜 | 표시기간 종료 일자 |
| image_list배열 최대사이즈: [5] | 상품 아이콘 리스트 |
| image_list 하위 요소 보기     codeRequired상품 아이콘 코드 |

```bash
Update product icons        Update product icons Update icons of the product Update display dates of icons       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Remove a product icon   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 쓰기권한 (mall.write_product) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| product_noRequired | 상품번호 |
| codeRequired | 상품 아이콘 코드 |

```bash
Remove a product icon        Remove a product icon       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

## Products icons

```json
Endpoints    GET /api/v2/admin/products/icons
```

```json
GET /api/v2/admin/products/icons
```

### Products icons property list

| Attribute | Description |
| --- | --- |
| code | 아이콘 코드 |
| path | 아이콘 URL |

### Retrieve a list of icons   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 읽기권한 (mall.read_product) |
| 호출건수 제한 | 40 |

```bash
Retrieve a list of icons        Retrieve a list of icons Retrieve icons with fields parameter       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/products/icons' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "icons": [        {            "code": "icon_01_01",            "path": "https://img.echosting.cafe24.com/icon/product/ko_KR/icon_01_01.gif"        },        {            "code": "icon_02_01",            "path": "https://img.echosting.cafe24.com/icon/product/ko_KR/icon_02_01.gif"        },        {            "code": "icon_05_01",            "path": "https://img.echosting.cafe24.com/icon/product/ko_KR/icon_05_01.gif"        },        {            "code": "custom_1",            "path": "https://{domain}/web/upload/custom_115855429954932.gif"        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/products/icons' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "icons": [        {            "code": "icon_01_01",            "path": "https://img.echosting.cafe24.com/icon/product/ko_KR/icon_01_01.gif"        },        {            "code": "icon_02_01",            "path": "https://img.echosting.cafe24.com/icon/product/ko_KR/icon_02_01.gif"        },        {            "code": "icon_05_01",            "path": "https://img.echosting.cafe24.com/icon/product/ko_KR/icon_05_01.gif"        },        {            "code": "custom_1",            "path": "https://{domain}/web/upload/custom_115855429954932.gif"        }    ]}
```
