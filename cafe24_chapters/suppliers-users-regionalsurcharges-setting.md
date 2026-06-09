# SUPPLIERS USERS REGIONALSURCHARGES SETTING


## Suppliers users regionalsurcharges setting

```json
Endpoints    GET /api/v2/admin/suppliers/users/{supplier_id}/regionalsurcharges/setting
PUT /api/v2/admin/suppliers/users/{supplier_id}/regionalsurcharges/setting
```

```json
GET /api/v2/admin/suppliers/users/{supplier_id}/regionalsurcharges/setting
PUT /api/v2/admin/suppliers/users/{supplier_id}/regionalsurcharges/setting
```

### Suppliers users regionalsurcharges setting property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| supplier_id최대글자수 : [20자] | 공급사 아이디 |
| use_regional_surcharge | 지역별 배송비 사용여부 T : 사용함 F : 사용안함 |
| region_setting_type | 지역 설정 방식 A : 간편 설정 N : 지명 설정 Z : 우편번호 설정 |
| jeju_surcharge_amount최소: [0]~최대: [999999999] | 제주 추가 배송비 |
| remote_area_surcharge_amount최소: [0]~최대: [999999999] | 도서산간 추가 배송비 |

### Retrieve a supplier user's regional shipping fee settings   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 공급사 정보 읽기권한 (mall.read_supply) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| supplier_idRequired최대글자수 : [20자] | 공급사 아이디 |

```bash
Retrieve a supplier user's regional shipping fee settings        Retrieve a supplier user's regional shipping fee settings       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Update a supplier user's regional shipping fee settings   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 공급사 정보 쓰기권한 (mall.write_supply) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| supplier_idRequired최대글자수 : [20자] | 공급사 아이디 |
| use_regional_surchargeRequired | 지역별 배송비 사용여부   T : 사용함 F : 사용안함 |
| region_setting_typeRequired | 지역 설정 방식   A : 간편 설정 N : 지명 설정 Z : 우편번호 설정 |
| jeju_surcharge_amount최소: [0]~최대: [999999999] | 제주 추가 배송비 |
| remote_area_surcharge_amount최소: [0]~최대: [999999999] | 도서산간 추가 배송비 |

```bash
Update a supplier user's regional shipping fee settings        Update a supplier user's regional shipping fee settings       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
