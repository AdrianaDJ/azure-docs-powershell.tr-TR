---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: 4fdfd5c5da9cc803cacdd2aca90b7f66771988fd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322609"
---
# <span data-ttu-id="54fb1-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="54fb1-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="54fb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54fb1-102">SYNOPSIS</span></span>
<span data-ttu-id="54fb1-103">Bir VMSS yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="54fb1-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="54fb1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="54fb1-104">SYNTAX</span></span>

### <span data-ttu-id="54fb1-105">DefaultParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="54fb1-105">DefaultParameterSet (Default)</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-MaxPrice <Double>] [-TerminateScheduledEvents] [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>]
 [-ProximityPlacementGroupId <String>] [-ScaleInPolicy <String[]>] [-EncryptionAtHost]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54fb1-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="54fb1-106">ExplicitIdentityParameterSet</span></span>
```
New-AzVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>] [[-SkuName] <String>]
 [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <PSVirtualMachineScaleSetExtension[]>] [-SkipExtensionsOnOverprovisionedVMs]
 [-SinglePlacementGroup <Boolean>] [-ZoneBalance] [-PlatformFaultDomainCount <Int32>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-EnableAutomaticRepair] [-AutomaticRepairGracePeriod <String>]
 [-AutoOSUpgrade] [-DisableAutoRollback <Boolean>] [-EnableUltraSSD] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-EvictionPolicy <String>]
 [-MaxPrice <Double>] [-TerminateScheduledEvents] [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>]
 [-ProximityPlacementGroupId <String>] [-ScaleInPolicy <String[]>] -IdentityType <ResourceIdentityType>
 [-IdentityId <String[]>] [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="54fb1-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="54fb1-107">DESCRIPTION</span></span>
<span data-ttu-id="54fb1-108">**Yeni-AzVmssConfig** cmdlet 'i, yapılandırılabilir yerel sanal Manager ölçek KÜMESI (VMSS) nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="54fb1-108">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="54fb1-109">VMSS nesnesini yapılandırmak için diğer cmdlet 'ler gereklidir.</span><span class="sxs-lookup"><span data-stu-id="54fb1-109">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="54fb1-110">Bu cmdlet 'ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="54fb1-110">These cmdlets are:</span></span>
- <span data-ttu-id="54fb1-111">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="54fb1-111">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="54fb1-112">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="54fb1-112">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="54fb1-113">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="54fb1-113">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="54fb1-114">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="54fb1-114">Add-AzVmssExtension</span></span>

## <span data-ttu-id="54fb1-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="54fb1-115">EXAMPLES</span></span>

### <span data-ttu-id="54fb1-116">Örnek 1: bir VMSS yapılandırma nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="54fb1-116">Example 1: Create a VMSS configuration object</span></span>
```powershell
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

<span data-ttu-id="54fb1-117">Bu örnek bir VMSS yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="54fb1-117">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="54fb1-118">İlk komut, bir VMSS yapılandırma nesnesi oluşturmak için **New-AzVmssConfig** cmdlet 'ini kullanır ve sonucu $VMSS adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="54fb1-118">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="54fb1-119">İkinci komut, ilk komutta oluşturulan VMSS yapılandırma nesnesini kullanan bir VMSS oluşturmak için **New-AzVmss** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="54fb1-119">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

### <span data-ttu-id="54fb1-120">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="54fb1-120">Example 2</span></span>

<span data-ttu-id="54fb1-121">Bir VMSS yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="54fb1-121">Creates a VMSS configuration object.</span></span> <span data-ttu-id="54fb1-122">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="54fb1-122">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzVmssConfig -Location <String> -Overprovision $false -SkuCapacity 2 -SkuName 'Standard_A0' -Tag 'Sql' -UpgradePolicyMode Automatic
```

## <span data-ttu-id="54fb1-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="54fb1-123">PARAMETERS</span></span>

### <span data-ttu-id="54fb1-124">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="54fb1-124">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="54fb1-125">VM 'deki durum değişikliği nedeniyle otomatik onarımların askıya alındığı süre.</span><span class="sxs-lookup"><span data-stu-id="54fb1-125">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="54fb1-126">Kullanım süresi, durum değişikliği tamamlandıktan sonra başlar.</span><span class="sxs-lookup"><span data-stu-id="54fb1-126">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="54fb1-127">Bu, erken veya kazayla onarılmasını önlemeye yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="54fb1-127">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="54fb1-128">Süre ISO 8601 biçiminde belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="54fb1-128">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="54fb1-129">İzin verilen en düşük kullanım süresi 30 dakika (PT30M), bu da varsayılan değerdir.</span><span class="sxs-lookup"><span data-stu-id="54fb1-129">The minimum allowed grace period is 30 minutes (PT30M), which is also the default value.</span></span> <span data-ttu-id="54fb1-130">İzin verilen en büyük kullanım süresi 90 dakikadır (PT90M).</span><span class="sxs-lookup"><span data-stu-id="54fb1-130">The maximum allowed grace period is 90 minutes (PT90M).</span></span>

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

### <span data-ttu-id="54fb1-131">-Autoosupgrad</span><span class="sxs-lookup"><span data-stu-id="54fb1-131">-AutoOSUpgrade</span></span>
<span data-ttu-id="54fb1-132">Resmin daha yeni bir sürümü kullanılabilir hale geldiğinde, bir yerde ölçeklendirme kümesi örneklerine otomatik olarak işletim sistemi yükseltmeleri uygulanıp uygulanmayacağı.</span><span class="sxs-lookup"><span data-stu-id="54fb1-132">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="54fb1-133">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="54fb1-133">-BootDiagnostic</span></span>
<span data-ttu-id="54fb1-134">Sanal makine ölçek kümesi önyükleme tanılaması profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="54fb1-134">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="54fb1-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54fb1-135">-DefaultProfile</span></span>
<span data-ttu-id="54fb1-136">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="54fb1-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54fb1-137">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="54fb1-137">-DisableAutoRollback</span></span>
<span data-ttu-id="54fb1-138">Otomatik OS yükseltme Ilkesi için otomatik geri almayı devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="54fb1-138">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="54fb1-139">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="54fb1-139">-EnableAutomaticRepair</span></span>
<span data-ttu-id="54fb1-140">Sanal makine ölçek kümesinde otomatik onarımları etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="54fb1-140">Enables automatic repairs on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="54fb1-141">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="54fb1-141">-EnableUltraSSD</span></span>
<span data-ttu-id="54fb1-142">Sanal makine ölçek kümesinde UltraSSD_LRS depolama hesabı türüne sahip bir veya birden çok yönetilen veri diskine sahip olmak olanak verir.</span><span class="sxs-lookup"><span data-stu-id="54fb1-142">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="54fb1-143">Depolama hesap türü UltraSSD_LRS yönetilen diskler yalnızca bu özellik etkinse bir VMSUBNET 'e eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="54fb1-143">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="54fb1-144">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="54fb1-144">-EncryptionAtHost</span></span>
<span data-ttu-id="54fb1-145">Bu parametre, konaktaki kaynak/Temp diski dahil tüm disklerde şifrelemeyi etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="54fb1-145">This parameter will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="54fb1-146">Varsayılan: Bu özellik kaynak için doğru olarak ayarlanmadıkça konaktaki şifreleme devre dışı bırakılır.</span><span class="sxs-lookup"><span data-stu-id="54fb1-146">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

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

### <span data-ttu-id="54fb1-147">-Çıkarma Ilkesi</span><span class="sxs-lookup"><span data-stu-id="54fb1-147">-EvictionPolicy</span></span>
<span data-ttu-id="54fb1-148">Ölçek kümesindeki sanal makinelerin çıkarma ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="54fb1-148">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="54fb1-149">Uzantılı</span><span class="sxs-lookup"><span data-stu-id="54fb1-149">-Extension</span></span>
<span data-ttu-id="54fb1-150">VMSS için uzantı bilgileri nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="54fb1-150">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="54fb1-151">Bu nesneyi eklemek için **Add-AzVmssExtension** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="54fb1-151">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="54fb1-152">-Healthprobeıd</span><span class="sxs-lookup"><span data-stu-id="54fb1-152">-HealthProbeId</span></span>
<span data-ttu-id="54fb1-153">Sanal makine ölçeği kümesindeki bir örneğin durumunu belirlemek için kullanılan yük dengeleyici araştırması KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="54fb1-153">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="54fb1-154">Healthprobeıd, '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName} ' biçiminde.</span><span class="sxs-lookup"><span data-stu-id="54fb1-154">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="54fb1-155">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="54fb1-155">-IdentityId</span></span>
<span data-ttu-id="54fb1-156">Sanal makine ölçek kümesiyle ilişkili kullanıcı kimliklerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="54fb1-156">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="54fb1-157">Kullanıcı kimliği başvuruları formda ARM kaynak kimlikleri olacaktır: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="54fb1-157">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="54fb1-158">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="54fb1-158">-IdentityType</span></span>
<span data-ttu-id="54fb1-159">Sanal makine ölçek kümesi için kullanılan kimlik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="54fb1-159">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="54fb1-160">' Systemassigneduserın ' türü, örtülü olarak oluşturulmuş bir kimlik ve Kullanıcı tarafından atanan kimlikler kümesini içerir.</span><span class="sxs-lookup"><span data-stu-id="54fb1-160">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="54fb1-161">' None ' türü, sanal makine ölçek kümesindeki tüm kimlikleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="54fb1-161">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="54fb1-162">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="54fb1-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="54fb1-163">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="54fb1-163">SystemAssigned</span></span>
- <span data-ttu-id="54fb1-164">Kullanıcı tarafından atanmış</span><span class="sxs-lookup"><span data-stu-id="54fb1-164">UserAssigned</span></span>
- <span data-ttu-id="54fb1-165">Systemassigneduseratandı</span><span class="sxs-lookup"><span data-stu-id="54fb1-165">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="54fb1-166">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="54fb1-166">None</span></span>

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

### <span data-ttu-id="54fb1-167">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="54fb1-167">-LicenseType</span></span>
<span data-ttu-id="54fb1-168">Kendi lisans senaryonuzu verecek lisans türünü belirtin.</span><span class="sxs-lookup"><span data-stu-id="54fb1-168">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="54fb1-169">-Konum</span><span class="sxs-lookup"><span data-stu-id="54fb1-169">-Location</span></span>
<span data-ttu-id="54fb1-170">VMSS 'nin oluşturulduğu Azure konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="54fb1-170">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="54fb1-171">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="54fb1-171">-MaxPrice</span></span>
<span data-ttu-id="54fb1-172">Bir spot VM/VMSS için ödemek istediğiniz en yüksek fiyatı belirtir.</span><span class="sxs-lookup"><span data-stu-id="54fb1-172">Specifies the maximum price you are willing to pay for a Spot VM/VMSS.</span></span> <span data-ttu-id="54fb1-173">Bu fiyat ABD doları cinsindendir.</span><span class="sxs-lookup"><span data-stu-id="54fb1-173">This price is in US Dollars.</span></span> <span data-ttu-id="54fb1-174">Bu fiyat VM boyutu için geçerli nokta fiyatıyla karşılaştırılır.</span><span class="sxs-lookup"><span data-stu-id="54fb1-174">This price will be compared with the current Spot price for the VM size.</span></span> <span data-ttu-id="54fb1-175">Ayrıca, fiyatlar nokta VM/VMSS oluşturma/güncelleştirme sırasında karşılaştırılır ve işlem yalnızca maxPrice geçerli nokta fiyatından büyükse başarılı olur.</span><span class="sxs-lookup"><span data-stu-id="54fb1-175">Also, the prices are compared at the time of create/update of Spot VM/VMSS and the operation will only succeed if the maxPrice is greater than the current Spot price.</span></span> <span data-ttu-id="54fb1-176">Geçerli nokta fiyatı VM/VMSS oluşturulduktan sonra maxPrice 'den fazla olursa maxPrice de bir spot VM/VMSS çıkarmak için kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="54fb1-176">The maxPrice will also be used for evicting a Spot VM/VMSS if the current Spot price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="54fb1-177">Olası değerler: sıfırdan büyük herhangi bir ondalık değer.</span><span class="sxs-lookup"><span data-stu-id="54fb1-177">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="54fb1-178">Örnek: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="54fb1-178">Example: 0.01538.</span></span>  <span data-ttu-id="54fb1-179">-1, Fiyat nedenlerinin nokta VM/VMSS 'den çıkarılmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="54fb1-179">-1 indicates that the Spot VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="54fb1-180">Ayrıca, sizin sağlanmadıysa varsayılan en fazla fiyat-1 ' dir.</span><span class="sxs-lookup"><span data-stu-id="54fb1-180">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="54fb1-181">-Networkınterfaceconfiguration</span><span class="sxs-lookup"><span data-stu-id="54fb1-181">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="54fb1-182">VMSS yapılandırması için ağ özelliklerini içeren ağ profili nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="54fb1-182">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="54fb1-183">Bu nesneyi eklemek için **Add-Azvmssnetworkınterfaceyapılandırma** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="54fb1-183">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="54fb1-184">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="54fb1-184">-OsProfile</span></span>
<span data-ttu-id="54fb1-185">VMSS yapılandırması işletim sistemi özelliklerini içeren işletim sistemi profili nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="54fb1-185">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="54fb1-186">Bu nesneyi ayarlamak için **set-AzVmssOsProfile** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="54fb1-186">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="54fb1-187">-Overprovision</span><span class="sxs-lookup"><span data-stu-id="54fb1-187">-Overprovision</span></span>
<span data-ttu-id="54fb1-188">Cmdlet 'in VMSS 'yi içerip içermediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="54fb1-188">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="54fb1-189">-PlanName</span><span class="sxs-lookup"><span data-stu-id="54fb1-189">-PlanName</span></span>
<span data-ttu-id="54fb1-190">Plan adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="54fb1-190">Specifies the plan name.</span></span>

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

### <span data-ttu-id="54fb1-191">-Planürün</span><span class="sxs-lookup"><span data-stu-id="54fb1-191">-PlanProduct</span></span>
<span data-ttu-id="54fb1-192">Plan ürünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="54fb1-192">Specifies the plan product.</span></span>

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

### <span data-ttu-id="54fb1-193">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="54fb1-193">-PlanPromotionCode</span></span>
<span data-ttu-id="54fb1-194">Plan promosyon kodunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="54fb1-194">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="54fb1-195">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="54fb1-195">-PlanPublisher</span></span>
<span data-ttu-id="54fb1-196">Publisher planı 'nı belirtir.</span><span class="sxs-lookup"><span data-stu-id="54fb1-196">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="54fb1-197">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="54fb1-197">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="54fb1-198">Her bir yerleştirme grubu için hata etki alanı sayısı.</span><span class="sxs-lookup"><span data-stu-id="54fb1-198">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="54fb1-199">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="54fb1-199">-Priority</span></span>
<span data-ttu-id="54fb1-200">Ölçek kümesindeki sanal birim için öncelik.</span><span class="sxs-lookup"><span data-stu-id="54fb1-200">The priority for the virtual machien in the scale set.</span></span>  <span data-ttu-id="54fb1-201">Yalnızca desteklenen değerler ' Regular ', ' nokta ' ve ' düşük ' değerleridir.</span><span class="sxs-lookup"><span data-stu-id="54fb1-201">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="54fb1-202">' Regular ' normal sanal makine içindir.</span><span class="sxs-lookup"><span data-stu-id="54fb1-202">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="54fb1-203">' Spot ', spot sanal makine içindir.</span><span class="sxs-lookup"><span data-stu-id="54fb1-203">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="54fb1-204">' Low ', spot sanal makine için de, ancak ' nokta ' ile değiştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="54fb1-204">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="54fb1-205">Lütfen ' düşük ' yerine ' nokta ' kullanın.</span><span class="sxs-lookup"><span data-stu-id="54fb1-205">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="54fb1-206">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="54fb1-206">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="54fb1-207">Bu ölçek kümesiyle kullanılacak yakınlık Yerleşim grubunun kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="54fb1-207">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="54fb1-208">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="54fb1-208">-RollingUpgradePolicy</span></span>
<span data-ttu-id="54fb1-209">Çalışırken yükseltme ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="54fb1-209">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="54fb1-210">-Scaleınpolicy</span><span class="sxs-lookup"><span data-stu-id="54fb1-210">-ScaleInPolicy</span></span>
<span data-ttu-id="54fb1-211">Sanal makine ölçeği kümesinde ölçeklendirme yapılırken izlenen kurallar.</span><span class="sxs-lookup"><span data-stu-id="54fb1-211">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="54fb1-212">Olası değerler: ' default ', ' OldestVM ' ve ' NewestVM '.</span><span class="sxs-lookup"><span data-stu-id="54fb1-212">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="54fb1-213">' Varsayılan ' sanal makine ölçeği kümesi içinde ölçeklendirildiyse, ölçek kümesi ilk olarak bölgeler genelinde dengelenebilir ve bu bir zonal ölçeği kümesidir.</span><span class="sxs-lookup"><span data-stu-id="54fb1-213">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="54fb1-214">Ardından, hata etki alanları genelinde mümkün olduğunca dengeli olacaktır.</span><span class="sxs-lookup"><span data-stu-id="54fb1-214">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="54fb1-215">Her hata etki alanı içinde, kaldırılmak üzere seçilen sanal makineler, ölçek ile korunmayan en yeni değerler olacaktır.</span><span class="sxs-lookup"><span data-stu-id="54fb1-215">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="54fb1-216">' OldestVM ' sanal makine ölçeği kümesi ölçeklendiğinde, ölçeğe korunmayan en eski sanal makineler kaldırılmak üzere seçilir.</span><span class="sxs-lookup"><span data-stu-id="54fb1-216">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="54fb1-217">Zonal sanal makine ölçek kümeleri için, ölçek kümesi önce bölgeler arasında dengelenecek.</span><span class="sxs-lookup"><span data-stu-id="54fb1-217">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="54fb1-218">Her bir bölgede, korunmayan en eski sanal makineler kaldırılmak üzere seçilir.</span><span class="sxs-lookup"><span data-stu-id="54fb1-218">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="54fb1-219">' NewestVM ' sanal makine ölçeği kümesi ölçeklendiğinde, ölçeğe korunmayan en yeni sanal makineler kaldırılmak üzere seçilir.</span><span class="sxs-lookup"><span data-stu-id="54fb1-219">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="54fb1-220">Zonal sanal makine ölçek kümeleri için, ölçek kümesi önce bölgeler arasında dengelenecek.</span><span class="sxs-lookup"><span data-stu-id="54fb1-220">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="54fb1-221">Her bir bölgede, korunmayan en yeni sanal makineler kaldırılmak üzere seçilir.</span><span class="sxs-lookup"><span data-stu-id="54fb1-221">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="54fb1-222">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="54fb1-222">-SinglePlacementGroup</span></span>
<span data-ttu-id="54fb1-223">Tek yerleşim grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="54fb1-223">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="54fb1-224">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="54fb1-224">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="54fb1-225">Uzantıların fazladan sağlanan diğer VM 'lerde çalıştırılmamıştır.</span><span class="sxs-lookup"><span data-stu-id="54fb1-225">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="54fb1-226">-Skukapasitesi</span><span class="sxs-lookup"><span data-stu-id="54fb1-226">-SkuCapacity</span></span>
<span data-ttu-id="54fb1-227">VMSS 'deki örneklerin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="54fb1-227">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="54fb1-228">-SkuName</span><span class="sxs-lookup"><span data-stu-id="54fb1-228">-SkuName</span></span>
<span data-ttu-id="54fb1-229">Tüm VMSS örneklerinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="54fb1-229">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="54fb1-230">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="54fb1-230">-SkuTier</span></span>
<span data-ttu-id="54fb1-231">VMSS 'nin katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="54fb1-231">Specifies the tier of VMSS.</span></span> <span data-ttu-id="54fb1-232">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="54fb1-232">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="54fb1-233">Ardından</span><span class="sxs-lookup"><span data-stu-id="54fb1-233">Standard</span></span>
- <span data-ttu-id="54fb1-234">Ana</span><span class="sxs-lookup"><span data-stu-id="54fb1-234">Basic</span></span>

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

### <span data-ttu-id="54fb1-235">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="54fb1-235">-StorageProfile</span></span>
<span data-ttu-id="54fb1-236">VMSS yapılandırması için disk özelliklerini içeren depolama profili nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="54fb1-236">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="54fb1-237">Bu nesneyi ayarlamak için **set-AzVmssStorageProfile** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="54fb1-237">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="54fb1-238">Etiketli</span><span class="sxs-lookup"><span data-stu-id="54fb1-238">-Tag</span></span>
<span data-ttu-id="54fb1-239">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="54fb1-239">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="54fb1-240">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="54fb1-240">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="54fb1-241">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="54fb1-241">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="54fb1-242">Yapılandırılabilir süre (dakika cinsinden) silinen bir sanal makinenin, etkinlik otomatik onaylanmadan (zaman aşımına uğramadan) önce zamanlanmış olayı sonlandırmasını sağlamak gerekecektir.</span><span class="sxs-lookup"><span data-stu-id="54fb1-242">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="54fb1-243">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="54fb1-243">-TerminateScheduledEvents</span></span>
<span data-ttu-id="54fb1-244">Zamanlanmış olayları Sonlandır özelliğini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="54fb1-244">Enable the Terminate Scheduled events</span></span>

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

### <span data-ttu-id="54fb1-245">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="54fb1-245">-UpgradePolicyMode</span></span>
<span data-ttu-id="54fb1-246">Belirtilen ölçek kümesindeki sanal makinelere yükseltme modu.</span><span class="sxs-lookup"><span data-stu-id="54fb1-246">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="54fb1-247">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="54fb1-247">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="54fb1-248">Otomatik</span><span class="sxs-lookup"><span data-stu-id="54fb1-248">Automatic</span></span>
- <span data-ttu-id="54fb1-249">El ile</span><span class="sxs-lookup"><span data-stu-id="54fb1-249">Manual</span></span>

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

### <span data-ttu-id="54fb1-250">-Bölge</span><span class="sxs-lookup"><span data-stu-id="54fb1-250">-Zone</span></span>
<span data-ttu-id="54fb1-251">Sanal makine ölçek kümesi için bölge listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="54fb1-251">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="54fb1-252">-Bölgbakiye</span><span class="sxs-lookup"><span data-stu-id="54fb1-252">-ZoneBalance</span></span>
<span data-ttu-id="54fb1-253">Bölge kesilmesi durumunda, tam çift sanal makine dağıtımını x bölgeler çapraz olarak zorunlu tutulmayacağı.</span><span class="sxs-lookup"><span data-stu-id="54fb1-253">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="54fb1-254">-Onay</span><span class="sxs-lookup"><span data-stu-id="54fb1-254">-Confirm</span></span>
<span data-ttu-id="54fb1-255">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="54fb1-255">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54fb1-256">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54fb1-256">-WhatIf</span></span>
<span data-ttu-id="54fb1-257">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="54fb1-257">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="54fb1-258">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="54fb1-258">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54fb1-259">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54fb1-259">CommonParameters</span></span>
<span data-ttu-id="54fb1-260">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="54fb1-260">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54fb1-261">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="54fb1-261">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54fb1-262">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="54fb1-262">INPUTS</span></span>

### <span data-ttu-id="54fb1-263">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="54fb1-263">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="54fb1-264">System. String</span><span class="sxs-lookup"><span data-stu-id="54fb1-264">System.String</span></span>

### <span data-ttu-id="54fb1-265">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="54fb1-265">System.Collections.Hashtable</span></span>

### <span data-ttu-id="54fb1-266">System. Int32</span><span class="sxs-lookup"><span data-stu-id="54fb1-266">System.Int32</span></span>

### <span data-ttu-id="54fb1-267">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. modeller. Yükseltmodu, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="54fb1-267">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="54fb1-268">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSetOSProfile</span><span class="sxs-lookup"><span data-stu-id="54fb1-268">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="54fb1-269">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSetStorageProfile</span><span class="sxs-lookup"><span data-stu-id="54fb1-269">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="54fb1-270">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSetNetworkConfiguration []</span><span class="sxs-lookup"><span data-stu-id="54fb1-270">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="54fb1-271">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSetExtension []</span><span class="sxs-lookup"><span data-stu-id="54fb1-271">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="54fb1-272">System. String []</span><span class="sxs-lookup"><span data-stu-id="54fb1-272">System.String[]</span></span>

### <span data-ttu-id="54fb1-273">Microsoft. Azure. Management. COMPUTE. model. RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="54fb1-273">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="54fb1-274">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="54fb1-274">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="54fb1-275">Microsoft. Azure. Management. COMPUTE. modeller. BootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="54fb1-275">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="54fb1-276">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. modeller. Kaynakıdentitytype, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="54fb1-276">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="54fb1-277">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="54fb1-277">OUTPUTS</span></span>

### <span data-ttu-id="54fb1-278">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="54fb1-278">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="54fb1-279">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="54fb1-279">NOTES</span></span>

## <span data-ttu-id="54fb1-280">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="54fb1-280">RELATED LINKS</span></span>

[<span data-ttu-id="54fb1-281">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="54fb1-281">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="54fb1-282">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="54fb1-282">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="54fb1-283">Add-Azvmssnetworkınterfaceconfiguration</span><span class="sxs-lookup"><span data-stu-id="54fb1-283">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="54fb1-284">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="54fb1-284">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="54fb1-285">Yeni-AzVmss</span><span class="sxs-lookup"><span data-stu-id="54fb1-285">New-AzVmss</span></span>](./New-AzVmss.md)
