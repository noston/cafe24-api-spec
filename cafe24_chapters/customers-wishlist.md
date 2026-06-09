# CUSTOMERS WISHLIST


## Customers wishlist

```json
Endpoints    GET /api/v2/admin/customers/{member_id}/wishlist/count
GET /api/v2/admin/customers/{member_id}/wishlist
```

```json
GET /api/v2/admin/customers/{member_id}/wishlist/count
GET /api/v2/admin/customers/{member_id}/wishlist
```

### Customers wishlist property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호. |
| wishlist_no | 관심상품번호 |
| product_no | 상품번호 |
| variant_code형식 : [A-Z0-9]글자수 최소: [12자]~최대: [12자] | 품목코드 시스템이 품목에 부여한 코드. 해당 쇼핑몰 내에서 품목 코드는 중복되지 않음. |
| additional_option | 추가입력 옵션 |
| attached_file_option | 파일 첨부 옵션 |
| price | 상품 판매가 상품의 판매 가격. 쿠폰 및 혜택을 적용하기 전의 가격. 상품 등록시엔 모든 멀티 쇼핑몰에 동일한 가격으로 등록하며, 멀티쇼핑몰별로 다른 가격을 입력하고자 할 경우 상품 수정을 통해 가격을 다르게 입력할 수 있다. ※ 판매가 = [ 공급가 + (공급가 * 마진율) + 추가금액 ] |
| product_bundle | 세트상품 여부 |
| created_date | 담은일자 관심상품을 담은 일자 |
| price_content최대글자수 : [20자] | 판매가 대체문구 |

### Retrieve a count of products in customer wishlist   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 개인화정보 읽기권한 (mall.read_personal) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| member_idRequired | 회원아이디 |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |

```bash
Retrieve a count of products in customer wishlist        Retrieve a count of products in customer wishlist       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Retrieve a list of products in customer wishlist   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 개인화정보 읽기권한 (mall.read_personal) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| member_idRequired | 회원아이디 |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |

```bash
Retrieve a list of products in customer wishlist        Retrieve a list of products in customer wishlist Retrieve wishlist with fields parameter       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
