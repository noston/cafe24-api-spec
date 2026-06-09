# SHIPPING SUPPLIERS ADDITIONALFEES


## Shipping suppliers additionalfees

```json
Endpoints    GET /api/v2/admin/shipping/suppliers/{supplier_id}/additionalfees
```

```json
GET /api/v2/admin/shipping/suppliers/{supplier_id}/additionalfees
```

### Shipping suppliers additionalfees property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| oversea_additional_fee | 해외배송 부가금액 사용여부 T : 사용함 F : 사용안함 |
| country_code | 국가코드 |
| fee_name | 부과금액 명칭 |
| min_value | 조건 최소값 |
| max_value | 조건 최대값 |
| additional_fee | 부가금액 |
| unit | 해외배송 부가금액 단위 W : 정액 P : 퍼센트 |
| rounding_unit | 절사단위 F : 절사안함 0 : 1원단위 1 : 10원단위 2 : 100원단위 3 : 1000원단위 |
| rounding_rule | 절사 방법 L : 내림 U : 반올림 C : 올림 |

### Retrieve additional handling fees for supplier international shipping   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 공급사 정보 읽기권한 (mall.read_supply) |
| 호출건수 제한 | 30 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| supplier_idRequired | 공급사 아이디 |
| limit최소: [1]~최대: [500] | 조회결과 최대건수   DEFAULT 100 |
| offset최대값: [500] | 조회결과 시작위치   DEFAULT 0 |

```bash
Retrieve additional handling fees for supplier international shipping        Retrieve additional handling fees for supplier international shipping       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
