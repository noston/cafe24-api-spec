# APPS


## Apps

```json
Endpoints    GET /api/v2/admin/apps
PUT /api/v2/admin/apps
```

```json
GET /api/v2/admin/apps
PUT /api/v2/admin/apps
```

### Apps property list

| Attribute | Description |
| --- | --- |
| version | 버전 |
| version_expiration_date | 버전 만료일 |
| initial_version | 최초 버전 |
| previous_version | 이전 버전 |
| extension_type | 확장 타입 section : 섹션(쇼핑몰 프론트에 html 삽입이 필요한 앱 타입) embedded : 임베디드(쇼핑몰 프론트에 임베디드되어 자동으로 구동되는 앱 타입) |

### Retrieve an app information   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 앱 읽기권한 (mall.read_application) |
| 호출건수 제한 | 40 |

```bash
Retrieve an app information        Retrieve an app information       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/apps' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "app": {        "version": "2020-03-01",        "version_expiration_date": null,        "initial_version": "2019-06-26",        "previous_version": "2019-12-11",        "extension_type": "section"    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/apps' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "app": {        "version": "2020-03-01",        "version_expiration_date": null,        "initial_version": "2019-06-26",        "previous_version": "2019-12-11",        "extension_type": "section"    }}
```

### Update an app information   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 앱 쓰기권한 (mall.write_application) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| version | 버전 |
| extension_type | 확장 타입   section : 섹션(쇼핑몰 프론트에 html 삽입이 필요한 앱 타입) embedded : 임베디드(쇼핑몰 프론트에 임베디드되어 자동으로 구동되는 앱 타입) |

```bash
Update an app information        Update an app information       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/apps' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "request": {        "version": "2019-12-11",        "extension_type": "section"    }}'    Response  Copy     {    "app": {        "version": "2019-12-11",        "extension_type": "section"    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/apps' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "request": {        "version": "2019-12-11",        "extension_type": "section"    }}'
```

```json
{    "app": {        "version": "2019-12-11",        "extension_type": "section"    }}
```
