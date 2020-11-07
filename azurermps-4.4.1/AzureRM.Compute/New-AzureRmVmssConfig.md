---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssConfig.md
ms.openlocfilehash: 3229f1e09cca1b32b62e5b7233806b20ed8ed78e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764572"
---
# <span data-ttu-id="d1e9f-101">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="d1e9f-101">New-AzureRmVmssConfig</span></span>

## <span data-ttu-id="d1e9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1e9f-102">SYNOPSIS</span></span>
<span data-ttu-id="d1e9f-103">Bir VMSS yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-103">Creates a VMSS configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1e9f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d1e9f-104">SYNTAX</span></span>

```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int64>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-Zone <String[]>]
 [-PlanName <String>] [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RollingUpgradePolicy <RollingUpgradePolicy>] [-AutoOSUpgrade] [-HealthProbeId <String>]
 [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>] [-AssignIdentity]
 [-IdentityType <ResourceIdentityType>] [-RecoveryPolicyMode <RecoveryMode>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1e9f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d1e9f-105">DESCRIPTION</span></span>
<span data-ttu-id="d1e9f-106">**Yeni-AzureRmVmssConfig** cmdlet 'i, yapılandırılabilir yerel sanal Manager ölçek KÜMESI (VMSS) nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-106">The **New-AzureRmVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span>
<span data-ttu-id="d1e9f-107">VMSS nesnesini yapılandırmak için diğer cmdlet 'ler gereklidir.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-107">Other cmdlets are needed to configure the VMSS object.</span></span>
<span data-ttu-id="d1e9f-108">Bu cmdlet 'ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="d1e9f-108">These cmdlets are:</span></span>

- <span data-ttu-id="d1e9f-109">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="d1e9f-109">Set-AzureRmVmssOsProfile</span></span>
- <span data-ttu-id="d1e9f-110">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="d1e9f-110">Set-AzureRmVmssStorageProfile</span></span>
- <span data-ttu-id="d1e9f-111">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="d1e9f-111">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="d1e9f-112">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="d1e9f-112">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="d1e9f-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d1e9f-113">EXAMPLES</span></span>

### <span data-ttu-id="d1e9f-114">Örnek 1: bir VMSS yapılandırma nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="d1e9f-114">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="d1e9f-115">Bu örnek bir VMSS yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-115">This example creates a VMSS configuration object.</span></span>
<span data-ttu-id="d1e9f-116">İlk komut, bir VMSS yapılandırma nesnesi oluşturmak için **New-AzureRmVmssConfig** cmdlet 'ini kullanır ve sonucu $VMSS adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-116">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="d1e9f-117">İkinci komut, ilk komutta oluşturulan VMSS yapılandırma nesnesini kullanan bir VMSS oluşturmak için **New-AzureRmVmss** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-117">The second command uses the **New-AzureRmVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="d1e9f-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d1e9f-118">PARAMETERS</span></span>

### <span data-ttu-id="d1e9f-119">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="d1e9f-119">-AssignIdentity</span></span>
<span data-ttu-id="d1e9f-120">Sanal makine ölçek kümesi için sistem tarafından atanan kimliği belirtin.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-120">Specify the system assigned identity for the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1e9f-121">-Autoosupgrad</span><span class="sxs-lookup"><span data-stu-id="d1e9f-121">-AutoOSUpgrade</span></span>
<span data-ttu-id="d1e9f-122">Resmin daha yeni bir sürümü kullanılabilir hale geldiğinde, bir yerde ölçeklendirme kümesi örneklerine otomatik olarak işletim sistemi yükseltmeleri uygulanıp uygulanmayacağı.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-122">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1e9f-123">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d1e9f-123">-BootDiagnostic</span></span>
<span data-ttu-id="d1e9f-124">Sanal makine ölçek kümesi önyükleme tanılaması profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-124">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="d1e9f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1e9f-125">-DefaultProfile</span></span>
<span data-ttu-id="d1e9f-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1e9f-127">Uzantılı</span><span class="sxs-lookup"><span data-stu-id="d1e9f-127">-Extension</span></span>
<span data-ttu-id="d1e9f-128">VMSS için uzantı bilgileri nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-128">Specifies the extension information object for the VMSS.</span></span>
<span data-ttu-id="d1e9f-129">Bu nesneyi eklemek için **Add-Azurermvmssextenma** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-129">You can use the **Add-AzureRmVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="d1e9f-130">-Healthprobeıd</span><span class="sxs-lookup"><span data-stu-id="d1e9f-130">-HealthProbeId</span></span>
<span data-ttu-id="d1e9f-131">Sanal makine ölçeği kümesindeki bir örneğin durumunu belirlemek için kullanılan yük dengeleyici araştırması KIMLIĞINI belirtin.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-131">Specify the ID of a load balancer probe used to determine the health of an instance in the virtual machine scale set.</span></span> <span data-ttu-id="d1e9f-132">Healthprobeıd, '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName} ' biçiminde.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-132">HealthProbeId is in the form of '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/loadBalancers/{loadBalancerName}/probes/{probeName}'.</span></span>

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

### <span data-ttu-id="d1e9f-133">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="d1e9f-133">-IdentityType</span></span>
<span data-ttu-id="d1e9f-134">Yapılandırılmışsa, sanal makine ölçek kümesinin kimliğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-134">Specify the identity of the virtual machine scale set, if configured.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: (All)
Aliases: 
Accepted values: SystemAssigned

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1e9f-135">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="d1e9f-135">-LicenseType</span></span>
<span data-ttu-id="d1e9f-136">Kendi lisans senaryonuzu verecek lisans türünü belirtin.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-136">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="d1e9f-137">-Konum</span><span class="sxs-lookup"><span data-stu-id="d1e9f-137">-Location</span></span>
<span data-ttu-id="d1e9f-138">VMSS 'nin oluşturulduğu Azure konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-138">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="d1e9f-139">-Networkınterfaceconfiguration</span><span class="sxs-lookup"><span data-stu-id="d1e9f-139">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="d1e9f-140">VMSS yapılandırması için ağ özelliklerini içeren ağ profili nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-140">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="d1e9f-141">Bu nesneyi eklemek için **Add-Azurermvmssnetworkınterfaceyapılandırma** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-141">You can use the **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="d1e9f-142">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="d1e9f-142">-OsProfile</span></span>
<span data-ttu-id="d1e9f-143">VMSS yapılandırması işletim sistemi özelliklerini içeren işletim sistemi profili nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-143">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="d1e9f-144">Bu nesneyi ayarlamak için **set-AzureRmVmssOsProfile** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-144">You can use the **Set-AzureRmVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="d1e9f-145">-Overprovision</span><span class="sxs-lookup"><span data-stu-id="d1e9f-145">-Overprovision</span></span>
<span data-ttu-id="d1e9f-146">Cmdlet 'in VMSS 'yi içerip içermediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-146">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="d1e9f-147">-PlanName</span><span class="sxs-lookup"><span data-stu-id="d1e9f-147">-PlanName</span></span>
<span data-ttu-id="d1e9f-148">Plan adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-148">Specifies the plan name.</span></span>

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

### <span data-ttu-id="d1e9f-149">-Planürün</span><span class="sxs-lookup"><span data-stu-id="d1e9f-149">-PlanProduct</span></span>
<span data-ttu-id="d1e9f-150">Plan ürünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-150">Specifies the plan product.</span></span>

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

### <span data-ttu-id="d1e9f-151">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="d1e9f-151">-PlanPromotionCode</span></span>
<span data-ttu-id="d1e9f-152">Plan promosyon kodunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-152">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="d1e9f-153">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="d1e9f-153">-PlanPublisher</span></span>
<span data-ttu-id="d1e9f-154">Publisher planı 'nı belirtir.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-154">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="d1e9f-155">-RecoveryPolicyMode</span><span class="sxs-lookup"><span data-stu-id="d1e9f-155">-RecoveryPolicyMode</span></span>
<span data-ttu-id="d1e9f-156">Kurtarma ilkesini belirtin.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-156">Specify the recovery policy.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Compute.Automation.RecoveryMode]
Parameter Sets: (All)
Aliases: 
Accepted values: None, OverProvision, Reprovision

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1e9f-157">-RollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="d1e9f-157">-RollingUpgradePolicy</span></span>
<span data-ttu-id="d1e9f-158">Çalışırken yükseltme ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-158">Specifies the rolling upgrade policy.</span></span>

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

### <span data-ttu-id="d1e9f-159">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="d1e9f-159">-SinglePlacementGroup</span></span>
<span data-ttu-id="d1e9f-160">Tek yerleşim grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-160">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="d1e9f-161">-Skukapasitesi</span><span class="sxs-lookup"><span data-stu-id="d1e9f-161">-SkuCapacity</span></span>
<span data-ttu-id="d1e9f-162">VMSS 'deki örneklerin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-162">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1e9f-163">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d1e9f-163">-SkuName</span></span>
<span data-ttu-id="d1e9f-164">Tüm VMSS örneklerinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-164">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="d1e9f-165">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="d1e9f-165">-SkuTier</span></span>
<span data-ttu-id="d1e9f-166">VMSS 'nin katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-166">Specifies the tier of VMSS.</span></span>

<span data-ttu-id="d1e9f-167">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="d1e9f-167">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d1e9f-168">Ardından</span><span class="sxs-lookup"><span data-stu-id="d1e9f-168">Standard</span></span>
- <span data-ttu-id="d1e9f-169">Ana</span><span class="sxs-lookup"><span data-stu-id="d1e9f-169">Basic</span></span>

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

### <span data-ttu-id="d1e9f-170">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="d1e9f-170">-StorageProfile</span></span>
<span data-ttu-id="d1e9f-171">VMSS yapılandırması için disk özelliklerini içeren depolama profili nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-171">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="d1e9f-172">Bu nesneyi ayarlamak için **set-AzureRmVmssStorageProfile** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-172">You can use the **Set-AzureRmVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="d1e9f-173">Etiketli</span><span class="sxs-lookup"><span data-stu-id="d1e9f-173">-Tag</span></span>
<span data-ttu-id="d1e9f-174">VMSS 'ye atanacak etiketleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-174">Specifies the tags that will be assigned to the VMSS.</span></span>

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

### <span data-ttu-id="d1e9f-175">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="d1e9f-175">-UpgradePolicyMode</span></span>
<span data-ttu-id="d1e9f-176">Belirtilen ölçek kümesindeki sanal makinelere yükseltme modu.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-176">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>

<span data-ttu-id="d1e9f-177">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="d1e9f-177">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d1e9f-178">Otomatik</span><span class="sxs-lookup"><span data-stu-id="d1e9f-178">Automatic</span></span>
- <span data-ttu-id="d1e9f-179">El ile</span><span class="sxs-lookup"><span data-stu-id="d1e9f-179">Manual</span></span>

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

### <span data-ttu-id="d1e9f-180">-Bölge</span><span class="sxs-lookup"><span data-stu-id="d1e9f-180">-Zone</span></span>
<span data-ttu-id="d1e9f-181">Sanal makine ölçek kümesi için bölge listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-181">Specifies the zone list for the virtual machine scale set.</span></span>

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

### <span data-ttu-id="d1e9f-182">-Onay</span><span class="sxs-lookup"><span data-stu-id="d1e9f-182">-Confirm</span></span>
<span data-ttu-id="d1e9f-183">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1e9f-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1e9f-184">-WhatIf</span></span>
<span data-ttu-id="d1e9f-185">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-185">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d1e9f-186">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1e9f-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1e9f-187">CommonParameters</span></span>
<span data-ttu-id="d1e9f-188">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1e9f-189">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1e9f-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1e9f-190">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d1e9f-190">INPUTS</span></span>

## <span data-ttu-id="d1e9f-191">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d1e9f-191">OUTPUTS</span></span>

### <span data-ttu-id="d1e9f-192">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="d1e9f-192">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="d1e9f-193">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d1e9f-193">NOTES</span></span>

## <span data-ttu-id="d1e9f-194">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d1e9f-194">RELATED LINKS</span></span>

[<span data-ttu-id="d1e9f-195">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="d1e9f-195">Set-AzureRmVmssOsProfile</span></span>](./Set-AzureRmVmssOsProfile.md)

[<span data-ttu-id="d1e9f-196">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="d1e9f-196">Set-AzureRmVmssStorageProfile</span></span>](./Set-AzureRmVmssStorageProfile.md)

[<span data-ttu-id="d1e9f-197">Add-Azurermvmssnetworkınterfaceconfiguration</span><span class="sxs-lookup"><span data-stu-id="d1e9f-197">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="d1e9f-198">Add-Azurermvmssextenma</span><span class="sxs-lookup"><span data-stu-id="d1e9f-198">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="d1e9f-199">Yeni-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="d1e9f-199">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)


