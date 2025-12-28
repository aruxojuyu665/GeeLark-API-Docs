# Modify tag

> API Reference > Tag Management > Modify tag

**Source:** [https://doc.geelark.com/web/#/602813392/101527939](https://doc.geelark.com/web/#/602813392/101527939)

---

## Interface Description

- Modify tag information including name and color.
**Refer to the [Create Tag](https://showdoc.geelark.cn/web/#/602813392/101527936) for the list of tag colors.**

## Request URL

- `https://openapi.geelark.com/open/v1/tag/update`

## Request Method

- POST

## Request Parameters

| Parameter Name | Required | Type | Description | Example |
| --- | --- | --- | --- | --- |
| list | Yes | array[Tag] | Array of tags to update | Refer to Request Example |

### list Modify Tag Array 

| Parameter Name | Required | Type | Description | Example |
| --- | --- | --- | --- | --- |
| id | Yes | string | Tag ID | Refer to Request Example |
| name | No | string | New tag name, up to 30 characters | Refer to Request Example |
| color | No | string | New tag color | Refer to Request Example |

- If the tag information includes a name, it cannot be an empty string.

## Request Example

```json
{
  "list": [
    {
      "id": "528989565894198272",
      "name": "tagEmptyUpdate",
      "color": "red"
    },
    {
      "id": "528994200482481152",
      "name": "tagUpdate",
      "color": "red"
    }
  ]
}

```

## Response Example

```json
{
  "traceId": "B178151A9586E88195C4BF1493BBC98B",
  "code": 0,
  "msg": "success",
  "data": {
    "totalAmount": 2,
    "successAmount": 2,
    "failAmount": 0
  }
}

```

## Error Codes
Below are the specific error codes for this interface. For other error codes, please refer to the [API Call Instructions](https://showdoc.geelark.cn/web/#/602813388/101527801).

| Error Code | Description |
| --- | --- |
| 43020 | Tag name is empty |
| 43022 | Tag does not exist |
| 43023 | Tag color not supported |