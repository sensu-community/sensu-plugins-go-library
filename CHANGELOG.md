# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic
Versioning](http://semver.org/spec/v2.0.0.html).

## Unreleased

### Fixed
- Fixed a regression where camelcase names were not being kebab-cased in the CLI.

## [0.16.0]

### Changed
- Added support for Go generics

## [0.15.0] - 2022-02-17
### Changed
- Removed aws specific functionality, that will now exist as part of cloudwatch plugin

### Added
- Add ToProm function for sensu corev2 metric points

### Fixed
- CLI usage is no longer displayed when business logic execution fails.


## [0.14.1] - 2021-09-10
### Fixed
- Fix for annotation override output polluting check output

## [0.14.0] - 2021-08-09
### Added
- Added new aws sub-package to facilite aws service plugin development

## [0.13.1] - 2021-04-23
### Fixed
- Fix internal module references to use sensu/sensu-plugin-sdk  

## [0.13.0] - 2021-04-22
### Changed
- Plugin options using annotation paths will now look for downcased annotation key path as well as uncased path to fix a cornercase associated annotations provied as part of agent config file being automatically downcased.
- Update module to refer to sensu/sensu-plugin-sdk to reflect repository transfer into sensu github org

## [0.12.0] - 2021-03-18

### Added
Added new Hostname templating function.

## [0.11.0] - 2020-10-30
### Added
- Added support for event ID attribute
- Added new UUIDFromBytes templating function.

## [0.10.0] - 2020-10-07

### Added
Added UnixTime func to template expansion. See README for details.

## [0.9.0] - 2020-10-07

### Fixed
- Fix checks that use stdin, do not validate stdin json as event for check plugins

### Added
- Bump api/core/v2 version to 2.3.0 (adds support for new output_metric_format)

## [0.8.0] - 2020-08-14

### Added
- Added support for to designated PluginConfigOptions as Secret. If Secret, the default value for the argument will not be displayed in the usage message. This prevents sensitive values stored in envvars from leaking into the usage message.

### Fixed
- Do not create commandline flag unless Argument is set for PluginConfigOption

## [0.7.0] - 2020-06-03

### Added
- Added support to require a valid Sensu license file to execute enterprise handlers.

### Changed
- Updated go version from 1.12 to 1.13 in the mod file.
- Migrated TravisCI to Github Actions.
- Use go modules where appropriate for dependencies.

## [0.6.0] - 2020-02-06

### Added
- Added helpers for TLS configuration.

### Fixed
- Logs an error if the plugin fails to initialize.
- Prevent duplicated error messages fix the formatting.
- Fixed a bug that could result in a panic when CA certificate is specified.

## [0.5.0] - 2020-02-05

### Added
- Added package httpclient.
- Added documentation to a few packages.
- Added package version.

### Fixed
- Fixed a panic that could occur on nil checks or entities.
- Cleaned up argument parsing.

### Removed
- Removed package http.
