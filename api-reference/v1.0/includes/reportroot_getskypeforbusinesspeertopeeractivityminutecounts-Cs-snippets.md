
```Cs

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var report = await graphClient.Reports.GetSkypeForBusinessPeerToPeerActivityMinuteCounts('D7')
	.Request()
	.GetAsync();

```