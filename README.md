# module-ubuntu-linux-app/azurerm

## Description
Terraform module for Ubuntu Linux app deployment on Microsoft Azure

## Deployment
This module creates a single instance having one network interface.

## Usage
```tf
module "Agent" {
	source  = "armdupre/module-ubuntu-linux-app/azurerm"
	Eth0SubnetId = module.Vnet.PublicSubnet.id
	ResourceGroupName = azurerm_resource_group.ResourceGroup.name
	SshKeyName = azurerm_ssh_public_key.SshKey.name
}
```