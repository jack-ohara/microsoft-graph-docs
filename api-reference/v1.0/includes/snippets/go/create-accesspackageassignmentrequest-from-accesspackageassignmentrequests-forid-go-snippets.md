---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewAccessPackageAssignmentRequest()
requestType := graphmodels.ADMINREMOVE_ACCESSPACKAGEREQUESTTYPE 
requestBody.SetRequestType(&requestType) 
assignment := graphmodels.Newassignment()
id := "a6bb6942-3ae1-4259-9908-0133aaee9377"
assignment.SetId(&id) 
requestBody.SetAssignment(assignment)

result, err := graphClient.IdentityGovernance().EntitlementManagement().AssignmentRequests().Post(requestBody)


```