---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssConfig.md
ms.openlocfilehash: e65bfa607f9689a85f7734b1913bbabadd4dd115
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752825"
---
# <span data-ttu-id="55096-101">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="55096-101">New-AzVmssConfig</span></span>

## <span data-ttu-id="55096-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55096-102">SYNOPSIS</span></span>
<span data-ttu-id="55096-103">Bir VMSS yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="55096-103">Creates a VMSS configuration object.</span></span>

## <span data-ttu-id="55096-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="55096-104">SYNTAX</span></span>

### <span data-ttu-id="55096-105">DefaultParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="55096-105">DefaultParameterSet (Default)</span></span>
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
 [-MaxPrice <Double>] [-TerminateScheduledEvents] [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>]
 [-ProximityPlacementGroupId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="55096-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="55096-106">ExplicitIdentityParameterSet</span></span>
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
 [-MaxPrice <Double>] [-TerminateScheduledEvents] [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>]
 [-ProximityPlacementGroupId <String>] -IdentityType <ResourceIdentityType> [-IdentityId <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55096-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="55096-107">AssignIdentityParameterSet</span></span>
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
 [-MaxPrice <Double>] [-TerminateScheduledEvents] [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>]
 [-ProximityPlacementGroupId <String>] [-AssignIdentity] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55096-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="55096-108">DESCRIPTION</span></span>
<span data-ttu-id="55096-109">**Yeni-AzVmssConfig** cmdlet 'i, yapılandırılabilir yerel sanal Manager ölçek KÜMESI (VMSS) nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="55096-109">The **New-AzVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="55096-110">VMSS nesnesini yapılandırmak için diğer cmdlet 'ler gereklidir.</span><span class="sxs-lookup"><span data-stu-id="55096-110">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="55096-111">Bu cmdlet 'ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="55096-111">These cmdlets are:</span></span>
- <span data-ttu-id="55096-112">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="55096-112">Set-AzVmssOsProfile</span></span>
- <span data-ttu-id="55096-113">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="55096-113">Set-AzVmssStorageProfile</span></span>
- <span data-ttu-id="55096-114">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="55096-114">Add-AzVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="55096-115">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="55096-115">Add-AzVmssExtension</span></span>

## <span data-ttu-id="55096-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="55096-116">EXAMPLES</span></span>

### <span data-ttu-id="55096-117">Örnek 1: bir VMSS yapılandırma nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="55096-117">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="55096-118">Bu örnek bir VMSS yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="55096-118">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="55096-119">İlk komut, bir VMSS yapılandırma nesnesi oluşturmak için **New-AzVmssConfig** cmdlet 'ini kullanır ve sonucu $VMSS adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="55096-119">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="55096-120">İkinci komut, ilk komutta oluşturulan VMSS yapılandırma nesnesini kullanan bir VMSS oluşturmak için **New-AzVmss** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="55096-120">The second command uses the **New-AzVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="55096-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="55096-121">PARAMETERS</span></span>

### <span data-ttu-id="55096-122">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="55096-122">-AssignIdentity</span></span>
<span data-ttu-id="55096-123">Sanal makine ölçek kümesi için sistem tarafından atanan kimliği belirtin.</span><span class="sxs-lookup"><span data-stu-id="55096-123">Specify the system assigned identity for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="55096-124">-Autoosupgrad</span><span class="sxs-lookup"><span data-stu-id="55096-124">-AutoOSUpgrade</span></span>
<span data-ttu-id="55096-125">Resmin daha yeni bir sürümü kullanılabilir hale geldiğinde, bir yerde ölçeklendirme kümesi örneklerine otomatik olarak işletim sistemi yükseltmeleri uygulanıp uygulanmayacağı.</span><span class="sxs-lookup"><span data-stu-id="55096-125">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="55096-126">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="55096-126">-BootDiagnostic</span></span>
<span data-ttu-id="55096-127">Sanal makine ölçek kümesi önyükleme tanılaması profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="55096-127">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="55096-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55096-128">-DefaultProfile</span></span>
<span data-ttu-id="55096-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="55096-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55096-130">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="55096-130">-DisableAutoRollback</span></span>
<span data-ttu-id="55096-131">Otomatik OS yükseltme Ilkesi için otomatik geri almayı devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="55096-131">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="55096-132">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="55096-132">-EnableUltraSSD</span></span>
<span data-ttu-id="55096-133">Sanal makine ölçek kümesinde UltraSSD_LRS depolama hesabı türüne sahip bir veya birden çok yönetilen veri diskine sahip olmak olanak verir.</span><span class="sxs-lookup"><span data-stu-id="55096-133">Enables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="55096-134">Depolama hesap türü UltraSSD_LRS yönetilen diskler yalnızca bu özellik etkinse bir VMSUBNET 'e eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="55096-134">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="55096-135">-Çıkarma Ilkesi</span><span class="sxs-lookup"><span data-stu-id="55096-135">-EvictionPolicy</span></span>
<span data-ttu-id="55096-136">Ölçek kümesindeki sanal makinelerin çıkarma ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="55096-136">Specifies the eviction policy for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="55096-137">Uzantılı</span><span class="sxs-lookup"><span data-stu-id="55096-137">-Extension</span></span>
<span data-ttu-id="55096-138">VMSS için uzantı bilgileri nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="55096-138">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="55096-139">Bu nesneyi eklemek için **Add-AzVmssExtension** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="55096-139">You can use the **Add-AzVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="55096-140">-Healthprobeıd</span><span class="sxs-lookup"><span data-stu-id="55096-140">-HealthProbeId</span></span>
<span data-ttu-id="55096-141">Sanal makine ölçeği kümesindeki bir örneğin durumunu belirlemek için kullanılan yük dengeleyici araştırması KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="55096-141">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="55096-142">Healthprobeıd, '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName} ' biçiminde.</span><span class="sxs-lookup"><span data-stu-id="55096-142">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="55096-143">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="55096-143">-IdentityId</span></span>
<span data-ttu-id="55096-144">Sanal makine ölçek kümesiyle ilişkili kullanıcı kimliklerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="55096-144">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="55096-145">Kullanıcı kimliği başvuruları formda ARM kaynak kimlikleri olacaktır: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="55096-145">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="55096-146">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="55096-146">-IdentityType</span></span>
<span data-ttu-id="55096-147">Sanal makine ölçek kümesi için kullanılan kimlik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="55096-147">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="55096-148">' Systemassigneduserın ' türü, örtülü olarak oluşturulmuş bir kimlik ve Kullanıcı tarafından atanan kimlikler kümesini içerir.</span><span class="sxs-lookup"><span data-stu-id="55096-148">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="55096-149">' None ' türü, sanal makine ölçek kümesindeki tüm kimlikleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="55096-149">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="55096-150">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="55096-150">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="55096-151">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="55096-151">SystemAssigned</span></span>
- <span data-ttu-id="55096-152">Kullanıcı tarafından atanmış</span><span class="sxs-lookup"><span data-stu-id="55096-152">UserAssigned</span></span>
- <span data-ttu-id="55096-153">Systemassigneduseratandı</span><span class="sxs-lookup"><span data-stu-id="55096-153">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="55096-154">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="55096-154">None</span></span>

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

### <span data-ttu-id="55096-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="55096-155">-LicenseType</span></span>
<span data-ttu-id="55096-156">Kendi lisans senaryonuzu verecek lisans türünü belirtin.</span><span class="sxs-lookup"><span data-stu-id="55096-156">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="55096-157">-Konum</span><span class="sxs-lookup"><span data-stu-id="55096-157">-Location</span></span>
<span data-ttu-id="55096-158">VMSS 'nin oluşturulduğu Azure konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="55096-158">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="55096-159">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="55096-159">-MaxPrice</span></span>
<span data-ttu-id="55096-160">Düşük öncelikli VM/VMSS için ödemek istediğiniz en yüksek fiyatı belirtir.</span><span class="sxs-lookup"><span data-stu-id="55096-160">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="55096-161">Bu fiyat ABD doları cinsindendir.</span><span class="sxs-lookup"><span data-stu-id="55096-161">This price is in US Dollars.</span></span> <span data-ttu-id="55096-162">Bu fiyat VM boyutu için geçerli düşük öncelik fiyatıyla karşılaştırılır.</span><span class="sxs-lookup"><span data-stu-id="55096-162">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="55096-163">Ayrıca, düşük öncelikli VM/VMSS oluşturma/güncelleştirme sırasında fiyatlar karşılaştırılır ve işlem yalnızca maxPrice geçerli düşük öncelik fiyatından büyükse başarıdır.</span><span class="sxs-lookup"><span data-stu-id="55096-163">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="55096-164">Geçerli düşük öncelik fiyatının VM/VMSS oluşturulduktan sonra maxPrice 'den fazla olması durumunda, maxPrice de düşük öncelikli VM/VMSS çıkarmak için kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="55096-164">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="55096-165">Olası değerler: sıfırdan büyük herhangi bir ondalık değer.</span><span class="sxs-lookup"><span data-stu-id="55096-165">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="55096-166">Örnek: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="55096-166">Example: 0.01538.</span></span>  <span data-ttu-id="55096-167">-1 düşük öncelikli VM/VMSS 'nin fiyat nedenlerinin çıkarılmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="55096-167">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="55096-168">Ayrıca, sizin sağlanmadıysa varsayılan en fazla fiyat-1 ' dir.</span><span class="sxs-lookup"><span data-stu-id="55096-168">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="55096-169">-Networkınterfaceconfiguration</span><span class="sxs-lookup"><span data-stu-id="55096-169">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="55096-170">VMSS yapılandırması için ağ özelliklerini içeren ağ profili nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="55096-170">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="55096-171">Bu nesneyi eklemek için **Add-Azvmssnetworkınterfaceyapılandırma** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="55096-171">You can use the **Add-AzVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="55096-172">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="55096-172">-OsProfile</span></span>
<span data-ttu-id="55096-173">VMSS yapılandırması işletim sistemi özelliklerini içeren işletim sistemi profili nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="55096-173">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="55096-174">Bu nesneyi ayarlamak için **set-AzVmssOsProfile** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="55096-174">You can use the **Set-AzVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="55096-175">-Overprovision</span><span class="sxs-lookup"><span data-stu-id="55096-175">-Overprovision</span></span>
<span data-ttu-id="55096-176">Cmdlet 'in VMSS 'yi içerip içermediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="55096-176">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="55096-177">-PlanName</span><span class="sxs-lookup"><span data-stu-id="55096-177">-PlanName</span></span>
<span data-ttu-id="55096-178">Plan adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="55096-178">Specifies the plan name.</span></span>

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

### <span data-ttu-id="55096-179">-Planürün</span><span class="sxs-lookup"><span data-stu-id="55096-179">-PlanProduct</span></span>
<span data-ttu-id="55096-180">Plan ürünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="55096-180">Specifies the plan product.</span></span>

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

### <span data-ttu-id="55096-181">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="55096-181">-PlanPromotionCode</span></span>
<span data-ttu-id="55096-182">Plan promosyon kodunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="55096-182">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="55096-183">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="55096-183">-PlanPublisher</span></span>
<span data-ttu-id="55096-184">Publisher planı 'nı belirtir.</span><span class="sxs-lookup"><span data-stu-id="55096-184">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="55096-185">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="55096-185">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="55096-186">Her bir yerleştirme grubu için hata etki alanı sayısı.</span><span class="sxs-lookup"><span data-stu-id="55096-186">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="55096-187">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="55096-187">-Priority</span></span>
<span data-ttu-id="55096-188">Ölçek kümesindeki sanal makinelerin önceliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="55096-188">Specifies the priority for the virtual machines in the scale set.</span></span>

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

### <span data-ttu-id="55096-189">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="55096-189">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="55096-190">ProximityPlacementGroup kimliği</span><span class="sxs-lookup"><span data-stu-id="55096-190">The Id of ProximityPlacementGroup</span></span>

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

### <span data-ttu-id="55096-191">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="55096-191">-RollingUpgradePolicy</span></span>
<span data-ttu-id="55096-192">Çalışırken yükseltme ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="55096-192">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="55096-193">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="55096-193">-SinglePlacementGroup</span></span>
<span data-ttu-id="55096-194">Tek yerleşim grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="55096-194">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="55096-195">-Skukapasitesi</span><span class="sxs-lookup"><span data-stu-id="55096-195">-SkuCapacity</span></span>
<span data-ttu-id="55096-196">VMSS 'deki örneklerin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="55096-196">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="55096-197">-SkuName</span><span class="sxs-lookup"><span data-stu-id="55096-197">-SkuName</span></span>
<span data-ttu-id="55096-198">Tüm VMSS örneklerinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="55096-198">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="55096-199">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="55096-199">-SkuTier</span></span>
<span data-ttu-id="55096-200">VMSS 'nin katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="55096-200">Specifies the tier of VMSS.</span></span> <span data-ttu-id="55096-201">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="55096-201">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="55096-202">Ardından</span><span class="sxs-lookup"><span data-stu-id="55096-202">Standard</span></span>
- <span data-ttu-id="55096-203">Ana</span><span class="sxs-lookup"><span data-stu-id="55096-203">Basic</span></span>

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

### <span data-ttu-id="55096-204">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="55096-204">-StorageProfile</span></span>
<span data-ttu-id="55096-205">VMSS yapılandırması için disk özelliklerini içeren depolama profili nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="55096-205">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="55096-206">Bu nesneyi ayarlamak için **set-AzVmssStorageProfile** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="55096-206">You can use the **Set-AzVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="55096-207">Etiketli</span><span class="sxs-lookup"><span data-stu-id="55096-207">-Tag</span></span>
<span data-ttu-id="55096-208">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="55096-208">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="55096-209">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="55096-209">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="55096-210">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="55096-210">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="55096-211">Yapılandırılabilir süre (dakika cinsinden) silinen bir sanal makinenin, etkinlik otomatik onaylanmadan (zaman aşımına uğramadan) önce zamanlanmış olayı sonlandırmasını sağlamak gerekecektir.</span><span class="sxs-lookup"><span data-stu-id="55096-211">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="55096-212">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="55096-212">-TerminateScheduledEvents</span></span>
<span data-ttu-id="55096-213">Zamanlanmış olayları Sonlandır özelliğini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="55096-213">Enable the Terminate Scheduled events</span></span>

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

### <span data-ttu-id="55096-214">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="55096-214">-UpgradePolicyMode</span></span>
<span data-ttu-id="55096-215">Belirtilen ölçek kümesindeki sanal makinelere yükseltme modu.</span><span class="sxs-lookup"><span data-stu-id="55096-215">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="55096-216">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="55096-216">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="55096-217">Otomatik</span><span class="sxs-lookup"><span data-stu-id="55096-217">Automatic</span></span>
- <span data-ttu-id="55096-218">El ile</span><span class="sxs-lookup"><span data-stu-id="55096-218">Manual</span></span>

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

### <span data-ttu-id="55096-219">-Bölge</span><span class="sxs-lookup"><span data-stu-id="55096-219">-Zone</span></span>
<span data-ttu-id="55096-220">Sanal makine ölçek kümesi için bölge listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="55096-220">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="55096-221">-Bölgbakiye</span><span class="sxs-lookup"><span data-stu-id="55096-221">-ZoneBalance</span></span>
<span data-ttu-id="55096-222">Bölge kesilmesi durumunda, tam çift sanal makine dağıtımını x bölgeler çapraz olarak zorunlu tutulmayacağı.</span><span class="sxs-lookup"><span data-stu-id="55096-222">Whether to force strictly even Virtual Machine distribution cross x-zones in case there is zone outage.</span></span>

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

### <span data-ttu-id="55096-223">-Onay</span><span class="sxs-lookup"><span data-stu-id="55096-223">-Confirm</span></span>
<span data-ttu-id="55096-224">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="55096-224">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55096-225">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55096-225">-WhatIf</span></span>
<span data-ttu-id="55096-226">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="55096-226">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="55096-227">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="55096-227">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55096-228">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55096-228">CommonParameters</span></span>
<span data-ttu-id="55096-229">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="55096-229">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55096-230">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="55096-230">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55096-231">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="55096-231">INPUTS</span></span>

### <span data-ttu-id="55096-232">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="55096-232">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="55096-233">System. String</span><span class="sxs-lookup"><span data-stu-id="55096-233">System.String</span></span>

### <span data-ttu-id="55096-234">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="55096-234">System.Collections.Hashtable</span></span>

### <span data-ttu-id="55096-235">System. Int32</span><span class="sxs-lookup"><span data-stu-id="55096-235">System.Int32</span></span>

### <span data-ttu-id="55096-236">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. modeller. Yükseltmodu, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="55096-236">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.UpgradeMode, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="55096-237">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSetOSProfile</span><span class="sxs-lookup"><span data-stu-id="55096-237">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetOSProfile</span></span>

### <span data-ttu-id="55096-238">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSetStorageProfile</span><span class="sxs-lookup"><span data-stu-id="55096-238">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetStorageProfile</span></span>

### <span data-ttu-id="55096-239">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSetNetworkConfiguration []</span><span class="sxs-lookup"><span data-stu-id="55096-239">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetNetworkConfiguration[]</span></span>

### <span data-ttu-id="55096-240">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSetExtension []</span><span class="sxs-lookup"><span data-stu-id="55096-240">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetExtension[]</span></span>

### <span data-ttu-id="55096-241">System. String []</span><span class="sxs-lookup"><span data-stu-id="55096-241">System.String[]</span></span>

### <span data-ttu-id="55096-242">Microsoft. Azure. Management. COMPUTE. model. RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="55096-242">Microsoft.Azure.Management.Compute.Models.RollingUpgradePolicy</span></span>

### <span data-ttu-id="55096-243">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="55096-243">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="55096-244">Microsoft. Azure. Management. COMPUTE. modeller. BootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="55096-244">Microsoft.Azure.Management.Compute.Models.BootDiagnostics</span></span>

### <span data-ttu-id="55096-245">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. modeller. Kaynakıdentitytype, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="55096-245">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="55096-246">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="55096-246">OUTPUTS</span></span>

### <span data-ttu-id="55096-247">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="55096-247">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="55096-248">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="55096-248">NOTES</span></span>

## <span data-ttu-id="55096-249">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="55096-249">RELATED LINKS</span></span>

[<span data-ttu-id="55096-250">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="55096-250">Set-AzVmssOsProfile</span></span>](./Set-AzVmssOsProfile.md)

[<span data-ttu-id="55096-251">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="55096-251">Set-AzVmssStorageProfile</span></span>](./Set-AzVmssStorageProfile.md)

[<span data-ttu-id="55096-252">Add-Azvmssnetworkınterfaceconfiguration</span><span class="sxs-lookup"><span data-stu-id="55096-252">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="55096-253">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="55096-253">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="55096-254">Yeni-AzVmss</span><span class="sxs-lookup"><span data-stu-id="55096-254">New-AzVmss</span></span>](./New-AzVmss.md)
