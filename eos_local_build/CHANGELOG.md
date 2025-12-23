<!-- https://developers.home-assistant.io/docs/add-ons/presentation#keeping-a-changelog -->

## 1.2.4

- Revert the fixed change of IP listen addreess for server and EOSdash to 0.0.0.0

## 1.2.3

- Change IP listen addreess for server and EOSdash to 0.0.0.0 and add default config

## 1.2.2

- Add info about usage of new "recorder.get_statistics" action, which makes the usage of SQL sensors obsolete

## 1.2.1

- EOS (non local build) version update

## 1.2

- Add info about breaking change for config and optimization payload

## 1.1.6

- Add git client

## 1.1.5

- Readd build.yaml

## 1.1.4

- Bump version due to duplicated slug of local build version

## 1.1.3

- Bump version for Github builder Action

## 1.1.2

- Add eos dashboard (default 8504) to configuration

## 1.1.1

- updated documentation for new EOS version
  Important: naming changes in the EOS optimize call requires reconfiguration of the optimize automation call !!!

## 1.1.0

- update EOS version 02.03.2025

## 1.0.12

- remove apparmor profile

## 1.0.11

- armv7 is also not working up to now

## 1.0.10

- Missing execute permission on s6 scripts.

## 1.0.9

- local installation worked, remote doesn't. Maybe apparmor profile is not correctly applied?

## 1.0.8

- armhf is also not supported

## 1.0.7

- Wrong comments in README.md's

## 1.0.6

- docker image URL has to be lowercase

## 1.0.5

- URL for submodules is stored in the config and .gitmodules

## 1.0.4

- submodules need to use https not ssh url's

## 1.0.3

- Updated to newest EOS upstream version

## 1.0.2

- i386 is not supported

## 1.0.1

- Fix Github Actions checkouts with submodules

## 1.0.0

- Initial release
