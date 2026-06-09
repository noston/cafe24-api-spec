# ORDERS RECEIVERS HISTORY


## Orders receivers history

```json
Endpoints    GET /api/v2/admin/orders/{order_id}/receivers/history
```

```json
GET /api/v2/admin/orders/{order_id}/receivers/history
```

### Orders receivers history property list

| Attribute | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호 |
| name | 수령자명 |
| phone | 전화번호 |
| cellphone | 수령자 휴대 전화 |
| zipcode | 우편번호 |
| address1 | 기본 주소 |
| address2 | 상세 주소 |
| address_state | 주/도 |
| address_city | 시/군/도시 |
| address_street | 도로명 |
| address_full | 전체주소 |
| name_en | 수령자명 (영문) |
| city_en | 수령자 도시 (영문) |
| state_en | 수령자 주 (영문) |
| street_en | 수령자 주소 (영문) |
| country_code | 국가코드 |
| country_name | 국가명 |
| country_name_en | 국가명 (영문) |
| shipping_message | 배송 메세지 |
| updated_date | 수정일 |
| user_id | 주문자 수정자 ID |
| user_name | 주문자 수정자 명 |
| shipping_code | 배송번호 |

### Retrieve a list of recipient history of an order   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 읽기권한 (mall.read_order) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| order_idRequired주문번호 | 주문번호 |

```bash
Retrieve a list of recipient history of an order        Retrieve a list of recipient history of an order Retrieve history with fields parameter       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
