# FINANCIALS MONTHLYREVIEWS


## Financials monthlyreviews

```json
Endpoints    GET /api/v2/admin/financials/monthlyreviews
```

```json
GET /api/v2/admin/financials/monthlyreviews
```

### Financials monthlyreviews property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| month | 년월 |
| count | 리뷰 개수 합계 |
| rating_average | 리뷰 평점 평균 |

### Retrieve the total count for monthly reviews and ratings   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 게시판 읽기권한 (mall.read_community) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| start_monthRequired | 검색 시작월 |
| end_monthRequired | 검색 종료월 |

```bash
Retrieve the total count for monthly reviews and ratings        Retrieve the total count for monthly reviews and ratings       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/financials/monthlyreviews?start_month=2022-04&end_month=2022-05' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "monthlyreviews": [        {            "shop_no": 1,            "month": "2022-04",            "count": 3,            "rating_average": 4        },        {            "shop_no": 1,            "month": "2022-05",            "count": 5,            "rating_average": 3.33        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/financials/monthlyreviews?start_month=2022-04&end_month=2022-05' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "monthlyreviews": [        {            "shop_no": 1,            "month": "2022-04",            "count": 3,            "rating_average": 4        },        {            "shop_no": 1,            "month": "2022-05",            "count": 5,            "rating_average": 3.33        }    ]}
```
