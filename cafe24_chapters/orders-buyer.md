# ORDERS BUYER


## Orders buyer

```json
Endpoints    GET /api/v2/admin/orders/{order_id}/buyer
PUT /api/v2/admin/orders/{order_id}/buyer
```

```json
GET /api/v2/admin/orders/{order_id}/buyer
PUT /api/v2/admin/orders/{order_id}/buyer
```

### Orders buyer property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호. |
| member_id | 회원아이디 |
| member_group_no | 주문당시 주문자 회원 등급 번호 |
| name | 주문자명 |
| names_furigana | 주문자 이름 후리가나 |
| email | 주문자 이메일 해당 회원의 이메일 |
| phone | 주문자 일반 전화 |
| cellphone | 주문자 휴대 전화 |
| customer_notification | 고객 알림 고객에게 알릴 문구 |
| updated_date | 수정일 |
| user_id | 주문자 수정자 ID 주문자정보를 수정한 사람의 ID |
| user_name | 주문자 수정자 명 주문자정보를 수정한 사람의 이름 |
| company_name | 상호명 |
| company_registration_no | 사업자등록번호 |
| buyer_zipcode | 주문자 우편번호 |
| buyer_address1 | 주문자 기본주소 |
| buyer_address2 | 주문자 상세주소 |
| order_id주문번호 | 주문번호 |

### Retrieve customer details of an order   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 읽기권한 (mall.read_order) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| order_idRequired주문번호 | 주문번호 |

```bash
Retrieve customer details of an order        Retrieve customer details of an order Retrieve buyer with fields parameter       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Update customer information of an order   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 쓰기권한 (mall.write_order) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호.   DEFAULT 1 |
| order_idRequired주문번호 | 주문번호 |
| name | 주문자명 |
| email이메일 | 주문자 이메일   해당 회원의 이메일 |
| phone | 주문자 일반 전화 |
| cellphone | 주문자 휴대 전화 |
| customer_notification | 고객 알림   고객에게 알릴 문구 |

```bash
Update customer information of an order        Update customer information of an order       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
