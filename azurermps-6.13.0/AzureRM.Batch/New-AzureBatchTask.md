---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2B4BFDDA-9721-42E6-84E1-A209CB782954
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchTask.md
ms.openlocfilehash: a081e6da07557033430033adc8ef28cb4b63da8c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588588"
---
# <span data-ttu-id="71cd6-101">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="71cd6-101">New-AzureBatchTask</span></span>

## <span data-ttu-id="71cd6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71cd6-102">SYNOPSIS</span></span>
<span data-ttu-id="71cd6-103">Bir iş altında toplu görev oluşturur.</span><span class="sxs-lookup"><span data-stu-id="71cd6-103">Creates a Batch task under a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71cd6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="71cd6-104">SYNTAX</span></span>

### <span data-ttu-id="71cd6-105">JobId_Single (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="71cd6-105">JobId_Single (Default)</span></span>
```
New-AzureBatchTask -JobId <String> -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>]
 [-AuthenticationTokenSettings <PSAuthenticationTokenSettings>] [-UserIdentity <PSUserIdentity>]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-OutputFile <PSOutputFile[]>]
 [-ExitConditions <PSExitConditions>] [-ContainerSettings <PSTaskContainerSettings>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71cd6-106">JobId_Bulk</span><span class="sxs-lookup"><span data-stu-id="71cd6-106">JobId_Bulk</span></span>
```
New-AzureBatchTask -JobId <String> [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71cd6-107">JobObject_Bulk</span><span class="sxs-lookup"><span data-stu-id="71cd6-107">JobObject_Bulk</span></span>
```
New-AzureBatchTask [-Job <PSCloudJob>] [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71cd6-108">JobObject_Single</span><span class="sxs-lookup"><span data-stu-id="71cd6-108">JobObject_Single</span></span>
```
New-AzureBatchTask [-Job <PSCloudJob>] -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>]
 [-AuthenticationTokenSettings <PSAuthenticationTokenSettings>] [-UserIdentity <PSUserIdentity>]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-OutputFile <PSOutputFile[]>]
 [-ExitConditions <PSExitConditions>] [-ContainerSettings <PSTaskContainerSettings>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71cd6-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="71cd6-109">DESCRIPTION</span></span>
<span data-ttu-id="71cd6-110">**New-AzureBatchTask** cmdlet 'ı, *JobId* parametresi veya *iş* parametresi tarafından belirtilen işin altında bir Azure toplu işlemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="71cd6-110">The **New-AzureBatchTask** cmdlet creates an Azure Batch task under the job specified by the *JobId* parameter or the *Job* parameter.</span></span>

## <span data-ttu-id="71cd6-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="71cd6-111">EXAMPLES</span></span>

### <span data-ttu-id="71cd6-112">Örnek 1: toplu görev oluşturma</span><span class="sxs-lookup"><span data-stu-id="71cd6-112">Example 1: Create a Batch task</span></span>
```
PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
```

<span data-ttu-id="71cd6-113">Bu komut, iş-000001 KIMLIĞI olan işin altında KIMLIK Task23 olan bir görev oluşturur.</span><span class="sxs-lookup"><span data-stu-id="71cd6-113">This command creates a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="71cd6-114">Görev belirtilen komutu çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="71cd6-114">The task runs the specified command.</span></span>
<span data-ttu-id="71cd6-115">$Context değişkenine bağlam atamak için **Get-AzureRmBatchAccountKeys** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="71cd6-115">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="71cd6-116">Örnek 2: toplu görev oluşturma</span><span class="sxs-lookup"><span data-stu-id="71cd6-116">Example 2: Create a Batch task</span></span>
```
PS C:\> $autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
PS C:\> $userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
PS C:\>Get-AzureBatchJob -Id "Job-000001" -BatchContext $Context | New-AzureBatchTask -Id "Task26" -CommandLine "cmd /c echo hello > newFile.txt" -UserIdentity $userIdentity -BatchContext $Context
```

<span data-ttu-id="71cd6-117">Bu komut, **Get-AzureBatchJob** cmdlet 'ini kullanarak 000001 kimliğine sahip olan toplu işlemi alır.</span><span class="sxs-lookup"><span data-stu-id="71cd6-117">This command gets the Batch job that has the ID Job-000001 by using the **Get-AzureBatchJob** cmdlet.</span></span>
<span data-ttu-id="71cd6-118">Komut bu işi ardışık düzen işlecini kullanarak geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="71cd6-118">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="71cd6-119">Komut, iş altında KIMLIK Task26 olan bir görev oluşturur.</span><span class="sxs-lookup"><span data-stu-id="71cd6-119">The command creates a task that has the ID Task26 under that job.</span></span>
<span data-ttu-id="71cd6-120">Görev, yükseltilmiş izinleri kullanarak belirtilen komutu çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="71cd6-120">The task runs the specified command by using elevated permissions.</span></span>

### <span data-ttu-id="71cd6-121">Örnek 3: ardışık düzeni kullanarak belirtilen işe görev koleksiyonu ekleme</span><span class="sxs-lookup"><span data-stu-id="71cd6-121">Example 3: Add a collection of tasks to the specified job by using the pipeline</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> Get-AzureBatchJob -Id "Job-000001" -BatchContext $Context | New-AzureBatchTask -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="71cd6-122">İlk komut, **Get-AzureRmBatchAccountKeys** kullanarak contosobatchaccount adlı toplu hesap için hesap anahtarlarına bir nesne başvurusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="71cd6-122">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="71cd6-123">Komut bu nesne başvurusunu $Context değişkenine depolar.</span><span class="sxs-lookup"><span data-stu-id="71cd6-123">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="71cd6-124">Sonraki iki komut, New-Object cmdlet 'ini kullanarak **Ince görev** nesneleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="71cd6-124">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="71cd6-125">Komutlar $Task 01 ve $Task 02 değişkenlerinde görevleri depolar.</span><span class="sxs-lookup"><span data-stu-id="71cd6-125">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>
<span data-ttu-id="71cd6-126">Son komutu, **Get-AzureBatchJob** kullanarak, 000001 kimliğine sahip olan toplu işlemi alır.</span><span class="sxs-lookup"><span data-stu-id="71cd6-126">The final command gets the Batch job that has the ID Job-000001 by using **Get-AzureBatchJob**.</span></span>
<span data-ttu-id="71cd6-127">Ardından komut bu işi ardışık düzen işlecini kullanarak geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="71cd6-127">Then the command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="71cd6-128">Komut bu iş altında bir görev koleksiyonu ekler.</span><span class="sxs-lookup"><span data-stu-id="71cd6-128">The command adds a collection of tasks under that job.</span></span>
<span data-ttu-id="71cd6-129">Komut, $Context depolanan bağlamı kullanır.</span><span class="sxs-lookup"><span data-stu-id="71cd6-129">The command uses the context stored in $Context.</span></span>

### <span data-ttu-id="71cd6-130">Örnek 4: belirtilen işe görevler koleksiyonu ekleme</span><span class="sxs-lookup"><span data-stu-id="71cd6-130">Example 4: Add a collection of tasks to the specified job</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> New-AzureBatchTask -JobId "Job-000001" -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="71cd6-131">İlk komut, **Get-AzureRmBatchAccountKeys** kullanarak contosobatchaccount adlı toplu hesap için hesap anahtarlarına bir nesne başvurusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="71cd6-131">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="71cd6-132">Komut bu nesne başvurusunu $Context değişkenine depolar.</span><span class="sxs-lookup"><span data-stu-id="71cd6-132">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="71cd6-133">Sonraki iki komut, New-Object cmdlet 'ini kullanarak **Ince görev** nesneleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="71cd6-133">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="71cd6-134">Komutlar $Task 01 ve $Task 02 değişkenlerinde görevleri depolar.</span><span class="sxs-lookup"><span data-stu-id="71cd6-134">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>
<span data-ttu-id="71cd6-135">Son komut $Task $Task 01 ' de depolanan görevleri, 000001-</span><span class="sxs-lookup"><span data-stu-id="71cd6-135">The final command adds the tasks stored in $Task01 and $Task02 under the job that has the ID Job-000001.</span></span>

### <span data-ttu-id="71cd6-136">Örnek 5: çıkış dosyalarıyla görev ekleme</span><span class="sxs-lookup"><span data-stu-id="71cd6-136">Example 5: Add a task with output files</span></span>
```
PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
PS C:\>$blobContainerDestination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileBlobContainerDestination "https://myaccount.blob.core.windows.net/sascontainer?sv=2015-04-05&st=2015-04-29T22%3A18%3A26Z&se=2015-04-30T02%3A23%3A26Z&sr=b&sp=rw&spr=https&sig=Z%2FRHIX5Xcg0Mq2rqI3OlWTjEg2tYkboXr1P9ZUXDtkk%3D"
PS C:\>$destination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileDestination $blobContainerDestination
PS C:\>$uploadOptions = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileUploadOptions "TaskSuccess"
PS C:\>$outputFile = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFile "*.txt", $blobContainerDestination, $uploadOptions

PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -OutputFile $outputFile -BatchContext $Context
```

### <span data-ttu-id="71cd6-137">Örnek 6: kimlik doğrulama belirteci ayarlarıyla görev ekleme</span><span class="sxs-lookup"><span data-stu-id="71cd6-137">Example 6: Add a task with authentication token settings</span></span>
```
PS C:\>$authSettings = New-Object Microsoft.Azure.Commands.Batch.Models.PSAuthenticationTokenSettings
PS C:\>$authSettings.Access = "Job"
PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -AuthenticationTokenSettings $authSettings -BatchContext $Context
```

### <span data-ttu-id="71cd6-138">Örnek 7: kapsayıcıda çalışan bir görev ekleme</span><span class="sxs-lookup"><span data-stu-id="71cd6-138">Example 7: Add a task which runs in a container</span></span>
```
PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ContainerSettings New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskContainerSettings "containerImageName"
```

## <span data-ttu-id="71cd6-139">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="71cd6-139">PARAMETERS</span></span>

### <span data-ttu-id="71cd6-140">-Affinityınformation</span><span class="sxs-lookup"><span data-stu-id="71cd6-140">-AffinityInformation</span></span>
<span data-ttu-id="71cd6-141">Toplu Iş hizmetinin, görevin çalıştırılacağı düğümü seçmek için kullandığı bir konum ipucunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="71cd6-141">Specifies a locality hint that the Batch service uses to select a node on which to run the task.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSAffinityInformation
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71cd6-142">-Applicationpackagereferfer</span><span class="sxs-lookup"><span data-stu-id="71cd6-142">-ApplicationPackageReferences</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases: ApplicationPackageReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71cd6-143">-AuthenticationTokenSettings</span><span class="sxs-lookup"><span data-stu-id="71cd6-143">-AuthenticationTokenSettings</span></span>
<span data-ttu-id="71cd6-144">Görevin toplu hizmet işlemlerini gerçekleştirmek için kullanabileceği bir kimlik doğrulama belirtecinin ayarları.</span><span class="sxs-lookup"><span data-stu-id="71cd6-144">The settings for an authentication token that the task can use to perform Batch service operations.</span></span>
<span data-ttu-id="71cd6-145">Bu ayarlanırsa, toplu hizmet, göreve hesap erişim anahtarı gerekmeden toplu Iş hizmeti işlemlerinin kimliğini doğrulamak için kullanılabilecek bir kimlik doğrulama belirteciyle sağlanır.</span><span class="sxs-lookup"><span data-stu-id="71cd6-145">If this is set, the Batch service provides the task with an authentication token which can be used to authenticate Batch service operations without requiring an account access key.</span></span> <span data-ttu-id="71cd6-146">Belirteç, AZ_BATCH_AUTHENTICATION_TOKEN ortamı değişkeniyle sağlanır.</span><span class="sxs-lookup"><span data-stu-id="71cd6-146">The token is provided via the AZ_BATCH_AUTHENTICATION_TOKEN environment variable.</span></span> <span data-ttu-id="71cd6-147">Görevin belirteci kullanarak gerçekleştirebileceği işlemler ayarlara bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="71cd6-147">The operations that the task can carry out using the token depend on the settings.</span></span> <span data-ttu-id="71cd6-148">Örneğin, bir görev projeye başka görevler eklemek için iş izinleri isteyebilir ya da işin veya diğer görevlerin durumunu denetleyebilir.</span><span class="sxs-lookup"><span data-stu-id="71cd6-148">For example, a task can request job permissions in order to add other tasks to the job, or check the status of the job or of other tasks.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSAuthenticationTokenSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71cd6-149">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="71cd6-149">-BatchContext</span></span>
<span data-ttu-id="71cd6-150">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="71cd6-150">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="71cd6-151">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="71cd6-151">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="71cd6-152">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="71cd6-152">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="71cd6-153">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="71cd6-153">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="71cd6-154">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="71cd6-154">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71cd6-155">-CommandLine</span><span class="sxs-lookup"><span data-stu-id="71cd6-155">-CommandLine</span></span>
<span data-ttu-id="71cd6-156">Görevin komut satırını belirtir.</span><span class="sxs-lookup"><span data-stu-id="71cd6-156">Specifies the command line for the task.</span></span>

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71cd6-157">-Kısıtlamalar</span><span class="sxs-lookup"><span data-stu-id="71cd6-157">-Constraints</span></span>
<span data-ttu-id="71cd6-158">Bu göreve uygulanan yürütme kısıtlamalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="71cd6-158">Specifies the execution constraints that apply to this task.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71cd6-159">-ContainerSettings</span><span class="sxs-lookup"><span data-stu-id="71cd6-159">-ContainerSettings</span></span>
<span data-ttu-id="71cd6-160">Görevin çalıştığı kapsayıcının ayarları.</span><span class="sxs-lookup"><span data-stu-id="71cd6-160">The settings for the container under which the task runs.</span></span>
<span data-ttu-id="71cd6-161">Bu görevi çalıştıran havuzda containerConfiguration ayarlanmışsa, bu da ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="71cd6-161">If the pool that will run this task has containerConfiguration set, this must be set as well.</span></span> <span data-ttu-id="71cd6-162">Bu görevi çalıştıran havuzda containerConfiguration ayarlanmamışsa, bu ayarlanmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="71cd6-162">If the pool that will run this task doesn't have containerConfiguration set, this must not be set.</span></span> <span data-ttu-id="71cd6-163">Bu belirtildiğinde, tüm dizinler AZ_BATCH_NODE_ROOT_DIR (düğümdeki Azure toplu Iş dizinlerinin kökü) kapsayıcıya eşlenir, tüm görev ortam değişkenleri kapsayıcıya eşlenir ve görev komut satırı kapsayıcıda yürütülür.</span><span class="sxs-lookup"><span data-stu-id="71cd6-163">When this is specified, all directories recursively below the AZ_BATCH_NODE_ROOT_DIR (the root of Azure Batch directories on the node) are mapped into the container, all task environment variables are mapped into the container, and the task command line is executed in the container.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSTaskContainerSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71cd6-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71cd6-164">-DefaultProfile</span></span>
<span data-ttu-id="71cd6-165">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="71cd6-165">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71cd6-166">-Bağımlılson</span><span class="sxs-lookup"><span data-stu-id="71cd6-166">-DependsOn</span></span>
<span data-ttu-id="71cd6-167">Görevin diğer görevlere bağlı olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="71cd6-167">Specifies that the task depends on other tasks.</span></span>
<span data-ttu-id="71cd6-168">Tüm bağlı görevler başarıyla tamamlanıncaya kadar görev planlanmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="71cd6-168">The task will not be scheduled until all depended-on tasks have completed successfully.</span></span>

```yaml
Type: Microsoft.Azure.Batch.TaskDependencies
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71cd6-169">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="71cd6-169">-DisplayName</span></span>
<span data-ttu-id="71cd6-170">Görevin görünen adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="71cd6-170">Specifies the display name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71cd6-171">-EnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="71cd6-171">-EnvironmentSettings</span></span>
<span data-ttu-id="71cd6-172">Anahtar/değer çiftleri olarak, bu cmdlet 'in göreve eklediği ortam ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="71cd6-172">Specifies the environment settings, as key/value pairs, that this cmdlet adds to the task.</span></span>
<span data-ttu-id="71cd6-173">Anahtar, ortam ayarı adıdır.</span><span class="sxs-lookup"><span data-stu-id="71cd6-173">The key is the environment setting name.</span></span>
<span data-ttu-id="71cd6-174">Değer, ortam ayarıdır.</span><span class="sxs-lookup"><span data-stu-id="71cd6-174">The value is the environment setting.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: EnvironmentSetting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71cd6-175">-ExitConditions</span><span class="sxs-lookup"><span data-stu-id="71cd6-175">-ExitConditions</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSExitConditions
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71cd6-176">-ID</span><span class="sxs-lookup"><span data-stu-id="71cd6-176">-Id</span></span>
<span data-ttu-id="71cd6-177">Görevin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="71cd6-177">Specifies the ID of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71cd6-178">-Job</span><span class="sxs-lookup"><span data-stu-id="71cd6-178">-Job</span></span>
<span data-ttu-id="71cd6-179">Bu cmdlet 'in görev oluşturduğu işi belirtir.</span><span class="sxs-lookup"><span data-stu-id="71cd6-179">Specifies the job under which this cmdlet creates the task.</span></span>
<span data-ttu-id="71cd6-180">Bir **Ince iş** nesnesi edinmek için Get-AzureBatchJob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="71cd6-180">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: JobObject_Bulk, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71cd6-181">-JobId</span><span class="sxs-lookup"><span data-stu-id="71cd6-181">-JobId</span></span>
<span data-ttu-id="71cd6-182">Bu cmdlet 'in görev oluşturduğu işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="71cd6-182">Specifies the ID of the job under which this cmdlet creates the task.</span></span>

```yaml
Type: System.String
Parameter Sets: JobId_Single, JobId_Bulk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71cd6-183">-Multiınstancesettings</span><span class="sxs-lookup"><span data-stu-id="71cd6-183">-MultiInstanceSettings</span></span>
<span data-ttu-id="71cd6-184">Çok örnekli bir görevin nasıl çalıştırılacağı hakkında bilgi belirtir.</span><span class="sxs-lookup"><span data-stu-id="71cd6-184">Specifies information about how to run a multi-instance task.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71cd6-185">-ÇıktıDosyası</span><span class="sxs-lookup"><span data-stu-id="71cd6-185">-OutputFile</span></span>
<span data-ttu-id="71cd6-186">Komut satırını çalıştırdıktan sonra, toplu Iş hizmetinin COMPUTE düğümünden karşıya yükleneceği dosyaların listesini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="71cd6-186">Gets or sets a list of files that the Batch service will upload from the compute node after running the command line.</span></span>
<span data-ttu-id="71cd6-187">Çok örnekli görevler için, dosyalar yalnızca birincil görevin yürütüldüğü işlem düğümünden karşıya yüklenir.</span><span class="sxs-lookup"><span data-stu-id="71cd6-187">For multi-instance tasks, the files will only be uploaded from the compute node on which the primary task is executed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSOutputFile[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71cd6-188">-ResourceFiles</span><span class="sxs-lookup"><span data-stu-id="71cd6-188">-ResourceFiles</span></span>
<span data-ttu-id="71cd6-189">Kaynak dosyalarını anahtar/değer çiftleri olarak, görevin gerektirdiği şekilde belirtir.</span><span class="sxs-lookup"><span data-stu-id="71cd6-189">Specifies resource files, as key/value pairs, that the task requires.</span></span>
<span data-ttu-id="71cd6-190">Anahtar, kaynak dosyası yoludur.</span><span class="sxs-lookup"><span data-stu-id="71cd6-190">The key is the resource file path.</span></span>
<span data-ttu-id="71cd6-191">Değer, kaynak dosyası blob kaynağıdır.</span><span class="sxs-lookup"><span data-stu-id="71cd6-191">The value is the resource file blob source.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: ResourceFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71cd6-192">-Görevler</span><span class="sxs-lookup"><span data-stu-id="71cd6-192">-Tasks</span></span>
<span data-ttu-id="71cd6-193">Eklenecek görevlerin koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="71cd6-193">Specifies the collection of tasks to be added.</span></span>
<span data-ttu-id="71cd6-194">Her görevin benzersiz bir KIMLIĞI olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="71cd6-194">Each task must have a unique ID.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask[]
Parameter Sets: JobId_Bulk, JobObject_Bulk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71cd6-195">-UserIdentity</span><span class="sxs-lookup"><span data-stu-id="71cd6-195">-UserIdentity</span></span>
<span data-ttu-id="71cd6-196">Görevin çalıştığı kullanıcı kimliği.</span><span class="sxs-lookup"><span data-stu-id="71cd6-196">The user identity under which the task runs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSUserIdentity
Parameter Sets: JobId_Single, JobObject_Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71cd6-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71cd6-197">CommonParameters</span></span>
<span data-ttu-id="71cd6-198">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="71cd6-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71cd6-199">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71cd6-199">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71cd6-200">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="71cd6-200">INPUTS</span></span>

### <span data-ttu-id="71cd6-201">Microsoft.Azure.Commands.Batch. Modeller. Pscses Işi</span><span class="sxs-lookup"><span data-stu-id="71cd6-201">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>
<span data-ttu-id="71cd6-202">Parametreler: Iş (ByValue)</span><span class="sxs-lookup"><span data-stu-id="71cd6-202">Parameters: Job (ByValue)</span></span>

### <span data-ttu-id="71cd6-203">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="71cd6-203">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="71cd6-204">Parametreler: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="71cd6-204">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="71cd6-205">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="71cd6-205">OUTPUTS</span></span>

### <span data-ttu-id="71cd6-206">System. void</span><span class="sxs-lookup"><span data-stu-id="71cd6-206">System.Void</span></span>

## <span data-ttu-id="71cd6-207">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="71cd6-207">NOTES</span></span>

## <span data-ttu-id="71cd6-208">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="71cd6-208">RELATED LINKS</span></span>

[<span data-ttu-id="71cd6-209">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="71cd6-209">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="71cd6-210">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="71cd6-210">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="71cd6-211">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="71cd6-211">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="71cd6-212">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="71cd6-212">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="71cd6-213">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="71cd6-213">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="71cd6-214">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="71cd6-214">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="71cd6-215">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="71cd6-215">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


