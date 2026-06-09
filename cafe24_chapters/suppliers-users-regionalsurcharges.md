# SUPPLIERS USERS REGIONALSURCHARGES


## Suppliers users regionalsurcharges

```json
Endpoints    GET /api/v2/admin/suppliers/users/{supplier_id}/regionalsurcharges
POST /api/v2/admin/suppliers/users/{supplier_id}/regionalsurcharges
DELETE /api/v2/admin/suppliers/users/{supplier_id}/regionalsurcharges/{regional_surcharge_no}
```

```json
GET /api/v2/admin/suppliers/users/{supplier_id}/regionalsurcharges
POST /api/v2/admin/suppliers/users/{supplier_id}/regionalsurcharges
DELETE /api/v2/admin/suppliers/users/{supplier_id}/regionalsurcharges/{regional_surcharge_no}
```

### Suppliers users regionalsurcharges property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| regional_surcharge_no | 지역별 배송비 등록 번호 |
| supplier_id최대글자수 : [20자] | 공급사 아이디 |
| country_code최대글자수 : [2자] | 국가코드 KR : 대한민국 JP : 일본 VN : 베트남 |
| region_name최대글자수 : [255자] | 특수지역명 |
| surcharge_region_name최대글자수 : [300자] | 지역명 추가배송비를 부과할 지역이름 지역 설정방식(region_setting_type)이 'N'으로 설정 되어있는 경우 필수 입력 |
| start_zipcode최대글자수 : [8자] | 시작 우편번호 지역 설정 방식(region_setting_type)이 'Z'로 설정 되어있는 경우 필수 입력 |
| end_zipcode최대글자수 : [8자] | 끝 우편번호 지역 설정 방식(region_setting_type)이 'Z'로 설정 되어있는 경우 필수 입력 |
| regional_surcharge_amount최소: [1]~최대: [999999999] | 지역 추가 배송비 부과할 추가배송비 금액 |
| use_regional_surcharge | 지역별 배송비 사용여부 T : 사용함 F : 사용안함 |

### Retrieve a supplier user's list of regional shipping fees   cafe24 youtube

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
| offset최대값: [10000] | 조회결과 시작위치   DEFAULT 0 |
| limit최소: [1]~최대: [100] | 조회결과 최대건수   DEFAULT 10 |

```bash
Retrieve a supplier user's list of regional shipping fees        Retrieve a supplier user's list of regional shipping fees Retrieve regionalsurcharges with fields parameter Retrieve regionalsurcharges using paging       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Create regional shipping fee for a supplier user   cafe24 youtube

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
| country_code최대글자수 : [2자] | 국가코드   EC 한국, 일본, 베트남, 필리핀 버전에서는 사용할 수 없음.   KR : 대한민국 JP : 일본 VN : 베트남 |
| region_nameRequired최대글자수 : [255자] | 특수지역명 |
| use_regional_surchargeRequired | 지역별 배송비 사용여부   T : 사용함 F : 사용안함 |
| surcharge_region_name최대글자수 : [300자] | 지역명 |
| start_zipcode최대글자수 : [8자] | 시작 우편번호 |
| end_zipcode최대글자수 : [8자] | 끝 우편번호 |
| regional_surcharge_amountRequired최소: [1]~최대: [999999999] | 지역 추가 배송비 |

```bash
Create regional shipping fee for a supplier user        Create regional shipping fee for a supplier user Create a setting for suppliers users regionalsurcharge with region_setting_type field valuse is 'z' Try creating a setting for suppliers users regionalsurcharge by without region_name field       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Delete supplier user's regional shipping fee settings   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 공급사 정보 쓰기권한 (mall.write_supply) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| supplier_idRequired최대글자수 : [20자] | 공급사 아이디 |
| regional_surcharge_noRequired | 지역별 배송비 등록 번호 |

```bash
Delete supplier user's regional shipping fee settings        Delete supplier user's regional shipping fee settings       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
