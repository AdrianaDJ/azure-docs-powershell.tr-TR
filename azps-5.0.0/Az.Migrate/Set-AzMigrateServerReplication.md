---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/set-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Set-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Set-AzMigrateServerReplication.md
ms.openlocfilehash: bb7f951403fd2298a2890f0b92f756c0417e94c9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278621"
---
# <span data-ttu-id="c65fc-101">Set-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="c65fc-101">Set-AzMigrateServerReplication</span></span>

## <span data-ttu-id="c65fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c65fc-102">SYNOPSIS</span></span>
<span data-ttu-id="c65fc-103">Çoğaltma sunucusunun hedef özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c65fc-103">Updates the target properties for the replicating server.</span></span>

## <span data-ttu-id="c65fc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c65fc-104">SYNTAX</span></span>

### <span data-ttu-id="c65fc-105">Byıdvmwarecbt (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c65fc-105">ByIDVMwareCbt (Default)</span></span>
```
Set-AzMigrateServerReplication -TargetObjectID <String> [-NicToUpdate <IVMwareCbtNicInput[]>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetNetworkId <String>] [-TargetResourceGroupID <String>] [-TargetVMName <String>]
 [-TargetVMSize <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c65fc-106">Byinputobjectvmwareci</span><span class="sxs-lookup"><span data-stu-id="c65fc-106">ByInputObjectVMwareCbt</span></span>
```
Set-AzMigrateServerReplication -InputObject <IMigrationItem> [-NicToUpdate <IVMwareCbtNicInput[]>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetNetworkId <String>] [-TargetResourceGroupID <String>] [-TargetVMName <String>]
 [-TargetVMSize <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c65fc-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c65fc-107">DESCRIPTION</span></span>
<span data-ttu-id="c65fc-108">Set-AzMigrateServerReplication cmdlet 'i, çoğaltma sunucusunun hedef özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c65fc-108">The Set-AzMigrateServerReplication cmdlet updates the target properties for the replicating server.</span></span>

## <span data-ttu-id="c65fc-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c65fc-109">EXAMPLES</span></span>

### <span data-ttu-id="c65fc-110">Örnek 1: kimliğe göre güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="c65fc-110">Example 1: Update by id</span></span>
```powershell
PS C:\> Set-AzMigrateServerReplication -TargetObjectID '/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_500f44f8-2aa3-587b-8958-ead358639629' -TargetVMName 'rb-w2k12r2-1'

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Update
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Update
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="c65fc-111">Kimliğe göre.</span><span class="sxs-lookup"><span data-stu-id="c65fc-111">By id.</span></span>

## <span data-ttu-id="c65fc-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c65fc-112">PARAMETERS</span></span>

### <span data-ttu-id="c65fc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c65fc-113">-DefaultProfile</span></span>
<span data-ttu-id="c65fc-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c65fc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c65fc-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c65fc-115">-InputObject</span></span>
<span data-ttu-id="c65fc-116">Özelliklerin güncellenmesi gereken çoğaltma sunucusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c65fc-116">Specifies the replicating server for which the properties need to be updated.</span></span>
<span data-ttu-id="c65fc-117">Sunucu nesnesi Get-AzMigrateServerReplication cmdlet kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="c65fc-117">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="c65fc-118">Oluşturmak için, ıNPUTOBJECT özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c65fc-118">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c65fc-119">-NicToUpdate</span><span class="sxs-lookup"><span data-stu-id="c65fc-119">-NicToUpdate</span></span>
<span data-ttu-id="c65fc-120">Oluşturulacak Azure VM için NIC 'ı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c65fc-120">Updates the NIC for the Azure VM to be created.</span></span>
<span data-ttu-id="c65fc-121">Oluşturmak için, NICTOUPDATE özelliklerine yönelik Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c65fc-121">To construct, see NOTES section for NICTOUPDATE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtNicInput[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c65fc-122">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="c65fc-122">-SubscriptionId</span></span>
<span data-ttu-id="c65fc-123">Abonelik kimliği.</span><span class="sxs-lookup"><span data-stu-id="c65fc-123">The subscription Id.</span></span>

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

### <span data-ttu-id="c65fc-124">-TargetAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c65fc-124">-TargetAvailabilitySet</span></span>
<span data-ttu-id="c65fc-125">VM oluşturma için kullanılacak kullanılabilirlik kümesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c65fc-125">Specifies the Availability Set to be used for VM creation.</span></span>

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

### <span data-ttu-id="c65fc-126">-TargetAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="c65fc-126">-TargetAvailabilityZone</span></span>
<span data-ttu-id="c65fc-127">VM oluşturma için kullanılacak kullanılabilirlik bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c65fc-127">Specifies the Availability Zone to be used for VM creation.</span></span>

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

### <span data-ttu-id="c65fc-128">-Targetnetworkıd</span><span class="sxs-lookup"><span data-stu-id="c65fc-128">-TargetNetworkId</span></span>
<span data-ttu-id="c65fc-129">Sunucunun geçirilmesi gereken hedef Azure aboneliğindeki sanal ağ kimliğini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c65fc-129">Updates the Virtual Network id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="c65fc-130">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="c65fc-130">-TargetObjectID</span></span>
<span data-ttu-id="c65fc-131">Özelliklerin güncellenmesi gereken repltonlu sunucuyu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c65fc-131">Specifies the replcating server for which the properties need to be updated.</span></span>
<span data-ttu-id="c65fc-132">KIMLIK, Get-AzMigrateServerReplication cmdlet kullanılarak alınmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c65fc-132">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="c65fc-133">-Targetresourcegroupıd</span><span class="sxs-lookup"><span data-stu-id="c65fc-133">-TargetResourceGroupID</span></span>
<span data-ttu-id="c65fc-134">Sunucunun geçirilmesi gereken hedef Azure aboneliğindeki kaynak grubu kimliğini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c65fc-134">Updates the Resource Group id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="c65fc-135">-TargetVMName</span><span class="sxs-lookup"><span data-stu-id="c65fc-135">-TargetVMName</span></span>
<span data-ttu-id="c65fc-136">Özelliklerin güncellenmesi gereken repltonlu sunucuyu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c65fc-136">Specifies the replcating server for which the properties need to be updated.</span></span>
<span data-ttu-id="c65fc-137">KIMLIK, Get-AzMigrateServerReplication cmdlet kullanılarak alınmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c65fc-137">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="c65fc-138">-TargetVMSize</span><span class="sxs-lookup"><span data-stu-id="c65fc-138">-TargetVMSize</span></span>
<span data-ttu-id="c65fc-139">Oluşturulacak Azure VM 'yi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c65fc-139">Updates the SKU of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="c65fc-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c65fc-140">CommonParameters</span></span>
<span data-ttu-id="c65fc-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c65fc-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c65fc-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c65fc-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c65fc-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c65fc-143">INPUTS</span></span>

## <span data-ttu-id="c65fc-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c65fc-144">OUTPUTS</span></span>

### <span data-ttu-id="c65fc-145">Microsoft. Azure. PowerShell. cmdlet. geçir. modeller. Api20180110. ıjob</span><span class="sxs-lookup"><span data-stu-id="c65fc-145">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="c65fc-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c65fc-146">NOTES</span></span>

<span data-ttu-id="c65fc-147">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="c65fc-147">ALIASES</span></span>

<span data-ttu-id="c65fc-148">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="c65fc-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c65fc-149">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c65fc-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c65fc-150">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c65fc-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c65fc-151">INPUTOBJECT <IMigrationItem> : özelliklerin güncellenmesi gereken çoğaltma sunucusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c65fc-151">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the properties need to be updated.</span></span> <span data-ttu-id="c65fc-152">Sunucu nesnesi Get-AzMigrateServerReplication cmdlet kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="c65fc-152">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="c65fc-153">`[Location <String>]`: Kaynak konumu</span><span class="sxs-lookup"><span data-stu-id="c65fc-153">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="c65fc-154">`[CurrentJobId <String>]`: Yürütülen işin ARM kimliği.</span><span class="sxs-lookup"><span data-stu-id="c65fc-154">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="c65fc-155">`[CurrentJobName <String>]`: İş adı.</span><span class="sxs-lookup"><span data-stu-id="c65fc-155">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="c65fc-156">`[CurrentJobStartTime <DateTime?>]`: İşin başlangıç saati.</span><span class="sxs-lookup"><span data-stu-id="c65fc-156">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="c65fc-157">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Geçiş sağlayıcısı özel ayarları.</span><span class="sxs-lookup"><span data-stu-id="c65fc-157">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

<span data-ttu-id="c65fc-158">NICTOUPDATE <ıvmwarecbtnicınput [] >: oluşturulacak Azure VM 'yi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c65fc-158">NICTOUPDATE <IVMwareCbtNicInput[]>: Updates the NIC for the Azure VM to be created.</span></span>
  - <span data-ttu-id="c65fc-159">`IsPrimaryNic <String>`: Bunun birincil NIC olup olmadığını gösteren bir değer.</span><span class="sxs-lookup"><span data-stu-id="c65fc-159">`IsPrimaryNic <String>`: A value indicating whether this is the primary NIC.</span></span>
  - <span data-ttu-id="c65fc-160">`NicId <String>`: NIC kimliği.</span><span class="sxs-lookup"><span data-stu-id="c65fc-160">`NicId <String>`: The NIC Id.</span></span>
  - <span data-ttu-id="c65fc-161">`[IsSelectedForMigration <String>]`: Bu NIC 'in geçiş için seçilip seçilmediğini gösteren bir değer.</span><span class="sxs-lookup"><span data-stu-id="c65fc-161">`[IsSelectedForMigration <String>]`: A value indicating whether this NIC is selected for migration.</span></span>
  - <span data-ttu-id="c65fc-162">`[TargetStaticIPAddress <String>]`: Statik IP adresi.</span><span class="sxs-lookup"><span data-stu-id="c65fc-162">`[TargetStaticIPAddress <String>]`: The static IP address.</span></span>
  - <span data-ttu-id="c65fc-163">`[TargetSubnetName <String>]`: Hedef alt ağ adı.</span><span class="sxs-lookup"><span data-stu-id="c65fc-163">`[TargetSubnetName <String>]`: Target subnet name.</span></span>

## <span data-ttu-id="c65fc-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c65fc-164">RELATED LINKS</span></span>

