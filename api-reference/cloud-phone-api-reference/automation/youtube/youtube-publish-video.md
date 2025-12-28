# YouTube publish Video

> API Reference > Cloud Phone API Reference > Automation > YouTube > YouTube publish Video

**Source:** [https://doc.geelark.com/web/#/602813392/101528381](https://doc.geelark.com/web/#/602813392/101528381)

---

## Request URL

- `https://openapi.geelark.com/open/v1/rpa/task/youtubePubVideo`

## Request Method

- POST

## Request Parameters

| Parameter | Required | Type | Description |
| --- | --- | --- | --- |
| name | No | string | Task name, up to 128 characters |
| remark | No | string | Remarks, up to 200 characters |
| scheduleAt | Yes | int | Scheduled time (timestamp) |
| id | Yes | string | Cloud phone ID |
| title | Yes | string | Title, up to 100 characters |
| description | Yes | string | Description, up to 5000 characters |
| video | Yes | string | Video, refer to the User Guide - File Upload for creating automation tasks |

## Request Example

```json
{
 "name":"test",
 "remark":"test remark",
 "scheduleAt": 1741846843,
 "id":"557536075321468390",
 "title":"title",
 "description":"description",
 "video": "https://material.geelark.com/a.mp4"
}

```

## Response Example

```json
{
    "traceId": "A4D8BCF69B878A71AC589F5CB1D80EAB",
    "code": 0,
    "msg": "success",
    "data": {
        "taskId": "558017255909123564"
    }
}

```