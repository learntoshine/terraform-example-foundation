<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|:----:|:-----:|:-----:|
| access\_context\_manager\_policy\_id | The ID of the access context manager policy the perimeter lies in. Can be obtained by running `gcloud access-context-manager policies list --organization YOUR-ORGANIZATION_ID --format="value(name)"`. | string | n/a | yes |
| alert\_pubsub\_topic | The name of the Cloud Pub/Sub topic where budget related messages will be published, in the form of `projects/{project_id}/topics/{topic_id}` | string | `"null"` | no |
| alert\_spent\_percents | A list of percentages of the budget to alert on when threshold is exceeded | list(number) | `<list>` | no |
| billing\_account | The ID of the billing account to associated this project with | string | n/a | yes |
| budget\_amount | The amount to use as the budget | number | `"1000"` | no |
| env\_code | A short form of the environment field | string | `"p"` | no |
| org\_id | The organization id for the associated services | string | n/a | yes |
| parent\_folder | Optional - if using a folder for testing. | string | `""` | no |
| perimeter\_name | Access context manager service perimeter name to attach the restricted svpc project. | string | n/a | yes |
| skip\_gcloud\_download | Whether to skip downloading gcloud (assumes gcloud is already available outside the module) | bool | `"true"` | no |
| terraform\_service\_account | Service account email of the account to impersonate to run Terraform | string | n/a | yes |

## Outputs

| Name | Description |
|------|-------------|
| access\_context\_manager\_policy\_id | Access Context Manager Policy ID. |
| base\_shared\_vpc\_project | Project sample base project. |
| floating\_project | Project sample floating project. |
| restricted\_enabled\_apis | Activated APIs. |
| restricted\_shared\_vpc\_project | Project sample restricted project id. |
| restricted\_shared\_vpc\_project\_number | Project sample restricted project. |
| vpc\_service\_control\_perimeter\_name | VPC Service Control name. |

<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
