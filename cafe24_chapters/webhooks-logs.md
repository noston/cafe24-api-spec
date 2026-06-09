# WEBHOOKS LOGS


## Webhooks logs

```json
Endpoints    GET /api/v2/admin/webhooks/logs
```

```json
GET /api/v2/admin/webhooks/logs
```

### Webhooks logs property list

| Attribute | Description |
| --- | --- |
| log_id | 로그 ID |
| log_type | 로그 종류 G : 일반 발송 R : 재발송 T : 테스트 발송 |
| event_no | 이벤트 번호 |
| mall_id | 쇼핑몰 ID |
| trace_id | Trace ID |
| requested_time | 전송일시 |
| request_endpoint | 요청 URL |
| request_body | 요청 내용 |
| success | 웹훅 발송 성공 여부 T : 성공 F : 실패 |
| response_http_code | 응답 http code |
| response_body | 응답 내용 |

### Retrieve a list of webhook logs   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 앱 읽기권한 (mall.read_application) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| event_no | 이벤트 번호 |
| requested_start_date날짜 | 발송 시작일시 |
| requested_end_date날짜 | 발송 종료일시 |
| success | 웹훅 발송 성공 여부   T : 성공 F : 실패 |
| log_type | 로그 종류   G : 일반 발송 R : 재발송 T : 테스트 발송 |
| since_log_id | 해당 로그 ID 이후 검색 |
| limit최소: [1]~최대: [10000] | 조회결과 최대건수 |

```bash
Retrieve a list of webhook logs        Retrieve a list of webhook logs       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/webhooks/logs' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "logs": [        {            "log_id": "zV7Ur3oBsq3B53njmYm-",            "log_type": "G",            "event_no": 90001,            "mall_id": "bestshop",            "trace_id": "0d492786-ae82-4073-aa88-0991b08ee732",            "requested_time": "2020-08-03T10:10:10+09:00",            "request_endpoint": "https://app.com/webhooks/regist_product",            "request_body": "{\"event_no\":90001,\"resource\":{\"mall_id\":\"cafe24bestshop\",\"event_shop_no\":\"1\",\"product_code\":\"P000CCAO\"}}",            "success": "T",            "response_http_code": null,            "response_body": null        },        {            "log_id": "dV7Ur3oBsq3B53njJIbP",            "log_type": "G",            "event_no": 90001,            "mall_id": "bestshop",            "trace_id": "518e78fd-e59e-45e4-8fe7-46620ea9b000",            "requested_time": "2020-08-03T10:10:10+09:00",            "request_endpoint": "https://app.com/webhooks/regist_product",            "request_body": "{\"event_no\":90001,\"resource\":{\"mall_id\":\"cafe24bestshop\",\"event_shop_no\":\"1\",\"product_code\":\"P000CCAP\"}}",            "success": "F",            "response_http_code": 403,            "response_body": "<html><head><title>403 Forbidden</title></head><body><center><h1>403 Forbidden</h1></center></body></html>"        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/webhooks/logs' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "logs": [        {            "log_id": "zV7Ur3oBsq3B53njmYm-",            "log_type": "G",            "event_no": 90001,            "mall_id": "bestshop",            "trace_id": "0d492786-ae82-4073-aa88-0991b08ee732",            "requested_time": "2020-08-03T10:10:10+09:00",            "request_endpoint": "https://app.com/webhooks/regist_product",            "request_body": "{\"event_no\":90001,\"resource\":{\"mall_id\":\"cafe24bestshop\",\"event_shop_no\":\"1\",\"product_code\":\"P000CCAO\"}}",            "success": "T",            "response_http_code": null,            "response_body": null        },        {            "log_id": "dV7Ur3oBsq3B53njJIbP",            "log_type": "G",            "event_no": 90001,            "mall_id": "bestshop",            "trace_id": "518e78fd-e59e-45e4-8fe7-46620ea9b000",            "requested_time": "2020-08-03T10:10:10+09:00",            "request_endpoint": "https://app.com/webhooks/regist_product",            "request_body": "{\"event_no\":90001,\"resource\":{\"mall_id\":\"cafe24bestshop\",\"event_shop_no\":\"1\",\"product_code\":\"P000CCAP\"}}",            "success": "F",            "response_http_code": 403,            "response_body": "<html><head><title>403 Forbidden</title></head><body><center><h1>403 Forbidden</h1></center></body></html>"        }    ]}
```
