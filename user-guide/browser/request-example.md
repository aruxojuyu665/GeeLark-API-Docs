# Request example

> User Guide > Browser > Request example

**Source:** [https://doc.geelark.com/web/#/602813392/101528612](https://doc.geelark.com/web/#/602813392/101528612)

---

## Example

```
const url = "http://localhost:40185/api/v1/browser/start"; // Sample request address

var data = {
 "id": "123456789xxxx"
};

fetch(url, {
 method: "POST",
 headers: {
 "Content-Type": "application/json",
 },
 body: JSON.stringify(data),
})
 .then((res) => res.json())
 .then((res) => {
 console.log(res);
 })
 .catch((err) => {
 console.error(err);
 });

```