# Remove Team Apps

> API Reference > Cloud Phone API Reference > Application Management > Remove Team Apps

**Source:** [https://doc.geelark.com/web/#/602813392/101528689](https://doc.geelark.com/web/#/602813392/101528689)

---

## API Description
Remove the application from the team applications.

## Request URL

- `https://openapi.geelark.com/open/v1/app/remove`

## Request Method

- POST

## Request Parameters

| Parameter Name | Required | Type | Description | Example |
| --- | --- | --- | --- | --- |
| id | Yes | string | Team application ID | 497652752864775437 |

## Request Example

```json
{
 "id": "497652752864775437"
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