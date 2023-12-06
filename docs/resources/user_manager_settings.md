# routeros_user_manager_settings (Resource)


## Example Usage
```terraform
resource "routeros_user_manager_settings" "settings" {
  enabled = true
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Optional

- `accounting_port` (Number) Port to listen for RADIUS accounting requests.
- `authentication_port` (Number) Port to listen for RADIUS authentication requests.
- `certificate` (String) Certificate for use in EAP TLS-type authentication methods.
- `enabled` (Boolean) An option whether the User Manager functionality is enabled.
- `use_profiles` (Boolean) An option whether to use Profiles and Limitations. When set to `false`, only User configuration is required to run User Manager.

### Read-Only

- `id` (String) The ID of this resource.

## Import
Import is supported using the following syntax:
```shell
terraform import routeros_user_manager_settings.settings .
```