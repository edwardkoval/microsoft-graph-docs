
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const educationUser = {
  @odata.id:"https://graph.microsoft.com/beta/education/users/14011"
};

let res = await client.api('/education/classes/11017/teachers/$ref')
	.version('beta')
	.post({educationUser : educationUser});

```