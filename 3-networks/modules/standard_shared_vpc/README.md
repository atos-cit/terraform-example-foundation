<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|:----:|:-----:|:-----:|
| bgp\_asn\_subnet | BGP ASN for Subnets cloud routers. | number | n/a | yes |
| default\_fw\_rules\_enabled | Toggle creation of default firewall rules. | bool | `"true"` | no |
| default\_region1 | Default region 1 for subnets and Cloud Routers | string | n/a | yes |
| default\_region2 | Default region 2 for subnets and Cloud Routers | string | n/a | yes |
| dns\_enable\_inbound\_forwarding | Toggle inbound query forwarding for VPC DNS. | bool | `"true"` | no |
| dns\_enable\_logging | Toggle DNS logging for VPC DNS. | bool | `"true"` | no |
| environment\_code | A short form of the folder level resources (environment) within the Google Cloud organization. | string | n/a | yes |
| nat\_bgp\_asn | BGP ASN for first NAT cloud routes. | number | `"0"` | no |
| nat\_enabled | Toggle creation of NAT cloud router. | bool | `"false"` | no |
| nat\_num\_addresses | Number of external IPs to reserve for Cloud NAT. | number | `"2"` | no |
| nat\_num\_addresses\_region1 | Number of external IPs to reserve for first Cloud NAT. | number | `"2"` | no |
| nat\_num\_addresses\_region2 | Number of external IPs to reserve for second Cloud NAT. | number | `"2"` | no |
| private\_service\_cidr | CIDR range for private service networking. Used for Cloud SQL and other managed services. | string | n/a | yes |
| project\_id | Project ID for Private Shared VPC. | string | n/a | yes |
| secondary\_ranges | Secondary ranges that will be used in some of the subnets | object | `<map>` | no |
| subnets | The list of subnets being created | list(map(string)) | `<list>` | no |
| vpc\_label | Label for VPC. | string | n/a | yes |
| windows\_activation\_enabled | Enable Windows license activation for Windows workloads. | bool | `"false"` | no |

## Outputs

| Name | Description |
|------|-------------|
| allow\_iap\_rdp | Firewall rule allow_iap_rdp created in the network |
| allow\_iap\_ssh | Firewall rule allow_iap_ssh created in the network |
| allow\_lb | Firewall rule allow_lb created in the network |
| default\_policy | DNS Policy created in the network |
| dns\_record\_set\_gcr\_api | DNS Record set for GCR APIs |
| dns\_record\_set\_private\_api | DNS Record set for Private APIs |
| network\_name | The name of the VPC being created |
| network\_self\_link | The URI of the VPC being created |
| region1\_router1 | Router 1 for Region 1 |
| region1\_router2 | Router 2 for Region 1 |
| region2\_router1 | Router 1 for Region 2 |
| region2\_router2 | Router 2 for Region 2 |
| subnets\_flow\_logs | Whether the subnets have VPC flow logs enabled |
| subnets\_ips | The IPs and CIDRs of the subnets being created |
| subnets\_names | The names of the subnets being created |
| subnets\_private\_access | Whether the subnets have access to Google API's without a public IP |
| subnets\_regions | The region where the subnets will be created |
| subnets\_secondary\_ranges | The secondary ranges associated with these subnets |
| subnets\_self\_links | The self-links of subnets being created |

<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->