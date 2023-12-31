# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## [0.5.0] - 2023-12-04
### Added
- Variable `enable_fabio_lb` (default: `false`), when enabled will provision external IP and Forwarding Rule (i.e. load balancer) which points to Fabio LB port of 9999 on Nomad clients
### Changed
- Split Nomad clients and related resources into its own file, `nomad_clients.tf` for easier management

## [0.4.0] - 2023-11-25
### Changed
- Added Consul and Nomad DC names as suffixes for cluster and load balancer resources for easier identification.
- Updated `google` and `google-beta` providers from `~> 4.0` to `~> 5.0`

## [0.3.1] - 2023-10-07
### Changed
- Updated `google` provider from `>= 4.78.0` to `~> 4.0`

## [0.3.0] - 2023-10-02
### Added
- New variables, `consul_dc` and `nomad_dc` for the Consul and Nomd datacenter names respectively
### Removed
- `environment` variable

## [0.2.0] - 2023-09-30
### Added
- Custom service account for Compute Engine
- L7 application load balancer in front of the Consul and Nomad servers 
- Cloud Router (NAT)
- [Custom input validation rules](https://developer.hashicorp.com/terraform/language/values/variables#custom-validation-rules)
### Changed
- Consul and Nomad servers no longer provisioned with external IPs
- `can_ip_forward` set to `true`
- `firewall.tf` renamed to `network.tf`

## [0.1.0] - 2023-09-28
### Added
- Initial commit
