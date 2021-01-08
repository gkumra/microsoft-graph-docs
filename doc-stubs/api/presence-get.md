---
title: "Get presence"
description: "Read the properties and relationships of a presence object."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Get presence
Namespace: microsoft.graph

Read the properties and relationships of a [presence](../resources/presence.md) object.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from most to least privileged)|
|:---|:---|
|Delegated (work or school account)|**TODO: Provide applicable permissions.**|
|Delegated (personal Microsoft account)|**TODO: Provide applicable permissions.**|
|Application|**TODO: Provide applicable permissions.**|

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /me/presence
GET /users/{usersId}/presence
GET /communications/presences/{presenceId}
```

## Optional query parameters
This method supports some of the OData query parameters to help customize the response. For general information, see [OData query parameters](/graph/query-parameters).

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body
Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a [presence](../resources/presence.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "get_presence"
}
-->
``` http
GET https://graph.microsoft.com/beta/me/presence
```


### Response
**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.presence"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": {
    "@odata.type": "#microsoft.graph.presence",
    "id": "bf423481-3481-bf42-8134-42bf813442bf",
    "availability": "String",
    "activity": "String",
    "outOfOfficeSettings": {
      "@odata.type": "microsoft.graph.outOfOfficeSettings"
    }
  }
}
```

