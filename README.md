# Quantforce API

![](http://www.quantforce.net/wp-content/uploads/2016/12/logo.png)

Quantforce is a solution to build and use predictive model

### _This is primarily documentation_

## What is QuantForce?

QuantForce is all the tools you need to create a predictive model from your data.

See QuantForce web site for more infos

[/www.quantforce.net](/www.quantforce.net)

## Servers

You can use QuantFroce servers. You can also ask for a on premises version to be sure your data doesn't get out from your company \(Windows Server\).

## Hierarchy

The concept is quite simple.

From your account you can create as many child account as you want. This way you can organise like you do with your customer. If a customer have a customer you can handle it.

From an account you can create as many project as you want. A project represents a full data workflow.

From a project you can create as many node as you want. A node can do operation on data.

![](http://www.quantforce.net/wp-content/uploads/2017/01/API-Big-Picture.png)

## How to call Quantforce API

Every call to Quantforce API requires a subscription key. This key needs to be either passed through the request header.

You'll find the subscription key in you user account details.

Passing the subscription key in the HTTP request header:

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



