
```Javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const driveItem = {
  parentReference: {
    id: "{new-parent-folder-id}"
  },
  name: "new-item-name.txt"
};

let res = await client.api('/me/drive/items/{item-id}')
	.update({driveItem : driveItem});

```