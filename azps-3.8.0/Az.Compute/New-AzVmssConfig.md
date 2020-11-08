---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: 3c22f34b1dc4e01cf4e3ea2f2b3f9c6045197734
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94095772"
---
# <span data-ttu-id="18245-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="18245-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="18245-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18245-102">SYNOPSIS</span></span>
<span data-ttu-id="18245-103">Bir VMSS yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="18245-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="18245-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="18245-104">SYNTAX</span></span>

### <span data-ttu-id="18245-105">DefaultParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="18245-105">DefaultParameterSet (Default)</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutomaticRepairMaxInstanceRepairsPercent <Int32>] [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>]
 [-EnableUltraSSD] [-HealthProbeId <String>] [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-TerminateScheduledEvents]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="18245-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="18245-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutomaticRepairMaxInstanceRepairsPercent <Int32>] [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>]
 [-EnableUltraSSD] [-HealthProbeId <String>] [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-TerminateScheduledEvents]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] -IdentityType <ResourceIdentityType> [-IdentityId <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18245-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="18245-107">AssignIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutomaticRepairMaxInstanceRepairsPercent <Int32>] [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>]
 [-EnableUltraSSD] [-HealthProbeId <String>] [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-TerminateScheduledEvents]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] [-AssignIdentity] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="18245-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="18245-108">DESCRIPTION</span></span>
<span data-ttu-id="18245-109">**Yeni-AzVmssConfig** cmdlet 'i, yapılandırılabilir yerel sanal Manager ölçek KÜMESI (VMSS) nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="18245-109">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="18245-110">VMSS nesnesini yapılandırmak için diğer cmdlet 'ler gereklidir.</span><span class="sxs-lookup"><span data-stu-id="18245-110">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="18245-111">Bu cmdlet 'ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="18245-111">These cmdlets are:</span></span>
- <span data-ttu-id="18245-112">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="18245-112">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="18245-113">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="18245-113">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="18245-114">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="18245-114">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="18245-115">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="18245-115">Add-AzVmssExtension</span></span>

## <span data-ttu-id="18245-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="18245-116">EXAMPLES</span></span>

### <span data-ttu-id="18245-117">Örnek 1: bir VMSS yapılandırma nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="18245-117">Example 1: Create a VMSS configuration object</span></span>
```
PS C:\> $VMSS = New-AzVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic" -NetworkInterfaceConfiguration $NetCfg `
            | Add-AzVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
            | Set-AzVmssOSProfile -ComputerNamePrefix "Test" -AdminUsername $adminUsername -AdminPassword $AdminPassword `
            | Set-AzVmssStorageProfile -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VHDContainer `
            | Add-AzVmssAdditionalUnattendContent -ComponentName  $AUCComponentName -Content  $AUCContent -PassName  $AUCPassName -SettingName  $AUCSetting `
            | Remove-AzVmssAdditionalUnattendContent -ComponentName  $AUCComponentName;

New-AzVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

<span data-ttu-id="18245-118">Bu örnek bir VMSS yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="18245-118">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="18245-119">İlk komut, bir VMSS yapılandırma nesnesi oluşturmak için **New-AzVmssConfig** cmdlet 'ini kullanır ve sonucu $VMSS adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="18245-119">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="18245-120">İkinci komut, ilk komutta oluşturulan VMSS yapılandırma nesnesini kullanan bir VMSS oluşturmak için **New-AzVmss** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="18245-120">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="18245-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="18245-121">PARAMETERS</span></span>

### <span data-ttu-id="18245-122">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="18245-122">-AssignIdentity</span></span>
<span data-ttu-id="18245-123">Sanal makine ölçek kümesi için sistem tarafından atanan kimliği belirtin.</span><span class="sxs-lookup"><span data-stu-id="18245-123">Specify the system assigned identity for the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18245-124">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="18245-124">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="18245-125">VM 'deki durum değişikliği nedeniyle otomatik onarımların askıya alındığı süre.</span><span class="sxs-lookup"><span data-stu-id="18245-125">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="18245-126">Kullanım süresi, durum değişikliği tamamlandıktan sonra başlar.</span><span class="sxs-lookup"><span data-stu-id="18245-126">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="18245-127">Bu, erken veya kazayla onarılmasını önlemeye yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="18245-127">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="18245-128">Süre ISO 8601 biçiminde belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="18245-128">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="18245-129">Varsayılan değer 5 dakikadır (PT5M).</span><span class="sxs-lookup"><span data-stu-id="18245-129">The default value is 5 minutes (PT5M).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18245-130">-AutomaticRepairMaxInstanceRepairsPercent</span><span class="sxs-lookup"><span data-stu-id="18245-130">-AutomaticRepairMaxInstanceRepairsPercent</span></span>
<span data-ttu-id="18245-131">Aynı anda onarılacak sanal makinelerin yüzdesi (ölçek kümesi kapasitesi).</span><span class="sxs-lookup"><span data-stu-id="18245-131">The percentage (capacity of scaleset) of virtual machines that will be simultaneously repaired.</span></span> <span data-ttu-id="18245-132">Varsayılan değer %20 ' dir.</span><span class="sxs-lookup"><span data-stu-id="18245-132">The default value is 20%.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18245-133">-Autoosupgrad</span><span class="sxs-lookup"><span data-stu-id="18245-133">-AutoOSUpgrade</span></span>
<span data-ttu-id="18245-134">Resmin daha yeni bir sürümü kullanılabilir hale geldiğinde, bir yerde ölçeklendirme kümesi örneklerine otomatik olarak işletim sistemi yükseltmeleri uygulanıp uygulanmayacağı.</span><span class="sxs-lookup"><span data-stu-id="18245-134">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="18245-135">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="18245-135">-BootDiagnostic</span></span>
<span data-ttu-id="18245-136">Sanal makine ölçek kümesi önyükleme tanılaması profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="18245-136">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.BootDiagnostics
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18245-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18245-137">-DefaultProfile</span></span>
<span data-ttu-id="18245-138">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="18245-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18245-139">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="18245-139">-DisableAutoRollback</span></span>
<span data-ttu-id="18245-140">Otomatik OS yükseltme Ilkesi için otomatik geri almayı devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="18245-140">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18245-141">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="18245-141">-EnableAutomaticRepair</span></span>
<span data-ttu-id="18245-142">Sanal makine ölçek kümesinde otomatik onarımları etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="18245-142">Enables automatic repairs on the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18245-143">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="18245-143">-EnableUltraSSD</span></span>
<span data-ttu-id="18245-144">Sanal makine ölçek kümesinde UltraSSD_LRS depolama hesabı türüne sahip bir veya birden çok yönetilen veri diskine sahip olmak olanak verir.</span><span class="sxs-lookup"><span data-stu-id="18245-144">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="18245-145">Depolama hesap türü UltraSSD_LRS yönetilen diskler yalnızca bu özellik etkinse bir VMSUBNET 'e eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="18245-145">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18245-146">-Çıkarma Ilkesi</span><span class="sxs-lookup"><span data-stu-id="18245-146">-EvictionPolicy</span></span>
<span data-ttu-id="18245-147">Ölçek kümesindeki sanal makinelerin çıkarma ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="18245-147">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18245-148">Uzantılı</span><span class="sxs-lookup"><span data-stu-id="18245-148">-Extension</span></span>
<span data-ttu-id="18245-149">VMSS için uzantı bilgileri nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="18245-149">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="18245-150">Bu nesneyi eklemek için **Add-AzVmssExtension** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="18245-150">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18245-151">-Healthprobeıd</span><span class="sxs-lookup"><span data-stu-id="18245-151">-HealthProbeId</span></span>
<span data-ttu-id="18245-152">Sanal makine ölçeği kümesindeki bir örneğin durumunu belirlemek için kullanılan yük dengeleyici araştırması KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="18245-152">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="18245-153">Healthprobeıd, '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName} ' biçiminde.</span><span class="sxs-lookup"><span data-stu-id="18245-153">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18245-154">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="18245-154">-IdentityId</span></span>
<span data-ttu-id="18245-155">Sanal makine ölçek kümesiyle ilişkili kullanıcı kimliklerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="18245-155">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="18245-156">Kullanıcı kimliği başvuruları formda ARM kaynak kimlikleri olacaktır: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="18245-156">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18245-157">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="18245-157">-IdentityType</span></span>
<span data-ttu-id="18245-158">Sanal makine ölçek kümesi için kullanılan kimlik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="18245-158">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="18245-159">' Systemassigneduserın ' türü, örtülü olarak oluşturulmuş bir kimlik ve Kullanıcı tarafından atanan kimlikler kümesini içerir.</span><span class="sxs-lookup"><span data-stu-id="18245-159">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="18245-160">' None ' türü, sanal makine ölçek kümesindeki tüm kimlikleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="18245-160">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="18245-161">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="18245-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="18245-162">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="18245-162">SystemAssigned</span></span>
- <span data-ttu-id="18245-163">Kullanıcı tarafından atanmış</span><span class="sxs-lookup"><span data-stu-id="18245-163">UserAssigned</span></span>
- <span data-ttu-id="18245-164">Systemassigneduseratandı</span><span class="sxs-lookup"><span data-stu-id="18245-164">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="18245-165">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="18245-165">None</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18245-166">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="18245-166">-LicenseType</span></span>
<span data-ttu-id="18245-167">Kendi lisans senaryonuzu verecek lisans türünü belirtin.</span><span class="sxs-lookup"><span data-stu-id="18245-167">Specify the license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18245-168">-Konum</span><span class="sxs-lookup"><span data-stu-id="18245-168">-Location</span></span>
<span data-ttu-id="18245-169">VMSS 'nin oluşturulduğu Azure konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="18245-169">Specifies the Azure location where the VMSS is created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18245-170">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="18245-170">-MaxPrice</span></span>
<span data-ttu-id="18245-171">Düşük öncelikli VM/VMSS için ödemek istediğiniz en yüksek fiyatı belirtir.</span><span class="sxs-lookup"><span data-stu-id="18245-171">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="18245-172">Bu fiyat ABD doları cinsindendir.</span><span class="sxs-lookup"><span data-stu-id="18245-172">This price is in US Dollars.</span></span> <span data-ttu-id="18245-173">Bu fiyat VM boyutu için geçerli düşük öncelik fiyatıyla karşılaştırılır.</span><span class="sxs-lookup"><span data-stu-id="18245-173">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="18245-174">Ayrıca, düşük öncelikli VM/VMSS oluşturma/güncelleştirme sırasında fiyatlar karşılaştırılır ve işlem yalnızca maxPrice geçerli düşük öncelik fiyatından büyükse başarıdır.</span><span class="sxs-lookup"><span data-stu-id="18245-174">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="18245-175">Geçerli düşük öncelik fiyatının VM/VMSS oluşturulduktan sonra maxPrice 'den fazla olması durumunda, maxPrice de düşük öncelikli VM/VMSS çıkarmak için kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="18245-175">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="18245-176">Olası değerler: sıfırdan büyük herhangi bir ondalık değer.</span><span class="sxs-lookup"><span data-stu-id="18245-176">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="18245-177">Örnek: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="18245-177">Example: 0.01538.</span></span>  <span data-ttu-id="18245-178">-1 düşük öncelikli VM/VMSS 'nin fiyat nedenlerinin çıkarılmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="18245-178">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="18245-179">Ayrıca, sizin sağlanmadıysa varsayılan en fazla fiyat-1 ' dir.</span><span class="sxs-lookup"><span data-stu-id="18245-179">Also, the default max price is -1 if it is not provided by you.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18245-180">-Networkınterfaceconfiguration</span><span class="sxs-lookup"><span data-stu-id="18245-180">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="18245-181">VMSS yapılandırması için ağ özelliklerini içeren ağ profili nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="18245-181">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="18245-182">Bu nesneyi eklemek için **Add-Azvmssnetworkınterfaceyapılandırma** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="18245-182">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18245-183">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="18245-183">-OsProfile</span></span>
<span data-ttu-id="18245-184">VMSS yapılandırması işletim sistemi özelliklerini içeren işletim sistemi profili nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="18245-184">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="18245-185">Bu nesneyi ayarlamak için **set-AzVmssOsProfile** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="18245-185">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18245-186">-Overprovision</span><span class="sxs-lookup"><span data-stu-id="18245-186">-Overprovision</span></span>
<span data-ttu-id="18245-187">Cmdlet 'in VMSS 'yi içerip içermediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="18245-187">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18245-188">-PlanName</span><span class="sxs-lookup"><span data-stu-id="18245-188">-PlanName</span></span>
<span data-ttu-id="18245-189">Plan adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="18245-189">Specifies the plan name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18245-190">-Planürün</span><span class="sxs-lookup"><span data-stu-id="18245-190">-PlanProduct</span></span>
<span data-ttu-id="18245-191">Plan ürünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="18245-191">Specifies the plan product.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18245-192">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="18245-192">-PlanPromotionCode</span></span>
<span data-ttu-id="18245-193">Plan promosyon kodunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="18245-193">Specifies the plan promotion code.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18245-194">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="18245-194">-PlanPublisher</span></span>
<span data-ttu-id="18245-195">Publisher planı 'nı belirtir.</span><span class="sxs-lookup"><span data-stu-id="18245-195">Specifies the plan publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18245-196">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="18245-196">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="18245-197">Her bir yerleştirme grubu için hata etki alanı sayısı.</span><span class="sxs-lookup"><span data-stu-id="18245-197">Fault Domain count for each placement group.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18245-198">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="18245-198">-Priority</span></span>
<span data-ttu-id="18245-199">Ölçek kümesindeki sanal birim için öncelik.</span><span class="sxs-lookup"><span data-stu-id="18245-199">The priority for the virtual machien in the scale set.</span></span>  <span data-ttu-id="18245-200">Yalnızca desteklenen değerler ' Regular ', ' nokta ' ve ' düşük ' değerleridir.</span><span class="sxs-lookup"><span data-stu-id="18245-200">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="18245-201">' Regular ' normal sanal makine içindir.</span><span class="sxs-lookup"><span data-stu-id="18245-201">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="18245-202">' Spot ', spot sanal makine içindir.</span><span class="sxs-lookup"><span data-stu-id="18245-202">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="18245-203">' Low ', spot sanal makine için de, ancak ' nokta ' ile değiştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="18245-203">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="18245-204">Lütfen ' düşük ' yerine ' nokta ' kullanın.</span><span class="sxs-lookup"><span data-stu-id="18245-204">Please use 'Spot' instead of 'Low'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18245-205">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="18245-205">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="18245-206">Bu ölçek kümesiyle kullanılacak yakınlık Yerleşim grubunun kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="18245-206">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18245-207">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="18245-207">-RollingUpgradePolicy</span></span>
<span data-ttu-id="18245-208">Çalışırken yükseltme ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="18245-208">Specifies the rolling upgrade policy.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18245-209">-Scaleınpolicy</span><span class="sxs-lookup"><span data-stu-id="18245-209">-ScaleInPolicy</span></span>
<span data-ttu-id="18245-210">Sanal makine ölçeği kümesinde ölçeklendirme yapılırken izlenen kurallar.</span><span class="sxs-lookup"><span data-stu-id="18245-210">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="18245-211">Olası değerler: ' default ', ' OldestVM ' ve ' NewestVM '.</span><span class="sxs-lookup"><span data-stu-id="18245-211">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="18245-212">' Varsayılan ' sanal makine ölçeği kümesi içinde ölçeklendirildiyse, ölçek kümesi ilk olarak bölgeler genelinde dengelenebilir ve bu bir zonal ölçeği kümesidir.</span><span class="sxs-lookup"><span data-stu-id="18245-212">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="18245-213">Ardından, hata etki alanları genelinde mümkün olduğunca dengeli olacaktır.</span><span class="sxs-lookup"><span data-stu-id="18245-213">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="18245-214">Her hata etki alanı içinde, kaldırılmak üzere seçilen sanal makineler, ölçek ile korunmayan en yeni değerler olacaktır.</span><span class="sxs-lookup"><span data-stu-id="18245-214">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="18245-215">' OldestVM ' sanal makine ölçeği kümesi ölçeklendiğinde, ölçeğe korunmayan en eski sanal makineler kaldırılmak üzere seçilir.</span><span class="sxs-lookup"><span data-stu-id="18245-215">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="18245-216">Zonal sanal makine ölçek kümeleri için, ölçek kümesi önce bölgeler arasında dengelenecek.</span><span class="sxs-lookup"><span data-stu-id="18245-216">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="18245-217">Her bir bölgede, korunmayan en eski sanal makineler kaldırılmak üzere seçilir.</span><span class="sxs-lookup"><span data-stu-id="18245-217">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="18245-218">' NewestVM ' sanal makine ölçeği kümesi ölçeklendiğinde, ölçeğe korunmayan en yeni sanal makineler kaldırılmak üzere seçilir.</span><span class="sxs-lookup"><span data-stu-id="18245-218">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="18245-219">Zonal sanal makine ölçek kümeleri için, ölçek kümesi önce bölgeler arasında dengelenecek.</span><span class="sxs-lookup"><span data-stu-id="18245-219">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="18245-220">Her bir bölgede, korunmayan en yeni sanal makineler kaldırılmak üzere seçilir.</span><span class="sxs-lookup"><span data-stu-id="18245-220">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18245-221">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="18245-221">-SinglePlacementGroup</span></span>
<span data-ttu-id="18245-222">Tek yerleşim grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="18245-222">Specifies the single placement group.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18245-223">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="18245-223">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="18245-224">Uzantıların fazladan sağlanan diğer VM 'lerde çalıştırılmamıştır.</span><span class="sxs-lookup"><span data-stu-id="18245-224">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="18245-225">-Skukapasitesi</span><span class="sxs-lookup"><span data-stu-id="18245-225">-SkuCapacity</span></span>
<span data-ttu-id="18245-226">VMSS 'deki örneklerin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="18245-226">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18245-227">-SkuName</span><span class="sxs-lookup"><span data-stu-id="18245-227">-SkuName</span></span>
<span data-ttu-id="18245-228">Tüm VMSS örneklerinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="18245-228">Specifies the size of all the instances of VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18245-229">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="18245-229">-SkuTier</span></span>
<span data-ttu-id="18245-230">VMSS 'nin katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="18245-230">Specifies the tier of VMSS.</span></span> <span data-ttu-id="18245-231">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="18245-231">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="18245-232">Ardından</span><span class="sxs-lookup"><span data-stu-id="18245-232">Standard</span></span>
- <span data-ttu-id="18245-233">Ana</span><span class="sxs-lookup"><span data-stu-id="18245-233">Basic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18245-234">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="18245-234">-StorageProfile</span></span>
<span data-ttu-id="18245-235">VMSS yapılandırması için disk özelliklerini içeren depolama profili nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="18245-235">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="18245-236">Bu nesneyi ayarlamak için **set-AzVmssStorageProfile** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="18245-236">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18245-237">Etiketli</span><span class="sxs-lookup"><span data-stu-id="18245-237">-Tag</span></span>
<span data-ttu-id="18245-238">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="18245-238">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="18245-239">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="18245-239">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18245-240">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="18245-240">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="18245-241">Yapılandırılabilir süre (dakika cinsinden) silinen bir sanal makinenin, etkinlik otomatik onaylanmadan (zaman aşımına uğramadan) önce zamanlanmış olayı sonlandırmasını sağlamak gerekecektir.</span><span class="sxs-lookup"><span data-stu-id="18245-241">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18245-242">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="18245-242">-TerminateScheduledEvents</span></span>
<span data-ttu-id="18245-243">Zamanlanmış olayları Sonlandır özelliğini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="18245-243">Enable the Terminate Scheduled events</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18245-244">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="18245-244">-UpgradePolicyMode</span></span>
<span data-ttu-id="18245-245">Belirtilen ölçek kümesindeki sanal makinelere yükseltme modu.</span><span class="sxs-lookup"><span data-stu-id="18245-245">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="18245-246">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="18245-246">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="18245-247">Otomatik</span><span class="sxs-lookup"><span data-stu-id="18245-247">Automatic</span></span>
- <span data-ttu-id="18245-248">El ile</span><span class="sxs-lookup"><span data-stu-id="18245-248">Manual</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.UpgradeMode]
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18245-249">-Bölge</span><span class="sxs-lookup"><span data-stu-id="18245-249">-Zone</span></span>
<span data-ttu-id="18245-250">Sanal makine ölçek kümesi için bölge listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="18245-250">Specifies the zone list for the virtual machine scale set.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18245-251">-Bölgbakiye</span><span class="sxs-lookup"><span data-stu-id="18245-251">-ZoneBalance</span></span>
<span data-ttu-id="18245-252">Bölge kesilmesi durumunda, tam çift sanal makine dağıtımını x bölgeler çapraz olarak zorunlu tutulmayacağı.</span><span class="sxs-lookup"><span data-stu-id="18245-252">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="18245-253">-Onay</span><span class="sxs-lookup"><span data-stu-id="18245-253">-Confirm</span></span>
<span data-ttu-id="18245-254">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="18245-254">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18245-255">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18245-255">-WhatIf</span></span>
<span data-ttu-id="18245-256">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="18245-256">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="18245-257">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="18245-257">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18245-258">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18245-258">CommonParameters</span></span>
<span data-ttu-id="18245-259">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="18245-259">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18245-260">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="18245-260">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18245-261">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="18245-261">INPUTS</span></span>

### <span data-ttu-id="18245-262">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="18245-262">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="18245-263">System. String</span><span class="sxs-lookup"><span data-stu-id="18245-263">System.String</span></span>

### <span data-ttu-id="18245-264">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="18245-264">System.Collections.Hashtable</span></span>

### <span data-ttu-id="18245-265">System. Int32</span><span class="sxs-lookup"><span data-stu-id="18245-265">System.Int32</span></span>

### <span data-ttu-id="18245-266">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. modeller. Yükseltmodu, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="18245-266">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="18245-267">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSetOSProfile</span><span class="sxs-lookup"><span data-stu-id="18245-267">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="18245-268">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSetStorageProfile</span><span class="sxs-lookup"><span data-stu-id="18245-268">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="18245-269">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSetNetworkConfiguration []</span><span class="sxs-lookup"><span data-stu-id="18245-269">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="18245-270">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSetExtension []</span><span class="sxs-lookup"><span data-stu-id="18245-270">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="18245-271">System. String []</span><span class="sxs-lookup"><span data-stu-id="18245-271">System.String[]</span></span>

### <span data-ttu-id="18245-272">Microsoft. Azure. Management. COMPUTE. model. RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="18245-272">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="18245-273">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="18245-273">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="18245-274">Microsoft. Azure. Management. COMPUTE. modeller. BootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="18245-274">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="18245-275">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. modeller. Kaynakıdentitytype, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="18245-275">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="18245-276">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="18245-276">OUTPUTS</span></span>

### <span data-ttu-id="18245-277">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="18245-277">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="18245-278">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="18245-278">NOTES</span></span>

## <span data-ttu-id="18245-279">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="18245-279">RELATED LINKS</span></span>

[<span data-ttu-id="18245-280">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="18245-280">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="18245-281">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="18245-281">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="18245-282">Add-Azvmssnetworkınterfaceconfiguration</span><span class="sxs-lookup"><span data-stu-id="18245-282">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="18245-283">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="18245-283">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="18245-284">Yeni-AzVmss</span><span class="sxs-lookup"><span data-stu-id="18245-284">New-AzVmss</span></span>](./New-AzVmss.md)
