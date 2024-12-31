1. To start download Entra AD Connect from Microsoft website:[Download Microsoft Entra Connect from Official Microsoft Download Center](https://www.microsoft.com/en-us/download/details.aspx?id=47594)
![](attachments/Pasted%20image%2020241231103628.png)
2. On the **Express settings** page, click **Customize** as we do not want to use the default installation and synchronization settings.

	At **Install required components** you can change your installation location, use an existing SQL server, use an existing service account, specify sync groups or import settings. We are going to leave all the settings unchecked and click **Install**.
![](attachments/Pasted%20image%2020241231134838.png)

3. The **User sign-in** page allows us to choose a sign-in method for our synchronized users. We are going to select **Password Hash Synchronization** which will allow our used to sign into the cloud with the same password and their on-premise account.
![](attachments/Pasted%20image%2020241231135400.png)
4. Next **Connect to Azure AD with your global administrator account**. Once done you will be taken straight to the **Connect your directories** page. Ensure your forest is selected and click **Add Directory**. In the popup window select **Create new AD Account** and enter your domain administrator account information below, then click **OK**.
![](attachments/Pasted%20image%2020241231104003.png)
![](attachments/Pasted%20image%2020241231104013.png)
![](attachments/Pasted%20image%2020241231104039.png)
![](attachments/Pasted%20image%2020241231135719.png)

![](attachments/Pasted%20image%2020241231104115.png)
![](attachments/Pasted%20image%2020241231104123.png)
5. Under Domain and OU filtering it is extremely important you only sync the specified OU’s that you wish to sync otherwise you risk deleting data or user accounts which are already in Azure AD.
![](attachments/Pasted%20image%2020241231104133.png)
6. On the **Uniquely identifying your users** page I am leaving all settings as **default** and clicking next. As this is a new installation of Azure AD Connect I am going to allow Azure AD Connect to select the default recommended sync attributes for me. I will also do the same for the Filter users and devices page.
![](attachments/Pasted%20image%2020241231104139.png)
7. The **Optional features** page will lastly present any additional features you can enable. I am going to enable the **Password writeback** feature. This means if I change a user password in Azure AD, the password will write back to the on-premise directory user it is synced with, allowing user passwords to be updated in Azure AD or on-premise.
![](attachments/Pasted%20image%2020241231104147.png)
8. On the final page you can check the option **Enable staging mode**. By using staging mode you can review any changes that will occur in Azure AD once the sync is enabled without actually making the changes. With this setting you can review if the changes you are making are correct and will not have any adverse effects before going live. I am simple going to select **Install** without enabling staging mode.
![](attachments/Pasted%20image%2020241231104152.png)
![](attachments/Pasted%20image%2020241231104158.png)
![](attachments/Pasted%20image%2020241231104206.png)
![](attachments/Pasted%20image%2020241231104211.png)
![](attachments/Pasted%20image%2020241231104217.png)
![](attachments/Pasted%20image%2020241231104225.png)
![](attachments/Pasted%20image%2020241231104236.png)
![](attachments/Pasted%20image%2020241231104340.png)
![](attachments/Pasted%20image%2020241231104433.png)

Success!! 