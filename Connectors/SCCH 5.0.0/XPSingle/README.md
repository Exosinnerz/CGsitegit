# Sitecore Connect for Content Hub module for the XPSingle Environment

This template deploys Sitecore Connect for Content Hub module into a Sitecore XPSingle Environment (single all-in-one instance).

## Required Parameters

| Parameter                                 | Description
--------------------------------------------|------------------------------------------------
| sqlServerLogin                            | The name of the administrator account for the newly created Azure SQL server.
| sqlServerPassword                         | The password for the administrator account for Azure SQL server.
| msDeployPackageUrl                        | The HTTP(s) URL to a Sitecore Connect for Content Hub Web Deploy package.

## Deploying as part of Sitecore deployment

In order to configure Sitecore deployment parameters to include Sitecore Connect for Content Hub:

* Add the following snippet to the `modules` parameter:
```JSON
  {
    "name": "Sitecore.Connector.CMP",
    "templateLink": "<URL of the ARM template file for Sitecore Connect for Content Hub>",
    "parameters":
    {
      "msDeployPackageUrl": "<URL of the WDP file  for Sitecore Connect for Content Hub>"
    }
  }
```

* Configure Bootloader module according to [MODULES.md](../../MODULES.md).