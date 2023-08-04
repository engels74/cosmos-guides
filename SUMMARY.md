# Table of contents

* [Cosmos Guides](README.md)

## Docker & Compose Setup

* [01) Docker installation](docker-and-compose-setup/01-docker-installation.md)
* [02) Cosmos Server setup](docker-and-compose-setup/02-cosmos-server-setup.md)
* [03) QoL Docker Compose setup](docker-and-compose-setup/03-qol-docker-compose-setup.md)

## Cosmos Server setup

* [01) Initial launch of Cosmos Server](cosmos-server-setup/01-initial-launch-of-cosmos-server.md)
* [02) Initial setup of Cosmos Server](cosmos-server-setup/02-initial-setup-of-cosmos-server.md)
* [03) Cosmos hostname setup](cosmos-server-setup/03-cosmos-hostname-setup.md)
* [04) DNS Challenge setup (CF)](cosmos-server-setup/04-dns-challenge-setup-cf/README.md)
  * [04a) SSL/TLS settings](cosmos-server-setup/04-dns-challenge-setup-cf/04a-ssl-tls-settings.md)
  * [04b) SSL Wildcard setup](cosmos-server-setup/04-dns-challenge-setup-cf/04b-ssl-wildcard-setup.md)
  * [04c) Creating a DNS Zone API Key](cosmos-server-setup/04-dns-challenge-setup-cf/04c-creating-a-dns-zone-api-key.md)
* [05) Finishing hostname setup](cosmos-server-setup/05-finishing-hostname-setup.md)
* [06) Admin account setup](cosmos-server-setup/06-admin-account-setup.md)
* [07) Final Steps](cosmos-server-setup/07-final-steps.md)

## Pterodactyl Setup

* [00) Information about Pterodactyl](pterodactyl-setup/00-information-about-pterodactyl.md)
* [01) Installing Pterodactyl](pterodactyl-setup/01-installing-pterodactyl/README.md)
  * [01a) The Docker Compose example](pterodactyl-setup/01-installing-pterodactyl/01a-the-docker-compose-example.md)
  * [01b) Launching Pterodactyl](pterodactyl-setup/01-installing-pterodactyl/01b-launching-pterodactyl.md)
  * [01c) Isolating networks](pterodactyl-setup/01-installing-pterodactyl/01c-isolating-networks.md)
* [02) Creating URLs](pterodactyl-setup/02-creating-urls/README.md)
  * [02a) Create URL for pt-panel](pterodactyl-setup/02-creating-urls/02a-create-url-for-pt-panel.md)
  * [02b) Create URL for pt-wings](pterodactyl-setup/02-creating-urls/02b-create-url-for-pt-wings.md)
  * [02c) Setting up CORS](pterodactyl-setup/02-creating-urls/02c-setting-up-cors/README.md)
    * [02ca) CORS Option 1 (secure)](pterodactyl-setup/02-creating-urls/02c-setting-up-cors/02ca-cors-option-1-secure.md)
    * [02cb) CORS Option 2 (failsafe)](pterodactyl-setup/02-creating-urls/02c-setting-up-cors/02cb-cors-option-2-failsafe.md)
* [03) Setup of the Panel](pterodactyl-setup/03-setup-of-the-panel/README.md)
  * [03a) Creating the first user](pterodactyl-setup/03-setup-of-the-panel/03a-creating-the-first-user.md)
  * [03b) Setting up a location](pterodactyl-setup/03-setup-of-the-panel/03b-setting-up-a-location.md)
  * [03c) Setting up the node](pterodactyl-setup/03-setup-of-the-panel/03c-setting-up-the-node.md)
  * [03d) IP and Port allocation](pterodactyl-setup/03-setup-of-the-panel/03d-ip-and-port-allocation.md)
* [04) Connecting the Wings](pterodactyl-setup/04-connecting-the-wings/README.md)
  * [04a) Creating the config.yml](pterodactyl-setup/04-connecting-the-wings/04a-creating-the-config.yml.md)
  * [04b) Check if pt-wings work](pterodactyl-setup/04-connecting-the-wings/04b-check-if-pt-wings-work.md)
  * [04c) Final touches](pterodactyl-setup/04-connecting-the-wings/04c-final-touches.md)

## Using Pterodactyl

* [00) Overview](using-pterodactyl/00-overview.md)
* [01) Setting up a game server](using-pterodactyl/01-setting-up-a-game-server/README.md)
  * [01a) Creating a server](using-pterodactyl/01-setting-up-a-game-server/01a-creating-a-server/README.md)
    * [01aa) Core Details](using-pterodactyl/01-setting-up-a-game-server/01a-creating-a-server/01aa-core-details.md)
    * [01ab) Allocation Management](using-pterodactyl/01-setting-up-a-game-server/01a-creating-a-server/01ab-allocation-management.md)
    * [01ac) Application Feature Limits](using-pterodactyl/01-setting-up-a-game-server/01a-creating-a-server/01ac-application-feature-limits.md)
    * [01ad) Resource Management](using-pterodactyl/01-setting-up-a-game-server/01a-creating-a-server/01ad-resource-management.md)
  * [01b) Game server configuration](using-pterodactyl/01-setting-up-a-game-server/01b-game-server-configuration/README.md)
    * [01ba) Startup Configuration](using-pterodactyl/01-setting-up-a-game-server/01b-game-server-configuration/01ba-startup-configuration.md)
    * [01bb) Service Variables](using-pterodactyl/01-setting-up-a-game-server/01b-game-server-configuration/01bb-service-variables.md)
  * [01c) Final Steps](using-pterodactyl/01-setting-up-a-game-server/01c-final-steps/README.md)
    * [01ca) The Pterodactyl Terminal](using-pterodactyl/01-setting-up-a-game-server/01c-final-steps/01ca-the-pterodactyl-terminal.md)
    * [01cb) Accessing the SFTP server](using-pterodactyl/01-setting-up-a-game-server/01c-final-steps/01cb-accessing-the-sftp-server.md)
* [02) Importing new eggs](using-pterodactyl/02-importing-new-eggs/README.md)
  * [02a) Locating the egg](using-pterodactyl/02-importing-new-eggs/02a-locating-the-egg.md)
  * [02b) Downloading the egg](using-pterodactyl/02-importing-new-eggs/02b-downloading-the-egg.md)
  * [02c) Creating a Nest](using-pterodactyl/02-importing-new-eggs/02c-creating-a-nest.md)
  * [02d) Importing the egg to the nest](using-pterodactyl/02-importing-new-eggs/02d-importing-the-egg-to-the-nest.md)
* [03) Setting up a SteamCMD server](using-pterodactyl/03-setting-up-a-steamcmd-server/README.md)
  * [03a) Creating a server](using-pterodactyl/03-setting-up-a-steamcmd-server/03a-creating-a-server.md)
  * [03b) Game server configuration](using-pterodactyl/03-setting-up-a-steamcmd-server/03b-game-server-configuration/README.md)
    * [03ba) Allocation Management](using-pterodactyl/03-setting-up-a-steamcmd-server/03b-game-server-configuration/03ba-allocation-management.md)
    * [03bb) Nest Configuration](using-pterodactyl/03-setting-up-a-steamcmd-server/03b-game-server-configuration/03bb-nest-configuration.md)
  * [03c) Service Variables](using-pterodactyl/03-setting-up-a-steamcmd-server/03c-service-variables.md)
  * [03d) Final Steps](using-pterodactyl/03-setting-up-a-steamcmd-server/03d-final-steps.md)

## Troubleshooting

* [00) Overview](troubleshooting/00-overview/README.md)
  * [01) The Node shows up as offline](troubleshooting/00-overview/01-the-node-shows-up-as-offline.md)
  * [02) My Panel login page is blank](troubleshooting/00-overview/02-my-panel-login-page-is-blank.md)
