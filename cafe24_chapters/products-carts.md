# PRODUCTS CARTS


## Products carts

```json
Endpoints    GET /api/v2/admin/products/{product_no}/carts/count
GET /api/v2/admin/products/{product_no}/carts
```

```json
GET /api/v2/admin/products/{product_no}/carts/count
GET /api/v2/admin/products/{product_no}/carts
```

### Products carts property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| member_id | 회원아이디 |
| created_date | 담은일자 |
| product_no | 상품번호 |
| variant_code | 상품 품목 코드 |
| quantity | 수량 |
| product_bundle | 세트상품 여부 T : 세트상품 F : 세트상품 아님 |

### Retrieve a count of carts containing a product   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 개인화정보 읽기권한 (mall.read_personal) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호.   DEFAULT 1 |
| product_noRequired | 상품번호   시스템에서 부여한 상품의 번호. 상품 번호는 쇼핑몰 내에서 중복되지 않는다. |

```bash
Retrieve a count of carts containing a product        Retrieve a count of carts containing a product       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Retrieve a list of carts containing a product   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 개인화정보 읽기권한 (mall.read_personal) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| product_noRequired | 상품번호 |
| limit최소: [1]~최대: [100] | 조회결과 최대건수   DEFAULT 10 |
| offset최대값: [10000] | 조회결과 시작위치   DEFAULT 0 |

```bash
Retrieve a list of carts containing a product        Retrieve a list of carts containing a product Retrieve carts with fields parameter Retrieve carts using paging       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
