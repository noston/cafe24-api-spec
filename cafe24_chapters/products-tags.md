# PRODUCTS TAGS


## Products tags

```json
Endpoints    GET /api/v2/admin/products/{product_no}/tags
GET /api/v2/admin/products/{product_no}/tags/count
POST /api/v2/admin/products/{product_no}/tags
DELETE /api/v2/admin/products/{product_no}/tags/{tag}
```

```json
GET /api/v2/admin/products/{product_no}/tags
GET /api/v2/admin/products/{product_no}/tags/count
POST /api/v2/admin/products/{product_no}/tags
DELETE /api/v2/admin/products/{product_no}/tags/{tag}
```

### Products tags property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호. |
| tags Required | 상품 태그 |
| product_no | 상품번호 시스템에서 부여한 상품의 번호. 상품 번호는 쇼핑몰 내에서 중복되지 않는다. |
| tag | 상품 태그 검색 또는 분류를 위하여 상품에 입력하는 검색어 정보(해시태그) |

### Retrieve a list of a product's product tags   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 읽기권한 (mall.read_product) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호.   DEFAULT 1 |
| product_noRequired | 상품번호   시스템에서 부여한 상품의 번호. 상품 번호는 쇼핑몰 내에서 중복되지 않는다. |

```bash
Retrieve a list of a product's product tags        Retrieve a list of a product's product tags Retrieve tags with fields parameter       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Retrieve a count of a product's product tags   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 읽기권한 (mall.read_product) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호.   DEFAULT 1 |
| product_noRequired | 상품번호   시스템에서 부여한 상품의 번호. 상품 번호는 쇼핑몰 내에서 중복되지 않는다. |

```bash
Retrieve a count of a product's product tags        Retrieve a count of a product's product tags       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Create product tags   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 쓰기권한 (mall.write_product) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호.   DEFAULT 1 |
| shop_no | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호.   DEFAULT 1 |
| product_noRequired | 상품번호   시스템에서 부여한 상품의 번호. 상품 번호는 쇼핑몰 내에서 중복되지 않는다. |
| tagsRequired배열 최대사이즈: [100] | 상품 태그   쇼핑 큐레이션 사용 시 - 배열 최대사이즈 : [100] |

```bash
Create product tags        Create product tags Post a product tag Try posting a product tag without tags field       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Delete a product tag   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 쓰기권한 (mall.write_product) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호.   DEFAULT 1 |
| product_noRequired | 상품번호   시스템에서 부여한 상품의 번호. 상품 번호는 쇼핑몰 내에서 중복되지 않는다. |
| tag | 상품 태그   검색 또는 분류를 위하여 상품에 입력하는 검색어 정보(해시태그) |

```bash
Delete a product tag        Delete a product tag       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
