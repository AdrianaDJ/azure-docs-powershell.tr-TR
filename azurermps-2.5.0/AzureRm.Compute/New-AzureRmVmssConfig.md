---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmssconfig
schema: 2.0.0
ms.openlocfilehash: 4bc4782aaf235f81853a7304861a33ca53a75b45
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939781"
---
# <span data-ttu-id="db9c7-101">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="db9c7-101">New-AzureRmVmssConfig</span></span>

## <span data-ttu-id="db9c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db9c7-102">SYNOPSIS</span></span>
<span data-ttu-id="db9c7-103">Bir VMSS yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="db9c7-103">Creates a VMSS configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db9c7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="db9c7-104">SYNTAX</span></span>

### <span data-ttu-id="db9c7-105">DefaultParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="db9c7-105">DefaultParameterSet (Default)</span></span>
```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db9c7-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="db9c7-106">ExplicitIdentityParameterSet</span></span>
```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db9c7-107">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="db9c7-107">AssignIdentityParameterSet</span></span>
```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int32>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-Priority <String>] [-AssignIdentity]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db9c7-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="db9c7-108">DESCRIPTION</span></span>
<span data-ttu-id="db9c7-109">**Yeni-AzureRmVmssConfig** cmdlet 'i, yapılandırılabilir yerel sanal Manager ölçek KÜMESI (VMSS) nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="db9c7-109">The **New-AzureRmVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span> <span data-ttu-id="db9c7-110">VMSS nesnesini yapılandırmak için diğer cmdlet 'ler gereklidir.</span><span class="sxs-lookup"><span data-stu-id="db9c7-110">Other cmdlets are needed to configure the VMSS object.</span></span> <span data-ttu-id="db9c7-111">Bu cmdlet 'ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="db9c7-111">These cmdlets are:</span></span>

- <span data-ttu-id="db9c7-112">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="db9c7-112">Set-AzureRmVmssOsProfile</span></span>
- <span data-ttu-id="db9c7-113">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="db9c7-113">Set-AzureRmVmssStorageProfile</span></span>
- <span data-ttu-id="db9c7-114">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="db9c7-114">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="db9c7-115">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="db9c7-115">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="db9c7-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="db9c7-116">EXAMPLES</span></span>

### <span data-ttu-id="db9c7-117">Örnek 1: bir VMSS yapılandırma nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="db9c7-117">Example 1: Create a VMSS configuration object</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic" -NetworkInterfaceConfiguration $NetCfg `
            | Add-AzureRmVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
            | Set-AzureRmVmssOSProfile -ComputerNamePrefix "Test" -AdminUsername $adminUsername -AdminPassword $AdminPassword `
            | Set-AzureRmVmssStorageProfile -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VHDContainer `
            | Add-AzureRmVmssAdditionalUnattendContent -ComponentName  $AUCComponentName -Content  $AUCContent -PassName  $AUCPassName -SettingName  $AUCSetting `
            | Remove-AzureRmVmssAdditionalUnattendContent -ComponentName  $AUCComponentName;

New-AzureRmVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

<span data-ttu-id="db9c7-118">Bu örnek bir VMSS yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="db9c7-118">This example creates a VMSS configuration object.</span></span> <span data-ttu-id="db9c7-119">İlk komut, bir VMSS yapılandırma nesnesi oluşturmak için **New-AzureRmVmssConfig** cmdlet 'ini kullanır ve sonucu $VMSS adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="db9c7-119">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span> <span data-ttu-id="db9c7-120">İkinci komut, ilk komutta oluşturulan VMSS yapılandırma nesnesini kullanan bir VMSS oluşturmak için **New-AzureRmVmss** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="db9c7-120">The second command uses the **New-AzureRmVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="db9c7-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="db9c7-121">PARAMETERS</span></span>

### <span data-ttu-id="db9c7-122">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="db9c7-122">-AssignIdentity</span></span>
<span data-ttu-id="db9c7-123">Sanal makine ölçek kümesi için sistem tarafından atanan kimliği belirtin.</span><span class="sxs-lookup"><span data-stu-id="db9c7-123">Specify the system assigned identity for the virtual machine scale set.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db9c7-124">-Autoosupgrad</span><span class="sxs-lookup"><span data-stu-id="db9c7-124">-AutoOSUpgrade</span></span>
<span data-ttu-id="db9c7-125">Resmin daha yeni bir sürümü kullanılabilir hale geldiğinde, bir yerde ölçeklendirme kümesi örneklerine otomatik olarak işletim sistemi yükseltmeleri uygulanıp uygulanmayacağı.</span><span class="sxs-lookup"><span data-stu-id="db9c7-125">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db9c7-126">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="db9c7-126">-BootDiagnostic</span></span>
<span data-ttu-id="db9c7-127">Sanal makine ölçek kümesi önyükleme tanılaması profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="db9c7-127">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

```yaml
Type: BootDiagnostics
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db9c7-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db9c7-128">-DefaultProfile</span></span>
<span data-ttu-id="db9c7-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="db9c7-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db9c7-130">Uzantılı</span><span class="sxs-lookup"><span data-stu-id="db9c7-130">-Extension</span></span>
<span data-ttu-id="db9c7-131">VMSS için uzantı bilgileri nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="db9c7-131">Specifies the extension information object for the VMSS.</span></span> <span data-ttu-id="db9c7-132">Bu nesneyi eklemek için **Add-Azurermvmssextenma** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="db9c7-132">You can use the **Add-AzureRmVmssExtension** cmdlet to add this object.</span></span>

```yaml
Type: VirtualMachineScaleSetExtension[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db9c7-133">-Healthprobeıd</span><span class="sxs-lookup"><span data-stu-id="db9c7-133">-HealthProbeId</span></span>
<span data-ttu-id="db9c7-134">Sanal makine ölçeği kümesindeki bir örneğin durumunu belirlemek için kullanılan yük dengeleyici araştırması KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="db9c7-134">Specifies the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span>
<span data-ttu-id="db9c7-135">Healthprobeıd, '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName} ' biçiminde.</span><span class="sxs-lookup"><span data-stu-id="db9c7-135">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db9c7-136">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="db9c7-136">-IdentityId</span></span>
<span data-ttu-id="db9c7-137">Sanal makine ölçek kümesiyle ilişkili kullanıcı kimliklerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="db9c7-137">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="db9c7-138">Kullanıcı kimliği başvuruları formda ARM kaynak kimlikleri olacaktır: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="db9c7-138">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db9c7-139">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="db9c7-139">-IdentityType</span></span>
<span data-ttu-id="db9c7-140">Sanal makine ölçek kümesi için kullanılan kimlik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="db9c7-140">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="db9c7-141">' Systemassigneduserın ' türü, örtülü olarak oluşturulmuş bir kimlik ve Kullanıcı tarafından atanan kimlikler kümesini içerir.</span><span class="sxs-lookup"><span data-stu-id="db9c7-141">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="db9c7-142">' None ' türü, sanal makine ölçek kümesindeki tüm kimlikleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="db9c7-142">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="db9c7-143">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="db9c7-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="db9c7-144">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="db9c7-144">SystemAssigned</span></span>
- <span data-ttu-id="db9c7-145">Kullanıcı tarafından atanmış</span><span class="sxs-lookup"><span data-stu-id="db9c7-145">UserAssigned</span></span>
- <span data-ttu-id="db9c7-146">Systemassigneduseratandı</span><span class="sxs-lookup"><span data-stu-id="db9c7-146">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="db9c7-147">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="db9c7-147">None</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db9c7-148">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="db9c7-148">-LicenseType</span></span>
<span data-ttu-id="db9c7-149">Kendi lisans senaryonuzu verecek lisans türünü belirtin.</span><span class="sxs-lookup"><span data-stu-id="db9c7-149">Specify the license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db9c7-150">-Konum</span><span class="sxs-lookup"><span data-stu-id="db9c7-150">-Location</span></span>
<span data-ttu-id="db9c7-151">VMSS 'nin oluşturulduğu Azure konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="db9c7-151">Specifies the Azure location where the VMSS is created.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db9c7-152">-Networkınterfaceconfiguration</span><span class="sxs-lookup"><span data-stu-id="db9c7-152">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="db9c7-153">VMSS yapılandırması için ağ özelliklerini içeren ağ profili nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="db9c7-153">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="db9c7-154">Bu nesneyi eklemek için **Add-Azurermvmssnetworkınterfaceyapılandırma** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="db9c7-154">You can use the **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

```yaml
Type: VirtualMachineScaleSetNetworkConfiguration[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db9c7-155">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="db9c7-155">-OsProfile</span></span>
<span data-ttu-id="db9c7-156">VMSS yapılandırması işletim sistemi özelliklerini içeren işletim sistemi profili nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="db9c7-156">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="db9c7-157">Bu nesneyi ayarlamak için **set-AzureRmVmssOsProfile** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="db9c7-157">You can use the **Set-AzureRmVmssOsProfile** cmdlet to set this object.</span></span>

```yaml
Type: VirtualMachineScaleSetOSProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db9c7-158">-Overprovision</span><span class="sxs-lookup"><span data-stu-id="db9c7-158">-Overprovision</span></span>
<span data-ttu-id="db9c7-159">Cmdlet 'in VMSS 'yi içerip içermediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="db9c7-159">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db9c7-160">-PlanName</span><span class="sxs-lookup"><span data-stu-id="db9c7-160">-PlanName</span></span>
<span data-ttu-id="db9c7-161">Plan adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="db9c7-161">Specifies the plan name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db9c7-162">-Planürün</span><span class="sxs-lookup"><span data-stu-id="db9c7-162">-PlanProduct</span></span>
<span data-ttu-id="db9c7-163">Plan ürünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="db9c7-163">Specifies the plan product.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db9c7-164">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="db9c7-164">-PlanPromotionCode</span></span>
<span data-ttu-id="db9c7-165">Plan promosyon kodunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="db9c7-165">Specifies the plan promotion code.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db9c7-166">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="db9c7-166">-PlanPublisher</span></span>
<span data-ttu-id="db9c7-167">Publisher planı 'nı belirtir.</span><span class="sxs-lookup"><span data-stu-id="db9c7-167">Specifies the plan publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db9c7-168">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="db9c7-168">-Priority</span></span>
<span data-ttu-id="db9c7-169">Ölçek kümesindeki sanal makinelerin önceliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="db9c7-169">Specifies the priority for the virtual machines in the scale set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db9c7-170">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="db9c7-170">-RollingUpgradePolicy</span></span>
<span data-ttu-id="db9c7-171">Çalışırken yükseltme ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="db9c7-171">Specifies the rolling upgrade policy.</span></span>

```yaml
Type: RollingUpgradePolicy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db9c7-172">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="db9c7-172">-SinglePlacementGroup</span></span>
<span data-ttu-id="db9c7-173">Tek yerleşim grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="db9c7-173">Specifies the single placement group.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db9c7-174">-Skukapasitesi</span><span class="sxs-lookup"><span data-stu-id="db9c7-174">-SkuCapacity</span></span>
<span data-ttu-id="db9c7-175">VMSS 'deki örneklerin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="db9c7-175">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db9c7-176">-SkuName</span><span class="sxs-lookup"><span data-stu-id="db9c7-176">-SkuName</span></span>
<span data-ttu-id="db9c7-177">Tüm VMSS örneklerinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="db9c7-177">Specifies the size of all the instances of VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db9c7-178">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="db9c7-178">-SkuTier</span></span>
<span data-ttu-id="db9c7-179">VMSS 'nin katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="db9c7-179">Specifies the tier of VMSS.</span></span> <span data-ttu-id="db9c7-180">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="db9c7-180">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="db9c7-181">Ardından</span><span class="sxs-lookup"><span data-stu-id="db9c7-181">Standard</span></span>
- <span data-ttu-id="db9c7-182">Ana</span><span class="sxs-lookup"><span data-stu-id="db9c7-182">Basic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db9c7-183">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="db9c7-183">-StorageProfile</span></span>
<span data-ttu-id="db9c7-184">VMSS yapılandırması için disk özelliklerini içeren depolama profili nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="db9c7-184">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="db9c7-185">Bu nesneyi ayarlamak için **set-AzureRmVmssStorageProfile** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="db9c7-185">You can use the **Set-AzureRmVmssStorageProfile** cmdlet to set this object.</span></span>

```yaml
Type: VirtualMachineScaleSetStorageProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db9c7-186">Etiketli</span><span class="sxs-lookup"><span data-stu-id="db9c7-186">-Tag</span></span>
<span data-ttu-id="db9c7-187">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="db9c7-187">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="db9c7-188">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="db9c7-188">For example:</span></span>

<span data-ttu-id="db9c7-189">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="db9c7-189">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db9c7-190">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="db9c7-190">-UpgradePolicyMode</span></span>
<span data-ttu-id="db9c7-191">Belirtilen ölçek kümesindeki sanal makinelere yükseltme modu.</span><span class="sxs-lookup"><span data-stu-id="db9c7-191">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>

<span data-ttu-id="db9c7-192">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="db9c7-192">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="db9c7-193">Otomatik</span><span class="sxs-lookup"><span data-stu-id="db9c7-193">Automatic</span></span>
- <span data-ttu-id="db9c7-194">El ile</span><span class="sxs-lookup"><span data-stu-id="db9c7-194">Manual</span></span>

```yaml
Type: UpgradeMode
Parameter Sets: (All)
Aliases: 
Accepted values: Automatic, Manual, Rolling

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db9c7-195">-Bölge</span><span class="sxs-lookup"><span data-stu-id="db9c7-195">-Zone</span></span>
<span data-ttu-id="db9c7-196">Sanal makine ölçek kümesi için bölge listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="db9c7-196">Specifies the zone list for the virtual machine scale set.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db9c7-197">-Onay</span><span class="sxs-lookup"><span data-stu-id="db9c7-197">-Confirm</span></span>
<span data-ttu-id="db9c7-198">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="db9c7-198">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db9c7-199">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db9c7-199">-WhatIf</span></span>
<span data-ttu-id="db9c7-200">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="db9c7-200">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="db9c7-201">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="db9c7-201">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db9c7-202">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db9c7-202">CommonParameters</span></span>
<span data-ttu-id="db9c7-203">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="db9c7-203">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db9c7-204">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db9c7-204">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db9c7-205">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="db9c7-205">INPUTS</span></span>

### <span data-ttu-id="db9c7-206">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="db9c7-206">None</span></span>
<span data-ttu-id="db9c7-207">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="db9c7-207">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="db9c7-208">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="db9c7-208">OUTPUTS</span></span>

### <span data-ttu-id="db9c7-209">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="db9c7-209">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="db9c7-210">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="db9c7-210">NOTES</span></span>

## <span data-ttu-id="db9c7-211">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="db9c7-211">RELATED LINKS</span></span>

[<span data-ttu-id="db9c7-212">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="db9c7-212">Set-AzureRmVmssOsProfile</span></span>](./Set-AzureRmVmssOsProfile.md)

[<span data-ttu-id="db9c7-213">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="db9c7-213">Set-AzureRmVmssStorageProfile</span></span>](./Set-AzureRmVmssStorageProfile.md)

[<span data-ttu-id="db9c7-214">Add-Azurermvmssnetworkınterfaceconfiguration</span><span class="sxs-lookup"><span data-stu-id="db9c7-214">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="db9c7-215">Add-Azurermvmssextenma</span><span class="sxs-lookup"><span data-stu-id="db9c7-215">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="db9c7-216">Yeni-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="db9c7-216">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)
