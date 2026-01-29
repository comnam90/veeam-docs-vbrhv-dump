---
title: "Installing oVirt KVM Plug-In in Unattended Mode"
product: "vbrhv"
doc_type: "userguide"
source_url: "https://helpcenter.veeam.com/docs/vbrhv/userguide/install_unattended.html"
last_updated: "11/18/2025"
product_version: "13.7.0.473"
---

# Installing oVirt KVM Plug-In in Unattended Mode


You can install oVirt KVM Plug-in in the unattended mode using the command line interface. The unattended installation mode does not require user interaction — the installation runs automatically in the background, and you do not have to respond to the installation wizard prompts. You can use the unattended installation mode to automate the oVirt KVM Plug-in installation process in large-scale environments.

To install oVirt KVM Plug-in in the unattended mode, use either of the following options:

* If oVirt KVM Plug-in is a part of Veeam Backup & Replication installation package, follow the instructions provided in the Veeam Backup & Replication User Guide, section [Installing Veeam Backup & Replication in Unattended Mode](https://helpcenter.veeam.com/docs/vbr/userguide/silent_mode_vbr.html?ver=13).
* If oVirt KVM Plug-in is delivered as a separate .EXE file, follow the instructions provided in this section.

Before You Begin

Before you start unattended installation, do the following:

1. Download the KVMPlugin\_13.7.0.473.exe file as described in section [Installing oVirt KVM Plug-In](install_plugin.md) (steps 1-3).
2. Check compatibility of the oVirt KVM Plug-in and Veeam Backup & Replication versions. For more information, see [System Requirements](system_requirements.md).

Installation Command-Line Syntax

Open the command prompt and run the .EXE file using the following parameters:

|  |
| --- |
| %path% /silent /accepteula /acceptthirdpartylicenses /acceptlicensingpolicy /acceptrequiredsoftware |

The following command-line parameters are used to run the setup file:

| Parameter | Required | Description |
| --- | --- | --- |
| %path% | Yes | Specifies a path to the installation .EXE file on the backup server or in a network shared folder. |
| /silent | Yes | Sets the user interface level to None, which means no user interaction is needed during installation. |
| /accepteula | Yes | Confirms that you accept the terms of the Veeam license agreement. |
| /acceptthirdpartylicenses | Yes | Confirms that you accept the license agreement for 3rd party components that Veeam incorporates. |
| /acceptlicensingpolicy | Yes | Confirms that you accept the Veeam licensing policy. |
| /acceptrequiredsoftware | Yes | Confirms that you accept the license agreements for each required software that Veeam will install. |
| /uninstall | No | Uninstalls the plug-in. |
| /repair | No | Replaces missing files and firewall rules. |

Examples

The following command installs oVirt KVM Plug-in:

|  |
| --- |
| KVMPlugin\_13.7.0.473.exe /silent /accepteula /acceptthirdpartylicenses /acceptlicensingpolicy /acceptrequiredsoftware |

The following command repairs oVirt KVM Plug-in:

|  |
| --- |
| KVMPlugin\_13.7.0.473.exe /silent /accepteula /acceptthirdpartylicenses /acceptlicensingpolicy /acceptrequiredsoftware /repair |

The following command uninstalls oVirt KVM Plug-in:

|  |
| --- |
| KVMPlugin\_13.7.0.473.exe /silent /accepteula /acceptthirdpartylicenses /acceptlicensingpolicy /acceptrequiredsoftware /uninstall |

Veeam Plug-in for OLVM and RHV provides the following status codes to report about the installation result:

| Code | Description |
| --- | --- |
| 0 | oVirt KVM Plug-in installation has successfully completed. |
| 1603 | oVirt KVM Plug-in installation has failed. |
| 3010 | oVirt KVM Plug-in installation has successfully completed. The backup server requires rebooting. |

|  |
| --- |
| Tip |
| For detailed logs of the oVirt KVM Plug-in installation, navigate to the Program Data\Veeam\Setup\Temp\ folder on the backup server and view the following files:   * VeeamPluginBootstrap.log * KVMPluginSetup.log * KVMPluginUISetup.log * KVMPluginProxySetup.log |


