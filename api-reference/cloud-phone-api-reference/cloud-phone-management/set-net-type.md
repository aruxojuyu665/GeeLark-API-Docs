# Set net type

> API Reference > Cloud Phone API Reference > Cloud Phone Management > Set net type

**Source:** [https://doc.geelark.com/web/#/602813392/101528562](https://doc.geelark.com/web/#/602813392/101528562)

---

## API Description
Set up the cloud phone network connection mode

## Request URL

- `https://openapi.geelark.com/open/v1/phone/net/set`

## Request Method

- POST

## Request Parameters

| Parameter Name | Required | Type | Description |
| --- | --- | --- | --- |
| id | Yes | string | Cloud Phone ID |
| netType | Yes | integer | Networking. 0-Wi-Fi, 1-Mobile. Only supported on Android 12/Android 13/Android 15 |

## Request Example

```json
{
  "id": "528086284158239744",
  "netType": 0
}

```

## Response Example

```json
{
  "traceId": "B04B0843BD86D9589AB3BAB6A9EA3D92",
  "code": 0,
  "msg": "success"
}

```

## Error Codes
For error codes, please refer to [API Call Description](https://open.geelark.com/web/#/602813392/101527834).

| Error Code | Description |
| --- | --- |
| 42001 | cloud phone not found |