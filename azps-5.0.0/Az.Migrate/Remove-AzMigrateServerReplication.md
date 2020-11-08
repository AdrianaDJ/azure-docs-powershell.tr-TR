---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/remove-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateServerReplication.md
ms.openlocfilehash: e9e6d3f9c045b9ff9cc2d5a4860b2c7fc5559f14
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278627"
---
# <span data-ttu-id="f4453-101">Remove-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="f4453-101">Remove-AzMigrateServerReplication</span></span>

## <span data-ttu-id="f4453-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4453-102">SYNOPSIS</span></span>
<span data-ttu-id="f4453-103">Geçirilmiş sunucu için çoğaltmayı durdurur.</span><span class="sxs-lookup"><span data-stu-id="f4453-103">Stops replication for the migrated server.</span></span>

## <span data-ttu-id="f4453-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f4453-104">SYNTAX</span></span>

### <span data-ttu-id="f4453-105">Byıdvmwarecbt (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f4453-105">ByIDVMwareCbt (Default)</span></span>
```
Remove-AzMigrateServerReplication -TargetObjectID <String> [-SubscriptionId <String>] [-ForceRemove <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f4453-106">Byinputobjectvmwareci</span><span class="sxs-lookup"><span data-stu-id="f4453-106">ByInputObjectVMwareCbt</span></span>
```
Remove-AzMigrateServerReplication -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-ForceRemove <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f4453-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f4453-107">DESCRIPTION</span></span>
<span data-ttu-id="f4453-108">Remove-AzMigrateServerReplication cmdlet 'i geçirilmiş bir sunucu için çoğaltmayı durdurur.</span><span class="sxs-lookup"><span data-stu-id="f4453-108">The Remove-AzMigrateServerReplication cmdlet stops the replication for a migrated server.</span></span>

## <span data-ttu-id="f4453-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f4453-109">EXAMPLES</span></span>

### <span data-ttu-id="f4453-110">Örnek 1: kimliğe göre kaldır.</span><span class="sxs-lookup"><span data-stu-id="f4453-110">Example 1: Remove by id.</span></span>
```powershell
PS C:\> Remove-AzMigrateServerReplication -TargetObjectID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f"

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Disable
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Disable
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="f4453-111">Kimliğe göre yeniden eşitleme.</span><span class="sxs-lookup"><span data-stu-id="f4453-111">Resync by id.</span></span>

### <span data-ttu-id="f4453-112">Örnek 2: giriş nesnesine göre kaldırma</span><span class="sxs-lookup"><span data-stu-id="f4453-112">Example 2: Remove by Input Object</span></span>
```powershell
PS C:\> $obj = Get-AzMigrateServerReplication -TargetObjectID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f"
PS C:\> Remove-AzMigrateServerReplication -InputObject $obj


ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Disable
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Disable
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="f4453-113">Ada göre.</span><span class="sxs-lookup"><span data-stu-id="f4453-113">By name.</span></span>

## <span data-ttu-id="f4453-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f4453-114">PARAMETERS</span></span>

### <span data-ttu-id="f4453-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4453-115">-DefaultProfile</span></span>
<span data-ttu-id="f4453-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f4453-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4453-117">-Forceretaþý</span><span class="sxs-lookup"><span data-stu-id="f4453-117">-ForceRemove</span></span>
<span data-ttu-id="f4453-118">Çoğaltmanın zorla kaldırılması gerekip gerekmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f4453-118">Specifies whether the replication needs to be force removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4453-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4453-119">-InputObject</span></span>
<span data-ttu-id="f4453-120">Çoğaltma sunucusunun makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f4453-120">Specifies the machine object of the replicating server.</span></span>
<span data-ttu-id="f4453-121">Oluşturmak için, ıNPUTOBJECT özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f4453-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f4453-122">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="f4453-122">-SubscriptionId</span></span>
<span data-ttu-id="f4453-123">Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="f4453-123">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="f4453-124">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="f4453-124">-TargetObjectID</span></span>
<span data-ttu-id="f4453-125">Replicatio 'in devre dışı bırakılması gereken repltonlu sunucuyu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f4453-125">Specifies the replcating server for which the replicatio needs to be disabled.</span></span>
<span data-ttu-id="f4453-126">KIMLIK, Get-AzMigrateServerReplication cmdlet kullanılarak alınmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f4453-126">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="f4453-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4453-127">CommonParameters</span></span>
<span data-ttu-id="f4453-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f4453-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4453-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f4453-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4453-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f4453-130">INPUTS</span></span>

## <span data-ttu-id="f4453-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f4453-131">OUTPUTS</span></span>

### <span data-ttu-id="f4453-132">Microsoft. Azure. PowerShell. cmdlet. geçir. modeller. Api20180110. ıjob</span><span class="sxs-lookup"><span data-stu-id="f4453-132">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="f4453-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f4453-133">NOTES</span></span>

<span data-ttu-id="f4453-134">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="f4453-134">ALIASES</span></span>

<span data-ttu-id="f4453-135">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="f4453-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f4453-136">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f4453-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f4453-137">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f4453-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f4453-138">INPUTOBJECT <IMigrationItem> : Çoğaltma sunucusunun makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f4453-138">INPUTOBJECT <IMigrationItem>: Specifies the machine object of the replicating server.</span></span>
  - <span data-ttu-id="f4453-139">`[Location <String>]`: Kaynak konumu</span><span class="sxs-lookup"><span data-stu-id="f4453-139">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="f4453-140">`[CurrentJobId <String>]`: Yürütülen işin ARM kimliği.</span><span class="sxs-lookup"><span data-stu-id="f4453-140">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="f4453-141">`[CurrentJobName <String>]`: İş adı.</span><span class="sxs-lookup"><span data-stu-id="f4453-141">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="f4453-142">`[CurrentJobStartTime <DateTime?>]`: İşin başlangıç saati.</span><span class="sxs-lookup"><span data-stu-id="f4453-142">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="f4453-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Geçiş sağlayıcısı özel ayarları.</span><span class="sxs-lookup"><span data-stu-id="f4453-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="f4453-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f4453-144">RELATED LINKS</span></span>

