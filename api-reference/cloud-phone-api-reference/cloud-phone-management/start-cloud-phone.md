# Start cloud phone

> API Reference > Cloud Phone API Reference > Cloud Phone Management > Start cloud phone

**Source:** [https://doc.geelark.com/web/#/602813392/101527840](https://doc.geelark.com/web/#/602813392/101527840)

---

## API Description
Batch start cloud phones.

## Request URL

- `https://openapi.geelark.com/open/v1/phone/start`

## Request Method

- POST

## Request Parameters

| Parameter Name | Required | Type | Description | Example |
| --- | --- | --- | --- | --- |
| ids | Yes | array[string] | List of cloud phone IDs | See request example |
| hideSideBar | No | bool | Whether to hide the sidebar | false, defaults to false if not provided |
| displayTimer | No | bool | Whether to display the timer | false, defaults to false if not provided |
| width | No | int | Cloud phone display width in px | Default: 336 (allowed range: 200<=width<=600) |
| center | No | int | Whether the cloud phone display is centered | 0: not centered, 1: centered; default is 1 if not provided |
| hideLibrary | No | bool | Whether to display the cloud phone Asset Library (Material Center) | true: do not display; false: display; default is false if not provided |
| hideMirror | No | bool | Whether to display the cloud phone mirror | true: do not display; false: display; default is false if not provided |

## Request Example

```json
{
    "ids":[
        "123456ABCDEF",
        "123456ABCDEF",
        "123456ABCDEF",
        "123456ABCDEF"
    ]
}

```

## Response Example

```json
{
 "code": 0,
 "msg": "success",
 "traceId": "12345678ABCDEF",
 "data": {
 "totalAmount": 3,
 "successAmount": 1,
 "failAmount": 2,
 "failDetails": [
 {
 "code": 43004,
 "id": "12345678ABCDEFG",
 "msg": "env is expired"
 },
 {
 "code": 42001,
 "id": "12345678ABCDEFG",
 "msg": "env not found"
 }
 ],
 "successDetails": [
 {
 "id": "12345678ABCDEFG",
 "url": "https://speedup.geelark.com/phone-api",
 "chargingMethod": "Per-minute usage"
 }
 ]
 }
}

```

## Response Data Description

| Parameter Name | Type | Description |
| --- | --- | --- |
| totalAmount | integer | Total number of requested IDs |
| successAmount | integer | Number of successful starts |
| successDetails | array[SuccessDetails] | Information about successed |
| failAmount | integer | Number of failed starts |
| failDetails | array[FailDetails] | Information about failures |

### SuccessDetails Successed Information

| Parameter Name | Type | Description |
| --- | --- | --- |
| id | string | ID of the cloud phone |
| url | string | remote url |
| chargingMethod | string | Billing type, Per-minute usage, Monthly rental, Parallels |

### FailDetails Failure Information

| Parameter Name | Type | Description |
| --- | --- | --- |
| code | integer | Failure code |
| id | string | ID of the failed cloud phone |
| msg | string | Failure message |

## Error Codes
Below are specific error codes for this interface. For other error codes, please refer to [API Documentation](https://showdoc.geelark.com/web/#/602813392/101527834).

| Error Code | Description |
| --- | --- |
| 42001 | Cloud phone does not exist |
| 43004 | Cloud phone has expired |
| 47004 | Device associated with cloud phone does not exist |
| 43007 | Cloud phone is already in use by another user |
| 45002 | Cloud phone proxy is unavailable |
| 47002 | Cloud phone resources are insufficient |
| 43020 | Cloud phone is currently unavailable, please try again later |
| 43029 | The selected cloud phone model is under maintenance, please try again later |