# PRODUCTS MEMOS


## Products memos

```json
Endpoints    GET /api/v2/admin/products/{product_no}/memos
GET /api/v2/admin/products/{product_no}/memos/{memo_no}
POST /api/v2/admin/products/{product_no}/memos
PUT /api/v2/admin/products/{product_no}/memos/{memo_no}
DELETE /api/v2/admin/products/{product_no}/memos/{memo_no}
```

```json
GET /api/v2/admin/products/{product_no}/memos
GET /api/v2/admin/products/{product_no}/memos/{memo_no}
POST /api/v2/admin/products/{product_no}/memos
PUT /api/v2/admin/products/{product_no}/memos/{memo_no}
DELETE /api/v2/admin/products/{product_no}/memos/{memo_no}
```

### Products memos property list

| Attribute | Description |
| --- | --- |
| memo_no | 메모 번호 시스템에서 부여한 상품 메모의 고유한 번호. 상품 메모 번호는 쇼핑몰 내에서 중복되지 않는다. |
| author_id최대글자수 : [20자] | 작성자 아이디 메모를 작성한 관리자의 아이디 정보. |
| created_date | 생성일 메모를 작성한 시간. |
| memo | 메모 메모의 내용. HTML을 사용하여 등록할 수 있다. |

### Retrieve a list of product memos   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 읽기권한 (mall.read_product) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| product_noRequired | 상품번호   시스템에서 부여한 상품의 번호. 상품 번호는 쇼핑몰 내에서 중복되지 않는다. |
| offset최대값: [8000] | 조회결과 시작위치   DEFAULT 0 |
| limit최소: [1]~최대: [100] | 조회결과 최대건수   조회하고자 하는 최대 건수를 지정할 수 있음. 예) 10 입력시 10건만 표시함.   DEFAULT 10 |

```bash
Retrieve a list of product memos        Retrieve a list of product memos Retrieve memos using paging Retrieve memos with fields parameter       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Retrieve a product memo   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 읽기권한 (mall.read_product) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| product_noRequired | 상품번호   시스템에서 부여한 상품의 번호. 상품 번호는 쇼핑몰 내에서 중복되지 않는다. |
| memo_noRequired | 메모 번호   시스템에서 부여한 상품 메모의 고유한 번호. 상품 메모 번호는 쇼핑몰 내에서 중복되지 않는다. |

```bash
Retrieve a product memo        Retrieve a product memo Retrieve a product memo with fields parameter       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Create a product memo   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 쓰기권한 (mall.write_product) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| product_noRequired | 상품번호   시스템에서 부여한 상품의 번호. 상품 번호는 쇼핑몰 내에서 중복되지 않는다. |
| author_idRequired최대글자수 : [20자] | 작성자 아이디   메모를 작성한 관리자의 아이디 정보. |
| memoRequired | 메모   메모의 내용. HTML을 사용하여 등록할 수 있다. |

```bash
Create a product memo        Create a product memo Post a product memo Try posting a product memo without author_id field Try posting a product memo without memo field       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Update a product memo   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 쓰기권한 (mall.write_product) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| product_noRequired | 상품번호   시스템에서 부여한 상품의 번호. 상품 번호는 쇼핑몰 내에서 중복되지 않는다. |
| memo_noRequired | 메모 번호   시스템에서 부여한 상품 메모의 고유한 번호. 상품 메모 번호는 쇼핑몰 내에서 중복되지 않는다. |
| author_idRequired최대글자수 : [20자] | 작성자 아이디   메모를 작성한 관리자의 아이디 정보. |
| memoRequired | 메모   메모의 내용. HTML을 사용하여 등록할 수 있다. |

```bash
Update a product memo        Update a product memo       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Delete a product memo   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 쓰기권한 (mall.write_product) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| product_noRequired | 상품번호   시스템에서 부여한 상품의 번호. 상품 번호는 쇼핑몰 내에서 중복되지 않는다. |
| memo_noRequired | 메모 번호   시스템에서 부여한 상품 메모의 고유한 번호. 상품 메모 번호는 쇼핑몰 내에서 중복되지 않는다. |

```bash
Delete a product memo        Delete a product memo       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
