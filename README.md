# Watch Me Build The Lab Here
https://www.loom.com/share/5fc6613df973410d814bf1213bb397bc

# Provisioning a virtual-machine for Actve Directory on AWS
A hands-on lab demonstrating the setup and configuration of a Virtual Machine  for Active Directory on AWS
# Building a Windows Virtual Machine / EC2 Instance on AWS

This guide walks through the process of launching a Windows-based EC2 instance using the AWS Management Console.

---


## Step 1: Access the EC2 Service

1. If EC2 is not visible under *Recently visited*, type **EC2** into the search bar and select it.

---

## Step 2: Launch a New Instance
![image alt](https://github.com/glenpagesr-dev/virtual-machine/blob/de0a375a6c6786a98759c812968a7f3727ca9afa/VM%20Instance%20EC2.png)
1. Click **Launch instance**.
2.  Under **Application and OS Images (AMI)**, select a **Windows** operating system (such as *Microsoft Windows Server 2022 Base*).
![image alt](https://github.com/glenpagesr-dev/virtual-machine/blob/f170461ce55ee9f3c8b42a7fad0b9a909bdfe9c2/VM%20widows%20OS.png)
---

## Step 3: Choose an Instance Type
![image aly](https://github.com/glenpagesr-dev/virtual-machine/blob/4705d4d005d0d4a8a00ecdf3f2cedd5aa7256c51/VM%20instance%20type.png)
1. Scroll to the **Instance type** section.
2. Select an instance type that provides balanced performance, such as:
   - `t3.xlarge` (4 vCPUs, 16 GiB memory)

---

## Step 4: Configure a Key Pair
![image alt](https://github.com/glenpagesr-dev/virtual-machine/blob/2c2d3707efeabae267be522be02ab05be55f8fc0/VM%20keypair.png)

1. In the **Key pair (login)** section, choose an existing key pair or create a new one.
2. If creating a new key pair:
   - Provide a name (for example: `WindowsTest`).
   - Download and securely store the private key file (`.pem`).

> **Important:** You will need this key pair to retrieve the Windows administrator password and connect to the instance.

---

## Step 5: Review and Launch
![image alt](https://github.com/glenpagesr-dev/virtual-machine/blob/871d18ec57c01f924a29fb3599eab8e652fdb2c6/VM%20Launch%20Instance.png)
1. Leave the remaining settings at their default values unless specific networking, storage, or security configurations are required.
2. Click **Launch instance** to begin provisioning.

---

## Step 6: Verify Instance Status

1. After launch, select the **instance ID** to view details.
2. Wait for the **Instance state** to change from `Initializing` to `Running`.
3. Confirm that both **Status checks** have passed.

---

## Next Steps: Connecting to the Instance
![image alt](https://github.com/glenpagesr-dev/virtual-machine/blob/be3f9e649e6413a6e3588dc6f4ce24e3d535f339/VM%20Connect.png)

- Decrypt the Windows administrator password using your key pair.
- Connect using **Remote Desktop Protocol (RDP)** and the instance’s public IPv4 address.
