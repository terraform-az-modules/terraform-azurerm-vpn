<!-- BEGIN_TF_DOCS -->
## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | >= 1.6.6 |
| <a name="requirement_azurerm"></a> [azurerm](#requirement\_azurerm) | >=3.116.0 |

## Providers

No providers.

## Modules

| Name | Source | Version |
|------|--------|---------|
| <a name="module_log-analytics"></a> [log-analytics](#module\_log-analytics) | clouddrove/log-analytics/azure | 2.0.0 |
| <a name="module_resource_group"></a> [resource\_group](#module\_resource\_group) | terraform-az-modules/resource-group/azure | 1.0.0 |
| <a name="module_subnet"></a> [subnet](#module\_subnet) | terraform-az-modules/subnet/azure | 1.0.0 |
| <a name="module_vnet"></a> [vnet](#module\_vnet) | terraform-az-modules/vnet/azure | 1.0.0 |
| <a name="module_vpn"></a> [vpn](#module\_vpn) | ../../ | n/a |

## Resources

No resources.

## Inputs

No inputs.

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_local_network_gw_connection_id"></a> [local\_network\_gw\_connection\_id](#output\_local\_network\_gw\_connection\_id) | The ID of the Virtual Network Gateway Connection. |
| <a name="output_vpn_gw_id"></a> [vpn\_gw\_id](#output\_vpn\_gw\_id) | The ID of the Virtual Network Gateway. |
<!-- END_TF_DOCS -->