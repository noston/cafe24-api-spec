# CATEGORIES PRODUCTS


## Categories products

```json
Endpoints    GET /api/v2/admin/categories/{category_no}/products
GET /api/v2/admin/categories/{category_no}/products/count
POST /api/v2/admin/categories/{category_no}/products
PUT /api/v2/admin/categories/{category_no}/products
DELETE /api/v2/admin/categories/{category_no}/products/{product_no}
```

```json
GET /api/v2/admin/categories/{category_no}/products
GET /api/v2/admin/categories/{category_no}/products/count
POST /api/v2/admin/categories/{category_no}/products
PUT /api/v2/admin/categories/{category_no}/products
DELETE /api/v2/admin/categories/{category_no}/products/{product_no}
```

### Categories products property list

| Attribute | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호 |
| product_no | 상품번호 상품의 고유한 일련 번호. 해당 쇼핑몰 내에서 상품 번호는 중복되지 않음. |
| sequence_no | 표시 순서 |
| auto_sort | 자동 정렬 여부 |
| sold_out | 품절여부 |
| fixed_sort | 고정 여부 |
| not_for_sale | 판매안함 여부 |
| display_group최소: [1]~최대: [3] | 상세 상품분류 1 : 일반상품 2 : 추천상품 3 : 신상품 DEFAULT 1 |
| sequence최소: [1]~최대: [999998] | 진열 순서 |

### Retrieve a list of products by category   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 읽기권한 (mall.read_product) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| category_noRequired | 분류 번호 |
| display_groupRequired최소: [1]~최대: [3] | 상세 상품분류   1 : 일반상품 2 : 추천상품 3 : 신상품 |
| limit최소: [1]~최대: [50000] | 조회결과 최대건수   DEFAULT 50000 |

```bash
Retrieve a list of products by category        Retrieve a list of products by category Retrieve mobile disaplayed products of the category Retrieve products of the category using limit parameter Retrieve product_no and product name of products using fields parameter       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Retrieve a count of products by category   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 읽기권한 (mall.read_product) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| category_noRequired | 분류 번호 |
| display_groupRequired최소: [1]~최대: [3] | 상세 상품분류   1 : 일반상품 2 : 추천상품 3 : 신상품 |

```bash
Retrieve a count of products by category        Retrieve a count of products by category       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Add products to a category   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 쓰기권한 (mall.write_product) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| category_noRequired | 분류 번호 |
| display_group최소: [1]~최대: [3] | 상세 상품분류   1 : 일반상품 2 : 추천상품 3 : 신상품   DEFAULT 1 |
| product_noRequired | 상품번호 |

```bash
Add products to a category        Add products to a category Post a product in the category Try posting a product in the category without product_no Add products to a certain category by using only required fields Try adding products to a certain category by without product_no field       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Update a product in product category   cafe24 youtube

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
| category_noRequired | 분류 번호 |
| display_groupRequired최소: [1]~최대: [3] | 상세 상품분류   1 : 일반상품 2 : 추천상품 3 : 신상품 |
| product_noRequired | 상품번호 |
| sequence최소: [1]~최대: [999999] | 진열 순서 |
| auto_sort | 자동 정렬 여부   T : 자동 정렬 사용함 F : 자동 정렬 사용안함 |
| fixed_sort | 고정 여부   T : 진열순위 고정 사용함 F : 진열순위 고정 사용안함 |

```bash
Update a product in product category        Update a product in product category       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Delete a product by category   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 쓰기권한 (mall.write_product) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| category_noRequired | 분류 번호 |
| product_noRequired | 상품번호 |
| display_group최소: [1]~최대: [3] | 상세 상품분류   일반상품 영역에서 진열안함 처리 시, 추천상품/신상품 영역에서도 동시에 진열안함 처리된다.   1 : 일반상품 2 : 추천상품 3 : 신상품   DEFAULT 1 |

```bash
Delete a product by category        Delete a product by category       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
