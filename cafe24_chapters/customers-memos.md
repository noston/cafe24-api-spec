# CUSTOMERS MEMOS


## Customers memos

```json
Endpoints    GET /api/v2/admin/customers/{member_id}/memos/count
GET /api/v2/admin/customers/{member_id}/memos
GET /api/v2/admin/customers/{member_id}/memos/{memo_no}
POST /api/v2/admin/customers/{member_id}/memos
PUT /api/v2/admin/customers/{member_id}/memos/{memo_no}
DELETE /api/v2/admin/customers/{member_id}/memos/{memo_no}
```

```json
GET /api/v2/admin/customers/{member_id}/memos/count
GET /api/v2/admin/customers/{member_id}/memos
GET /api/v2/admin/customers/{member_id}/memos/{memo_no}
POST /api/v2/admin/customers/{member_id}/memos
PUT /api/v2/admin/customers/{member_id}/memos/{memo_no}
DELETE /api/v2/admin/customers/{member_id}/memos/{memo_no}
```

### Customers memos property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| memo_no | 메모 번호 시스템에서 부여한 상품 메모의 고유한 번호. 상품 메모 번호는 쇼핑몰 내에서 중복되지 않는다. |
| author_id | 작성자 아이디 메모를 작성한 관리자의 아이디 정보. |
| memo | 메모 내용 메모의 내용. HTML을 사용하여 등록할 수 있다. |
| important_flag | 중요 메모 여부 중요 메모의 구분여부. T : 중요 메모 F : 일반 메모 |
| created_date | 생성일 메모를 작성한 시간. |

### Retrieve a count of customer memos   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 회원 읽기권한 (mall.read_customer) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호.   DEFAULT 1 |
| member_idRequired | 회원아이디 |

```bash
Retrieve a count of customer memos        Retrieve a count of customer memos       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Retrieve a list of customer memos   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 회원 읽기권한 (mall.read_customer) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| member_idRequired | 회원아이디 |
| start_date날짜 | 검색 시작일 |
| end_date날짜 | 검색 종료일 |
| important_flag | 중요 메모 여부   T : 중요 메모 F : 일반 메모 |
| memo | 메모 |
| offset최대값: [10000] | 조회결과 시작위치   DEFAULT 0 |
| limit최소: [1]~최대: [100] | 조회결과 최대건수   DEFAULT 10 |

```bash
Retrieve a list of customer memos        Retrieve a list of customer memos Retrieve memos with fields parameter Retrieve memos using paging       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Retrieve a customer memo   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 회원 읽기권한 (mall.read_customer) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| memo_noRequired | 메모 번호   시스템에서 부여한 상품 메모의 고유한 번호. 상품 메모 번호는 쇼핑몰 내에서 중복되지 않는다. |
| member_idRequired | 회원아이디 |

```bash
Retrieve a customer memo        Retrieve a customer memo Retrieve a customer memo with fields parameter       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Create a customer memo   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 회원 쓰기권한 (mall.write_customer) |
| 호출건수 제한 | 30 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| member_idRequired | 회원아이디 |
| author_idRequired최대글자수 : [20자] | 작성자 아이디   메모를 작성한 관리자의 아이디 정보. |
| memoRequired | 메모   메모의 내용. HTML을 사용하여 등록할 수 있다. |
| important_flag | 중요 메모 여부   중요 메모의 구분여부.   T : 중요 메모 F : 일반 메모   DEFAULT F |

```bash
Create a customer memo        Create a customer memo Post a memo of a customer using only author_id and memo fields Try posting a memo of a customer without using author_id field Try posting a memo of a customer without using memo field       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Update a customer memo   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 회원 쓰기권한 (mall.write_customer) |
| 호출건수 제한 | 30 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| memo_noRequired | 메모 번호   시스템에서 부여한 상품 메모의 고유한 번호. 상품 메모 번호는 쇼핑몰 내에서 중복되지 않는다. |
| member_idRequired | 회원아이디 |
| author_idRequired최대글자수 : [20자] | 작성자 아이디   메모를 작성한 관리자의 아이디 정보. |
| memo | 메모   메모의 내용. HTML을 사용하여 등록할 수 있다. |
| important_flag | 중요 메모 여부   중요 메모의 구분여부.   T : 중요 메모 F : 일반 메모 |

```bash
Update a customer memo        Update a customer memo       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Delete a customer memo   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 회원 쓰기권한 (mall.write_customer) |
| 호출건수 제한 | 30 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| memo_noRequired | 메모 번호   시스템에서 부여한 상품 메모의 고유한 번호. 상품 메모 번호는 쇼핑몰 내에서 중복되지 않는다. |
| member_idRequired | 회원아이디 |

```bash
Delete a customer memo        Delete a customer memo       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
