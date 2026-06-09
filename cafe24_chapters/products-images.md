# PRODUCTS IMAGES


## Products images

```json
Endpoints    POST /api/v2/admin/products/{product_no}/images
DELETE /api/v2/admin/products/{product_no}/images
```

```json
POST /api/v2/admin/products/{product_no}/images
DELETE /api/v2/admin/products/{product_no}/images
```

### Products images property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호. |
| product_no | 상품번호 상품의 고유한 일련 번호. 해당 쇼핑몰 내에서 상품 번호는 중복되지 않음. |
| detail_image | 상세이미지 상품 상세 화면에 표시되는 상품 이미지. |
| list_image | 목록이미지 상품 분류 화면, 메인 화면, 상품 검색 화면에 표시되는 상품의 목록 이미지. |
| tiny_image | 작은목록이미지 상품 상세 화면 하단에 표시되는 상품 목록 이미지. |
| small_image | 축소이미지 최근 본 상품 영역에 표시되는 상품의 목록 이미지. |

### Upload product images   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 쓰기권한 (mall.write_product) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호.   DEFAULT 1 |
| product_noRequired | 상품번호   상품의 고유한 일련 번호. 해당 쇼핑몰 내에서 상품 번호는 중복되지 않음. |
| detail_image | 상세이미지   상품 상세 화면에 표시되는 상품 이미지. |
| list_image | 목록이미지   Youtube shopping 이용 시에는 미제공   상품 분류 화면, 메인 화면, 상품 검색 화면에 표시되는 상품의 목록 이미지. |
| tiny_image | 작은목록이미지   Youtube shopping 이용 시에는 미제공   상품 상세 화면 하단에 표시되는 상품 목록 이미지. |
| small_image | 축소이미지   Youtube shopping 이용 시에는 미제공   최근 본 상품 영역에 표시되는 상품의 목록 이미지. |
| image_upload_typeRequired | 이미지 업로드 타입   Youtube shopping 이용 시에는 미제공   이미지 타입이 대표 이미지 인지, 개별 이미지 인지 업로드 타입을 지정할 수 있음. 대표 이미지(A)로 업로드 하는 경우 상세이미지(detail_image)에 이미지를 업로드하면 다른 나머지 이미지에도 모두 반영됨.   A : 대표이미지등록 B : 개별이미지등록 |

```bash
Upload product images        Upload product images       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Delete product images   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 쓰기권한 (mall.write_product) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호.   DEFAULT 1 |
| product_noRequired | 상품번호   시스템에서 부여한 상품의 번호. 상품 번호는 쇼핑몰 내에서 중복되지 않는다. |

```bash
Delete product images        Delete product images       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

## Products images

```json
Endpoints    POST /api/v2/admin/products/images
```

```json
POST /api/v2/admin/products/images
```

### Products images property list

| Attribute | Description |
| --- | --- |
| path | 상세이미지 |

### Upload images   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 쓰기권한 (mall.write_product) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 20 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| imageRequired | 상세이미지   ● 이미지 파일 용량 제한 : 10MB ● 한 호출당 이미지 전체 용량 제한 : 30MB |

```bash
Upload images        Upload images       Request   cURL Java Python Node.js PHP Go  Copy     curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/products/images' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "requests": [        {            "image": "iVBORw0KGgoAAAANSUhEUgAAAAoAAAAKCAYAAACNMs+9AAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAAAJcEhZcwAADsMAAA7DAcdvqGQAAAAXSURBVChTY1BQdvhPDB5ViBdTW6HDfwA+dpbJG+7kLwAAAABJRU5ErkJggg==\n"        },        {            "image": "/9j/4AAQSkZJRgABAQEAYABgAAD/2wBDAAEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQH/2wBDAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQH/wAARCAACAAIDASIAAhEBAxEB/8QAHwAAAQUBAQEBAQEAAAAAAAAAAAECAwQFBgcICQoL/8QAtRAAAgEDAwIEAwUFBAQAAAF9AQIDAAQRBRIhMUEGE1FhByJxFDKBkaEII0KxwRVS0fAkM2JyggkKFhcYGRolJicoKSo0NTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqDhIWGh4iJipKTlJWWl5iZmqKjpKWmp6ipqrKztLW2t7i5usLDxMXGx8jJytLT1NXW19jZ2uHi4+Tl5ufo6erx8vP09fb3+Pn6/8QAHwEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoL/8QAtREAAgECBAQDBAcFBAQAAQJ3AAECAxEEBSExBhJBUQdhcRMiMoEIFEKRobHBCSMzUvAVYnLRChYkNOEl8RcYGRomJygpKjU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6goOEhYaHiImKkpOUlZaXmJmaoqOkpaanqKmqsrO0tba3uLm6wsPExcbHyMnK0tPU1dbX2Nna4uPk5ebn6Onq8vP09fb3+Pn6/9oADAMBAAIRAxEAPwD+/iiiigD/2Q=="        }    ]}'    Response  Copy     {    "images": [        {            "path": "https://{domain}/web/upload/NNEditor/20180130/12ecf27747401c8502ddd6b2e79e1e64.png"        },        {            "path": "https://{domain}/web/upload/NNEditor/20180130/4672d70e72991f3e54627a8be4aea995.png"        }    ]}
```

```bash
curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/products/images' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "requests": [        {            "image": "iVBORw0KGgoAAAANSUhEUgAAAAoAAAAKCAYAAACNMs+9AAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAAAJcEhZcwAADsMAAA7DAcdvqGQAAAAXSURBVChTY1BQdvhPDB5ViBdTW6HDfwA+dpbJG+7kLwAAAABJRU5ErkJggg==\n"        },        {            "image": "/9j/4AAQSkZJRgABAQEAYABgAAD/2wBDAAEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQH/2wBDAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQH/wAARCAACAAIDASIAAhEBAxEB/8QAHwAAAQUBAQEBAQEAAAAAAAAAAAECAwQFBgcICQoL/8QAtRAAAgEDAwIEAwUFBAQAAAF9AQIDAAQRBRIhMUEGE1FhByJxFDKBkaEII0KxwRVS0fAkM2JyggkKFhcYGRolJicoKSo0NTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqDhIWGh4iJipKTlJWWl5iZmqKjpKWmp6ipqrKztLW2t7i5usLDxMXGx8jJytLT1NXW19jZ2uHi4+Tl5ufo6erx8vP09fb3+Pn6/8QAHwEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoL/8QAtREAAgECBAQDBAcFBAQAAQJ3AAECAxEEBSExBhJBUQdhcRMiMoEIFEKRobHBCSMzUvAVYnLRChYkNOEl8RcYGRomJygpKjU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6goOEhYaHiImKkpOUlZaXmJmaoqOkpaanqKmqsrO0tba3uLm6wsPExcbHyMnK0tPU1dbX2Nna4uPk5ebn6Onq8vP09fb3+Pn6/9oADAMBAAIRAxEAPwD+/iiiigD/2Q=="        }    ]}'
```

```json
{    "images": [        {            "path": "https://{domain}/web/upload/NNEditor/20180130/12ecf27747401c8502ddd6b2e79e1e64.png"        },        {            "path": "https://{domain}/web/upload/NNEditor/20180130/4672d70e72991f3e54627a8be4aea995.png"        }    ]}
```
