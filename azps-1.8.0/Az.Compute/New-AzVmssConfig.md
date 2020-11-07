---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: beb9c067fb2ca625fcf756747a52eef0bf1ca9b5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761299"
---
# <span data-ttu-id="a8e1f-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="a8e1f-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="a8e1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8e1f-102">SYNOPSIS</span></span>
<span data-ttu-id="a8e1f-103">Bir VMSS yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="a8e1f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a8e1f-104">SYNTAX</span></span>

### <span data-ttu-id="a8e1f-105">DefaultParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a8e1f-105">DefaultParameterSet (Default)</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-ZoneBalance]
 [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>] [-PlanName <String>] [-PlanPublisher <String>]
 [-PlanProduct <String>] [-PlanPromotionCode <String>] [-RollingUpgradePolicy <RollingUpgradePolicy>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8e1f-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8e1f-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-ZoneBalance]
 [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>] [-PlanName <String>] [-PlanPublisher <String>]
 [-PlanProduct <String>] [-PlanPromotionCode <String>] [-RollingUpgradePolicy <RollingUpgradePolicy>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8e1f-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8e1f-107">AssignIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-ZoneBalance]
 [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>] [-PlanName <String>] [-PlanPublisher <String>]
 [-PlanProduct <String>] [-PlanPromotionCode <String>] [-RollingUpgradePolicy <RollingUpgradePolicy>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-AssignIdentity] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8e1f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a8e1f-108">DESCRIPTION</span></span>
<span data-ttu-id="a8e1f-109">**Yeni-AzVmssConfig** cmdlet 'i, yapılandırılabilir yerel sanal Manager ölçek KÜMESI (VMSS) nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-109">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="a8e1f-110">VMSS nesnesini yapılandırmak için diğer cmdlet 'ler gereklidir.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-110">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="a8e1f-111">Bu cmdlet 'ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="a8e1f-111">These cmdlets are:</span></span>
- <span data-ttu-id="a8e1f-112">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="a8e1f-112">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="a8e1f-113">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="a8e1f-113">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="a8e1f-114">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8e1f-114">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="a8e1f-115">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="a8e1f-115">Add-AzVmssExtension</span></span>

## <span data-ttu-id="a8e1f-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a8e1f-116">EXAMPLES</span></span>

### <span data-ttu-id="a8e1f-117">Örnek 1: bir VMSS yapılandırma nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="a8e1f-117">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="a8e1f-118">Bu örnek bir VMSS yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-118">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="a8e1f-119">İlk komut, bir VMSS yapılandırma nesnesi oluşturmak için **New-AzVmssConfig** cmdlet 'ini kullanır ve sonucu $VMSS adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-119">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="a8e1f-120">İkinci komut, ilk komutta oluşturulan VMSS yapılandırma nesnesini kullanan bir VMSS oluşturmak için **New-AzVmss** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-120">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="a8e1f-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a8e1f-121">PARAMETERS</span></span>

### <span data-ttu-id="a8e1f-122">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="a8e1f-122">-AssignIdentity</span></span>
<span data-ttu-id="a8e1f-123">Sanal makine ölçek kümesi için sistem tarafından atanan kimliği belirtin.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-123">Specify the system assigned identity for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="a8e1f-124">-Autoosupgrad</span><span class="sxs-lookup"><span data-stu-id="a8e1f-124">-AutoOSUpgrade</span></span>
<span data-ttu-id="a8e1f-125">Resmin daha yeni bir sürümü kullanılabilir hale geldiğinde, bir yerde ölçeklendirme kümesi örneklerine otomatik olarak işletim sistemi yükseltmeleri uygulanıp uygulanmayacağı.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-125">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="a8e1f-126">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="a8e1f-126">-BootDiagnostic</span></span>
<span data-ttu-id="a8e1f-127">Sanal makine ölçek kümesi önyükleme tanılaması profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-127">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="a8e1f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8e1f-128">-DefaultProfile</span></span>
<span data-ttu-id="a8e1f-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8e1f-130">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="a8e1f-130">-DisableAutoRollback</span></span>
<span data-ttu-id="a8e1f-131">Otomatik OS yükseltme Ilkesi için otomatik geri almayı devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="a8e1f-131">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="a8e1f-132">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="a8e1f-132">-EnableUltraSSD</span></span>
<span data-ttu-id="a8e1f-133">Sanal makine ölçek kümesinde UltraSSD_LRS depolama hesabı türüne sahip bir veya birden çok yönetilen veri diskine sahip olmak olanak verir.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-133">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="a8e1f-134">Depolama hesap türü UltraSSD_LRS yönetilen diskler yalnızca bu özellik etkinse bir VMSUBNET 'e eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-134">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="a8e1f-135">-Çıkarma Ilkesi</span><span class="sxs-lookup"><span data-stu-id="a8e1f-135">-EvictionPolicy</span></span>
<span data-ttu-id="a8e1f-136">Ölçek kümesindeki sanal makinelerin çıkarma ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-136">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="a8e1f-137">Uzantılı</span><span class="sxs-lookup"><span data-stu-id="a8e1f-137">-Extension</span></span>
<span data-ttu-id="a8e1f-138">VMSS için uzantı bilgileri nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-138">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="a8e1f-139">Bu nesneyi eklemek için **Add-AzVmssExtension** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-139">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8e1f-140">-Healthprobeıd</span><span class="sxs-lookup"><span data-stu-id="a8e1f-140">-HealthProbeId</span></span>
<span data-ttu-id="a8e1f-141">Sanal makine ölçeği kümesindeki bir örneğin durumunu belirlemek için kullanılan yük dengeleyici araştırması KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-141">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="a8e1f-142">Healthprobeıd, '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName} ' biçiminde.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-142">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="a8e1f-143">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="a8e1f-143">-IdentityId</span></span>
<span data-ttu-id="a8e1f-144">Sanal makine ölçek kümesiyle ilişkili kullanıcı kimliklerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-144">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="a8e1f-145">Kullanıcı kimliği başvuruları formda ARM kaynak kimlikleri olacaktır: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="a8e1f-145">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="a8e1f-146">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="a8e1f-146">-IdentityType</span></span>
<span data-ttu-id="a8e1f-147">Sanal makine ölçek kümesi için kullanılan kimlik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-147">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="a8e1f-148">' Systemassigneduserın ' türü, örtülü olarak oluşturulmuş bir kimlik ve Kullanıcı tarafından atanan kimlikler kümesini içerir.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-148">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="a8e1f-149">' None ' türü, sanal makine ölçek kümesindeki tüm kimlikleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-149">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="a8e1f-150">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="a8e1f-150">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a8e1f-151">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="a8e1f-151">SystemAssigned</span></span>
- <span data-ttu-id="a8e1f-152">Kullanıcı tarafından atanmış</span><span class="sxs-lookup"><span data-stu-id="a8e1f-152">UserAssigned</span></span>
- <span data-ttu-id="a8e1f-153">Systemassigneduseratandı</span><span class="sxs-lookup"><span data-stu-id="a8e1f-153">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="a8e1f-154">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a8e1f-154">None</span></span>

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

### <span data-ttu-id="a8e1f-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="a8e1f-155">-LicenseType</span></span>
<span data-ttu-id="a8e1f-156">Kendi lisans senaryonuzu verecek lisans türünü belirtin.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-156">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="a8e1f-157">-Konum</span><span class="sxs-lookup"><span data-stu-id="a8e1f-157">-Location</span></span>
<span data-ttu-id="a8e1f-158">VMSS 'nin oluşturulduğu Azure konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-158">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="a8e1f-159">-Networkınterfaceconfiguration</span><span class="sxs-lookup"><span data-stu-id="a8e1f-159">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="a8e1f-160">VMSS yapılandırması için ağ özelliklerini içeren ağ profili nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-160">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="a8e1f-161">Bu nesneyi eklemek için **Add-Azvmssnetworkınterfaceyapılandırma** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-161">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="a8e1f-162">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="a8e1f-162">-OsProfile</span></span>
<span data-ttu-id="a8e1f-163">VMSS yapılandırması işletim sistemi özelliklerini içeren işletim sistemi profili nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-163">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="a8e1f-164">Bu nesneyi ayarlamak için **set-AzVmssOsProfile** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-164">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="a8e1f-165">-Overprovision</span><span class="sxs-lookup"><span data-stu-id="a8e1f-165">-Overprovision</span></span>
<span data-ttu-id="a8e1f-166">Cmdlet 'in VMSS 'yi içerip içermediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-166">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="a8e1f-167">-PlanName</span><span class="sxs-lookup"><span data-stu-id="a8e1f-167">-PlanName</span></span>
<span data-ttu-id="a8e1f-168">Plan adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-168">Specifies the plan name.</span></span>

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

### <span data-ttu-id="a8e1f-169">-Planürün</span><span class="sxs-lookup"><span data-stu-id="a8e1f-169">-PlanProduct</span></span>
<span data-ttu-id="a8e1f-170">Plan ürünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-170">Specifies the plan product.</span></span>

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

### <span data-ttu-id="a8e1f-171">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="a8e1f-171">-PlanPromotionCode</span></span>
<span data-ttu-id="a8e1f-172">Plan promosyon kodunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-172">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="a8e1f-173">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="a8e1f-173">-PlanPublisher</span></span>
<span data-ttu-id="a8e1f-174">Publisher planı 'nı belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-174">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="a8e1f-175">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="a8e1f-175">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="a8e1f-176">Her bir yerleştirme grubu için hata etki alanı sayısı.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-176">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="a8e1f-177">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="a8e1f-177">-Priority</span></span>
<span data-ttu-id="a8e1f-178">Ölçek kümesindeki sanal makinelerin önceliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-178">Specifies the priority for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="a8e1f-179">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="a8e1f-179">-RollingUpgradePolicy</span></span>
<span data-ttu-id="a8e1f-180">Çalışırken yükseltme ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-180">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="a8e1f-181">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="a8e1f-181">-SinglePlacementGroup</span></span>
<span data-ttu-id="a8e1f-182">Tek yerleşim grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-182">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="a8e1f-183">-Skukapasitesi</span><span class="sxs-lookup"><span data-stu-id="a8e1f-183">-SkuCapacity</span></span>
<span data-ttu-id="a8e1f-184">VMSS 'deki örneklerin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-184">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="a8e1f-185">-SkuName</span><span class="sxs-lookup"><span data-stu-id="a8e1f-185">-SkuName</span></span>
<span data-ttu-id="a8e1f-186">Tüm VMSS örneklerinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-186">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="a8e1f-187">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="a8e1f-187">-SkuTier</span></span>
<span data-ttu-id="a8e1f-188">VMSS 'nin katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-188">Specifies the tier of VMSS.</span></span> <span data-ttu-id="a8e1f-189">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="a8e1f-189">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a8e1f-190">Ardından</span><span class="sxs-lookup"><span data-stu-id="a8e1f-190">Standard</span></span>
- <span data-ttu-id="a8e1f-191">Ana</span><span class="sxs-lookup"><span data-stu-id="a8e1f-191">Basic</span></span>

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

### <span data-ttu-id="a8e1f-192">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="a8e1f-192">-StorageProfile</span></span>
<span data-ttu-id="a8e1f-193">VMSS yapılandırması için disk özelliklerini içeren depolama profili nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-193">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="a8e1f-194">Bu nesneyi ayarlamak için **set-AzVmssStorageProfile** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-194">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="a8e1f-195">Etiketli</span><span class="sxs-lookup"><span data-stu-id="a8e1f-195">-Tag</span></span>
<span data-ttu-id="a8e1f-196">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-196">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a8e1f-197">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="a8e1f-197">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a8e1f-198">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="a8e1f-198">-UpgradePolicyMode</span></span>
<span data-ttu-id="a8e1f-199">Belirtilen ölçek kümesindeki sanal makinelere yükseltme modu.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-199">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="a8e1f-200">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="a8e1f-200">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a8e1f-201">Otomatik</span><span class="sxs-lookup"><span data-stu-id="a8e1f-201">Automatic</span></span>
- <span data-ttu-id="a8e1f-202">El ile</span><span class="sxs-lookup"><span data-stu-id="a8e1f-202">Manual</span></span>

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

### <span data-ttu-id="a8e1f-203">-Bölge</span><span class="sxs-lookup"><span data-stu-id="a8e1f-203">-Zone</span></span>
<span data-ttu-id="a8e1f-204">Sanal makine ölçek kümesi için bölge listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-204">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="a8e1f-205">-Bölgbakiye</span><span class="sxs-lookup"><span data-stu-id="a8e1f-205">-ZoneBalance</span></span>
<span data-ttu-id="a8e1f-206">Bölge kesilmesi durumunda, tam çift sanal makine dağıtımını x bölgeler çapraz olarak zorunlu tutulmayacağı.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-206">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="a8e1f-207">-Onay</span><span class="sxs-lookup"><span data-stu-id="a8e1f-207">-Confirm</span></span>
<span data-ttu-id="a8e1f-208">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-208">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8e1f-209">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8e1f-209">-WhatIf</span></span>
<span data-ttu-id="a8e1f-210">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-210">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a8e1f-211">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-211">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8e1f-212">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8e1f-212">CommonParameters</span></span>
<span data-ttu-id="a8e1f-213">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a8e1f-213">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8e1f-214">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8e1f-214">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8e1f-215">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a8e1f-215">INPUTS</span></span>

### <span data-ttu-id="a8e1f-216">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="a8e1f-216">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a8e1f-217">System. String</span><span class="sxs-lookup"><span data-stu-id="a8e1f-217">System.String</span></span>

### <span data-ttu-id="a8e1f-218">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a8e1f-218">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a8e1f-219">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a8e1f-219">System.Int32</span></span>

### <span data-ttu-id="a8e1f-220">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. modeller. Yükseltmodu, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="a8e1f-220">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="a8e1f-221">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSetOSProfile</span><span class="sxs-lookup"><span data-stu-id="a8e1f-221">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="a8e1f-222">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSetStorageProfile</span><span class="sxs-lookup"><span data-stu-id="a8e1f-222">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="a8e1f-223">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSetNetworkConfiguration []</span><span class="sxs-lookup"><span data-stu-id="a8e1f-223">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="a8e1f-224">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSetExtension []</span><span class="sxs-lookup"><span data-stu-id="a8e1f-224">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="a8e1f-225">System. String []</span><span class="sxs-lookup"><span data-stu-id="a8e1f-225">System.String[]</span></span>

### <span data-ttu-id="a8e1f-226">Microsoft. Azure. Management. COMPUTE. model. RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="a8e1f-226">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="a8e1f-227">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a8e1f-227">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="a8e1f-228">Microsoft. Azure. Management. COMPUTE. modeller. BootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="a8e1f-228">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="a8e1f-229">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. modeller. Kaynakıdentitytype, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="a8e1f-229">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="a8e1f-230">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a8e1f-230">OUTPUTS</span></span>

### <span data-ttu-id="a8e1f-231">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a8e1f-231">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="a8e1f-232">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a8e1f-232">NOTES</span></span>

## <span data-ttu-id="a8e1f-233">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a8e1f-233">RELATED LINKS</span></span>

[<span data-ttu-id="a8e1f-234">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="a8e1f-234">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="a8e1f-235">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="a8e1f-235">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="a8e1f-236">Add-Azvmssnetworkınterfaceconfiguration</span><span class="sxs-lookup"><span data-stu-id="a8e1f-236">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="a8e1f-237">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="a8e1f-237">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="a8e1f-238">Yeni-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a8e1f-238">New-AzVmss</span></span>](./New-AzVmss.md)