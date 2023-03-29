# KU DAQ System

This repository contains code that will be used to monitor the Front-End Drivers for the CMS detector. These instructions may differ based on your OS.

## Reminders Before Your Move Forward:


*   Setup your lxplus account.
*   Setup your CMS account.
*   Download Firefox.


# Accessing the Network

### Installing Putty
Putty is a clinet-program for the SSH, Telnet, and Rlogin protocol. These protocols are used to run a remote sessions from your computer. We will be using Putty as part of our port-forwarding to access the remote computers on CMS Cluster.

Putty can be downloaded [here](https://www.putty.org/)

Follow the steps in the "How to tune your PuTTY configuration for accessing the .CMS or .CMS904 networks" from the [Cluster User Guide Page](https://twiki.cern.ch/twiki/bin/viewauth/CMS/ClusterUsersGuide).

Make sure you can hop on to your lxplus account.

### Loging into your CMS User (cmsusr.cern.ch).

#### Method 1
First two steps are for Mac users. Windows user should use Putty to login to lxplus. Preferable for windows.

In your console use:
```
kinit [username]@cern.ch
ssh -Y [username]@lxplus.cern.ch 
<lxplus password>
ssh -Y [username]@cmsusr
<cmsusr password>
```
#### Method 2
Only for Mac users. Works for windows users as well, but basically comes out to be same as the previous method.

In your console use:
```
kinit [username]@cern.ch
ssh -tt -Y [username]@lxplus.cern.ch ssh -tt -Y [username]@cmsusr
<cmsusr password>
```

#### Changing Password
If this is your first time of accessing your `cmsusr`, command to change your password after logging in. Enter the following command in your console:
```
kpasswd
```

You will be prompted to enter your current/temporary password and then for your desired password.

### Accessing DAQ Host
#### Method 1: 
```
kinit [username]@CERN.CH 
ssh -Y [username]@lxplus.cern.ch 
ssh -Y local14chstack@fpixp1hc 
```

#### Method 2: 
```
kinit [username]@CERN.CH 
ssh -tt -Y [username]@lxplus.cern.ch ssh -tt -Y local14chstack@fpixp1hc 
```
Note: please contact someone working on CMS pixel DAQ for the password to login to fpixp1hc.

# Helpful Links



*   [Operating the FPix test-setup](https://twiki.cern.ch/twiki/bin/viewauth/CMS/14ChannelStack )
*   [Pixel Online Software](https://gitlab.cern.ch/cmspops/pos )
*   [Pixel Online Software Installation](https://twiki.cern.ch/twiki/bin/viewauth/CMS/PixelOnlineSoftwareInstallation)
*   [Pixel Remote Connections](https://twiki.cern.ch/twiki/bin/view/CMS/PixelRemoteConnections )
*   [Pixel Infrastructure](https://twiki.cern.ch/twiki/bin/view/CMS/PixelInfrastructure)
*   [.CMS Cluster user's guide](https://twiki.cern.ch/twiki/bin/viewauth/CMS/ClusterUsersGuide )
*   [FED Software](https://gitlab.cern.ch/cmspos/FecSoftware )
*   [Pixel DAQ Info](https://github.com/ku-cms/PixelDAQ )
*   [Git Info](https://github.com/caleb-james-smith/git-commands )
*   [Port forwarding for Windows using Putty](https://sysnews.ma.ic.ac.uk/ssh/port-forwarding-for-Windows-using-PuTTY.html )
