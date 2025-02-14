# My Project

Base URLs:

# Authentication

- HTTP Authentication, scheme: bearer

# APP

## POST API_1 接收群組資料同步

POST /api/App/API_1

> Body Parameters

```json
[
  {
    "groupGUID": "E8985C66-6969-439E-A3B1-9DD5D68355E0",
    "isDeleted": true,
    "groupName": "南波萬",
    "permissionType": 1,
    "startDate": 1723184852752,
    "endDate": 1723194852752,
    "startTime": "18:30:00",
    "endTime": "18:30:00",
    "monday": true,
    "tuesDay": true,
    "wednesday": true,
    "thursday": true,
    "friday": true,
    "saturday": false,
    "sunday": false,
    "groupPassword": "00001111"
  },
  {
    "groupGUID": "2252F95E-6D60-45A7-9CCD-441F433B8F2E",
    "isDeleted": false,
    "groupName": "南波兔",
    "permissionType": 0,
    "startDate": 1723184852752,
    "endDate": 1723194852752,
    "startTime": "08:30:00",
    "endTime": "17:30:00",
    "monday": true,
    "tuesDay": true,
    "wednesday": true,
    "thursday": true,
    "friday": true,
    "saturday": false,
    "sunday": false,
    "groupPassword": "123456",
    "customName": "測試新增第2筆"
  },
  {
    "groupGUID": "4748848a-ea3a-4e33-86f9-da53ff316d6a",
    "isDeleted": false,
    "groupName": "TomTom",
    "permissionType": 0,
    "startDate": 0,
    "endDate": 0,
    "startTime": "00:00:00",
    "endTime": "00:00:00",
    "monday": false,
    "tuesDay": false,
    "wednesday": false,
    "thursday": false,
    "friday": false,
    "saturday": false,
    "sunday": false,
    "groupPassword": "9453"
  }
]
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|array[object]| no |none|

> Response Examples

```json
{
  "id": "(string)通常為識別碼",
  "success": "(boolean)是否執行成功",
  "errorMessage": "(string)若執行失敗的原因說明",
  "anyMsg": "(string)若執行成功的內容補充",
  "anyObject": "(object)需要回傳的物件"
}
```

```json
{
  "id": "",
  "success": false,
  "errorMessage": "匯入 3筆，失敗 1筆。",
  "anyMsg": "",
  "anyObject": [
    "GroupGUID: 4748848a-ea3a-4e33-86f9-da53ff316d6a, ErrorMessage: 資料不存在，無法執行刪除。"
  ]
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» id|string|true|none||none|
|» success|string|true|none||none|
|» errorMessage|string|true|none||none|
|» anyMsg|string|true|none||none|
|» anyObject|string|true|none||none|

HTTP Status Code **400**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» id|string|true|none||none|
|» success|boolean|true|none||none|
|» errorMessage|string|true|none||none|
|» anyMsg|string|true|none||none|
|» anyObject|[string]|true|none||none|

## GET API_1 查詢群組資料

GET /api/App/API_1/1

> Response Examples

```json
{
  "result": [
    {
      "groupGUID": "2252F95E-6D60-45A7-9CCD-441F433B8F2E",
      "isDeleted": false,
      "groupName": "測試新增第2筆",
      "permissionType": 0,
      "startDate": 1723184852752,
      "endDate": 1723194852752,
      "startTime": "08:30:00",
      "endTime": "17:30:00",
      "monday": true,
      "tuesDay": true,
      "wednesday": true,
      "thursday": true,
      "friday": true,
      "saturday": false,
      "sunday": false,
      "status": 1,
      "groupPassword": "123456"
    }
  ],
  "pages": 1,
  "total": 1,
  "input": 1
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» result|[object]|true|none||none|
|»» groupGUID|string|false|none||none|
|»» isDeleted|boolean|false|none||none|
|»» groupName|string|false|none||none|
|»» permissionType|integer|false|none||none|
|»» startDate|integer|false|none||none|
|»» endDate|integer|false|none||none|
|»» startTime|string|false|none||none|
|»» endTime|string|false|none||none|
|»» monday|boolean|false|none||none|
|»» tuesDay|boolean|false|none||none|
|»» wednesday|boolean|false|none||none|
|»» thursday|boolean|false|none||none|
|»» friday|boolean|false|none||none|
|»» saturday|boolean|false|none||none|
|»» sunday|boolean|false|none||none|
|»» status|integer|false|none||none|
|»» groupPassword|string|false|none||none|
|» pages|integer|true|none||none|
|» total|integer|true|none||none|
|» input|integer|true|none||none|

## GET API_1 查詢群組資料(近期)

GET /api/App/API_1/1732787850/1

> Response Examples

```json
{
  "result": [
    {
      "groupGUID": "2252F95E-6D60-45A7-9CCD-441F433B8F2E",
      "isDeleted": false,
      "groupName": "測試新增第2筆",
      "permissionType": 0,
      "startDate": 1723184852752,
      "endDate": 1723194852752,
      "startTime": "08:30:00",
      "endTime": "17:30:00",
      "monday": true,
      "tuesDay": true,
      "wednesday": true,
      "thursday": true,
      "friday": true,
      "saturday": false,
      "sunday": false,
      "status": 1,
      "groupPassword": "123456"
    },
    {
      "groupGUID": "E8985C66-6969-439E-A3B1-9DD5D68355E0",
      "isDeleted": false,
      "groupName": "測試新增第1筆",
      "permissionType": 1,
      "startDate": 1723184852752,
      "endDate": 1723194852752,
      "startTime": "18:30:00",
      "endTime": "18:30:00",
      "monday": true,
      "tuesDay": true,
      "wednesday": true,
      "thursday": true,
      "friday": true,
      "saturday": false,
      "sunday": false,
      "status": 1,
      "groupPassword": "122222222"
    }
  ],
  "pages": 1,
  "total": 2,
  "input": {
    "id": "1",
    "time": 1724123237088
  }
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» result|[object]|true|none||none|
|»» groupGUID|string|true|none||none|
|»» isDeleted|boolean|true|none||none|
|»» groupName|string|true|none||none|
|»» permissionType|integer|true|none||none|
|»» startDate|integer|true|none||none|
|»» endDate|integer|true|none||none|
|»» startTime|string|true|none||none|
|»» endTime|string|true|none||none|
|»» monday|boolean|true|none||none|
|»» tuesDay|boolean|true|none||none|
|»» wednesday|boolean|true|none||none|
|»» thursday|boolean|true|none||none|
|»» friday|boolean|true|none||none|
|»» saturday|boolean|true|none||none|
|»» sunday|boolean|true|none||none|
|»» status|integer|true|none||none|
|»» groupPassword|string|true|none||none|
|» pages|integer|true|none||none|
|» total|integer|true|none||none|
|» input|object|true|none||none|
|»» id|string|true|none||none|
|»» time|integer|true|none||none|

## POST API_2 接收人員資料同步

POST /api/App/API_2

> Body Parameters

```json
[
  {
    "memberGUID": "ba731543-57de-4594-a107-1111de702066",
    "isDeleted": false,
    "memberID": "123456",
    "memberName": "宏康TXT",
    "cardID": null,
    "refA": "從txt拿到的資料",
    "refB": null,
    "refC": null,
    "refD": null,
    "refE": null,
    "enable": 1,
    "groupList": []
  }
]
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|array[object]| no |none|

> Response Examples

```json
{
  "id": "(string)通常為識別碼",
  "success": "(boolean)是否執行成功",
  "errorMessage": "(string)若執行失敗的原因說明",
  "anyMsg": "(string)若執行成功的內容補充",
  "anyObject": "(object)需要回傳的物件"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» id|string|true|none||none|
|» success|string|true|none||none|
|» errorMessage|string|true|none||none|
|» anyMsg|string|true|none||none|
|» anyObject|string|true|none||none|

## GET API_2 查詢人員資料

GET /api/App/API_2/1

> Response Examples

```json
{
  "result": [
    {
      "memberGUID": "212D673A-D215-451D-953C-195E7EF3E4B2",
      "isDeleted": false,
      "memberID": "9001",
      "memberName": "A_Test001",
      "cardID": "001001",
      "refA": null,
      "refB": null,
      "refC": null,
      "refD": null,
      "refE": null,
      "enable": 1,
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044",
        "E8985C66-6969-439E-A3B1-9DD5D68355E0"
      ]
    }
  ],
  "pages": 1,
  "total": 1,
  "input": 1
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» result|[object]|true|none||none|
|»» memberGUID|string|false|none||none|
|»» isDeleted|boolean|false|none||none|
|»» memberID|string|false|none||none|
|»» memberName|string|false|none||none|
|»» cardID|string|false|none||none|
|»» refA|null|false|none||none|
|»» refB|null|false|none||none|
|»» refC|null|false|none||none|
|»» refD|null|false|none||none|
|»» refE|null|false|none||none|
|»» enable|integer|false|none||none|
|»» groupList|[string]|false|none||none|
|» pages|integer|true|none||none|
|» total|integer|true|none||none|
|» input|integer|true|none||none|

## GET API_2 查詢人員資料(近期)

GET /api/App/API_1/1732781529/1

> Response Examples

```json
{
  "result": [
    {
      "memberGUID": "212D673A-D215-451D-953C-195E7EF3E4B2",
      "isDeleted": false,
      "memberID": "9001",
      "memberName": "A_Test001",
      "cardID": "001001",
      "refA": null,
      "refB": null,
      "refC": null,
      "refD": null,
      "refE": null,
      "enable": 1,
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044",
        "E8985C66-6969-439E-A3B1-9DD5D68355E0"
      ]
    }
  ],
  "pages": 1,
  "total": 1,
  "input": {
    "id": "1",
    "time": 1724059627471
  }
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» result|[object]|true|none||none|
|»» memberGUID|string|false|none||none|
|»» isDeleted|boolean|false|none||none|
|»» memberID|string|false|none||none|
|»» memberName|string|false|none||none|
|»» cardID|string|false|none||none|
|»» refA|null|false|none||none|
|»» refB|null|false|none||none|
|»» refC|null|false|none||none|
|»» refD|null|false|none||none|
|»» refE|null|false|none||none|
|»» enable|integer|false|none||none|
|»» groupList|[string]|false|none||none|
|» pages|integer|true|none||none|
|» total|integer|true|none||none|
|» input|object|true|none||none|
|»» id|string|true|none||none|
|»» time|integer|true|none||none|

## POST API_4 確認連線狀態

POST /api/App/API_4/139b02b8-4098-4726-b02b-92af49977cf5

> Response Examples

```json
{
  "id": "(string)通常為識別碼",
  "success": "(boolean)是否執行成功",
  "errorMessage": "(string)若執行失敗的原因說明",
  "anyMsg": "(string)若執行成功的內容補充",
  "anyObject": "(object)需要回傳的物件"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» id|string|true|none||none|
|» success|string|true|none||none|
|» errorMessage|string|true|none||none|
|» anyMsg|string|true|none||none|
|» anyObject|string|true|none||none|

## POST API_5 新增授權紀錄

POST /api/App/API_5

> Body Parameters

```json
{
  "identifyingMode": "string",
  "success": true,
  "deviceGUID": "string",
  "memberGUID": "string",
  "score": 0,
  "recTime": 0,
  "image": "string"
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» identifyingMode|body|string| yes |none|
|» success|body|boolean| yes |none|
|» deviceGUID|body|string| yes |none|
|» memberGUID|body|string| yes |none|
|» score|body|integer| yes |none|
|» recTime|body|integer| yes |none|
|» image|body|string| yes |none|

> Response Examples

```json
{
  "id": "(string)通常為識別碼",
  "success": "(boolean)是否執行成功",
  "errorMessage": "(string)若執行失敗的原因說明",
  "anyMsg": "(string)若執行成功的內容補充",
  "anyObject": "(object)需要回傳的物件"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» id|string|true|none||none|
|» success|string|true|none||none|
|» errorMessage|string|true|none||none|
|» anyMsg|string|true|none||none|
|» anyObject|string|true|none||none|

## POST API_11 通知同步已完成

POST /api/App/API_11/3C-E3-6B-95-90-DD

> Response Examples

```json
{
  "id": "(str)通常為識別碼",
  "success": "(bool)是否執行成功",
  "errorMessage": "(str)若執行失敗的原因說明",
  "anyMsg": "(str)若執行成功的內容補充",
  "anyObject": "(obj)需要回傳的物件"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» id|string|true|none||none|
|» success|string|true|none||none|
|» errorMessage|string|true|none||none|
|» anyMsg|string|true|none||none|
|» anyObject|string|true|none||none|

## GET API_12 查詢平板設定

GET /api/App/API_12

> Response Examples

```json
{
  "result": {
    "hideMemberID": "(str)不顯示工號設定值",
    "hideName": "(str)不顯示名稱設定值",
    "identifyingLogic": "(str)驗證方式多模式判定邏輯設定值",
    "identifyingMode": "(str)驗證方式設定值",
    "powerSavingMode": "(str)自動關閉時間設定值",
    "voiceSwitch": "(str)語音設定設定值"
  }
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» result|object|true|none||none|
|»» hideMemberID|string|true|none||none|
|»» hideName|string|true|none||none|
|»» identifyingLogic|string|true|none||none|
|»» identifyingMode|string|true|none||none|
|»» powerSavingMode|string|true|none||none|
|»» voiceSwitch|string|true|none||none|

## GET API_13 詢問系統時間

GET /api/App/API_13/1

> Response Examples

```json
{
  "id": "(str)通常為識別碼",
  "success": "(bool)是否執行成功",
  "errorMessage": "(str)若執行失敗的原因說明",
  "anyMsg": "(str)若執行成功的內容補充",
  "anyObject": "(obj)需要回傳的物件"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» id|string|true|none||none|
|» success|string|true|none||none|
|» errorMessage|string|true|none||none|
|» anyMsg|string|true|none||none|
|» anyObject|string|true|none||none|

## POST API_17 接收訪客資料同步

POST /api/App/API_17

> Body Parameters

```json
[
  {
    "memberGUID": "92701099-7F6B-44E9-AEE9-804240C545BC",
    "isDeleted": false,
    "memberName": "訪客A卡",
    "cardID": "VC0001",
    "groupList": [
      "a991bef8-f7ce-4ab5-b5a1-653e67d7a044",
      "E8985C66-6969-439E-A3B1-9DD5D68355E0"
    ],
    "enable": 0
  },
  {
    "memberGUID": "92701099-7F6B-44E9-AEE9-804240C545BB",
    "isDeleted": false,
    "memberName": "訪客B卡",
    "cardID": "VC0002",
    "groupList": [
      "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
    ],
    "enable": 1
  }
]
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|array[object]| no |none|

> Response Examples

```json
{
  "id": "(string)通常為識別碼",
  "success": "(boolean)是否執行成功",
  "errorMessage": "(string)若執行失敗的原因說明",
  "anyMsg": "(string)若執行成功的內容補充",
  "anyObject": "(object)需要回傳的物件"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» id|string|true|none||none|
|» success|string|true|none||none|
|» errorMessage|string|true|none||none|
|» anyMsg|string|true|none||none|
|» anyObject|string|true|none||none|

## GET API_17 查詢訪客資料

GET /api/App/API_17/1

> Response Examples

```json
{
  "result": [
    {
      "memberGUID": "ded5b948-6912-400a-b8b8-1eb5ebb7a3bf",
      "isDeleted": false,
      "memberName": "波賽隆納",
      "cardID": "00002",
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044",
        "E8985C66-6969-439E-A3B1-9DD5D68355E0"
      ]
    },
    {
      "memberGUID": "92701099-7F6B-44E9-AEE9-804240C545B9",
      "isDeleted": false,
      "memberName": "A_Guest002",
      "cardID": "002003",
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ]
    }
  ],
  "pages": 1,
  "total": 2,
  "input": 1
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» result|[object]|true|none||none|
|»» memberGUID|string|true|none||none|
|»» isDeleted|boolean|true|none||none|
|»» memberName|string|true|none||none|
|»» cardID|string|true|none||none|
|»» groupList|[string]|true|none||none|
|» pages|integer|true|none||none|
|» total|integer|true|none||none|
|» input|integer|true|none||none|

## GET API_17 查詢訪客資料(近期)

GET /api/App/API_17/1724051726352/1

> Response Examples

```json
{
  "result": [
    {
      "memberGUID": "92701099-7F6B-44E9-AEE9-804240C545B8",
      "isDeleted": false,
      "memberName": "A_Guest001",
      "cardID": "002002",
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044",
        "E8985C66-6969-439E-A3B1-9DD5D68355E0"
      ]
    }
  ],
  "pages": 1,
  "total": 1,
  "input": {
    "id": "1",
    "time": 1724051726352
  }
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» result|[object]|true|none||none|
|»» memberGUID|string|false|none||none|
|»» isDeleted|boolean|false|none||none|
|»» memberName|string|false|none||none|
|»» cardID|string|false|none||none|
|»» groupList|[string]|false|none||none|
|» pages|integer|true|none||none|
|» total|integer|true|none||none|
|» input|object|true|none||none|
|»» id|string|true|none||none|
|»» time|integer|true|none||none|

## POST API_20 接收特徵值資料同步

POST /api/App/API_20

> Body Parameters

```json
[
  {
    "memberGUID": "ba731543-57de-4594-a107-1111de702066",
    "vectorData": "[-0.0012837137, 0.06816744, -0.06598474, -0.027947478, 0.026577882, -0.07754078, 0.03390746, 0.01807471, 0.048739824, -0.022473335, 0.034474567, -0.035314973, 0.044366956, -0.016920779, 0.057297606, -0.015492372, -0.043766133, 7.9704734E-4, -0.041529648, -0.11313759, -0.0046951766, -0.015357371, 0.07290429, -0.032406613, -0.026581947, -0.06948335, -0.03498411, 0.017000673, 0.014518958, 0.10735486, -0.06609248, -0.046951555, 0.049119998, -0.05052203, -0.035652425, -0.0054386454, -0.0051116976, -0.0074302773, 0.04690254, -0.076947734, 0.036532946, -0.01600288, 5.003766E-4, -0.05599622, -0.033845827, -0.11767441, -0.017302468, 0.03355063, 0.03068105, 0.04135602, 0.020222526, -0.0849751, 0.06351026, 0.04327523, -0.0826298, -0.021909475, -0.07549542, -0.003967494, 0.059476748, -0.053459186, -0.052011468, -0.0015123389, -0.06401556, 0.1064544, 0.0730663, 0.008440156, -0.031680547, 0.021256806, 0.01770871, 0.02294031, 0.0640834, 0.045913976, -0.0066873697, 0.01719872, 0.050427143, -0.038381014, -0.051261142, 0.09928541, -0.014081431, -0.020124651, -0.045333017, 0.015833002, 0.033822823, 0.0035436086, 0.023436526, 0.005210057, 0.010641321, 0.023113055, -0.041313972, 0.0017234636, 0.04840396, -0.06306731, -0.016618213, 0.048228614, -0.05860294, 0.020397596, -0.0040105646, -0.048325837, 0.023149276, 0.021497305, 0.02542234, 0.001423101, -0.03847826, 0.033051603, -0.050883748, 0.010057847, -0.048067603, 0.029882139, 0.002390609, 0.02364897, 0.04536185, 0.008070301, 0.09782937, 0.01607665, -0.021134922, -0.024267867, 0.02077869, 0.10988332, -0.04022436, -0.05710005, -0.06526216, 0.040354848, -0.026996395, -0.041004825, 0.01667872, -0.009918466, 0.018909365, 0.02757943, -0.012014068, -0.011986559, -0.008903988, -0.039641663, -0.020289438, 0.006232837, 0.044184666, -0.042693596, 0.04827714, -0.117331125, -0.023126604, 0.045310177, -0.024908088, -0.09433279, -0.030399399, -0.021645991, 0.020175593, 0.045646165, -0.012025253, 0.051957015, 0.0022971653, 0.06350601, -0.06780656, 0.10594183, 0.055441998, 0.0384737, -0.0020157257, -0.030890688, 0.00317416, -0.036041576, -0.017837282, 0.0063049705, 0.041767348, -0.03474145, 0.013384973, -0.0031241858, -0.02042929, -0.031526137, 0.029221976, 0.08768757, -0.015609735, 0.041251503, 0.0093477825, -0.0436332, -0.06744512, 0.063199796, -0.04707808, -0.027626883, 0.038746748, 0.03505377, 0.05234082, -0.02899629, 0.057742, 0.024527146, 0.10174837, -0.015775856, -0.005935146, -0.028586844, 0.009931833, -0.00232714, -0.03044229, -0.08410741, 0.048337277, 0.059974644, -0.14358619, 0.020155285, 0.033727255, 0.06913234, -0.101239555, 0.029054424, 0.012676313, -0.023562372, -0.0119081875, 0.005333544, 0.0152621, -0.0250363, -0.0021461244, 0.04677041, 0.04586149, -0.0919101, 0.035870515, 0.01884833, 0.0040163705, -0.02532243, 0.05043542, -0.042549875, -0.10566708, -0.032682132, 0.011077641, 0.073414035, 0.023841178, -0.0018067064, 0.04776727, -0.048235398, 0.012997843, 0.10947739, 0.025356732, -0.013873828, -0.043778338, 0.022253266, 0.040535327, -0.0033540623, -0.041557368, 0.06756234, -0.01545481, -0.013308063, -0.059866674, -0.024479402, 0.008066069, 0.044292405, -0.06643295, 0.032951735, 0.049655672, 0.024010252, 0.08974381, 0.002720277, 0.023839453, 0.007047114, -0.018798154, -0.08488727, -0.015990673, 0.020704929, -0.079844385, 0.017074034, 0.04684432, -0.03561248, -0.024244193, 0.025698135, -0.049549766, -0.013006418, -0.040067915, -0.054823827, -0.010224276, -0.0016450168, 0.004490581, -0.097023405, 0.044953678, -0.028250108, -0.061577823, -0.023522934, -0.011159104, 0.031054206, 0.03277657, 0.035841323, 0.040522132, -0.06301379, -0.0736916, 0.043478888, -0.022190364, 0.023235176, -0.009134338, 0.017020218, 0.058517415, 0.023142787, 0.021390682, 0.03759567, 0.028910397, 0.082111664, -0.037798617, -0.024919108, 0.0037654075, 0.043933604, -0.003534388, 0.03656415, 0.068762705, -0.019190235, 0.050265215, 0.018048916, 0.02444453, -0.08917784, -0.036282495, 0.0018109926, 0.007885284, 0.02313612, -0.015456805, 0.015663195, -0.15130988, 0.050836824, -0.024023151, 0.017536879, -0.035309214, -0.0032191416, -0.039198056, -0.023569712, 0.03814345, 0.10556181, 0.065086134, -0.054430176, 0.05633583, 0.04535345, -0.04343695, -0.013429303, -0.127278, 5.375648E-4, -0.028292106, -0.020540614, -0.048545554, 0.042233627, -0.031885747, 0.032239985, 0.020707361, 0.039576698, -0.029204605, 0.0575067, 0.08251868, -0.06839964, -0.031221068, 0.02708497, 0.024758158, 0.002981574, -0.063427374, 0.010360903, -0.041303176, 0.05330237, -0.042723585, -0.053488318, 0.041982766, 0.025908621, 0.011471547, -0.02734938, -0.0665334, -0.017945366, -0.040036894, -0.009998044, -0.003197183, -0.021719255, 0.04357749, 0.014786995, 0.019758452, 0.0034856687, -0.03291582, -0.03833848, -0.026782228, -0.028225131, -0.04330963, -0.027336525, 0.04218641, -0.009227811, -0.06592777, -0.07138546, -0.038324744, 0.05070099, -0.02775659, -0.019352995, 0.022891898, -0.018375179, 0.013019571, -0.0010053235, -0.011572035, 0.09557176, -0.03617038, -0.052345574, 0.028169377, 0.040512554, -0.059516482, 0.039062634, 0.028836645, -0.039125238, 0.011404687, -0.015379305, -0.03905453, -0.050578482, 0.002339892, 0.012082908, 0.043760136, 0.028082501, -0.030886976, 0.0455876, 8.514223E-4, -0.0038330038, 0.07858645, -0.08566611, 0.0130600305, -0.0034677007, -0.002943223, 0.006646864, -0.029760266, 0.07489718, -0.032083347, 0.021633351, 0.016203191, 1.8841357E-4, -0.057043046, 0.015996682, -0.023133911, -0.0183704, -0.053990167, -0.011789514, 0.023314834, 0.01616479, -0.036764216, -0.057554126, -0.058337484, 0.031150136, -0.011957739, 0.0077833543, 0.041125804, -0.0052219424, -0.009061662, -0.03261788, -0.0013532866, -0.036385782, -0.06329012, 0.01121227, -0.064743645, 0.01322068, -0.0018518418, 0.054746166, 0.067731254, -0.033494975, -0.04887886, -0.039406385, -0.050062533, 0.0423645, -0.07642694, -0.0046947165, 0.011626654, -0.02033805, 0.0065371073, 0.026095463, -0.004302159, -0.027915524, 0.032677233, -0.013280409, 0.008404291, -0.041966446, -0.039371915, 0.015667569, 0.0044199293, -0.010667098, -0.013265046, 0.036886968, -0.0028294483, 0.05268207, 0.006306185, -0.08048791, 0.018941864, -0.0071956785, -0.13049772, 0.012089155, -0.06235688, 0.052121263, 0.018418504, 0.025806779, -0.05056038, -0.04321279, 0.11191874, -0.020147432, -0.022570383, -0.01967763, -0.012932444, 0.049748883, 0.033633027, -0.00980675, 0.06342438, -0.021024793, 0.05112105, -0.03265332, 1.7258617E-4, -0.040593475, -0.012921521, 0.03827327, -0.023214541, 0.055699732, 0.008376023, -0.052981887, 0.0049525728, -0.036979407, 0.030247137, 0.023784088, 0.046387065, 0.009465973, -0.03496188, -0.004993758, -0.04315276, 0.013299946, 0.017150434, 0.010121237, -0.09246814, 0.02580189, -0.040734407, -8.760155E-4, 0.046182934, 0.066685386]"
  }
]
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|array[object]| no |none|

> Response Examples

```json
{
  "id": "(str)通常為識別碼",
  "success": "(bool)是否執行成功",
  "errorMessage": "(str)若執行失敗的原因說明",
  "anyMsg": "(str)若執行成功的內容補充",
  "anyObject": "(obj)需要回傳的物件"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» id|string|true|none||none|
|» success|string|true|none||none|
|» errorMessage|string|true|none||none|
|» anyMsg|string|true|none||none|
|» anyObject|string|true|none||none|

## GET API_20 查詢特徵值資料

GET /api/App/API_20/c208c77f-2b04-4915-b4d6-5c36c70c273e

> Response Examples

```json
{
  "result": [
    {
      "memberGUID": "212D673A-D215-451D-953C-195E7EF3E4B2",
      "vectorData": "將註冊圖丟給AI的API去取得"
    },
    {
      "memberGUID": "212D673A-D215-451D-953C-195E7EF3E4B3",
      "vectorData": "特徵值陣列B"
    }
  ],
  "pages": 1,
  "total": 2,
  "input": 1
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» result|[object]|true|none||none|
|»» memberGUID|string|true|none||none|
|»» vectorData|string|true|none||none|
|» pages|integer|true|none||none|
|» total|integer|true|none||none|
|» input|integer|true|none||none|

## GET API_20 查詢特徵值資料(近期)

GET /api/App/API_20/1726739385/165

> Response Examples

```json
{
  "result": [
    {
      "memberGUID": "212D673A-D215-451D-953C-195E7EF3E4B2",
      "vectorData": "將註冊圖丟給AI的API去取得"
    }
  ],
  "pages": 1,
  "total": 1,
  "input": {
    "id": "1",
    "time": 1724059627471
  }
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» result|[object]|true|none||none|
|»» memberGUID|string|false|none||none|
|»» vectorData|string|false|none||none|
|» pages|integer|true|none||none|
|» total|integer|true|none||none|
|» input|object|true|none||none|
|»» id|string|true|none||none|
|»» time|integer|true|none||none|

## GET API_21 查詢使用者資料(近期&帳號)

GET /api/App/API_21/admin

> Response Examples

```json
{
  "result": [
    {
      "isDeleted": "(boolean)是否刪除該筆資料",
      "privilege": "(number)0最高權限|1一般權限",
      "account": "(string)帳號",
      "password": "(string)密碼，MD5加密"
    }
  ]
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» result|[object]|true|none||none|
|»» isDeleted|string|false|none||none|
|»» privilege|string|false|none||none|
|»» account|string|false|none||none|
|»» password|string|false|none||none|

## POST API_22 接收人員資料同步

POST /api/App/API_22

> Body Parameters

```json
"[\r\n    {\r\n        \"isDeleted\": false,\r\n        \"memberID\": \"API22_0001\",\r\n        \"memberName\": \"你決定\",\r\n        \"enrollImage\" : \"/9j/4AAQSkZJRgABAQAASABIAAD/...//Z\" /* 手動省略超長一串 */\r\n    }\r\n]"
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|array[object]| no |none|

> Response Examples

```json
{
  "id": "(string)通常為識別碼",
  "success": "(boolean)是否執行成功",
  "errorMessage": "(string)若執行失敗的原因說明",
  "anyMsg": "(string)若執行成功的內容補充",
  "anyObject": "(object)需要回傳的物件"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» id|string|true|none||none|
|» success|string|true|none||none|
|» errorMessage|string|true|none||none|
|» anyMsg|string|true|none||none|
|» anyObject|string|true|none||none|

# APP 接口

## GET Trigger 後台異動通知

GET /api/App/Trigger/API_12/X

> Response Examples

```json
{
  "description": "請施打 /api/App/apiName/guid 向後台取得資料更新。",
  "url": "/api/App/API_1/2252F95E-6D60-45A7-9CCD-441F433B8F2E"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» description|string|true|none||none|
|» url|string|true|none||none|

## GET Disconnect 後台刪除設備通知

GET /api/App/Disconnect/139b02b8-4098-4726-b02b-92af49977cf5

> Response Examples

```json
{
  "description": "後台已與設備 139b02b8-4098-4726-b02b-92af49977cf5 斷開連線，請將平板功能解鎖。"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» description|string|true|none||none|

## GET Status 攝影機搜尋回應

GET /api/App/Status

> Response Examples

```json
{
  "description": "設備已準備連線。",
  "guid": "BB68843E-9A83-46E8-9884-F7F53B1E2E90"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» description|string|true|none||none|
|» guid|string|true|none||none|

## GET StartSync 開始同步通知

GET /api/App/StartSync/139b02b8-4098-4726-b02b-92af49977cf5/1

> Response Examples

```json
{
  "description": "設備將開始與後台的同步作業，同步期間請勿操作系統。",
  "remark": "模式選擇：0回拋資料給FRS，再從FRS索取資料；1清空平板資料，再從FRS索取資料。"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» description|string|true|none||none|
|» remark|string|true|none||none|

# Record

## POST QueryHitList 檢視成功列表(頁碼+縮圖)

POST /api/record/QueryHitList

> Body Parameters

```json
"{\r\n    \"filterValue\": \"波賽隆納\",\r\n    // \"Sort\": [\r\n    //     {\r\n    //         \"Field\": \"id\",\r\n    //         \"Reverse\": true\r\n    //     }\r\n    // ],\r\n    \"PageNumber\": 1,\r\n    \"PageSize\": 25,\r\n    \"startTime\": 0,\r\n    \"endTime\": 1726124574384\r\n}"
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» filterValue|body|string| yes |none|
|» PageNumber|body|integer| yes |none|
|» PageSize|body|integer| yes |none|
|» startTime|body|integer| yes |none|
|» endTime|body|integer| yes |none|

> Response Examples

```json
{
  "result": [
    {
      "id": "(number)驗證紀錄識別項",
      "deviceClass": "(number)裝置類別，0攝影機|1熱感攝影機|2門口機",
      "deviceClassName": "(string)裝置類別",
      "deviceName": "(string)裝置名稱",
      "recTime": "(number)紀錄時間",
      "utcOffset": "(string)時區時差，格式hh:00:00",
      "memberId": "(string)工號",
      "memberName": "(string)人員名稱",
      "cardId": "(string)卡號",
      "groupNameString": "(string)群組名稱，當有多筆會以底線區隔",
      "identifyingMode": "(string)驗證模式"
    }
  ],
  "pages": "(number)查詢結果總頁數",
  "total": "(number)查詢結果總比數",
  "input": {
    "startTime": "(number)搜尋開始時間，單位毫秒",
    "endTime": "(number)搜尋結束時間，單位毫秒",
    "filterField": [
      "(string)搜尋詞彙適用欄位，可以不使用該參數，由後端代為處理"
    ],
    "filterValue": "(string)搜尋詞彙",
    "sort": [
      {
        "field": "(string)排序欄位",
        "reverse": "(boolean)是否倒序"
      }
    ],
    "pageNumber": "(number)第幾頁",
    "pageSize": "(number)一頁幾筆"
  }
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» result|[object]|true|none||none|
|»» id|string|false|none||none|
|»» deviceClass|string|false|none||none|
|»» deviceClassName|string|false|none||none|
|»» deviceName|string|false|none||none|
|»» recTime|string|false|none||none|
|»» utcOffset|string|false|none||none|
|»» memberId|string|false|none||none|
|»» memberName|string|false|none||none|
|»» cardId|string|false|none||none|
|»» groupNameString|string|false|none||none|
|»» identifyingMode|string|false|none||none|
|» pages|string|true|none||none|
|» total|string|true|none||none|
|» input|object|true|none||none|
|»» startTime|string|true|none||none|
|»» endTime|string|true|none||none|
|»» filterField|[string]|true|none||none|
|»» filterValue|string|true|none||none|
|»» sort|[object]|true|none||none|
|»»» field|string|false|none||none|
|»»» reverse|string|false|none||none|
|»» pageNumber|string|true|none||none|
|»» pageSize|string|true|none||none|

## POST QueryHitListSinglePage  檢視成功列表(全部+縮圖)

POST /api/record/QueryHitListSinglePage

> Body Parameters

```json
{
  "FilterValue": "",
  "Sort": [
    {
      "Field": "id",
      "Reverse": true
    }
  ],
  "startTime": 1734364800000,
  "endTime": 1734451200000
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» FilterValue|body|string| yes |none|
|» Sort|body|[object]| yes |none|
|»» Field|body|string| no |none|
|»» Reverse|body|boolean| no |none|
|» startTime|body|integer| yes |none|
|» endTime|body|integer| yes |none|

> Response Examples

```json
{
  "result": [
    {
      "id": "(number)驗證紀錄識別項",
      "deviceClass": "(number)裝置類別，0攝影機|1熱感攝影機|2門口機",
      "deviceClassName": "(string)裝置類別",
      "deviceName": "(string)裝置名稱",
      "recTime": "(number)紀錄時間",
      "utcOffset": "(string)時區時差，格式hh:00:00",
      "memberId": "(string)工號",
      "memberName": "(string)人員名稱",
      "cardId": "(string)卡號",
      "groupNameString": "(string)群組名稱，當有多筆會以底線區隔",
      "identifyingMode": "(string)驗證模式"
    }
  ],
  "pages": 1,
  "total": "(number)查詢結果總比數",
  "input": {
    "startTime": "(number)搜尋開始時間，單位毫秒",
    "endTime": "(number)搜尋結束時間，單位毫秒",
    "filterField": [
      "(string)搜尋詞彙適用欄位，格式"
    ],
    "filterValue": "(string)搜尋詞彙",
    "sort": [
      {
        "field": "(string)排序欄位",
        "reverse": "(boolean)是否倒序"
      }
    ]
  }
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» result|[object]|true|none||none|
|»» id|string|false|none||none|
|»» deviceClass|string|false|none||none|
|»» deviceClassName|string|false|none||none|
|»» deviceName|string|false|none||none|
|»» recTime|string|false|none||none|
|»» utcOffset|string|false|none||none|
|»» memberId|string|false|none||none|
|»» memberName|string|false|none||none|
|»» cardId|string|false|none||none|
|»» groupNameString|string|false|none||none|
|»» identifyingMode|string|false|none||none|
|» pages|integer|true|none||none|
|» total|string|true|none||none|
|» input|object|true|none||none|
|»» startTime|string|true|none||none|
|»» endTime|string|true|none||none|
|»» filterField|[string]|true|none||none|
|»» filterValue|string|true|none||none|
|»» sort|[object]|true|none||none|
|»»» field|string|false|none||none|
|»»» reverse|string|false|none||none|

## GET QueryHitImage  檢視成功列(原圖)

GET /api/record/QueryHitImage/{hitId}

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|hitId|path|string| yes |辨識成功紀錄ID|

> Response Examples

```json
{
  "result": {
    "id": "(number)驗證紀錄識別項",
    "queryImage": "(string)截圖，格式為base64"
  }
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» result|object|true|none||none|
|»» id|string|true|none||none|
|»» queryImage|string|true|none||none|

## POST QueryNotHitList 檢視失敗列表(頁碼+縮圖)

POST /api/record/QueryNotHitList

> Body Parameters

```json
{
  "FilterValue": "",
  "Sort": [
    {
      "Field": "id",
      "Reverse": true
    }
  ],
  "PageNumber": 1,
  "PageSize": 20,
  "startTime": 0,
  "endTime": 1722989009185
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» FilterValue|body|string| yes |none|
|» Sort|body|[object]| yes |none|
|»» Field|body|string| no |none|
|»» Reverse|body|boolean| no |none|
|» PageNumber|body|integer| yes |none|
|» PageSize|body|integer| yes |none|
|» startTime|body|integer| yes |none|
|» endTime|body|integer| yes |none|

> Response Examples

```json
{
  "result": [
    {
      "id": "(number)驗證紀錄識別項",
      "deviceClass": "(number)裝置類別，0攝影機|1熱感攝影機|2門口機",
      "deviceClassName": "(string)裝置類別",
      "deviceName": "(string)裝置名稱",
      "recTime": "(number)紀錄時間",
      "utcOffset": "(string)時區時差，格式hh:00:00",
      "identifyingMode": "(string)驗證模式"
    }
  ],
  "pages": "(number)查詢結果總頁數",
  "total": "(number)查詢結果總比數",
  "input": {
    "startTime": "(number)搜尋開始時間，單位毫秒",
    "endTime": "(number)搜尋結束時間，單位毫秒",
    "filterField": [
      "(string)搜尋詞彙適用欄位，格式"
    ],
    "filterValue": "(string)搜尋詞彙",
    "sort": [
      {
        "field": "(string)排序欄位",
        "reverse": "(boolean)是否倒序"
      }
    ],
    "pageNumber": "(number)第幾頁",
    "pageSize": "(number)一頁幾筆"
  }
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» result|[object]|true|none||none|
|»» id|string|false|none||none|
|»» deviceClass|string|false|none||none|
|»» deviceClassName|string|false|none||none|
|»» deviceName|string|false|none||none|
|»» recTime|string|false|none||none|
|»» utcOffset|string|false|none||none|
|»» identifyingMode|string|false|none||none|
|» pages|string|true|none||none|
|» total|string|true|none||none|
|» input|object|true|none||none|
|»» startTime|string|true|none||none|
|»» endTime|string|true|none||none|
|»» filterField|[string]|true|none||none|
|»» filterValue|string|true|none||none|
|»» sort|[object]|true|none||none|
|»»» field|string|false|none||none|
|»»» reverse|string|false|none||none|
|»» pageNumber|string|true|none||none|
|»» pageSize|string|true|none||none|

## POST QueryNotHitListSinglePage 檢視失敗列表(全部+縮圖)

POST /api/record/QueryNotHitListSinglePage

> Body Parameters

```json
{
  "FilterValue": "",
  "Sort": [
    {
      "Field": "id",
      "Reverse": true
    }
  ],
  "startTime": 0,
  "endTime": 1722989009185
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» FilterValue|body|string| yes |none|
|» Sort|body|[object]| yes |none|
|»» Field|body|string| no |none|
|»» Reverse|body|boolean| no |none|
|» startTime|body|integer| yes |none|
|» endTime|body|integer| yes |none|

> Response Examples

```json
{
  "result": [
    {
      "id": "(number)驗證紀錄識別項",
      "deviceClass": "(number)裝置類別，0攝影機|1熱感攝影機|2門口機",
      "deviceClassName": "(string)裝置類別",
      "deviceName": "(string)裝置名稱",
      "recTime": "(number)紀錄時間",
      "utcOffset": "(string)時區時差，格式hh:00:00",
      "identifyingMode": "(string)驗證模式"
    }
  ],
  "pages": "(number)查詢結果總頁數",
  "total": "(number)查詢結果總比數",
  "input": {
    "startTime": "(number)搜尋開始時間，單位毫秒",
    "endTime": "(number)搜尋結束時間，單位毫秒",
    "filterField": [
      "(string)搜尋詞彙適用欄位，格式"
    ],
    "filterValue": "(string)搜尋詞彙",
    "sort": [
      {
        "field": "(string)排序欄位",
        "reverse": "(boolean)是否倒序"
      }
    ]
  }
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» result|[object]|true|none||none|
|»» id|string|false|none||none|
|»» deviceClass|string|false|none||none|
|»» deviceClassName|string|false|none||none|
|»» deviceName|string|false|none||none|
|»» recTime|string|false|none||none|
|»» utcOffset|string|false|none||none|
|»» identifyingMode|string|false|none||none|
|» pages|string|true|none||none|
|» total|string|true|none||none|
|» input|object|true|none||none|
|»» startTime|string|true|none||none|
|»» endTime|string|true|none||none|
|»» filterField|[string]|true|none||none|
|»» filterValue|string|true|none||none|
|»» sort|[object]|true|none||none|
|»»» field|string|false|none||none|
|»»» reverse|string|false|none||none|

## GET QueryNotHitImage 檢視失敗列表(原圖)

GET /api/record/QueryNotHitImage/{notHitId}

> Body Parameters

```json
{}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|notHitId|path|string| yes |辨識失敗紀錄ID|
|body|body|object| no |none|

> Response Examples

```json
{
  "result": {
    "id": "(number)驗證紀錄識別項",
    "queryImage": "(string)截圖，格式為base64"
  }
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» result|object|true|none||none|
|»» id|string|true|none||none|
|»» queryImage|string|true|none||none|

# Employee

## POST QueryEmployeeList 檢視人員列表(頁碼)

POST /api/Employee/QueryEmployeeList

> Body Parameters

```json
{
  "filterField": [],
  "filterValue": "",
  "pageNumber": 1,
  "pageSize": 25
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» filterField|body|[string]| yes |none|
|» filterValue|body|string| yes |none|
|» pageNumber|body|integer| yes |none|
|» pageSize|body|integer| yes |none|

> Response Examples

```json
{
  "result": [
    {
      "employeeID": "(string)工號",
      "employeeName": "(string)人員名稱",
      "cardID": "(string)卡號",
      "memberGUID": "(string)人員識別項",
      "enable": "(number)是否啟用人員，0停用|1啟用",
      "refA": "(string)備註",
      "createTime": "(string)建立日期，格式yyyy-MM-dd HH:mm",
      "utcOffset": "(string)時區時差，格式hh:00:00",
      "enrollImage": "(string)照片縮圖，格式為base64",
      "group": [
        {
          "groupGUID": "(string)群組識別項",
          "groupName": "(string)群組名稱"
        }
      ],
      "groupName": "(string)顯示用群組名稱"
    }
  ],
  "pages": "(number)查詢結果總頁數",
  "total": "(number)查詢結果總比數",
  "input": {
    "filterField": [
      "(string)搜尋詞彙適用欄位，格式"
    ],
    "filterValue": "(string)搜尋詞彙",
    "sort": [
      {
        "field": "(string)排序欄位",
        "reverse": "(boolean)是否倒序"
      }
    ],
    "pageNumber": "(number)第幾頁",
    "pageSize": "(number)一頁幾筆"
  }
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» result|[object]|true|none||none|
|»» employeeID|string|false|none||none|
|»» employeeName|string|false|none||none|
|»» cardID|string|false|none||none|
|»» memberGUID|string|false|none||none|
|»» enable|string|false|none||none|
|»» refA|string|false|none||none|
|»» createTime|string|false|none||none|
|»» utcOffset|string|false|none||none|
|»» enrollImage|string|false|none||none|
|»» group|[object]|false|none||none|
|»»» groupGUID|string|false|none||none|
|»»» groupName|string|false|none||none|
|»» groupName|string|false|none||none|
|» pages|string|true|none||none|
|» total|string|true|none||none|
|» input|object|true|none||none|
|»» filterField|[string]|true|none||none|
|»» filterValue|string|true|none||none|
|»» sort|[object]|true|none||none|
|»»» field|string|false|none||none|
|»»» reverse|string|false|none||none|
|»» pageNumber|string|true|none||none|
|»» pageSize|string|true|none||none|

## POST QuerySinglePage 檢視人員列表(全部)

POST /api/Employee/QuerySinglePage

> Body Parameters

```json
{
  "filterValue": "0031",
  "sort": [
    {
      "field": "employeeName",
      "reverse": false
    }
  ]
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» filterValue|body|string| yes |none|
|» sort|body|[object]| yes |none|
|»» field|body|string| no |none|
|»» reverse|body|boolean| no |none|

> Response Examples

```json
{
  "result": [
    {
      "employeeID": "(string)工號",
      "employeeName": "(string)人員名稱",
      "cardID": "(string)卡號",
      "memberGUID": "(string)人員識別項",
      "enable": "(number)是否啟用人員，0停用|1啟用",
      "refA": "(string)備註",
      "createTime": "(string)建立日期，格式yyyy-MM-dd HH:mm",
      "utcOffset": "(string)時區時差，格式hh:00:00",
      "enrollImage": "(string)照片縮圖，格式為base64",
      "group": [
        {
          "groupGUID": "(string)群組識別項",
          "groupName": "(string)群組名稱"
        }
      ],
      "groupName": "(string)顯示用群組名稱"
    }
  ],
  "pages": "(number)查詢結果總頁數",
  "total": "(number)查詢結果總比數",
  "input": {
    "filterField": [
      "(string)搜尋詞彙適用欄位，格式"
    ],
    "filterValue": "(string)搜尋詞彙",
    "sort": [
      {
        "field": "(string)排序欄位",
        "reverse": "(boolean)是否倒序"
      }
    ]
  }
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» result|[object]|true|none||none|
|»» employeeID|string|false|none||none|
|»» employeeName|string|false|none||none|
|»» cardID|string|false|none||none|
|»» memberGUID|string|false|none||none|
|»» enable|string|false|none||none|
|»» refA|string|false|none||none|
|»» createTime|string|false|none||none|
|»» utcOffset|string|false|none||none|
|»» enrollImage|string|false|none||none|
|»» group|[object]|false|none||none|
|»»» groupGUID|string|false|none||none|
|»»» groupName|string|false|none||none|
|»» groupName|string|false|none||none|
|» pages|string|true|none||none|
|» total|string|true|none||none|
|» input|object|true|none||none|
|»» filterField|[string]|true|none||none|
|»» filterValue|string|true|none||none|
|»» sort|[object]|true|none||none|
|»»» field|string|false|none||none|
|»»» reverse|string|false|none||none|

## GET QueryEmployee 檢視人員(縮圖)

GET /api/Employee/QueryEmployee/fb0552d4-43f7-45b9-9f1d-fa6b0660b005

> Response Examples

```json
{
  "result": [
    {
      "memberGUID": "312D673A-D215-451D-953C-195E7EF3E4B4",
      "employeeID": "1002",
      "employeeName": "ENABLE測試",
      "cardID": "001007",
      "enable": 0,
      "refA": null,
      "createTime": 1728958688489,
      "utcOffset": "08:00:00",
      "enrollImage": "",
      "group": [
        {
          "groupGUID": "a991bef8-f7ce-4ab5-b5a1-653e67d7a044",
          "groupName": "Default"
        },
        {
          "groupGUID": "E8985C66-6969-439E-A3B1-9DD5D68355E0",
          "groupName": "南波萬"
        }
      ],
      "groupName": "Default,南波萬"
    }
  ],
  "pages": 1,
  "total": 1,
  "input": "312D673A-D215-451D-953C-195E7EF3E4B4"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» result|[object]|true|none||none|
|»» memberGUID|string|false|none||none|
|»» employeeID|string|false|none||none|
|»» employeeName|string|false|none||none|
|»» cardID|string|false|none||none|
|»» enable|integer|false|none||none|
|»» refA|null|false|none||none|
|»» createTime|integer|false|none||none|
|»» utcOffset|string|false|none||none|
|»» enrollImage|string|false|none||none|
|»» group|[object]|false|none||none|
|»»» groupGUID|string|true|none||none|
|»»» groupName|string|true|none||none|
|»» groupName|string|false|none||none|
|» pages|integer|true|none||none|
|» total|integer|true|none||none|
|» input|string|true|none||none|

## GET QueryImage 檢視人員(原圖)

GET /api/Employee/QueryImage/cb813995-5552-46c6-a515-1b38c42b3652

> Response Examples

```json
{
  "result": {
    "memberGUID": "(number)驗證紀錄識別項",
    "enrollImage": "(string)照片，格式為base64"
  }
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» result|object|true|none||none|
|»» memberGUID|string|true|none||none|
|»» enrollImage|string|true|none||none|

## POST CheckImage 檢查照片

POST /api/Employee/CheckImage

> Body Parameters

```yaml
image: string

```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» image|body|string(binary)| yes |none|

> Response Examples

```json
{
  "id": "(string)通常為識別碼",
  "success": "(boolean)是否執行成功",
  "errorMessage": "(string)若執行失敗的原因說明",
  "anyMsg": "(string)若執行成功的內容補充",
  "anyObject": [
    {
      "groupList": [
        "(string)群組識別項，後台專用(經匹配後之結果)"
      ],
      "imageFilePath": "(string)照片存放路徑，後台專用(經匹配後之結果)",
      "status": "(int)匯入格式分析狀態，0正常|1錯誤|2容許錯誤範圍由後台調整資料",
      "statusDescription": "(string)匯入格式分析狀態描述",
      "employeeName": "(stinrg)CSV輸入項",
      "employeeID": "(stinrg)CSV輸入項",
      "cardNo": "(stinrg)CSV輸入項",
      "group": "(stinrg)CSV輸入項",
      "remarkA": "(stinrg)CSV輸入項",
      "remarkB": "(stinrg)CSV輸入項",
      "remarkC": "(stinrg)CSV輸入項",
      "remarkD": "(stinrg)CSV輸入項",
      "remarkE": "(stinrg)CSV輸入項"
    }
  ]
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» id|string|true|none||none|
|» success|string|true|none||none|
|» errorMessage|string|true|none||none|
|» anyMsg|string|true|none||none|
|» anyObject|[object]|true|none||none|
|»» groupList|[string]|false|none||none|
|»» imageFilePath|string|false|none||none|
|»» status|string|false|none||none|
|»» statusDescription|string|false|none||none|
|»» employeeName|string|false|none||none|
|»» employeeID|string|false|none||none|
|»» cardNo|string|false|none||none|
|»» group|string|false|none||none|
|»» remarkA|string|false|none||none|
|»» remarkB|string|false|none||none|
|»» remarkC|string|false|none||none|
|»» remarkD|string|false|none||none|
|»» remarkE|string|false|none||none|

## POST Enroll 註冊人員

POST /api/Employee/Enroll

> Body Parameters

```yaml
EmployeeID: S0008
EmployeeName: 星巴客1
CardID: EC0001
RefA: ""
EnrollImage: string
GroupGUID: a991bef8-f7ce-4ab5-b5a1-653e67d7a044

```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» EmployeeID|body|string| yes |工號|
|» EmployeeName|body|string| yes |人員名稱|
|» CardID|body|string| no |卡號|
|» RefA|body|string| yes |備註|
|» EnrollImage|body|string(binary)| yes |臉照|
|» GroupGUID|body|string| yes |設定群組(如果需要多個，就設置重複 Key 的參數)|

> Response Examples

```json
{
  "id": "(string)通常為識別碼",
  "success": "(boolean)是否執行成功",
  "errorMessage": "(string)若執行失敗的原因說明",
  "anyMsg": "(string)若執行成功的內容補充",
  "anyObject": "(object)需要回傳的物件"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» id|string|true|none||none|
|» success|string|true|none||none|
|» errorMessage|string|true|none||none|
|» anyMsg|string|true|none||none|
|» anyObject|string|true|none||none|

## POST EnrollList 批次註冊人員

POST /api/Employee/EnrollList

> Body Parameters

```yaml
CsvDocument: string
FileList: string

```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» CsvDocument|body|string(binary)| yes |註冊人員明細|
|» FileList|body|string(binary)| yes |none|

> Response Examples

```json
{
  "id": "(string)通常為識別碼",
  "success": "(boolean)是否執行成功",
  "errorMessage": "(string)若執行失敗的原因說明",
  "anyMsg": "(string)若執行成功的內容補充",
  "anyObject": [
    {
      "groupList": [
        "(string)群組識別項，後台專用(經匹配後之結果)"
      ],
      "imageFilePath": "(string)照片存放路徑，後台專用(經匹配後之結果)",
      "status": "(int)匯入格式分析狀態，0正常|1錯誤|2容許錯誤範圍由後台調整資料",
      "statusDescription": "(string)匯入格式分析狀態描述",
      "employeeName": "(stinrg)CSV輸入項",
      "employeeID": "(stinrg)CSV輸入項",
      "cardNo": "(stinrg)CSV輸入項",
      "group": "(stinrg)CSV輸入項",
      "refA": "(stinrg)CSV輸入項"
    }
  ]
}
```

```json
{
  "id": "",
  "success": false,
  "errorMessage": "",
  "anyMsg": "",
  "anyObject": [
    {
      "groupList": [],
      "imageFilePath": "",
      "status": 1,
      "statusDescription": "Employee ID 無法重複。",
      "employeeName": "張捷致",
      "employeeID": "910113651",
      "cardNo": "A0001",
      "group": "Default_測試新增第1筆",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [],
      "imageFilePath": "",
      "status": 1,
      "statusDescription": "Employee ID 無法重複。",
      "employeeName": "唐勝玉",
      "employeeID": "919693079",
      "cardNo": "A0002",
      "group": "Default_測試新增第2筆",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [],
      "imageFilePath": "",
      "status": 1,
      "statusDescription": "Employee ID 無法重複。",
      "employeeName": "楊健鳴",
      "employeeID": "956216538",
      "cardNo": "A0003",
      "group": "Default_new",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [],
      "imageFilePath": "",
      "status": 1,
      "statusDescription": "Employee ID 無法重複。",
      "employeeName": "周研萍",
      "employeeID": "954106472",
      "cardNo": "A0004",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [],
      "imageFilePath": "",
      "status": 1,
      "statusDescription": "Employee ID 無法重複。",
      "employeeName": "楊全娜",
      "employeeID": "927773162",
      "cardNo": "A0005",
      "group": "Default",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [],
      "imageFilePath": "",
      "status": 1,
      "statusDescription": "Employee ID 無法重複。",
      "employeeName": "藍珮肇",
      "employeeID": "954062138",
      "cardNo": "A0006",
      "group": "new",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [],
      "imageFilePath": "",
      "status": 1,
      "statusDescription": "Employee ID 無法重複。",
      "employeeName": "蔡園妍",
      "employeeID": "952621482",
      "cardNo": "A0007",
      "group": "測試新增第1筆",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [],
      "imageFilePath": "",
      "status": 1,
      "statusDescription": "Employee ID 無法重複。",
      "employeeName": "鄭奇鈺",
      "employeeID": "929172288",
      "cardNo": "A0008",
      "group": "測試新增第2筆",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [],
      "imageFilePath": "",
      "status": 1,
      "statusDescription": "Employee ID 無法重複。",
      "employeeName": "陳偉明",
      "employeeID": "931528446",
      "cardNo": "A0009",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [],
      "imageFilePath": "",
      "status": 1,
      "statusDescription": "Employee ID 無法重複。",
      "employeeName": "金城雅",
      "employeeID": "919981058",
      "cardNo": "A0010",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [],
      "imageFilePath": "",
      "status": 1,
      "statusDescription": "Employee ID 無法重複。",
      "employeeName": "林卓泉",
      "employeeID": "919051874",
      "cardNo": "A0011",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [],
      "imageFilePath": "",
      "status": 1,
      "statusDescription": "Employee ID 無法重複。",
      "employeeName": "陸帆羽",
      "employeeID": "926895709",
      "cardNo": "A0012",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [],
      "imageFilePath": "",
      "status": 1,
      "statusDescription": "Employee ID 無法重複。",
      "employeeName": "蔡若菡",
      "employeeID": "936298090",
      "cardNo": "A0013",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [],
      "imageFilePath": "",
      "status": 1,
      "statusDescription": "Employee ID 無法重複。",
      "employeeName": "葉嘉影",
      "employeeID": "938268081",
      "cardNo": "A0014",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [],
      "imageFilePath": "",
      "status": 1,
      "statusDescription": "Employee ID 無法重複。",
      "employeeName": "王謙鑫",
      "employeeID": "955250432",
      "cardNo": "A0015",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [],
      "imageFilePath": "",
      "status": 1,
      "statusDescription": "Employee ID 無法重複。",
      "employeeName": "楊邦駱",
      "employeeID": "919611743",
      "cardNo": "A0016",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [],
      "imageFilePath": "",
      "status": 1,
      "statusDescription": "Employee ID 無法重複。",
      "employeeName": "董均爾",
      "employeeID": "961242226",
      "cardNo": "A0017",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [],
      "imageFilePath": "",
      "status": 1,
      "statusDescription": "Employee ID 無法重複。",
      "employeeName": "溫來奇",
      "employeeID": "925773358",
      "cardNo": "A0018",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [],
      "imageFilePath": "",
      "status": 1,
      "statusDescription": "Employee ID 無法重複。",
      "employeeName": "曹思精",
      "employeeID": "923566523",
      "cardNo": "A0019",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [],
      "imageFilePath": "",
      "status": 1,
      "statusDescription": "Employee ID 無法重複。",
      "employeeName": "古津燕",
      "employeeID": "921819915",
      "cardNo": "A0020",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [],
      "imageFilePath": "",
      "status": 1,
      "statusDescription": "Employee ID 無法重複。",
      "employeeName": "黃堇琦",
      "employeeID": "915486493",
      "cardNo": "A0021",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [],
      "imageFilePath": "",
      "status": 1,
      "statusDescription": "Employee ID 無法重複。",
      "employeeName": "黃君芸",
      "employeeID": "921287850",
      "cardNo": "A0022",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [],
      "imageFilePath": "",
      "status": 1,
      "statusDescription": "Employee ID 無法重複。",
      "employeeName": "梁宸瑋",
      "employeeID": "915547866",
      "cardNo": "A0023",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [],
      "imageFilePath": "",
      "status": 1,
      "statusDescription": "Employee ID 無法重複。",
      "employeeName": "陳奇拓",
      "employeeID": "931633419",
      "cardNo": "A0024",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [],
      "imageFilePath": "",
      "status": 1,
      "statusDescription": "Employee ID 無法重複。",
      "employeeName": "李棋祺",
      "employeeID": "956644765",
      "cardNo": "A0025",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [],
      "imageFilePath": "",
      "status": 1,
      "statusDescription": "Employee ID 無法重複。",
      "employeeName": "朱雄風",
      "employeeID": "913096197",
      "cardNo": "A0026",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [],
      "imageFilePath": "",
      "status": 1,
      "statusDescription": "Employee ID 無法重複。",
      "employeeName": "湯中婉",
      "employeeID": "936615484",
      "cardNo": "A0027",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [],
      "imageFilePath": "",
      "status": 1,
      "statusDescription": "Employee ID 無法重複。",
      "employeeName": "王林汝",
      "employeeID": "911061801",
      "cardNo": "A0028",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [],
      "imageFilePath": "",
      "status": 1,
      "statusDescription": "Employee ID 無法重複。",
      "employeeName": "吳冬霞",
      "employeeID": "916458031",
      "cardNo": "A0029",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [],
      "imageFilePath": "",
      "status": 1,
      "statusDescription": "Employee ID 無法重複。",
      "employeeName": "余熙辛",
      "employeeID": "910415661",
      "cardNo": "A0030",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [],
      "imageFilePath": "",
      "status": 1,
      "statusDescription": "Employee ID 無法重複。",
      "employeeName": "周珍芬",
      "employeeID": "960834338",
      "cardNo": "A0031",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [],
      "imageFilePath": "",
      "status": 1,
      "statusDescription": "Employee ID 無法重複。",
      "employeeName": "黃尚錦",
      "employeeID": "923904546",
      "cardNo": "A0032",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [],
      "imageFilePath": "",
      "status": 1,
      "statusDescription": "註冊照片未匹配。",
      "employeeName": "田曄祟",
      "employeeID": "922509754",
      "cardNo": "A0033",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\蔡崇聰_989171674.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "蔡崇聰",
      "employeeID": "989171674",
      "cardNo": "A0034",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\溫之尹_923531503.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "溫之尹",
      "employeeID": "923531503",
      "cardNo": "A0035",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\張才祐_989227616.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "張才祐",
      "employeeID": "989227616",
      "cardNo": "A0036",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\劉文暉_920086756.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "劉文暉",
      "employeeID": "920086756",
      "cardNo": "A0037",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\陳信旭_929201752.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "陳信旭",
      "employeeID": "929201752",
      "cardNo": "A0038",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\張敬馨_917392160.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "張敬馨",
      "employeeID": "917392160",
      "cardNo": "A0039",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\簡城翔_927177024.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "簡城翔",
      "employeeID": "927177024",
      "cardNo": "A0040",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\方家術_961409474.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "方家術",
      "employeeID": "961409474",
      "cardNo": "A0041",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\白天浩_963818547.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "白天浩",
      "employeeID": "963818547",
      "cardNo": "A0042",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\侯子潞_930500129.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "侯子潞",
      "employeeID": "930500129",
      "cardNo": "A0043",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\石修寧_929432042.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "石修寧",
      "employeeID": "929432042",
      "cardNo": "A0044",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\宋嬡濮_955651170.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "宋嬡濮",
      "employeeID": "955651170",
      "cardNo": "A0045",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\卓全鷺_928699157.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "卓全鷺",
      "employeeID": "928699157",
      "cardNo": "A0046",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\張洪筠_961144025.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "張洪筠",
      "employeeID": "961144025",
      "cardNo": "A0047",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\周影景_968372894.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "周影景",
      "employeeID": "968372894",
      "cardNo": "A0048",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\黃瀾玲_935763907.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "黃瀾玲",
      "employeeID": "935763907",
      "cardNo": "A0049",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\田亞倩_923914980.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "田亞倩",
      "employeeID": "923914980",
      "cardNo": "A0050",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\劉方磊_919684938.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "劉方磊",
      "employeeID": "919684938",
      "cardNo": "A0051",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\陳品泛_987270579.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "陳品泛",
      "employeeID": "987270579",
      "cardNo": "A0052",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\朱政豪_935166374.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "朱政豪",
      "employeeID": "935166374",
      "cardNo": "A0053",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\嚴國坤_913445978.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "嚴國坤",
      "employeeID": "913445978",
      "cardNo": "A0054",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\謝俞諄_954110579.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "謝俞諄",
      "employeeID": "954110579",
      "cardNo": "A0055",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\邵宛沐_952042723.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "邵宛沐",
      "employeeID": "952042723",
      "cardNo": "A0056",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\孫嚴威_960476745.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "孫嚴威",
      "employeeID": "960476745",
      "cardNo": "A0057",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\袁亭棋_912389419.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "袁亭棋",
      "employeeID": "912389419",
      "cardNo": "A0058",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\孫琪谷_953237227.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "孫琪谷",
      "employeeID": "953237227",
      "cardNo": "A0059",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\廖悟瀟_926096886.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "廖悟瀟",
      "employeeID": "926096886",
      "cardNo": "A0060",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\藍宸容_921794011.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "藍宸容",
      "employeeID": "921794011",
      "cardNo": "A0061",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\林明秉_923282660.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "林明秉",
      "employeeID": "923282660",
      "cardNo": "A0062",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\鐘璟穎_952468129.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "鐘璟穎",
      "employeeID": "952468129",
      "cardNo": "A0063",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\傅竹紈_982466356.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "傅竹紈",
      "employeeID": "982466356",
      "cardNo": "A0064",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\金娟露_932486937.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "金娟露",
      "employeeID": "932486937",
      "cardNo": "A0065",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\張勝慧_919012369.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "張勝慧",
      "employeeID": "919012369",
      "cardNo": "A0066",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\丁嚴思_928514904.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "丁嚴思",
      "employeeID": "928514904",
      "cardNo": "A0067",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\范瑋笑_928199151.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "范瑋笑",
      "employeeID": "928199151",
      "cardNo": "A0068",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\吳君慈_921300904.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "吳君慈",
      "employeeID": "921300904",
      "cardNo": "A0069",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\莊泓湘_913141850.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "莊泓湘",
      "employeeID": "913141850",
      "cardNo": "A0070",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\賴汶諄_952799002.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "賴汶諄",
      "employeeID": "952799002",
      "cardNo": "A0071",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\林昀璟_953406082.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "林昀璟",
      "employeeID": "953406082",
      "cardNo": "A0072",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\吳慶聰_923258283.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "吳慶聰",
      "employeeID": "923258283",
      "cardNo": "A0073",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\吳新然_952965416.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "吳新然",
      "employeeID": "952965416",
      "cardNo": "A0074",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\鄧江瑞_920372682.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "鄧江瑞",
      "employeeID": "920372682",
      "cardNo": "A0075",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\李永薇_972564776.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "李永薇",
      "employeeID": "972564776",
      "cardNo": "A0076",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\歐于懷_937444839.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "歐于懷",
      "employeeID": "937444839",
      "cardNo": "A0077",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\錢少鴻_921615835.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "錢少鴻",
      "employeeID": "921615835",
      "cardNo": "A0078",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\古丞璟_936925415.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "古丞璟",
      "employeeID": "936925415",
      "cardNo": "A0079",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\高夫慶_923012906.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "高夫慶",
      "employeeID": "923012906",
      "cardNo": "A0080",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\黃嘉廷_913674120.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "黃嘉廷",
      "employeeID": "913674120",
      "cardNo": "A0081",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\蔡凌清_930879419.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "蔡凌清",
      "employeeID": "930879419",
      "cardNo": "A0082",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\李睿馨_926921214.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "李睿馨",
      "employeeID": "926921214",
      "cardNo": "A0083",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\邵漢霞_988476207.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "邵漢霞",
      "employeeID": "988476207",
      "cardNo": "A0084",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\賴木鴻_958136722.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "賴木鴻",
      "employeeID": "958136722",
      "cardNo": "A0085",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\張華英_914068744.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "張華英",
      "employeeID": "914068744",
      "cardNo": "A0086",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\汪召雄_915139941.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "汪召雄",
      "employeeID": "915139941",
      "cardNo": "A0087",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\張可堯_927249651.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "張可堯",
      "employeeID": "927249651",
      "cardNo": "A0088",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\李昀瀾_956712549.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "李昀瀾",
      "employeeID": "956712549",
      "cardNo": "A0089",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\王清良_987172090.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "王清良",
      "employeeID": "987172090",
      "cardNo": "A0090",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\柯易哲_939366141.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "柯易哲",
      "employeeID": "939366141",
      "cardNo": "A0091",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\翁聖鑫_935855359.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "翁聖鑫",
      "employeeID": "935855359",
      "cardNo": "A0092",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\阮耀聰_926485477.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "阮耀聰",
      "employeeID": "926485477",
      "cardNo": "A0093",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\吳佑茂_956968571.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "吳佑茂",
      "employeeID": "956968571",
      "cardNo": "A0094",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\黃棋耿_935077764.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "黃棋耿",
      "employeeID": "935077764",
      "cardNo": "A0095",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\朱楠蓁_952422919.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "朱楠蓁",
      "employeeID": "952422919",
      "cardNo": "A0096",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\邱語諄_955412188.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "邱語諄",
      "employeeID": "955412188",
      "cardNo": "A0097",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\孫智汝_932894290.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "孫智汝",
      "employeeID": "932894290",
      "cardNo": "A0098",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\蔡俠方_927298591.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "蔡俠方",
      "employeeID": "927298591",
      "cardNo": "A0099",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    },
    {
      "groupList": [
        "a991bef8-f7ce-4ab5-b5a1-653e67d7a044"
      ],
      "imageFilePath": "D:\\develop\\臉辨資料中心\\frs_net6\\Web.Api\\bin\\Debug\\net6.0\\UploadEnroll\\utc_20240905_070610\\李以華_960795207.jpeg",
      "status": 2,
      "statusDescription": "Group 配置預設群組。",
      "employeeName": "李以華",
      "employeeID": "960795207",
      "cardNo": "A0100",
      "group": "",
      "remarkA": "",
      "remarkB": "",
      "remarkC": "",
      "remarkD": "",
      "remarkE": ""
    }
  ]
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» id|string|true|none||none|
|» success|string|true|none||none|
|» errorMessage|string|true|none||none|
|» anyMsg|string|true|none||none|
|» anyObject|[object]|true|none||none|
|»» groupList|[string]|false|none||none|
|»» imageFilePath|string|false|none||none|
|»» status|string|false|none||none|
|»» statusDescription|string|false|none||none|
|»» employeeName|string|false|none||none|
|»» employeeID|string|false|none||none|
|»» cardNo|string|false|none||none|
|»» group|string|false|none||none|
|»» refA|string|false|none||none|

HTTP Status Code **400**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» id|string|true|none||none|
|» success|boolean|true|none||none|
|» errorMessage|string|true|none||none|
|» anyMsg|string|true|none||none|
|» anyObject|[object]|true|none||none|
|»» groupList|[string]|true|none||none|
|»» imageFilePath|string|true|none||none|
|»» status|integer|true|none||none|
|»» statusDescription|string|true|none||none|
|»» employeeName|string|true|none||none|
|»» employeeID|string|true|none||none|
|»» cardNo|string|true|none||none|
|»» group|string|true|none||none|
|»» remarkA|string|true|none||none|
|»» remarkB|string|true|none||none|
|»» remarkC|string|true|none||none|
|»» remarkD|string|true|none||none|
|»» remarkE|string|true|none||none|

## PUT Edit 編輯人員

PUT /api/Employee/Edit

> Body Parameters

```json
{
  "memberGUID": "fe73f289-ff9a-4999-82ba-56a1128ff7fe",
  "employeeID": "EMID0001",
  "employeeName": "編輯測試",
  "cardID": "CID0001",
  "refA": "隨便寫",
  "enable": 1,
  "groupGUID": [
    "a991bef8-f7ce-4ab5-b5a1-653e67d7a044",
    "E8985C66-6969-439E-A3B1-9DD5D68355E0"
  ]
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» memberGUID|body|string| yes |none|
|» employeeID|body|string| yes |none|
|» employeeName|body|string| yes |none|
|» cardID|body|string| yes |none|
|» refA|body|string| yes |none|
|» enable|body|integer| yes |none|
|» groupGUID|body|[string]| yes |none|

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

## PUT EditImage 更換臉照

PUT /api/Employee/EditImage

> Body Parameters

```yaml
MemberGUID: 48bc6a7a-91cd-4527-ae0a-44c07deb6653
EnrollImage: string

```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» MemberGUID|body|string| yes |人員識別項|
|» EnrollImage|body|string(binary)| yes |照片|

> Response Examples

```json
{
  "id": "(string)通常為識別碼",
  "success": "(boolean)是否執行成功",
  "errorMessage": "(string)若執行失敗的原因說明",
  "anyMsg": "(string)若執行成功的內容補充",
  "anyObject": "(object)需要回傳的物件"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» id|string|true|none||none|
|» success|string|true|none||none|
|» errorMessage|string|true|none||none|
|» anyMsg|string|true|none||none|
|» anyObject|string|true|none||none|

## PUT EditEnable 開啟關閉人員

PUT /api/Employee/EditEnable/48bc6a7a-91cd-4527-ae0a-44c07deb6653

> Response Examples

```json
{
  "id": "(string)通常為識別碼",
  "success": "(boolean)是否執行成功",
  "errorMessage": "(string)若執行失敗的原因說明",
  "anyMsg": "(string)若執行成功的內容補充",
  "anyObject": "(object)需要回傳的物件"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» id|string|true|none||none|
|» success|string|true|none||none|
|» errorMessage|string|true|none||none|
|» anyMsg|string|true|none||none|
|» anyObject|string|true|none||none|

## PUT EditGroup 設定多人員關聯群組

PUT /api/Employee/EditGroup

> Body Parameters

```json
{
  "MemberList": [
    "312D673A-D215-451D-953C-195E7EF3E4B4",
    "212D673A-D215-451D-953C-195E7EF3E4B2"
  ],
  "GroupList": [
    "a991bef8-f7ce-4ab5-b5a1-653e67d7a044",
    "E8985C66-6969-439E-A3B1-9DD5D68355E0"
  ]
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» MemberList|body|[string]| yes |none|
|» GroupList|body|[string]| yes |none|

> Response Examples

```json
{
  "id": "(string)通常為識別碼",
  "success": "(boolean)是否執行成功",
  "errorMessage": "(string)若執行失敗的原因說明",
  "anyMsg": "(string)若執行成功的內容補充",
  "anyObject": "(object)需要回傳的物件"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» id|string|true|none||none|
|» success|string|true|none||none|
|» errorMessage|string|true|none||none|
|» anyMsg|string|true|none||none|
|» anyObject|string|true|none||none|

## DELETE Remove 移除人員

DELETE /api/Employee/Remove

> Body Parameters

```json
{
  "MemberGUID": ""
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» MemberGUID|body|string| yes |none|

> Response Examples

```json
{
  "id": "(string)通常為識別碼",
  "success": "(boolean)是否執行成功",
  "errorMessage": "(string)若執行失敗的原因說明",
  "anyMsg": "(string)若執行成功的內容補充",
  "anyObject": "(object)需要回傳的物件"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» id|string|true|none||none|
|» success|string|true|none||none|
|» errorMessage|string|true|none||none|
|» anyMsg|string|true|none||none|
|» anyObject|string|true|none||none|

## DELETE RemoveList 批次移除人員

DELETE /api/Employee/RemoveList

> Body Parameters

```json
{
  "MemberGUID": [
    "312D673A-D215-451D-953C-195E7EF3E4B4",
    "312D673A-D215-451D-953C-195E7EF3E4B5"
  ]
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» MemberGUID|body|[string]| yes |none|

> Response Examples

```json
{
  "id": "(string)通常為識別碼",
  "success": "(boolean)是否執行成功",
  "errorMessage": "(string)若執行失敗的原因說明",
  "anyMsg": "(string)若執行成功的內容補充",
  "anyObject": "(object)需要回傳的物件"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» id|string|true|none||none|
|» success|string|true|none||none|
|» errorMessage|string|true|none||none|
|» anyMsg|string|true|none||none|
|» anyObject|string|true|none||none|

# Visitor

## POST QueryVisitorList 檢視訪客列表(頁碼)

POST /api/visitor/QueryVisitorList

> Body Parameters

```json
{
  "FilterValue": "",
  "Sort": [
    {
      "Field": "visitorName",
      "Reverse": true
    }
  ],
  "PageNumber": 1,
  "PageSize": 20
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» FilterValue|body|string| yes |none|
|» Sort|body|[object]| yes |none|
|»» Field|body|string| no |none|
|»» Reverse|body|boolean| no |none|
|» PageNumber|body|integer| yes |none|
|» PageSize|body|integer| yes |none|

> Response Examples

```json
{
  "result": [
    {
      "memberName": "(string)訪客名稱",
      "memberGUID": "(string)訪客識別項",
      "cardID": "(string)卡號",
      "createTime": "(string)建立日期，格式yyyy-MM-dd HH:mm",
      "utcOffset": "(string)時區時差，格式hh:00:00",
      "group": [
        {
          "groupGUID": "(string)群組識別項",
          "groupName": "(string)群組名稱"
        }
      ],
      "groupName": "(string)顯示用群組名稱"
    }
  ],
  "pages": "(number)查詢結果總頁數",
  "total": "(number)查詢結果總比數",
  "input": {
    "filterField": [
      "(string)搜尋詞彙適用欄位，格式"
    ],
    "filterValue": "(string)搜尋詞彙",
    "sort": [
      {
        "field": "(string)排序欄位",
        "reverse": "(boolean)是否倒序"
      }
    ],
    "pageNumber": "(number)第幾頁",
    "pageSize": "(number)一頁幾筆"
  }
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» result|[object]|true|none||none|
|»» memberName|string|false|none||none|
|»» memberGUID|string|false|none||none|
|»» cardID|string|false|none||none|
|»» createTime|string|false|none||none|
|»» utcOffset|string|false|none||none|
|»» group|[object]|false|none||none|
|»»» groupGUID|string|false|none||none|
|»»» groupName|string|false|none||none|
|»» groupName|string|false|none||none|
|» pages|string|true|none||none|
|» total|string|true|none||none|
|» input|object|true|none||none|
|»» filterField|[string]|true|none||none|
|»» filterValue|string|true|none||none|
|»» sort|[object]|true|none||none|
|»»» field|string|false|none||none|
|»»» reverse|string|false|none||none|
|»» pageNumber|string|true|none||none|
|»» pageSize|string|true|none||none|

## POST QuerySinglePage 檢視訪客列表(全部)

POST /api/Visitor/QuerySinglePage

> Body Parameters

```json
{
  "filterValue": ""
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» filterValue|body|string| yes |none|

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

## POST Enroll 添加訪客

POST /api/visitor/Enroll

> Body Parameters

```json
{
  "VisitorName": "黃小寶",
  "CardID": "00003"
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» VisitorName|body|string| yes |none|
|» CardID|body|string| yes |none|

> Response Examples

```json
{
  "id": "(string)通常為識別碼",
  "success": "(boolean)是否執行成功",
  "errorMessage": "(string)若執行失敗的原因說明",
  "anyMsg": "(string)若執行成功的內容補充",
  "anyObject": "(object)需要回傳的物件"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» id|string|true|none||none|
|» success|string|true|none||none|
|» errorMessage|string|true|none||none|
|» anyMsg|string|true|none||none|
|» anyObject|string|true|none||none|

## PUT Edit 編輯訪客

PUT /api/visitor/Edit

> Body Parameters

```json
{
  "MemberGuid": "0d9b8425-727b-4a3e-882b-48dbfe543db8",
  "VisitorName": "波賽",
  "CardID": "00009",
  "Enable": 1
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» MemberGuid|body|string| yes |none|
|» VisitorName|body|string| yes |none|
|» CardID|body|string| yes |none|
|» Enable|body|integer| yes |none|

> Response Examples

```json
{
  "id": "(string)通常為識別碼",
  "success": "(boolean)是否執行成功",
  "errorMessage": "(string)若執行失敗的原因說明",
  "anyMsg": "(string)若執行成功的內容補充",
  "anyObject": "(object)需要回傳的物件"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» id|string|true|none||none|
|» success|string|true|none||none|
|» errorMessage|string|true|none||none|
|» anyMsg|string|true|none||none|
|» anyObject|string|true|none||none|

## PUT EditEnable 開啟關閉訪客

PUT /api/visitor/EditEnable/92701099-7F6B-44E9-AEE9-804240C545BB

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

## DELETE Remove 移除訪客

DELETE /api/visitor/Remove

> Body Parameters

```json
{
  "MemberGUID": "3bae758d-6db7-4e46-9c94-dcfbdb29668f"
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» MemberGUID|body|string| yes |none|

> Response Examples

```json
{
  "id": "(string)通常為識別碼",
  "success": "(boolean)是否執行成功",
  "errorMessage": "(string)若執行失敗的原因說明",
  "anyMsg": "(string)若執行成功的內容補充",
  "anyObject": "(object)需要回傳的物件"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» id|string|true|none||none|
|» success|string|true|none||none|
|» errorMessage|string|true|none||none|
|» anyMsg|string|true|none||none|
|» anyObject|string|true|none||none|

## DELETE RemoveList 批次移除訪客

DELETE /api/visitor/RemoveList

> Body Parameters

```json
{
  "memberGUID": [
    "3be96078-fc98-4c6c-893e-17994a51bbe3",
    "01c8604c-9c41-4879-9004-2fc86db24650"
  ]
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» memberGUID|body|[string]| yes |none|

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

# Group

## POST QueryGroupList 檢視群組列表

POST /api/group/QueryGroupList

> Body Parameters

```json
{
  "FilterField": [
    "groupGUID"
  ],
  "FilterValue": "",
  "Sort": [],
  "PageNumber": 1,
  "PageSize": 10
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» FilterField|body|[string]| yes |none|
|» FilterValue|body|string| yes |none|
|» Sort|body|[string]| yes |none|
|» PageNumber|body|integer| yes |none|
|» PageSize|body|integer| yes |none|

> Response Examples

```json
{
  "result": [
    {
      "groupName": "(string)群組名稱",
      "groupGUID": "(string)群組識別碼",
      "status": "(number)生效日期的開關，0自訂截止日期|1永久生效",
      "startDate": "(number)起始日期，單位毫秒",
      "endDate": "(number)結束日期，單位毫秒",
      "permissionType": "(number)驗證時段的開關，0自訂時段啟用|1全時段啟用",
      "startTime": "(string)起始時間，格式00:00:00",
      "endTime": "(string)結束時間，格式00:00:00",
      "monday": "(boolean)周一啟用",
      "tuesDay": "(boolean)周二啟用",
      "wednesday": "(boolean)周三啟用",
      "thursday": "(boolean)周四啟用",
      "friday": "(boolean)周五啟用",
      "saturday": "(boolean)周六啟用",
      "sunday": "(boolean)周日啟用",
      "createTime": "(number)建立日期，單位毫秒",
      "utcOffset": "(string)時區時差，格式hh:00:00",
      "isDefault": "(number)是否屬於無法刪除的預設值，0否|1是",
      "groupPassword": "(string)自訂群組密碼，通常為4-8位純數字",
      "modifyTime": "(number)最後修改日期，單位毫秒",
      "memberCount": "(number)該群組被使用的人數",
      "memberGUID": [
        "(string)人員識別碼"
      ]
    }
  ],
  "pages": "(number)查詢結果總頁數",
  "total": "(number)查詢結果總比數",
  "input": {
    "filterField": [
      "(string)搜尋詞彙適用欄位，格式"
    ],
    "filterValue": "(string)搜尋詞彙",
    "sort": [
      {
        "field": "(string)排序欄位",
        "reverse": "(boolean)是否倒序"
      }
    ],
    "pageNumber": "(number)第幾頁",
    "pageSize": "(number)一頁幾筆"
  }
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» result|[object]|true|none||none|
|»» groupName|string|false|none||none|
|»» groupGUID|string|false|none||none|
|»» status|string|false|none||none|
|»» startDate|string|false|none||none|
|»» endDate|string|false|none||none|
|»» permissionType|string|false|none||none|
|»» startTime|string|false|none||none|
|»» endTime|string|false|none||none|
|»» monday|string|false|none||none|
|»» tuesDay|string|false|none||none|
|»» wednesday|string|false|none||none|
|»» thursday|string|false|none||none|
|»» friday|string|false|none||none|
|»» saturday|string|false|none||none|
|»» sunday|string|false|none||none|
|»» createTime|string|false|none||none|
|»» utcOffset|string|false|none||none|
|»» isDefault|string|false|none||none|
|»» groupPassword|string|false|none||none|
|»» modifyTime|string|false|none||none|
|»» memberCount|string|false|none||none|
|»» memberGUID|[string]|false|none||none|
|» pages|string|true|none||none|
|» total|string|true|none||none|
|» input|object|true|none||none|
|»» filterField|[string]|true|none||none|
|»» filterValue|string|true|none||none|
|»» sort|[object]|true|none||none|
|»»» field|string|false|none||none|
|»»» reverse|string|false|none||none|
|»» pageNumber|string|true|none||none|
|»» pageSize|string|true|none||none|

## POST QuerySinglePage 檢視群組列表(全部)

POST /api/Group/QuerySinglePage

> Body Parameters

```json
{
  "filterValue": ""
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» filterValue|body|string| yes |none|

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

## GET GetVisitorGroup 檢視訪客群組

GET /api/group/GetVisitorGroup

> Response Examples

```json
{
  "result": {
    "groupGUID": "(string)群組識別碼",
    "permissionType": "(number)驗證時段的開關，0自訂時段啟用|1全時段啟用",
    "startTime": "(string)起始時間，格式00:00:00",
    "endTime": "(string)結束時間，格式00:00:00",
    "monday": "(boolean)周一啟用",
    "tuesDay": "(boolean)周二啟用",
    "wednesday": "(boolean)周三啟用",
    "thursday": "(boolean)周四啟用",
    "friday": "(boolean)周五啟用",
    "saturday": "(boolean)周六啟用",
    "sunday": "(boolean)周日啟用",
    "utcOffset": "(string)時區時差，格式hh:00:00"
  }
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» result|object|true|none||none|
|»» groupGUID|string|true|none||none|
|»» permissionType|string|true|none||none|
|»» startTime|string|true|none||none|
|»» endTime|string|true|none||none|
|»» monday|string|true|none||none|
|»» tuesDay|string|true|none||none|
|»» wednesday|string|true|none||none|
|»» thursday|string|true|none||none|
|»» friday|string|true|none||none|
|»» saturday|string|true|none||none|
|»» sunday|string|true|none||none|
|»» utcOffset|string|true|none||none|

## POST Add 添加群組

POST /api/group/Add

> Body Parameters

```json
{
  "GroupName": "ฮีโร่ของฉัน ฮีโร่ของฉัน ฮีโร่ของฉัน",
  "permissionType": 1,
  "endDate": 1823194852752,
  "startTime": "08:30:00",
  "endTime": "18:30:00",
  "monday": true,
  "tuesday": true,
  "wednesday": true,
  "thursday": true,
  "friday": true,
  "saturday": false,
  "sunday": false,
  "status": 0,
  "groupPassword": "",
  "memberGUID": [],
  "deviceAllArea": 0,
  "deviceFilter": "67273ea7-eae6-482a-a50d-b46cf37e2682"
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» GroupName|body|string| yes |none|
|» permissionType|body|integer| yes |none|
|» endDate|body|integer| yes |none|
|» startTime|body|string| yes |none|
|» endTime|body|string| yes |none|
|» monday|body|boolean| yes |none|
|» tuesday|body|boolean| yes |none|
|» wednesday|body|boolean| yes |none|
|» thursday|body|boolean| yes |none|
|» friday|body|boolean| yes |none|
|» saturday|body|boolean| yes |none|
|» sunday|body|boolean| yes |none|
|» status|body|integer| yes |none|
|» groupPassword|body|string| yes |none|
|» memberGUID|body|[string]| yes |none|
|» deviceAllArea|body|integer| yes |none|
|» deviceFilter|body|string| yes |none|

> Response Examples

```json
{
  "id": "(string)通常為識別碼",
  "success": "(boolean)是否執行成功",
  "errorMessage": "(string)若執行失敗的原因說明",
  "anyMsg": "(string)若執行成功的內容補充",
  "anyObject": "(object)需要回傳的物件"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» id|string|true|none||none|
|» success|string|true|none||none|
|» errorMessage|string|true|none||none|
|» anyMsg|string|true|none||none|
|» anyObject|string|true|none||none|

## PUT Edit 編輯群組

PUT /api/group/Edit

> Body Parameters

```json
{
  "groupGUID": "79bf8a44-b787-47ee-8342-6075f465cac3",
  "deviceAllArea": 1,
  "deviceFilter": ""
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» groupGUID|body|string| yes |none|
|» deviceAllArea|body|integer| yes |none|
|» deviceFilter|body|string| yes |none|

> Response Examples

```json
{
  "id": "(string)通常為識別碼",
  "success": "(boolean)是否執行成功",
  "errorMessage": "(string)若執行失敗的原因說明",
  "anyMsg": "(string)若執行成功的內容補充",
  "anyObject": "(object)需要回傳的物件"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **400**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» id|string|true|none||none|
|» success|string|true|none||none|
|» errorMessage|string|true|none||none|
|» anyMsg|string|true|none||none|
|» anyObject|string|true|none||none|

## PUT EditMember 設定多群組關聯人員

PUT /api/Group/EditMember

> Body Parameters

```json
{
  "MemberList": [
    "312D673A-D215-451D-953C-195E7EF3E4B4",
    "212D673A-D215-451D-953C-195E7EF3E4B2"
  ],
  "GroupList": [
    "a991bef8-f7ce-4ab5-b5a1-653e67d7a044",
    "E8985C66-6969-439E-A3B1-9DD5D68355E0"
  ]
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» MemberList|body|[string]| yes |none|
|» GroupList|body|[string]| yes |none|

> Response Examples

```json
{
  "id": "(string)通常為識別碼",
  "success": "(boolean)是否執行成功",
  "errorMessage": "(string)若執行失敗的原因說明",
  "anyMsg": "(string)若執行成功的內容補充",
  "anyObject": "(object)需要回傳的物件"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» id|string|true|none||none|
|» success|string|true|none||none|
|» errorMessage|string|true|none||none|
|» anyMsg|string|true|none||none|
|» anyObject|string|true|none||none|

## DELETE Remove 移除群組

DELETE /api/group/Remove

> Body Parameters

```json
{
  "GroupGUID": ""
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» GroupGUID|body|string| yes |none|

> Response Examples

```json
{
  "id": "(string)通常為識別碼",
  "success": "(boolean)是否執行成功",
  "errorMessage": "(string)若執行失敗的原因說明",
  "anyMsg": "(string)若執行成功的內容補充",
  "anyObject": "(object)需要回傳的物件"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» id|string|true|none||none|
|» success|string|true|none||none|
|» errorMessage|string|true|none||none|
|» anyMsg|string|true|none||none|
|» anyObject|string|true|none||none|

## DELETE RemoveList 批次移除群組

DELETE /api/group/RemoveList

> Body Parameters

```json
{
  "GroupGUID": [
    "E8985C66-6969-439E-A3B1-9DD5D68355E0",
    "2252F95E-6D60-45A7-9CCD-441F433B8F2E",
    "2252F95E-6D60-45A7-9CCD-441F433B8F2A"
  ]
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» GroupGUID|body|[string]| yes |none|

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

# Setup/設定(平板、EzPro)

## GET GetList 檢視平板設定(列表格式)

GET /api/setup/GetList

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

## PUT EditList 批次編輯設定

PUT /api/setup/EditList

> Body Parameters

```json
[
  {
    "settingName": "SqlDestination",
    "settingChoice": "D:\\FRS_Backup"
  }
]
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|array[object]| no |none|

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

## GET GetSetting 檢視平板設定

GET /api/setup/GetSetting

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

## GET GetEzPro 檢視EZPRO

GET /api/setup/GetEzPro

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

## GET GetAI 檢視AI設定

GET /api/setup/GetAI

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

## GET GetPanel 檢視平板同步設定

GET /api/setup/GetPanel

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

## GET GetSQL 檢視資料庫備份還原設定

GET /api/setup/GetSQL

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

## GET GetExport 檢視結過拋發設定

GET /api/setup/GetExport

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

# Setup/辨識主機

## GET GetServerList 檢視辨識主機

GET /api/setup/GetServerList

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

## POST AddServer 添加辨識主機

POST /api/setup/AddServer

> Body Parameters

```json
{
  "ServerName": "測試添加",
  "ServerIP": "192.168.1.155",
  "ServerPort": "8080"
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» ServerName|body|string| yes |none|
|» ServerIP|body|string| yes |none|
|» ServerPort|body|string| yes |none|

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

## PUT EditServer 編輯辨識主機

PUT /api/setup/EditServer

> Body Parameters

```json
{
  "ServerGUID": "681929a7-8d98-4f83-a64d-cc9e94323104",
  "ServerName": "救苦救難",
  "ServerIP": "192.168.1.155",
  "ServerPort": "8080"
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» ServerGUID|body|string| yes |none|
|» ServerName|body|string| yes |none|
|» ServerIP|body|string| yes |none|
|» ServerPort|body|string| yes |none|

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

## DELETE RemoveServer 移除辨識主機

DELETE /api/setup/RemoveServer

> Body Parameters

```json
{
  "ServerGUID": "681929a7-8d98-4f83-a64d-cc9e94323104"
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» ServerGUID|body|string| yes |none|

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

# Setup/備份還原

## GET GetRestoreFiles 檢視備份時間點列表

GET /api/setup/GetRestoreFiles

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

## POST Restore 還原備份至當前資料庫

POST /api/setup/Restore/20241225_08

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

# Setup/結果拋發

## POST ExportTest 測試拋發

POST /api/setup/ExportTest

> Body Parameters

```json
"/*{\r\n    \"path\": \"D:\\\\develop\\\\臉辨資料中心\\\\frs_net6\\\\Web.Api\\\\bin\\\\Debug\\\\net6.0\\\\UploadTemp\"\r\n}*/\r\n{\r\n    \"path\": \"C:\\\\Users\\\\IoNetworks\\\\Desktop\\\\FRS_files\"\r\n}"
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» path|body|string| yes |none|

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

# Login

## POST SignIn 登入

POST /api/login/SignIn

> Body Parameters

```json
{
  "Account": "admin",
  "Password": "P@ssw0rd"
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» Account|body|string| yes |none|
|» Password|body|string| yes |none|

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

## GET VerifyToken 驗證授權

GET /api/login/VerifyToken

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

## GET GetList 檢視使用者

GET /api/login/GetList

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

## POST Add 添加使用者

POST /api/login/Add

> Body Parameters

```yaml
Account: ctetechcorp
Password: ctetechcorp
Image: string
Privilege: "1"

```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» Account|body|string| yes |帳號|
|» Password|body|string| yes |密碼|
|» Image|body|string(binary)| yes |頭像|
|» Privilege|body|string| yes |角色，最高權限0|一般權限1|

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

## PUT Edit 編輯使用者

PUT /api/login/Edit

> Body Parameters

```yaml
Account: admin
Password: P@ssw0rd
Image: string
Privilege: "1"

```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» Account|body|string| yes |帳號|
|» Password|body|string| yes |密碼|
|» Image|body|string(binary)| no |頭像|
|» Privilege|body|string| no |角色，最高權限0|一般權限1|

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

## PUT EditPassword 編輯密碼

PUT /api/login/EditPassword

> Body Parameters

```json
{
  "Account": "admin",
  "OldPassword": "P@ssw0rd123",
  "NewPassword": "P@ssw0rd"
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» Account|body|string| yes |none|
|» OldPassword|body|string| yes |none|
|» NewPassword|body|string| yes |none|

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

## DELETE Remove 移除使用者

DELETE /api/login/Remove

> Body Parameters

```json
{
  "Account": "lucas"
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» Account|body|string| yes |none|

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

# Panel

## POST QueryPanelList 檢視平板列表

POST /api/cam/panel/QueryPanelList

> Body Parameters

```json
{
  "FilterValue": "",
  "Sort": [
    {
      "Field": "IpAdress",
      "Reverse": true
    }
  ],
  "PageNumber": 1,
  "PageSize": 5
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» FilterValue|body|string| yes |none|
|» Sort|body|[object]| yes |none|
|»» Field|body|string| no |none|
|»» Reverse|body|boolean| no |none|
|» PageNumber|body|integer| yes |none|
|» PageSize|body|integer| yes |none|

> Response Examples

```json
{
  "result": [
    {
      "deviceGUID": "(guid)設備識別碼",
      "name": "(string)設備名稱",
      "deviceClass": "(0|1|2)設備類別，0一般攝影機|1熱感攝影機|2門口機",
      "ipAddress": "(string)設備IP",
      "port": "(string)設備Port",
      "lastConnectTime": "(int)最後連線時間",
      "lastSyncTime": "(int)最後同步時間",
      "createTime": "(int)創建時間",
      "utcOffset": "(string)時區時差，格式hh:00:00",
      "status": "(0|1|2|3)狀態編碼，0同步中|1正常|2斷線|3異常",
      "statusName": "(string)狀態說明"
    }
  ],
  "pages": "(number)查詢結果總頁數",
  "total": "(number)查詢結果總比數",
  "input": {
    "filterField": [
      "(string)搜尋詞彙適用欄位，格式"
    ],
    "filterValue": "(string)搜尋詞彙",
    "sort": [
      {
        "field": "(string)排序欄位",
        "reverse": "(boolean)是否倒序"
      }
    ],
    "pageNumber": "(number)第幾頁",
    "pageSize": "(number)一頁幾筆"
  }
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» result|[object]|true|none||none|
|»» deviceGUID|string|false|none||none|
|»» name|string|false|none||none|
|»» deviceClass|string|false|none||none|
|»» ipAddress|string|false|none||none|
|»» port|string|false|none||none|
|»» lastConnectTime|string|false|none||none|
|»» lastSyncTime|string|false|none||none|
|»» createTime|string|false|none||none|
|»» utcOffset|string|false|none||none|
|»» status|string|false|none||none|
|»» statusName|string|false|none||none|
|» pages|string|true|none||none|
|» total|string|true|none||none|
|» input|object|true|none||none|
|»» filterField|[string]|true|none||none|
|»» filterValue|string|true|none||none|
|»» sort|[object]|true|none||none|
|»»» field|string|false|none||none|
|»»» reverse|string|false|none||none|
|»» pageNumber|string|true|none||none|
|»» pageSize|string|true|none||none|

## POST QuerySinglePage 檢視平板列表(不分頁)

POST /api/cam/panel/QuerySinglePage

> Body Parameters

```json
{
  "filterValue": ""
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» filterValue|body|string| yes |none|

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

## POST DetectIp 偵測可連線設備

POST /api/cam/panel/DetectIp

> Body Parameters

```json
{
  "ip": "192.168.1.112",
  "ip2": ""
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» ip|body|string| yes |none|
|» ip2|body|string| yes |none|

> Response Examples

```json
{
  "id": "(string)通常為識別碼",
  "success": "(boolean)是否執行成功",
  "errorMessage": "(string)若執行失敗的原因說明",
  "anyMsg": "(string)若執行成功的內容補充",
  "anyObject": [
    {
      "deviceGUID": "(string)設備識別碼，平板提供",
      "deviceName": "(string)設備名稱，預設可隨意調整",
      "ip": "(string)設備IP",
      "port": "(string)設備Port",
      "syncMode": "(0|1)模式選擇，0為要求平板將資料拋給後台同步，1為要求平板清空資料；最後都會從後台索取資料"
    }
  ]
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» id|string|true|none||none|
|» success|string|true|none||none|
|» errorMessage|string|true|none||none|
|» anyMsg|string|true|none||none|
|» anyObject|[object]|true|none||none|
|»» deviceGUID|string|false|none||none|
|»» deviceName|string|false|none||none|
|»» ip|string|false|none||none|
|»» port|string|false|none||none|
|»» syncMode|string|false|none||none|

## POST AddPanel 添加設備

POST /api/cam/panel/AddPanel

> Body Parameters

```json
{
  "deviceGUID": "1d52d4ba-3759-4089-948d-8c123bcf1fef",
  "deviceName": "Panel_TEST",
  "ip": "192.168.1.112",
  "port": "8080",
  "syncMode": 1
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» deviceGUID|body|string| yes |none|
|» deviceName|body|string| yes |none|
|» ip|body|string| yes |none|
|» port|body|string| yes |none|
|» syncMode|body|integer| yes |none|

> Response Examples

```json
{
  "id": "(string)通常為識別碼",
  "success": "(boolean)是否執行成功",
  "errorMessage": "(string)若執行失敗的原因說明",
  "anyMsg": "(string)若執行成功的內容補充",
  "anyObject": "(object)需要回傳的物件"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» id|string|true|none||none|
|» success|string|true|none||none|
|» errorMessage|string|true|none||none|
|» anyMsg|string|true|none||none|
|» anyObject|string|true|none||none|

## POST AddPanelList 批次添加設備

POST /api/cam/panel/AddPanelList

> Body Parameters

```json
[
  {
    "DeviceGUID": "BB68843E-9A83-46E8-9884-F7F53B1E2E90",
    "DeviceName": "門口機",
    "IP": "192.168.1.85",
    "Port": "7021",
    "syncMode": 1
  }
]
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|array[object]| no |none|

> Response Examples

```json
{
  "id": "(string)通常為識別碼",
  "success": "(boolean)是否執行成功",
  "errorMessage": "(string)若執行失敗的原因說明",
  "anyMsg": "(string)若執行成功的內容補充",
  "anyObject": {
    "inputCount": "(int)匯入設備數量"
  }
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» id|string|true|none||none|
|» success|string|true|none||none|
|» errorMessage|string|true|none||none|
|» anyMsg|string|true|none||none|
|» anyObject|object|true|none||none|
|»» inputCount|string|true|none||none|

## POST AddPanelInit 新增初次同步任務

POST /api/cam/panel/AddPanelInit

> Body Parameters

```json
{
  "DeviceGUID": "31a2d8b9-c9f2-44b3-b3a0-2615f8d32faa"
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» DeviceGUID|body|string| yes |none|

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

## PUT EditPanel 編輯設備

PUT /api/cam/panel/EditPanel

> Body Parameters

```json
{
  "DeviceGUID": "BB68843E-9A83-46E8-9884-F7F53B1E2E90",
  "DeviceName": "DOOR-2"
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» DeviceGUID|body|string| yes |none|
|» DeviceName|body|string| yes |none|

> Response Examples

```json
{
  "id": "(string)通常為識別碼",
  "success": "(boolean)是否執行成功",
  "errorMessage": "(string)若執行失敗的原因說明",
  "anyMsg": "(string)若執行成功的內容補充",
  "anyObject": "(object)需要回傳的物件"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» id|string|true|none||none|
|» success|string|true|none||none|
|» errorMessage|string|true|none||none|
|» anyMsg|string|true|none||none|
|» anyObject|string|true|none||none|

## DELETE RemovePanel 移除設備

DELETE /api/cam/panel/RemovePanel

> Body Parameters

```json
{
  "DeviceGUID": "6a3e97f6-3ee5-4ebb-9ff4-d08796ab3fcf"
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» DeviceGUID|body|string| yes |none|

> Response Examples

```json
{
  "id": "(string)通常為識別碼",
  "success": "(boolean)是否執行成功",
  "errorMessage": "(string)若執行失敗的原因說明",
  "anyMsg": "(string)若執行成功的內容補充",
  "anyObject": "(object)需要回傳的物件"
}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

HTTP Status Code **200**

|Name|Type|Required|Restrictions|Title|description|
|---|---|---|---|---|---|
|» id|string|true|none||none|
|» success|string|true|none||none|
|» errorMessage|string|true|none||none|
|» anyMsg|string|true|none||none|
|» anyObject|string|true|none||none|

## DELETE RemovePanelList 批次移除設備

DELETE /api/cam/panel/RemovePanelList

> Body Parameters

```json
{
  "DeviceGUID": [
    "BB68843E-9A83-46E8-9884-F7F53B1E2E90",
    "BB68843E-9A83-46E8-9884-F7F53B1E2E90"
  ]
}
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» DeviceGUID|body|[string]| yes |none|

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

# System 測試區塊

## GET TestHttpStatus 確認後台服務啟用

GET /api/system/TestHttpStatus

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|status|query|array[string]| no |none|

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

## GET [X]GetAccounts 取得帳戶列表

GET /api/system/GetAccounts

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

## POST ImportImageToBase64 確認圖片轉base64的字串內容

POST /api/system/ImportImageToBase64

> Body Parameters

```yaml
file: string
Description: "123"

```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» file|body|string(binary)| yes |none|
|» Description|body|string| yes |none|

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

## PUT Base64ToImage 確認base64字串轉圖片

PUT /api/system/Base64ToImage

> Body Parameters

```json
"{\r\n    \"base64\": \"/9j/4AAQSkZJRgABAQAASABIAAD/.../Z\" /* 手動省略超長一串 */\r\n}"
```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|base64|query|string| no |none|
|body|body|object| no |none|
|» base64|body|string| yes |none|

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

## GET TestTime 確認輸入時間與系統時間

GET /api/system/TestTime

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|timeValue|query|string| yes |本地區的時間|

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

## GET TestEzPro 確認EzPro的紀錄功能

GET /api/system/TestEzPro

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|source|query|string| yes |FR[平板提供的GUID]|
|caption|query|string| yes |none|
|description|query|string| yes |none|

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

## GET TestTrigger 測試平板的API

GET /api/system/TestTrigger

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|name|query|string| yes |none|
|para|query|string| yes |none|

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

## GET TestStart 測試平板的API

GET /api/system/TestStart

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|deviceGuid|query|string| yes |none|
|ip|query|string| yes |none|
|port|query|string| yes |none|
|syncMode|query|string| yes |none|

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

## GET TestDisconnect 測試平板的API

GET /api/system/TestDisconnect

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|deviceGuid|query|string| yes |none|
|ip|query|string| yes |none|
|port|query|string| yes |none|

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

## GET TestStatus 測試平板的API

GET /api/system/TestStatus

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|ip|query|string| yes |none|
|port|query|string| yes |none|

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

## GET TestMonitorCount 監控背景服務

GET /api/system/TestMonitorCount

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

## GET TestMonitorList 查看佇列內容

GET /api/system/TestMonitorList

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|selected|query|string| yes |通知佇列資料|

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

## POST TestAiAndFace 測試AI解析圖片與相似度

POST /api/system/TestAiAndFace

> Body Parameters

```yaml
Description: "123"
File: []

```

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|body|body|object| no |none|
|» Description|body|string| yes |none|
|» File|body|string(binary)| yes |none|

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

## GET TestPauseAndResume 更改通知佇列狀態(調整後仍會被背景排程更正)

GET /api/system/TestPauseAndResume

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

## GET GetApiLog 查看LOG紀錄

GET /api/system/GetApiLog

### Params

|Name|Location|Type|Required|Description|
|---|---|---|---|---|
|word|query|string| yes |none|

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

## GET GetRemoteIp 查看Request夾帶的IP資訊

GET /api/system/GetRemoteIp

> Response Examples

> 200 Response

```json
{}
```

### Responses

|HTTP Status Code |Meaning|Description|Data schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|none|Inline|

### Responses Data Schema

# Data Schema

