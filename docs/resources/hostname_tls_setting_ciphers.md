---
page_title: "cloudflare_hostname_tls_setting_ciphers Resource - Cloudflare"
subcategory: ""
description: |-
  Provides a Cloudflare per-hostname TLS setting resource, specifically for ciphers suites. Used to set ciphers suites for hostnames under the specified zone.
---

# cloudflare_hostname_tls_setting_ciphers (Resource)

Provides a Cloudflare per-hostname TLS setting resource, specifically for ciphers suites. Used to set ciphers suites for hostnames under the specified zone.

## Example Usage

```terraform
resource "cloudflare_hostname_tls_setting_ciphers" "example" {
  zone_id  = "0da42c8d2132a9ddaf714f9e7c920711"
  hostname = "sub.example.com"
  value    = ["ECDHE-RSA-AES128-GCM-SHA256"]
}
```
<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `hostname` (String) Hostname that belongs to this zone name. **Modifying this attribute will force creation of a new resource.**
- `value` (List of String) Ciphers suites value.
- `zone_id` (String) The zone identifier to target for the resource. **Modifying this attribute will force creation of a new resource.**

### Optional

- `ports` (List of Number) Ports to use within the IP rule.

### Read-Only

- `created_at` (String)
- `id` (String) The ID of this resource.
- `updated_at` (String)

## Import

Import is supported using the following syntax:

```shell
$ terraform import cloudflare_hostname_tls_setting_ciphers.example <zone_id>/<hostname>
```