## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| aa\_ip\_configuration\_name | Name for the active-active ip\_configuration | `string` | `"vnetGatewayAAConfig"` | no |
| certification\_enable | Set to false to prevent the module from creating certificate resources. | `bool` | `false` | no |
| custom\_name | Override default naming convention | `string` | `null` | no |
| deployment\_mode | Specifies how the infrastructure/resource is deployed | `string` | `"terraform"` | no |
| diagnostic\_setting\_enable | n/a | `bool` | `false` | no |
| enable | Flag to control the module creation. | `bool` | `true` | no |
| enable\_active\_active | If true, an active-active Virtual Network Gateway will be created. An active-active gateway requires a HighPerformance or an UltraPerformance sku. If false, an active-standby gateway will be created. Defaults to false. | `bool` | `false` | no |
| enable\_bgp | If true, BGP (Border Gateway Protocol) will be enabled for this Virtual Network Gateway. Defaults to false | `bool` | `false` | no |
| environment | Environment (e.g. `prod`, `dev`, `staging`). | `string` | `null` | no |
| eventhub\_authorization\_rule\_id | Specifies the ID of an Event Hub Namespace Authorization Rule used to send Diagnostics Data. | `string` | `null` | no |
| eventhub\_name | Specifies the name of the Event Hub where Diagnostics Data should be sent. | `string` | `null` | no |
| express\_route\_circuit\_id | The ID of the Express Route Circuit when creating an ExpressRoute connection | `string` | `null` | no |
| extra\_tags | Variable to pass extra tags. | `map(string)` | `null` | no |
| gateway\_connection\_protocol | The IKE protocol version to use. Possible values are IKEv1 and IKEv2. Defaults to IKEv2 | `string` | `"IKEv2"` | no |
| gateway\_connection\_type | The type of connection. Valid options are IPsec (Site-to-Site), ExpressRoute (ExpressRoute), and Vnet2Vnet (VNet-to-VNet) | `string` | `"IPsec"` | no |
| gateway\_type | The type of the Virtual Network Gateway. Valid options are Vpn or ExpressRoute | `string` | `"Vpn"` | no |
| ip\_configuration\_name | Name for the ip\_configuration | `string` | `"vnetGatewayConfig"` | no |
| label\_order | The order of labels used to construct resource names or tags. If not specified, defaults to ['name', 'environment', 'location']. | `list(string)` | <pre>[<br>  "name",<br>  "environment",<br>  "location"<br>]</pre> | no |
| local\_bgp\_settings | Local Network Gateway's BGP speaker settings | `list(object({ asn_number = number, peering_address = string, peer_weight = number }))` | `null` | no |
| local\_networks | List of local virtual network connections to connect to gateway | `list(object({ local_gw_name = string, local_gateway_address = string, local_address_space = list(string), shared_key = string }))` | `[]` | no |
| local\_networks\_ipsec\_policy | IPSec policy for local networks. Only a single policy can be defined for a connection. | `map(string)` | `null` | no |
| location | The location/region where the virtual network is created. | `string` | `"canadacentral"` | no |
| log\_analytics\_destination\_type | Possible values are AzureDiagnostics and Dedicated, default to AzureDiagnostics. When set to Dedicated, logs sent to a Log Analytics workspace will go into resource specific tables, instead of the legacy AzureDiagnostics table. | `string` | `"AzureDiagnostics"` | no |
| log\_analytics\_workspace\_id | n/a | `string` | `null` | no |
| log\_category\_pip | Categories of logs to be recorded in diagnostic setting for vpngw. | `list(string)` | <pre>[<br>  "DDoSProtectionNotifications"<br>]</pre> | no |
| log\_category\_vpngw | Categories of logs to be recorded in diagnostic setting for pip\_gw. | `list(string)` | <pre>[<br>  "GatewayDiagnosticLog"<br>]</pre> | no |
| managedby | ManagedBy, eg 'terraform-az-modules'. | `string` | `"terraform-az-modules"` | no |
| metric\_enabled | Whether metric diagnonsis should be enable in diagnostic settings for vpn module. | `bool` | `true` | no |
| name | Name  (e.g. `app` or `cluster`). | `string` | `""` | no |
| peer\_virtual\_network\_gateway\_id | The ID of the peer virtual network gateway when creating a VNet-to-VNet connection | `string` | `null` | no |
| public\_ip\_allocation\_method | Defines the allocation method for this IP address. Possible values are Static or Dynamic. Defaults to Dynamic | `string` | `"Static"` | no |
| public\_ip\_sku | The SKU of the Public IP. Accepted values are Basic and Standard. Defaults to Basic | `string` | `"Standard"` | no |
| public\_ip\_zones | Zones for the VPN public IP. Required for \*AZ gateway SKUs. | `list(string)` | `[]` | no |
| repository | Terraform current module repo | `string` | `"https://github.com/terraform-az-modules/terraform-azure-vpn"` | no |
| resource\_group\_name | The name of an existing resource group to be imported. | `string` | `null` | no |
| resource\_position\_prefix | Controls the placement of the resource type keyword (e.g., "vnet", "ddospp") in the resource name.<br><br>- If true, the keyword is prepended: "vnet-core-dev".<br>- If false, the keyword is appended: "core-dev-vnet".<br><br>This helps maintain naming consistency based on organizational preferences. | `bool` | `true` | no |
| root\_certificate\_name | Name for the root certificate in VPN client configuration | `string` | `"point-to-site-root-certifciate"` | no |
| sku | Configuration of the size and capacity of the virtual network gateway | `string` | `"VpnGw1"` | no |
| storage\_account\_id | The ID of the Storage Account where logs should be sent. | `string` | `null` | no |
| sts\_vpn | Set to false to prevent the module from creating sts vpn resources. | `bool` | `false` | no |
| subnet\_id | The ID of the Subnet where this Network Interface should be located in. | `string` | `""` | no |
| vpn\_ad | Set to false to prevent the module from creating vpn ad resources. | `bool` | `false` | no |
| vpn\_client\_configuration | Virtual Network Gateway client configuration to accept IPSec point-to-site connections | `object({ address_space = string, vpn_client_protocols = list(string), aad_tenant = string, aad_audience = string, aad_issuer = string, vpn_auth_types = list(string) })` | `null` | no |
| vpn\_client\_configuration\_c | Virtual Network Gateway client configuration to accept IPSec point-to-site connections | `object({ address_space = string, vpn_client_protocols = list(string), certificate = string })` | `null` | no |
| vpn\_gw\_generation | The Generation of the Virtual Network gateway. Possible values include Generation1, Generation2 or None | `string` | `"Generation1"` | no |
| vpn\_gw\_sku | Configuration of the size and capacity of the virtual network gateway. Valid options are Basic, VpnGw3, VpnGw2, VpnGw3, VpnGw4,VpnGw5, VpnGw3AZ, VpnGw3, VpnGw3AZ,VpnGw4AZ and VpnGw5AZ and depend on the type, vpn\_type and generation arguments | `string` | `"VpnGw1"` | no |
| vpn\_type | The routing type of the Virtual Network Gateway. Valid options are RouteBased or PolicyBased. Defaults to RouteBased | `string` | `"RouteBased"` | no |

## Outputs

| Name | Description |
|------|-------------|
| local\_network\_gw\_connection\_id | The ID of the Virtual Network Gateway Connection. |
| local\_network\_gw\_id | The ID of the Local Network Gateway. |
| vpn\_gw\_id | The ID of the active Virtual Network Gateway. |

