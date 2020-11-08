---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/restart-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Restart-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Restart-AzMigrateServerReplication.md
ms.openlocfilehash: 35bf416249f24d7158720e2a9c28230da3f4f291
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278624"
---
# <span data-ttu-id="7a53b-101">Restart-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="7a53b-101">Restart-AzMigrateServerReplication</span></span>

## <span data-ttu-id="7a53b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a53b-102">SYNOPSIS</span></span>
<span data-ttu-id="7a53b-103">Belirtilen sunucu için çoğaltmayı yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="7a53b-103">Restarts the replication for specified server.</span></span>

## <span data-ttu-id="7a53b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7a53b-104">SYNTAX</span></span>

### <span data-ttu-id="7a53b-105">Byıdvmwarecbt (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7a53b-105">ByIDVMwareCbt (Default)</span></span>
```
Restart-AzMigrateServerReplication -TargetObjectID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7a53b-106">Byinputobjectvmwareci</span><span class="sxs-lookup"><span data-stu-id="7a53b-106">ByInputObjectVMwareCbt</span></span>
```
Restart-AzMigrateServerReplication -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7a53b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7a53b-107">DESCRIPTION</span></span>
<span data-ttu-id="7a53b-108">Restart-AzMigrateServerReplication cmdlet 'i belirtilen sunucu için yinelemeyi onarır.</span><span class="sxs-lookup"><span data-stu-id="7a53b-108">The Restart-AzMigrateServerReplication cmdlet repairs the replication for the specified server.</span></span>

## <span data-ttu-id="7a53b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7a53b-109">EXAMPLES</span></span>

### <span data-ttu-id="7a53b-110">Örnek 1: kimliğe göre.</span><span class="sxs-lookup"><span data-stu-id="7a53b-110">Example 1: By id.</span></span>
```powershell
PS C:\> Restart-AzMigrateServerReplication -TargetObjectID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f"

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Restart
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Restart
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="7a53b-111">Kimliğe göre.</span><span class="sxs-lookup"><span data-stu-id="7a53b-111">By id.</span></span>

### <span data-ttu-id="7a53b-112">Örnek 2: giriş nesnesine göre</span><span class="sxs-lookup"><span data-stu-id="7a53b-112">Example 2: By Input Object</span></span>
```powershell
PS C:\> $obj = Get-AzMigrateServerReplication -TargetObjectID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f"
PS C:\> $output = Restart-AzMigrateServerReplication -InputObject $obj
ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Restart
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Restart
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="7a53b-113">Giriş nesnesine göre.</span><span class="sxs-lookup"><span data-stu-id="7a53b-113">By Input Object.</span></span>

## <span data-ttu-id="7a53b-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7a53b-114">PARAMETERS</span></span>

### <span data-ttu-id="7a53b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a53b-115">-DefaultProfile</span></span>
<span data-ttu-id="7a53b-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7a53b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a53b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a53b-117">-InputObject</span></span>
<span data-ttu-id="7a53b-118">Çoğaltma sunucusunun makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a53b-118">Specifies the machine object of the replicating server.</span></span>
<span data-ttu-id="7a53b-119">Oluşturmak için, ıNPUTOBJECT özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7a53b-119">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IMigrationItem
Parameter Sets: ByInputObjectVMwareCbt
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a53b-120">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="7a53b-120">-SubscriptionId</span></span>
<span data-ttu-id="7a53b-121">Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="7a53b-121">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="7a53b-122">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="7a53b-122">-TargetObjectID</span></span>
<span data-ttu-id="7a53b-123">Yeniden eşitlerinizin başlatılması gereken repltonlu sunucuyu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a53b-123">Specifies the replcating server for which the resync needs to be initiated.</span></span>
<span data-ttu-id="7a53b-124">KIMLIK, Get-AzMigrateServerReplication cmdlet kullanılarak alınmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7a53b-124">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIDVMwareCbt
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a53b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a53b-125">CommonParameters</span></span>
<span data-ttu-id="7a53b-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7a53b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a53b-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7a53b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a53b-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7a53b-128">INPUTS</span></span>

## <span data-ttu-id="7a53b-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7a53b-129">OUTPUTS</span></span>

### <span data-ttu-id="7a53b-130">Microsoft. Azure. PowerShell. cmdlet. geçir. modeller. Api20180110. ıjob</span><span class="sxs-lookup"><span data-stu-id="7a53b-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="7a53b-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7a53b-131">NOTES</span></span>

<span data-ttu-id="7a53b-132">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="7a53b-132">ALIASES</span></span>

<span data-ttu-id="7a53b-133">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="7a53b-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7a53b-134">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7a53b-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7a53b-135">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7a53b-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7a53b-136">INPUTOBJECT <IMigrationItem> : Çoğaltma sunucusunun makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a53b-136">INPUTOBJECT <IMigrationItem>: Specifies the machine object of the replicating server.</span></span>
  - <span data-ttu-id="7a53b-137">`[Location <String>]`: Kaynak konumu</span><span class="sxs-lookup"><span data-stu-id="7a53b-137">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="7a53b-138">`[CurrentJobId <String>]`: Yürütülen işin ARM kimliği.</span><span class="sxs-lookup"><span data-stu-id="7a53b-138">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="7a53b-139">`[CurrentJobName <String>]`: İş adı.</span><span class="sxs-lookup"><span data-stu-id="7a53b-139">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="7a53b-140">`[CurrentJobStartTime <DateTime?>]`: İşin başlangıç saati.</span><span class="sxs-lookup"><span data-stu-id="7a53b-140">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="7a53b-141">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Geçiş sağlayıcısı özel ayarları.</span><span class="sxs-lookup"><span data-stu-id="7a53b-141">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="7a53b-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7a53b-142">RELATED LINKS</span></span>

