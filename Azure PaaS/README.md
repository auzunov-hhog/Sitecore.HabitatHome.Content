# Introduction 
HabitatHome Demo and the tools and processes in it is a Sitecore&reg; solution example built using Sitecore Experience Accelerator&trade; (SXA) on Sitecore Experience Platform&trade; (XP)  following the Helix architecture principles.

This Section is dedicated to the deployment of the Habitat Home Demo project onto Azure PaaS.

# Important Notice

### License
Please read the LICENSE carefully prior to using the code in this repository
 
### Support

The code, samples and/or solutions provided in this repository are ***unsupported by Sitecore PSS***. Support is provided on a best-effort basis via GitHub issues or Slack #habitathome (see end of README for additional information).

It is assumed that you already have a working Azure tenant and associated account with necessary permissions. All normal Azure charges apply to this installation and should be carefully consdiered before deployment.

### Warranty

The code, samples and/or solutions provided in this repository are for example purposes only and **without warranty (expressed or implied)**. The code has not been extensively tested and is not guaranteed to be bug free.  

# Getting Started

## Prerequisites

- A working Azure tenant and associated account with necessary permissions.
- dev.sitecore.com credentials with permissions to download Sitecore installation files

### SSL Only
The demo is configured for **HTTPS/SSL**. Please ensure that you create an appropriate self-signed certificate

### Build / Deployment

In order to deploy the assets, you need either Visual Studio 2017 or MSBuild Tools for Visual Studio 2017.

### Custom install - before you start

The following is a list of default values / assumptions for install locations

**Project Folder**		`c:\projects\sitecore.habitathome.content\`  
**Deploy Folder**		`c:\Deploy`  

if these values are not correct you will need to edit the cake-config.json in the `\Azure PaaS\Cake` folder.  

#### The hostname habitathome.dev.local is used in the SXA Hostname (Site Grouping). 

If you do not use habitathome.dev.local you will need to modify the Host Name in 
`/sitecore/content/Habitat Sites/Habitat Home/Settings/Site Grouping/Habitat Home` after successfully deploying the site.
The Habitat Home site will not respond / render correctly until this value is modified. 

## Installation:

All installation instructions assume using **PowerShell 5.1** in _**administrative**_ mode.

### 1. Clone this repository

#### Setting Git for Long Paths

- Before cloning, you need to configure git to allow long paths, which is not the default.

`git config --system core.longpaths true`

Clone the Sitecore.HabitatHome.Content repository locally - defaults are configured for **C:\Projects\Sitecore.HabitatHome.Content**. 


- Clone 
-- **https**:	`git clone https://github.com/Sitecore/Sitecore.HabitatHome.Content.git` 
-- **ssh**:		`git clone git@github.com:Sitecore/Sitecore.HabitatHome.Content.git`

### 2. Deploy Sitecore.HabitatHome.Content

From the Azure PaaS\Cake folder

- Run **`.\build.ps1`** 

### 3. Validating deployment

# Contribute or Issues
Please post any issues on Slack Community [#habitathome](https://sitecorechat.slack.com/messages/habitathome/) channel or create an issue on [GitHub](https://github.com/Sitecore/Sitecore.HabitatHome.Content/issues). Contributions are always welcome!