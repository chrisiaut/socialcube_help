# Setup

## Get the WEGA IP address
To set up WEGA you need the IP address of the WEGA DNS Server. Head over to [https://www.socialcube.net/wega/settings](https://www.socialcube.net/wega/setting) where the IP address will be displayed.

If you haven't already done it, activate WEGA via the [Institution modules page](https://socialcube.net/institution/modules). This can only be done by the **institution admin** of your institution.

On the Wega settings page you need to enter the external IP addresses of your network, then change the filter rules as you wish and click the save button. After that the IP address of the WEGA DNS server will be displayed to you.

## Setup by platform
* [Windows 7-10](#windows)
* [Windows Server](#windowsserver)
* [Linux](#linux)

## <a id="windows"></a>Windows 7-10

### Step 1

#### Windows 10
In Windows 10, in the search box on the taskbar, type View network connections, and then select View network connections at the top of the list.

#### Windows 8
In Windows 8.1, select the Start button, start typing View network connections, and then select View network connections in the list.

#### Windows 7
In Windows 7, open Network Connections by selecting the Start button, and then selecting Control Panel. In the search box, type adapter, and then, under Network and Sharing Center, select View network connections.

### Step 2
Right-click the connection that you want to change, and then select **Properties**.
Select the **Networking tab**. Under This connection uses the following items, select either Internet Protocol Version 4 (TCP/IPv4) and then select **Properties**.

To specify a DNS server address, select **Use the following DNS server addresses**, and then, in the Preferred DNS server type the address of the primary the WEGA webfilter you received from the [WEGA Settings page](https://www.socialcube.net/wega/settings)

![Change DNS Windows](https://www.pictshare.net/461d17df4f.png)

## <a id="windowsserver"></a>Windows Server 2003 - 2016 (DNS Server role)
This should be done on the networks (last) DNS server. All external client requests should go through this server in order to protect your network.

If you have redundant DNS servers you can repeat these steps on every DNS in your network.

1. Open DNS Manager.
2. In the console tree, click the applicable DNS server.
3. On the Action menu, click Properties.
4. On the Forwarders tab, click the "Edit" button.
5. Add the IP of the WEGA DNS on the **first position**.
6. Add external DNS Servers (like google's 8.8.8.8) **after** the WEGA IP so that if WEGA ever fails the internet would still work for your users.

![Windows Server DNS forwarder settings](https://www.pictshare.net/5a26926752.jpg)


## <a id="linux"></a>Linux
This should be done on either all clients or your networks primary DNS server (router).

1. Edit the /etc/resolv.conf file and add the IP you got from the [WEGA Settings page](https://www.socialcube.net/wega/settings)

Note that if you add multiple Servers Linux won't use them in the order you wrote them but it will alternate or even use both at the same time so if you enter multiple IPs, the filter might only work in 50% of the requests.