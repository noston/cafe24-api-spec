# BOARDS SEO


## Boards seo

```json
Endpoints    GET /api/v2/admin/boards/{board_no}/seo
PUT /api/v2/admin/boards/{board_no}/seo
```

```json
GET /api/v2/admin/boards/{board_no}/seo
PUT /api/v2/admin/boards/{board_no}/seo
```

### Boards seo property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| board_no | 게시판 번호 |
| meta_title | 브라우저 타이틀 [MALL_NAME] : 쇼핑몰명 [BOARD_NAME] : 게시판 제목 [BOARD_GUIDE] : 게시판 안내글 [ARTICLE_TITLE] : 게시물 제목 |
| meta_author | 메타태그1 : Author [MALL_NAME] : 쇼핑몰명 [BOARD_NAME] : 게시판 제목 [BOARD_GUIDE] : 게시판 안내글 [ARTICLE_TITLE] : 게시물 제목 |
| meta_description | 메타태그2 : Description [MALL_NAME] : 쇼핑몰명 [BOARD_NAME] : 게시판 제목 [BOARD_GUIDE] : 게시판 안내글 [ARTICLE_TITLE] : 게시물 제목 |
| meta_keywords | 메타태그3 : Keywords [MALL_NAME] : 쇼핑몰명 [BOARD_NAME] : 게시판 제목 [BOARD_GUIDE] : 게시판 안내글 [ARTICLE_TITLE] : 게시물 제목 |

### Retrieve SEO settings for board   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 게시판 읽기권한 (mall.read_community) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| board_noRequired | 게시판 번호 |

```bash
Retrieve SEO settings for board        Retrieve SEO settings for board       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Update SEO settings for board   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 게시판 쓰기권한 (mall.write_community) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| board_noRequired | 게시판 번호 |
| meta_title최대글자수 : [100자] | 브라우저 타이틀   [MALL_NAME] : 쇼핑몰명 [BOARD_NAME] : 게시판 제목 [BOARD_GUIDE] : 게시판 안내글 [ARTICLE_TITLE] : 게시물 제목 |
| meta_author | 메타태그1 : Author   [MALL_NAME] : 쇼핑몰명 [BOARD_NAME] : 게시판 제목 [BOARD_GUIDE] : 게시판 안내글 [ARTICLE_TITLE] : 게시물 제목 |
| meta_description | 메타태그2 : Description   [MALL_NAME] : 쇼핑몰명 [BOARD_NAME] : 게시판 제목 [BOARD_GUIDE] : 게시판 안내글 [ARTICLE_TITLE] : 게시물 제목 |
| meta_keywords | 메타태그3 : Keywords   [MALL_NAME] : 쇼핑몰명 [BOARD_NAME] : 게시판 제목 [BOARD_GUIDE] : 게시판 안내글 [ARTICLE_TITLE] : 게시물 제목 |

```bash
Update SEO settings for board        Update SEO settings for board       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
