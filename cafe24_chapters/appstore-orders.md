# APPSTORE ORDERS


## Appstore orders

```json
Endpoints    GET /api/v2/admin/appstore/orders/{order_id}
POST /api/v2/admin/appstore/orders
```

```json
GET /api/v2/admin/appstore/orders/{order_id}
POST /api/v2/admin/appstore/orders
```

### Appstore orders property list

| Attribute | Description |
| --- | --- |
| order_id | 주문아이디 앱스토어 주문의 주문 ID |
| order_name | 주문명 앱스토어 주문의 주문 이름. 주문 생성시 지정이 가능하며, 사용자가 결제시 해당 결제의 내용이 무엇인지 알 수 있는 내용이어야 함. |
| order_amount | 주문금액 앱스토어 주문 생성시 결제 요청한 주문 금액 |
| currency | 화폐단위 KRW : ￦ 원 USD : $ 달러 JPY : ¥ 엔 PHP : ₱ 페소 |
| return_url | Return Url 사용자가 결제 후 이동해야하는 페이지. |
| automatic_payment최대글자수 : [1자] | 정기과금 여부 T : 사용함 F : 사용안함 |
| created_date | 주문 생성일 |
| confirmation_url | 결제 Url 사용자가 결제하기 위해 자동으로 이동하는 페이지 주소 |

### Retreive a Cafe24 Store order   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 앱 읽기권한 (mall.read_application) |
| 호출건수 제한 | 10 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| order_id | 주문번호   조회하고자하는 앱스토어 주문 번호 |

```bash
Retreive a Cafe24 Store order        Retreive a Cafe24 Store order       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/appstore/orders/cafe24-20180704-100000000' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "order": {        "order_id": "cafe24-20180704-100000000",        "order_name": "App Name_Appstore Order Name",        "order_amount": "1000.00",        "currency": "KRW",        "return_url": "https://sample_shop.cafe24.com",        "automatic_payment": "F",        "created_date": "2018-07-04T13:52:49+09:00"    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/appstore/orders/cafe24-20180704-100000000' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "order": {        "order_id": "cafe24-20180704-100000000",        "order_name": "App Name_Appstore Order Name",        "order_amount": "1000.00",        "currency": "KRW",        "return_url": "https://sample_shop.cafe24.com",        "automatic_payment": "F",        "created_date": "2018-07-04T13:52:49+09:00"    }}
```

### Create a Cafe24 Store order   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 앱 쓰기권한 (mall.write_application) |
| 호출건수 제한 | 10 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| order_nameRequired최대글자수 : [100자] | 주문명   앱스토어 주문의 주문 이름. 주문 생성시 지정이 가능하며, 사용자가 결제시 해당 결제의 내용이 무엇인지 알 수 있는 내용이어야 함. |
| order_amountRequired | 주문금액   사용자에게 결제 받고자 하는 주문 금액 입력 |
| return_urlRequired최대글자수 : [250자] | Return Url   사용자가 결제 후 이동해야하는 페이지. 결제 완료 페이지 주소를 입력한다. |
| automatic_payment최대글자수 : [1자] | 정기과금 여부   T : 사용함 F : 사용안함   DEFAULT F |

```bash
Create a Cafe24 Store order        Create a Cafe24 Store order       Request   cURL Java Python Node.js PHP Go  Copy     curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/appstore/orders' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "request": {        "order_name": "Appstore Order Name",        "order_amount": "1000.00",        "return_url": "https://sample_shop.cafe24.com",        "automatic_payment": "F"    }}'    Response  Copy     {    "order": {        "order_id": "cafe24-20180704-100000000",        "order_name": "Appstore Order Name",        "order_amount": "1000.00",        "currency": "KRW",        "return_url": "https://sample_shop.cafe24.com",        "automatic_payment": "F",        "confirmation_url": "https://samplemall.cafe24.com/disp/common/myapps/order?signature=BAhpBBMxojw%3D--d1c0134218f0ff3c0f57cb3b57bcc34e6f170727"    }}
```

```bash
curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/appstore/orders' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "request": {        "order_name": "Appstore Order Name",        "order_amount": "1000.00",        "return_url": "https://sample_shop.cafe24.com",        "automatic_payment": "F"    }}'
```

```json
{    "order": {        "order_id": "cafe24-20180704-100000000",        "order_name": "Appstore Order Name",        "order_amount": "1000.00",        "currency": "KRW",        "return_url": "https://sample_shop.cafe24.com",        "automatic_payment": "F",        "confirmation_url": "https://samplemall.cafe24.com/disp/common/myapps/order?signature=BAhpBBMxojw%3D--d1c0134218f0ff3c0f57cb3b57bcc34e6f170727"    }}
```
