# MAINS PRODUCTS


## Mains products

```json
Endpoints    GET /api/v2/admin/mains/{display_group}/products
GET /api/v2/admin/mains/{display_group}/products/count
POST /api/v2/admin/mains/{display_group}/products
PUT /api/v2/admin/mains/{display_group}/products
DELETE /api/v2/admin/mains/{display_group}/products/{product_no}
```

```json
GET /api/v2/admin/mains/{display_group}/products
GET /api/v2/admin/mains/{display_group}/products/count
POST /api/v2/admin/mains/{display_group}/products
PUT /api/v2/admin/mains/{display_group}/products
DELETE /api/v2/admin/mains/{display_group}/products/{product_no}
```

### Mains products property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호. |
| product_no | 상품번호 |
| product_name | 상품명 |
| fixed_sort | 고정 여부 |
| fix_product_no | 진열순위 고정 상품번호 |

### Retrieve a list of products in main category   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 읽기권한 (mall.read_product) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| display_groupRequired | 메인분류 번호 |

```bash
Retrieve a list of products in main category        Retrieve a list of products in main category Retrieve mobile disaplayed products of the main category Retrieve products of the main category using fields parameter       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Retrieve a count of products in main category   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 읽기권한 (mall.read_product) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| display_groupRequired | 메인분류 번호 |

```bash
Retrieve a count of products in main category        Retrieve a count of products in main category       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Set main category products   cafe24 youtube

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
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| display_groupRequired | 메인분류 번호 |
| product_noRequired | 상품번호 |

```bash
Set main category products        Set main category products Post a product in the mains category Try posting a product in the mains category without product_no       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Update fixed sorting of products in main category   cafe24 youtube

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
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| display_groupRequired | 메인분류 번호 |
| product_noRequired | 상품번호   요청한 상품번호의 순서 대로 진열순위가 지정 |
| fix_product_no | 진열순위 고정 상품번호   진열순위를 고정하고자 하는 상품번호를 지정 |

```bash
Update fixed sorting of products in main category        Update fixed sorting of products in main category       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Delete a product in main category   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 쓰기권한 (mall.write_product) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| display_groupRequired | 메인분류 번호 |
| product_noRequired | 상품번호 |

```bash
Delete a product in main category        Delete a product in main category       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
