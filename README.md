<p align="center">
  <img width="403" height="65" alt="image" src="https://github.com/user-attachments/assets/95416299-a06d-42a8-a81f-ad82de7cd432" />
</p>

# Accessing Windows 10 Remote Desktop on Azure VM via IP address

Welcome! This tutorial will walk you through the process of setting up and connecting to a **Remote Desktop (RDP)** session on an **Azure Virtual Machine** using its **Public IP address**. By the end, you'll be able to access your Azure VM from anywhere!

---

## Prerequisites

Before we begin, you’ll need the following:

- A **Microsoft Azure** account
- Basic knowledge of **Azure Virtual Machines**
- An **RDP client** on your computer (e.g., **Windows Remote Desktop**, or **Microsoft Remote Desktop for macOS**)

---

## Operating Systems Used

- **Microsoft Windows 11** (version 21H2)

---

## Installation Steps

### Step 1: Create a Resource Group

1. In the Azure portal, search for **Resource Groups** using the search bar.
2. Click on **+ Create** to start the process of creating a new resource group.

   ![Create Resource Group](https://github.com/user-attachments/assets/aac66d07-7c50-43fa-882d-53fd0e805968)

3. Give your resource group a name (e.g., **MyResourceGroup**). 
4. Select a region that works best for you. Make sure to note down the region, as you’ll need it when creating your virtual machine.
5. Click **Review + Create**, then hit **Create** when you're ready.

   ![Resource Group Creation](https://github.com/user-attachments/assets/fc25e85e-ebaf-4e1d-bd08-47c19af5b155)

---

### Step 2: Create a Virtual Machine

1. Once your resource group is created, search for **Virtual Machines** in the Azure portal and click on **+ Create**.

   ![Public IP Address](https://github.com/user-attachments/assets/f54684c3-79b2-4c8d-9d6d-66dabe628d27)


2. Select the resource group you just created. This will help keep everything organized.

   ![Create Virtual Machine](https://github.com/user-attachments/assets/0ce8f331-8400-4b75-be9c-54a386ab7d50)
   ![Select Resource Group](https://github.com/user-attachments/assets/41187d82-4c1c-4010-83f1-e928b2c2da68)

3. For the **VM Name**, you can use the same name as the resource group, but it’s a good idea to pick something distinct so that it's easier to identify.

4. Choose the same **Region** for the VM as the resource group to reduce data transfer costs, improve performance, and make management easier.

5. For **Image**, select **Windows 10 Pro**.

   ![VM Configuration](https://github.com/user-attachments/assets/3938b3a5-e888-4157-8954-ca21be560de6)

6. Choose a **VM size**. Select a size with at least **2 vCPUs** for optimal performance.
7. Creat a **Username and Password** they will be used to login into Remote desktop.
---

<img width="482" height="202" alt="image" src="https://github.com/user-attachments/assets/900ff104-b2c4-49cd-b4f7-cc2c66bbf25a" />

- Don't forget to check the licensing box.
- click next to networking.

### Step 3: Networking and IP address

1. In the **Networking** section, ensure that a **Public IP** is selected. This will allow you to connect to your VM remotely.

<img width="858" height="394" alt="image" src="https://github.com/user-attachments/assets/f08b1177-cb3c-46d4-a9ef-7d3ee741b2db" />


2. Make sure the **Network Security Group (NSG)** allows **RDP (Port 3389)** traffic. This is essential for connecting via Remote Desktop.

   - If it’s not set up, you can add a rule to allow inbound RDP traffic (Port 3389).

---

### Step 4: Review and Create the VM

1. After configuring your VM and networking settings, click **Review + Create** to review your selections.

   <img width="495" height="83" alt="image" src="https://github.com/user-attachments/assets/33f795d2-9d35-4f2a-89ea-e9e2eecc30da" />

2. When you’re satisfied, click **Create** to deploy the VM.

---

### Step 5: Connect to Your Virtual Machine Using RDP

1. Once your VM is deployed, navigate to the **Overview** page of your VM in the Azure portal.
2. Copy the **Public IP address** of your VM. You’ll use this to connect remotely.
   

3. Open **Remote Desktop Connection** on your local computer (type **mstsc** in the Run dialog on Windows).
4. In the **Remote Desktop Connection** window, paste the **Public IP address** of your VM and click **Connect**.
5. When prompted, enter the **username** and **password** you created during the VM setup.

---

## Troubleshooting

If you’re having trouble connecting, here are a few things to check:

- Ensure that your **Public IP** address is correctly assigned and static.
- Make sure that **Port 3389** is open in your **Network Security Group** to allow RDP traffic.
- If you're still having issues, try restarting your VM or check the **Azure firewall settings**.

---

## Conclusion

Congratulations, you've successfully set up your **Windows 10 Azure VM** and connected via **Remote Desktop** using a **Public IP address**! Now you can access and manage your VM remotely with ease.

If you found this guide helpful or need further assistance, feel free to reach out by opening an issue. I'd love to hear how it worked for you!

---

## License

This project is licensed under the MIT License. See the [LICENSE.md](LICENSE.md) file for more details.

---

Thanks for following along, and happy coding! 😊
