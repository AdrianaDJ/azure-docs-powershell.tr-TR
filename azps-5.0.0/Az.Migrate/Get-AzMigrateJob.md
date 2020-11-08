---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
ms.openlocfilehash: bb28550a0b23fa9032832873a78771d25d2a38bd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280073"
---
# <span data-ttu-id="26956-101">Get-AzMigrateJob</span><span class="sxs-lookup"><span data-stu-id="26956-101">Get-AzMigrateJob</span></span>

## <span data-ttu-id="26956-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26956-102">SYNOPSIS</span></span>
<span data-ttu-id="26956-103">Bir Azure geçiş işinin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="26956-103">Retrieves the status of an Azure Migrate job.</span></span>

## <span data-ttu-id="26956-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="26956-104">SYNTAX</span></span>

### <span data-ttu-id="26956-105">ListByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="26956-105">ListByName (Default)</span></span>
```
Get-AzMigrateJob -ProjectName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="26956-106">GetById</span><span class="sxs-lookup"><span data-stu-id="26956-106">GetById</span></span>
```
Get-AzMigrateJob -JobID <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="26956-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="26956-107">GetByInputObject</span></span>
```
Get-AzMigrateJob -InputObject <IJob> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="26956-108">GetByName</span><span class="sxs-lookup"><span data-stu-id="26956-108">GetByName</span></span>
```
Get-AzMigrateJob -JobName <String> -ProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="26956-109">Liste</span><span class="sxs-lookup"><span data-stu-id="26956-109">ListById</span></span>
```
Get-AzMigrateJob -ProjectID <String> -ResourceGroupID <String> [-SubscriptionId <String>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="26956-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="26956-110">DESCRIPTION</span></span>
<span data-ttu-id="26956-111">Get-AzMigrateJob cmdlet 'i, bir Azure geçiş işinin durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="26956-111">The Get-AzMigrateJob cmdlet retrives the status of an Azure Migrate job.</span></span>

## <span data-ttu-id="26956-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="26956-112">EXAMPLES</span></span>

### <span data-ttu-id="26956-113">Örnek 1: Iş kimliğine göre alma</span><span class="sxs-lookup"><span data-stu-id="26956-113">Example 1: Get By Job Id</span></span>
```powershell
PS C:\> Get-AzMigrateJob -JobID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b" 

ActivityId                       : 68af14b4-46ae-48d1-b3e9-cdcffb9e8a93 ActivityId: 74d1a396-1d37-4264-8a5b-b727aaef0171
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 9/16/20 11:57:33 AM
Error                            : {}
FriendlyName                     : Associate replication policy
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b
Location                         :
Name                             : 997e2a92-5afe-49c7-a81a-89660aec9b7b
ScenarioName                     : AssociateProtectionProfile
StartTime                        : 9/16/20 11:57:32 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 42752b89-5fad-52fd-bf93-679fbdb6fed9
TargetObjectName                 : migrateAzMigratePWSHTc8d1sitepolicy
Task                             : {CloudPairingPrerequisitesCheck, CloudPairingPrepareSite}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="26956-114">Bu, bir işi kimliğiyle alır.</span><span class="sxs-lookup"><span data-stu-id="26956-114">This retrieves a job by it's Id.</span></span>

### <span data-ttu-id="26956-115">Örnek 2: kaynak grubuna ve projeye göre liste</span><span class="sxs-lookup"><span data-stu-id="26956-115">Example 2: List by resource group and project</span></span>
```powershell
PS C:\> Get-AzMigrateJob -ResourceGroupName 'azmigratepwshtestasr13072020' -ProjectName 'AzMigrateTestProjectPWSH'

ActivityId                       :
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         :
EndTime                          : 9/21/20 4:13:40 PM
Error                            : {}
FriendlyName                     : Update the virtual machine
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/1c89e38e-34ec-4903-aa7c-115201bf2de1
Location                         :
Name                             : 1c89e38e-34ec-4903-aa7c-115201bf2de1
ScenarioName                     : UpdateVmProperties
StartTime                        : 9/21/20 4:13:34 PM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 593b735d-2a34-53b2-b8ed-e33da5650703
TargetObjectName                 : rb-w2k12r2-1
Task                             : {}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="26956-116">Bu, projedeki tüm işleri alır.</span><span class="sxs-lookup"><span data-stu-id="26956-116">This gets all jobs in a project.</span></span>

### <span data-ttu-id="26956-117">Örnek 3: kaynak grubuna, projeye ve iş adına göre alma</span><span class="sxs-lookup"><span data-stu-id="26956-117">Example 3: Get by resource group, project and job name</span></span>
```powershell
PS C:\> Get-AzMigrateJob -ResourceGroupName 'azmigratepwshtestasr13072020' -ProjectName 'AzMigrateTestProjectPWSH' -JobName 7ae1ee7c-442c-499d-8b0e-81d52a42b71e

ActivityId                       : 6986b7e5-0f1f-49d8-8b4b-77e6f66bcb92 ActivityId: eb73c6a1-7c66-469f-a853-d896aa38cc0f
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 8/21/20 6:41:48 AM
Error                            : {}
FriendlyName                     : Create replication policy
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/7ae1ee7c-442c-499d-8b0e-81d52a42b71e
Location                         :
Name                             : 7ae1ee7c-442c-499d-8b0e-81d52a42b71e
ScenarioName                     : AddProtectionProfile
StartTime                        : 8/21/20 6:41:48 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 18b2ccec-e39a-517b-ae5d-dd395e9f4f96
TargetObjectName                 : samplePolicy3
Task                             : {AddProtectionProfilePreflightsCheckTask, AddProtectionProfileTask}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="26956-118">Bu belirli bir iş alır.</span><span class="sxs-lookup"><span data-stu-id="26956-118">This gets a specific job.</span></span>

## <span data-ttu-id="26956-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="26956-119">PARAMETERS</span></span>

### <span data-ttu-id="26956-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26956-120">-DefaultProfile</span></span>
<span data-ttu-id="26956-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="26956-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26956-122">-Filtre</span><span class="sxs-lookup"><span data-stu-id="26956-122">-Filter</span></span>
<span data-ttu-id="26956-123">OData filtre seçenekleri.</span><span class="sxs-lookup"><span data-stu-id="26956-123">OData filter options.</span></span>

```yaml
Type: System.String
Parameter Sets: ListById, ListByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26956-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26956-124">-InputObject</span></span>
<span data-ttu-id="26956-125">Çoğaltma sunucusunun iş nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="26956-125">Specifies the job object of the replicating server.</span></span>
<span data-ttu-id="26956-126">Oluşturmak için, ıNPUTOBJECT özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="26956-126">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob
Parameter Sets: GetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26956-127">-JobId</span><span class="sxs-lookup"><span data-stu-id="26956-127">-JobID</span></span>
<span data-ttu-id="26956-128">Ayrıntıların alınması gereken iş kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="26956-128">Specifies the job id for which the details needs to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26956-129">-JobName</span><span class="sxs-lookup"><span data-stu-id="26956-129">-JobName</span></span>
<span data-ttu-id="26956-130">İş tanımlayıcısı</span><span class="sxs-lookup"><span data-stu-id="26956-130">Job identifier</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26956-131">-ProjectID</span><span class="sxs-lookup"><span data-stu-id="26956-131">-ProjectID</span></span>
<span data-ttu-id="26956-132">Sunucularda çoğaltma yapan Azure geçiş projesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="26956-132">Specifies the Azure Migrate Project in which servers are replicating.</span></span>

```yaml
Type: System.String
Parameter Sets: ListById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26956-133">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="26956-133">-ProjectName</span></span>
<span data-ttu-id="26956-134">Proje geçirme adı.</span><span class="sxs-lookup"><span data-stu-id="26956-134">The name of the migrate project.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName, ListByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26956-135">-Resourcegroupıd</span><span class="sxs-lookup"><span data-stu-id="26956-135">-ResourceGroupID</span></span>
<span data-ttu-id="26956-136">Geçerli abonelikteki Azure geçiş projesi kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="26956-136">Specifies the Resource Group of the Azure Migrate Project in the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ListById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26956-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26956-137">-ResourceGroupName</span></span>
<span data-ttu-id="26956-138">Kurtarma Hizmetleri kasasındaki kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="26956-138">The name of the resource group where the recovery services vault is present.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName, ListByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26956-139">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="26956-139">-SubscriptionId</span></span>
<span data-ttu-id="26956-140">Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="26956-140">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26956-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26956-141">CommonParameters</span></span>
<span data-ttu-id="26956-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="26956-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26956-143">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="26956-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26956-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="26956-144">INPUTS</span></span>

## <span data-ttu-id="26956-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="26956-145">OUTPUTS</span></span>

### <span data-ttu-id="26956-146">Microsoft. Azure. PowerShell. cmdlet. geçir. modeller. Api20180110. ıjob</span><span class="sxs-lookup"><span data-stu-id="26956-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="26956-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="26956-147">NOTES</span></span>

<span data-ttu-id="26956-148">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="26956-148">ALIASES</span></span>

<span data-ttu-id="26956-149">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="26956-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="26956-150">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="26956-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="26956-151">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="26956-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="26956-152">INPUTOBJECT <IJob> : Çoğaltma sunucusunun iş nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="26956-152">INPUTOBJECT <IJob>: Specifies the job object of the replicating server.</span></span>
  - <span data-ttu-id="26956-153">`[Location <String>]`: Kaynak konumu</span><span class="sxs-lookup"><span data-stu-id="26956-153">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="26956-154">`[ActivityId <String>]`: Etkinlik kimliği.</span><span class="sxs-lookup"><span data-stu-id="26956-154">`[ActivityId <String>]`: The activity id.</span></span>
  - <span data-ttu-id="26956-155">`[AllowedAction <String[]>]`: İşe Izin verilen eylem.</span><span class="sxs-lookup"><span data-stu-id="26956-155">`[AllowedAction <String[]>]`: The Allowed action the job.</span></span>
  - <span data-ttu-id="26956-156">`[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`: Kaynak sunucu, kaynak bulut, hedef sunucu, hedef bulut gibi etkilenen nesne özellikleri iş akışı nesnesi ayrıntılarına göre.</span><span class="sxs-lookup"><span data-stu-id="26956-156">`[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`: The affected object properties like source server, source cloud, target server, target cloud etc. based on the workflow object details.</span></span>
    - <span data-ttu-id="26956-157">`[(Any) <String>]`: Bu, hiçbir özelliğin bu nesneye ekleneolabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="26956-157">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="26956-158">`[EndTime <DateTime?>]`: Bitiş saati.</span><span class="sxs-lookup"><span data-stu-id="26956-158">`[EndTime <DateTime?>]`: The end time.</span></span>
  - <span data-ttu-id="26956-159">`[Error <IJobErrorDetails[]>]`: Hatalar.</span><span class="sxs-lookup"><span data-stu-id="26956-159">`[Error <IJobErrorDetails[]>]`: The errors.</span></span>
    - <span data-ttu-id="26956-160">`[CreationTime <DateTime?>]`: İş hatasının oluşturulma zamanı.</span><span class="sxs-lookup"><span data-stu-id="26956-160">`[CreationTime <DateTime?>]`: The creation time of job error.</span></span>
    - <span data-ttu-id="26956-161">`[ErrorLevel <String>]`: Hata düzeyi hata.</span><span class="sxs-lookup"><span data-stu-id="26956-161">`[ErrorLevel <String>]`: Error level of error.</span></span>
    - <span data-ttu-id="26956-162">`[ProviderErrorDetailErrorCode <Int32?>]`: Hata kodu.</span><span class="sxs-lookup"><span data-stu-id="26956-162">`[ProviderErrorDetailErrorCode <Int32?>]`: The Error code.</span></span>
    - <span data-ttu-id="26956-163">`[ProviderErrorDetailErrorId <String>]`: Sağlayıcı hata kimliği.</span><span class="sxs-lookup"><span data-stu-id="26956-163">`[ProviderErrorDetailErrorId <String>]`: The Provider error Id.</span></span>
    - <span data-ttu-id="26956-164">`[ProviderErrorDetailErrorMessage <String>]`: Hata iletisi.</span><span class="sxs-lookup"><span data-stu-id="26956-164">`[ProviderErrorDetailErrorMessage <String>]`: The Error message.</span></span>
    - <span data-ttu-id="26956-165">`[ProviderErrorDetailPossibleCaus <String>]`: Hatanın olası nedenleri.</span><span class="sxs-lookup"><span data-stu-id="26956-165">`[ProviderErrorDetailPossibleCaus <String>]`: The possible causes for the error.</span></span>
    - <span data-ttu-id="26956-166">`[ProviderErrorDetailRecommendedAction <String>]`: Hatayı çözmek için önerilen eylem.</span><span class="sxs-lookup"><span data-stu-id="26956-166">`[ProviderErrorDetailRecommendedAction <String>]`: The recommended action to resolve the error.</span></span>
    - <span data-ttu-id="26956-167">`[ServiceErrorDetailActivityId <String>]`: Etkinlik kimliği.</span><span class="sxs-lookup"><span data-stu-id="26956-167">`[ServiceErrorDetailActivityId <String>]`: Activity Id.</span></span>
    - <span data-ttu-id="26956-168">`[ServiceErrorDetailCode <String>]`: Hata kodu.</span><span class="sxs-lookup"><span data-stu-id="26956-168">`[ServiceErrorDetailCode <String>]`: Error code.</span></span>
    - <span data-ttu-id="26956-169">`[ServiceErrorDetailMessage <String>]`: Hata iletisi.</span><span class="sxs-lookup"><span data-stu-id="26956-169">`[ServiceErrorDetailMessage <String>]`: Error message.</span></span>
    - <span data-ttu-id="26956-170">`[ServiceErrorDetailPossibleCaus <String>]`: Hatanın olası nedenleri.</span><span class="sxs-lookup"><span data-stu-id="26956-170">`[ServiceErrorDetailPossibleCaus <String>]`: Possible causes of error.</span></span>
    - <span data-ttu-id="26956-171">`[ServiceErrorDetailRecommendedAction <String>]`: Hatayı çözmek için önerilen eylem.</span><span class="sxs-lookup"><span data-stu-id="26956-171">`[ServiceErrorDetailRecommendedAction <String>]`: Recommended action to resolve error.</span></span>
    - <span data-ttu-id="26956-172">`[TaskId <String>]`: Görevin kimliği.</span><span class="sxs-lookup"><span data-stu-id="26956-172">`[TaskId <String>]`: The Id of the task.</span></span>
  - <span data-ttu-id="26956-173">`[FriendlyName <String>]`: DisplayName.</span><span class="sxs-lookup"><span data-stu-id="26956-173">`[FriendlyName <String>]`: The DisplayName.</span></span>
  - <span data-ttu-id="26956-174">`[ScenarioName <String>]`: ScenarioName.</span><span class="sxs-lookup"><span data-stu-id="26956-174">`[ScenarioName <String>]`: The ScenarioName.</span></span>
  - <span data-ttu-id="26956-175">`[StartTime <DateTime?>]`: Başlangıç saati.</span><span class="sxs-lookup"><span data-stu-id="26956-175">`[StartTime <DateTime?>]`: The start time.</span></span>
  - <span data-ttu-id="26956-176">`[State <String>]`: Işin durumu.</span><span class="sxs-lookup"><span data-stu-id="26956-176">`[State <String>]`: The status of the Job.</span></span> <span data-ttu-id="26956-177">Bu değerlerden biri-NotStarted, InProgress, başarılı, başarısız, Iptal edildi, askıya alınmış veya diğer değerlerinden biridir.</span><span class="sxs-lookup"><span data-stu-id="26956-177">It is one of these values - NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended or Other.</span></span>
  - <span data-ttu-id="26956-178">`[StateDescription <String>]`: Işin durumunun açıklaması.</span><span class="sxs-lookup"><span data-stu-id="26956-178">`[StateDescription <String>]`: The description of the state of the Job.</span></span> <span data-ttu-id="26956-179">Örneğin, tamamlandı durumu için, açıklama tamamlanabilir, PartiallySucceeded, Completedwithınformation veya atlandı.</span><span class="sxs-lookup"><span data-stu-id="26956-179">For e.g. - For Succeeded state, description can be Completed, PartiallySucceeded, CompletedWithInformation or Skipped.</span></span>
  - <span data-ttu-id="26956-180">`[TargetInstanceType <String>]`: {Microsoft.Azure.SiteRecovery.V2015_11_10. AffectedObjectType} sınıfının etkilenen nesnesinin türü.</span><span class="sxs-lookup"><span data-stu-id="26956-180">`[TargetInstanceType <String>]`: The type of the affected object which is of {Microsoft.Azure.SiteRecovery.V2015_11_10.AffectedObjectType} class.</span></span>
  - <span data-ttu-id="26956-181">`[TargetObjectId <String>]`: Etkilenen nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="26956-181">`[TargetObjectId <String>]`: The affected Object Id.</span></span>
  - <span data-ttu-id="26956-182">`[TargetObjectName <String>]`: Etkilenen nesnenin adı.</span><span class="sxs-lookup"><span data-stu-id="26956-182">`[TargetObjectName <String>]`: The name of the affected object.</span></span>
  - <span data-ttu-id="26956-183">`[Task <IAsrTask[]>]`: Görevler.</span><span class="sxs-lookup"><span data-stu-id="26956-183">`[Task <IAsrTask[]>]`: The tasks.</span></span>
    - <span data-ttu-id="26956-184">`[AllowedAction <String[]>]`: Bu görevde uygulanabilir durum/eylemler.</span><span class="sxs-lookup"><span data-stu-id="26956-184">`[AllowedAction <String[]>]`: The state/actions applicable on this task.</span></span>
    - <span data-ttu-id="26956-185">`[CustomDetailInstanceType <String>]`: Görev ayrıntılarının türü.</span><span class="sxs-lookup"><span data-stu-id="26956-185">`[CustomDetailInstanceType <String>]`: The type of task details.</span></span>
    - <span data-ttu-id="26956-186">`[EndTime <DateTime?>]`: Bitiş saati.</span><span class="sxs-lookup"><span data-stu-id="26956-186">`[EndTime <DateTime?>]`: The end time.</span></span>
    - <span data-ttu-id="26956-187">`[Error <IJobErrorDetails[]>]`: Görev hata ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="26956-187">`[Error <IJobErrorDetails[]>]`: The task error details.</span></span>
    - <span data-ttu-id="26956-188">`[FriendlyName <String>]`: Ad.</span><span class="sxs-lookup"><span data-stu-id="26956-188">`[FriendlyName <String>]`: The name.</span></span>
    - <span data-ttu-id="26956-189">`[GroupTaskCustomDetailChildTask <IAsrTask[]>]`: Alt görevler.</span><span class="sxs-lookup"><span data-stu-id="26956-189">`[GroupTaskCustomDetailChildTask <IAsrTask[]>]`: The child tasks.</span></span>
    - <span data-ttu-id="26956-190">`[GroupTaskCustomDetailInstanceType <String>]`: Görev ayrıntılarının türü.</span><span class="sxs-lookup"><span data-stu-id="26956-190">`[GroupTaskCustomDetailInstanceType <String>]`: The type of task details.</span></span>
    - <span data-ttu-id="26956-191">`[Name <String>]`: Benzersiz görev adı.</span><span class="sxs-lookup"><span data-stu-id="26956-191">`[Name <String>]`: The unique Task name.</span></span>
    - <span data-ttu-id="26956-192">`[StartTime <DateTime?>]`: Başlangıç saati.</span><span class="sxs-lookup"><span data-stu-id="26956-192">`[StartTime <DateTime?>]`: The start time.</span></span>
    - <span data-ttu-id="26956-193">`[State <String>]`: Eyalet.</span><span class="sxs-lookup"><span data-stu-id="26956-193">`[State <String>]`: The State.</span></span> <span data-ttu-id="26956-194">Bu değerlerden biri-NotStarted, InProgress, başarılı, başarısız, Iptal edildi, askıya alınmış veya diğer değerlerinden biridir.</span><span class="sxs-lookup"><span data-stu-id="26956-194">It is one of these values - NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended or Other.</span></span>
    - <span data-ttu-id="26956-195">`[StateDescription <String>]`: Görev durumunun açıklaması.</span><span class="sxs-lookup"><span data-stu-id="26956-195">`[StateDescription <String>]`: The description of the task state.</span></span> <span data-ttu-id="26956-196">Örneğin, başarılı durum Için, açıklama tamamlanabilir, PartiallySucceeded, Completedwithınformation veya atlandı.</span><span class="sxs-lookup"><span data-stu-id="26956-196">For example - For Succeeded state, description can be Completed, PartiallySucceeded, CompletedWithInformation or Skipped.</span></span>
    - <span data-ttu-id="26956-197">`[TaskId <String>]`: Kimlik.</span><span class="sxs-lookup"><span data-stu-id="26956-197">`[TaskId <String>]`: The Id.</span></span>
    - <span data-ttu-id="26956-198">`[TaskType <String>]`: Görevin türü.</span><span class="sxs-lookup"><span data-stu-id="26956-198">`[TaskType <String>]`: The type of task.</span></span> <span data-ttu-id="26956-199">CustomDetails özelliğindeki Ayrıntılar bu türe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="26956-199">Details in CustomDetails property depend on this type.</span></span>

## <span data-ttu-id="26956-200">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="26956-200">RELATED LINKS</span></span>

