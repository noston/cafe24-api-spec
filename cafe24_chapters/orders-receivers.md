# ORDERS RECEIVERS


## Orders receivers

```json
Endpoints    GET /api/v2/admin/orders/{order_id}/receivers
PUT /api/v2/admin/orders/{order_id}/receivers
PUT /api/v2/admin/orders/{order_id}/receivers/{shipping_code}
```

```json
GET /api/v2/admin/orders/{order_id}/receivers
PUT /api/v2/admin/orders/{order_id}/receivers
PUT /api/v2/admin/orders/{order_id}/receivers/{shipping_code}
```

### Orders receivers property list

| Attribute | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호 멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호. DEFAULT 1 |
| name | 수령자명 |
| name_furigana | 수령자명 (발음) |
| phone | 전화번호 |
| cellphone | 수령자 휴대 전화 |
| virtual_phone_no | 수령자 안심번호 |
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
| clearance_information_type | 통관정보 유형 I : 신분증 ID P : 여권번호 C : 개인통관고유부호 |
| clearance_information | 통관정보 |
| wished_delivery_date | 희망배송일 |
| wished_delivery_time | 희망배송시간 |
| shipping_code | 배송번호 |
| change_default_shipping_address | 기본배송지 변경 여부 T : 변경함 F : 변경안함 |
| use_fast_delivery_date | 가능한 빠른 배송일 설정 여부 T: 사용함 F: 사용안함 |
| use_fast_delivery_time | 가능한 빠른 배송시간 설정 여부 T: 사용함 F: 사용안함 |

### Retrieve a list of recipients of an order   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 읽기권한 (mall.read_order) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호.   DEFAULT 1 |
| order_idRequired주문번호 | 주문번호 |
| shipping_code | 배송번호   ,(콤마)로 여러 건을 검색할 수 있다. |

```bash
Retrieve a list of recipients of an order        Retrieve a list of recipients of an order       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Update order recipients   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 쓰기권한 (mall.write_order) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 100 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| order_idRequired주문번호 | 주문번호 |
| name최대글자수 : [20자] | 수령자명 |
| phone최대글자수 : [20자] | 수령자 일반 전화   한국몰일 경우 02-0000-0000 형태로 입력 그외 해외몰일 경우 국가번호-000-0000 형태로 입력 |
| cellphone최대글자수 : [20자] | 수령자 휴대 전화   한국몰일 경우 010-0000-0000 형태로 입력 그외 해외몰일 경우 국가번호-000-0000 형태로 입력 |
| shipping_message | 배송 메세지 |
| name_furigana | 수령자명 (발음)   Youtube shopping 이용 시에는 미제공   해외몰 중 일본몰인 경우에만 필수 입력 |
| zipcode최소글자수 : [2자]최대글자수 : [14자] | 우편번호 |
| address1최대글자수 : [255자] | 기본 주소 |
| address2최대글자수 : [255자] | 상세 주소 |
| address_state | 주/도   해외몰인 경우 필수 입력 |
| address_city | 시/군/도시   해외몰인 경우 필수 입력 |
| name_en | 수령자명 (영문) |
| city_en | 수령자 도시 (영문) |
| state_en | 수령자 주 (영문) |
| street_en | 수령자 주소 (영문) |
| country_code | 국가코드   해외몰인 경우 필수 입력 한국 : KR / 중국: CN / 일본: JP / 필리핀: PH / 미국: US / 대만: TW / 베트남 : VN |
| clearance_information_type | 통관정보 유형   I : 신분증 ID P : 여권번호 C : 개인통관고유부호 |
| clearance_information | 통관정보 |
| shipping_code | 배송번호 |
| change_default_shipping_address | 기본배송지 변경 여부   T : 변경함 F : 변경안함   DEFAULT F |
| virtual_phone_no | 수령자 안심번호   Youtube shopping 이용 시에는 미제공   복수 배송지 주문일 경우 수령자 안심번호 수정 불가 |
| wished_delivery_date날짜 | 희망배송일   Youtube shopping 이용 시에는 미제공 |
| use_fast_delivery_date | 가능한 빠른 배송일 설정 여부   Youtube shopping 이용 시에는 미제공   가능한 빠른 배송시간 설정 여부'가 'T' 일때는 null 로 응답함   T: 사용함 F: 사용안함 |
| wished_delivery_time | 희망배송시간   Youtube shopping 이용 시에는 미제공   희망배송 시작시간(start_hour) 00~23 까지 입력 가능  희망배송 종료시간(end_hour) 00~23 까지 입력 가능 |
| wished_delivery_time 하위 요소 보기     start_hour희망배송 시작시간 end_hour희망배송 종료시간 |
| use_fast_delivery_time | 가능한 빠른 배송시간 설정 여부   가능한 빠른 배송일 설정 여부'가 'T' 일때는 null 로 응답함   T: 사용함 F: 사용안함 |

```bash
Update order recipients        Update order recipients       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Change shipping information   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 쓰기권한 (mall.write_order) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| order_idRequired주문번호 | 주문번호 |
| shipping_codeRequired | 배송번호 |
| name최대글자수 : [20자] | 수령자명 |
| phone최대글자수 : [20자] | 수령자 일반 전화 |
| cellphone최대글자수 : [20자] | 수령자 휴대 전화 |
| shipping_message | 배송 메세지 |
| name_furigana | 수령자명 (발음) |
| zipcode최소글자수 : [2자]최대글자수 : [14자] | 우편번호 |
| address1최대글자수 : [255자] | 기본 주소 |
| address2최대글자수 : [255자] | 상세 주소 |
| address_state | 주/도 |
| address_city | 시/군/도시 |
| name_en | 수령자명 (영문) |
| city_en | 수령자 도시 (영문) |
| state_en | 수령자 주 (영문) |
| street_en | 수령자 주소 (영문) |
| country_code | 국가코드 |
| clearance_information_type | 통관정보 유형   I : 신분증 ID P : 여권번호 C : 개인통관고유부호 |
| clearance_information | 통관정보 |
| change_default_shipping_address | 기본배송지 변경 여부   T : 변경함 F : 변경안함   DEFAULT F |
| virtual_phone_no | 수령자 안심번호   복수 배송지 주문일 경우 수령자 안심번호 수정 불가 |
| wished_delivery_date날짜 | 희망배송일 |
| use_fast_delivery_date | 가능한 빠른 배송일 설정 여부   가능한 빠른 배송시간 설정 여부'가 'T' 일때는 null 로 응답함   T: 사용함 F: 사용안함 |
| wished_delivery_time | 희망배송시간   희망배송 시작시간(start_hour) 00~23 까지 입력 가능  희망배송 종료시간(end_hour) 00~23 까지 입력 가능 |
| wished_delivery_time 하위 요소 보기     start_hour희망배송 시작시간 end_hour희망배송 종료시간 |
| use_fast_delivery_time | 가능한 빠른 배송시간 설정 여부   가능한 빠른 배송일 설정 여부'가 'T' 일때는 null 로 응답함   T: 사용함 F: 사용안함 |
| receiver_direct_input_check | 주소 직접입력 |

```bash
Change shipping information        Change shipping information Update the receive's address       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
