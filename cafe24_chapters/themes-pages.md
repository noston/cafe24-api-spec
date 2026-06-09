# THEMES PAGES


## Themes pages

```json
Endpoints    GET /api/v2/admin/themes/{skin_no}/pages
POST /api/v2/admin/themes/{skin_no}/pages
PUT /api/v2/admin/themes/{skin_no}/pages
DELETE /api/v2/admin/themes/{skin_no}/pages
```

```json
GET /api/v2/admin/themes/{skin_no}/pages
POST /api/v2/admin/themes/{skin_no}/pages
PUT /api/v2/admin/themes/{skin_no}/pages
DELETE /api/v2/admin/themes/{skin_no}/pages
```

### Themes pages property list

| Attribute | Description |
| --- | --- |
| skin_no | 디자인 번호 |
| skin_code | 디자인 코드 |
| path | 파일 경로 |
| source | 소스 코드 |
| display_location | 화면 분류 |

### Retrieve a theme page   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 디자인 읽기권한 (mall.read_design) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| skin_noRequired | 디자인 번호 |
| pathRequired | 파일 경로 |

```bash
Retrieve a theme page        Retrieve a theme page Retrieve pages with fields parameter       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Create a theme page   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 디자인 쓰기권한 (mall.write_design) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| skin_noRequired | 디자인 번호 |
| pathRequired | 파일/디렉토리 경로 |
| source | 소스 코드 |
| display_location | 화면 분류 |

```bash
Create a theme page        Create a theme page Set a certain design skin to a certain path by using only required fields Try setting a certain design skin to a certain path without using path field       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Update a theme page   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 디자인 쓰기권한 (mall.write_design) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| skin_noRequired | 디자인 번호 |
| pathRequired | 파일 경로 |
| sourceRequired | 소스 코드 |

```bash
Update a theme page        Update a theme page       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Delete a theme page   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 디자인 쓰기권한 (mall.write_design) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| skin_noRequired | 디자인 번호 |
| pathRequired | 파일 경로 |

```bash
Delete a theme page        Delete a theme page       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
