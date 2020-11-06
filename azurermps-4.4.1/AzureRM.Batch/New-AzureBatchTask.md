---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2B4BFDDA-9721-42E6-84E1-A209CB782954
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchTask.md
ms.openlocfilehash: dd8825be6491b0a0c8c8589f77180b38f9f230d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591149"
---
# <span data-ttu-id="06209-101">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="06209-101">New-AzureBatchTask</span></span>

## <span data-ttu-id="06209-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06209-102">SYNOPSIS</span></span>
<span data-ttu-id="06209-103">Bir iş altında toplu görev oluşturur.</span><span class="sxs-lookup"><span data-stu-id="06209-103">Creates a Batch task under a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06209-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="06209-104">SYNTAX</span></span>

### <span data-ttu-id="06209-105">JobId_Single (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="06209-105">JobId_Single (Default)</span></span>
```
New-AzureBatchTask -JobId <String> -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>] [-RunElevated]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-ExitConditions <PSExitConditions>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06209-106">JobId_Bulk</span><span class="sxs-lookup"><span data-stu-id="06209-106">JobId_Bulk</span></span>
```
New-AzureBatchTask -JobId <String> [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06209-107">JobObject_Bulk</span><span class="sxs-lookup"><span data-stu-id="06209-107">JobObject_Bulk</span></span>
```
New-AzureBatchTask [-Job <PSCloudJob>] [-Tasks <PSCloudTask[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06209-108">JobObject_Single</span><span class="sxs-lookup"><span data-stu-id="06209-108">JobObject_Single</span></span>
```
New-AzureBatchTask [-Job <PSCloudJob>] -Id <String> [-DisplayName <String>] [-CommandLine <String>]
 [-ResourceFiles <IDictionary>] [-EnvironmentSettings <IDictionary>] [-RunElevated]
 [-AffinityInformation <PSAffinityInformation>] [-Constraints <PSTaskConstraints>]
 [-MultiInstanceSettings <PSMultiInstanceSettings>] [-DependsOn <TaskDependencies>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>] [-ExitConditions <PSExitConditions>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06209-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="06209-109">DESCRIPTION</span></span>
<span data-ttu-id="06209-110">**New-AzureBatchTask** cmdlet 'ı, *JobId* parametresi veya *iş* parametresi tarafından belirtilen işin altında bir Azure toplu işlemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="06209-110">The **New-AzureBatchTask** cmdlet creates an Azure Batch task under the job specified by the *JobId* parameter or the *Job* parameter.</span></span>

## <span data-ttu-id="06209-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="06209-111">EXAMPLES</span></span>

### <span data-ttu-id="06209-112">Örnek 1: toplu görev oluşturma</span><span class="sxs-lookup"><span data-stu-id="06209-112">Example 1: Create a Batch task</span></span>
```
PS C:\>New-AzureBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -BatchContext $Context
```

<span data-ttu-id="06209-113">Bu komut, iş-000001 KIMLIĞI olan işin altında KIMLIK Task23 olan bir görev oluşturur.</span><span class="sxs-lookup"><span data-stu-id="06209-113">This command creates a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="06209-114">Görev belirtilen komutu çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="06209-114">The task runs the specified command.</span></span>
<span data-ttu-id="06209-115">$Context değişkenine bağlam atamak için **Get-AzureRmBatchAccountKeys** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="06209-115">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="06209-116">Örnek 2: toplu görev oluşturma</span><span class="sxs-lookup"><span data-stu-id="06209-116">Example 2: Create a Batch task</span></span>
```
PS C:\>Get-AzureBatchJob -Id "Job-000001" -BatchContext $Context | New-AzureBatchTask -Id "Task26" -CommandLine "cmd /c echo hello > newFile.txt" -RunElevated -BatchContext $Context
```

<span data-ttu-id="06209-117">Bu komut, **Get-AzureBatchJob** cmdlet 'ini kullanarak 000001 kimliğine sahip olan toplu işlemi alır.</span><span class="sxs-lookup"><span data-stu-id="06209-117">This command gets the Batch job that has the ID Job-000001 by using the **Get-AzureBatchJob** cmdlet.</span></span>
<span data-ttu-id="06209-118">Komut bu işi ardışık düzen işlecini kullanarak geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="06209-118">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="06209-119">Komut, iş altında KIMLIK Task26 olan bir görev oluşturur.</span><span class="sxs-lookup"><span data-stu-id="06209-119">The command creates a task that has the ID Task26 under that job.</span></span>
<span data-ttu-id="06209-120">Görev, yükseltilmiş izinleri kullanarak belirtilen komutu çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="06209-120">The task runs the specified command by using elevated permissions.</span></span>

### <span data-ttu-id="06209-121">Örnek 3: ardışık düzeni kullanarak belirtilen işe görev koleksiyonu ekleme</span><span class="sxs-lookup"><span data-stu-id="06209-121">Example 3: Add a collection of tasks to the specified job by using the pipeline</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> Get-AzureBatchJob -Id "Job-000001" -BatchContext $Context | New-AzureBatchTask -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="06209-122">İlk komut, **Get-AzureRmBatchAccountKeys** kullanarak contosobatchaccount adlı toplu hesap için hesap anahtarlarına bir nesne başvurusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="06209-122">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="06209-123">Komut bu nesne başvurusunu $Context değişkenine depolar.</span><span class="sxs-lookup"><span data-stu-id="06209-123">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="06209-124">Sonraki iki komut, New-Object cmdlet 'ini kullanarak **Ince görev** nesneleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="06209-124">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="06209-125">Komutlar $Task 01 ve $Task 02 değişkenlerinde görevleri depolar.</span><span class="sxs-lookup"><span data-stu-id="06209-125">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>

<span data-ttu-id="06209-126">Son komutu, **Get-AzureBatchJob** kullanarak, 000001 kimliğine sahip olan toplu işlemi alır.</span><span class="sxs-lookup"><span data-stu-id="06209-126">The final command gets the Batch job that has the ID Job-000001 by using **Get-AzureBatchJob**.</span></span>
<span data-ttu-id="06209-127">Ardından komut bu işi ardışık düzen işlecini kullanarak geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="06209-127">Then the command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="06209-128">Komut bu iş altında bir görev koleksiyonu ekler.</span><span class="sxs-lookup"><span data-stu-id="06209-128">The command adds a collection of tasks under that job.</span></span>
<span data-ttu-id="06209-129">Komut, $Context depolanan bağlamı kullanır.</span><span class="sxs-lookup"><span data-stu-id="06209-129">The command uses the context stored in $Context.</span></span>

### <span data-ttu-id="06209-130">Örnek 4: belirtilen işe görevler koleksiyonu ekleme</span><span class="sxs-lookup"><span data-stu-id="06209-130">Example 4: Add a collection of tasks to the specified job</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $Task01 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task23", "cmd /c dir /s")
PS C:\> $Task02 = New-Object Microsoft.Azure.Commands.Batch.Models.PSCloudTask("Task24", "cmd /c dir /s")
PS C:\> New-AzureBatchTask -JobId "Job-000001" -Tasks @($Task01, $Task02) -BatchContext $Context
```

<span data-ttu-id="06209-131">İlk komut, **Get-AzureRmBatchAccountKeys** kullanarak contosobatchaccount adlı toplu hesap için hesap anahtarlarına bir nesne başvurusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="06209-131">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="06209-132">Komut bu nesne başvurusunu $Context değişkenine depolar.</span><span class="sxs-lookup"><span data-stu-id="06209-132">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="06209-133">Sonraki iki komut, New-Object cmdlet 'ini kullanarak **Ince görev** nesneleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="06209-133">The next two commands create **PSCloudTask** objects by using the New-Object cmdlet.</span></span>
<span data-ttu-id="06209-134">Komutlar $Task 01 ve $Task 02 değişkenlerinde görevleri depolar.</span><span class="sxs-lookup"><span data-stu-id="06209-134">The commands store the tasks in the $Task01 and $Task02 variables.</span></span>

<span data-ttu-id="06209-135">Son komut $Task $Task 01 ' de depolanan görevleri, 000001-</span><span class="sxs-lookup"><span data-stu-id="06209-135">The final command adds the tasks stored in $Task01 and $Task02 under the job that has the ID Job-000001.</span></span>

## <span data-ttu-id="06209-136">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="06209-136">PARAMETERS</span></span>

### <span data-ttu-id="06209-137">-Affinityınformation</span><span class="sxs-lookup"><span data-stu-id="06209-137">-AffinityInformation</span></span>
<span data-ttu-id="06209-138">Toplu Iş hizmetinin, görevin çalıştırılacağı düğümü seçmek için kullandığı bir konum ipucunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="06209-138">Specifies a locality hint that the Batch service uses to select a node on which to run the task.</span></span>

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

### <span data-ttu-id="06209-139">-Applicationpackagereferfer</span><span class="sxs-lookup"><span data-stu-id="06209-139">-ApplicationPackageReferences</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06209-140">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="06209-140">-BatchContext</span></span>
<span data-ttu-id="06209-141">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="06209-141">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="06209-142">Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** nesnesi edinmek için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="06209-142">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="06209-143">-CommandLine</span><span class="sxs-lookup"><span data-stu-id="06209-143">-CommandLine</span></span>
<span data-ttu-id="06209-144">Görevin komut satırını belirtir.</span><span class="sxs-lookup"><span data-stu-id="06209-144">Specifies the command line for the task.</span></span>

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

### <span data-ttu-id="06209-145">-Kısıtlamalar</span><span class="sxs-lookup"><span data-stu-id="06209-145">-Constraints</span></span>
<span data-ttu-id="06209-146">Bu göreve uygulanan yürütme kısıtlamalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="06209-146">Specifies the execution constraints that apply to this task.</span></span>

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

### <span data-ttu-id="06209-147">-Bağımlılson</span><span class="sxs-lookup"><span data-stu-id="06209-147">-DependsOn</span></span>
<span data-ttu-id="06209-148">Görevin diğer görevlere bağlı olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="06209-148">Specifies that the task depends on other tasks.</span></span>
<span data-ttu-id="06209-149">Tüm bağlı görevler başarıyla tamamlanıncaya kadar görev planlanmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="06209-149">The task will not be scheduled until all depended-on tasks have completed successfully.</span></span>

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

### <span data-ttu-id="06209-150">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="06209-150">-DisplayName</span></span>
<span data-ttu-id="06209-151">Görevin görünen adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="06209-151">Specifies the display name of the task.</span></span>

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

### <span data-ttu-id="06209-152">-EnvironmentSettings</span><span class="sxs-lookup"><span data-stu-id="06209-152">-EnvironmentSettings</span></span>
<span data-ttu-id="06209-153">Anahtar/değer çiftleri olarak, bu cmdlet 'in göreve eklediği ortam ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="06209-153">Specifies the environment settings, as key/value pairs, that this cmdlet adds to the task.</span></span>
<span data-ttu-id="06209-154">Anahtar, ortam ayarı adıdır.</span><span class="sxs-lookup"><span data-stu-id="06209-154">The key is the environment setting name.</span></span>
<span data-ttu-id="06209-155">Değer, ortam ayarıdır.</span><span class="sxs-lookup"><span data-stu-id="06209-155">The value is the environment setting.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06209-156">-ExitConditions</span><span class="sxs-lookup"><span data-stu-id="06209-156">-ExitConditions</span></span>
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

### <span data-ttu-id="06209-157">-ID</span><span class="sxs-lookup"><span data-stu-id="06209-157">-Id</span></span>
<span data-ttu-id="06209-158">Görevin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="06209-158">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="06209-159">-Job</span><span class="sxs-lookup"><span data-stu-id="06209-159">-Job</span></span>
<span data-ttu-id="06209-160">Bu cmdlet 'in görev oluşturduğu işi belirtir.</span><span class="sxs-lookup"><span data-stu-id="06209-160">Specifies the job under which this cmdlet creates the task.</span></span>
<span data-ttu-id="06209-161">Bir **Ince iş** nesnesi edinmek için Get-AzureBatchJob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="06209-161">To obtain a **PSCloudJob** object, use the Get-AzureBatchJob cmdlet.</span></span>

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

### <span data-ttu-id="06209-162">-JobId</span><span class="sxs-lookup"><span data-stu-id="06209-162">-JobId</span></span>
<span data-ttu-id="06209-163">Bu cmdlet 'in görev oluşturduğu işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="06209-163">Specifies the ID of the job under which this cmdlet creates the task.</span></span>

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

### <span data-ttu-id="06209-164">-Multiınstancesettings</span><span class="sxs-lookup"><span data-stu-id="06209-164">-MultiInstanceSettings</span></span>
<span data-ttu-id="06209-165">Çok örnekli bir görevin nasıl çalıştırılacağı hakkında bilgi belirtir.</span><span class="sxs-lookup"><span data-stu-id="06209-165">Specifies information about how to run a multi-instance task.</span></span>

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

### <span data-ttu-id="06209-166">-ResourceFiles</span><span class="sxs-lookup"><span data-stu-id="06209-166">-ResourceFiles</span></span>
<span data-ttu-id="06209-167">Kaynak dosyalarını anahtar/değer çiftleri olarak, görevin gerektirdiği şekilde belirtir.</span><span class="sxs-lookup"><span data-stu-id="06209-167">Specifies resource files, as key/value pairs, that the task requires.</span></span>
<span data-ttu-id="06209-168">Anahtar, kaynak dosyası yoludur.</span><span class="sxs-lookup"><span data-stu-id="06209-168">The key is the resource file path.</span></span>
<span data-ttu-id="06209-169">Değer, kaynak dosyası blob kaynağıdır.</span><span class="sxs-lookup"><span data-stu-id="06209-169">The value is the resource file blob source.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06209-170">-Runyükselmesine</span><span class="sxs-lookup"><span data-stu-id="06209-170">-RunElevated</span></span>
<span data-ttu-id="06209-171">Görev işleminin Yönetici ayrıcalıklarıyla çalışacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="06209-171">Indicates that the task process runs with administrator privileges.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: JobId_Single, JobObject_Single
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06209-172">-Görevler</span><span class="sxs-lookup"><span data-stu-id="06209-172">-Tasks</span></span>
<span data-ttu-id="06209-173">Eklenecek görevlerin koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="06209-173">Specifies the collection of tasks to be added.</span></span>
<span data-ttu-id="06209-174">Her görevin benzersiz bir KIMLIĞI olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="06209-174">Each task must have a unique ID.</span></span>

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

### <span data-ttu-id="06209-175">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06209-175">-DefaultProfile</span></span>
<span data-ttu-id="06209-176">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="06209-176">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06209-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06209-177">CommonParameters</span></span>
<span data-ttu-id="06209-178">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="06209-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06209-179">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06209-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06209-180">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="06209-180">INPUTS</span></span>

### <span data-ttu-id="06209-181">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="06209-181">BatchAccountContext</span></span>
<span data-ttu-id="06209-182">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="06209-182">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="06209-183">Pschoparlör Işi</span><span class="sxs-lookup"><span data-stu-id="06209-183">PSCloudJob</span></span>
<span data-ttu-id="06209-184">Parametre ' Iş ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="06209-184">Parameter 'Job' accepts value of type 'PSCloudJob' from the pipeline</span></span>

## <span data-ttu-id="06209-185">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="06209-185">OUTPUTS</span></span>

## <span data-ttu-id="06209-186">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="06209-186">NOTES</span></span>

## <span data-ttu-id="06209-187">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="06209-187">RELATED LINKS</span></span>

[<span data-ttu-id="06209-188">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="06209-188">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="06209-189">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="06209-189">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="06209-190">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="06209-190">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="06209-191">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="06209-191">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="06209-192">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="06209-192">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="06209-193">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="06209-193">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="06209-194">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="06209-194">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


