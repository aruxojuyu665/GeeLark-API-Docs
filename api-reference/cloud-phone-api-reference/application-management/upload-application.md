# Upload Application

> API Reference > Cloud Phone API Reference > Application Management > Upload Application

**Source:** [https://doc.geelark.com/web/#/602813392/101527967](https://doc.geelark.com/web/#/602813392/101527967)

---

## API Description
Upload Application

## Request URL

- `https://openapi.geelark.com/open/v1/app/upload`

## Request Method

- POST

## Request Parameters

| Parameter | Required | Type | Description | Example |
| --- | --- | --- | --- | --- |
| fileUrl | Yes | string | Application installation file link (supports apk, xapk only) | [https://material.geelark.cn/user-upload/495622401615203830/apk/uCeztwvXpswsHPH5WFht.apk](https://material.geelark.cn/user-upload/495622401615203830/apk/uCeztwvXpswsHPH5WFht.apk) |
| desc | No | string | Remarks | Application description |

## Request Example

```json
{
    "fileUrl" : "https://material.geelark.cn/user-upload/495622401615203830/apk/uCeztwvXpswsHPH5WFht.apk",
    "desc" : "app description"
}

```

## Response Data Description

| Parameter | Type | Description |
| --- | --- | --- |
| taskId | string | Task ID for querying upload status |

## Response Example

```json
{
    "traceId": "B82825D58F85FB31B755BD6CA32A30A9",
    "code": 0,
    "msg": "success",
    "data": {
        "taskId": "1830906144634757120"
    }
}

```

## Error Codes
Please refer to [API Call Documentation](https://showdoc.geelark.com/web/#/602813392/101527834).