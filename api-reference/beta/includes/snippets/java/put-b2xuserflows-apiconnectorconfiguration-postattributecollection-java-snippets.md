---
description: "Automatically generated file. DO NOT MODIFY"
---

```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IdentityApiConnector identityApiConnector = new IdentityApiConnector();
identityApiConnector.additionalDataManager().put("@odata.id", new JsonPrimitive("https://graph.microsoft.com/beta/identity/apiConnectors/{id}"));

graphClient.identity().b2xUserFlows("B2X_1_testuserflow").postAttributeCollection().reference()
	.buildRequest()
	.put(identityApiConnector);

```