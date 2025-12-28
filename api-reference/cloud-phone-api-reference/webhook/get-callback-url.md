# Get callback url

> API Reference > Cloud Phone API Reference > Webhook > Get callback url

**Source:** [https://doc.geelark.com/web/#/602813392/101527974](https://doc.geelark.com/web/#/602813392/101527974)

---

## Interface Description
Retrieve the callback interface URL set by the user.

## Request URL

- `https://openapi.geelark.com/open/v1/callback/get`

## Request Method

- POST

## Response Example

```json
{
    "traceId": "9CEA6CC9B5BB68BBAE4ABDF9BE5AC89D",
    "code": 0,
    "msg": "success",
    "data": {
        "url": "http://example.geelark.com/phone/callback/test"
    }
}

```

## Response Body Data Description

| Parameter Name | Type | Description |
| --- | --- | --- |
| url | string | The set callback URL |

## Error Codes
Below are the specific error codes for this interface. For other error codes, please refer to the [API Call Instructions](https://showdoc.geelark.com/web/#/602813388/101527801).

| Error Code | Description |
| --- | --- |
| 51001 | Callback URL not set |