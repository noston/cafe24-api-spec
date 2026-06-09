# CREDITS


## Credits

```json
Endpoints    GET /api/v2/admin/credits
```

```json
GET /api/v2/admin/credits
```

### Credits property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| issue_date | 등록일 |
| member_id최대글자수 : [20자] | 회원아이디 |
| group_name | 회원등급명 |
| increase_amount | 지급 금액 |
| decrease_amount | 차감 금액 |
| balance | 잔액 |
| admin_id | 관리자 아이디 |
| admin_name | 관리자 이름 |
| reason | 처리사유 |
| case | 예치금 유형 |
| order_id | 주문번호 |

### Retrieve a list of credits by date range   cafe24

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
| order_id주문번호 | 주문번호 |
| search_field | 검색필드   id : 아이디 reason : 처리사유 |
| keyword | 검색어 |
| limit최소: [1]~최대: [200] | 조회결과 최대건수   DEFAULT 50 |
| offset최대값: [10000] | 조회결과 시작위치   DEFAULT 0 |

```bash
Retrieve a list of credits by date range        Retrieve a list of credits by date range Retrieve credits with fields parameter Retrieve credits using paging Retrieve a specific credits with case parameter       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/credits?start_date=2018-04-06&end_date=2018-07-05' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "credits": [        {            "shop_no": 1,            "issue_date": "2018-05-18T11:56:41+09:00",            "member_id": "sampleid",            "group_name": "Standard Membership",            "increase_amount": "1000.00",            "decrease_amount": "",            "balance": "1000.00",            "admin_id": "admin",            "admin_name": "John Doe",            "reason": "credits for order refund",            "case": "C",            "order_id": "20180421-0000010"        },        {            "shop_no": 1,            "issue_date": "2018-06-18T12:01:34+09:00",            "member_id": "sampleid",            "group_name": "Standard Membership",            "increase_amount": "1000.00",            "decrease_amount": "",            "balance": "2000.00",            "admin_id": "admin",            "admin_name": "John Doe",            "reason": "credits for order refund",            "case": "B",            "order_id": "20180425-0000012"        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/credits?start_date=2018-04-06&end_date=2018-07-05' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "credits": [        {            "shop_no": 1,            "issue_date": "2018-05-18T11:56:41+09:00",            "member_id": "sampleid",            "group_name": "Standard Membership",            "increase_amount": "1000.00",            "decrease_amount": "",            "balance": "1000.00",            "admin_id": "admin",            "admin_name": "John Doe",            "reason": "credits for order refund",            "case": "C",            "order_id": "20180421-0000010"        },        {            "shop_no": 1,            "issue_date": "2018-06-18T12:01:34+09:00",            "member_id": "sampleid",            "group_name": "Standard Membership",            "increase_amount": "1000.00",            "decrease_amount": "",            "balance": "2000.00",            "admin_id": "admin",            "admin_name": "John Doe",            "reason": "credits for order refund",            "case": "B",            "order_id": "20180425-0000012"        }    ]}
```
