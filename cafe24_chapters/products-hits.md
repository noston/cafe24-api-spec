# PRODUCTS HITS


## Products hits

```json
Endpoints    GET /api/v2/admin/products/{product_no}/hits/count
```

```json
GET /api/v2/admin/products/{product_no}/hits/count
```

### Retrieve a count of product views   cafe24 youtube

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
Retrieve a count of product views        Retrieve a count of product views       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
