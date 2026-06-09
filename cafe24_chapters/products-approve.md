# PRODUCTS APPROVE


## Products approve

```json
Endpoints    GET /api/v2/admin/products/{product_no}/approve
POST /api/v2/admin/products/{product_no}/approve
PUT /api/v2/admin/products/{product_no}/approve
```

```json
GET /api/v2/admin/products/{product_no}/approve
POST /api/v2/admin/products/{product_no}/approve
PUT /api/v2/admin/products/{product_no}/approve
```

### Products approve property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호. |
| status Required | 상태 공급사가 승인 요청한 해당 상품의 승인 상태 N : 승인요청 (신규상품) 상태값 E : 승인요청 (상품수정) 상태값 C : 승인완료 상태값 R : 승인거절 상태값 I : 검수진행중 상태값 Empty Value : 요청된적 없음 |
| product_no Required | 상품번호 시스템에서 부여한 상품의 번호. 상품 번호는 쇼핑몰 내에서 중복되지 않는다. |

### Retrieve a product approval status   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 읽기권한 (mall.read_product) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호.   DEFAULT 1 |
| product_noRequired | 상품번호   상품의 고유한 일련 번호. 해당 쇼핑몰 내에서 상품 번호는 중복되지 않음. |

```bash
Retrieve a product approval status        Retrieve a product approval status       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Create a product approval request   cafe24

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
| product_noRequired | 상품번호   시스템에서 부여한 상품의 번호. 상품 번호는 쇼핑몰 내에서 중복되지 않는다. |
| user_idRequired | 공급사 운영자 아이디   승인 요청한 공급사의 아이디 |

```bash
Create a product approval request        Create a product approval request       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Update a product approval status   cafe24

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
| product_noRequired | 상품번호   시스템에서 부여한 상품의 번호. 상품 번호는 쇼핑몰 내에서 중복되지 않는다. |
| user_idRequired | 공급사 운영자 아이디   승인 요청한 공급사의 아이디 |
| statusRequired | 상태   공급사가 승인 요청한 해당 상품의 승인 상태   C : 승인완료 상태값 R : 승인거절 상태값 I : 검수진행중 상태값 |

```bash
Update a product approval status        Update a product approval status       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
