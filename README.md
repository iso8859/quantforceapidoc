# Quantforce API

![](http://www.quantforce.net/wp-content/uploads/2016/12/logo.png)

Quantforce is a solution to build and use predictive model

### _This is primarily documentation_

# Servers

You can use QuantFroce servers. You can also ask for a on premises version to be sure your data doesn't get out from your company \(Windows Server\).

## Hierarchy

The concept is quite simple.

From your account you can create as many qfAccount as you want. A qfAccount represent your customer account.

From a qfAccount you can create as many project as you want. A project represent a full data workflow.

From a project you can create as many node as you want. A node can do a operation on data.

![](http://www.quantforce.net/wp-content/uploads/2017/01/API-Big-Picture.png)

## How to call Quantforce API

Every call to Quantforce API requires a subscription key. This key needs to be either passed through a query string parameter or specified in the request header.

You'll find the subscription key in you user account details.

**1.**Passing the subscription key through a query string, see below as a Computer Vision API example:

`https://api.quantforce.net/api/v1.0/qfaccount?subscription-key=<Your subscription key>`

**2.**Passing the subscription key can also be specified in the HTTP request header:

`subscription-key: <Your subscription key>`

Content type could be json or XML. You set it using the header

```
Content-Type: application/json
```

or

```asciidoc
Content-Type: application/xml
```

For example

```asciidoc
GET /api/Accoount
HEADER
Accept: application/xml
subscription-key: KRJQ8-RQ822-YRMXF-6TTXC-HD2VM

ANSWER Body

<AccountModel xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
  <_id>1</_id>
  <mail>info@quantforce.net</mail>
  <subscriptionKey>KRJQ8-RQ822-YRMXF-6TTXC-HD2VM</subscriptionKey>
</AccountModel>
```

```
GET /api/Accoount
HEADER
Accept: application/json
subscription-key: KRJQ8-RQ822-YRMXF-6TTXC-HD2VM

ANSWER body

{
  "_id": 1,
  "mail": "info@quantforce.net",
  "subscriptionKey": "KRJQ8-RQ822-YRMXF-6TTXC-HD2VM"
}
```



