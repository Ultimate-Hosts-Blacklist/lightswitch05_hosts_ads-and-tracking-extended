# About lightswitch05_hosts_ads-and-tracking-extended

[![Build Status](https://travis-ci.org/Ultimate-Hosts-Blacklist/lightswitch05_hosts_ads-and-tracking-extended.svg?branch=master)](https://travis-ci.org/Ultimate-Hosts-Blacklist/lightswitch05_hosts_ads-and-tracking-extended)

```
# Collection of Analytics, Ads, and tracking hosts to block.
# 
# Title: Lightswitch05's ads-and-tracking-extended.txt
# Details: https://github.com/lightswitch05/hosts
# Issues: https://github.com/lightswitch05/hosts/issues
# Source: https://raw.githubusercontent.com/lightswitch05/hosts/master/ads-and-tracking-extended.txt
# 	
# Copyright 2019 Daniel White
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
# 
# http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
```

--------------------------------------------------------------------------------

# About Ultimate-Hosts-Blacklist

[Ultimate-Hosts-Blacklist](https://github.com/Ultimate-Hosts-Blacklist) serve a place to test and keep a track on each input sources that are present into [Ultimate Hosts Blacklist](https://github.com/mitchellkrogza/Ultimate.Hosts.Blacklist).

As [Ultimate Hosts Blacklist](https://github.com/mitchellkrogza/Ultimate.Hosts.Blacklist) grew up it became impossible to test the whole repository, as it takes weeks to finish. That's why we use the GitHub organization system in order to create different repository for each list that are present into [Ultimate Hosts Blacklist](https://github.com/mitchellkrogza/Ultimate.Hosts.Blacklist).

--------------------------------------------------------------------------------

# About PyFunceble

PyFunceble like [Funceble](https://github.com/funilrys/funceble) is A tool to check domains or IP availability by returning 3 possible [status](https://github.com/funilrys/PyFunceble/wiki/Columns#status): ACTIVE, INACTIVE or INVALID.

It also has been described by one of its most active user as:

> [An] excellent script for checking ACTIVE, INACTIVE and EXPIRED domain names.

If you need further informations about PyFunceble or Funceble please report to our [Wiki page](https://github.com/funilrys/PyFunceble/wiki) and/or if you don't find any answer feel free to create an issue into one of the [Dead Hosts](https://github.com/search?q=user%3Adead-hosts&type=Repositories&utf8=%E2%9C%93)'s or [Py-Funceble](https://github.com/search?utf8=%E2%9C%93&q=funceble+user%3Afunilrys&type=)'s repositories.

## About the status returned by PyFunceble

For an up to date version of this part please report to the [Status](https://github.com/funilrys/PyFunceble/wiki/Columns#status) section of our Wiki.

### ACTIVE

This status is returned when **one of the following cases** is met:

- We can extract the expiration date from `Lookup().whois()`.

  - _Please note that we don't check if the date is in the past._

- `Lookup().nslookup()` don't return `server can't find domain-name.me: NXDOMAIN`.

- `HTTOCode().get()` return one the following code `[100, 101, 200, 201, 202, 203, 204, 205, 206]`.

### INACTIVE

This status is returned when **all the following cases** are met:

- We can't extract the expiration date from `Lookup().whois()`.
- `Lookup().nslookup()` return `server can't find domain-name.me: NXDOMAIN`.

### INVALID

This status is returned when **the following case** is met:

- Domain extension has an invalid format or is unregistered in **[IANA](https://www.iana.org/domains/root/db) Root Zone Database**.

  - Understand by this that the extension **is not present into the `iana-domains-db.json` file**.
