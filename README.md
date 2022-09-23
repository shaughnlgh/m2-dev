# Magento 2 Developer Setup Guide

The purpose of this guide is to help setup a Magento 2 environment easily and to ensure faster setups when onboarding 
new developers within your project. The intention for this is to help others that may have experieced issues before and
to show an alternative setup that may have not been considered before.

There are many great tools / libs that we will use in order to try and streamline the installation/setup proces.

This guide has been written for MacOS users, however can be adapted to cater for other OS's users as well. Having said 
this, we will assume:
- you are a MacOS user,
- you know some Docker basics,
- you are familiar with using terminal or similar,
- you have some basic git knowledge,
- and you are setting up a new or existing Magento 2 project.

## [1. Environment setup](docs/enviroment-setup.md)

## [2. PHPStorm configurations](docs/phpstorm-config.md)

## [3. Project CI/CD Pipelines - TBD](docs/project-pipelines-gitlab.md)

## [4. Module CI/CD Pipelines - TBD](docs/module-pipelines-gitlab.md)


## Useful Links:

Magento development guide - <https://developer.adobe.com/commerce/php/development/>

Warden guide - <https://docs.warden.dev/>

Everything Magento 2 - <https://github.com/run-as-root/awesome-magento2>


## Notes:

I am looking at potentially adding unit testing configs to the `PHPStorm configurations` doc as soon as I get around to
setting it up. I prefere running the unit tests in CLI, but some may be more confortable running it from PHPStorm.

I also currently run my CI testing pipelines on individual modules rather than the whole project, and setting up 
pipelines on GitLab vs GitHub vs BitBucket is very different, so will need to find a way to set those out nicely. I 
would also like to see if its worth while switching to / implementing 
<https://github.com/run-as-root/gitlab-pipeline-templates>.

Please feel free to contribute or update where necessary.