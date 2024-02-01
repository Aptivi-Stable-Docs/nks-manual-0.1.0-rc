---
description: How settings works.
---

# 🔧 Kernel Settings

The kernel is extensively configurable. It allows you to customize your kernel to fit your needs across all areas, ranging from general kernel settings to networking to screensavers. It's an exciting feature!

## How it works?

The kernel configuration files are stored in the below software paths (`Paths.AppDataPath` under the `KS.Files` namespace):

* Windows: `%localappdata%\KS\`
* Linux: `~/.config/ks/`

When the kernel starts up, different configuration files are read for different purposes. The below settings paths describe the purpose and the type of each.

* Configuration: `KernelMainConfig.json`
  * Description: Stores all the main kernel configuration
  * Type: JSON
  * Location: `Paths.ConfigurationPath` under the `KS.Files` namespace
* Screensaver Configuration: `KernelSaverConfig.json`
  * Description: Stores all the screensaver configuration
  * Type: JSON
  * Location: `Paths.SaverConfigurationPath` under the `KS.Files` namespace
* Driver Configuration: `KernelDriverConfig.json`
  * Description: Stores all the driver configuration
  * Type: JSON
  * Location: `Paths.DriverConfigurationPath` under the `KS.Files` namespace
* Splash Configuration: `KernelSplashConfig.json`
  * Description: Stores all the splash configuration
  * Type: JSON
  * Location: `Paths.SplashConfigurationPath` under the `KS.Files` namespace
* Aliases: `Aliases.json`
  * Description: Stores all the user-defined aliases
  * Type: JSON
  * Location: `Paths.AliasesPath` under the `KS.Files` namespace
* Users: `Users.json`
  * Description: Stores all the users
  * Type: JSON
  * Location: `Paths.UsersPath` under the `KS.Files` namespace
* Speed Dial: `SpeedDial.json`
  * Description: Stores all the saved connections
  * Type: JSON
  * Location: `Paths.SpeedDialPath` under the `KS.Files` namespace
* Remote Debug Device Names: `DebugDevicesNames.json`
  * Description: Stores all the remote debug device names
  * Type: JSON
  * Location: `Paths.DebugDevNamesPath` under the `KS.Files` namespace
* MOTD: `MOTD.txt`
  * Description: Stores the message of the day
  * Type: Text file
  * Location: `Paths.MOTDPath` under the `KS.Files` namespace
* MAL: `MAL.txt`
  * Description: Stores the message of the day after login
  * Type: Text file
  * Location: `Paths.MALPath` under the `KS.Files` namespace
* User Groups: `UserGroups.json`
  * Description: Stores the user groups
  * Type: JSON
  * Location: `Paths.UserGroupsPath` under the `KS.Files` namespace

## Settings

<figure><img src="../../../.gitbook/assets/Beta3-092-Settings.png" alt=""><figcaption></figcaption></figure>

The kernel provides an easy-to-use tool to seamlessly configure the kernel settings. It can be easily invoked using the `settings` command. Running this command alone provides you with the normal kernel settings. The two switches will change the mode:

* `-saver`: Lets you configure the screensavers
* `-splash`: Lets you configure the splashes
* `-addonsaver`: Lets you configure the screensavers from the Extra Screensavers addon
* `-driver`: Lets you configure the kernel drivers
* `-type=configType`: Lets you configure a custom section of the kernel settings, including your mod-defined ones.

Selecting a section leads to the settings application listing all the available configuration options, which you can then set their individual options. It even allows you to save the settings if you like the current configuration, load the user settings, and find a settings entry for easier access.

### System updates and information

From the main page, you can easily check for kernel updates and check the system information right from it.

### Inner workings

You can find more information about the mechanics of the settings application by clicking on the below link.

{% content-ref url="mechanics-of-settings-app.md" %}
[mechanics-of-settings-app.md](mechanics-of-settings-app.md)
{% endcontent-ref %}

## Settings on your Shell

Additionally, you can change the kernel settings and list them using the following available commands:

* `lsconfigs`: This command allows you to list all configurations and their entries.
* `lsconfigvalues`: This command allows you to list all configuration keys and their values
* `getconfigvalue`: This command allows you to get a config value by the variable name
* `setconfigvalue`: This command allows you to set a config value by the variable name to the specified value

This feature is useful for your UESH scripts and for your quick shortcut to change your settings.

## Settings format

The settings format is out of scope for this page, so click the below link to learn more.

{% content-ref url="settings-format.md" %}
[settings-format.md](settings-format.md)
{% endcontent-ref %}

## Custom settings

The custom settings and its relationship with your mods is out of scope for this page, so click the below link to learn more.

{% content-ref url="custom-settings.md" %}
[custom-settings.md](custom-settings.md)
{% endcontent-ref %}
