---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2B4BFDDA-9721-42E6-84E1-A209CB782954
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchTask.md
ms.openlocfilehash: adb3a44a5d913d636d216750358ebd96c8fc5a29
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93938624"
---
# <span data-ttu-id="81eb1-101">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="81eb1-101">New-AzBatchTask</span></span>

## <span data-ttu-id="81eb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81eb1-102">SYNOPSIS</span></span>
<span data-ttu-id="81eb1-103">Bir iş altında toplu görev oluşturur.</span><span class="sxs-lookup"><span data-stu-id="81eb1-103">Creates a Batch task under a job.</span></span>

## <span data-ttu-id="81eb1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="81eb1-104">SYNTAX</span></span>

### <span data-ttu-id="81eb1-105">JobId_Single (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="81eb1-105">JobId_Single (Default)</span></span>
```
New-AzBatchTask -JobId <String> -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>]
 [-AuthenticationTokenSettings <PSAuthenticationTokenSettings>] [-UserIdentity <PSUserIdentity>]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-OutputFile <PSOutputFile[]>]
 [-ExitConditions <PSExitConditions>] [-ContainerSettings <PSTaskContainerSettings>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81eb1-106">JobId_Bulk</span><span class="sxs-lookup"><span data-stu-id="81eb1-106">JobId_Bulk</span></span>
```
New-AzBatchTask -JobId <String> [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81eb1-107">JobObject_Bulk</span><span class="sxs-lookup"><span data-stu-id="81eb1-107">JobObject_Bulk</span></span>
```
New-AzBatchTask [-Job <PSCloudJob>] [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81eb1-108">JobObject_Single</span><span class="sxs-lookup"><span data-stu-id="81eb1-108">JobObject_Single</span></span>
```
New-AzBatchTask [-Job <PSCloudJob>] -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>]
 [-AuthenticationTokenSettings <PSAuthenticationTokenSettings>] [-UserIdentity <PSUserIdentity>]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-OutputFile <PSOutputFile[]>]
 [-ExitConditions <PSExitConditions>] [-ContainerSettings <PSTaskContainerSettings>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81eb1-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="81eb1-109">DESCRIPTION</span></span>
<span data-ttu-id="81eb1-110">**New-AzBatchTask** cmdlet 'ı, *JobId* parametresi veya *iş* parametresi tarafından belirtilen iş altında bir Azure toplu işlemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="81eb1-110">The **New-AzBatchTask** cmdlet creates an Azure Batch task under the job specified by the *JobId* parameter or the *Job* parameter.</span></span>

## <span data-ttu-id="81eb1-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="81eb1-111">EXAMPLES</span></span>

### <span data-ttu-id="81eb1-112">Örnek 1: toplu görev oluşturma</span><span class="sxs-lookup"><span data-stu-id="81eb1-112">Example 1: Create a Batch task</span></span>
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
```

<span data-ttu-id="81eb1-113">Bu komut, iş-000001 KIMLIĞI olan işin altında KIMLIK Task23 olan bir görev oluşturur.</span><span class="sxs-lookup"><span data-stu-id="81eb1-113">This command creates a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="81eb1-114">Görev belirtilen komutu çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="81eb1-114">The task runs the specified command.</span></span>
<span data-ttu-id="81eb1-115">$Context değişkenine bağlam atamak için **Get-AzBatchAccountKeys** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="81eb1-115">Use the **Get-AzBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="81eb1-116">Örnek 2: toplu görev oluşturma</span><span class="sxs-lookup"><span data-stu-id="81eb1-116">Example 2: Create a Batch task</span></span>
```
PS C:\> $autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
PS C:\> $userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
PS C:\>Get-AzBatchJob -Id "Job-000001" -BatchContext $Context | New-AzBatchTask -Id "Task26" -CommandLine "cmd /c echo hello > newFile.txt" -UserIdentity $userIdentity -BatchContext $Context
```

<span data-ttu-id="81eb1-117">Bu komut, **Get-AzBatchJob** cmdlet 'ini kullanarak 000001 kimliğine sahip toplu işlemi alır.</span><span class="sxs-lookup"><span data-stu-id="81eb1-117">This command gets the Batch job that has the ID Job-000001 by using the **Get-AzBatchJob** cmdlet.</span></span>
<span data-ttu-id="81eb1-118">Komut bu işi ardışık düzen işlecini kullanarak geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="81eb1-118">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="81eb1-119">Komut, iş altında KIMLIK Task26 olan bir görev oluşturur.</span><span class="sxs-lookup"><span data-stu-id="81eb1-119">The command creates a task that has the ID Task26 under that job.</span></span>
<span data-ttu-id="81eb1-120">Görev, yükseltilmiş izinleri kullanarak belirtilen komutu çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="81eb1-120">The task runs the specified command by using elevated permissions.</span></span>

### <span data-ttu-id="81eb1-121">Örnek 3: ardışık düzeni kullanarak belirtilen işe görev koleksiyonu ekleme</span><span class="sxs-lookup"><span data-stu-id="81eb1-121">Example 3: Add a collection of tasks to the specified job by using the pipeline</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> Get-AzBatchJob -Id "Job-000001" -BatchContext $Context | New-AzBatchTask -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="81eb1-122">İlk komut, **Get-AzBatchAccountKeys** kullanarak contosobatchaccount adlı toplu hesap için hesap anahtarlarına bir nesne başvurusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="81eb1-122">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKeys**.</span></span>
<span data-ttu-id="81eb1-123">Komut bu nesne başvurusunu $Context değişkenine depolar.</span><span class="sxs-lookup"><span data-stu-id="81eb1-123">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="81eb1-124">Sonraki iki komut, New-Object cmdlet 'ini kullanarak **Ince görev** nesneleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="81eb1-124">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="81eb1-125">Komutlar $Task 01 ve $Task 02 değişkenlerinde görevleri depolar.</span><span class="sxs-lookup"><span data-stu-id="81eb1-125">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>
<span data-ttu-id="81eb1-126">Final komutu, **Get-AzBatchJob** kullanarak, 000001 kimliğine sahip toplu işlemi alır.</span><span class="sxs-lookup"><span data-stu-id="81eb1-126">The final command gets the Batch job that has the ID Job-000001 by using **Get-AzBatchJob**.</span></span>
<span data-ttu-id="81eb1-127">Ardından komut bu işi ardışık düzen işlecini kullanarak geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="81eb1-127">Then the command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="81eb1-128">Komut bu iş altında bir görev koleksiyonu ekler.</span><span class="sxs-lookup"><span data-stu-id="81eb1-128">The command adds a collection of tasks under that job.</span></span>
<span data-ttu-id="81eb1-129">Komut, $Context depolanan bağlamı kullanır.</span><span class="sxs-lookup"><span data-stu-id="81eb1-129">The command uses the context stored in $Context.</span></span>

### <span data-ttu-id="81eb1-130">Örnek 4: belirtilen işe görevler koleksiyonu ekleme</span><span class="sxs-lookup"><span data-stu-id="81eb1-130">Example 4: Add a collection of tasks to the specified job</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> New-AzBatchTask -JobId "Job-000001" -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="81eb1-131">İlk komut, **Get-AzBatchAccountKeys** kullanarak contosobatchaccount adlı toplu hesap için hesap anahtarlarına bir nesne başvurusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="81eb1-131">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKeys**.</span></span>
<span data-ttu-id="81eb1-132">Komut bu nesne başvurusunu $Context değişkenine depolar.</span><span class="sxs-lookup"><span data-stu-id="81eb1-132">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="81eb1-133">Sonraki iki komut, New-Object cmdlet 'ini kullanarak **Ince görev** nesneleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="81eb1-133">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="81eb1-134">Komutlar $Task 01 ve $Task 02 değişkenlerinde görevleri depolar.</span><span class="sxs-lookup"><span data-stu-id="81eb1-134">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>
<span data-ttu-id="81eb1-135">Son komut $Task $Task 01 ' de depolanan görevleri, 000001-</span><span class="sxs-lookup"><span data-stu-id="81eb1-135">The final command adds the tasks stored in $Task01 and $Task02 under the job that has the ID Job-000001.</span></span>

### <span data-ttu-id="81eb1-136">Örnek 5: çıkış dosyalarıyla görev ekleme</span><span class="sxs-lookup"><span data-stu-id="81eb1-136">Example 5: Add a task with output files</span></span>
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
PS C:\>$blobContainerDestination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileBlobContainerDestination "https://myaccount.blob.core.windows.net/sascontainer?sv=2015-04-05&st=2015-04-29T22%3A18%3A26Z&se=2015-04-30T02%3A23%3A26Z&sr=b&sp=rw&spr=https&sig=Z%2FRHIX5Xcg0Mq2rqI3OlWTjEg2tYkboXr1P9ZUXDtkk%3D"
PS C:\>$destination = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileDestination $blobContainerDestination
PS C:\>$uploadOptions = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFileUploadOptions "TaskSuccess"
PS C:\>$outputFile = New-Object Microsoft.Azure.Commands.Batch.Models.PSOutputFile "*.txt", $blobContainerDestination, $uploadOptions

PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -OutputFile $outputFile -BatchContext $Context
```

### <span data-ttu-id="81eb1-137">Örnek 6: kimlik doğrulama belirteci ayarlarıyla görev ekleme</span><span class="sxs-lookup"><span data-stu-id="81eb1-137">Example 6: Add a task with authentication token settings</span></span>
```
PS C:\>$authSettings = New-Object Microsoft.Azure.Commands.Batch.Models.PSAuthenticationTokenSettings
PS C:\>$authSettings.Access = "Job"
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -AuthenticationTokenSettings $authSettings -BatchContext $Context
```

### <span data-ttu-id="81eb1-138">Örnek 7: kapsayıcıda çalışan bir görev ekleme</span><span class="sxs-lookup"><span data-stu-id="81eb1-138">Example 7: Add a task which runs in a container</span></span>
```
PS C:\>New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ContainerSettings New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskContainerSettings "containerImageName"
```

## <span data-ttu-id="81eb1-139">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="81eb1-139">PARAMETERS</span></span>

### <span data-ttu-id="81eb1-140">-Affinityınformation</span><span class="sxs-lookup"><span data-stu-id="81eb1-140">-AffinityInformation</span></span>
<span data-ttu-id="81eb1-141">Toplu Iş hizmetinin, görevin çalıştırılacağı düğümü seçmek için kullandığı bir konum ipucunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="81eb1-141">Specifies a locality hint that the Batch service uses to select a node on which to run the task.</span></span>

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

### <span data-ttu-id="81eb1-142">-Applicationpackagereferfer</span><span class="sxs-lookup"><span data-stu-id="81eb1-142">-ApplicationPackageReferences</span></span>
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

### <span data-ttu-id="81eb1-143">-AuthenticationTokenSettings</span><span class="sxs-lookup"><span data-stu-id="81eb1-143">-AuthenticationTokenSettings</span></span>
<span data-ttu-id="81eb1-144">Görevin toplu hizmet işlemlerini gerçekleştirmek için kullanabileceği bir kimlik doğrulama belirtecinin ayarları.</span><span class="sxs-lookup"><span data-stu-id="81eb1-144">The settings for an authentication token that the task can use to perform Batch service operations.</span></span>
<span data-ttu-id="81eb1-145">Bu ayarlanırsa, toplu hizmet, göreve hesap erişim anahtarı gerekmeden toplu Iş hizmeti işlemlerinin kimliğini doğrulamak için kullanılabilecek bir kimlik doğrulama belirteciyle sağlanır.</span><span class="sxs-lookup"><span data-stu-id="81eb1-145">If this is set, the Batch service provides the task with an authentication token which can be used to authenticate Batch service operations without requiring an account access key.</span></span> <span data-ttu-id="81eb1-146">Belirteç, AZ_BATCH_AUTHENTICATION_TOKEN ortamı değişkeniyle sağlanır.</span><span class="sxs-lookup"><span data-stu-id="81eb1-146">The token is provided via the AZ_BATCH_AUTHENTICATION_TOKEN environment variable.</span></span> <span data-ttu-id="81eb1-147">Görevin belirteci kullanarak gerçekleştirebileceği işlemler ayarlara bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="81eb1-147">The operations that the task can carry out using the token depend on the settings.</span></span> <span data-ttu-id="81eb1-148">Örneğin, bir görev projeye başka görevler eklemek için iş izinleri isteyebilir ya da işin veya diğer görevlerin durumunu denetleyebilir.</span><span class="sxs-lookup"><span data-stu-id="81eb1-148">For example, a task can request job permissions in order to add other tasks to the job, or check the status of the job or of other tasks.</span></span>

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

### <span data-ttu-id="81eb1-149">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="81eb1-149">-BatchContext</span></span>
<span data-ttu-id="81eb1-150">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="81eb1-150">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="81eb1-151">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="81eb1-151">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="81eb1-152">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="81eb1-152">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="81eb1-153">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="81eb1-153">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="81eb1-154">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="81eb1-154">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="81eb1-155">-CommandLine</span><span class="sxs-lookup"><span data-stu-id="81eb1-155">-CommandLine</span></span>
<span data-ttu-id="81eb1-156">Görevin komut satırını belirtir.</span><span class="sxs-lookup"><span data-stu-id="81eb1-156">Specifies the command line for the task.</span></span>

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

### <span data-ttu-id="81eb1-157">-Kısıtlamalar</span><span class="sxs-lookup"><span data-stu-id="81eb1-157">-Constraints</span></span>
<span data-ttu-id="81eb1-158">Bu göreve uygulanan yürütme kısıtlamalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="81eb1-158">Specifies the execution constraints that apply to this task.</span></span>

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

### <span data-ttu-id="81eb1-159">-ContainerSettings</span><span class="sxs-lookup"><span data-stu-id="81eb1-159">-ContainerSettings</span></span>
<span data-ttu-id="81eb1-160">Görevin çalıştığı kapsayıcının ayarları.</span><span class="sxs-lookup"><span data-stu-id="81eb1-160">The settings for the container under which the task runs.</span></span>
<span data-ttu-id="81eb1-161">Bu görevi çalıştıran havuzda containerConfiguration ayarlanmışsa, bu da ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="81eb1-161">If the pool that will run this task has containerConfiguration set, this must be set as well.</span></span> <span data-ttu-id="81eb1-162">Bu görevi çalıştıran havuzda containerConfiguration ayarlanmamışsa, bu ayarlanmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="81eb1-162">If the pool that will run this task doesn't have containerConfiguration set, this must not be set.</span></span> <span data-ttu-id="81eb1-163">Bu belirtildiğinde, tüm dizinler AZ_BATCH_NODE_ROOT_DIR (düğümdeki Azure toplu Iş dizinlerinin kökü) kapsayıcıya eşlenir, tüm görev ortam değişkenleri kapsayıcıya eşlenir ve görev komut satırı kapsayıcıda yürütülür.</span><span class="sxs-lookup"><span data-stu-id="81eb1-163">When this is specified, all directories recursively below the AZ_BATCH_NODE_ROOT_DIR (the root of Azure Batch directories on the node) are mapped into the container, all task environment variables are mapped into the container, and the task command line is executed in the container.</span></span>

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

### <span data-ttu-id="81eb1-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81eb1-164">-DefaultProfile</span></span>
<span data-ttu-id="81eb1-165">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="81eb1-165">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81eb1-166">-Bağımlılson</span><span class="sxs-lookup"><span data-stu-id="81eb1-166">-DependsOn</span></span>
<span data-ttu-id="81eb1-167">Görevin diğer görevlere bağlı olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="81eb1-167">Specifies that the task depends on other tasks.</span></span>
<span data-ttu-id="81eb1-168">Tüm bağlı görevler başarıyla tamamlanıncaya kadar görev planlanmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="81eb1-168">The task will not be scheduled until all depended-on tasks have completed successfully.</span></span>

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

### <span data-ttu-id="81eb1-169">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="81eb1-169">-DisplayName</span></span>
<span data-ttu-id="81eb1-170">Görevin görünen adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="81eb1-170">Specifies the display name of the task.</span></span>

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

### <span data-ttu-id="81eb1-171">-EnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="81eb1-171">-EnvironmentSettings</span></span>
<span data-ttu-id="81eb1-172">Anahtar/değer çiftleri olarak, bu cmdlet 'in göreve eklediği ortam ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="81eb1-172">Specifies the environment settings, as key/value pairs, that this cmdlet adds to the task.</span></span>
<span data-ttu-id="81eb1-173">Anahtar, ortam ayarı adıdır.</span><span class="sxs-lookup"><span data-stu-id="81eb1-173">The key is the environment setting name.</span></span>
<span data-ttu-id="81eb1-174">Değer, ortam ayarıdır.</span><span class="sxs-lookup"><span data-stu-id="81eb1-174">The value is the environment setting.</span></span>

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

### <span data-ttu-id="81eb1-175">-ExitConditions</span><span class="sxs-lookup"><span data-stu-id="81eb1-175">-ExitConditions</span></span>
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

### <span data-ttu-id="81eb1-176">-ID</span><span class="sxs-lookup"><span data-stu-id="81eb1-176">-Id</span></span>
<span data-ttu-id="81eb1-177">Görevin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="81eb1-177">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="81eb1-178">-Job</span><span class="sxs-lookup"><span data-stu-id="81eb1-178">-Job</span></span>
<span data-ttu-id="81eb1-179">Bu cmdlet 'in görev oluşturduğu işi belirtir.</span><span class="sxs-lookup"><span data-stu-id="81eb1-179">Specifies the job under which this cmdlet creates the task.</span></span>
<span data-ttu-id="81eb1-180">Bir **Ince iş** nesnesi edinmek için Get-AzBatchJob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="81eb1-180">To obtain a **PSCloudJob** object, use the Get-AzBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="81eb1-181">-JobId</span><span class="sxs-lookup"><span data-stu-id="81eb1-181">-JobId</span></span>
<span data-ttu-id="81eb1-182">Bu cmdlet 'in görev oluşturduğu işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="81eb1-182">Specifies the ID of the job under which this cmdlet creates the task.</span></span>

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

### <span data-ttu-id="81eb1-183">-Multiınstancesettings</span><span class="sxs-lookup"><span data-stu-id="81eb1-183">-MultiInstanceSettings</span></span>
<span data-ttu-id="81eb1-184">Çok örnekli bir görevin nasıl çalıştırılacağı hakkında bilgi belirtir.</span><span class="sxs-lookup"><span data-stu-id="81eb1-184">Specifies information about how to run a multi-instance task.</span></span>

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

### <span data-ttu-id="81eb1-185">-ÇıktıDosyası</span><span class="sxs-lookup"><span data-stu-id="81eb1-185">-OutputFile</span></span>
<span data-ttu-id="81eb1-186">Komut satırını çalıştırdıktan sonra, toplu Iş hizmetinin COMPUTE düğümünden karşıya yükleneceği dosyaların listesini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="81eb1-186">Gets or sets a list of files that the Batch service will upload from the compute node after running the command line.</span></span>
<span data-ttu-id="81eb1-187">Çok örnekli görevler için, dosyalar yalnızca birincil görevin yürütüldüğü işlem düğümünden karşıya yüklenir.</span><span class="sxs-lookup"><span data-stu-id="81eb1-187">For multi-instance tasks, the files will only be uploaded from the compute node on which the primary task is executed.</span></span>

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

### <span data-ttu-id="81eb1-188">-ResourceFiles</span><span class="sxs-lookup"><span data-stu-id="81eb1-188">-ResourceFiles</span></span>
<span data-ttu-id="81eb1-189">Kaynak dosyalarını anahtar/değer çiftleri olarak, görevin gerektirdiği şekilde belirtir.</span><span class="sxs-lookup"><span data-stu-id="81eb1-189">Specifies resource files, as key/value pairs, that the task requires.</span></span>
<span data-ttu-id="81eb1-190">Anahtar, kaynak dosyası yoludur.</span><span class="sxs-lookup"><span data-stu-id="81eb1-190">The key is the resource file path.</span></span>
<span data-ttu-id="81eb1-191">Değer, kaynak dosyası blob kaynağıdır.</span><span class="sxs-lookup"><span data-stu-id="81eb1-191">The value is the resource file blob source.</span></span>

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

### <span data-ttu-id="81eb1-192">-Görevler</span><span class="sxs-lookup"><span data-stu-id="81eb1-192">-Tasks</span></span>
<span data-ttu-id="81eb1-193">Eklenecek görevlerin koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="81eb1-193">Specifies the collection of tasks to be added.</span></span>
<span data-ttu-id="81eb1-194">Her görevin benzersiz bir KIMLIĞI olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="81eb1-194">Each task must have a unique ID.</span></span>

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

### <span data-ttu-id="81eb1-195">-UserIdentity</span><span class="sxs-lookup"><span data-stu-id="81eb1-195">-UserIdentity</span></span>
<span data-ttu-id="81eb1-196">Görevin çalıştığı kullanıcı kimliği.</span><span class="sxs-lookup"><span data-stu-id="81eb1-196">The user identity under which the task runs.</span></span>

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

### <span data-ttu-id="81eb1-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81eb1-197">CommonParameters</span></span>
<span data-ttu-id="81eb1-198">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="81eb1-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81eb1-199">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81eb1-199">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81eb1-200">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="81eb1-200">INPUTS</span></span>

### <span data-ttu-id="81eb1-201">Microsoft.Azure.Commands.Batch. Modeller. Pscses Işi</span><span class="sxs-lookup"><span data-stu-id="81eb1-201">Microsoft.Azure.Commands.Batch.Models.PSCloudJob</span></span>

### <span data-ttu-id="81eb1-202">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="81eb1-202">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="81eb1-203">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="81eb1-203">OUTPUTS</span></span>

### <span data-ttu-id="81eb1-204">System. void</span><span class="sxs-lookup"><span data-stu-id="81eb1-204">System.Void</span></span>

## <span data-ttu-id="81eb1-205">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="81eb1-205">NOTES</span></span>

## <span data-ttu-id="81eb1-206">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="81eb1-206">RELATED LINKS</span></span>

[<span data-ttu-id="81eb1-207">Get-Aztopluaccountkeys</span><span class="sxs-lookup"><span data-stu-id="81eb1-207">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="81eb1-208">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="81eb1-208">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="81eb1-209">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="81eb1-209">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="81eb1-210">Yeni-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="81eb1-210">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="81eb1-211">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="81eb1-211">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="81eb1-212">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="81eb1-212">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="81eb1-213">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="81eb1-213">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


