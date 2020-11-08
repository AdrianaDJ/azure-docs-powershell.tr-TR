---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/start-azmigratetestmigrationcleanup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigrationCleanup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigrationCleanup.md
ms.openlocfilehash: df4eac2c6380c36dcd07c906ccbbee4d2a93f27b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278619"
---
# <span data-ttu-id="6f716-101">Start-AzMigrateTestMigrationCleanup</span><span class="sxs-lookup"><span data-stu-id="6f716-101">Start-AzMigrateTestMigrationCleanup</span></span>

## <span data-ttu-id="6f716-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f716-102">SYNOPSIS</span></span>
<span data-ttu-id="6f716-103">Çoğaltma sunucusu için test geçişini temizler.</span><span class="sxs-lookup"><span data-stu-id="6f716-103">Cleans up the test migration for the replicating server.</span></span>

## <span data-ttu-id="6f716-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6f716-104">SYNTAX</span></span>

### <span data-ttu-id="6f716-105">Byıdvmwarecbt (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6f716-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateTestMigrationCleanup -TargetObjectID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6f716-106">Byinputobjectvmwareci</span><span class="sxs-lookup"><span data-stu-id="6f716-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateTestMigrationCleanup -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6f716-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6f716-107">DESCRIPTION</span></span>
<span data-ttu-id="6f716-108">Start-AzMigrateTestMigrationCleanup cmdlet 'i çoğaltma sunucusu için test geçişinin temizlenmesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="6f716-108">The Start-AzMigrateTestMigrationCleanup cmdlet initiates the clean up of the test migration for the replicating server.</span></span>

## <span data-ttu-id="6f716-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6f716-109">EXAMPLES</span></span>

### <span data-ttu-id="6f716-110">Örnek 1: makine kimliğine göre.</span><span class="sxs-lookup"><span data-stu-id="6f716-110">Example 1: By machine id.</span></span>
```powershell
PS C:\> Start-AzMigrateTestMigrationCleanup -TargetObjectID '/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f'


ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Test Migrate Cleanup
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : TestMigrateCleanup
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="6f716-111">Makine kimliğine göre.</span><span class="sxs-lookup"><span data-stu-id="6f716-111">By machine id.</span></span>

### <span data-ttu-id="6f716-112">Örnek 2: giriş nesnesine göre</span><span class="sxs-lookup"><span data-stu-id="6f716-112">Example 2: By input object</span></span>
```powershell
PS C:\> $obj = Get-AzMigrateServerReplication -TargetObjectID $env.srsMachineId -SubscriptionId $env.srsSubscriptionId
PS C:\> Start-AzMigrateTestMigrationCleanup -InputObject $ob


AllowedOperation            : {DisableMigration, TestMigrate, Migrate}

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Test Migrate Cleanup
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : TestMigrateCleanup
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="6f716-113">Giriş nesnesine göre.</span><span class="sxs-lookup"><span data-stu-id="6f716-113">By input object.</span></span>

## <span data-ttu-id="6f716-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6f716-114">PARAMETERS</span></span>

### <span data-ttu-id="6f716-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f716-115">-DefaultProfile</span></span>
<span data-ttu-id="6f716-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6f716-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f716-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f716-117">-InputObject</span></span>
<span data-ttu-id="6f716-118">Test geçişi Temizleme işleminin başlatılması gereken çoğaltma sunucusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f716-118">Specifies the replicating server for which the test migration cleanup needs to be initiated.</span></span>
<span data-ttu-id="6f716-119">Sunucu nesnesi, yapı Için Get-AzMigrateServerReplication cmdlet kullanılarak alınabilir, ıNPUTOBJECT özelliklerinin notlar bölümü görebilir ve karma tablo oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6f716-119">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6f716-120">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="6f716-120">-SubscriptionId</span></span>
<span data-ttu-id="6f716-121">Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="6f716-121">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="6f716-122">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="6f716-122">-TargetObjectID</span></span>
<span data-ttu-id="6f716-123">Test geçişi Temizleme işleminin başlatılması gereken çoğaltma sunucusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f716-123">Specifies the replicating server for which the test migration cleanup needs to be initiated.</span></span>
<span data-ttu-id="6f716-124">KIMLIK, Get-AzMigrateServerReplication cmdlet kullanılarak alınmalıdır.</span><span class="sxs-lookup"><span data-stu-id="6f716-124">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="6f716-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f716-125">CommonParameters</span></span>
<span data-ttu-id="6f716-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6f716-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f716-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6f716-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f716-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6f716-128">INPUTS</span></span>

## <span data-ttu-id="6f716-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6f716-129">OUTPUTS</span></span>

### <span data-ttu-id="6f716-130">Microsoft. Azure. PowerShell. cmdlet. geçir. modeller. Api20180110. ıjob</span><span class="sxs-lookup"><span data-stu-id="6f716-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="6f716-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6f716-131">NOTES</span></span>

<span data-ttu-id="6f716-132">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="6f716-132">ALIASES</span></span>

<span data-ttu-id="6f716-133">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="6f716-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6f716-134">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="6f716-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6f716-135">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6f716-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6f716-136">INPUTOBJECT <IMigrationItem> : test geçişi Temizleme işleminin başlatılması gereken çoğaltma sunucusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f716-136">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the test migration cleanup needs to be initiated.</span></span> <span data-ttu-id="6f716-137">Sunucu nesnesi Get-AzMigrateServerReplication cmdlet kullanılarak alınabilir</span><span class="sxs-lookup"><span data-stu-id="6f716-137">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet</span></span>
  - <span data-ttu-id="6f716-138">`[Location <String>]`: Kaynak konumu</span><span class="sxs-lookup"><span data-stu-id="6f716-138">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="6f716-139">`[CurrentJobId <String>]`: Yürütülen işin ARM kimliği.</span><span class="sxs-lookup"><span data-stu-id="6f716-139">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="6f716-140">`[CurrentJobName <String>]`: İş adı.</span><span class="sxs-lookup"><span data-stu-id="6f716-140">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="6f716-141">`[CurrentJobStartTime <DateTime?>]`: İşin başlangıç saati.</span><span class="sxs-lookup"><span data-stu-id="6f716-141">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="6f716-142">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Geçiş sağlayıcısı özel ayarları.</span><span class="sxs-lookup"><span data-stu-id="6f716-142">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="6f716-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6f716-143">RELATED LINKS</span></span>

