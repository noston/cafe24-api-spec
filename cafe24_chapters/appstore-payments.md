# APPSTORE PAYMENTS


## Appstore payments

```json
Endpoints    GET /api/v2/admin/appstore/payments
GET /api/v2/admin/appstore/payments/count
```

```json
GET /api/v2/admin/appstore/payments
GET /api/v2/admin/appstore/payments/count
```

### Appstore payments property list

| Attribute | Description |
| --- | --- |
| order_id | 결제번호 앱스토어 주문의 주문 ID |
| payment_status | 결제상태 paid : 결제완료 refund : 환불 |
| title | 결제 명 앱스토어 주문의 주문 이름. 주문 생성시 지정이 가능하며, 사용자가 결제시 해당 결제의 내용이 무엇인지 알 수 있는 내용이어야 함. |
| approval_no | 승인번호 결제 승인 번호 |
| payment_gateway_name | 결제 PG사 이름 |
| payment_method | 결제수단 |
| payment_amount | 결제금액 |
| refund_amount | 환불금액 |
| currency | 화폐단위 KRW : ￦ 원 USD : $ 달러 JPY : ¥ 엔 PHP : ₱ 페소 |
| locale_code | 결제국가 |
| automatic_payment | 정기과금 여부 T : 사용함 F : 사용안함 |
| pay_date | 결제승인일 |
| refund_date | 환불승인일 |
| expiration_date | 만료일 |

### Retrieve a list of Cafe24 Store payments   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 앱 읽기권한 (mall.read_application) |
| 호출건수 제한 | 10 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| order_id | 주문번호   조회하고자하는 앱스토어 주문 번호   ,(콤마)로 여러 건을 검색할 수 있다. |
| start_dateRequired날짜 | 검색 시작일   해당일 이후에 결제완료된 주문 검색 |
| end_dateRequired날짜 | 검색 종료일   해당일 이전에 결제완료된 주문 검색 |
| currency | 화폐단위   KRW : ￦ 원 USD : $ 달러 JPY : ¥ 엔 PHP : ₱ 페소 |
| limit최소: [1]~최대: [50] | 조회결과 최대건수   조회하고자 하는 최대 건수를 지정할 수 있음. 예) 10 입력시 10건만 표시함.   DEFAULT 20 |
| offset최대값: [10000] | 조회결과 시작위치   DEFAULT 0 |

```bash
Retrieve a list of Cafe24 Store payments        Retrieve a list of Cafe24 Store payments Retrieve payments with fields parameter Retrieve a specific payments with order_id parameter Retrieve payments using paging       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/appstore/payments?start_date=2018-04-06&end_date=2018-07-05' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "payments": [        {            "order_id": "cafe24-20180704-100000000",            "payment_status": "paid",            "title": "App Name_App Store Order1",            "approval_no": "10000000",            "payment_gateway_name": "allat",            "payment_method": "card",            "payment_amount": "1000.00",            "refund_amount": "0.00",            "currency": "KRW",            "locale_code": "ko_KR",            "automatic_payment": "T",            "pay_date": "2018-07-04T11:19:27+09:00",            "refund_date": null,            "expiration_date": "2018-08-04T11:19:27+09:00"        },        {            "order_id": "cafe24-20180704-200000000",            "payment_status": "refund",            "title": "App Name_App Store Order2",            "approval_no": "20000000",            "payment_gateway_name": "allat",            "payment_method": "card",            "payment_amount": "1000.00",            "refund_amount": "1000.00",            "currency": "KRW",            "locale_code": "ko_KR",            "automatic_payment": "F",            "pay_date": "2018-07-04T11:19:27+09:00",            "refund_date": "2018-07-05T09:12:19+09:00",            "expiration_date": null        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/appstore/payments?start_date=2018-04-06&end_date=2018-07-05' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "payments": [        {            "order_id": "cafe24-20180704-100000000",            "payment_status": "paid",            "title": "App Name_App Store Order1",            "approval_no": "10000000",            "payment_gateway_name": "allat",            "payment_method": "card",            "payment_amount": "1000.00",            "refund_amount": "0.00",            "currency": "KRW",            "locale_code": "ko_KR",            "automatic_payment": "T",            "pay_date": "2018-07-04T11:19:27+09:00",            "refund_date": null,            "expiration_date": "2018-08-04T11:19:27+09:00"        },        {            "order_id": "cafe24-20180704-200000000",            "payment_status": "refund",            "title": "App Name_App Store Order2",            "approval_no": "20000000",            "payment_gateway_name": "allat",            "payment_method": "card",            "payment_amount": "1000.00",            "refund_amount": "1000.00",            "currency": "KRW",            "locale_code": "ko_KR",            "automatic_payment": "F",            "pay_date": "2018-07-04T11:19:27+09:00",            "refund_date": "2018-07-05T09:12:19+09:00",            "expiration_date": null        }    ]}
```

### Retrieve a count of Cafe24 Store payments   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 앱 읽기권한 (mall.read_application) |
| 호출건수 제한 | 10 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| order_id | 주문번호   조회하고자하는 앱스토어 주문 번호   ,(콤마)로 여러 건을 검색할 수 있다. |
| start_dateRequired날짜 | 검색 시작일   해당일 이후에 결제완료된 주문 검색 |
| end_dateRequired날짜 | 검색 종료일   해당일 이전에 결제완료된 주문 검색 |
| currency | 화폐단위   KRW : ￦ 원 USD : $ 달러 JPY : ¥ 엔 PHP : ₱ 페소 |

```bash
Retrieve a count of Cafe24 Store payments        Retrieve a count of Cafe24 Store payments       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/appstore/payments/count?start_date=2018-04-06&end_date=2018-07-05' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "count": 2}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/appstore/payments/count?start_date=2018-04-06&end_date=2018-07-05' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "count": 2}
```
