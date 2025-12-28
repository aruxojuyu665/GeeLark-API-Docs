# Set GPS

> API Reference > Cloud Phone API Reference > Cloud Phone Management > Set GPS

**Source:** [https://doc.geelark.com/web/#/602813392/101527934](https://doc.geelark.com/web/#/602813392/101527934)

---

## Interface Description

- Set/update the GPS information of cloud phones, including longitude and latitude.- Longitude range: `[-180.0, 180.0]`- Latitude range: `[-90.0, 90.0]`

## Request URL

- `https://openapi.geelark.com/open/v1/phone/gps/set`

## Request Method

- POST

## Request Parameters

| Parameter Name | Required | Type | Description | Example |
| --- | --- | --- | --- | --- |
| list | Yes | array[GPS] | Cloud phone GPS info | Refer to Request Example |

### list Cloud Phone GPS Info 

| Parameter Name | Required | Type | Description | Example |
| --- | --- | --- | --- | --- |
| id | Yes | string | Cloud phone ID | Refer to Request Example |
| longitude | Yes | float | Longitude | Refer to Request Example |
| latitude | Yes | float | Latitude | Refer to Request Example |

## Request Example

```json
{
    "list": [
        {
            "id": "528086321789535232",
            "latitude": 1.30243,
            "longitude": 103.87546
        },
        {
            "id": "530011895768286208",
            "latitude": 11.30243,
            "longitude": 104.87546
        }
    ]
}

```

## Response Example

```json
{
    "traceId": "870AE3259C965B45A0D09C92A4EA8F81",
    "code": 0,
    "msg": "success",
    "data": {
        "totalAmount": 2,
        "successAmount": 2,
        "failAmount": 0
    }
}

```

### Response Data Description

| Parameter Name | Type | Description |
| --- | --- | --- |
| totalAmount | integer | Total number of requested IDs |
| successAmount | integer | Total number of successful requests |
| failAmount | integer | Total number of failed requests |

## Error Codes
Below are the specific error codes for this interface. For other error codes, please refer to the [API Call Instructions](https://showdoc.geelark.com/web/#/602813388/101527801).

| Error Code | Description |
| --- | --- |
| 42001 | Cloud phone does not exist |
| 43012 | Latitude/longitude range error |