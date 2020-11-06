---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: CE32F620-8DB2-4004-8012-F1C4AA235B60
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssConfig.md
ms.openlocfilehash: 4b87c121368232769672c24bc5005f3a50bfd39a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588975"
---
# <span data-ttu-id="97b02-101">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="97b02-101">New-AzureRmVmssConfig</span></span>

## <span data-ttu-id="97b02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97b02-102">SYNOPSIS</span></span>
<span data-ttu-id="97b02-103">Bir VMSS yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="97b02-103">Creates a VMSS configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97b02-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="97b02-104">SYNTAX</span></span>

```
New-AzureRmVmssConfig [[-Overprovision] <Boolean>] [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-SkuName] <String>] [[-SkuTier] <String>] [[-SkuCapacity] <Int64>] [[-UpgradePolicyMode] <UpgradeMode>]
 [[-OsProfile] <VirtualMachineScaleSetOSProfile>] [[-StorageProfile] <VirtualMachineScaleSetStorageProfile>]
 [[-NetworkInterfaceConfiguration] <VirtualMachineScaleSetNetworkConfiguration[]>]
 [[-Extension] <VirtualMachineScaleSetExtension[]>] [-SinglePlacementGroup <Boolean>] [-PlanName <String>]
 [-PlanPublisher <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-RecoveryPolicyMode <RecoveryMode>] [-BootDiagnostic <BootDiagnostics>] [-LicenseType <String>]
 [-IdentityType <ResourceIdentityType>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97b02-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="97b02-105">DESCRIPTION</span></span>
<span data-ttu-id="97b02-106">**Yeni-AzureRmVmssConfig** cmdlet 'i, yapılandırılabilir yerel sanal Manager ölçek KÜMESI (VMSS) nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="97b02-106">The **New-AzureRmVmssConfig** cmdlet creates a configurable local Virtual Manager Scale Set (VMSS) object.</span></span>
<span data-ttu-id="97b02-107">VMSS nesnesini yapılandırmak için diğer cmdlet 'ler gereklidir.</span><span class="sxs-lookup"><span data-stu-id="97b02-107">Other cmdlets are needed to configure the VMSS object.</span></span>
<span data-ttu-id="97b02-108">Bu cmdlet 'ler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="97b02-108">These cmdlets are:</span></span>

- <span data-ttu-id="97b02-109">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="97b02-109">Set-AzureRmVmssOsProfile</span></span>
- <span data-ttu-id="97b02-110">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="97b02-110">Set-AzureRmVmssStorageProfile</span></span>
- <span data-ttu-id="97b02-111">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="97b02-111">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>
- <span data-ttu-id="97b02-112">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="97b02-112">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="97b02-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="97b02-113">EXAMPLES</span></span>

### <span data-ttu-id="97b02-114">Örnek 1: bir VMSS yapılandırma nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="97b02-114">Example 1: Create a VMSS configuration object</span></span>
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

<span data-ttu-id="97b02-115">Bu örnek bir VMSS yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="97b02-115">This example creates a VMSS configuration object.</span></span>
<span data-ttu-id="97b02-116">İlk komut, bir VMSS yapılandırma nesnesi oluşturmak için **New-AzureRmVmssConfig** cmdlet 'ini kullanır ve sonucu $VMSS adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="97b02-116">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="97b02-117">İkinci komut, ilk komutta oluşturulan VMSS yapılandırma nesnesini kullanan bir VMSS oluşturmak için **New-AzureRmVmss** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="97b02-117">The second command uses the **New-AzureRmVmss** cmdlet to create a VMSS that uses the VMSS configuration object created in the first command.</span></span>

## <span data-ttu-id="97b02-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="97b02-118">PARAMETERS</span></span>

### <span data-ttu-id="97b02-119">-BootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="97b02-119">-BootDiagnostic</span></span>
<span data-ttu-id="97b02-120">Sanal makine ölçek kümesi önyükleme tanılaması profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="97b02-120">Specifies the virtual machine scale set boot diagnostics profile.</span></span>

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

### <span data-ttu-id="97b02-121">Uzantılı</span><span class="sxs-lookup"><span data-stu-id="97b02-121">-Extension</span></span>
<span data-ttu-id="97b02-122">VMSS için uzantı bilgileri nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="97b02-122">Specifies the extension information object for the VMSS.</span></span>
<span data-ttu-id="97b02-123">Bu nesneyi eklemek için **Add-Azurermvmssextenma** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="97b02-123">You can use the **Add-AzureRmVmssExtension** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="97b02-124">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="97b02-124">-IdentityType</span></span>
<span data-ttu-id="97b02-125">Yapılandırılmışsa, sanal makine ölçek kümesinin kimliğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="97b02-125">Specify the identity of the virtual machine scale set, if configured.</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97b02-126">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="97b02-126">-LicenseType</span></span>
<span data-ttu-id="97b02-127">Kendi lisans senaryonuzu verecek lisans türünü belirtin.</span><span class="sxs-lookup"><span data-stu-id="97b02-127">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="97b02-128">-Konum</span><span class="sxs-lookup"><span data-stu-id="97b02-128">-Location</span></span>
<span data-ttu-id="97b02-129">VMSS 'nin oluşturulduğu Azure konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="97b02-129">Specifies the Azure location where the VMSS is created.</span></span>

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

### <span data-ttu-id="97b02-130">-Networkınterfaceconfiguration</span><span class="sxs-lookup"><span data-stu-id="97b02-130">-NetworkInterfaceConfiguration</span></span>
<span data-ttu-id="97b02-131">VMSS yapılandırması için ağ özelliklerini içeren ağ profili nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="97b02-131">Specifies the network profile object that contains the networking properties for the VMSS configuration.</span></span>
<span data-ttu-id="97b02-132">Bu nesneyi eklemek için **Add-Azurermvmssnetworkınterfaceyapılandırma** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="97b02-132">You can use the **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet to add this object.</span></span>

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

### <span data-ttu-id="97b02-133">-OsProfile</span><span class="sxs-lookup"><span data-stu-id="97b02-133">-OsProfile</span></span>
<span data-ttu-id="97b02-134">VMSS yapılandırması işletim sistemi özelliklerini içeren işletim sistemi profili nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="97b02-134">Specifies the operating system profile object that contains the operating system properties for the VMSS configuration.</span></span>
<span data-ttu-id="97b02-135">Bu nesneyi ayarlamak için **set-AzureRmVmssOsProfile** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="97b02-135">You can use the **Set-AzureRmVmssOsProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="97b02-136">-Overprovision</span><span class="sxs-lookup"><span data-stu-id="97b02-136">-Overprovision</span></span>
<span data-ttu-id="97b02-137">Cmdlet 'in VMSS 'yi içerip içermediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="97b02-137">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="97b02-138">-PlanName</span><span class="sxs-lookup"><span data-stu-id="97b02-138">-PlanName</span></span>
<span data-ttu-id="97b02-139">Plan adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="97b02-139">Specifies the plan name.</span></span>

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

### <span data-ttu-id="97b02-140">-Planürün</span><span class="sxs-lookup"><span data-stu-id="97b02-140">-PlanProduct</span></span>
<span data-ttu-id="97b02-141">Plan ürünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="97b02-141">Specifies the plan product.</span></span>

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

### <span data-ttu-id="97b02-142">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="97b02-142">-PlanPromotionCode</span></span>
<span data-ttu-id="97b02-143">Plan promosyon kodunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="97b02-143">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="97b02-144">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="97b02-144">-PlanPublisher</span></span>
<span data-ttu-id="97b02-145">Publisher planı 'nı belirtir.</span><span class="sxs-lookup"><span data-stu-id="97b02-145">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="97b02-146">-RecoveryPolicyMode</span><span class="sxs-lookup"><span data-stu-id="97b02-146">-RecoveryPolicyMode</span></span>
<span data-ttu-id="97b02-147">Kurtarma ilkesini belirtin.</span><span class="sxs-lookup"><span data-stu-id="97b02-147">Specify the recovery policy.</span></span>

```yaml
Type: RecoveryMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97b02-148">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="97b02-148">-SinglePlacementGroup</span></span>
<span data-ttu-id="97b02-149">Tek yerleşim grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="97b02-149">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="97b02-150">-Skukapasitesi</span><span class="sxs-lookup"><span data-stu-id="97b02-150">-SkuCapacity</span></span>
<span data-ttu-id="97b02-151">VMSS 'deki örneklerin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="97b02-151">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97b02-152">-SkuName</span><span class="sxs-lookup"><span data-stu-id="97b02-152">-SkuName</span></span>
<span data-ttu-id="97b02-153">Tüm VMSS örneklerinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="97b02-153">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="97b02-154">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="97b02-154">-SkuTier</span></span>
<span data-ttu-id="97b02-155">VMSS 'nin katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="97b02-155">Specifies the tier of VMSS.</span></span>

<span data-ttu-id="97b02-156">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="97b02-156">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="97b02-157">Ardından</span><span class="sxs-lookup"><span data-stu-id="97b02-157">Standard</span></span>
- <span data-ttu-id="97b02-158">Ana</span><span class="sxs-lookup"><span data-stu-id="97b02-158">Basic</span></span>

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

### <span data-ttu-id="97b02-159">-StorageProfile</span><span class="sxs-lookup"><span data-stu-id="97b02-159">-StorageProfile</span></span>
<span data-ttu-id="97b02-160">VMSS yapılandırması için disk özelliklerini içeren depolama profili nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="97b02-160">Specifies the storage profile object that contains the disk properties for the VMSS configuration.</span></span>
<span data-ttu-id="97b02-161">Bu nesneyi ayarlamak için **set-AzureRmVmssStorageProfile** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="97b02-161">You can use the **Set-AzureRmVmssStorageProfile** cmdlet to set this object.</span></span>

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

### <span data-ttu-id="97b02-162">Etiketli</span><span class="sxs-lookup"><span data-stu-id="97b02-162">-Tag</span></span>
<span data-ttu-id="97b02-163">VMSS 'ye atanacak etiketleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="97b02-163">Specifies the tags that will be assigned to the VMSS.</span></span>

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

### <span data-ttu-id="97b02-164">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="97b02-164">-UpgradePolicyMode</span></span>
<span data-ttu-id="97b02-165">Belirtilen ölçek kümesindeki sanal makinelere yükseltme modu.</span><span class="sxs-lookup"><span data-stu-id="97b02-165">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>

<span data-ttu-id="97b02-166">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="97b02-166">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="97b02-167">Otomatik</span><span class="sxs-lookup"><span data-stu-id="97b02-167">Automatic</span></span>
- <span data-ttu-id="97b02-168">El ile</span><span class="sxs-lookup"><span data-stu-id="97b02-168">Manual</span></span>

```yaml
Type: UpgradeMode
Parameter Sets: (All)
Aliases: 
Accepted values: Automatic, Manual

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97b02-169">-Onay</span><span class="sxs-lookup"><span data-stu-id="97b02-169">-Confirm</span></span>
<span data-ttu-id="97b02-170">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="97b02-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97b02-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97b02-171">-WhatIf</span></span>
<span data-ttu-id="97b02-172">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="97b02-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="97b02-173">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="97b02-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97b02-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97b02-174">CommonParameters</span></span>
<span data-ttu-id="97b02-175">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="97b02-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97b02-176">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97b02-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97b02-177">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="97b02-177">INPUTS</span></span>

### <span data-ttu-id="97b02-178">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="97b02-178">None</span></span>
<span data-ttu-id="97b02-179">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="97b02-179">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="97b02-180">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="97b02-180">OUTPUTS</span></span>

### <span data-ttu-id="97b02-181">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="97b02-181">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="97b02-182">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="97b02-182">NOTES</span></span>

## <span data-ttu-id="97b02-183">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="97b02-183">RELATED LINKS</span></span>

[<span data-ttu-id="97b02-184">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="97b02-184">Set-AzureRmVmssOsProfile</span></span>](./Set-AzureRmVmssOsProfile.md)

[<span data-ttu-id="97b02-185">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="97b02-185">Set-AzureRmVmssStorageProfile</span></span>](./Set-AzureRmVmssStorageProfile.md)

[<span data-ttu-id="97b02-186">Add-Azurermvmssnetworkınterfaceconfiguration</span><span class="sxs-lookup"><span data-stu-id="97b02-186">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="97b02-187">Add-Azurermvmssextenma</span><span class="sxs-lookup"><span data-stu-id="97b02-187">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="97b02-188">Yeni-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="97b02-188">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)


