# Pre-Requisites for Knowledge Mining Ready Lab

If you attended this lab as part of the Microsoft Ready event, you were provided an environment which was preloaded with all of the Azure resources you needed, including the sample dataset that is used to complete all of the activities covered in this lab. 

We are making all of this information available to you here should you wish to work on this lab in your own Azure subscription to further your understanding of the materials which were presented at Winter Ready.  In order to complete this lab, you will need to complete the following pre-reqisites before beginning.

1.	Have your own Azure account 
1.	Be familiar [Azure Portal](https://portal.azure.com)
1.	Make sure you can create Azure resources in your subscription (including paid resources).

  *Note, if your organizations policy prohibits you from creating resources in the subscription, you can use a [free subscription](https://signup.azure.com) for the purposes of this lab.*

4. Create a resource group for this workshop where you will add each of the resources you will create in the next steps.
4. **Create** an [Azure Storage Account](https://docs.microsoft.com/en-us/azure/storage/common/storage-quickstart-create-account?tabs=azure-portal).
Select Performance: *Standard* tier, not Premium
Select Account kind: *StorageV2 (general purpose v2)*
4. **Install** [Azure Storage Explorer](https://azure.microsoft.com/en-us/features/storage-explorer/)
4. You will need to **copy** two storage containers that hold the clinical trials data for this lab from a read only location to your Storage Account.
    1. **Open** Azure Storage Explorer and select *Managed Accounts*, *Add and Account...*, *Use a shared access signature (SAS) URI*. The *Display name* will autofill. Select *Next*
    1. **Add** the following *URI*, then select *Next*, then select *Connect* to add the *clinical-trials-small* container.
        ```
        https://clinicalsmall.blob.core.windows.net/clinical-trials-small?st=2020-01-31T21%3A51%3A29Z&se=2021-02-01T21%3A51%3A00Z&sp=rl&sv=2018-03-28&sr=c&sig=4%2BUe2%2B3RfbdKg9DGhqeWMUYI2oDI7nFOKrwEWpPSgdQ%3D
        ```       
    3. **Select** *Toggle Explorer* to view the Explorer. Right click on the *clinical-trials-small* Blob Container that you just connected to and select *Copy Blob Container*
        ![](images/copyblobcontainer.png)
    3. **Find** your Storage Account in the Explorer. Right click on its *Blob Containers* and select *Paste Blob Container*.
        ![](images/pasteblobcontainer.png)
    1. Confirm that the container copied successfully by checking the Activities at the bottom of the Azure Storage Explorer.
    
    2. **Repeat** the steps above to add the *diseases* storage container using the following URI to connect:
        ```
        https://clinicalsmall.blob.core.windows.net/diseases?st=2020-01-31T21%3A54%3A56Z&se=2021-02-01T21%3A54%3A00Z&sp=rl&sv=2018-03-28&sr=c&sig=SqZXItNjZI3Eu6kTPu8Poov0rYnICSQuXJ0buOWOQhk%3D
        ```
    
4.	**Create** an [Azure Search](https://docs.microsoft.com/en-us/azure/search/search-create-service-portal) resource. (A Free Tier should be sufficient for this workshop).
[Learn more](https://docs.microsoft.com/en-us/azure/search/search-sku-tier)

4.	**Create** a [Cognitive Services resource](https://docs.microsoft.com/en-us/azure/cognitive-services/cognitive-services-apis-create-account?tabs=multiservice%2Cwindows).

  *Note - You need to create the Cognitive Services resource in the same region as you Azure Search resource.*

5.  **Install** [PowerBI desktop](https://powerbi.microsoft.com/en-us/desktop/).

### Next: [Module 1: Using Azure Portal to Create Your Index - No Code Required](Module&#32;1.md)
