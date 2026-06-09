# MENUS


## Menus

```json
Endpoints    GET /api/v2/admin/menus
```

```json
GET /api/v2/admin/menus
```

### Menus property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| mode | 메뉴 모드 new_pro: PC 어드민 mobile_admin : 모바일 어드민 |
| menu_no | 메뉴 번호 |
| name | 메뉴명 |
| path | 메뉴 경로 |
| contains_app_url | 앱 URL 포함 여부 T : 포함 F : 미포함 |

### Retrieve menus   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 읽기권한 (mall.read_store) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| mode | 메뉴 모드   new_pro: PC 어드민 mobile_admin : 모바일 어드민   DEFAULT new_pro |
| menu_no | 메뉴 번호   ,(콤마)로 여러 건을 검색할 수 있다. |
| contains_app_url | 앱 URL 포함 여부   T : 포함 F : 미포함 |

```bash
Retrieve menus        Retrieve menus Retrieve menus with fields parameter Retrieve a specific menus with menu_no parameter Retrieve multiple menus       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/menus' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "menus": [        {            "shop_no": 1,            "mode": "new_pro",            "menu_no": "2",            "name": "Themes (PC)",            "path": "https://sample.cafe24.com/disp/admin/shop1/Manage/Index",            "contains_app_url": "F"        },        {            "shop_no": 1,            "mode": "new_pro",            "menu_no": "78",            "name": "Returns",            "path": "https://sample.cafe24.com/admin/php/shop1/s_new/order_returns.php",            "contains_app_url": "T"        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/menus' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "menus": [        {            "shop_no": 1,            "mode": "new_pro",            "menu_no": "2",            "name": "Themes (PC)",            "path": "https://sample.cafe24.com/disp/admin/shop1/Manage/Index",            "contains_app_url": "F"        },        {            "shop_no": 1,            "mode": "new_pro",            "menu_no": "78",            "name": "Returns",            "path": "https://sample.cafe24.com/admin/php/shop1/s_new/order_returns.php",            "contains_app_url": "T"        }    ]}
```
