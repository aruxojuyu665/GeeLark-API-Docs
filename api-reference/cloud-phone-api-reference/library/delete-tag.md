# delete tag

> API Reference > Cloud Phone API Reference > Library > delete tag

**Source:** [https://doc.geelark.com/web/#/602813392/101528429](https://doc.geelark.com/web/#/602813392/101528429)

---

## Interface Description
delete material tag

## Request URL

- `https://openapi.geelark.cn/open/v1/material/tag/del`

## Request Method

- POST

## Request Parameters

| Parameter Name | Required | Type | Description | Example |
| --- | --- | --- | --- | --- |
| ids | Yes | array[string] | tag id | Refer to Request Example |

## Request Example

```json
{
    "ids" : ["570461738663674391"]
}

```

## Response Example

```json
{
  "traceId": "ACEB0CFEB887F99CB989BC9D9FF92BBC",
  "code": 0,
  "msg": "success",
  "data": {
    "totalAmount": 2,
    "successAmount": 1,
    "failAmount": 1,
    "failDetails": [
      {
        "code": 43022,
        "id": "528953724308030464",
        "msg": "tag not found"
      }
    ]
  }
}

```

## Response Data Description

| Parameter Name | Type | Description |
| --- | --- | --- |
| totalAmount | integer | Total delete requests |
| successAmount | integer | Total successes |
| failAmount | integer | Total failures |
| failDetails | array[FailDetails] | Failure details |

### Failure Details 

| Parameter Name | Type | Description |
| --- | --- | --- |
| code | integer | Error code |
| id | string | Tag ID |
| msg | string | Error msg |

## Error Codes
Below are specific error codes for the API. For other error codes, please refer to [API Call Description](https://showdoc.geelark.com/web/#/602813392/101527834).

| Error Code | Description |
| --- | --- |
| 43022 | tag not found |