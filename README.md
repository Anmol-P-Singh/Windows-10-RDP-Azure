<p align="center">
  <img width="403" height="65" alt="image" src="https://github.com/user-attachments/assets/95416299-a06d-42a8-a81f-ad82de7cd432" />
</p>

# How to Access Windows 10 Remote Desktop on Azure VM with Public IP

Hey there! Welcome to this tutorial. I’ll walk you through the entire process of setting up and connecting to a **Remote Desktop (RDP)** session on an **Azure Virtual Machine** using its **Public IP address**. By the end of this guide, you'll be able to access your Azure VM from anywhere.

---

## Prerequisites

Before we jump in, here’s what you’ll need:

- A **Microsoft Azure** account (if you don’t have one, create it [here](https://azure.microsoft.com/))
- Basic knowledge of **Azure Virtual Machines**
- An **RDP client** on your computer (e.g., **Windows Remote Desktop** or **Microsoft Remote Desktop for macOS**)

---

## Operating Systems Used

- **Microsoft Windows 11** (version 21H2)

---

## Installation Steps

### Step 1: Create a Resource Group

1. In the Azure portal, use the search bar to find **Resource Groups**.
2. Click on **+ Create** to start the process of creating your new resource group.

   ![Create Resource Group](https://github.com/user-attachments/assets/aac66d07-7c50-43fa-882d-53fd0e805968)

3. Give your resource group a name (for example, **MyResourceGroup**). 
4. Pick a region that works best for you. You’ll need to remember this when creating your virtual machine.
5. Click **Review + Create**, then hit **Create** when you're ready.

   ![Resource Group Creation](https://github.com/user-attachments/assets/fc25e85e-ebaf-4e1d-bd08-47c19af5b155)

---

### Step 2: Create a Virtual Machine

1. Once your resource group is created, search for **Virtual Machines** in the Azure portal and click on **+ Create**.

   ![Public IP Address](https://github.com/user-attachments/assets/f54684c3-79b2-4c8d-9d6d-66dabe628d27)

2. Select the resource group you just created. This keeps everything organized!

   ![Create Virtual Machine](https://github.com/user-attachments/assets/0ce8f331-8400-4b75-be9c-54a386ab7d50)
   ![Select Resource Group](https://github.com/user-attachments/assets/41187d82-4c1c-4010-83f1-e928b2c2da68)

3. For the **VM Name**, you can name it the same as your resource group, but I recommend picking something a little different so it’s easier to identify.

4. Choose the **Region** that matches your resource group to save on data transfer costs and improve performance.

5. For the **Image**, choose **Windows 10 Pro**.

   ![VM Configuration](https://github.com/user-attachments/assets/3938b3a5-e888-4157-8954-ca21be560de6)

6. Pick a **VM size** with at least **2 vCPUs** for optimal performance.
7. **Create a Username and Password**—these will be used to log in to your remote desktop.

---

<img width="482" height="202" alt="image" src="https://github.com/user-attachments/assets/900ff104-b2c4-49cd-b4f7-cc2c66bbf25a" />

- Don't forget to check the licensing box.
- Once you’re done, click **Next** to go to the **Networking** tab.

### Step 3: Networking and IP Address

1. In the **Networking** section, make sure a **Public IP** is selected. This allows you to connect to your VM from anywhere.

   ![Networking](https://github.com/user-attachments/assets/f08b1177-cb3c-46d4-a9ef-7d3ee741b2db)

2. Ensure that the **Network Security Group (NSG)** allows **RDP (Port 3389)** traffic. This is critical for remote connections.

   - If it’s not set up, you can add a rule to allow inbound RDP traffic on **Port 3389**.

---

### Step 4: Review and Create the VM

1. After you’ve configured everything, click **Review + Create** to review your settings.

   <img width="495" height="83" alt="image" src="https://github.com/user-attachments/assets/33f795d2-9d35-4f2a-89ea-e9e2eecc30da" />

2. Once you’re happy with your settings, click **Create** to deploy your VM.

---

### Step 5: Connect to Your Virtual Machine Using RDP

1. Once your VM is deployed, head over to the **Overview** page in the Azure portal.
2. Copy the **Public IP address** of your VM—you’ll need it to connect remotely.
   
   ![Public IP](https://github.com/user-attachments/assets/f3451d6d-a074-47b6-a66d-d13cd87ca8d0)

3. Open **Remote Desktop Connection** on your computer (just hit the Start menu, type 'Remote Desktop' in the search bar, and click on the app).

   ![Remote Desktop App](https://github.com/user-attachments/assets/e0ac2082-2a2d-490f-8a6e-410bab7391a4)

4. In the **Remote Desktop Connection** window, paste the **Public IP address** of your VM and click **Connect**.

   ![Connect to VM](https://github.com/user-attachments/assets/cb6ccc33-faee-4244-be9f-d35509b6a881)

5. When prompted, enter the **username** and **password** you created during the VM setup. If you don’t see the option, click **More Choices** and select **Different User**.

   ![Login](https://github.com/user-attachments/assets/b01468b3-296b-424b-bf1d-c12a15bbb62b)

6. Finally, **click Yes** on the prompt that appears after pressing Enter to accept the connection.

---

## Congratulations

Congrats! 🎉 You’ve just set up your **Windows 10 Azure VM** and connected to it via **Remote Desktop** using the **Public IP address**. Now you can access and manage your VM from anywhere.

---

