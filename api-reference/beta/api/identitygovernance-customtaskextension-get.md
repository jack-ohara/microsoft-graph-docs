---
title: "Get customTaskExtension"
description: "Read the properties and relationships of a customTaskExtension object."
author: "AlexFilipin"
ms.localizationpriority: medium
ms.prod: "governance"
doc_type: apiPageType
---

# Get customTaskExtension

Namespace: microsoft.graph.identityGovernance

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Read the properties and relationships of a [customTaskExtension](../resources/identitygovernance-customtaskextension.md) object.

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|LifecycleWorkflows.Read.All, LifecycleWorkflows.ReadWrite.All|
|Delegated (personal Microsoft account)|Not supported.|
|Application|LifecycleWorkflows.Read.All, LifecycleWorkflows.ReadWrite.All|

For delegated scenarios, the admin needs one of the following [Azure AD roles](/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles):

- Global administrator
- Global reader
- Lifecycle workflows administrator

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /identityGovernance/lifecycleWorkflows/customTaskExtensions/{customTaskExtensionId}
```

## Optional query parameters

This method supports the `$select` and `$expand` OData query parameters to help customize the response. For general information, see [OData query parameters](/graph/query-parameters).

## Request headers

|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body

Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a [customTaskExtension](../resources/identitygovernance-customtaskextension.md) object in the response body.

## Examples

### Request

The following is an example of a request.
<!-- {
  "blockType": "request",
  "name": "lifecycleworkflows_get_customtaskextension"
}
-->
``` http
GET https://graph.microsoft.com/beta/identityGovernance/lifecycleWorkflows/customTaskExtensions/ffcc4c85-5a14-448e-a390-77abf2700369
```

### Response

The following is an example of the response
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.identityGovernance.customTaskExtension"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#identityGovernance/lifecycleWorkflows/customTaskExtensions/$entity",
    "id": "ffcc4c85-5a14-448e-a390-77abf2700369",
    "displayName": "Grant manager access to mailbox and OneDrive",
    "description": "Grant manager access to mailbox and OneDrive",
    "createdDateTime": "2022-08-24T20:36:14.7006029Z",
    "lastModifiedDateTime": "2022-08-24T22:42:34.0744491Z",
    "endpointConfiguration": {
        "@odata.type": "#microsoft.graph.logicAppTriggerEndpointConfiguration",
        "subscriptionId": "c500b67c-e9b7-4ad2-a90d-77d41385ae55",
        "resourceGroupName": "RG-LCM",
        "logicAppWorkflowName": "ManagerAccess"
    },
    "authenticationConfiguration": {
        "@odata.type": "#microsoft.graph.azureAdTokenAuthentication",
        "resourceId": "542dc01a-0b5d-4edc-b3f9-5cfe6393f557"
    },
    "clientConfiguration": {
        "@odata.type": "#microsoft.graph.customExtensionClientConfiguration",
        "maximumRetries": 1,
        "timeoutInMilliseconds": 1000
    },
    "callbackConfiguration": {
        "@odata.type": "#microsoft.graph.identityGovernance.customTaskExtensionCallbackConfiguration",
        "timeoutDuration": "PT10M"
    },
    "createdBy": {
        "@odata.type": "#microsoft.graph.user",
        "id": "a698128f-b34f-44db-a9f9-7661c7aba8d8"
    },
    "lastModifiedBy": {
        "@odata.type": "#microsoft.graph.user",
        "id": "a698128f-b34f-44db-a9f9-7661c7aba8d8"
    }
}
```
