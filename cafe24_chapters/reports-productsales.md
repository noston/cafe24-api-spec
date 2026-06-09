# REPORTS PRODUCTSALES


## Reports productsales

```json
Endpoints    GET /api/v2/admin/reports/productsales
```

```json
GET /api/v2/admin/reports/productsales
```

### Reports productsales property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| collection_date | 정산 수집 일자 |
| collection_hour | 정산 수집 시간 |
| product_no | 상품번호 |
| variants_code | 품목코드 |
| product_price | 상품 구매금액 |
| settle_count | 결제완료 수량 |
| refund_count | 환불완료 수량 |
| sale_count | 판매완료 수량 |
| return_product_count | 반품완료 수량 |
| exchange_product_count | 교환완료 수량 |
| cancel_product_count | 취소완료 수량 |
| total_sale_count | 누적 판매 수량 |
| total_cancel_count | 누적 취소 수량 |

### Retrieve hourly product sales statistics of a store   cafe24 youtube

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
| limit최소: [1]~최대: [1000] | 조회결과 최대건수   DEFAULT 100 |
| offset최대값: [10000] | 조회결과 시작위치   DEFAULT 0 |

```bash
Retrieve hourly product sales statistics of a store        Retrieve hourly product sales statistics of a store Retrieve productsales with fields parameter Retrieve a specific productsales with collection_hour parameter Retrieve productsales using paging       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/reports/productsales?start_date=2021-02-25&end_date=2021-02-25' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "productsales": [        {            "shop_no": 1,            "collection_date": "2021-02-25",            "collection_hour": "16",            "product_no": 25,            "variants_code": "P000ZNEM000A",            "product_price": "10000.00",            "settle_count": 1,            "refund_count": 0,            "sale_count": 1,            "exchange_product_count": 0,            "cancel_product_count": 0,            "return_product_count": 0,            "total_sale_count": 1,            "total_cancel_count": 0        },        {            "shop_no": 1,            "collection_date": "2021-02-25",            "collection_hour": "15",            "product_no": 26,            "variants_code": "P000ZORU000A",            "product_price": "1000.00",            "settle_count": 1,            "refund_count": 0,            "sale_count": 1,            "exchange_product_count": 0,            "cancel_product_count": 0,            "return_product_count": 0,            "total_sale_count": 1,            "total_cancel_count": 0        }    ],    "links": [        {            "rel": "next",            "href": "https://{mallid}.cafe24api.com/api/v2/admin/reports/productsales?limit=10&offset=10"        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/reports/productsales?start_date=2021-02-25&end_date=2021-02-25' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "productsales": [        {            "shop_no": 1,            "collection_date": "2021-02-25",            "collection_hour": "16",            "product_no": 25,            "variants_code": "P000ZNEM000A",            "product_price": "10000.00",            "settle_count": 1,            "refund_count": 0,            "sale_count": 1,            "exchange_product_count": 0,            "cancel_product_count": 0,            "return_product_count": 0,            "total_sale_count": 1,            "total_cancel_count": 0        },        {            "shop_no": 1,            "collection_date": "2021-02-25",            "collection_hour": "15",            "product_no": 26,            "variants_code": "P000ZORU000A",            "product_price": "1000.00",            "settle_count": 1,            "refund_count": 0,            "sale_count": 1,            "exchange_product_count": 0,            "cancel_product_count": 0,            "return_product_count": 0,            "total_sale_count": 1,            "total_cancel_count": 0        }    ],    "links": [        {            "rel": "next",            "href": "https://{mallid}.cafe24api.com/api/v2/admin/reports/productsales?limit=10&offset=10"        }    ]}
```
