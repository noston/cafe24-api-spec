# REPORTS HOURLYSALES


## Reports hourlysales

```json
Endpoints    GET /api/v2/admin/reports/hourlysales
```

```json
GET /api/v2/admin/reports/hourlysales
```

### Reports hourlysales property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| collection_date | 정산 수집 일자 |
| collection_hour | 정산 수집 시간 |
| order_count | 주문수 |
| item_count | 품목수 |
| order_price_amount | 상품 구매금액 |
| order_sale_price | 할인금액 |
| shipping_fee | 배송비 |
| coupon_discount_price | 쿠폰 할인금액 |
| actual_order_amount | 실결제금액 |
| refund_amount | 환불 금액 |
| sales | 순매출 |
| used_points | 적립금 |
| used_credits | 예치금 |
| used_naver_points | 네이버 마일리지 |
| used_naver_cash | 네이버캐시 |
| refund_points | 환불 적립금 |
| refund_credits | 환불 예치금 |
| refund_naver_points | 환불 네이버 마일리지 |
| refund_naver_cash | 환불 네이버캐시 |

### Retrieve hourly sales statistics of a store   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 매출통계 읽기권한 (mall.read_salesreport) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| start_dateRequired날짜 | 검색 시작일 |
| end_dateRequired날짜 | 검색 종료일 |
| collection_hour | 정산 수집 시간   수집 시간을 특정하여 검색 00 ~ 23 까지의 값을 입력할 수 있다. |
| limit최소: [1]~최대: [1000] | 조회결과 최대건수   DEFAULT 744 |
| offset최대값: [10000] | 조회결과 시작위치   DEFAULT 0 |

```bash
Retrieve hourly sales statistics of a store        Retrieve hourly sales statistics of a store Retrieve hourlysales with fields parameter Retrieve a specific hourlysales with collection_hour parameter Retrieve hourlysales using paging       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/reports/hourlysales?start_date=2021-02-24&end_date=2021-02-24' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "hourlysales": [        {            "shop_no": 1,            "collection_date": "2021-02-24",            "collection_hour": "12",            "order_count": 6,            "item_count": 7,            "order_price_amount": "53000.00",            "shipping_fee": "40.00",            "order_sale_price": "5050.00",            "coupon_discount_price": "1000.00",            "actual_order_amount": "46990.00",            "refund_amount": "0.00",            "sales": "46990.00",            "used_points": "100.00",            "used_credits": "0.00",            "used_naver_points": "0.00",            "used_naver_cash": "0.00",            "refund_points": "0.00",            "refund_credits": "0.00",            "refund_naver_points": "0.00",            "refund_naver_cash": "0.00"        },        {            "shop_no": 1,            "collection_date": "2021-02-24",            "collection_hour": "11",            "order_count": 2,            "item_count": 4,            "order_price_amount": "85000.00",            "shipping_fee": "20.00",            "order_sale_price": "20.00",            "coupon_discount_price": "0.00",            "actual_order_amount": "85000.00",            "refund_amount": "0.00",            "sales": "85000.00",            "used_points": "300.00",            "used_credits": "0.00",            "used_naver_points": "0.00",            "used_naver_cash": "0.00",            "refund_points": "0.00",            "refund_credits": "0.00",            "refund_naver_points": "0.00",            "refund_naver_cash": "0.00"        }    ],    "links": [        {            "rel": "next",            "href": "https://{mallid}.cafe24api.com/api/v2/admin/reports/hourlysales?limit=10&offset=10"        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/reports/hourlysales?start_date=2021-02-24&end_date=2021-02-24' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "hourlysales": [        {            "shop_no": 1,            "collection_date": "2021-02-24",            "collection_hour": "12",            "order_count": 6,            "item_count": 7,            "order_price_amount": "53000.00",            "shipping_fee": "40.00",            "order_sale_price": "5050.00",            "coupon_discount_price": "1000.00",            "actual_order_amount": "46990.00",            "refund_amount": "0.00",            "sales": "46990.00",            "used_points": "100.00",            "used_credits": "0.00",            "used_naver_points": "0.00",            "used_naver_cash": "0.00",            "refund_points": "0.00",            "refund_credits": "0.00",            "refund_naver_points": "0.00",            "refund_naver_cash": "0.00"        },        {            "shop_no": 1,            "collection_date": "2021-02-24",            "collection_hour": "11",            "order_count": 2,            "item_count": 4,            "order_price_amount": "85000.00",            "shipping_fee": "20.00",            "order_sale_price": "20.00",            "coupon_discount_price": "0.00",            "actual_order_amount": "85000.00",            "refund_amount": "0.00",            "sales": "85000.00",            "used_points": "300.00",            "used_credits": "0.00",            "used_naver_points": "0.00",            "used_naver_cash": "0.00",            "refund_points": "0.00",            "refund_credits": "0.00",            "refund_naver_points": "0.00",            "refund_naver_cash": "0.00"        }    ],    "links": [        {            "rel": "next",            "href": "https://{mallid}.cafe24api.com/api/v2/admin/reports/hourlysales?limit=10&offset=10"        }    ]}
```
