---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter)

requestBody := graphmodels.NewAccessPackageResourceRequest()
catalogId := "26ac0c0a-08bc-4a7b-a313-839f58044ba5"
requestBody.SetCatalogId(&catalogId) 
requestType := "AdminAdd"
requestBody.SetRequestType(&requestType) 
justification := ""
requestBody.SetJustification(&justification) 
accessPackageResource := graphmodels.NewaccessPackageResource()
displayName := "Faculty cafeteria ordering"
accessPackageResource.SetDisplayName(&displayName) 
description := "Example application"
accessPackageResource.SetDescription(&description) 
url := "https://myapps.microsoft.com/example.com/signin/Faculty%20cafeteria%20ordering/f1e3b407-942d-4934-9a3f-cef1975cb988/"
accessPackageResource.SetUrl(&url) 
resourceType := "Application"
accessPackageResource.SetResourceType(&resourceType) 
originId := "2f1099a6-d4fc-4cc9-a0ef-ddd3f1bf0b7e"
accessPackageResource.SetOriginId(&originId) 
originSystem := "AadApplication"
accessPackageResource.SetOriginSystem(&originSystem) 


accessPackageResourceAttribute := graphmodels.NewAccessPackageResourceAttribute()
attributeName := "extension_2b676109c7c74ae2b41549205f1947ed_personalTitle"
accessPackageResourceAttribute.SetAttributeName(&attributeName) 
isEditable := true
accessPackageResourceAttribute.SetIsEditable(&isEditable) 
isPersistedOnAssignmentRemoval := true
accessPackageResourceAttribute.SetIsPersistedOnAssignmentRemoval(&isPersistedOnAssignmentRemoval) 
attributeSource := graphmodels.NewAccessPackageResourceAttributeSource()
additionalData := map[string]interface{}{
question := graphmodels.New()
	isRequired := false
question.SetIsRequired(&isRequired) 
sequence := int32(0)
question.SetSequence(&sequence) 
	isSingleLineQuestion := true
question.SetIsSingleLineQuestion(&isSingleLineQuestion) 
text := graphmodels.New()
defaultText := "Title"
text.SetDefaultText(&defaultText) 
	localizedTexts := []graphmodels.able {

	}
	text.SetLocalizedTexts(localizedTexts)
	question.SetText(text)
	attributeSource.SetQuestion(question)
}
attributeSource.SetAdditionalData(additionalData)
accessPackageResourceAttribute.SetAttributeSource(attributeSource)
attributeDestination := graphmodels.NewAccessPackageResourceAttributeDestination()
accessPackageResourceAttribute.SetAttributeDestination(attributeDestination)

attributes := []graphmodels.AccessPackageResourceAttributeable {
	accessPackageResourceAttribute,

}
accessPackageResource.SetAttributes(attributes)
requestBody.SetAccessPackageResource(accessPackageResource)

result, err := graphClient.IdentityGovernance().EntitlementManagement().AccessPackageResourceRequests().Post(requestBody)


```