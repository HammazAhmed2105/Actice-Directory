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
---

## Step 2: Configure Static IP for Splunk Server
1. On the Splunk virtual machine, open the terminal and type:
    ```bash
    sudo nano /etc/netplan/00-installer-config.yaml
    ```
2. Modify the configuration:
    ```yaml
    dhcp4: false
    addresses: [192.168.10.10/24]
    gateway4: 192.168.10.1
    nameservers:
        addresses: [8.8.8.8]
    ```
3. Save and apply changes:
    ```bash
    sudo netplan apply
    ```
4. Verify the IP:
    ```bash
    ip a
    ```
5. Test connectivity by pinging Google:
    ```bash
    ping google.com
    ```

---

## Step 3: Download Splunk Enterprise
1. On the host machine, go to [splunk.com](https://www.splunk.com) and log in or sign up.
2. Navigate to **Products** > **Free Trials and Downloads** > **Splunk Enterprise**.
3. Select **Linux** and download the `.deb` file.
4. Save the file to a directory (e.g., `Active_Directory_Project`).

---

## Step 4: Install Guest Additions in VirtualBox
1. On the Splunk VM, install Guest Additions:
    ```bash
    sudo apt-get install virtualbox-guest-additions-iso
    ```
2. Reboot the virtual machine:
    ```bash
    sudo reboot
    ```
3. Add the user to the `vboxsf` group:
    ```bash
    sudo adduser <username> vboxsf
    ```

---

## Step 5: Mount Shared Folder
1. Create a directory for the shared folder:
    ```bash
    mkdir ~/share
    ```
2. Mount the shared folder:
    ```bash
    sudo mount -t vboxsf -o uid=1000,gid=1000 <shared-folder-name> ~/share
    ```
3. Verify files in the shared folder:
    ```bash
    ls -la ~/share
    ```

---

## Step 6: Install Splunk
1. Navigate to the shared folder and install Splunk:
    ```bash
    sudo dpkg -i <splunk-installer>.deb
    ```
2. Change to the Splunk directory:
    ```bash
    cd /opt/splunk/bin
    ```
3. Start Splunk:
    ```bash
    sudo ./splunk start
    ```
4. Accept the license agreement and set an admin username and password.

---

## Step 7: Enable Splunk on Boot
1. Enable Splunk to start on boot:
    ```bash
    sudo ./splunk enable boot-start -user splunk
    ```
2. Restart the virtual machine and verify Splunk starts automatically.

---
