teraform fmt -- formate the .tf file  

terrafrom workspace new workspace  --create workspaces in isolated state 

terrafrom state-- list pull mv workspaces 

terraform taint-- deletes  and recreates the resource

terrform import---- imports already manually created resource 

terraform init-- download the provider modules for provisioning 

terrafrom plan--  shows the resource plans that are going to be orchestrated

terrafrom apply--  creates teh resource 

terrafrom destroy-- deletes the resoure 

terrafrom workspace select newworkspace --  select a different workspace 

TF_LOG=dEBUG terrafrom apply -- run terrafrom in debug mode 
BACKEND

terraform {
  backend "azurerm" {
    resource_group_name  = "StorageAccount-ResourceGroup"
    storage_account_name = "abcd1234"
    container_name       = "tfstate"
    key                  = "prod.terraform.tfstate"
  }
}

condition 
condition ? true_val : false_val



variable "users" {
  type = map(object({
    is_admin = boolean
  }))
}

locals {
  admin_users = {
    for name, user in var.users : name => user
    if user.is_admin
  }
  regular_users = {
    for name, user in var.users : name => user
    if !user.is_admin
  }
}
var.a != "" ? var.a : "default-a"

