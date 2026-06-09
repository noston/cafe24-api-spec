# BENEFITS SETTING


## Benefits setting

```json
Endpoints    GET /api/v2/admin/benefits/setting
PUT /api/v2/admin/benefits/setting
```

```json
GET /api/v2/admin/benefits/setting
PUT /api/v2/admin/benefits/setting
```

### Benefits setting property list

| Attribute | Description |
| --- | --- |
| use_gift | 사은품기능 사용여부 T : 사용함 F : 사용안함 |
| available_payment_methods | 사은품 제공 결제수단 all : 모든결제 bank_only : 무통장입금만 exclude_bank : 무통장입금 외 모든결제 |
| allow_point_payment | 적립금 전액결제 시 사은품 제공 여부 T : 제공함 F : 제공안함 |
| gift_calculation_scope | 사은품제공 계산범위 all : 전체 주문 상품 기준 benefit : 혜택 적용 상품만 기준 |
| gift_calculation_type | 사은품제공 계산방식 total_order : 총 주문금액 기준 actual_payment : 실결제금액 기준 |
| include_point_usage | 적립금 사용금액 포함 여부 T : 포함 F : 미포함 |
| include_shipping_fee | 배송비 포함여부 I : 포함계산 E : 배송비 제외 계산 |
| display_soldout_gifts | 품절 사은품 표시여부 grayed : 표시하되 선택불가 disabled : 표시하지 않음 |
| gift_grant_type | 사은품 지급형태 S : 고객 선택형 A : 자동 지급형 |
| gift_selection_mode | 사은품 선택방식 S : 단일선택 M : 복수선택 |
| gift_grant_mode | 사은품 지급방식 S : 단일 지급 M : 복수 지급 |
| gift_selection_step | 사은품 선택단계 order_form : 주문서 화면 order_complete : 주문완료 화면 order_detail : 주문상세조회 화면 |
| gift_available_condition | 사은품 신청 가능 조건 during_period : 설정 기간 동안만 신청 가능 after_period : 설정 기간 이후에도 신청 가능 |
| offer_only_one_in_automatic | 자동 지급형 사은품 지급수량 T : 1개만 지급 F : 상품 구매수량에 따라 지급 |
| allow_gift_review | 사은품 상품 상품후기 작성가능여부 T : 작성 가능 F : 작성 불가 |

### Retrieve incentive settings   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 읽기권한 (mall.read_store) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |

```bash
Retrieve incentive settings        Retrieve incentive settings       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/benefits/setting?shop_no=1' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "benefit": {        "use_gift": "T",        "available_payment_methods": "all",        "allow_point_payment": "T",        "gift_calculation_scope": "all",        "gift_calculation_type": "total_order",        "include_shipping_fee": "I",        "display_soldout_gifts": "grayed",        "gift_grant_type": "S",        "gift_grant_mode": "S",        "gift_selection_mode": "S",        "gift_selection_step": [            "order_complete",            "order_detail"        ],        "gift_available_condition": "during_period",        "offer_only_one_in_automatic": "F",        "allow_gift_review": "T"    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/benefits/setting?shop_no=1' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "benefit": {        "use_gift": "T",        "available_payment_methods": "all",        "allow_point_payment": "T",        "gift_calculation_scope": "all",        "gift_calculation_type": "total_order",        "include_shipping_fee": "I",        "display_soldout_gifts": "grayed",        "gift_grant_type": "S",        "gift_grant_mode": "S",        "gift_selection_mode": "S",        "gift_selection_step": [            "order_complete",            "order_detail"        ],        "gift_available_condition": "during_period",        "offer_only_one_in_automatic": "F",        "allow_gift_review": "T"    }}
```

### Update incentive settings   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 쓰기권한 (mall.write_store) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| use_gift | 사은품기능 사용여부   T : 사용함 F : 사용안함 |
| available_payment_methods | 사은품 제공 결제수단   all : 모든결제 bank_only : 무통장입금만 exclude_bank : 무통장입금 외 모든결제 |
| allow_point_payment | 적립금 전액결제 시 사은품 제공 여부   T : 제공함 F : 제공안함 |
| gift_calculation_scope | 사은품제공 계산범위   all : 전체 주문 상품 기준 benefit : 혜택 적용 상품만 기준 |
| gift_calculation_type | 사은품제공 계산방식   total_order : 총 주문금액 기준 actual_payment : 실결제금액 기준 |
| include_point_usage | 적립금 사용금액 포함 여부   T : 포함 F : 미포함 |
| include_shipping_fee | 배송비 포함여부   I : 포함계산 E : 배송비 제외 계산 |
| display_soldout_gifts | 품절 사은품 표시여부   grayed : 표시하되 선택불가 disabled : 표시하지 않음 |
| gift_grant_type | 사은품 지급형태   S : 고객 선택형 A : 자동 지급형 |
| gift_selection_mode | 사은품 선택방식   S : 단일선택 M : 복수선택 |
| gift_grant_mode | 사은품 지급방식   S : 단일 지급 M : 복수 지급 |
| gift_selection_step | 사은품 선택단계   order_form : 주문서 화면 order_complete : 주문완료 화면 order_detail : 주문상세조회 화면 |
| gift_available_condition | 사은품 신청 가능 조건   사은품선택단계(gift_selection_step)에서 주문상세조회(order_detail)항목이 선택된 경우만 입력 가능   during_period : 설정 기간 동안만 신청 가능 after_period : 설정 기간 이후에도 신청 가능 |
| offer_only_one_in_automatic | 자동 지급형 사은품 지급수량   T : 1개만 지급 F : 상품 구매수량에 따라 지급 |
| allow_gift_review | 사은품 상품 상품후기 작성가능여부   T : 작성 가능 F : 작성 불가 |

```bash
Update incentive settings        Update incentive settings       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/benefits/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "use_gift": "T",        "available_payment_methods": "all",        "allow_point_payment": "T",        "gift_calculation_scope": "all",        "gift_calculation_type": "total_order",        "include_shipping_fee": "I",        "display_soldout_gifts": "grayed",        "gift_grant_type": "S",        "gift_selection_mode": "S",        "gift_selection_step": [            "order_complete",            "order_detail"        ],        "gift_available_condition": "during_period",        "allow_gift_review": "T"    }}'    Response  Copy     {    "benefit": {        "use_gift": "T",        "available_payment_methods": "all",        "allow_point_payment": "T",        "gift_calculation_scope": "all",        "gift_calculation_type": "total_order",        "include_shipping_fee": "I",        "display_soldout_gifts": "grayed",        "gift_grant_type": "S",        "gift_selection_mode": "S",        "gift_selection_step": [            "order_complete",            "order_detail"        ],        "gift_available_condition": "during_period",        "allow_gift_review": "T"    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/benefits/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "use_gift": "T",        "available_payment_methods": "all",        "allow_point_payment": "T",        "gift_calculation_scope": "all",        "gift_calculation_type": "total_order",        "include_shipping_fee": "I",        "display_soldout_gifts": "grayed",        "gift_grant_type": "S",        "gift_selection_mode": "S",        "gift_selection_step": [            "order_complete",            "order_detail"        ],        "gift_available_condition": "during_period",        "allow_gift_review": "T"    }}'
```

```json
{    "benefit": {        "use_gift": "T",        "available_payment_methods": "all",        "allow_point_payment": "T",        "gift_calculation_scope": "all",        "gift_calculation_type": "total_order",        "include_shipping_fee": "I",        "display_soldout_gifts": "grayed",        "gift_grant_type": "S",        "gift_selection_mode": "S",        "gift_selection_step": [            "order_complete",            "order_detail"        ],        "gift_available_condition": "during_period",        "allow_gift_review": "T"    }}
```
