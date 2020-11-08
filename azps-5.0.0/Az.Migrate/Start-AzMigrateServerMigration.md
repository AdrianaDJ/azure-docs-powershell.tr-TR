---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/start-azmigrateservermigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateServerMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateServerMigration.md
ms.openlocfilehash: 6a6eb5adb947793be1faf0d1d1921941e0d54065
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278623"
---
# <span data-ttu-id="61e83-101">Start-AzMigrateServerMigration</span><span class="sxs-lookup"><span data-stu-id="61e83-101">Start-AzMigrateServerMigration</span></span>

## <span data-ttu-id="61e83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61e83-102">SYNOPSIS</span></span>
<span data-ttu-id="61e83-103">Çoğaltma sunucusunun geçişini başlatır.</span><span class="sxs-lookup"><span data-stu-id="61e83-103">Starts the migration for the replicating server.</span></span>

## <span data-ttu-id="61e83-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="61e83-104">SYNTAX</span></span>

### <span data-ttu-id="61e83-105">Byıdvmwarecbt (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="61e83-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateServerMigration -TargetObjectID <String> [-SubscriptionId <String>] [-TurnOffSourceServer]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="61e83-106">Byinputobjectvmwareci</span><span class="sxs-lookup"><span data-stu-id="61e83-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateServerMigration -InputObject <IMigrationItem> [-SubscriptionId <String>] [-TurnOffSourceServer]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="61e83-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="61e83-107">DESCRIPTION</span></span>
<span data-ttu-id="61e83-108">Çoğaltma sunucusunun geçişini başlatır.</span><span class="sxs-lookup"><span data-stu-id="61e83-108">Starts the migration for the replicating server.</span></span>

## <span data-ttu-id="61e83-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="61e83-109">EXAMPLES</span></span>

### <span data-ttu-id="61e83-110">Örnek 1: kimliğe göre</span><span class="sxs-lookup"><span data-stu-id="61e83-110">Example 1: By id</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Start-AzMigrateServerMigration -TargetObjectID "/Subscriptions/7xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_52f42ee7-8eb3-1aa4-e2d5-1ae83f86b085"

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Migrate
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Migrate
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="61e83-111">Kimliğe göre</span><span class="sxs-lookup"><span data-stu-id="61e83-111">By id</span></span>

## <span data-ttu-id="61e83-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="61e83-112">PARAMETERS</span></span>

### <span data-ttu-id="61e83-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61e83-113">-DefaultProfile</span></span>
<span data-ttu-id="61e83-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="61e83-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61e83-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61e83-115">-InputObject</span></span>
<span data-ttu-id="61e83-116">Geçişin başlatılması gereken çoğaltma sunucusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="61e83-116">Specifies the replicating server for which migration needs to be initiated.</span></span>
<span data-ttu-id="61e83-117">Sunucu nesnesi Get-AzMigrateServerReplication cmdlet kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="61e83-117">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="61e83-118">Oluşturmak için, ıNPUTOBJECT özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="61e83-118">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="61e83-119">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="61e83-119">-SubscriptionId</span></span>
<span data-ttu-id="61e83-120">Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="61e83-120">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="61e83-121">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="61e83-121">-TargetObjectID</span></span>
<span data-ttu-id="61e83-122">Geçişin başlatılması gereken repltonlu sunucuyu belirtir.</span><span class="sxs-lookup"><span data-stu-id="61e83-122">Specifies the replcating server for which migration needs to be initiated.</span></span>
<span data-ttu-id="61e83-123">KIMLIK, Get-AzMigrateServerReplication cmdlet kullanılarak alınmalıdır.</span><span class="sxs-lookup"><span data-stu-id="61e83-123">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="61e83-124">-TurnOffSourceServer</span><span class="sxs-lookup"><span data-stu-id="61e83-124">-TurnOffSourceServer</span></span>
<span data-ttu-id="61e83-125">Kaynak sunucunun geçiş sonrası özelliğinin kapatılıp kapatılmaması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="61e83-125">Specifies whether the source server should be turned off post migration.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61e83-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61e83-126">CommonParameters</span></span>
<span data-ttu-id="61e83-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="61e83-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61e83-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="61e83-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61e83-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="61e83-129">INPUTS</span></span>

## <span data-ttu-id="61e83-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="61e83-130">OUTPUTS</span></span>

### <span data-ttu-id="61e83-131">Microsoft. Azure. PowerShell. cmdlet. geçir. modeller. Api20180110. ıjob</span><span class="sxs-lookup"><span data-stu-id="61e83-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="61e83-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="61e83-132">NOTES</span></span>

<span data-ttu-id="61e83-133">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="61e83-133">ALIASES</span></span>

<span data-ttu-id="61e83-134">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="61e83-134">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="61e83-135">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="61e83-135">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="61e83-136">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="61e83-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="61e83-137">INPUTOBJECT <IMigrationItem> : geçişin başlatılması gereken çoğaltma sunucusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="61e83-137">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which migration needs to be initiated.</span></span> <span data-ttu-id="61e83-138">Sunucu nesnesi Get-AzMigrateServerReplication cmdlet kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="61e83-138">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="61e83-139">`[Location <String>]`: Kaynak konumu</span><span class="sxs-lookup"><span data-stu-id="61e83-139">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="61e83-140">`[CurrentJobId <String>]`: Yürütülen işin ARM kimliği.</span><span class="sxs-lookup"><span data-stu-id="61e83-140">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="61e83-141">`[CurrentJobName <String>]`: İş adı.</span><span class="sxs-lookup"><span data-stu-id="61e83-141">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="61e83-142">`[CurrentJobStartTime <DateTime?>]`: İşin başlangıç saati.</span><span class="sxs-lookup"><span data-stu-id="61e83-142">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="61e83-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Geçiş sağlayıcısı özel ayarları.</span><span class="sxs-lookup"><span data-stu-id="61e83-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="61e83-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="61e83-144">RELATED LINKS</span></span>

