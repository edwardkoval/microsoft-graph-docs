
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

let res = await client.api('/groups')
	.filter('hasMembersWithLicenseErrors+eq+true,')
	.select('id,displayName')
	.get();

```