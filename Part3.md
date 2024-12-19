# Active Directory Project: Part 3 - Installing and Configuring Sysmon and Splunk
## Step 1: Set Up NAT Network in VirtualBox
1. Open VirtualBox and click on **Tools** > **Network**.
2. Select **NAT Network** and click **Create**.
3. Name the network (e.g., `ad_project`) and set the IPv4 prefix to `192.168.10.0/24`.
4. Enable DHCP and click **Apply**.
- ![NAT](https://i.imgur.com/TvD4DHh.png)
5. For each virtual machine (Splunk server, Active Directory server, Windows, Kali):
    - Go to **Settings** > **Network**.
    - Change **Attached to** to **NAT Network** and select the created network (`ad_project`).
- ![NAT](https://i.imgur.com/q42HUie.png)
