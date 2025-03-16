# azure-resource-group
Terraform module for managing Azure Resource Groups. Provides a standardized way to create and manage resource groups across multiple environments.
## Usage

```hcl
module "resource_group" {
    source              = "github.com/open-terraform-modules/azure-resource-group"
    resource_group_name = "example-rg"
    location            = "West Europe"
    tags                = {
        environment = "dev"
        project     = "example"
    }
}
```

## Inputs

| Name                | Description                              | Type     | Default | Required |
|---------------------|------------------------------------------|----------|---------|----------|
| name                | The name of the resource group           | `string` | n/a     | yes      |
| location            | The location of the resource group       | `string` | n/a     | yes      |
| tags                | A map of tags to assign to the resource  | `map`    | `{}`    | no       |

## Outputs

| Name              | Description                          |
|-------------------|--------------------------------------|
| id                | The ID of the resource group created |

## Contributing

To contribute to this project, follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit your changes (`git commit -m 'Add some feature'`).
5. Push to the branch (`git push origin feature-branch`).
6. Open a pull request.

## Author

This module is maintained by [Andres Montealegre](mailto:montealegre.af@gmail.com).