# hostSecurityProfile resource type

 > **Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change. Use of these APIs in production applications is not supported.

Defines the relevant security properties of a host (for example, desktop, server, firewall, or other endpoint) to provide additional context for alerts and targets for actions.

 Security profiles are populated by integrated solutions at their discretion. For example:

- A solution will populate **hostSecurityProfile** for any desktop, laptop, server, firewall, or other endpoint that their service is responsible for monitoring, alerting, or taking threat remediation actions against.
- A provider will populate **hostSecurityProfile** for a collected set of IP addresses that their service is responsible for isolating, monitoring, or configuring.

## Methods

| Method   | Return Type |Description|
|:---------------|:--------|:----------|
|[Get host security profile](../api/hostsecurityprofile_get.md) | [hostSecurityProfile](hostsecurityprofile.md) |Read properties and relationships of a hostSecurityProfile object.|
|[Update host security profile](../api/hostsecurityprofile_update.md) | [hostSecurityProfile](hostsecurityprofile.md)|Update a hostSecurityProfile object. |
|[List host security profiles](../api/hostsecurityprofile_list.md) |[hostSecurityProfile](hostsecurityprofile.md) collection| Get a hostSecurityProfile object collection.|

## Properties

| Property   | Type |Description|
|:---------------|:--------|:----------|
|azureSubscriptionId|String|Azure subscription ID of the entity, if this entity represents an Azure resource.|
|azureTenantId *|String|Azure Active Directory tenant ID of this resource.|
|createdDateTime *|DateTimeOffset|Time at which the alert was created. The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`.|
|fqdn|String|Fully Qualified Domain Name - Hostname including the DNS domain name (for example, `machine.company.com`).|
|id *|String|Provider-generated GUID/unique identifier. Read-only.|
|isAzureAdJoined|Boolean|True if the host is domain joined to Azure Active Directory Domain Services.|
|isAzureAdRegistered|Boolean|True if the host registered with Azure Active Directory Device Registration (for example, BYOD devices - i.e. is not fully managed by enterprise).|
|isHybridAzureDomainJoined|Boolean|True if the host is domain-joined (Active Directory on premises).
|lastModifiedDateTime|DateTimeOffset|Time at which the alert was last modified. The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`.|
|logicalName|String|A name for the host collection.|
|logonUsers|[logonUser](logonuser.md) collection|Security-related stateful information pertaining to one or more user logons to this host.|
|netBiosName|String|Local hostname - i.e. without the DNS domain name.|
|networkInterfaces|[networkInterface](networkinterface.md) collection|Collection of the NICs and related data (IP addresses and MAC address) associated with each NIC.|
|osVersion|String|Host operating system version.|
|parentHost|String|The parent host of this host.  Can be null.|
|platform|String|Name of the host operating system.|
|riskScore|String|Provider-calculated risk score of the host.|
|tags|String collection|User-definable labels that can be applied to an hostSecurityProfile and can serve as filter conditions (for example "HVA", "SAW", and so on) (supports [update](../api/hostsecurityprofile_update.md)).|
|vendorInformation *|[securityVendorInformation](securityvendorinformation.md)|Complex type that contains details about the security product/service vendor, provider, and subprovider (for example, vendor=Microsoft; provider=Windows Defender ATP; subProvider=AppLocker).|
(\* Indicates a mandatory field.)

## Relationships

None.

## JSON representation

The following is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.hostSecurityProfile"
}-->

```json
{
  "azureSubscriptionId": "String",
  "azureTenantId": "String",
  "createdDateTime": "String (timestamp)",
  "fqdn": "String",
  "id": "String (identifier)",
  "isAzureAdJoined": true,
  "isAzureAdRegistered": true,
  "isHybridAzureDomainJoined": true,
  "lastModifiedDateTime": "String (timestamp)",
  "logicalName": "String",
  "logonUsers": [{"@odata.type": "microsoft.graph.logonUser"}],
  "netBiosName": "String",
  "networkInterfaces": [{"@odata.type": "microsoft.graph.networkInterface"}],
  "osVersion": "String",
  "parentHost": "String",
  "platform": "String",
  "riskScore": "String",
  "tags": ["String"],
  "vendorInformation": {"@odata.type": "microsoft.graph.securityVendorInformation"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "hostSecurityProfile resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
