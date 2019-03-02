# Windows

## Creating a secure USB Drive for installation

### Format / Clear USB Drive using Powershell (no third party utilities)

* List all disks

`Get-Disk`

* Clear USB Drive after determining disk number
  * Note: These commands assume that X is the disk you want to clear

Either command option will result in the same result, two different methods listed below

`Clear-Disk -Number X -RemoveData`

`Get-Disk X | Clear-Disk -RemoveData`


## Registry Tweaks

### disable_win10_foistware.reg
* What it does
  * This tweak needs to be applied before a fresh install of Windows receives an Internet connection, and will prevent the Windows Store from installing apps such as Candy Crush Saga, etc.
* Sources
  * Advice from Will Dormann on Twitter https://twitter.com/wdormann/status/947918699754868736 
  * Original Gist link https://gist.github.com/wdormann/49f1807431b0d5b5cd151337e6478f20
  * All credit to Will Dormann with this find, this is a just a copy of the same registry tweak copied over here.

### Turn_Off_AutoPlay.reg
* What it does
  * Personally I don't trust Windows to do the right thing with Autoplay. I'd prefer to manually browse the contents and run anything as needed. I also don't want someone to insert a USB drive without my permission and have it AutoPlay.
* Local Policy (Alternative to Registry)
  * Can be set as a Local Policy following this guide from HowToGeek http://www.howtogeek.com/236241/how-to-enable-disable-and-customize-autoplay-in-windows-10/ 
* Sources
  * Registry Tweak from TenForums http://www.tenforums.com/tutorials/7119-autoplay-turn-off-windows-10-a.html

### UAC_Always_Notify.reg
* Advice from SwiftOnSecurity on Twitter https://decentsecurity.com/#/securing-your-computer/ 
* Follow these instructions to set UAC to the highest option, "Always notify me." Anything less allows any malware to instantly elevate to administrator level permissions. UAC isn't magic, but it's a layer you want to use.
* Registry Tweak from TenForums https://www.tenforums.com/tutorials/3577-change-user-account-control-uac-settings-windows-10-a.html

### Disable_OneDrive_Integration.reg
* OneDrive is annoying.
* Can be set as a Local Policy following this guide from HowToGeek https://www.howtogeek.com/225973/how-to-disable-onedrive-and-remove-it-from-file-explorer-on-windows-10/
* Registry Tweak from TenForums https://www.tenforums.com/tutorials/16278-enable-disable-onedrive-integration.html


### Specify_Ultimate_Performance_power_plan.reg
* Requires Windows 10 build 17083 and above
* Instead of adjusting the High Performance default plan with settings such as Never let Hard Disk sleep and disabling Hibernate, just use the Ultimate Performance plan which solves these things.
* Registry Tweak from TenForums https://www.tenforums.com/tutorials/91744-specify-default-active-power-plan-windows-10-a.html 

### Disable_Automatic_sign-in_after_Windows_Update_reestart.reg
* Requires Windows 10 build 17093 and above
* Prevents apps like Firefox, Chrome, etc from relaunching after a reboot
* Registry Tweak from TenForums https://www.tenforums.com/tutorials/49963-use-sign-info-auto-finish-after-update-restart-windows-10-a.html#option4 


# Linux
