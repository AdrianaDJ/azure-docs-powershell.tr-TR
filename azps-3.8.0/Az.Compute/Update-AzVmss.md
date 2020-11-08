---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: bf8fa8c4b7d1d08cdb6d0c2c348f5c97a2788a4e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104587"
---
# <span data-ttu-id="e537b-101">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e537b-101">Update-AzVmss</span></span>

## <span data-ttu-id="e537b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e537b-102">SYNOPSIS</span></span>
<span data-ttu-id="e537b-103">Bir VMSUBNET 'in durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e537b-103">Updates the state of a VMSS.</span></span>

## <span data-ttu-id="e537b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e537b-104">SYNTAX</span></span>

### <span data-ttu-id="e537b-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e537b-105">DefaultParameter (Default)</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-AutomaticRepairMaxInstanceRepairsPercent <Int32>]
 [-BootDiagnosticsEnabled <Boolean>] [-BootDiagnosticsStorageUri <String>] [-CustomData <String>]
 [-DisableAutoRollback <Boolean>] [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
 [-EnableAutomaticUpdate <Boolean>] [-ImageReferenceId <String>] [-ImageReferenceOffer <String>]
 [-ImageReferencePublisher <String>] [-ImageReferenceSku <String>] [-ImageReferenceVersion <String>]
 [-ImageUri <String>] [-LicenseType <String>] [-ManagedDiskStorageAccountType <String>]
 [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>] [-MaxUnhealthyInstancePercent <Int32>]
 [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-OsDiskCaching <CachingTypes>]
 [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>] [-PauseTimeBetweenBatches <String>]
 [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>] [-PlanPublisher <String>]
 [-ProvisionVMAgent <Boolean>] [-ProximityPlacementGroupId <String>] [-ScaleInPolicy <String[]>]
 [-SinglePlacementGroup <Boolean>] [-SkipExtensionsOnOverprovisionedVMs <Boolean>] [-SkuCapacity <Int32>]
 [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e537b-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="e537b-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-AutomaticRepairMaxInstanceRepairsPercent <Int32>]
 [-BootDiagnosticsEnabled <Boolean>] [-BootDiagnosticsStorageUri <String>] [-CustomData <String>]
 [-DisableAutoRollback <Boolean>] [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
 [-EnableAutomaticUpdate <Boolean>] [-IdentityId <String[]>] -IdentityType <ResourceIdentityType>
 [-ImageReferenceId <String>] [-ImageReferenceOffer <String>] [-ImageReferencePublisher <String>]
 [-ImageReferenceSku <String>] [-ImageReferenceVersion <String>] [-ImageUri <String>] [-LicenseType <String>]
 [-ManagedDiskStorageAccountType <String>] [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>]
 [-MaxUnhealthyInstancePercent <Int32>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-OsDiskCaching <CachingTypes>] [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>]
 [-PauseTimeBetweenBatches <String>] [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] [-SinglePlacementGroup <Boolean>] [-SkipExtensionsOnOverprovisionedVMs <Boolean>]
 [-SkuCapacity <Int32>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e537b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e537b-107">DESCRIPTION</span></span>
<span data-ttu-id="e537b-108">**Update-AzVmss** cmdlet 'ı sanal makine ölçek kümesi 'nın (VMSS) durumunu yerel BIR VMSS nesnesinin durumuna güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e537b-108">The **Update-AzVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="e537b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e537b-109">EXAMPLES</span></span>

### <span data-ttu-id="e537b-110">Örnek 1: bir VMSS durumunu yerel bir VMSS nesnesinin durumuna güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="e537b-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="e537b-111">Bu komut, Group001 adındaki kaynak grubuna ait olan VMSS001 adındaki VMSS 'nin durumunu yerel bir VMSS nesnesinin durumuna güncelleştirir $LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="e537b-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="e537b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e537b-112">PARAMETERS</span></span>

### <span data-ttu-id="e537b-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="e537b-113">-AsJob</span></span>
<span data-ttu-id="e537b-114">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="e537b-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="e537b-115">-Automaticosupgrad</span><span class="sxs-lookup"><span data-stu-id="e537b-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="e537b-116">Resmin daha yeni bir sürümü kullanılabilir hale geldiğinde, bir yerde ölçeklendirme kümesi örneklerine otomatik olarak işletim sistemi yükseltmeleri uygulanıp uygulanmayacağı.</span><span class="sxs-lookup"><span data-stu-id="e537b-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="e537b-117">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="e537b-117">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="e537b-118">VM 'deki durum değişikliği nedeniyle otomatik onarımların askıya alındığı süre.</span><span class="sxs-lookup"><span data-stu-id="e537b-118">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="e537b-119">Kullanım süresi, durum değişikliği tamamlandıktan sonra başlar.</span><span class="sxs-lookup"><span data-stu-id="e537b-119">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="e537b-120">Bu, erken veya kazayla onarılmasını önlemeye yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="e537b-120">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="e537b-121">Süre ISO 8601 biçiminde belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="e537b-121">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="e537b-122">Varsayılan değer 5 dakikadır (PT5M).</span><span class="sxs-lookup"><span data-stu-id="e537b-122">The default value is 5 minutes (PT5M).</span></span>

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

### <span data-ttu-id="e537b-123">-AutomaticRepairMaxInstanceRepairsPercent</span><span class="sxs-lookup"><span data-stu-id="e537b-123">-AutomaticRepairMaxInstanceRepairsPercent</span></span>
<span data-ttu-id="e537b-124">Aynı anda onarılacak sanal makinelerin yüzdesi (ölçek kümesi kapasitesi).</span><span class="sxs-lookup"><span data-stu-id="e537b-124">The percentage (capacity of scaleset) of virtual machines that will be simultaneously repaired.</span></span> <span data-ttu-id="e537b-125">Varsayılan değer %20 ' dir.</span><span class="sxs-lookup"><span data-stu-id="e537b-125">The default value is 20%.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e537b-126">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="e537b-126">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="e537b-127">Sanal makine ölçek kümesinde önyükleme tanılaması 'nın etkinleştirilmesi gerekip gerekmediği.</span><span class="sxs-lookup"><span data-stu-id="e537b-127">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="e537b-128">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="e537b-128">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="e537b-129">Konsol çıkışını ve ekran görüntüsünü yerleştirmek için kullanılacak depolama hesabının URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="e537b-129">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="e537b-130">-CustomData</span><span class="sxs-lookup"><span data-stu-id="e537b-130">-CustomData</span></span>
<span data-ttu-id="e537b-131">Özel verilerin Base-64 kodlu dizesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e537b-131">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="e537b-132">Bu, sanal makinede dosya olarak kaydedilmiş bir ikili diziye çözülür.</span><span class="sxs-lookup"><span data-stu-id="e537b-132">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="e537b-133">İkili dizinin en fazla uzunluğu 65535 bayttır.</span><span class="sxs-lookup"><span data-stu-id="e537b-133">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="e537b-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e537b-134">-DefaultProfile</span></span>
<span data-ttu-id="e537b-135">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e537b-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e537b-136">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="e537b-136">-DisableAutoRollback</span></span>
<span data-ttu-id="e537b-137">Otomatik OS yükseltme Ilkesi için otomatik geri almayı devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="e537b-137">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="e537b-138">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="e537b-138">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="e537b-139">Bu cmdlet 'in Linux OS için parola kimlik doğrulamasını devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e537b-139">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

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

### <span data-ttu-id="e537b-140">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="e537b-140">-EnableAutomaticRepair</span></span>
<span data-ttu-id="e537b-141">Sanal makine ölçek kümesinde otomatik onarımları etkinleştirme veya devre dışı bırakma.</span><span class="sxs-lookup"><span data-stu-id="e537b-141">Enable or disable automatic repairs on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="e537b-142">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="e537b-142">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="e537b-143">VMSS 'deki Windows sanal makinelerinin otomatik güncelleştirmeler için etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e537b-143">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="e537b-144">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="e537b-144">-IdentityId</span></span>
<span data-ttu-id="e537b-145">Sanal makine ölçek kümesiyle ilişkili kullanıcı kimliklerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e537b-145">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="e537b-146">Kullanıcı kimliği başvuruları formda ARM kaynak kimlikleri olacaktır: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="e537b-146">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e537b-147">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="e537b-147">-IdentityType</span></span>
<span data-ttu-id="e537b-148">Sanal makine ölçek kümesi için kullanılan kimlik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e537b-148">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="e537b-149">' Systemassigneduserın ' türü, örtülü olarak oluşturulmuş bir kimlik ve Kullanıcı tarafından atanan kimlikler kümesini içerir.</span><span class="sxs-lookup"><span data-stu-id="e537b-149">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="e537b-150">' None ' türü, sanal makine ölçek kümesindeki tüm kimlikleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e537b-150">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="e537b-151">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="e537b-151">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e537b-152">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="e537b-152">SystemAssigned</span></span>
- <span data-ttu-id="e537b-153">Kullanıcı tarafından atanmış</span><span class="sxs-lookup"><span data-stu-id="e537b-153">UserAssigned</span></span>
- <span data-ttu-id="e537b-154">Systemassigneduseratandı</span><span class="sxs-lookup"><span data-stu-id="e537b-154">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="e537b-155">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e537b-155">None</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e537b-156">-Imagereferenceıd</span><span class="sxs-lookup"><span data-stu-id="e537b-156">-ImageReferenceId</span></span>
<span data-ttu-id="e537b-157">Resim başvuru KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e537b-157">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="e537b-158">-Imagereferenceteklif</span><span class="sxs-lookup"><span data-stu-id="e537b-158">-ImageReferenceOffer</span></span>
<span data-ttu-id="e537b-159">Sanal makine görüntüsünün (Vmımage) teklifinin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e537b-159">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="e537b-160">Resim teklifi edinmek için Get-AzVMImageOffer cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e537b-160">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="e537b-161">-Imagereferencepublisher</span><span class="sxs-lookup"><span data-stu-id="e537b-161">-ImageReferencePublisher</span></span>
<span data-ttu-id="e537b-162">Vmımage yayımcısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e537b-162">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="e537b-163">Yayımcı edinmek için Get-AzVMImagePublisher cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e537b-163">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="e537b-164">-Imagereferencesku</span><span class="sxs-lookup"><span data-stu-id="e537b-164">-ImageReferenceSku</span></span>
<span data-ttu-id="e537b-165">VMImage SKU 'SU belirtir.</span><span class="sxs-lookup"><span data-stu-id="e537b-165">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="e537b-166">STB 'ler almak için Get-AzVMImageSku cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e537b-166">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="e537b-167">-Imagereferenceversion</span><span class="sxs-lookup"><span data-stu-id="e537b-167">-ImageReferenceVersion</span></span>
<span data-ttu-id="e537b-168">VMImage sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e537b-168">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="e537b-169">En son sürümü kullanmak için belirli bir sürüm yerine en son sürümünü belirtin.</span><span class="sxs-lookup"><span data-stu-id="e537b-169">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="e537b-170">-Imageurı</span><span class="sxs-lookup"><span data-stu-id="e537b-170">-ImageUri</span></span>
<span data-ttu-id="e537b-171">Kullanıcı görüntüsü için blob URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e537b-171">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="e537b-172">VMSS, Kullanıcı görüntüsünün aynı kapsayıcısında bir işletim sistemi diski oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e537b-172">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="e537b-173">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="e537b-173">-LicenseType</span></span>
<span data-ttu-id="e537b-174">Kendi lisans senaryonuzu verecek lisans türünü belirtin.</span><span class="sxs-lookup"><span data-stu-id="e537b-174">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="e537b-175">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="e537b-175">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="e537b-176">Yönetilen disk için depolama hesabı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e537b-176">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="e537b-177">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="e537b-177">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e537b-178">Standartlrs</span><span class="sxs-lookup"><span data-stu-id="e537b-178">StandardLRS</span></span>
- <span data-ttu-id="e537b-179">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="e537b-179">PremiumLRS</span></span>

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

### <span data-ttu-id="e537b-180">-Maxbatchınstancepercent</span><span class="sxs-lookup"><span data-stu-id="e537b-180">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="e537b-181">Tek bir toplu işlemde çalışırken yükseltme tarafından aynı anda Yükseltilecek toplam sanal makine örneklerinin en yüksek yüzdesi.</span><span class="sxs-lookup"><span data-stu-id="e537b-181">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="e537b-182">Bu en yüksek düzeyde, önceki veya gelecekteki toplu işlemdeki sağlıksız örnekler, daha yüksek güvenilirlik sağlamak amacıyla toplu işteki örneklerin yüzdesine neden olabilir.</span><span class="sxs-lookup"><span data-stu-id="e537b-182">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="e537b-183">Değer belirtilmezse, 20 olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="e537b-183">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e537b-184">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="e537b-184">-MaxPrice</span></span>
<span data-ttu-id="e537b-185">Düşük öncelikli VM/VMSS için ödemek istediğiniz en yüksek fiyatı belirtir.</span><span class="sxs-lookup"><span data-stu-id="e537b-185">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="e537b-186">Bu fiyat ABD doları cinsindendir.</span><span class="sxs-lookup"><span data-stu-id="e537b-186">This price is in US Dollars.</span></span> <span data-ttu-id="e537b-187">Bu fiyat VM boyutu için geçerli düşük öncelik fiyatıyla karşılaştırılır.</span><span class="sxs-lookup"><span data-stu-id="e537b-187">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="e537b-188">Ayrıca, düşük öncelikli VM/VMSS oluşturma/güncelleştirme sırasında fiyatlar karşılaştırılır ve işlem yalnızca maxPrice geçerli düşük öncelik fiyatından büyükse başarıdır.</span><span class="sxs-lookup"><span data-stu-id="e537b-188">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="e537b-189">Geçerli düşük öncelik fiyatının VM/VMSS oluşturulduktan sonra maxPrice 'den fazla olması durumunda, maxPrice de düşük öncelikli VM/VMSS çıkarmak için kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="e537b-189">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="e537b-190">Olası değerler: sıfırdan büyük herhangi bir ondalık değer.</span><span class="sxs-lookup"><span data-stu-id="e537b-190">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="e537b-191">Örnek: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="e537b-191">Example: 0.01538.</span></span>  <span data-ttu-id="e537b-192">-1 düşük öncelikli VM/VMSS 'nin fiyat nedenlerinin çıkarılmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="e537b-192">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="e537b-193">Ayrıca, sizin sağlanmadıysa varsayılan en fazla fiyat-1 ' dir.</span><span class="sxs-lookup"><span data-stu-id="e537b-193">Also, the default max price is -1 if it is not provided by you.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e537b-194">-Maxunhealthyınstancepercent</span><span class="sxs-lookup"><span data-stu-id="e537b-194">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="e537b-195">Ölçek kümesindeki toplam sanal makine örneklerinin, yükseltilme sonucu olarak, yükseltme sonucu olan veya çalışırken yükseltme iptal edilmeden önce sanal makine durumu denetimleri tarafından sağlıksız bir durumda bulunabildiği en yüksek oranı.</span><span class="sxs-lookup"><span data-stu-id="e537b-195">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="e537b-196">Bu kısıtlama, toplu işlem başlatılmadan önce işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="e537b-196">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="e537b-197">Değer belirtilmezse, 20 olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="e537b-197">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e537b-198">-Maxunhealthyyükseltildi Dedınstancepercent</span><span class="sxs-lookup"><span data-stu-id="e537b-198">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="e537b-199">Sağlıksız durumda olabilecek en yüksek yükseltilmiş sanal makine örneği yüzdesi.</span><span class="sxs-lookup"><span data-stu-id="e537b-199">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="e537b-200">Bu denetim her toplu iş yükseltildikten sonra gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="e537b-200">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="e537b-201">Bu yüzde aşılırsa, çalışırken güncelleştirme iptal edilir.</span><span class="sxs-lookup"><span data-stu-id="e537b-201">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="e537b-202">Değer belirtilmezse, 20 olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="e537b-202">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e537b-203">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="e537b-203">-OsDiskCaching</span></span>
<span data-ttu-id="e537b-204">İşletim sistemi diskinin önbelleğe alma modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e537b-204">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="e537b-205">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="e537b-205">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e537b-206">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e537b-206">None</span></span>
- <span data-ttu-id="e537b-207">Özelliğinin</span><span class="sxs-lookup"><span data-stu-id="e537b-207">ReadOnly</span></span>
- <span data-ttu-id="e537b-208">ReadWrite varsayılan değer ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="e537b-208">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="e537b-209">Önbellek değerini değiştirirseniz cmdlet sanal makineyi yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="e537b-209">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="e537b-210">Bu ayar, diskin tutarlılığını ve performansını etkiler.</span><span class="sxs-lookup"><span data-stu-id="e537b-210">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e537b-211">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="e537b-211">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="e537b-212">İşletim sistemi diskinde WriteAccelerator 'in etkinleştirilip etkinleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e537b-212">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="e537b-213">-Overprovision</span><span class="sxs-lookup"><span data-stu-id="e537b-213">-Overprovision</span></span>
<span data-ttu-id="e537b-214">Cmdlet 'in VMSS 'yi içerip içermediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e537b-214">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="e537b-215">-Pausetimebetweentoplu Işler</span><span class="sxs-lookup"><span data-stu-id="e537b-215">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="e537b-216">Bir toplu işteki tüm sanal makinelerin güncelleştirmesini tamamlama ve sonraki toplu işlemi başlatma arasındaki bekleme süresi.</span><span class="sxs-lookup"><span data-stu-id="e537b-216">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="e537b-217">Süre ISO 8601 biçiminde belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="e537b-217">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="e537b-218">Varsayılan değer 0 saniyedir (PT0S).</span><span class="sxs-lookup"><span data-stu-id="e537b-218">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="e537b-219">-PlanName</span><span class="sxs-lookup"><span data-stu-id="e537b-219">-PlanName</span></span>
<span data-ttu-id="e537b-220">Plan adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e537b-220">Specifies the plan name.</span></span>

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

### <span data-ttu-id="e537b-221">-Planürün</span><span class="sxs-lookup"><span data-stu-id="e537b-221">-PlanProduct</span></span>
<span data-ttu-id="e537b-222">Plan ürünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e537b-222">Specifies the plan product.</span></span>

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

### <span data-ttu-id="e537b-223">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="e537b-223">-PlanPromotionCode</span></span>
<span data-ttu-id="e537b-224">Plan promosyon kodunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e537b-224">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="e537b-225">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="e537b-225">-PlanPublisher</span></span>
<span data-ttu-id="e537b-226">Publisher planı 'nı belirtir.</span><span class="sxs-lookup"><span data-stu-id="e537b-226">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="e537b-227">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="e537b-227">-ProvisionVMAgent</span></span>
<span data-ttu-id="e537b-228">VMSS 'deki Windows sanal makinelerinde sanal makine aracısının sağlanması gerekip gerekmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e537b-228">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="e537b-229">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="e537b-229">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="e537b-230">Bu ölçek kümesiyle kullanılacak yakınlık Yerleşim grubunun kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="e537b-230">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="e537b-231">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e537b-231">-ResourceGroupName</span></span>
<span data-ttu-id="e537b-232">VMSS 'nin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e537b-232">Specifies the name of the resource group the VMSS belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e537b-233">-Scaleınpolicy</span><span class="sxs-lookup"><span data-stu-id="e537b-233">-ScaleInPolicy</span></span>
<span data-ttu-id="e537b-234">Sanal makine ölçeği kümesinde ölçeklendirme yapılırken izlenen kurallar.</span><span class="sxs-lookup"><span data-stu-id="e537b-234">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="e537b-235">Olası değerler: ' default ', ' OldestVM ' ve ' NewestVM '.</span><span class="sxs-lookup"><span data-stu-id="e537b-235">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="e537b-236">' Varsayılan ' sanal makine ölçeği kümesi içinde ölçeklendirildiyse, ölçek kümesi ilk olarak bölgeler genelinde dengelenebilir ve bu bir zonal ölçeği kümesidir.</span><span class="sxs-lookup"><span data-stu-id="e537b-236">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="e537b-237">Ardından, hata etki alanları genelinde mümkün olduğunca dengeli olacaktır.</span><span class="sxs-lookup"><span data-stu-id="e537b-237">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="e537b-238">Her hata etki alanı içinde, kaldırılmak üzere seçilen sanal makineler, ölçek ile korunmayan en yeni değerler olacaktır.</span><span class="sxs-lookup"><span data-stu-id="e537b-238">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="e537b-239">' OldestVM ' sanal makine ölçeği kümesi ölçeklendiğinde, ölçeğe korunmayan en eski sanal makineler kaldırılmak üzere seçilir.</span><span class="sxs-lookup"><span data-stu-id="e537b-239">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="e537b-240">Zonal sanal makine ölçek kümeleri için, ölçek kümesi önce bölgeler arasında dengelenecek.</span><span class="sxs-lookup"><span data-stu-id="e537b-240">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="e537b-241">Her bir bölgede, korunmayan en eski sanal makineler kaldırılmak üzere seçilir.</span><span class="sxs-lookup"><span data-stu-id="e537b-241">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="e537b-242">' NewestVM ' sanal makine ölçeği kümesi ölçeklendiğinde, ölçeğe korunmayan en yeni sanal makineler kaldırılmak üzere seçilir.</span><span class="sxs-lookup"><span data-stu-id="e537b-242">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="e537b-243">Zonal sanal makine ölçek kümeleri için, ölçek kümesi önce bölgeler arasında dengelenecek.</span><span class="sxs-lookup"><span data-stu-id="e537b-243">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="e537b-244">Her bir bölgede, korunmayan en yeni sanal makineler kaldırılmak üzere seçilir.</span><span class="sxs-lookup"><span data-stu-id="e537b-244">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e537b-245">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="e537b-245">-SinglePlacementGroup</span></span>
<span data-ttu-id="e537b-246">Tek yerleşim grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e537b-246">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="e537b-247">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="e537b-247">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="e537b-248">Uzantıların fazladan sağlanan diğer VM 'lerde çalıştırılmamıştır.</span><span class="sxs-lookup"><span data-stu-id="e537b-248">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="e537b-249">-Skukapasitesi</span><span class="sxs-lookup"><span data-stu-id="e537b-249">-SkuCapacity</span></span>
<span data-ttu-id="e537b-250">VMSS 'deki örneklerin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e537b-250">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e537b-251">-SkuName</span><span class="sxs-lookup"><span data-stu-id="e537b-251">-SkuName</span></span>
<span data-ttu-id="e537b-252">Tüm VMSS örneklerinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e537b-252">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="e537b-253">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="e537b-253">-SkuTier</span></span>
<span data-ttu-id="e537b-254">VMSS 'nin katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e537b-254">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="e537b-255">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="e537b-255">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e537b-256">Ardından</span><span class="sxs-lookup"><span data-stu-id="e537b-256">Standard</span></span>
- <span data-ttu-id="e537b-257">Ana</span><span class="sxs-lookup"><span data-stu-id="e537b-257">Basic</span></span>

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

### <span data-ttu-id="e537b-258">Etiketli</span><span class="sxs-lookup"><span data-stu-id="e537b-258">-Tag</span></span>
<span data-ttu-id="e537b-259">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="e537b-259">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e537b-260">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="e537b-260">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e537b-261">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="e537b-261">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="e537b-262">Yapılandırılabilir süre (dakika cinsinden) silinen bir sanal makinenin, etkinlik otomatik onaylanmadan (zaman aşımına uğramadan) önce zamanlanmış olayı sonlandırmasını sağlamak gerekecektir.</span><span class="sxs-lookup"><span data-stu-id="e537b-262">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="e537b-263">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="e537b-263">-TerminateScheduledEvents</span></span>
<span data-ttu-id="e537b-264">Zamanlanmış zamanlanmış olayının etkin veya devre dışı olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e537b-264">Specifies whether the Terminate Scheduled event is enabled or disabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e537b-265">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="e537b-265">-TimeZone</span></span>
<span data-ttu-id="e537b-266">Windows işletim sisteminin saat dilimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e537b-266">Specifies the time zone for Windows OS.</span></span>

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

### <span data-ttu-id="e537b-267">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="e537b-267">-UltraSSDEnabled</span></span>
<span data-ttu-id="e537b-268">Sanal makine ölçek kümesinde UltraSSD_LRS depolama hesabı türüne sahip bir veya birden çok yönetilen veri diskine sahip olan bir veya birden çok yönetilen veri diski</span><span class="sxs-lookup"><span data-stu-id="e537b-268">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="e537b-269">Depolama hesap türü UltraSSD_LRS yönetilen diskler yalnızca bu özellik etkinse bir VMSUBNET 'e eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="e537b-269">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e537b-270">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="e537b-270">-UpgradePolicyMode</span></span>
<span data-ttu-id="e537b-271">Belirtilen ölçek kümesindeki sanal makinelere yükseltme modu.</span><span class="sxs-lookup"><span data-stu-id="e537b-271">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="e537b-272">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="e537b-272">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e537b-273">Otomatik</span><span class="sxs-lookup"><span data-stu-id="e537b-273">Automatic</span></span>
- <span data-ttu-id="e537b-274">El ile</span><span class="sxs-lookup"><span data-stu-id="e537b-274">Manual</span></span>
- <span data-ttu-id="e537b-275">Melerdeki</span><span class="sxs-lookup"><span data-stu-id="e537b-275">Rolling</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.UpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e537b-276">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="e537b-276">-VhdContainer</span></span>
<span data-ttu-id="e537b-277">VMSS işletim sistemi disklerini depolamak için kullanılan kapsayıcı URL 'Lerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e537b-277">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e537b-278">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e537b-278">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="e537b-279">Yerel bir VMSS nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e537b-279">Specifies a local VMSS object.</span></span>
<span data-ttu-id="e537b-280">Bir VMSS nesnesi edinmek için Get-AzVmss cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e537b-280">To obtain a VMSS object, use the Get-AzVmss cmdlet.</span></span>
<span data-ttu-id="e537b-281">Bu sanal makine nesnesi, VMSS 'nin güncelleştirilmiş durumunu içerir.</span><span class="sxs-lookup"><span data-stu-id="e537b-281">This virtual machine object contains the updated state for the VMSS.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e537b-282">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="e537b-282">-VMScaleSetName</span></span>
<span data-ttu-id="e537b-283">Bu cmdlet 'in oluşturduğu VMSS 'nin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e537b-283">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e537b-284">-Onay</span><span class="sxs-lookup"><span data-stu-id="e537b-284">-Confirm</span></span>
<span data-ttu-id="e537b-285">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e537b-285">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e537b-286">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e537b-286">-WhatIf</span></span>
<span data-ttu-id="e537b-287">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e537b-287">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e537b-288">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e537b-288">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e537b-289">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e537b-289">CommonParameters</span></span>
<span data-ttu-id="e537b-290">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e537b-290">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e537b-291">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e537b-291">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e537b-292">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e537b-292">INPUTS</span></span>

### <span data-ttu-id="e537b-293">System. String</span><span class="sxs-lookup"><span data-stu-id="e537b-293">System.String</span></span>

### <span data-ttu-id="e537b-294">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e537b-294">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="e537b-295">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e537b-295">System.Boolean</span></span>

## <span data-ttu-id="e537b-296">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e537b-296">OUTPUTS</span></span>

### <span data-ttu-id="e537b-297">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e537b-297">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="e537b-298">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e537b-298">NOTES</span></span>

## <span data-ttu-id="e537b-299">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e537b-299">RELATED LINKS</span></span>

[<span data-ttu-id="e537b-300">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e537b-300">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="e537b-301">Yeni-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e537b-301">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="e537b-302">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e537b-302">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="e537b-303">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e537b-303">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="e537b-304">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e537b-304">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="e537b-305">Başlangıç-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e537b-305">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="e537b-306">Dur-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e537b-306">Stop-AzVmss</span></span>](./Stop-AzVmss.md)


