# Set Team App Authorization

> API Reference > Cloud Phone API Reference > Application Management > Set Team App Authorization

**Source:** [https://doc.geelark.com/web/#/602813392/101528691](https://doc.geelark.com/web/#/602813392/101528691)

---

## API Description
Grant team application permissions, including all permissions such as location permissions, which only apply to newly installed applications.

## Request URL

- `https://openapi.geelark.com/open/v1/app/auth/status`

## Request Method

- POST

## Request Parameters

| Parameter Name | Required | Type | Description | Example |
| --- | --- | --- | --- | --- |
| id | Yes | string | Team application ID | 497652752864775437 |
| appAuth | Yes | integer | App authorization 0 disables authorization; 1 enables authorization | 1 |

## Request Example

```json
{
 "id": "497652752864775437",
 "appAuth": 1
}

```

## Response Example

```json
{
 "traceId": "886A92FCBE9B7A52A7F583FCBD2BF6A8",
 "code": 0,
 "msg": "success"
}

```

## Error Codes
Please refer to [API Call Description](https://showdoc.geelark.com/web/#/602813392/101527834).