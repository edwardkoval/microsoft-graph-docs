
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const directoryRole = {
  roleTemplateId: "roleTemplateId-value"
};

let res = await client.api('/directoryRoles')
	.post({directoryRole : directoryRole});

```