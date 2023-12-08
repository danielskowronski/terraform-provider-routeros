# routeros_system_user_settings (Resource)


## Example Usage
```terraform
resource "routeros_system_user_settings" "settings" {
  minimum_categories      = 2
  minimum_password_length = 8
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Optional

- `minimum_categories` (Number) An option specifies the complexity requirements of the password, with categories being uppercase, lowercase, digit, and symbol.
- `minimum_password_length` (Number) An option specifies the minimum length of the password.

### Read-Only

- `id` (String) The ID of this resource.

## Import
Import is supported using the following syntax:
```shell
terraform import routeros_system_user_settings.settings .
```