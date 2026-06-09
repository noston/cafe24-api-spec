# CREDITS REPORT


## Credits report

```json
Endpoints    GET /api/v2/admin/credits/report
```

```json
GET /api/v2/admin/credits/report
```

### Credits report property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| increase_amount | 지급 금액 |
| decrease_amount | 차감 금액 |
| credits_total | 예치금 합계 |

### Retrieve a credit report by date range   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 적립금 읽기권한 (mall.read_mileage) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| start_dateRequired날짜 | 검색 시작일 |
| end_dateRequired날짜 | 검색 종료일 |
| type | 예치금 증가/차감 여부   I : 지급내역 D : 차감내역 |
| case | 예치금 유형   A : 주문취소 B : 예치금환불 C : 상품구매 D : 임의조정 E : 현금환불 G : 충전 |
| admin_id | 관리자 아이디 |
| search_field | 검색필드   id : 아이디 reason : 처리사유 |
| keyword | 검색어 |

```bash
Retrieve a credit report by date range        Retrieve a credit report by date range Retrieve report with fields parameter Retrieve a specific report with case parameter       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/credits/report?start_date=2018-04-06&end_date=2018-07-05' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "report": {        "shop_no": 1,        "increase_amount": "1000.00",        "decrease_amount": "0.00",        "credits_total": "1000.00"    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/credits/report?start_date=2018-04-06&end_date=2018-07-05' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "report": {        "shop_no": 1,        "increase_amount": "1000.00",        "decrease_amount": "0.00",        "credits_total": "1000.00"    }}
```
