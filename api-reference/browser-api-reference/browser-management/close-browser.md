# Close browser

> API Reference > Browser API Reference > Browser Management > Close browser

**Source:** [https://doc.geelark.com/web/#/602813392/101528634](https://doc.geelark.com/web/#/602813392/101528634)

---

## Interface Description
Used to close the corresponding browser. You need to specify the environment ID.

## Request URL

- `http://localhost:40185/api/v1/browser/stop`

## Request method

- POST

## Request Parameters

| Parameter Name | Required | Type | Description | Example |
| --- | --- | --- | --- | --- |
| id | Yes | string | browser id | 539893235657500146 |

## Request Example

```json
{
 "id": "539893235657500146"
}

```

## Example response

```json
{
    "traceId": "123456ABCDEF",
    "code": 0,
    "msg": "success"
}

```

## Error Code
Below are specific error codes for this interface. For other error codes, please refer to [API Documentation](https://showdoc.geelark.com/web/#/602813392/101528628).

| Error Code | Description |
| --- | --- |
| -1 | Shutdown failed |
| 43028 | The sub-user does not have permissions for this environment group |