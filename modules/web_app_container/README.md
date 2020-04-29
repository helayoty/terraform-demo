```HCL

module "web_app_container" {
  source              = "../modules/web_app_container"
  name                = var.prefix
  port                = "80"
  https_only          = "false"
  resource_group_name = azurerm_resource_group.myresourcegroup.name
  container_type      = "docker"
  container_image     = "innovationnorway/python-hello-world:latest" #"helayoty/temp"
}

```