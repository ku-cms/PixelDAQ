# KU DAQ System

This repository contains code that will be used to moniter the Front-End Drivers for the CMS detector. These instructions may differ for iOS users.

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
*   `kinit [username]@cern.ch`
*   `ssh -Y [username]@lxplus.cern.ch` 
*   Use your lxplus password.
*   `ssh -Y [username]@cmsusr`
*   Use your cmsusr password.

#### Method 2
Only for Mac users. Works for windows users as well, but basically comes out to be same as the previous method.

In your console use:
*  `kinit [username]@cern.ch`
*  `ssh -tt -Y [username]@lxplus.cern.ch ssh -tt -Y [username]@cmsusr`
*  Use your cmsusr password.


#### Changing Password
If this is your first time of accessing your `cmsusr`, command to change your password after logging in. Enter the following command in your console:

`kpasswd`

You will be prompted to enter your current/temporary password and then for your desired password.

### Accessing DAQ Host
#### Method 1: 

kinit caleb@CERN.CH 

ssh -Y caleb@lxplus.cern.ch 

ssh -Y local14chstack@fpixp1hc 

Use this password: localDAQ$ 

#### Method 2: 

kinit caleb@CERN.CH 

ssh -tt -Y caleb@lxplus.cern.ch ssh -tt -Y local14chstack@fpixp1hc 

Use this password: localDAQ$ 
