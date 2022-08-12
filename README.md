![veeam1](./images/veeam1.jpg)
#  Veeam Hands-on Lab for Microsoft Azure
## Deploy Veeam VM
1. After you login in to the Azure portal, in the search bar type **Veeam Backup for Microsoft Azure Free Edition** and click on **Veeam Backup for Microsoft Azure Free Edition**.
![veeam127](./images/veeam127.jpg)
2. Click on the **Create** button.
![veeam128](./images/veeam128.jpg)
3. Enter the details for the virtual machine.
   `````
   Resource Group: Veeam
   Virtual machine name: Veeam
   Region: EastUS2
   Size: Standard_DS1_V2
   Username: demouser
   Password: Password.1!!
   
   `````
![veeam104](./images/veeam104.jpg)
4. Click on **Review+Create** and Click on **Create**.
![veeam105](./images/veeam105.jpg)
5. Make sure that **Your deployment is complete**.
![veeam106](./images/veeam106.jpg)
6. Once the deployment is successful, click on **go to resource** or click on the search bar and type **Virtual machine**.
![veeam107](./images/veeam107.jpg)     
7. Select the virtual machine with the name **Veeam**.
![veeam108](./images/veeam108.jpg)
8. Select the Overview and copy **Public IP Address**.
![veeam109](./images/veeam109.jpg)

## Login to Veeam VM
1. Open the new browser and paste the value copied below and replace the **IPADDRESS** with the Veeam VM IP address.
  `````
  https://IPADDRESS
  `````
![veeam2](./images/veeam2.jpg)
2. Click on the **advance**.
![veeam3](./images/veeam3.jpg)
3. Click on the **click on processed to IP**.
![veeam4](./images/veeam4.jpg)
4. Enter **demouser** as the username and use **Password.1!!** for password and click on **Login**.
![veeam5](./images/veeam5.jpg)
5. Check all the **check boxes** in the license agreement and click on **Accept** and login into the VM.
![veeam6](./images/veeam6.jpg)

## Add a Microsoft Azure account
1. Click on **Add a Microsoft Azure Account First**.
![veeam7](./images/veeam7.jpg)
2. Click on **+ Add**.
![veeam8](./images/Veeam8.jpg)
3. Enter the **Name**, **Description** and click on the **Next**.
![veeam9](./images/veeam9.jpg)
4. In the **Service Account Type** click on **Specify existing service account**.
![veeam10](./images/veeam10.jpg)
5. Copy the **TenantID**, **Application ID**, and the **Secret key** of the service principal from the environment details tab.
![veeam11](./images/veeam11.jpg)
6. Paste the copied values in the respective fields and click **Next**.
![veeam12](./images/veeam12.jpg)
7. Move to the **Summary** and click **Finish** to set up the Microsoft account.
![veeam13](./images/veeam13.jpg)

## Add the Workers to Workspace
1. Go to the **Getting Started** page and click on **Review workers configuration**.
![veeam14](./images/veeam14.jpg)
2. Click on **+ Add**.
![veeam15](./images/veeam15.jpg)
3. Click on **region** and select the region of the resource group and **Apply** and Click **Next**.
![veeam16](./images/veeam16.jpg)
4. Select the **Virtual Network**, **Subnet** and **Network security Group** and **Next**.
![veeam18](./images/veeam18.jpg)
5. Click on **Finish**.
![veeam19](./images/veeam19.jpg)
6. Click on **Profile** and **+ Add**.
![veeam20](./images/veeam20.jpg)
7. Select the correct **Region** and click on **add**, then click on **Next**.
![veeam21](./images/veeam21.jpg)
8. Move to the **worker profile** and click **Next**.
![veeam22](./images/veeam22.jpg)
9. Go to **Summary** and click **Finish**.
![veeam23](./images/veeam23.jpg)
10. Move to the **Instance** tab and verify if the instance has been created. If it is still in creating state wait till it moves to **created** state.
![veeam24](./images/veeam24.jpg)

## Add the repository
1. Move to the **Getting Started** page and click on **Add repository**.
![veeam25](./images/veeam25.jpg)
2. Click on **+ Add**.
![veeam26](./images/veeam26.jpg)
3. Enter the **Name** and **Description** and click on **Next**.
![veeam27](./images/veeam27.jpg)
4. Select the **Storage account**, **Container**, **Create new folder**, and click on **Next**.
![veeam28](./images/veeam28.jpg)
5. Select **Options** and click on **Next**.
![veeam28](./images/veeam29.jpg)
6. Click on **Summary** and **Finish**.
![veeam30](./images/veeam30.jpg)
7. Verify that the repository is created and is in **Success** state.
![veeam31](./images/veeam31.jpg)

## Create a Backup Policy for Virtual Machines
1. Move to the **Getting started** page and **Create your first backup policy**.
![veeam32](./images/veeam32.jpg)
2. Click on **+ Add**.
![veeam33](./images/veeam33.jpg)
3. Click on **Policy Info** enter the **Name** and **Description** and click **Next**.
![veeam34](./images/veeam34.jpg)
4. Select the **Azure Active Directory**, select the directory which is given in the Azure, and select the **Region**.
![veeam35](./images/veeam35.jpg)
5. Select the  **All resource**.
![veeam36](./images/veeam36.jpg)
6. Select **Protect the following resources** and click on **Browse to select the specific resource from the global list...**
![veeam37](./images/veeam37.jpg)
7. Select the checkbox for the virtual machines and click on **ADD**.
![veeam38](./images/veeam38.jpg)
8. Click on **APPLY**.
![veeam39](./images/veeam39.jpg)
9. Click on **Next**.
![veeam40](./images/veeam40.jpg)
10. Move on to **Guest Processing**, turn on the **Enable application aware snapshots**, and click on **Next**.
![veeam41](./images/veeam41.jpg)
11. Select the **Targets**, turn on the **Enable Backup**, and click **Next**.
![veeam42](./images/veeam42.jpg)
12. Select the **Schedule**, turn on the **Daily Retension**, and **Edit Daily Settings**.
![veeam43](./images/veeam43.jpg)
13. Select the **Repository** : **AzureBackup**, click on **Apply**, and Click **Next**.
![veeam44](./images/veeam44.jpg)
14. Select **Settings** click on **Next**.
![veeam45](./images/veeam45.jpg)
15. Select **Cost Estimation** and review it, once done click on **Next**.
![veeam46](./images/veeam46.jpg)
16. Select **Summary** and review it, once done click on **Finish**.
![veeam47](./images/veeam47.jpg)
17. Select the **Checkbox** for the priority, and click on **Start**.
![veeam48](./images/veeam48.jpg)
18. Verify that the backup and snapshot creation is in **success** state.
![veeam49](./images/veeam49.jpg)

## Delete the Windows Virtual Machines
1. Log in to the Azure Portal Using the credentials given in the Environment details.
2. Search for the Virtual Machine in the search tab and select the  **Veeamwindows** VM and **Delete**.
![veeam50](./images/veeam50.jpg)
3. Select the **Veeamwindows** and check the checkbox for Confirmation and click **delete**.
![veeam51](./images/veeam51.jpg)

## Restoring the Windows Virtual Machine
1. Select **Protected data** and select the restore point of the Windows VM.
![veeam52](./images/veeam52.jpg)
2. Select **Restore** and click on **Restore VM**.
![veeam54](./images/Veeam54.jpg)
3. Select **VeeamWindows** and click on **Next**.
![veeam55](./images/veeam55.jpg)
4. Go to the **Account**, **Select Account**, and **Select Azure Active Directory**. Once done, click on **Apply** and click **Next**.
![veeam56](./images/veeam56.jpg)
5. Go to the **Restore Mode** and select the **Restore to Original Location** and click on **Next**.
![veeam57](./images/veeam57.jpg)
6. Go to **Reason** provide the **Restore Reason** and click **Next**.
![veeam58](./images/Veeam58.jpg) 
7. Go to **Summary** and read through the description and click on **Restore**.
![veeam59](./images/veeam59.jpg)
8. Go to the **Session Log** and verify that restore is in success state and Verify In the Azure Portal.
![veeam60](./images/veeam60.jpg)

## Azure SQL Backup
1. Move to **Policies**, select the **Azure SQL** and **ADD+**.
![Veeam61](./images/Veeam61.jpg)
2. Go to **PolicyInfo** Enter Value For **Name** and **Description** and Click **Next**.
![veeam62](./images/veeam62.jpg)
3. Select the **Sources** Select the **Azure Active Directory** for the Source in the Region select **select region**.
![veeam63](./images/veeam63.jpg)
4. Select the **Region** and click on **ADD** and click on **Apply**.
![veeam64](./images/veeam64.jpg)
5. Click on **Select resources to protect**, select **Protect the following resources** and click on **Browse to select the specific resource from global list**.
![veeam65](./images/veeam65.jpg)
![veeam66](./images/veeam66.jpg)
6.Select the checkbox for the **VeeamSQL** and click on **ADD**, click on **Apply** and then **Next**.
![veeam67](./images/veeam67.jpg)
7.Select the **Processing Options**, move to **Use staging servers (recommended for database consistency)**, and click on **select server**.
![veeam68](./images/veeam68.jpg)
8. Select the **Browse** option for **Staging server**, and click on **+ ADD** for adding SQL account.
![veeam69](./images/veeam69.jpg)
9. Select the **AccountInfo** enter the **Name** and **Description** and click on **Next**.
![veeam70](./images/veeam70.jpg)
10. Select the Account and enter **Username** ,**Password** and click on **Next**.
![veeam71](./images/veeam71.jpg)
11. Move to **Summary** and click **Next**.
![veeam72](./images/veeam72.jpg)
12. Select **Apply** and click **Next**.
![veeam73](./images/veeam73.jpg)
13. Select **Schedule**, enable the radio button for **Daily retention** and **Edit Daily Settings**.
![veeam74](./images/veeam74.jpg)
14. Select **Repository** for AzureBackup, click on **Apply** and click **Next**.
![veeam75](./images/veeam75.jpg)
15. Go to **Settings** and click on **Next**.
![veeam76](./images/veeam76.jpg)
16. Move **Cost Estimation** and click on **Next**.
![veeam77](./images/veeam77.jpg)
17. Move to **Summary** and click on **Finish**.
![veeam78](./images/veeam78.jpg)
18. In the **Policies**, click on **Azure SQL** and check the **Priority** and click on **Start**.
![veeam79](./images/veeam79.jpg)
19. Make sure that backup is in **Success** state.
![veeam81](./images/veeam81.jpg)

## Delete the SQL Database
1. Move to the Azure Portal and Search for the **SQL database** and open the database which had **backup**.
![veeam83](./images/veeam83.jpg)
2. Select the overview of **SQL Database** and click on **Delete**.
![veeam84](./images/veeam84.jpg)
3. **TYPE THE DATABASE NAME** and click on **Delete**.
![veeam85](./images/veeam85.jpg)
**Note**: Wait until deletion is success.

## Recovery of SQL Database
1. Move to **Protect data**, select **Azure SQL** and select the **checkbox for the Azure SQL** and Click on **restore**.
![veeam82](./images/veeam82.jpg)
2. Go to the **Databases**, select the **SQLdatabase**, and click on **Next**.
![veeam86](./images/veeam86.jpg)
3. Go to **Account** and then **select the Account**. Select the Account on the right, click **Apply** and then **Next**.
![veeam87](./images/veeam87.jpg)
4. Go to **Restore Mode**, select the checkbox for **Restore to the original location** and click on **Next**.
![veeam88](./images/veeam88.jpg)
5. Go to **SQL Account**, select **Account**, click **Apply** and **Next**.
![veeam89](./images/veeam89.jpg)
6. Go to **Reason**,**enter Reason**, and click **Next**.
![veeam90](./images/veeam90.jpg)
7. Select **Summary** and click on **Restore**.
![veeam91](./images/veeam91.jpg)
8. Move to the **Session log** and verify that the Restore is in **Success** state.
![veeam92](./images/veeam92.jpg)

## Recovery of files from Linux Virtual Machine.
1. Move to **Protected data**, select the **Virtual Machines**, click on **Restore** and select **file-level-recovery**.
![veeam93](./images/veeam93.jpg)
2. Click on **Virtual Machine**, click on **change restore point** and select the restore point. Once done, click on **APPLY** and then **Next**.
![veeam94](./images/veeam94.jpg)
3. Click on **Restore**, enter **Restore reason**, and click **Next**.
![veeam95](./images/veeam95.jpg)
4. Click on **Summary** and click **Start**.
![veeam96](./images/veeam96.jpg)
5. Move to **Protected Data**, select the **Virtual machine**, select **File-Level-Recovery** and click on **FLR**.
![veeam97](./images/veeam97.jpg)
6. Select the **URL** and open in a **New Browser**.
![veeam98](./images/veeam98.jpg)
Note: If you prompted with the **Connection is not private** then click on **Advance** and click on **continue to**.
 ![veeam99](./images/veeam99.jpg)
 7. Select the proper file and folder and click on **+ Add to restore list**.
 ![veeam100](./images/veeam100.jpg)
 8. Move to **Restore List**, select the file which you want to download, and click on **Download**.
 ![veeam101](./images/veeam101.jpg)

## Backup of Azure Files
1. Navigate to **Policies > Azure Files** and Click **Add**.
![veeam110](./images/veeam110.jpg)
2. Provide the **Name** and **Description** for **Info**.
![veeam111](./images/veeam111.jpg)
3. Go to the **Sources** and In the **Account** section select the **Configure account** and select the **Azure Active Dierctory** and Select the **ResourceGroup Region**.
![veeam112](./images/veeam112.jpg)
4. Click on **Resource to protect** and select the **File Share**, click on **Apply** and click **Next**. 
![veeam113](./images/veeam113.jpg)
5. Move to **Schedule** and enable the **Daily Retention**.
![veeam114](./images/veeam114.jpg)
6. Move to **Settings** and click on **Next**.
![veeam115](./images/veeam115.jpg)
7. Move to **Cost estimation** review it and click on **Next**.
![veeam116](./images/veeam116.jpg)
8. Move to **Summary** and click on **Finish**.
![veeam117](./images/veeam117.jpg)
9. Move to **Policies**, click on **Azure Files**, check the **Priority** box, and Click on **Start**.
![veeam118](./images/veeam118.jpg)
10. Make Sure that Snapshot creation is in **Success** state.
![veeam119](./images/veeam119.jpg)

## Recovery of Azure Files
1. Move to **Protect Data**, click on **Azure Files**, check **Priority**, click on **Restore**, and **File-Level Restore**.
![veeam120](./images/veeam120.jpg)
2. Click on **Account**, select **Account***, click on **Apply** and **Next**.
![veeam121](./images/veeam121.jpg)
3. Move to **Restore Mode**, restore to **Original Location**, and click **Next**.
![veeam122](./images/veeam122.jpg)
4.Move to the **Reason**, type the **Reason** and click **Next**.
![veeam123](./images/veeam123.jpg)
5. Move to **Summary** and click on **Finish**.
![veeam124](./images/veeam124.jpg)
6. Move to **Protected Data**, click on **Azure Files**, and click on **FLR**.
![veeam129](./images/veeam129.jpg)
7. Click on the URL it will redirect to another Tab.
![veeam130](./images/veeam130.jpg)
8. Select the **files** and click on **Add to Restore**.
![veeam131](./images/veeam131.jpg)
9. Select the **Restore list**, click on the check box of file, click on **restore**, and click on **keep**.
![veeam132](./images/veeam132.jpg)
