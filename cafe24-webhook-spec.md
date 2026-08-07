# Event sample data

 **You can find various  examples of webhook events and their parameters on this page.  

You can also find a list of sample data in the [Webhook] section in [Dashboard>Products>Apps>App setup].** 

 **Contents** 
- [App event sample data](#title1)
- [App event parameters](#title2)
- [Store event sample data](#title3)
- [Store event parameters](#title4)

 **Note** 
Please be aware that the data shown in these examples are used for tests and may differ from actual data.

## App event sample data

| Event no. | Event | Sample data |
| --- | --- | --- |
| 90077 | When an installed app has been deleted from the store | {   "event_no": 90077,   "resource":{     "mall_id": "leesunsin",     "client_id": "sample7eBNEqSfkd7I8hoA",     "app_name": "sample_app",     "deleted_date": "2020-07-01T12:30:15+09:00"   } }  |
| 90078 | When an installed app has expired on the store | {   "event_no": 90078,   "resource":{     "mall_id": "leesunsin",      "client_id": "sample7eBNEqSfkd7I8hoA",     "app_name": "sample_app",     "expired_date": "2020-07-01T12:30:15+09:00"   } }  |
| 90079 | When an installed app has its subscription renewed | {   "event_no": 90079,   "resource":{     "mall_id": "leesunsin",     "client_id": "sample7eBNEqSfkd7I8hoA",     "app_name": "sample_app",     "expire_date": "2020-08-31T23:59:59+09:00",     "previous_expire_date": "2020-07-31T23:59:59+09:00",     "updated_date": "2020-07-01T12:30:15+09:00"   } }  |
| 90157 | When an installed app has been paid for | {   "event_no": 90157,   "resource":{   "mall_id": "leesunsin",   "client_id": "sample7eBNEqSfkd7I8hoA",   "order_id": "Tb1dbe01667974041111",   "payed_date": "2022-12-01 13:54:30",   "currency": "KRW",   "amount": "1000",   "channel": "APP"   } }  |
| 90158 | When a refund has been requested for an installed app | {   "event_no": 90158,   "resource":{  "mall_id": "leesunsin",   "client_id": "sample7eBNEqSfkd7I8hoA",   "order_id": "Tb1dbe01667974041111",   "reason_code": "A",   "reason_detail": "The app does not function properly.",   "request_date": "2022-12-13T16:09:58+09:00"   } }  |
| 90159 | When payment for an installed app has been refunded | {   "event_no": 90159,   "resource":{  "mall_id": "leesunsin",   "client_id": "sample7eBNEqSfkd7I8hoA",   "order_id": "Tb1dbe01667974041111",   "currency": "KRW",   "refunded_amount": "200.00",   "expire_date": "2023-01-21T23:59:59+09:00",   "refunded_date": "2022-12-13T16:09:58+09:00"   } } }  |
| 90160 | When the return of an order received at the shopping mall has been completed (by cancellation number) | {     "event_no": 90160,     "resource": {         "mall_id": "sampleMall",         "event_shop_no": "1",         "order_id": "20230316-0000287",         "claim_code": "C20230329-0001215",         "claim_reason_type": "",         "claim_reason_type_text": "",         "claim_reason": "",         "order_price_amount": "38000.00",         "refund_amount": "35000.00",         "shipping_fee": "0.00",         "refund_shipping_fee": "0.00",         "refund_regional_surcharge": "0.00",         "return_shipping_fee": "0.00",         "return_regional_surcharge": "0.00",         "add_discount_amount": "0.00",         "member_grade_discount_amount": "0.00",         "shipping_discount_amount": "0.00",         "coupon_discount_amount": "-3000.00",         "point_used": "0.00",         "credit_used": "0.00"     } }  |

## App event parameters

| Parameter | Description | Memo |
| --- | --- | --- |
| event_no | Event type |
| mall_id | Store ID |
| client_id | App ID |
| app_name | App name |
| deleted_date | App deleted date |
| expired_date | App expiry date |
| previous_expire_date | App previous expiry date |
| updated_date | App new expiry date |
| order_id | Order ID |
| payed_date | Payment date |
| currency | Currency |
| amount | Payment amount |
| channel | Requested channel | App: In-app payment Web: Regular payment |
| reason_code | Refund request code | A: App features do not function properly B: App causes store performance to drop C: Legal issues such as personal information leaked D: Features are not as advertised E: For reasons agreed between customer and partner Z: Other reason |
| reason_detail | Reason details |
| request_date | Request date |
| refunded_amount | Refund amount |
| refunded_date | Refund date |

## Store event sample data

### Store>Products

| Event no. | Event | Sample data |
| --- | --- | --- |
| 90001 | When a product has been added to the store | {   "event_no": 90001,   "resource":{     "mall_id":"cafe24bestshop",     "event_shop_no":"1",     "product_no":36518,     "product_code":"P000CCAO",     "created_date":"2020-07-17T15:26:52+09:00",     "updated_date":"2020-07-17T15:26:52+09:00",     "product_name":"Sample Product Name",     "eng_product_name":"",     "supply_product_name":"Supply Sample Name",     "model_name":"Sample Product CAFE2468",     "custom_product_code":"CAFE2468",     "product_condition":"N",     "summary_description":"Flower Skirt",     "simple_description":"Sweet Ballerina Flower Pleated Skirt.",     "description":"desc.",     "display":"F",     "selling":"T",     "retail_price":"0.00",     "supply_price":"20000.00",     "price":"24680.00",     "price_content":null,     "adult_certification":"F",     "manufacturer_code":"M0000000",     "supplier_code":"S0000000",     "brand_code":"B0000000",     "trend_code":"T0000000",     "made_date":"2020-07-10",     "release_date":"2020-07-10",     "origin_place_code":126,     "shipping_scope":"B",     "translated":"F"  } }  |
| 90002 | When a product has been edited on the store |
| 90041 | When products have been edited in bulk on the store | {   "event_no": 90041,   "resource":{     "mall_id":"cafe24bestshop",      "event_shop_no":"1",     "product_no":"17652,17394,17293,16807,16118",     "action":"batch"   } }  |
| 90003 | When a product has been deleted from the store | {   "event_no": 90003,   "resource":{     "mall_id":"cafe24bestshop",     "event_shop_no":"4",     "product_no":7178,     "product_code":"P0000KQC"   } }  |
| 90022 | When a product has been restored on the store | {   "event_no": 90022,   "resource":{     "mall_id":"cafe24bestshop",     "event_shop_no":"1",     "product_no":131   } }  |
| 90075 | When a variant inventory has been changed on the store | {   "event_no": 90075,   "resource":{     "mall_id":"cafe24bestshop",     "product_no":36518,     "product_code":"P000CCAO",     "created_date":"2020-07-17T15:26:52+09:00",     "updated_date":"2020-07-17T15:26:52+09:00",     "product_name":"Sample Product Name",     "eng_product_name":"",     "supply_product_name":"Supply Sample Name",     "model_name":"Sample Product CAFE2468",     "custom_product_code":"CAFE2468",     "product_condition":"N",     "summary_description":"Flower Skirt",     "simple_description":"Sweet Ballerina Flower Pleated Skirt.",     "description":"desc.",     "display":"F",     "selling":"T",     "retail_price":"0.00",     "supply_price":"27000.00",     "price":"24680.00",     "price_content":null,     "adult_certification":"F",     "manufacturer_code":"M0000000",     "supplier_code":"S0000000",     "brand_code":"B0000000",     "trend_code":"T0000000",     "made_date":"2020-07-10",     "release_date":"2020-07-10",     "origin_place_code":126,     "shipping_scope":"B",     "translated":"F",     "status_text":"In case that item stock is less than or equal 0",     "variant_code":"P000CCAO000B",     "use_soldout":"T"   } }  |
| 90150 | Out-of-stock status of a product on a store has been updated. | {     "event_no": 90150,     "resource": {         "mall_id": "cafe24bestshop",         "event_shop_no": "1",         "sold_out_by_current_shop": "T",         "product_no": "1",         "sold_out": {             "1": "T",             "2": "F",             "3": "F"         }     } }  |

### Store>Orders

| Event no. | Event | Sample data |
| --- | --- | --- |
| 90023 | When an order has been processed on the store | {   "event_no": 90023,   "resource":{     "mall_id":"cafe24bestshop",     "event_shop_no":"1",     "order_id":"20200717-0029236",     "payment_gateway_name":"",     "currency":"KRW",     "order_date":"2020-07-17T15:28:14+09:00",     "order_place_name":"naver pay",     "member_id":"gdhong",     "member_authentication":null,     "buyer_name":"Jessica Hong",     "buyer_email":"gdhong@cafe24corp.com",     "buyer_phone":"02-0000-0000",     "buyer_cellphone":"010-2424-2424",     "group_no_when_ordering":"",     "first_order":null,     "order_from_mobile":"F",     "paid":"T",     "payment_date":"2020-07-17T15:24:07+09:00",     "billing_name":"Jessica Hong",     "bank_code":null,     "payment_method":"mileage",     "easypay_name":"",     "use_escrow":"F",     "bank_account_no":"",     "order_price_amount":"24680.00",     "membership_discount_amount":"0.00",     "actual_payment_amount":"0.00",     "mileage_spent_amount":"0.00",     "shipping_fee":"0.00",     "shipping_type":"A",     "shipping_status":"F",     "wished_delivery_date":"0000-00-00",     "wished_delivery_time":null,     "store_pickup":"F",     "shipping_message":"",     "order_place_id":"NCHECKOUT",     "ordering_product_code":"P00000BO,P00000DQ",     "ordering_product_name":"Sample Product Name 1,Sample Product Name 2"   } }  |
| 90024 | When an order's shipping status has been changed on the store | {     "event_no": 90024,     "resource": {       "mall_id":"cafe24bestshop",       "event_shop_no":"1",       "order_id":"20200717-0029236",       "payment_gateway_name":"",       "currency":"KRW",       "order_date":"2020-07-17T15:28:14+09:00",       "order_place_name":"네이버 페이",       "member_id":"gdhong",       "member_authentication":null,       "buyer_name":"홍길동",       "buyer_email":"gdhong@cafe24corp.com",       "buyer_phone":"02-0000-0000",       "buyer_cellphone":"010-2424-2424",       "group_no_when_ordering":"",       "first_order":null,       "order_from_mobile":"T",       "paid":"T",       "payment_date":"2020-07-17T15:24:07+09:00",       "billing_name":"홍길동",       "bank_code":null,       "payment_method":"card",       "easypay_name":"",       "use_escrow":"F",       "bank_account_no":"",       "order_price_amount":"24680.00",       "membership_discount_amount":"0.00",       "actual_payment_amount":"4000.00",       "mileage_spent_amount":"0.00",       "cancel_date":null,       "shipping_fee":"0.00",       "shipping_type":"A",       "shipping_status":"T",       "wished_delivery_date":"0000-00-00",       "wished_delivery_time":null,       "return_confirmed_date":null,       "store_pickup":"F",       "shipping_message":"",       "order_place_id":"NCHECKOUT",       "ordering_product_code":"P00000BO,P00000DQ",       "ordering_product_name":"카페24 샘플 상품1,카페24 샘플 상품2",       "included_deferpay_order":"F",       "deferpay_order_id":"",       "withdraw":"T",       "withdraw_type":"C"     } }  |
| 90071 | When shipping statuses have been changed in bulk on the store | {   "event_no": 90071,   "resource":{     "mall_id":"cafe24bestshop",     "event_shop_no":"1",     "order_id":"20200717-0001242,20200717-0001251,20200717-0001261,20200717-0001270,20200717-0001287",     "included_deferpay_order":"",     "deferpay_order_id":""   } }  |
| 90025 | When an order's payment status has been changed on the store | {     "event_no": 90025,     "resource": {       "mall_id":"cafe24bestshop",       "event_shop_no":"1",       "order_id":"20200717-0029236",       "payment_gateway_name":"",       "currency":"KRW",       "order_date":"2020-07-17T15:30:14+09:00",       "order_place_name":"모바일웹",       "member_id":"gdhong",       "member_authentication":null,       "buyer_name":"홍길동",       "buyer_email":"gdhong@cafe24corp.com",       "buyer_phone":"02-0000-0000",       "buyer_cellphone":"010-2424-2424",       "group_no_when_ordering":"",       "first_order":"F",       "order_from_mobile":"T",       "paid":"T",       "payment_date":"2020-07-17T15:24:07+09:00",       "billing_name":"홍길동",       "bank_code":"bank_20",       "payment_method":"cash",       "easypay_name":"",       "use_escrow":"F",       "bank_account_no":"382-222254-13-001",       "order_price_amount":"24680.00",       "membership_discount_amount":"0.00",       "actual_payment_amount":"27580",       "mileage_spent_amount":"100.00",       "shipping_fee":"3000.00",       "shipping_type":"A",       "shipping_status":"F",       "wished_delivery_date":"",       "wished_delivery_time":null,       "store_pickup":"F",       "shipping_message":"빠른 배송 부탁드립니다.",       "ordering_product_code":"P00000HK",       "ordering_product_name":"카페24 샘플 상품1",       "withdraw":"T",       "withdraw_type":"E"     } }  |
| 90026 | When an order's cancellation status has been changed on the store | {   "event_no": 90026,   "resource":{     "mall_id":"cafe24bestshop",     "event_shop_no":"1",     "order_id":"20200716-0000023",     "payment_gateway_name":"inicis",     "currency":"KRW",     "order_date":"2020-07-16T02:20:20+09:00",     "order_place_name":"naver pay",     "member_id":"gdhong",     "member_authentication":null,     "buyer_name":"Jessica Hong",     "buyer_email":"gdhong@cafe24corp.com",     "buyer_phone":"02-0000-0000",     "buyer_cellphone":"010-2424-2424",     "group_no_when_ordering":"1",     "first_order":"T",     "order_from_mobile":"T",     "paid":"T",     "payment_date":"2020-07-17T15:24:07+09:00",     "billing_name":"Jessica Hong",     "bank_code":"",     "payment_method":"card",     "easypay_name":"",     "use_escrow":"F",     "bank_account_no":"382-222254-13-001",     "order_price_amount":"24680.00",     "membership_discount_amount":"0.00",     "actual_payment_amount":"24580",     "mileage_spent_amount":"100.00",     "cancel_date":null,     "shipping_fee":"0.00",     "shipping_type":"A",     "shipping_status":"F",     "wished_delivery_date":"",     "wished_delivery_time":null,     "store_pickup":"F",     "shipping_message":"Quick Delivery please.",     "order_place_id":"mobile",     "ordering_product_code":"P00000HK",     "ordering_product_name":"Sample Product Name 1"   } }  |
| 90072 | When cancellation statuses have been changed in bulk on the store | {   "event_no": 90072,   "resource":{     "mall_id":"cafe24bestshop",     "event_shop_no":"1",     "order_id":"20200713-0000039,20200708-0000080"   } }  |
| 90027 | When an order's return status has been changed on the store | {     "event_no": 90027,     "resource": {       "mall_id":"cafe24bestshop",       "event_shop_no":"1",       "order_id":"20200716-0000023",       "payment_gateway_name":"inicis",       "currency":"KRW",       "order_date":"2020-07-16T02:20:20+09:00",       "order_place_name":"모바일웹",       "member_id":"gdhong",       "member_authentication":null,       "buyer_name":"홍길동",       "buyer_email":"gdhong@cafe24corp.com",       "buyer_phone":"02-0000-0000",       "buyer_cellphone":"010-2424-2424",       "group_no_when_ordering":"1",       "first_order":"T",       "order_from_mobile":"T",       "paid":"T",       "payment_date":"2020-07-17T15:24:07+09:00",       "billing_name":"홍길동",       "bank_code":"",       "payment_method":"card",       "easypay_name":"",       "use_escrow":"F",       "bank_account_no":"382-222254-13-001",       "order_price_amount":"24680.00",       "membership_discount_amount":"0.00",       "actual_payment_amount":"24580",       "mileage_spent_amount":"100.00",       "cancel_date":null,       "shipping_fee":"0.00",       "shipping_type":"A",       "shipping_status":"F",       "wished_delivery_date":"",       "wished_delivery_time":null,       "store_pickup":"F",       "shipping_message":"빠른 배송 부탁드립니다.",       "order_place_id":"mobile",       "ordering_product_code":"P00000HK",       "ordering_product_name":"카페24 샘플 상품1",       "claim_reason_type": "P",       "claim_reason": "not satisfied",       "claim_reason_type_text": "상품 불만족"     } }                   |
| 90074 | When return statuses have been changed in bulk on the store | {   "event_no": 90074,   "resource":{     "mall_id":"cafe24bestshop",     "event_shop_no":"1",     "order_id":"20200528-0000019,20200513-0000040"   } }  |
| 90028 | When an order's exchange status has been changed on the store | {   "event_no": 90028,   "resource":{     "mall_id":"cafe24bestshop",     "event_shop_no":"1",     "order_id":"20200716-0000023",     "payment_gateway_name":"inicis",     "currency":"KRW",     "order_date":"2020-07-16T02:20:20+09:00",     "order_place_name":"naver pay",     "member_id":"gdhong",     "member_authentication":null,     "buyer_name":"Jessica Hong",     "buyer_email":"gdhong@cafe24corp.com",     "buyer_phone":"02-0000-0000",     "buyer_cellphone":"010-2424-2424",     "group_no_when_ordering":"1",     "first_order":"T",     "order_from_mobile":"T",     "paid":"T",     "payment_date":"2020-07-17T15:24:07+09:00",     "billing_name":"Jessica Hong",     "bank_code":"",     "payment_method":"card",     "easypay_name":"",     "use_escrow":"F",     "bank_account_no":"382-222254-13-001",     "order_price_amount":"24680.00",     "membership_discount_amount":"0.00",     "actual_payment_amount":"24580",     "mileage_spent_amount":"100.00",     "cancel_date":null,     "shipping_fee":"0.00",     "shipping_type":"A",     "shipping_status":"F",     "wished_delivery_date":"",     "wished_delivery_time":null,     "store_pickup":"F",     "shipping_message":"Quick Delivery please.",     "order_place_id":"mobile",     "ordering_product_code":"P00000HK",     "ordering_product_name":"Sample Product Name1"   } }  |
| 90029 | When an order's refund status has been changed on the store | {   "event_no": 90029,   "resource":{     "mall_id":"cafe24bestshop",     "event_shop_no":"1",     "order_id":"20200716-0000023",     "payment_gateway_name":"dacom",     "currency":"KRW",     "order_date":"2020-07-16T02:20:20+09:00",     "order_place_name":"naver pay",     "member_id":"gdhong",     "member_authentication":null,     "buyer_name":"Jessica Hong",     "buyer_email":"gdhong@cafe24corp.com",     "buyer_phone":"02-0000-0000",     "buyer_cellphone":"010-2424-2424",     "group_no_when_ordering":"1",     "first_order":"F",     "order_from_mobile":"T",     "paid":"T",     "payment_date":"2020-07-17T15:24:07+09:00",     "billing_name":"Jessica Hong",     "bank_code":"",     "payment_method":"card",     "easypay_name":"",     "use_escrow":"F",     "bank_account_no":"382-222254-13-001",     "order_price_amount":"24680.00",     "membership_discount_amount":"0.00",     "actual_payment_amount":"24580",     "mileage_spent_amount":"100.00",     "cancel_date":null,     "shipping_fee":"0.00",     "shipping_type":"A",     "shipping_status":"T",     "wished_delivery_date":"",     "wished_delivery_time":null,     "return_confirmed_date":null,     "store_pickup":"F",     "shipping_message":"Quick Delivery please.",     "order_place_id":"mobile",     "ordering_product_code":"P00000HK",     "ordering_product_name":"Sample Product Name1"   } }  |
| 90073 | When refund statuses have been changed in bulk on the store | {   "event_no": 90073,   "resource":{      "mall_id":"cafe24bestshop",     "event_shop_no":"1",     "order_id":"20200529-0000015,20200527-0000078"   } }  |
| 90031 | When a product has been added to a processed order on the store | {   "event_no": 90031,   "resource":{     "mall_id":"cafe24bestshop",     "event_shop_no":"1",     "order_id":"20191009-0000126",     "payment_gateway_name":"",     "currency":"KRW",     "order_date":"2019-10-09T15:52:56+09:00",     "order_place_name":"naver pay",     "member_id":"gdhong",     "member_authentication":"B",     "buyer_name":"Jessica Hong",     "buyer_email":"gdhong@cafe24corp.com",     "buyer_phone":"02-0000-0000",     "buyer_cellphone":"010-2424-2424",     "group_no_when_ordering":"13",     "first_order":"F",     "order_from_mobile":"F",     "paid":"M",     "payment_date":"2019-10-09T15:53:08+09:00",     "billing_name":"Jessica Hong",     "bank_code":"bank_82",     "payment_method":"cash",     "easypay_name":"",     "use_escrow":"F",     "bank_account_no":"382-222254-13-001",     "order_price_amount":"24680.00",     "membership_discount_amount":"0.00",     "actual_payment_amount":"24580",     "mileage_spent_amount":"100.00",     "cancel_date":null,     "shipping_fee":"0.00",     "shipping_type":"A",     "shipping_status":"F",     "wished_delivery_date":"Quick delivery please.",     "wished_delivery_time":"ASAP",     "shipping_message":"",     "order_place_id":"self",     "ordering_product_code":"P0000BUC,P0000BUB",     "ordering_product_name":"Sample Product Name 1,Sample Product Name 2" }  |
| 90064 | When an order's shipping information has been changed on the store | {   "event_no": 90064,   "resource":{     "mall_id":"cafe24bestshop",     "event_shop_no":"1",     "order_id":"20200717-0024054",     "order_place_id":"self"   } }  |
| 90066 | When an admin memo has been added to an order on the store | {     "event_no": 90066,     "resource": {        "mall_id":"cafe24bestshop",        "event_shop_no":"1",        "order_id":"20200717-0000092",        "requested_date":"2020-07-17 15:38:22",        "order_place_id":"shopn",        "ordering_product_code":"P00000TW",        "ordering_product_name":"카페24 샘플 상품1",        "executor_id":"sample7eBNEqSfkd7I8hoA",        "execute_method":"V2X"     } }  |
| 90068 | When an admin memo has been edited on an order on the store | {     "event_no": 90068,     "resource": {        "mall_id":"cafe24bestshop",        "event_shop_no":"1",        "order_id":"20200114-0002249",        "requested_date":"2020-01-22 10:21:51",        "order_place_id":"mobile",        "executor_id":"sample7eBNEqSfkd7I8hoA",        "execute_method":"V2X"     } }  |
| 90069 | When an admin memo has been deleted from an order on the store | {     "event_no": 90069,     "resource": {        "mall_id":"cafe24bestshop",        "event_shop_no":"1",        "order_id":"20190715-0000014",        "requested_date":"2019-07-15 08:53:46",        "order_place_id":"self",        "executor_id":"sample7eBNEqSfkd7I8hoA",        "execute_method":"V2X"     } }  |
| 90070 | When a checkout form has been deleted on the store | {   "event_no": 90070,   "resource":{     "mall_id":"cafe24bestshop",     "event_shop_no":"1",     "order_id":"20200228-0000016"   } }  |
| 90084 | When items are added to shopping cart | {   "event_no": 90084,   "resource": {     "mall_id": "cafe24bestshop",     "event_shop_no": "1",     "member_id": "sampleid",     "shipping_type": "A",     "product_no": 781,     "variant_code": "P0000BEB000A",     "quantity": 1,     "product_bundle": "F"   } }  |
| 90162 | When a tracking number submitted to the store has been changed | {  "event_no": 90162, "resource":{  "mall_id": "cafe24bestshop",  "event_shop_no": "1",  "order_id": "20200717-0029236",  "shipping_code": "D-20220723-0000019-00",  "shipping_company_code": "0001",  "tracking_no": "123456789123"   } }  |

### Store>Customers

| Event no. | Event | Sample data |
| --- | --- | --- |
| 90032 | When a customer signs up for an account on the store | {   "event_no": 90032,   "resource":{     "mall_id":"cafe24bestshop",     "event_shop_no":"1",     "member_id":"gdhong",     "group_no":1,     "name":"Jake Park",     "nick_name":"vjakiev",     "name_english":"",     "name_phonetic":"",     "created_date":"2020-07-17T15:26:00+09:00",     "member_authentication":"T",     "birthday":"",     "gender":"",     "phone":"02-0000-0000",     "cellphone":"010-2468-2468",     "sms":"T",     "email":"gdhong@cafe24corp.com",     "news_mail":"T",     "total_mileage":"0.00",     "available_mileage":"0.00",     "recommend_id":"bestmember",     "residence":"",     "use_mobile_app":"T",     "member_type":"p"   } }  |
| 90063 | When a customer links their social media account to the store | {   "event_no": 90063,   "resource":{     "mall_id":"cafe24bestshop",     "event_shop_no":"1",     "member_id":"member",     "social_name": "kakao",     "social_member_code": 123456,   } }  |
| 90080 | When a customer's account information has been changed | {   "mall_id":"cafe24bestshop",   "event_shop_no":"1",   "member_id":"gdhong",   "diff_key": [       "name",       "phone",       "cellphone",       "gender",       "birthday"    ],   "sub_event_code":"EC_FRONT" }  |
| 90143 | When a customer signs in | {   "event_no": 90143,   "mall_id": "cafe24bestshop",   "event_shop_no": "1",   "member_id": "sampleid",   "group_name": "Standard Membership",   "inflow_name": "PC" }  |
| 90144 | When a customer's customer level has been updated | {   "event_no": 90144,   "mall_id": "cafe24bestshop",   "domain": "cafe24bestshop.cafe24.com" }  |
| 90145 | When a customer's account has been deactivated on the store | {   "mall_id": "cafe24bestshop",   "event_shop_no": "90145",   "member_id": "sampleid1, sampleid2, sampleid3" }  |
| 90146 | When a customer's account has been reactivated on the store | {   "mall_id": "cafe24bestshop",   "event_shop_no": "90146",   "member_id": "sampleid1, sampleid2, sampleid3" }  |
| 90147 | When a customer's account has been deleted from the store | {   "mall_id": "cafe24bestshop",   "event_shop_no": "90147",   "member_id": "sampleid1, sampleid2, sampleid3" }  |
| 90148 | When the points balance of a customer with a store account has been changed | {     "event_no": 90148,     "resource": {         "mall_id": "cafe24bestshop",         "shop_no": "1",         "member_id": "sampleid1",         "mileage_money": 100,         "avail_mileage": 1000,         "issue_datetime": "2022-01-25 16:54:45",         "case": "B",         "case_text": "points issued as a refund following an order cancellation",         "reason": null     } }  |

### Store>Boards

| Event no. | Event | Sample data |
| --- | --- | --- |
| 90033 | When a board post has been posted on the store | {   "event_no": 90033,   "resource":{     "mall_id":"cafe24bestshop",     "event_shop_no":"1",     "board_no":9,     "no":274,     "has_parent":"T",     "member_id":"bestmember",     "writer":"bestmember"   } }  |
| 90034 | When a comment has been posted on a board post in the store | {   "event_no": 90034,   "resource":{     "mall_id":"cafe24bestshop",     "event_shop_no":"1",     "board_no":8,     "member_id":"cafe24bestshop",     "writer":"Jake Park",     "comment_member_id":"33578422@n",     "comment_writer":"Jenny"   } }  |
| 90035 | When an urgent request has been sent on the store | {   "event_no": 90035,   "resource":{     "mall_id":"cafe24bestshop",     "event_shop_no":"1",     "member_id":null,     "writer":"bestmember"   } }  |
| 90036 | When a board post has been deleted from the store | {   "event_no": 90036,   "resource":{     "mall_id":"cafe24bestshop",     "event_shop_no":"1",     "board_no":4,     "no":81,     "member_id":"bestmember",     "writer":"bestmember"   } }  |
| 90037 | When a board post comment has been deleted from the store | {   "event_no": 90037,   "resource":{     "mall_id":"cafe24bestshop",     "event_shop_no":"1",     "board_no":6,     "member_id":"gdhong",     "writer":"Jake Park",     "comment_member_id":"gdhong",     "comment_writer":"Jenny"   } }  |
| 90038 | When an urgent request has been deleted from the store | {   "event_no": 90038,   "resource":{     "mall_id":"cafe24bestshop",     "event_shop_no":"1",     "member_id":"gdhong",     "writer":"Jake Park"   } }  |
| 90039 | When a board post has been edited on the store | {   "event_no": 90039,   "resource":{     "mall_id":"cafe24bestshop",     "event_shop_no":"1",     "board_no":1,     "no":82,     "has_parent":"F",     "member_id":"gdhong",     "writer":"Jake Park"   } }  |

### Store>Product categories

| Event no. | Event | Sample data |
| --- | --- | --- |
| 90042 | When a product category has been added to the store | {   "event_no": 90042,   "resource":{     "mall_id":"cafe24bestshop",     "event_shop_no":"1",     "category_no":96,     "category_name":"Private Order",     "use_display":"F",     "use_main":"F",     "display_type":"A",     "product_display_scope":"A",     "product_display_type":"A",     "product_display_key":"R",     "product_display_sort":"D",     "soldout_product_display":"N",     "sub_category_product_display":"F"   } }  |
| 90043 | When a product category has been edited on the store | {   "event_no": 90043,   "resource":{     "mall_id":"cafe24bestshop",     "event_shop_no":"1",     "category_no":24,     "category_name":"(Category) Outerwear",     "use_display":"T",     "use_main":"T",     "display_type":"A",     "product_display_scope":"A",     "product_display_type":"A",     "product_display_key":"R",     "product_display_sort":"D",     "soldout_product_display":"N",     "sub_category_product_display":"T"   } }  |
| 90046 | When a product category's layout settings have been changed in bulk on the store | {   "event_no": 90046,   "resource":{     "mall_id":"cafe24bestshop",     "event_shop_no":"1",     "product_display_scope":"A",     "product_display_type":"A",     "product_display_key":"U",     "product_display_sort":"A"   } }  |
| 90044 | When a product category has been deleted from the store | {   "event_no": 90044,   "resource":{     "mall_id":"cafe24bestshop",     "event_shop_no":"1",     "category_no":91   } }  |
| 90045 | When a product category's layout order has been changed on the store | {   "event_no": 90045,   "resource":{     "mall_id":"cafe24bestshop",     "event_shop_no":"1"   } }  |

### Store>Supplier

| Event no. | Event | Sample data |
| --- | --- | --- |
| 90090 | When a supplier has been added to the store | {  "event_no": 90090,   "resource":{     "mall_id": "cafe24bestshop",     "event_shop_no": "1",     "supplier_code": "S0000000",     "supplier_name": "Default Supplier",     "use_supplier": "T",     "trading_type": "D",     "supplier_type": "WS",     "status": "A",     "payment_type": "D",     "commission": "0.00",     "payment_period": "A"   } }  |
| 90091 | When a supplier added to the store has been edited | {   "event_no": 90091,   "resource":{     "mall_id": "cafe24bestshop",     "event_shop_no": "1",     "supplier_code": "S0000000",     "supplier_name": "Default Supplier",     "use_supplier": "T",     "trading_type": "D",     "supplier_type": "WS",     "status": "A",     "payment_type": "D",     "commission": "0.00",     "payment_period": "A"   } }  |
| 90092 | When a supplier added to the store has been edited in bulk | {  "event_no": 90092,   "resource":{     "mall_id": "cafe24bestshop",     "event_shop_no": "1",     "supplier_code": "S0000000,S000000A,S000000B"   } }  |
| 90093 | When a supplier added to the store has been deleted | {  "event_no": 90093,   "resource":{     "mall_id": "cafe24bestshop",     "event_shop_no": "1",     "supplier_code": "S0000000"   } }  |

### Store>Shipping carrier (will be updated)

| Evnet no. | Event | Sample data |
| --- | --- | --- |
| 90100 | When a shipping carrier has been added to the store | {     "event_no": 90100,     "resource": {         "mall_id": "cafe24bestshop",         "event_shop_no": "1",         "sc_id": "3",         "sc_name": "FASTBOX",         "is_basic": "T",         "phone1": "1588-3413",         "phone2": "1588-3413",         "email": "gdhong@cafe24corp.com",         "shipping_money": "3000",         "homepage": "www.fastbox.com",         "trace_url": "https://www.fastbox.com/ko/tool/parcel/tracking?gnbInvcNo=000000000000",         "sender_name": "cafe24bestshop",         "sender_phone": "010-2424-2424",         "sender_cellphone": "010-2424-2424",         "weight": "15",         "volume": "20",         "shipping_type": "01",         "box_type": "01",         "sender_zipcode": "07071",         "sender_address1": "15 Boramaero 5gil Dongjakgu",         "sender_address2": "Cafe24 22F",         "executor_id":"cafe24bestshop",         "execute_method":"ADMIN"     } }  |
| 90101 | When a shipping carrier added to the store has been edited | {     "event_no": 90101,     "resource": {         "mall_id": "cafe24bestshop",         "event_shop_no": "1",         "sc_id": "3",         "sc_name": "FASTBOX",         "is_basic": "T",         "phone1": "1588-3413",         "phone2": "1588-3413",         "email": "gdhong@cafe24corp.com",         "shipping_money": "3000",         "homepage": "www.fastbox.com",         "trace_url": "https://www.fastbox.com/ko/tool/parcel/tracking?gnbInvcNo=000000000000",         "executor_id":"cafe24bestshop",         "execute_method":"ADMIN"     } }  |
| 90102 | When a shipping carrier added to the store has been deleted | {     "event_no": 90102,     "resource": {         "mall_id": "cafe24bestshop",         "event_shop_no": "1",         "sc_id": "3",         "executor_id":"cafe24bestshop",         "execute_method":"ADMIN"     } }  |

### Store>My Store

| Event no. | Event | Sample data |
| --- | --- | --- |
| 90110 | When an additional store has been added to the store | {  "event_no": 90110,   "resource":{     "mall_id": "cafe24bestshop",     "shop_no": "2",     "shop_name": "MultiShop",     "language": "en_US",     "currency": "USD",     "is_active": "T"   } }  |
| 90111 | When an additional store added to the store has been edited | { "event_no": 90111,   "resource":{     "mall_id": "cafe24bestshop",     "shop_no": "2",     "shop_name": "MultiShop"     "is_active": "T"   } }  |
| 90112 | When an additional store added to the store has been deleted | { "event_no": 90112,   "resource":{     "mall_id":"cafe24bestshop",     "event_shop_no":"1"   } }  |
| 90113 | When a sub-admin has been added to the store | { "event_no": 90113,   "resource":{     "mall_id":"cafe24bestshop",     "sub_admin_id":"subadmin1",     "sub_admin_type":"A",     "user_name":"John Doe",     "available":"T"   } }  |
| 90114 | When a sub-admin added to the store has been edited | { "event_no": 90114,   "resource":{     "mall_id":"cafe24bestshop",     "sub_admin_id":"subadmin1",     "sub_admin_type":"A",     "user_name":"John Doe",     "available":"T",     "multishop_access_authority":"{1: 'T'}, {2: 'F'}, {3: 'T'}, {4: 'F'}"   } }  |
| 90115 | When a sub-admin added to the store has been deleted | { "event_no": 90115,   "resource":{     "mall_id":"cafe24bestshop",     "sub_admin_id":"subadmin1",   } }  |
| 90116 | When settings have changed concerning the Provision of Personal Information to Third Parties | { "event_no": 90116,   "resource":{   "mall_id": "cafe24bestshop",   "event_shop_no": "1",   "use_information_agreement": "T",   "use_consignment_agreement": "T"   } }  |
| 90117 | When an online store domain is added | { "event_no": 90117,   "resource":{   "mall_id": "cafe24bestshop",   "domain": "cafe24bestshop.cafe24.com"   } }  |
| 90119 | When an online store domain is deleted | { "event_no": 90119,   "resource":{   "mall_id": "cafe24bestshop",   "domain": "cafe24bestshop.cafe24.com"   } }  |
| 90121 | If the store profile info is edited | { "event_no": 90121,   "resource":{   "mall_id": "cafe24bestshop",     "event_shop_no":"1",   "shop_name":"cafe24bestshop"   "country":"ko_KR"   "zipcode":"07071"   "address1":"15 Boramaero 5gil Dongjakgu"   "address2":"Cafe24 22F"   "president_phone":"02-3284-0300"   } }  |
| 90166 | When the store has been deleted | {   "event_no": 90166,   "resource": {     "mall_id": "cafe24bestshop",     "event_shop_no": "1",     "trigger_name": "When the store has been deleted"   } }   |
| 90167 | When the store is deactivated | {   "event_no": 90167,   "resource": {     "trigger_name": "When the store is deactivated",     "sample": {     "event_shop_no": "1",       "mall_id": "cafe24bestshop"     }   } }  |
| 90168 | When the store is reactivated | {   "event_no": 90168,   "resource": {     "mall_id": "cafe24bestshop",     "event_shop_no": "1",     "trigger_name": "When the store is reactivated"   } }   |
| 90169 | When the store is blocked | {   "event_no": 90169,   "resource": {     "mall_id": "cafe24bestshop",     "event_shop_no": "1",     "trigger_name": "When the store is blocked"   } }   |

### Store > Settings

| Event NO. | Event | Sample data |
| --- | --- | --- |
| 90142 | When Kakao Sync settings have changed | {     "event_no": 90142,     "resource": {         "mall_id": "cafe24bestshop",         "event_shop_no": "1",         "kakaosync_used": "F",         "client_id": "81b6ceb301d48df7670859c8db411ef4"     } }   |

### Store > Incentive

| Event NO. | Event | Sample data |
| --- | --- | --- |
| 90047 | When an incentive is added to the store | {      "event_no": 90047,      "resource": {         "mall_id": "cafe24bestshop",         "shop_no": 1,         "benefit_no": 3,         "use_benefit": "T",         "benefit_name": "SampleBenefit",         "benefit_start_date": "2019-01-01T12: 00: 00+09: 00",         "benefit_end_date": "2019-01-31T12: 00: 00+09: 00",         "customer_group_list": [           8,           9         ],         "product_binding_type": "P",         "product_list": [           17,           25,           29         ],         "add_category_list": null,         "except_category_list": [           168,           175,           177         ]     } }  |
| 90048 | When an incentive on the store is edited | {      "event_no": 90048,      "resource": {         "mall_id": "cafe24bestshop",         "shop_no": 1,         "benefit_no": 3,         "use_benefit": "T",         "benefit_name": "SampleBenefit",         "benefit_start_date": "2019-01-01T12: 00: 00+09: 00",         "benefit_end_date": "2019-01-31T12: 00: 00+09: 00",         "customer_group_list": [           8,           9         ],         "product_binding_type": "P",         "product_list": [           17,           25,           29         ],         "add_category_list": null,         "except_category_list": [           168,           175,           177         ]     } }  |
| 90050 | When an incentive on the store is deleted | {     "event_no": 90050,     "resource": {         "mall_id": "cafe24bestshop",         "shop_no": 1,         "benefit_no": 3     } }   |

### Store >   Coupon

| Event NO. | Event | Sample data |
| --- | --- | --- |
| 90151 | When a coupon of the store has been edited | {     "event_no": 90151,     "resource": {         "mall_id": "cafe24bestshop",         "event_shop_no": 1,         "coupon_type": "O",         "coupon_no": 6072120804600000001,         "coupon_name": "Discount Coupon",         "issue_status_code": "ISSUING",         "issue_status": "Active"     } }  |
| 90152 | When a coupon of the store has been edited | {     "event_no": 90152,     "resource": {         "mall_id": "cafe24bestshop",         "event_shop_no": 1,         "coupon_type": "O",         "coupon_no": 6072120804600000001     } }  |
| 90153 | If a coupon is registered on the online store | {     "event_no": 90153,     "resource": {         "mall_id": "cafe24bestshop",         "event_shop_no": 1,         "coupon_type": "O",         "coupon_no": 6072120804600000001,         "coupon_name": "Discount Coupon",         "issue_status_code": "ISSUING",         "issue_status": "Active"     } }  |
| 90154 | If the issuance status of an online store coupon has been modified | {     "event_no": "90154",     "resource": {         "mall_id": "cafe24bestshop",         "event_shop_no": 1,         "coupon_no": 6072120804600000001,         "coupon_name": "Discount Coupon",         "issue_status_code": "ISSUING",         "issue_status": "Active",         "mode": "restart",         "type": "now",         "start_date": "2022-01-01 14:39",         "end_date": "2022-01-01 16:38"     } }  |

## Store event parameters

| Parameter | Description | Memo |
| --- | --- | --- |
| event_no | Event type | See event no. |
| mall_id | Store ID |  |
| event_shop_no | Multi-language store number A unique number assigned to a store using the default store language or other languages. |  |
| product_no | Product number system assigned code. This code cannot be duplicated. |  |
| created_date | Date when product was registered. | Date |
| updated_date | Date when product was modified. | Date |
| product_name | Product name | Maximum [250] characters |
| eng_product_name | Product name (English) English name of product. Necessary when shipping abroad. | Maximum [250] characters |
| supply_product_name | Supplier product name | Maximum [250] characters |
| model_name | Model | Maximum [100] characters |
| custom_product_code | Custom product code You may assign this code manually in case of stock management or other reasons. | Maximum [40] characters |
| product_condition | Product condition | N: New arrival B: Returned R: In stock U: Used E: Display product F: Refurbished S: Damaged |
| summary_description | Product Summary Description | Maximum [255] characters |
| simple_description | Simple Product Description |  |
| description | Detail description of product |  |
| display | Display status | T: Display F: Do not display |
| selling | Sale status | T: Sell F: Do not sell |
| retail_price | Product retail price | Between [0] and [2147483647] |
| supply_price | Product supply price | Between [0] and [2147483647] |
| price | Product price | Between [0] and [2147483647] |
| price_content | Replacement text for price | Maximum [20] characters |
| adult_certification | Whether product requires adult certification | T: Used F: Not used |
| manufacturer_code | Manufacturer code | Type: [A-Z0-9] Between [8] and [8] characters |
| supplier_code | Supplier code | Type: [A-Z0-9] Between [8] and [8] characters |
| brand_code | Brand code | Type: [A-Z0-9] Between [8] and [8] characters |
| trend_code | Trend code | Type: [A-Z0-9] Between [8] and [8] characters |
| made_date | Date of manufacture | Date |
| release_date | Date of release | Date |
| origin_place_code | Code of origin |  |
| manufacturer_code | Manufacturer code | Type: [A-Z0-9] Between [8] and [8] characters |
| translated | Whether translated or not | T: Translated F: Not translated |
| status_text | Description of current status |  |
| use_soldout | Whether to display out-of-stock products | T: Display F: Do not display |
| order_id | Order ID |  |
| payment_gateway_name | Payment gateway name |  |
| currency | Currency | KRW: ￦ Won USD: $ Dollar JPY : ¥ Yen |
| order_date | Ordered date | Date |
| order_place_name | Order path text |  |
| member_id | Member ID |  |
| member_authentication | Member authentication | T: Authorized F: Unauthorized B: Special treatment member J: Under 14 |
| buyer_name | Buyer name |  |
| buyer_email | Buyer Email |  |
| buyer_phone | Buyer phone number |  |
| buyer_cellphone | Buyer mobile number |  |
| group_no_when_ordering | Customer group number when ordering |  |
| first_order | First order | T: First order F: Not first order |
| order_from_mobile | Whether order was made on mobile | T: Made on mobile F: Was not made on mobile |
| paid | Whether order was paid for | T: Paid F: Unpaid M: Partially paid |
| payment_date | Payment date | Date |
| billing_name | Billing name |  |
| bank_code | Bank code | bank_code |
| payment_method | Payment method code | cash: Bank deposit card: Credit card cell: Mobile tcash: Bank transfer prepaid: Digital wallet balance credit: Credits point: Points pointfy: Transferable points cvs: Convenience store cod: Cash on delivery (COD) coupon: Coupon market_discount: Marketplace discount etc: Other |
| easypay_name | Easypay payment gateway name |  |
| use_escrow | Whether customer used escrow | T : Used escrow F : Did not use escrow |
| bank_account_no | Store bank account account for the order |  |
| order_price_amount | Order total |  |
| membership_discount_amount | Customer discount |  |
| actual_payment_amount | Amount paid |  |
| mileage_spent_amount | Points used |  |
| shipping_fee | Shipping fee |  |
| shipping_type | Delivery type | A: Domestic B: Abroad |
| shipping_status | Delivery status | F: Pre-shipment M: In transit T: Delivered W: Shipment on hold |
| wished_delivery_date | Preferred delivery date |  |
| wished_delivery_time | Preferred delivery time |  |
| store_pickup | Store pickup | T: Store pickup F: No store pickup |
| shipping_message | Delivery instructions |  |
| order_place_id | Available order path | cafe24: Cafe24 mobile: Mobile web mobile_d: Mobile app NCHECKOUT: NAVER Pay inpark: Interpark auction: Auction sk11st: 11th Street gmarket: Gmarket coupang: Coupang shopn: Smart store |
| ordering_product_code | Order product code |  |
| ordering_product_name | Order product name |  |
| cancel_date | Order cancellation date |  |
| return_confirmed_date | Date of confirming product return |  |
| included_deferpay_order | Whether to include COD |  |
| deferpay_order_id | COD order number |  |
| requested_date | Date of edited admin memo | When an admin leaves a memo on an order processed on the store. |
| name | Customer name |  |
| nick_name | Nickname of admin | Maximum [50] characters |
| name_english | Name (English) |  |
| name_phonetic | Name expressed phonetically (Japanese) |  |
| created_date | Signup day |  |
| birthday | Birthday of the customer |  |
| gender | Gender | M: Male F: Female |
| phone | Phone number |  |
| cellphone | Mobile number |  |
| sms | Whether to subscribe to SMS | T: Subscribe F: Do not subcribe |
| email | Email |  |
| news_mail | Whether to receive email | T: Subscribe F: Do not subcribe |
| total_mileage | Total points |  |
| available_mileage | Available points |  |
| recommend_id | Recommended ID |  |
| residence | Area code |  |
| use_mobile_app | Whether using mobile app or not | T: Yes F: No |
| member_type | Account type | P: Individual C: Business F: Foreigner |
| board_no | Board number |  |
| has_parent | Whether there is a parent board | When a post is added T: Yes F: No |
| writer | Author |  |
| comment_member_id | Commenter ID |  |
| comment_writer | Commenter name |  |
| retail_price | Retail price of product | Between [0] and [2147483647] |
| category_no | A unique identifier assigned to a product category. |  |
| category_name | Category name | Maximum [50] characters |
| use_display | Settings for displaying product category Whether or not the product category is displayed on the main page. | T : Display F : Do not display |
| use_main | Settings for displaying on main page | T : Display F : Do not display |
| display_type | Display settings | A: PC + Mobile P: PC M: Mobile F: Not displayed |
| product_display_scope | Category display scope | A : All G : By area |
| product_display_type | Product layout sorting method | A : Automatic sorting U : Custom sorting M : Automatic + Custom |
| product_display_key | Product layout key | A: Layout order R: Date added U: Date edited N: Product name P: Price S: Sales C: Views L: Likes |
| product_display_sort | Product layout sorting order | D: In descending order A: In ascending order |
| soldout_product_display | Out-of-stock product layout settings | B: Display at the bottom N: Display in same order |
| sub_category_product_display | Subcategory product layout settings Whether to display products in both the current category and its sub-categories. | T : Display F : Do not display |
| sub_event_code | Customer information edit place | EC_ADMIN : When an admin edits customer information through the store's admin page EC_FRONT : When a customer edits their customer information on the store website (front) |
| supplier_name | Supplier name |  |
| use_supplier | Whether using supplier or not | T: Yes F: No |
| trading_type | Supplier type | D: Purchasing agent C: Direct shipping |
| supplier_type | Supplier structure | WS: Wholesaler SF: Purchasing agent BS: Vendor ET: Other |
| status | Transaction status | A: Continuing P: Suspended N: Terminated |
| payment_type | Payout type | P : Sales-based commission D : Lump-sum |
| commission | Commission rate |  |
| payment_period | Settlement cycle | 0: Not selected C: Daily B: Weekly A: Monthly |
| sc_id | Shipping carrier ID |  |
| sc_name | Shipping carrier name |  |
| is_basic | Whether using default shipping carrier or not | T : Yes F : No |
| phone1 | Primary phone |  |
| phone2 | Secondary phone |  |
| shipping_money | Default shipping fee |  |
| trace_url | URL for tracking shipment |  |
| sender_name | Sender name |  |
| sender_phone | Sender primary phone |  |
| sender_cellphone | Sender mobile number |  |
| weight | Shipping weight |  |
| volume | Product volume |  |
| shipping_type | Shipping type | 01 : Prepayment 02 : Pay after delivery (PAD) 03 : On credit |
| box_type | Box type | 01 : Extra small 02 : small 03 : Medium 04 : Large 05 : Extra large |
| sender_zipcode | Send address (Zip code) |  |
| sender_address1 | Send address (Address Line 1) |  |
| sender_address2 | Send address (Address Line 2) |  |
| sShopName | Online store name |  |
| sLanguage | Language code | ko_KR : Korean en_US : English zh_CN : Chinese (Simplified) zh_TW : Chinese (Traditional) ja_JP : Japanese vi_VN : Vietnamese en_PH : English |
| sCurrency | Payment currency | KRW / USD / JPY / CNY / TWD / EUR / BRL / VND / PHP |
| sIsActive | Whether active or not | T : Active F : Disabled |
| sub_admin_id | Sub-admin ID |  |
| sub_admin_type | Sub-admin type | A : Store admin S : Supplier admin |
| user_name | Sub-admin name | Sub-admin names configured on the default store/Supplier sub-admin names only |
| multishop_access_authority | Permission to access multi-language store feature | T: Yes F: No |
| use_information_agreement | Require consent for Provision of Personal Information to Third Parties | T: Yes F: No |
| use_consignment_agreement | Require consent for Consignment of Personal Information Processing | T: Yes F: No |
| domain | domain |  |
| is_under14_joinable | Use settings for age-restricted account creation (Under 14) | T: Require age verification before usage F: Unauthorized account creation |
| kakaosync_used | Kakao Sync setup status | T: Yes F: No |
| group_name | Customer level |  |
| inflow_name | Traffic source | PC : Login with PC / Mobile : Login with M |
| country | Country of business Name of the country where the business is located. |  |
| zipcode | Postal code of business |  |
| address1 | Address 1 Business address (city / county / province) |  |
| address2 | Address 2 Business address (street address) |  |
| president_phone | Office phone number |  |
| Whether the product is bundle product | Whether the product is bundle product | T : Product bundlt F : Not a product bundle |
| benefit_no | Incentive number |  |
| use_benefit | Activation status | T : Active F : Inactive |
| benefit_name | Incentive name |  |
| benefit_start_date | Validity start date |  |
| benefit_end_date | Validity end date |  |
| customer_group_list | Eligible customer level |  |
| product_binding_type | Applicable products | A: All products P: Specific products E: All except for the selected products C: Specific categories |
| add_category_list | Selected product numbers | If applicable products are "Specific products (P)": Incentives are applied to the selected product numbers. If applicable products are "All except for the selected products (E)": Incentives are applied to all products, except for the selected product numbers. |
| add_category_list | Selected product category |  |
| except_category_list | Selected product category exceptions |  |
| Whether increased or decreased | Whether points were added or deducted | Increased(Added) / Decreased(Deducted) |
| Points amount | Amount of points added/deducted |  |
| Points balance | Total points after addition/deduction |  |
| Shopping Mall Number | Date added/deducted |  |
| Updated Date | Shop no. (Multi-language store no.) |  |
| Updated Datetime | Date and time added/deducted |  |
| sold_out_by_current_shop | Product is sold out | T: Out of stock, F: Not out of stock |  |
| sold_out | All store products are sold out | “1”:“T”,“2”:“F” |  |
| shop_no | Localized store no. |  |
| coupon_type | Coupon type | O: Online coupon / S: Offline coupon code |  |
| coupon_no | Coupon number |  |
| ccoupon_name | Coupon name |  |
| issue_status_code | Coupon issuance status code |  |
| issue_status | Coupon issuance status | Active |  |
| mode | Type of issuance status modification | pause : Pause issance / restart : Reactivate issuance |
| type | Details on types of issuance status modifications | Type of pause) later : Schedule a time for later / now : Pause issuance immediately Type of reactivation) later : Change reactivation date / now : Reactivate issuance immediately |
| start_date | Start date |
| end_date | Reactivation date | This field will be blank if the issuance is paused immediately. |
| claim_reason_type_text | Reason for return | Change of mind, Unsatisfactory product, Defective product, Shipping error |
| withdraw | Claim cancellation status | T: Withdrawn claim order / F: General Order |
| withdraw_type | Type of claim cancellation | This ingredient comes out only when the order's claim is withdrawn. C: Withdrawn Cancellation before paid / E: Withdrawn Exchanged before paid |
| case_text | Type of points | Points directly issued by the store operator, points issued as a refund following an order cancellation, etc. |
| case | Codes for the type of points | A, B, C, etc. |
| reason | Reason for issuance | Whenever API is used to increase or decrease points, the relevant reason is output. |
| executor_id | executor ID |  |
| execute_method | Type of executor |  |
| use_benefit | Incentive usage status |  |
| benefit_name | Incentive name |  |
| benefit_start_date | Incentive start date |  |
| benefit_end_date | Incentive end date |  |
| customer_group_list | Setting incentive customer eligibility |  |
| product_binding_type | Setting incentive product scope |  |
| product_list | Incentive applicable products |  |
| add_category_list | Incentive applicable product categories |  |
| except_category_list | Incentive excluded products |  |
| shipping_code | Shipment number |  |
| shipping_company_code | Shipping carrier code |  |
| tracking_no | Tracking number |  |

## Next page

**[Release](/app/front/app/launch)**