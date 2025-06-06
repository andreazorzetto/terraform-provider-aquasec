---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "aquasec_role_mapping_saas Resource - terraform-provider-aquasec"
subcategory: ""
description: |-
  
---

# aquasec_role_mapping_saas (Resource)

Role mappings in Aqua SaaS allow you to associate SAML group names with specific roles defined in the Aqua platform. This enables fine-grained access control via your identity provider (IdP).

The Terraform resource aquasec_role_mapping_saas enables you to define these mappings as code.

Prerequisites: permission_set_saas (`aquasec_permission_set_saas`), role (`aquasec_role`)

---

## Example Usage

```terraform
resource "aquasec_role_mapping_saas" "roles_mapping_saas" {
  saml_groups = ["group1", "group2"]
  csp_role    = "Administrator" # Must match an existing role
}

output "roles_mapping_saas" {
  value = aquasec_role_mapping_saas.roles_mapping_saas
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `csp_role` (String)
- `saml_groups` (List of String)

### Read-Only

- `account_id` (Number)
- `created` (String)
- `id` (String) The ID of this resource.
- `role_mapping_id` (Number)


