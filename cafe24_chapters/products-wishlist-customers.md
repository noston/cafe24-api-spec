# PRODUCTS WISHLIST CUSTOMERS


## Products wishlist customers

```json
Endpoints    GET /api/v2/admin/products/{product_no}/wishlist/customers
GET /api/v2/admin/products/{product_no}/wishlist/customers/count
```

```json
GET /api/v2/admin/products/{product_no}/wishlist/customers
GET /api/v2/admin/products/{product_no}/wishlist/customers/count
```

### Products wishlist customers property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| member_id | 회원아이디 |

### Retrieve a list of customers with a product in wishlist   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 개인정보 읽기권한 (mall.read_privacy) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| product_noRequired | 상품번호   상품의 고유한 일련 번호. 해당 쇼핑몰 내에서 상품 번호는 중복되지 않음. |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |

```bash
Retrieve a list of customers with a product in wishlist        Retrieve a list of customers with a product in wishlist       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Retrieve a count of customers with a product in wishlist   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 개인정보 읽기권한 (mall.read_privacy) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| product_noRequired | 상품번호 |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |

```bash
Retrieve a count of customers with a product in wishlist        Retrieve a count of customers with a product in wishlist       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
