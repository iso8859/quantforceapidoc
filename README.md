# Quantforce API

![](http://www.quantforce.net/wp-content/uploads/2016/12/logo.png)

Quantforce is a solution to build and use predictive model

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

```
Content-Type: application/XML
```

## Hierarchy

The concept is quite simple.

From your account you can create as many qfAccount as you want. A qfAccount represent your customer account.

From a qfAccount you can create as many project as you want. A project represent a full data workflow.

From a project you can create as many node as you want. A node can do a operation on data.





