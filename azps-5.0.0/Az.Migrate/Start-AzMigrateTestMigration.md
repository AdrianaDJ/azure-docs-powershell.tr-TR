---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/start-azmigratetestmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigration.md
ms.openlocfilehash: 9a4414ca5b86ac9ebf1867cf6a58d3e495c5ea71
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278620"
---
# <span data-ttu-id="5cc5f-101">Start-AzMigrateTestMigration</span><span class="sxs-lookup"><span data-stu-id="5cc5f-101">Start-AzMigrateTestMigration</span></span>

## <span data-ttu-id="5cc5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cc5f-102">SYNOPSIS</span></span>
<span data-ttu-id="5cc5f-103">Çoğaltma sunucusu için test geçişini başlatır.</span><span class="sxs-lookup"><span data-stu-id="5cc5f-103">Starts the test migration for the replicating server.</span></span>

## <span data-ttu-id="5cc5f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5cc5f-104">SYNTAX</span></span>

### <span data-ttu-id="5cc5f-105">Byıdvmwarecbt (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5cc5f-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateTestMigration -TargetObjectID <String> -TestNetworkID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5cc5f-106">Byinputobjectvmwareci</span><span class="sxs-lookup"><span data-stu-id="5cc5f-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateTestMigration -InputObject <IMigrationItem> -TestNetworkID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5cc5f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5cc5f-107">DESCRIPTION</span></span>
<span data-ttu-id="5cc5f-108">Start-AzMigrateTestMigration cmdlet 'i çoğaltma sunucusu için test geçişini başlatır.</span><span class="sxs-lookup"><span data-stu-id="5cc5f-108">The Start-AzMigrateTestMigration cmdlet initiates the test migration for the replicating server.</span></span>

## <span data-ttu-id="5cc5f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5cc5f-109">EXAMPLES</span></span>

### <span data-ttu-id="5cc5f-110">Örnek 1: makine kimliğine göre.</span><span class="sxs-lookup"><span data-stu-id="5cc5f-110">Example 1: By machine id.</span></span>
```powershell
PS C:\> Start-AzMigrateTestMigration -TargetObjectID '/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f' -TestNetworkId '/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG/providers/Microsoft.Network/virtualNetworks/AzMigrateTargetNetwork


ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Test Migrate
Id                               : /Subscriptions/xxx-xxx-xxxresourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : TestMigrate
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="5cc5f-111">Makine kimliğine göre.</span><span class="sxs-lookup"><span data-stu-id="5cc5f-111">By machine id.</span></span>

### <span data-ttu-id="5cc5f-112">Örnek 2: giriş nesnesine göre</span><span class="sxs-lookup"><span data-stu-id="5cc5f-112">Example 2: By input object</span></span>
```powershell
PS C:\> $obj = Get-AzMigrateServerReplication -TargetObjectID $env.srsMachineId -SubscriptionId $env.srsSubscriptionId
PS C:\> Start-AzMigrateTestMigration -InputObject $obj -TestNetworkId '/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG/providers/Microsoft.Network/virtualNetworks/AzMigrateTargetNetwork


ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Test Migrate
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : TestMigrate
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="5cc5f-113">Giriş nesnesine göre.</span><span class="sxs-lookup"><span data-stu-id="5cc5f-113">By input object.</span></span>

## <span data-ttu-id="5cc5f-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5cc5f-114">PARAMETERS</span></span>

### <span data-ttu-id="5cc5f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cc5f-115">-DefaultProfile</span></span>
<span data-ttu-id="5cc5f-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5cc5f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cc5f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5cc5f-117">-InputObject</span></span>
<span data-ttu-id="5cc5f-118">Test geçişinin başlatılması gereken çoğaltma sunucusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cc5f-118">Specifies the replicating server for which the test migration needs to be initiated.</span></span>
<span data-ttu-id="5cc5f-119">Sunucu nesnesi Get-AzMigrateServerReplication cmdlet kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="5cc5f-119">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="5cc5f-120">Oluşturmak için, ıNPUTOBJECT özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5cc5f-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5cc5f-121">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="5cc5f-121">-SubscriptionId</span></span>
<span data-ttu-id="5cc5f-122">Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="5cc5f-122">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="5cc5f-123">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="5cc5f-123">-TargetObjectID</span></span>
<span data-ttu-id="5cc5f-124">Test geçişinin başlatılması gereken çoğaltma sunucusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cc5f-124">Specifies the replicating server for which the test migration needs to be initiated.</span></span>
<span data-ttu-id="5cc5f-125">KIMLIK, Get-AzMigrateServerReplication cmdlet kullanılarak alınmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5cc5f-125">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="5cc5f-126">-Testnetworkıd</span><span class="sxs-lookup"><span data-stu-id="5cc5f-126">-TestNetworkID</span></span>
<span data-ttu-id="5cc5f-127">Test geçişi için kullanılacak hedef Azure aboneliğindeki sanal ağ kimliğini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5cc5f-127">Updates the Virtual Network id within the destination Azure subscription to be used for test migration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cc5f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cc5f-128">CommonParameters</span></span>
<span data-ttu-id="5cc5f-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5cc5f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cc5f-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5cc5f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cc5f-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5cc5f-131">INPUTS</span></span>

## <span data-ttu-id="5cc5f-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5cc5f-132">OUTPUTS</span></span>

### <span data-ttu-id="5cc5f-133">Microsoft. Azure. PowerShell. cmdlet. geçir. modeller. Api20180110. ıjob</span><span class="sxs-lookup"><span data-stu-id="5cc5f-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="5cc5f-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5cc5f-134">NOTES</span></span>

<span data-ttu-id="5cc5f-135">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="5cc5f-135">ALIASES</span></span>

<span data-ttu-id="5cc5f-136">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="5cc5f-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5cc5f-137">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5cc5f-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5cc5f-138">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5cc5f-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5cc5f-139">INPUTOBJECT <IMigrationItem> : test geçişinin başlatılması gereken çoğaltma sunucusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cc5f-139">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the test migration needs to be initiated.</span></span> <span data-ttu-id="5cc5f-140">Sunucu nesnesi Get-AzMigrateServerReplication cmdlet kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="5cc5f-140">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="5cc5f-141">`[Location <String>]`: Kaynak konumu</span><span class="sxs-lookup"><span data-stu-id="5cc5f-141">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="5cc5f-142">`[CurrentJobId <String>]`: Yürütülen işin ARM kimliği.</span><span class="sxs-lookup"><span data-stu-id="5cc5f-142">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="5cc5f-143">`[CurrentJobName <String>]`: İş adı.</span><span class="sxs-lookup"><span data-stu-id="5cc5f-143">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="5cc5f-144">`[CurrentJobStartTime <DateTime?>]`: İşin başlangıç saati.</span><span class="sxs-lookup"><span data-stu-id="5cc5f-144">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="5cc5f-145">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Geçiş sağlayıcısı özel ayarları.</span><span class="sxs-lookup"><span data-stu-id="5cc5f-145">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="5cc5f-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5cc5f-146">RELATED LINKS</span></span>

