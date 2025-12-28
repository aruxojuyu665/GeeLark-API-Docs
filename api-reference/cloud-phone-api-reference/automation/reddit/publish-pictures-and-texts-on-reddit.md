# Publish pictures and texts on Reddit

> API Reference > Cloud Phone API Reference > Automation > Reddit > Publish pictures and texts on Reddit

**Source:** [https://doc.geelark.com/web/#/602813392/101528462](https://doc.geelark.com/web/#/602813392/101528462)

---

## Request URL

- `https://openapi.geelark.com/open/v1/rpa/task/redditImage`

## Request Method

- POST

## Request Parameters

| Parameter | Required | Type | Description |
| --- | --- | --- | --- |
| name | No | string | Task name, up to 128 characters |
| remark | No | string | Remarks, up to 200 characters |
| scheduleAt | Yes | int | Scheduled time (timestamp) |
| id | Yes | string | Cloud phone ID |
| title | Yes | string | Title |
| description | No | string | Description |
| images | Yes | []string | Images, refer to the User Guide - File Upload for creating automation tasks |
| community | Yes | string | Community |

## Request Example

```json
{
 "name":"test",
 "remark":"test remark",
 "scheduleAt": 1741846843,
 "id":"557536075321468390",
 "title": "title",
 "description":"description",
 "images": ["https://material.geelark.com/a.jpg"],
 "community": "cat"
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