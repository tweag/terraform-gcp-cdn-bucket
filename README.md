# A Google Storage Bucket + CDN configuration

This modules contains essentially two things:

* A GCS bucket to store objects into
* A load-balancer connected to it

It also makes a few assumptions:

* A service account will be created to write into the bucket
* All objects are meant to be publicly-readable

## Module config

`> terraform-docs md .`
<!-- BEGIN mdsh -->
## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|:----:|:-----:|:-----:|
| cache\_retention\_days | The number of days to keep the objects around | string | null | no |
| labels | Labels to apply on all the resources | map | `<map>` | no |
| name | Name prefix for all the resources | string | n/a | yes |
| project | GCP project name | string | n/a | yes |
| region | GCP region in which to create the resources | string | n/a | yes |
| ssl\_certificate | A reference to the SSL certificate, google managed or not | string | n/a | yes |

## Outputs

| Name | Description |
|------|-------------|
| bucket\_name | Name of the GCS bucket that will receive the objects. |
| external\_ip | The external IP assigned to the global fowarding rule. |

<!-- END mdsh -->

## License

This work is licensed under the Apache License 2.0.
See [LICENSE](LICENSE) for more details.

## Sponsors

This work has been sponsored by [Digital Asset](https://digitalasset.com) and [Tweag I/O](https://tweag.io).

[![Digital Asset](https://avatars1.githubusercontent.com/u/9829909?s=200&v=4)](http://digitalasset.com)
[![Tweag I/O](https://avatars1.githubusercontent.com/u/6057932?s=200&v=4)](https://tweag.io)

This repository is maintained by [Tweag I/O](http://tweag.io)

Have questions? Need help? Tweet at
[@tweagio](http://twitter.com/tweagio).
