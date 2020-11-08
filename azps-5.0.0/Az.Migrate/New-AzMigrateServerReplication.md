---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateServerReplication.md
ms.openlocfilehash: 0ef21777f5a7f22fff5d9352f667d8968ff843f3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277314"
---
# <span data-ttu-id="2058b-101">New-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="2058b-101">New-AzMigrateServerReplication</span></span>

## <span data-ttu-id="2058b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2058b-102">SYNOPSIS</span></span>
<span data-ttu-id="2058b-103">Belirtilen sunucu için çoğaltmayı başlatır.</span><span class="sxs-lookup"><span data-stu-id="2058b-103">Starts replication for the specified server.</span></span>

## <span data-ttu-id="2058b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2058b-104">SYNTAX</span></span>

### <span data-ttu-id="2058b-105">Byıddefaultuser (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2058b-105">ByIdDefaultUser (Default)</span></span>
```
New-AzMigrateServerReplication -DiskType <DiskAccountType> -LicenseType <LicenseType> -MachineId <String>
 -OSDiskID <String> -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String>
 -TargetVMName <String> [-DiskEncryptionSetID <String>] [-PerformAutoResync <String>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2058b-106">Byıdpoweruser</span><span class="sxs-lookup"><span data-stu-id="2058b-106">ByIdPowerUser</span></span>
```
New-AzMigrateServerReplication -DiskToInclude <IVMwareCbtDiskInput[]> -LicenseType <LicenseType>
 -MachineId <String> -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String>
 -TargetVMName <String> [-PerformAutoResync <String>] [-SubscriptionId <String>]
 [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2058b-107">ByInputObjectDefaultUser</span><span class="sxs-lookup"><span data-stu-id="2058b-107">ByInputObjectDefaultUser</span></span>
```
New-AzMigrateServerReplication -DiskType <DiskAccountType> -InputObject <IVMwareMachine>
 -LicenseType <LicenseType> -OSDiskID <String> -TargetNetworkId <String> -TargetResourceGroupId <String>
 -TargetSubnetName <String> -TargetVMName <String> [-DiskEncryptionSetID <String>]
 [-PerformAutoResync <String>] [-SubscriptionId <String>] [-TargetAvailabilitySet <String>]
 [-TargetAvailabilityZone <String>] [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>]
 [-VMWarerunasaccountID <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2058b-108">ByInputObjectPowerUser</span><span class="sxs-lookup"><span data-stu-id="2058b-108">ByInputObjectPowerUser</span></span>
```
New-AzMigrateServerReplication -DiskToInclude <IVMwareCbtDiskInput[]> -InputObject <IVMwareMachine>
 -LicenseType <LicenseType> -TargetNetworkId <String> -TargetResourceGroupId <String>
 -TargetSubnetName <String> -TargetVMName <String> [-PerformAutoResync <String>] [-SubscriptionId <String>]
 [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2058b-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="2058b-109">DESCRIPTION</span></span>
<span data-ttu-id="2058b-110">New-AzMigrateServerReplication cmdlet 'i, Azure geçiş projesindeki belirli bir sunucu için çoğaltmayı başlatır.</span><span class="sxs-lookup"><span data-stu-id="2058b-110">The New-AzMigrateServerReplication cmdlet starts the replication for a particular discovered server in the Azure Migrate project.</span></span>

## <span data-ttu-id="2058b-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2058b-111">EXAMPLES</span></span>

### <span data-ttu-id="2058b-112">Örnek 1: yalnızca işletim sistemi diski olduğunda</span><span class="sxs-lookup"><span data-stu-id="2058b-112">Example 1: When there is only OS disk</span></span>
```powershell
PS C:\> New-AzMigrateServerReplication -MachineId "/subscriptions/xxx-xxx-xxx4/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.OffAzure/VMwareSites/AzMigratePWSHTc8d1site/machines/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f" -LicenseType NoLicenseType -TargetResourceGroupId "/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG" -TargetNetworkId  "/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG/providers/Microsoft.Network/virtualNetworks/AzMigrateTargetNetwork" -TargetSubnetName default -TargetVMName "prsadhu-TestVM" -DiskType "Standard_LRS" -OSDiskID "6000C299-343d-7bcd-c05e-a94bd63316dd"

ActivityId                       : 68af14b4-46ae-48d1-b3e9-cdcffb9e8a93 ActivityId: 74d1a396-1d37-4264-8a5b-b727aaef0171
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 9/16/20 11:57:33 AM
Error                            : {}
FriendlyName                     : Enable
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b
Location                         :
Name                             : 997e2a92-5afe-49c7-a81a-89660aec9b7b
ScenarioName                     : Enable
StartTime                        : 9/16/20 11:57:32 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 42752b89-5fad-52fd-bf93-679fbdb6fed9
TargetObjectName                 : migrateAzMigratePWSHTc8d1sitepolicy
Task                             : {CloudPairingPrerequisitesCheck, CloudPairingPrepareSite}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="2058b-113">Bu, yalnızca korunması gereken tek bir disk olduğunda senaryo içindir.</span><span class="sxs-lookup"><span data-stu-id="2058b-113">This is for the scenario, when there is only one single disk that has to be protected.</span></span>

### <span data-ttu-id="2058b-114">Örnek 2: birden çok disk olduğunda</span><span class="sxs-lookup"><span data-stu-id="2058b-114">Example 2: When there are multiple disks</span></span>
```powershell
PS C:\> $OSDisk = New-AzMigrateDiskMapping -DiskID '6000C299-343d-7bcd-c05e-a94bd63316dd' -DiskType 'Standard_LRS' -IsOSDisk 'true'
PS C:\> $DataDisk = New-AzMigrateDiskMapping -DiskID '7000C299-343d-7bcd-c05e-a94bd63316dd' -DiskType 'Standard_LRS' -IsOSDisk 'false'
PS C:\> $DisksToInclude += $OSDisk
PS C:\> $DisksToInclude += $DataDisk
PS C:\> New-AzMigrateServerReplication -MachineId "/subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.OffAzure/VMwareSites/AzMigratePWSHTc8d1site/machines/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f" -LicenseType NoLicenseType -TargetResourceGroupId "/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG" -TargetNetworkId  "/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG/providers/Microsoft.Network/virtualNetworks/AzMigrateTargetNetwork" -TargetSubnetName default -TargetVMName "prsadhu-TestVM" -DiskToInclude $DisksToInclude -PerformAutoResync true

ActivityId                       : 68af14b4-46ae-48d1-b3e9-cdcffb9e8a93 ActivityId: 74d1a396-1d37-4264-8a5b-b727aaef0171
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 9/16/20 11:57:33 AM
Error                            : {}
FriendlyName                     : Enable
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b
Location                         :
Name                             : 997e2a92-5afe-49c7-a81a-89660aec9b7b
ScenarioName                     : Enable
StartTime                        : 9/16/20 11:57:32 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 42752b89-5fad-52fd-bf93-679fbdb6fed9
TargetObjectName                 : migrateAzMigratePWSHTc8d1sitepolicy
Task                             : {CloudPairingPrerequisitesCheck, CloudPairingPrepareSite}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="2058b-115">Bu senaryo için, korunması gereken birden çok disk olduğunda.</span><span class="sxs-lookup"><span data-stu-id="2058b-115">This is for the scenario, when there are multiple disks that has to be protected.</span></span>

## <span data-ttu-id="2058b-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2058b-116">PARAMETERS</span></span>

### <span data-ttu-id="2058b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2058b-117">-DefaultProfile</span></span>
<span data-ttu-id="2058b-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2058b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2058b-119">-DiskEncryptionSetID</span><span class="sxs-lookup"><span data-stu-id="2058b-119">-DiskEncryptionSetID</span></span>
<span data-ttu-id="2058b-120">Kullanılacak disk şifrelemesi kümesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2058b-120">Specifies the disk encyption set to be used.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIdDefaultUser, ByInputObjectDefaultUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2058b-121">-Disktoınclude</span><span class="sxs-lookup"><span data-stu-id="2058b-121">-DiskToInclude</span></span>
<span data-ttu-id="2058b-122">Kaynak sunucudaki çoğaltmaya dahil edilecek diskleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="2058b-122">Specifies the disks on the source server to be included for replication.</span></span>
<span data-ttu-id="2058b-123">Oluşturmak için, DıSKTOÖZELLIKLER ve karma tablo oluşturma için Notlar bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="2058b-123">To construct, see NOTES section for DISKTOINCLUDE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtDiskInput[]
Parameter Sets: ByIdPowerUser, ByInputObjectPowerUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2058b-124">-DiskType</span><span class="sxs-lookup"><span data-stu-id="2058b-124">-DiskType</span></span>
<span data-ttu-id="2058b-125">Azure VM için kullanılacak disk türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="2058b-125">Specifies the type of disks to be used for the Azure VM.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Support.DiskAccountType
Parameter Sets: ByIdDefaultUser, ByInputObjectDefaultUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2058b-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2058b-126">-InputObject</span></span>
<span data-ttu-id="2058b-127">Geçirilecek bulunan sunucu olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2058b-127">Specifies the discovered server to be migrated.</span></span>
<span data-ttu-id="2058b-128">Sunucu nesnesi Get-AzMigrateServer cmdlet kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="2058b-128">The server object can be retrieved using the Get-AzMigrateServer cmdlet.</span></span>
<span data-ttu-id="2058b-129">Oluşturmak için, ıNPUTOBJECT özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2058b-129">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareMachine
Parameter Sets: ByInputObjectDefaultUser, ByInputObjectPowerUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2058b-130">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="2058b-130">-LicenseType</span></span>
<span data-ttu-id="2058b-131">Yükseltilecek kaynak sunucuya Azure Karma avantajı 'nın uygulanabilir olup olmadığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2058b-131">Specifies if Azure Hybrid benefit is applicable for the source server to be migrated.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Support.LicenseType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2058b-132">-MachineID</span><span class="sxs-lookup"><span data-stu-id="2058b-132">-MachineId</span></span>
<span data-ttu-id="2058b-133">Geçirilecek olan sunucunun makine KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2058b-133">Specifies the machine ID of the discovered server to be migrated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIdDefaultUser, ByIdPowerUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2058b-134">-OSDiskID</span><span class="sxs-lookup"><span data-stu-id="2058b-134">-OSDiskID</span></span>
<span data-ttu-id="2058b-135">Geçirilecek kaynak sunucunun Işletim sistemi diskini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2058b-135">Specifies the Operating System disk for the source server to be migrated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIdDefaultUser, ByInputObjectDefaultUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2058b-136">-PerformAutoResync</span><span class="sxs-lookup"><span data-stu-id="2058b-136">-PerformAutoResync</span></span>
<span data-ttu-id="2058b-137">Çoğaltmanın altında kaynak sunucu için değişiklik izlemenin kaybolduğu durumlarda çoğaltmanın otomatik onarılabileceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2058b-137">Specifies if replication be auto-repaired in case change tracking is lost for the source server under replication.</span></span>

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

### <span data-ttu-id="2058b-138">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="2058b-138">-SubscriptionId</span></span>
<span data-ttu-id="2058b-139">Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="2058b-139">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="2058b-140">-TargetAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2058b-140">-TargetAvailabilitySet</span></span>
<span data-ttu-id="2058b-141">VM Creationiçin kullanılacak kullanılabilirlik kümesini belirtir VM oluşturma için kullanılacak kullanılabilirlik kümesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2058b-141">Specifies the Availability Set to be used for VM creationSpecifies the Availability Set to be used for VM creation.</span></span>

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

### <span data-ttu-id="2058b-142">-TargetAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="2058b-142">-TargetAvailabilityZone</span></span>
<span data-ttu-id="2058b-143">VM oluşturma için kullanılacak kullanılabilirlik bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2058b-143">Specifies the Availability Zone to be used for VM creation.</span></span>

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

### <span data-ttu-id="2058b-144">-TargetBootDiagnosticsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2058b-144">-TargetBootDiagnosticsStorageAccount</span></span>
<span data-ttu-id="2058b-145">Önyükleme tanılaması için kullanılacak depolama hesabını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2058b-145">Specifies the storage account to be used for boot diagnostics.</span></span>

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

### <span data-ttu-id="2058b-146">-Targetnetworkıd</span><span class="sxs-lookup"><span data-stu-id="2058b-146">-TargetNetworkId</span></span>
<span data-ttu-id="2058b-147">Sunucunun geçirilmesi gereken hedef Azure aboneliğindeki sanal ağ kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2058b-147">Specifies the Virtual Network id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="2058b-148">-Targetresourcegroupıd</span><span class="sxs-lookup"><span data-stu-id="2058b-148">-TargetResourceGroupId</span></span>
<span data-ttu-id="2058b-149">Sunucunun geçirilmesi gereken hedef Azure aboneliğindeki kaynak grubu kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2058b-149">Specifies the Resource Group id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="2058b-150">-TargetSubnetName</span><span class="sxs-lookup"><span data-stu-id="2058b-150">-TargetSubnetName</span></span>
<span data-ttu-id="2058b-151">Hedef sanal netowk içindeki, sunucunun geçirilmesi gereken alt ağ adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2058b-151">Specifies the Subnet name within the destination Virtual Netowk to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="2058b-152">-TargetVMName</span><span class="sxs-lookup"><span data-stu-id="2058b-152">-TargetVMName</span></span>
<span data-ttu-id="2058b-153">Oluşturulacak Azure VM 'nin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2058b-153">Specifies the name of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="2058b-154">-TargetVMSize</span><span class="sxs-lookup"><span data-stu-id="2058b-154">-TargetVMSize</span></span>
<span data-ttu-id="2058b-155">Oluşturulacak Azure VM 'nin SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2058b-155">Specifies the SKU of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="2058b-156">-Vmwarerunaşama Ccountid</span><span class="sxs-lookup"><span data-stu-id="2058b-156">-VMWarerunasaccountID</span></span>
<span data-ttu-id="2058b-157">Hesap kimliği.</span><span class="sxs-lookup"><span data-stu-id="2058b-157">Account id.</span></span>

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

### <span data-ttu-id="2058b-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2058b-158">CommonParameters</span></span>
<span data-ttu-id="2058b-159">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2058b-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2058b-160">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2058b-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2058b-161">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2058b-161">INPUTS</span></span>

## <span data-ttu-id="2058b-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2058b-162">OUTPUTS</span></span>

### <span data-ttu-id="2058b-163">Microsoft. Azure. PowerShell. cmdlet. geçir. modeller. Api20180110. ıjob</span><span class="sxs-lookup"><span data-stu-id="2058b-163">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="2058b-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2058b-164">NOTES</span></span>

<span data-ttu-id="2058b-165">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="2058b-165">ALIASES</span></span>

<span data-ttu-id="2058b-166">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="2058b-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2058b-167">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2058b-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2058b-168">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2058b-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2058b-169">DISKTOıNCLUDE <ıvmwarecbtdiskınput [] >: çoğaltma için dahil edilecek kaynak sunucudaki diskleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="2058b-169">DISKTOINCLUDE <IVMwareCbtDiskInput[]>: Specifies the disks on the source server to be included for replication.</span></span>
  - <span data-ttu-id="2058b-170">`DiskId <String>`: Disk kimliği.</span><span class="sxs-lookup"><span data-stu-id="2058b-170">`DiskId <String>`: The disk Id.</span></span>
  - <span data-ttu-id="2058b-171">`IsOSDisk <String>`: Diskin işletim sistemi diski olduğunu gösteren bir değer.</span><span class="sxs-lookup"><span data-stu-id="2058b-171">`IsOSDisk <String>`: A value indicating whether the disk is the OS disk.</span></span>
  - <span data-ttu-id="2058b-172">`LogStorageAccountId <String>`: Günlük depolama hesabı ARM kimliği.</span><span class="sxs-lookup"><span data-stu-id="2058b-172">`LogStorageAccountId <String>`: The log storage account ARM Id.</span></span>
  - <span data-ttu-id="2058b-173">`LogStorageAccountSasSecretName <String>`: Günlük depolama hesabının Anahtar Kasası gizli adı.</span><span class="sxs-lookup"><span data-stu-id="2058b-173">`LogStorageAccountSasSecretName <String>`: The key vault secret name of the log storage account.</span></span>
  - <span data-ttu-id="2058b-174">`[DiskEncryptionSetId <String>]`: DiskEncryptionSet ARM kimliği.</span><span class="sxs-lookup"><span data-stu-id="2058b-174">`[DiskEncryptionSetId <String>]`: The DiskEncryptionSet ARM Id.</span></span>
  - <span data-ttu-id="2058b-175">`[DiskType <DiskAccountType?>]`: Disk türü.</span><span class="sxs-lookup"><span data-stu-id="2058b-175">`[DiskType <DiskAccountType?>]`: The disk type.</span></span>

<span data-ttu-id="2058b-176">INPUTOBJECT <IVMwareMachine> : geçirilecek bulunan sunucu olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2058b-176">INPUTOBJECT <IVMwareMachine>: Specifies the discovered server to be migrated.</span></span> <span data-ttu-id="2058b-177">Sunucu nesnesi Get-AzMigrateServer cmdlet kullanılarak alınabilir.</span><span class="sxs-lookup"><span data-stu-id="2058b-177">The server object can be retrieved using the Get-AzMigrateServer cmdlet.</span></span>
  - <span data-ttu-id="2058b-178">`[GuestOSDetailOstype <String>]`: İşletim sisteminin türü.</span><span class="sxs-lookup"><span data-stu-id="2058b-178">`[GuestOSDetailOstype <String>]`: Type of the operating system.</span></span>

## <span data-ttu-id="2058b-179">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2058b-179">RELATED LINKS</span></span>

