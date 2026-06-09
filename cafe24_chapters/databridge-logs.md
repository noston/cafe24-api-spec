# DATABRIDGE LOGS


## Databridge logs

```json
Endpoints    GET /api/v2/admin/databridge/logs
```

```json
GET /api/v2/admin/databridge/logs
```

### Databridge logs property list

| Attribute | Description |
| --- | --- |
| log_id | 로그 ID |
| mall_id | 쇼핑몰 ID |
| trace_id | Trace ID |
| requested_time | 전송일시 |
| request_endpoint | 요청 URL |
| request_body | 요청 내용 |
| success | 웹훅 발송 성공 여부 T : 성공 F : 실패 |
| response_http_code | 응답 http code |
| response_body | 응답 내용 |

### Retrieve a list of Databridge webhook logs   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 앱 읽기권한 (mall.read_application) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| requested_start_date날짜 | 발송 시작일시 |
| requested_end_date날짜 | 발송 종료일시 |
| success | 웹훅 발송 성공 여부   T : 성공 F : 실패 |
| since_log_id | 해당 로그 ID 이후 검색 |
| limit최소: [1]~최대: [10000] | 조회결과 최대건수 |

```bash
Retrieve a list of Databridge webhook logs        Retrieve a list of Databridge webhook logs       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/databridge/logs' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "logs": [        {            "log_id": "zj5sMJEBRpZEwGZ0UOOC",            "mall_id": "bestshop",            "trace_id": "ebc26aa3-fe56-4810-bb6f-5dcbc6db8933",            "requested_time": "2024-08-03T10:10:10+09:00",            "request_endpoint": "https://api.linkd.kr/webhook/simplepay-order",            "request_body": "{\"event_name\":\"create_order\",\"event_time\":\"2024-08-07T06:16:07+09:00\",\"event_data\":{\"mall_id\":\"bestshop\",\"shop_no\":1,\"member_id\":\"3456956195@k\",\"order_id\":\"20240807-0012613\",\"product_list\":[{\"product_no\":8991,\"variant_code\":\"P0000NHV00DL\",\"product_name\":\"[풀스택] NEW 에어스트 맨즈 아이스 슬랙스\",\"option_value\":\"사이즈=2XL (34~36), 색상=[MMSPT-08CHA] 숏 차콜그레이\",\"cate_no\":2088,\"cate_name\":\"맨즈 - 하의\",\"quantity\":1,\"product_price\":\"72000.00\",\"option_extra_price\":\"0.00\"},{\"product_no\":7288,\"variant_code\":\"P0000KUI00BR\",\"product_name\":\"에어윈드 맨즈 조거팬츠\",\"option_value\":\"색상=[MLSJT-06BEG] 모카베이지, 사이즈=2XL (34~36)\",\"cate_no\":2088,\"cate_name\":\"맨즈 - 하의\",\"quantity\":1,\"product_price\":\"59000.00\",\"option_extra_price\":\"0.00\"},{\"product_no\":11682,\"variant_code\":\"P0000RHI000C\",\"product_name\":\"[사은품] 에어프레시 크루 삭스 1개 (쿠폰 선택 시 재선택 필요)\",\"option_value\":\"사이즈=L (255~280mm), 색상=화이트\",\"cate_no\":-3,\"cate_name\":null,\"quantity\":1,\"product_price\":\"0.00\",\"option_extra_price\":\"0.00\"}],\"payment_method\":\"card\",\"is_paid\":\"T\",\"order_date\":\"2024-08-07T06:16:07+09:00\",\"pay_date\":\"2024-08-07T06:16:07+09:00\",\"first_order\":\"F\",\"regularpays\":\"F\",\"currency\":\"KRW\",\"payment_amount\":\"124450.00\",\"points_spent_amount\":\"0.00\",\"credits_spent_amount\":\"0.00\",\"shipping_fee\":\"0.00\"},\"analytics_data\":{\"event_source_url\":\"https://m.andar.co.kr/order/orderform.html?basket_type=all_buy&delvtype=A\",\"client_user_agent\":\"Mozilla/5.0 (Linux; Android 14; SM-F721N Build/UP1A.231005.007; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/114.0.0.0 Whale/1.0.0.0 Crosswalk/28.114.0.23 Mobile Safari/537.36 NAVER(inapp; search; 2000; 12.7.1)\",\"CVID\":\"CVID.505c50554a05016602.1722976985702\",\"CVID_Y\":\"CVID_Y.505c50554a05016602.1705717224905\",\"CVID_AD\":\"1722976985702.naverDA\",\"CVID_E\":null}}",            "success": "T",            "response_http_code": "200",            "response_body": "Message received okay."        },        {            "log_id": "dV7Ur3oBsq3B53njJIbP",            "mall_id": "bestshop",            "trace_id": "ebc26aa3-fe56-4810-bb6f-5dcbc6db8933",            "requested_time": "2024-08-03T10:10:10+09:00",            "request_endpoint": "https://api.linkd.kr/webhook/simplepay-order",            "request_body": "{\"event_name\":\"create_order\",\"event_time\":\"2024-08-07T06:16:07+09:00\",\"event_data\":{\"mall_id\":\"bestshop\",\"shop_no\":1,\"member_id\":\"3456956195@k\",\"order_id\":\"20240807-0012613\",\"product_list\":[{\"product_no\":8991,\"variant_code\":\"P0000NHV00DL\",\"product_name\":\"[풀스택] NEW 에어스트 맨즈 아이스 슬랙스\",\"option_value\":\"사이즈=2XL (34~36), 색상=[MMSPT-08CHA] 숏 차콜그레이\",\"cate_no\":2088,\"cate_name\":\"맨즈 - 하의\",\"quantity\":1,\"product_price\":\"72000.00\",\"option_extra_price\":\"0.00\"},{\"product_no\":7288,\"variant_code\":\"P0000KUI00BR\",\"product_name\":\"에어윈드 맨즈 조거팬츠\",\"option_value\":\"색상=[MLSJT-06BEG] 모카베이지, 사이즈=2XL (34~36)\",\"cate_no\":2088,\"cate_name\":\"맨즈 - 하의\",\"quantity\":1,\"product_price\":\"59000.00\",\"option_extra_price\":\"0.00\"},{\"product_no\":11682,\"variant_code\":\"P0000RHI000C\",\"product_name\":\"[사은품] 에어프레시 크루 삭스 1개 (쿠폰 선택 시 재선택 필요)\",\"option_value\":\"사이즈=L (255~280mm), 색상=화이트\",\"cate_no\":-3,\"cate_name\":null,\"quantity\":1,\"product_price\":\"0.00\",\"option_extra_price\":\"0.00\"}],\"payment_method\":\"card\",\"is_paid\":\"T\",\"order_date\":\"2024-08-07T06:16:07+09:00\",\"pay_date\":\"2024-08-07T06:16:07+09:00\",\"first_order\":\"F\",\"regularpays\":\"F\",\"currency\":\"KRW\",\"payment_amount\":\"124450.00\",\"points_spent_amount\":\"0.00\",\"credits_spent_amount\":\"0.00\",\"shipping_fee\":\"0.00\"},\"analytics_data\":{\"event_source_url\":\"https://m.andar.co.kr/order/orderform.html?basket_type=all_buy&delvtype=A\",\"client_user_agent\":\"Mozilla/5.0 (Linux; Android 14; SM-F721N Build/UP1A.231005.007; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/114.0.0.0 Whale/1.0.0.0 Crosswalk/28.114.0.23 Mobile Safari/537.36 NAVER(inapp; search; 2000; 12.7.1)\",\"CVID\":\"CVID.505c50554a05016602.1722976985702\",\"CVID_Y\":\"CVID_Y.505c50554a05016602.1705717224905\",\"CVID_AD\":\"1722976985702.naverDA\",\"CVID_E\":null}}",            "success": "F",            "response_http_code": "404",            "response_body": "{\"success\":false,\"error\":{\"message\" : \"\"\"Token \"4f735d6b-f18f-4eaf-969b-04f494ae29c0\" not found\"\"\",\"id\":null}}"        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/databridge/logs' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "logs": [        {            "log_id": "zj5sMJEBRpZEwGZ0UOOC",            "mall_id": "bestshop",            "trace_id": "ebc26aa3-fe56-4810-bb6f-5dcbc6db8933",            "requested_time": "2024-08-03T10:10:10+09:00",            "request_endpoint": "https://api.linkd.kr/webhook/simplepay-order",            "request_body": "{\"event_name\":\"create_order\",\"event_time\":\"2024-08-07T06:16:07+09:00\",\"event_data\":{\"mall_id\":\"bestshop\",\"shop_no\":1,\"member_id\":\"3456956195@k\",\"order_id\":\"20240807-0012613\",\"product_list\":[{\"product_no\":8991,\"variant_code\":\"P0000NHV00DL\",\"product_name\":\"[풀스택] NEW 에어스트 맨즈 아이스 슬랙스\",\"option_value\":\"사이즈=2XL (34~36), 색상=[MMSPT-08CHA] 숏 차콜그레이\",\"cate_no\":2088,\"cate_name\":\"맨즈 - 하의\",\"quantity\":1,\"product_price\":\"72000.00\",\"option_extra_price\":\"0.00\"},{\"product_no\":7288,\"variant_code\":\"P0000KUI00BR\",\"product_name\":\"에어윈드 맨즈 조거팬츠\",\"option_value\":\"색상=[MLSJT-06BEG] 모카베이지, 사이즈=2XL (34~36)\",\"cate_no\":2088,\"cate_name\":\"맨즈 - 하의\",\"quantity\":1,\"product_price\":\"59000.00\",\"option_extra_price\":\"0.00\"},{\"product_no\":11682,\"variant_code\":\"P0000RHI000C\",\"product_name\":\"[사은품] 에어프레시 크루 삭스 1개 (쿠폰 선택 시 재선택 필요)\",\"option_value\":\"사이즈=L (255~280mm), 색상=화이트\",\"cate_no\":-3,\"cate_name\":null,\"quantity\":1,\"product_price\":\"0.00\",\"option_extra_price\":\"0.00\"}],\"payment_method\":\"card\",\"is_paid\":\"T\",\"order_date\":\"2024-08-07T06:16:07+09:00\",\"pay_date\":\"2024-08-07T06:16:07+09:00\",\"first_order\":\"F\",\"regularpays\":\"F\",\"currency\":\"KRW\",\"payment_amount\":\"124450.00\",\"points_spent_amount\":\"0.00\",\"credits_spent_amount\":\"0.00\",\"shipping_fee\":\"0.00\"},\"analytics_data\":{\"event_source_url\":\"https://m.andar.co.kr/order/orderform.html?basket_type=all_buy&delvtype=A\",\"client_user_agent\":\"Mozilla/5.0 (Linux; Android 14; SM-F721N Build/UP1A.231005.007; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/114.0.0.0 Whale/1.0.0.0 Crosswalk/28.114.0.23 Mobile Safari/537.36 NAVER(inapp; search; 2000; 12.7.1)\",\"CVID\":\"CVID.505c50554a05016602.1722976985702\",\"CVID_Y\":\"CVID_Y.505c50554a05016602.1705717224905\",\"CVID_AD\":\"1722976985702.naverDA\",\"CVID_E\":null}}",            "success": "T",            "response_http_code": "200",            "response_body": "Message received okay."        },        {            "log_id": "dV7Ur3oBsq3B53njJIbP",            "mall_id": "bestshop",            "trace_id": "ebc26aa3-fe56-4810-bb6f-5dcbc6db8933",            "requested_time": "2024-08-03T10:10:10+09:00",            "request_endpoint": "https://api.linkd.kr/webhook/simplepay-order",            "request_body": "{\"event_name\":\"create_order\",\"event_time\":\"2024-08-07T06:16:07+09:00\",\"event_data\":{\"mall_id\":\"bestshop\",\"shop_no\":1,\"member_id\":\"3456956195@k\",\"order_id\":\"20240807-0012613\",\"product_list\":[{\"product_no\":8991,\"variant_code\":\"P0000NHV00DL\",\"product_name\":\"[풀스택] NEW 에어스트 맨즈 아이스 슬랙스\",\"option_value\":\"사이즈=2XL (34~36), 색상=[MMSPT-08CHA] 숏 차콜그레이\",\"cate_no\":2088,\"cate_name\":\"맨즈 - 하의\",\"quantity\":1,\"product_price\":\"72000.00\",\"option_extra_price\":\"0.00\"},{\"product_no\":7288,\"variant_code\":\"P0000KUI00BR\",\"product_name\":\"에어윈드 맨즈 조거팬츠\",\"option_value\":\"색상=[MLSJT-06BEG] 모카베이지, 사이즈=2XL (34~36)\",\"cate_no\":2088,\"cate_name\":\"맨즈 - 하의\",\"quantity\":1,\"product_price\":\"59000.00\",\"option_extra_price\":\"0.00\"},{\"product_no\":11682,\"variant_code\":\"P0000RHI000C\",\"product_name\":\"[사은품] 에어프레시 크루 삭스 1개 (쿠폰 선택 시 재선택 필요)\",\"option_value\":\"사이즈=L (255~280mm), 색상=화이트\",\"cate_no\":-3,\"cate_name\":null,\"quantity\":1,\"product_price\":\"0.00\",\"option_extra_price\":\"0.00\"}],\"payment_method\":\"card\",\"is_paid\":\"T\",\"order_date\":\"2024-08-07T06:16:07+09:00\",\"pay_date\":\"2024-08-07T06:16:07+09:00\",\"first_order\":\"F\",\"regularpays\":\"F\",\"currency\":\"KRW\",\"payment_amount\":\"124450.00\",\"points_spent_amount\":\"0.00\",\"credits_spent_amount\":\"0.00\",\"shipping_fee\":\"0.00\"},\"analytics_data\":{\"event_source_url\":\"https://m.andar.co.kr/order/orderform.html?basket_type=all_buy&delvtype=A\",\"client_user_agent\":\"Mozilla/5.0 (Linux; Android 14; SM-F721N Build/UP1A.231005.007; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/114.0.0.0 Whale/1.0.0.0 Crosswalk/28.114.0.23 Mobile Safari/537.36 NAVER(inapp; search; 2000; 12.7.1)\",\"CVID\":\"CVID.505c50554a05016602.1722976985702\",\"CVID_Y\":\"CVID_Y.505c50554a05016602.1705717224905\",\"CVID_AD\":\"1722976985702.naverDA\",\"CVID_E\":null}}",            "success": "F",            "response_http_code": "404",            "response_body": "{\"success\":false,\"error\":{\"message\" : \"\"\"Token \"4f735d6b-f18f-4eaf-969b-04f494ae29c0\" not found\"\"\",\"id\":null}}"        }    ]}
```
