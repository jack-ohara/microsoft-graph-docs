---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)


requestId := "https://graph.microsoft.com/beta/groups/{other-group-id}"

requestParameters := &graphconfig.RefRequestBuilderDeleteQueryParameters{
	Id: &requestId,
}
configuration := &graphconfig.RefRequestBuilderDeleteRequestConfiguration{
	QueryParameters: requestParameters,
}

graphClient.GroupsById("group-id").RejectedSenders().$ref().DeleteWithRequestConfigurationAndResponseHandler(configuration, nil)


```