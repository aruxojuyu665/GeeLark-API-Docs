# Set Phone Logo / Brand

> API Reference > Cloud Phone API Reference > OEM > Set Phone Logo / Brand

**Source:** [https://doc.geelark.com/web/#/602813392/101528564](https://doc.geelark.com/web/#/602813392/101528564)

---

## Interface Description
Once you’ve made an API request, you can set a brand name and logo in the top-left corner of the cloud phone, and the logo within the sidebar’s QR code.(To get access to this feature, please contact dominic@geelark.com for permission.)

## Request URL

- `https://openapi.geelark.com/open/v1/phone/customization`

## Request Method

- POST

## Request Parameters

| Parameter Name | Required | Type | Description | Example |
| --- | --- | --- | --- | --- |
| title | No | string | title | Refer to Request Example |
| logo | No | string | logo url | Refer to Request Example |
| hideHeader | No | bool | whether hide the header on the top of the cloud phone | false |

## Request Example

```json
{
    "title" : "GeeLark",
    "logo" : "https://material.geelark.cn/user-upload/banner0903_cn.jpg",
    "hideHeader" : false
}

```

## Response Example

```json
{
    "traceId": "ADD9A7489BB2198DBC0FB37082684CB0",
    "code": 0,
    "msg": "success"
}

```

## Error Codes
Below are the specific error codes for this interface. For other error codes, please refer to the [API Call Instructions](https://showdoc.geelark.cn/web/#/602813388/101527801).

| Error Code | Description |
| --- | --- |
| 40015 | Permission limit |
| 60003 | Illegal url，please upload temporary files to GeeLark and get the url |
| 60004 | Invalid file format |