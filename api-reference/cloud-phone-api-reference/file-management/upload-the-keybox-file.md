# Upload the keybox file

> API Reference > Cloud Phone API Reference > File Management > Upload the keybox file

**Source:** [https://doc.geelark.com/web/#/602813392/101528555](https://doc.geelark.com/web/#/602813392/101528555)

---

## API Description
Upload the keybox file and pass Google’s integrity verification. This is currently only supported on Android 12/13/15. For Android 12/13, simply upload the keybox file. Android 15 requires the following additional steps:

- Update Google Play and GMS to the latest version.- Log in with a valid Google account.- Download the Play Integrity API Checker from Google Play.

## Request URL

- `https://openapi.geelark.com/open/v1/phone/keyboxUpload`

## Request Method

- POST

## Request Parameters

| Parameter Name | Required | Type | Description | Example |
| --- | --- | --- | --- | --- |
| id | Yes | string | Cloud phone ID | Refer to request example |
| fileUrl | Yes | string | File URL | Refer to request example |

## Request Example

```json
{
    "id": "528715748189668352",
    "fileUrl":"https://material.geelark.cn/client-img/oakendn.xml"
}

```

## Response Example

```json
{
    "traceId": "A62BBBF3A294487F9B49B9FFA0F84CA8",
    "code": 0,
    "msg": "success",
    "data": {
        "taskId": "1850726441252569088"
    }
}

```

## Response Data Description

| Parameter Name | Type | Description |
| --- | --- | --- |
| taskId | string | Task ID |

## Error Codes
The following are specific error codes for this API. For other error codes, please refer to [API Call Description](https://showdoc.geelark.com/web/#/602813392/101527834).

| Error Code | Description |
| --- | --- |
| 42001 | Cloud phone does not exist |
| 42002 | Cloud phone is not running |
| 43026 | Cloud phone system not support |
| 60003 | Invalid file url |

## Callback Result and Example
Please refer to [Callback Example](https://showdoc.geelark.com/web/#/602813392/101527975).