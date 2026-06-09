# DASHBOARD


## Dashboard

```json
Endpoints    GET /api/v2/admin/dashboard
```

```json
GET /api/v2/admin/dashboard
```

### Dashboard property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호. |
| daily_sales_stats | 일일 현황 정보 일 단위의 매출 현황 정보 |
| weekly_sales_stats | 주간 매출 현황 주간 단위의 매출 현황 정보 |
| monthly_sales_stats | 월간 매출 현황 월간 단위의 매출 현황 정보 |
| sold_out_products_count | 품절된 상품 수 품절된 상품의 수. 재고관리기능과 품절기능이 활성화 되어있을 경우 집계에 포함됨. |
| new_members_count | 신규회원 수 신규가입한 회원의 숫자 |
| board_list | 게시판 목록 해당 몰의 게시판의 리스트 |

### Retrieve a dashboard   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 읽기권한 (mall.read_store) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호.   DEFAULT 1 |

```bash
Retrieve a dashboard        Retrieve a dashboard       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/dashboard' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "dashboard": [        {            "shop_no": 1,            "daily_sales_stats": [                {                    "title": "December 20",                    "date": "2017-12-20",                    "order_price": "0.00",                    "paid_price": "0.00",                    "refund_price": "0.00",                    "order_count": 0,                    "payed_count": 0,                    "refund_count": 0,                    "prepareproduct_count": 0,                    "prepare_count": 0,                    "standby_count": 0,                    "shipping_count": 0,                    "shipped_count": 0,                    "canceled_count": 0,                    "returned_count": 0,                    "exchanged_count": 0,                    "ordered_total_count": 0                },                {                    "title": "December 21 (Today)",                    "date": "2017-12-21",                    "order_price": "0.00",                    "paid_price": "0.00",                    "refund_price": "0.00",                    "order_count": 0,                    "payed_count": 0,                    "refund_count": 0,                    "prepareproduct_count": 0,                    "prepare_count": 0,                    "standby_count": 0,                    "shipping_count": 0,                    "shipped_count": 0,                    "canceled_count": 0,                    "returned_count": 0,                    "exchanged_count": 0,                    "ordered_total_count": 0                }            ],            "weekly_sales_stats": {                "ordered_total_price": "0.00",                "payed_total_price": "0.00",                "refunded_total_price": "0.00",                "ordered_count": 0,                "payed_count": 0,                "refunded_count": 0,                "ordered_average_total_price": "0.00",                "payed_average_total_price": "0.00",                "refunded_average_total_price": "0.00",                "ordered_average_count": 0,                "payed_average_count": 0,                "refunded_average_count": 0            },            "monthly_sales_stats": {                "ordered_total_price": "0.00",                "payed_total_price": "0.00",                "refunded_total_price": "0.00",                "ordered_count": 0,                "payed_count": 0,                "refunded_count": 0,                "ordered_average_total_price": "0.00",                "payed_average_total_price": "0.00",                "refunded_average_total_price": "0.00",                "ordered_average_count": 0,                "payed_average_count": 0,                "refunded_average_count": 0            },            "sold_out_products_count": 0,            "new_members_count": 0,            "board_list": [                {                    "type": "B",                    "board_no": 1,                    "board_name": "공지사항",                    "new_registered_count": 0,                    "page_url": "/disp/admin/mobile/index#/bulletins?board_no=1"                },                {                    "type": "B",                    "board_no": 2,                    "board_name": "뉴스/이벤트",                    "new_registered_count": 0,                    "page_url": "/disp/admin/mobile/index#/bulletins?board_no=2"                }            ]        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/dashboard' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "dashboard": [        {            "shop_no": 1,            "daily_sales_stats": [                {                    "title": "December 20",                    "date": "2017-12-20",                    "order_price": "0.00",                    "paid_price": "0.00",                    "refund_price": "0.00",                    "order_count": 0,                    "payed_count": 0,                    "refund_count": 0,                    "prepareproduct_count": 0,                    "prepare_count": 0,                    "standby_count": 0,                    "shipping_count": 0,                    "shipped_count": 0,                    "canceled_count": 0,                    "returned_count": 0,                    "exchanged_count": 0,                    "ordered_total_count": 0                },                {                    "title": "December 21 (Today)",                    "date": "2017-12-21",                    "order_price": "0.00",                    "paid_price": "0.00",                    "refund_price": "0.00",                    "order_count": 0,                    "payed_count": 0,                    "refund_count": 0,                    "prepareproduct_count": 0,                    "prepare_count": 0,                    "standby_count": 0,                    "shipping_count": 0,                    "shipped_count": 0,                    "canceled_count": 0,                    "returned_count": 0,                    "exchanged_count": 0,                    "ordered_total_count": 0                }            ],            "weekly_sales_stats": {                "ordered_total_price": "0.00",                "payed_total_price": "0.00",                "refunded_total_price": "0.00",                "ordered_count": 0,                "payed_count": 0,                "refunded_count": 0,                "ordered_average_total_price": "0.00",                "payed_average_total_price": "0.00",                "refunded_average_total_price": "0.00",                "ordered_average_count": 0,                "payed_average_count": 0,                "refunded_average_count": 0            },            "monthly_sales_stats": {                "ordered_total_price": "0.00",                "payed_total_price": "0.00",                "refunded_total_price": "0.00",                "ordered_count": 0,                "payed_count": 0,                "refunded_count": 0,                "ordered_average_total_price": "0.00",                "payed_average_total_price": "0.00",                "refunded_average_total_price": "0.00",                "ordered_average_count": 0,                "payed_average_count": 0,                "refunded_average_count": 0            },            "sold_out_products_count": 0,            "new_members_count": 0,            "board_list": [                {                    "type": "B",                    "board_no": 1,                    "board_name": "공지사항",                    "new_registered_count": 0,                    "page_url": "/disp/admin/mobile/index#/bulletins?board_no=1"                },                {                    "type": "B",                    "board_no": 2,                    "board_name": "뉴스/이벤트",                    "new_registered_count": 0,                    "page_url": "/disp/admin/mobile/index#/bulletins?board_no=2"                }            ]        }    ]}
```
