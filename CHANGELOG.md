# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## Unreleased

## [2.2.1] - 2018-4-9

## Removed `auto-approve` from terraform Makefile

## [2.2.0] - 2018-3-30

## Added
- colorful logging
- bug fixes and better support for GCP infrastructure
- `--gcp-revion` as part of the above change

## Updated
- `yaml_source` no longer throws errors when file is empty, just logs a message
- made the component class location method more flexible
- reorganized terraform files and made terraform a first class citizen and part of the `inventory.Inventory` component
- renamed vpc.VPC component to aws_vpc.AWSVpc as part of above change
- reorganize the defaul `secrets.yml` and removed unnecessary lines


## [2.1.0] - 2018-2-27

## Added
- `--version` flag to output version
- added cluster auto scaling iam policies by default
- added `--cloud` flag and supporting flags to create GCP/GKE infrastructure

### Updated
- Version handling in setup.py
- Updated yaml loader for config file reading to force string behavior
- Inventory component will use -D name= as the targe directory instead needing -o. 
- Inventory -D account replaced with -D name


## [2.0.0] - 2018-2-1
### Added
- `yaml_source` script to replace env-vars.sh
- Environment variables are now checked in ComponentBase class
- Defaults to component
- overwrite to template rendering
- added inventory component
- added vpn component

### Removed
- env-vars.sh script
- untracked roles directory for ansible

### Updated 
- makefile to support `yaml_source` change
- added distutil.dir_util to allow overwriting exisint directories
- added exit on failure for ComponentBase class
- added default config out file for Pentaong start-project
- updated config file output to sanitize and not include blank values

## [1.2.0] - 2017-11-8
### Added
- Added kops component

### Changed
- Added VPN name to include project name. Allows multiple VPN instances per VPC
- Set default versions to ansible roles
- Updated default kops cluster templates to use new kops component
- Updated make file to use Terraform outputs and improve robustness of creat and destroy
- Fixed legacy authorization bug in gcp coponent

### Removed
- Removed the older kops cluster creation


## [1.1.0] - 2017-10-4
### Added
- Added Changelog
- Added `add` method to `pentagon` command line
- Added component base class
- Added GCP and VPC components
- Added Example component

### Changed
- Changed VPC directory creation to utilize component class instead of 
- Change Click libary usage to "setup tools" method

### Removed
- Section about "changelog" vs "CHANGELOG".

## [1.0.0]

### Added
- First open source version of Pentagon
