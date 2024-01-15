# routeros_wifi_access_list (Resource)
*<span style="color:red">This resource requires a minimum version of RouterOS 7.13.</span>*

## Example Usage
```terraform
resource "routeros_wifi_access_list" "radius" {
  action            = "query-radius"
  comment           = "RADIUS"
  radius_accounting = true
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Optional

- `action` (String) An action to take when a client matches.
- `allow_signal_out_of_range` (String) An option that permits the client's signal to be out of the range always or for some time interval.
- `client_isolation` (Boolean) An option that specifies whether to deny forwarding data between clients connected to the same interface.
- `comment` (String)
- `disabled` (Boolean)
- `interface` (String) Interface name to compare with an interface to which the client actually connects to.
- `mac_address` (String) MAC address of the client.
- `mac_address_mask` (String) MAC address mask to apply when comparing clients' addresses.
- `passphrase` (String) PSK passphrase for the client if some PSK authentication algorithm is used.
- `place_before` (String) Before which position the rule will be inserted.  
	> Please check the effect of this option, as it does not work as you think!  
	> Best way to use in conjunction with a data source. See [example](../data-sources/firewall.md#example-usage).
- `radius_accounting` (Boolean) An option that specifies if RADIUS traffic accounting should be used in case of RADIUS authentication of the client.
- `signal_range` (String) The range in which the client signal must fall.
- `ssid_regexp` (String) The regular expression to compare the actual SSID the client connects to.
- `time` (String) Time of the day and days of the week when the rule is applicable.
- `vlan_id` (String) VLAN ID to use for VLAN tagging or `none`.

### Read-Only

- `id` (String) The ID of this resource.

## Import
Import is supported using the following syntax:
```shell
#The ID can be found via API or the terminal
#The command for the terminal is -> :put [/interface/wifi/access-list get [print show-ids]]
terraform import routeros_wifi_access_list.radius '*1'
```