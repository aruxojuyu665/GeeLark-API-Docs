# Publish pictures and texts on Threads

> API Reference > Cloud Phone API Reference > Automation > Threads > Publish pictures and texts on Threads

**Source:** [https://doc.geelark.com/web/#/602813392/101528655](https://doc.geelark.com/web/#/602813392/101528655)

---

## Request URL

- `https://openapi.geelark.com/open/v1/rpa/task/threadsImage`

## Request Method

- POST

## Request Parameters

| Parameter | Required | Type | Description |
| --- | --- | --- | --- |
| name | No | string | Task name, up to 128 characters |
| remark | No | string | Remarks, up to 200 characters |
| scheduleAt | Yes | int | Scheduled time (timestamp) |
| id | Yes | string | Cloud phone ID |
| topic | No | string | Topic |
| title | Yes | string | Title. Maximum 500 characters |
| images | Yes | []string | Images, refer to the User Guide - File Upload for creating automation tasks |

## Request Example

```json
{
 "name":"test",
 "remark":"test remark",
 "scheduleAt": 1741846843,
 "id":"557536075321468390",
 "title": "title",
 "images": ["https://material.geelark.com/a.jpg"]
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