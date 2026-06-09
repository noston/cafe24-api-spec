# KAKAOALIMTALK PROFILE


## Kakaoalimtalk profile

```json
Endpoints    GET /api/v2/admin/kakaoalimtalk/profile
```

```json
GET /api/v2/admin/kakaoalimtalk/profile
```

### Kakaoalimtalk profile property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 DEFAULT 1 |
| kakao_senderkey | 카카오 채널 발신 프로필 키 |

### Retrieve a Kakao Channel sender profile key   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 읽기권한 (mall.read_store) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |

```bash
Retrieve a Kakao Channel sender profile key        Retrieve a Kakao Channel sender profile key       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/kakaoalimtalk/profile' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "kakaoprofile": {        "shop_no": 1,        "kakao_senderkey": "e04b7660a7aedcc7916840e1e0add842b1608525"    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/kakaoalimtalk/profile' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "kakaoprofile": {        "shop_no": 1,        "kakao_senderkey": "e04b7660a7aedcc7916840e1e0add842b1608525"    }}
```
