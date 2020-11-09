---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: 4b262b219c479cc2c56311c54d41eb05e2eb866d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319601"
---
# <span data-ttu-id="552d6-101">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="552d6-101">Update-AzVmss</span></span>

## <span data-ttu-id="552d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="552d6-102">SYNOPSIS</span></span>
<span data-ttu-id="552d6-103">Bir VMSUBNET 'in durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="552d6-103">Updates the state of a VMSS.</span></span>

## <span data-ttu-id="552d6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="552d6-104">SYNTAX</span></span>

### <span data-ttu-id="552d6-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="552d6-105">DefaultParameter (Default)</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-BootDiagnosticsEnabled <Boolean>]
 [-BootDiagnosticsStorageUri <String>] [-CustomData <String>] [-DisableAutoRollback <Boolean>]
 [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
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
 [-VhdContainer <String[]>] [-AsJob] [-EncryptionAtHost <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="552d6-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="552d6-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-BootDiagnosticsEnabled <Boolean>]
 [-BootDiagnosticsStorageUri <String>] [-CustomData <String>] [-DisableAutoRollback <Boolean>]
 [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
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
 [-VhdContainer <String[]>] [-AsJob] [-EncryptionAtHost <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="552d6-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="552d6-107">DESCRIPTION</span></span>
<span data-ttu-id="552d6-108">**Update-AzVmss** cmdlet 'ı sanal makine ölçek kümesi 'nın (VMSS) durumunu yerel BIR VMSS nesnesinin durumuna güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="552d6-108">The **Update-AzVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="552d6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="552d6-109">EXAMPLES</span></span>

### <span data-ttu-id="552d6-110">Örnek 1: bir VMSS durumunu yerel bir VMSS nesnesinin durumuna güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="552d6-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="552d6-111">Bu komut, Group001 adındaki kaynak grubuna ait olan VMSS001 adındaki VMSS 'nin durumunu yerel bir VMSS nesnesinin durumuna güncelleştirir $LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="552d6-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="552d6-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="552d6-112">PARAMETERS</span></span>

### <span data-ttu-id="552d6-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="552d6-113">-AsJob</span></span>
<span data-ttu-id="552d6-114">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="552d6-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="552d6-115">-Automaticosupgrad</span><span class="sxs-lookup"><span data-stu-id="552d6-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="552d6-116">Resmin daha yeni bir sürümü kullanılabilir hale geldiğinde, bir yerde ölçeklendirme kümesi örneklerine otomatik olarak işletim sistemi yükseltmeleri uygulanıp uygulanmayacağı.</span><span class="sxs-lookup"><span data-stu-id="552d6-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="552d6-117">-AutomaticRepairGracePeriod</span><span class="sxs-lookup"><span data-stu-id="552d6-117">-AutomaticRepairGracePeriod</span></span>
<span data-ttu-id="552d6-118">VM 'deki durum değişikliği nedeniyle otomatik onarımların askıya alındığı süre.</span><span class="sxs-lookup"><span data-stu-id="552d6-118">The amount of time for which automatic repairs are suspended due to a state change on VM.</span></span> <span data-ttu-id="552d6-119">Kullanım süresi, durum değişikliği tamamlandıktan sonra başlar.</span><span class="sxs-lookup"><span data-stu-id="552d6-119">The grace time starts after the state change has completed.</span></span> <span data-ttu-id="552d6-120">Bu, erken veya kazayla onarılmasını önlemeye yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="552d6-120">This helps avoid premature or accidental repairs.</span></span> <span data-ttu-id="552d6-121">Süre ISO 8601 biçiminde belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="552d6-121">The time duration should be specified in ISO 8601 format.</span></span> <span data-ttu-id="552d6-122">İzin verilen en düşük kullanım süresi 30 dakika (PT30M), bu da varsayılan değerdir.</span><span class="sxs-lookup"><span data-stu-id="552d6-122">The minimum allowed grace period is 30 minutes (PT30M), which is also the default value.</span></span> <span data-ttu-id="552d6-123">İzin verilen en büyük kullanım süresi 90 dakikadır (PT90M).</span><span class="sxs-lookup"><span data-stu-id="552d6-123">The maximum allowed grace period is 90 minutes (PT90M).</span></span>

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

### <span data-ttu-id="552d6-124">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="552d6-124">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="552d6-125">Sanal makine ölçek kümesinde önyükleme tanılaması 'nın etkinleştirilmesi gerekip gerekmediği.</span><span class="sxs-lookup"><span data-stu-id="552d6-125">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="552d6-126">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="552d6-126">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="552d6-127">Konsol çıkışını ve ekran görüntüsünü yerleştirmek için kullanılacak depolama hesabının URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="552d6-127">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="552d6-128">-CustomData</span><span class="sxs-lookup"><span data-stu-id="552d6-128">-CustomData</span></span>
<span data-ttu-id="552d6-129">Özel verilerin Base-64 kodlu dizesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="552d6-129">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="552d6-130">Bu, sanal makinede dosya olarak kaydedilmiş bir ikili diziye çözülür.</span><span class="sxs-lookup"><span data-stu-id="552d6-130">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="552d6-131">İkili dizinin en fazla uzunluğu 65535 bayttır.</span><span class="sxs-lookup"><span data-stu-id="552d6-131">The maximum length of the binary array is 65535 bytes.</span></span> <br>
<span data-ttu-id="552d6-132">VM 'unuzda bulut-init kullanmak için, [oluşturma sırasında bir LINUX VM 'yi özelleştirmek amacıyla Cloud-Init kullanma](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="552d6-132">For using cloud-init for your VM, see [Using cloud-init to customize a Linux VM during creation](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

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

### <span data-ttu-id="552d6-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="552d6-133">-DefaultProfile</span></span>
<span data-ttu-id="552d6-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="552d6-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="552d6-135">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="552d6-135">-DisableAutoRollback</span></span>
<span data-ttu-id="552d6-136">Otomatik OS yükseltme Ilkesi için otomatik geri almayı devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="552d6-136">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="552d6-137">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="552d6-137">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="552d6-138">Bu cmdlet 'in Linux OS için parola kimlik doğrulamasını devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="552d6-138">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

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

### <span data-ttu-id="552d6-139">-EnableAutomaticRepair</span><span class="sxs-lookup"><span data-stu-id="552d6-139">-EnableAutomaticRepair</span></span>
<span data-ttu-id="552d6-140">Sanal makine ölçek kümesinde otomatik onarımları etkinleştirme veya devre dışı bırakma.</span><span class="sxs-lookup"><span data-stu-id="552d6-140">Enable or disable automatic repairs on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="552d6-141">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="552d6-141">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="552d6-142">VMSS 'deki Windows sanal makinelerinin otomatik güncelleştirmeler için etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="552d6-142">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="552d6-143">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="552d6-143">-EncryptionAtHost</span></span>
<span data-ttu-id="552d6-144">Bu parametre, sanal makine ölçek kümesi için ana bilgisayar şifrelemesini etkinleştirmek veya devre dışı bırakmak amacıyla istekte yer alan Kullanıcı tarafından kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="552d6-144">This parameter can be used by user in the request to enable or disable the Host Encryption for the virtual machine scale set.</span></span> 

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

### <span data-ttu-id="552d6-145">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="552d6-145">-IdentityId</span></span>
<span data-ttu-id="552d6-146">Sanal makine ölçek kümesiyle ilişkili kullanıcı kimliklerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="552d6-146">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="552d6-147">Kullanıcı kimliği başvuruları formda ARM kaynak kimlikleri olacaktır: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="552d6-147">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="552d6-148">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="552d6-148">-IdentityType</span></span>
<span data-ttu-id="552d6-149">Sanal makine ölçek kümesi için kullanılan kimlik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="552d6-149">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="552d6-150">' Systemassigneduserın ' türü, örtülü olarak oluşturulmuş bir kimlik ve Kullanıcı tarafından atanan kimlikler kümesini içerir.</span><span class="sxs-lookup"><span data-stu-id="552d6-150">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="552d6-151">' None ' türü, sanal makine ölçek kümesindeki tüm kimlikleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="552d6-151">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="552d6-152">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="552d6-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="552d6-153">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="552d6-153">SystemAssigned</span></span>
- <span data-ttu-id="552d6-154">Kullanıcı tarafından atanmış</span><span class="sxs-lookup"><span data-stu-id="552d6-154">UserAssigned</span></span>
- <span data-ttu-id="552d6-155">Systemassigneduseratandı</span><span class="sxs-lookup"><span data-stu-id="552d6-155">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="552d6-156">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="552d6-156">None</span></span>

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

### <span data-ttu-id="552d6-157">-Imagereferenceıd</span><span class="sxs-lookup"><span data-stu-id="552d6-157">-ImageReferenceId</span></span>
<span data-ttu-id="552d6-158">Resim başvuru KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="552d6-158">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="552d6-159">-Imagereferenceteklif</span><span class="sxs-lookup"><span data-stu-id="552d6-159">-ImageReferenceOffer</span></span>
<span data-ttu-id="552d6-160">Sanal makine görüntüsünün (Vmımage) teklifinin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="552d6-160">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="552d6-161">Resim teklifi edinmek için Get-AzVMImageOffer cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="552d6-161">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="552d6-162">-Imagereferencepublisher</span><span class="sxs-lookup"><span data-stu-id="552d6-162">-ImageReferencePublisher</span></span>
<span data-ttu-id="552d6-163">Vmımage yayımcısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="552d6-163">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="552d6-164">Yayımcı edinmek için Get-AzVMImagePublisher cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="552d6-164">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="552d6-165">-Imagereferencesku</span><span class="sxs-lookup"><span data-stu-id="552d6-165">-ImageReferenceSku</span></span>
<span data-ttu-id="552d6-166">VMImage SKU 'SU belirtir.</span><span class="sxs-lookup"><span data-stu-id="552d6-166">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="552d6-167">STB 'ler almak için Get-AzVMImageSku cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="552d6-167">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="552d6-168">-Imagereferenceversion</span><span class="sxs-lookup"><span data-stu-id="552d6-168">-ImageReferenceVersion</span></span>
<span data-ttu-id="552d6-169">VMImage sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="552d6-169">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="552d6-170">En son sürümü kullanmak için belirli bir sürüm yerine en son sürümünü belirtin.</span><span class="sxs-lookup"><span data-stu-id="552d6-170">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="552d6-171">-Imageurı</span><span class="sxs-lookup"><span data-stu-id="552d6-171">-ImageUri</span></span>
<span data-ttu-id="552d6-172">Kullanıcı görüntüsü için blob URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="552d6-172">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="552d6-173">VMSS, Kullanıcı görüntüsünün aynı kapsayıcısında bir işletim sistemi diski oluşturur.</span><span class="sxs-lookup"><span data-stu-id="552d6-173">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="552d6-174">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="552d6-174">-LicenseType</span></span>
<span data-ttu-id="552d6-175">Kendi lisans senaryonuzu verecek lisans türünü belirtin.</span><span class="sxs-lookup"><span data-stu-id="552d6-175">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="552d6-176">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="552d6-176">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="552d6-177">Yönetilen disk için depolama hesabı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="552d6-177">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="552d6-178">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="552d6-178">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="552d6-179">Standartlrs</span><span class="sxs-lookup"><span data-stu-id="552d6-179">StandardLRS</span></span>
- <span data-ttu-id="552d6-180">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="552d6-180">PremiumLRS</span></span>

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

### <span data-ttu-id="552d6-181">-Maxbatchınstancepercent</span><span class="sxs-lookup"><span data-stu-id="552d6-181">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="552d6-182">Tek bir toplu işlemde çalışırken yükseltme tarafından aynı anda Yükseltilecek toplam sanal makine örneklerinin en yüksek yüzdesi.</span><span class="sxs-lookup"><span data-stu-id="552d6-182">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="552d6-183">Bu en yüksek düzeyde, önceki veya gelecekteki toplu işlemdeki sağlıksız örnekler, daha yüksek güvenilirlik sağlamak amacıyla toplu işteki örneklerin yüzdesine neden olabilir.</span><span class="sxs-lookup"><span data-stu-id="552d6-183">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="552d6-184">Değer belirtilmezse, 20 olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="552d6-184">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="552d6-185">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="552d6-185">-MaxPrice</span></span>
<span data-ttu-id="552d6-186">Düşük öncelikli VM/VMSS için ödemek istediğiniz en yüksek fiyatı belirtir.</span><span class="sxs-lookup"><span data-stu-id="552d6-186">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="552d6-187">Bu fiyat ABD doları cinsindendir.</span><span class="sxs-lookup"><span data-stu-id="552d6-187">This price is in US Dollars.</span></span> <span data-ttu-id="552d6-188">Bu fiyat VM boyutu için geçerli düşük öncelik fiyatıyla karşılaştırılır.</span><span class="sxs-lookup"><span data-stu-id="552d6-188">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="552d6-189">Ayrıca, düşük öncelikli VM/VMSS oluşturma/güncelleştirme sırasında fiyatlar karşılaştırılır ve işlem yalnızca maxPrice geçerli düşük öncelik fiyatından büyükse başarıdır.</span><span class="sxs-lookup"><span data-stu-id="552d6-189">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="552d6-190">Geçerli düşük öncelik fiyatının VM/VMSS oluşturulduktan sonra maxPrice 'den fazla olması durumunda, maxPrice de düşük öncelikli VM/VMSS çıkarmak için kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="552d6-190">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="552d6-191">Olası değerler: sıfırdan büyük herhangi bir ondalık değer.</span><span class="sxs-lookup"><span data-stu-id="552d6-191">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="552d6-192">Örnek: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="552d6-192">Example: 0.01538.</span></span>  <span data-ttu-id="552d6-193">-1 düşük öncelikli VM/VMSS 'nin fiyat nedenlerinin çıkarılmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="552d6-193">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="552d6-194">Ayrıca, sizin sağlanmadıysa varsayılan en fazla fiyat-1 ' dir.</span><span class="sxs-lookup"><span data-stu-id="552d6-194">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="552d6-195">-Maxunhealthyınstancepercent</span><span class="sxs-lookup"><span data-stu-id="552d6-195">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="552d6-196">Ölçek kümesindeki toplam sanal makine örneklerinin, yükseltilme sonucu olarak, yükseltme sonucu olan veya çalışırken yükseltme iptal edilmeden önce sanal makine durumu denetimleri tarafından sağlıksız bir durumda bulunabildiği en yüksek oranı.</span><span class="sxs-lookup"><span data-stu-id="552d6-196">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="552d6-197">Bu kısıtlama, toplu işlem başlatılmadan önce işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="552d6-197">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="552d6-198">Değer belirtilmezse, 20 olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="552d6-198">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="552d6-199">-Maxunhealthyyükseltildi Dedınstancepercent</span><span class="sxs-lookup"><span data-stu-id="552d6-199">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="552d6-200">Sağlıksız durumda olabilecek en yüksek yükseltilmiş sanal makine örneği yüzdesi.</span><span class="sxs-lookup"><span data-stu-id="552d6-200">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="552d6-201">Bu denetim her toplu iş yükseltildikten sonra gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="552d6-201">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="552d6-202">Bu yüzde aşılırsa, çalışırken güncelleştirme iptal edilir.</span><span class="sxs-lookup"><span data-stu-id="552d6-202">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="552d6-203">Değer belirtilmezse, 20 olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="552d6-203">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="552d6-204">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="552d6-204">-OsDiskCaching</span></span>
<span data-ttu-id="552d6-205">İşletim sistemi diskinin önbelleğe alma modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="552d6-205">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="552d6-206">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="552d6-206">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="552d6-207">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="552d6-207">None</span></span>
- <span data-ttu-id="552d6-208">Özelliğinin</span><span class="sxs-lookup"><span data-stu-id="552d6-208">ReadOnly</span></span>
- <span data-ttu-id="552d6-209">ReadWrite varsayılan değer ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="552d6-209">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="552d6-210">Önbellek değerini değiştirirseniz cmdlet sanal makineyi yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="552d6-210">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="552d6-211">Bu ayar, diskin tutarlılığını ve performansını etkiler.</span><span class="sxs-lookup"><span data-stu-id="552d6-211">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="552d6-212">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="552d6-212">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="552d6-213">İşletim sistemi diskinde WriteAccelerator 'in etkinleştirilip etkinleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="552d6-213">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="552d6-214">-Overprovision</span><span class="sxs-lookup"><span data-stu-id="552d6-214">-Overprovision</span></span>
<span data-ttu-id="552d6-215">Cmdlet 'in VMSS 'yi içerip içermediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="552d6-215">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="552d6-216">-Pausetimebetweentoplu Işler</span><span class="sxs-lookup"><span data-stu-id="552d6-216">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="552d6-217">Bir toplu işteki tüm sanal makinelerin güncelleştirmesini tamamlama ve sonraki toplu işlemi başlatma arasındaki bekleme süresi.</span><span class="sxs-lookup"><span data-stu-id="552d6-217">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="552d6-218">Süre ISO 8601 biçiminde belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="552d6-218">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="552d6-219">Varsayılan değer 0 saniyedir (PT0S).</span><span class="sxs-lookup"><span data-stu-id="552d6-219">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="552d6-220">-PlanName</span><span class="sxs-lookup"><span data-stu-id="552d6-220">-PlanName</span></span>
<span data-ttu-id="552d6-221">Plan adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="552d6-221">Specifies the plan name.</span></span>

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

### <span data-ttu-id="552d6-222">-Planürün</span><span class="sxs-lookup"><span data-stu-id="552d6-222">-PlanProduct</span></span>
<span data-ttu-id="552d6-223">Plan ürünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="552d6-223">Specifies the plan product.</span></span>

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

### <span data-ttu-id="552d6-224">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="552d6-224">-PlanPromotionCode</span></span>
<span data-ttu-id="552d6-225">Plan promosyon kodunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="552d6-225">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="552d6-226">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="552d6-226">-PlanPublisher</span></span>
<span data-ttu-id="552d6-227">Publisher planı 'nı belirtir.</span><span class="sxs-lookup"><span data-stu-id="552d6-227">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="552d6-228">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="552d6-228">-ProvisionVMAgent</span></span>
<span data-ttu-id="552d6-229">VMSS 'deki Windows sanal makinelerinde sanal makine aracısının sağlanması gerekip gerekmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="552d6-229">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="552d6-230">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="552d6-230">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="552d6-231">Bu ölçek kümesiyle kullanılacak yakınlık Yerleşim grubunun kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="552d6-231">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="552d6-232">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="552d6-232">-ResourceGroupName</span></span>
<span data-ttu-id="552d6-233">VMSS 'nin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="552d6-233">Specifies the name of the resource group the VMSS belongs to.</span></span>

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

### <span data-ttu-id="552d6-234">-Scaleınpolicy</span><span class="sxs-lookup"><span data-stu-id="552d6-234">-ScaleInPolicy</span></span>
<span data-ttu-id="552d6-235">Sanal makine ölçeği kümesinde ölçeklendirme yapılırken izlenen kurallar.</span><span class="sxs-lookup"><span data-stu-id="552d6-235">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="552d6-236">Olası değerler: ' default ', ' OldestVM ' ve ' NewestVM '.</span><span class="sxs-lookup"><span data-stu-id="552d6-236">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="552d6-237">' Varsayılan ' sanal makine ölçeği kümesi içinde ölçeklendirildiyse, ölçek kümesi ilk olarak bölgeler genelinde dengelenebilir ve bu bir zonal ölçeği kümesidir.</span><span class="sxs-lookup"><span data-stu-id="552d6-237">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="552d6-238">Ardından, hata etki alanları genelinde mümkün olduğunca dengeli olacaktır.</span><span class="sxs-lookup"><span data-stu-id="552d6-238">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="552d6-239">Her hata etki alanı içinde, kaldırılmak üzere seçilen sanal makineler, ölçek ile korunmayan en yeni değerler olacaktır.</span><span class="sxs-lookup"><span data-stu-id="552d6-239">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="552d6-240">' OldestVM ' sanal makine ölçeği kümesi ölçeklendiğinde, ölçeğe korunmayan en eski sanal makineler kaldırılmak üzere seçilir.</span><span class="sxs-lookup"><span data-stu-id="552d6-240">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="552d6-241">Zonal sanal makine ölçek kümeleri için, ölçek kümesi önce bölgeler arasında dengelenecek.</span><span class="sxs-lookup"><span data-stu-id="552d6-241">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="552d6-242">Her bir bölgede, korunmayan en eski sanal makineler kaldırılmak üzere seçilir.</span><span class="sxs-lookup"><span data-stu-id="552d6-242">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="552d6-243">' NewestVM ' sanal makine ölçeği kümesi ölçeklendiğinde, ölçeğe korunmayan en yeni sanal makineler kaldırılmak üzere seçilir.</span><span class="sxs-lookup"><span data-stu-id="552d6-243">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="552d6-244">Zonal sanal makine ölçek kümeleri için, ölçek kümesi önce bölgeler arasında dengelenecek.</span><span class="sxs-lookup"><span data-stu-id="552d6-244">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="552d6-245">Her bir bölgede, korunmayan en yeni sanal makineler kaldırılmak üzere seçilir.</span><span class="sxs-lookup"><span data-stu-id="552d6-245">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="552d6-246">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="552d6-246">-SinglePlacementGroup</span></span>
<span data-ttu-id="552d6-247">Tek yerleşim grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="552d6-247">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="552d6-248">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="552d6-248">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="552d6-249">Uzantıların fazladan sağlanan diğer VM 'lerde çalıştırılmamıştır.</span><span class="sxs-lookup"><span data-stu-id="552d6-249">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="552d6-250">-Skukapasitesi</span><span class="sxs-lookup"><span data-stu-id="552d6-250">-SkuCapacity</span></span>
<span data-ttu-id="552d6-251">VMSS 'deki örneklerin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="552d6-251">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="552d6-252">-SkuName</span><span class="sxs-lookup"><span data-stu-id="552d6-252">-SkuName</span></span>
<span data-ttu-id="552d6-253">Tüm VMSS örneklerinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="552d6-253">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="552d6-254">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="552d6-254">-SkuTier</span></span>
<span data-ttu-id="552d6-255">VMSS 'nin katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="552d6-255">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="552d6-256">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="552d6-256">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="552d6-257">Ardından</span><span class="sxs-lookup"><span data-stu-id="552d6-257">Standard</span></span>
- <span data-ttu-id="552d6-258">Ana</span><span class="sxs-lookup"><span data-stu-id="552d6-258">Basic</span></span>

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

### <span data-ttu-id="552d6-259">Etiketli</span><span class="sxs-lookup"><span data-stu-id="552d6-259">-Tag</span></span>
<span data-ttu-id="552d6-260">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="552d6-260">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="552d6-261">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="552d6-261">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="552d6-262">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="552d6-262">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="552d6-263">Yapılandırılabilir süre (dakika cinsinden) silinen bir sanal makinenin, etkinlik otomatik onaylanmadan (zaman aşımına uğramadan) önce zamanlanmış olayı sonlandırmasını sağlamak gerekecektir.</span><span class="sxs-lookup"><span data-stu-id="552d6-263">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="552d6-264">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="552d6-264">-TerminateScheduledEvents</span></span>
<span data-ttu-id="552d6-265">Zamanlanmış zamanlanmış olayının etkin veya devre dışı olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="552d6-265">Specifies whether the Terminate Scheduled event is enabled or disabled.</span></span>

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

### <span data-ttu-id="552d6-266">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="552d6-266">-TimeZone</span></span>
<span data-ttu-id="552d6-267">Windows işletim sisteminin saat dilimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="552d6-267">Specifies the time zone for Windows OS.</span></span> <span data-ttu-id="552d6-268">Örneğin \" Pasifik standart saati \" .</span><span class="sxs-lookup"><span data-stu-id="552d6-268">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="552d6-269">Olası değerler, [TimeZoneInfo. GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones)tarafından döndürülen saat dilimlerinde [TimeZoneInfo.ID](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) değeri olabilir.</span><span class="sxs-lookup"><span data-stu-id="552d6-269">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

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

### <span data-ttu-id="552d6-270">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="552d6-270">-UltraSSDEnabled</span></span>
<span data-ttu-id="552d6-271">Sanal makine ölçek kümesinde UltraSSD_LRS depolama hesabı türüne sahip bir veya birden çok yönetilen veri diskine sahip olan bir veya birden çok yönetilen veri diski</span><span class="sxs-lookup"><span data-stu-id="552d6-271">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="552d6-272">Depolama hesap türü UltraSSD_LRS yönetilen diskler yalnızca bu özellik etkinse bir VMSUBNET 'e eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="552d6-272">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="552d6-273">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="552d6-273">-UpgradePolicyMode</span></span>
<span data-ttu-id="552d6-274">Belirtilen ölçek kümesindeki sanal makinelere yükseltme modu.</span><span class="sxs-lookup"><span data-stu-id="552d6-274">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="552d6-275">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="552d6-275">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="552d6-276">Otomatik</span><span class="sxs-lookup"><span data-stu-id="552d6-276">Automatic</span></span>
- <span data-ttu-id="552d6-277">El ile</span><span class="sxs-lookup"><span data-stu-id="552d6-277">Manual</span></span>
- <span data-ttu-id="552d6-278">Melerdeki</span><span class="sxs-lookup"><span data-stu-id="552d6-278">Rolling</span></span>

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

### <span data-ttu-id="552d6-279">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="552d6-279">-VhdContainer</span></span>
<span data-ttu-id="552d6-280">VMSS işletim sistemi disklerini depolamak için kullanılan kapsayıcı URL 'Lerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="552d6-280">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="552d6-281">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="552d6-281">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="552d6-282">Yerel bir VMSS nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="552d6-282">Specifies a local VMSS object.</span></span>
<span data-ttu-id="552d6-283">Bir VMSS nesnesi edinmek için Get-AzVmss cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="552d6-283">To obtain a VMSS object, use the Get-AzVmss cmdlet.</span></span>
<span data-ttu-id="552d6-284">Bu sanal makine nesnesi, VMSS 'nin güncelleştirilmiş durumunu içerir.</span><span class="sxs-lookup"><span data-stu-id="552d6-284">This virtual machine object contains the updated state for the VMSS.</span></span>

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

### <span data-ttu-id="552d6-285">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="552d6-285">-VMScaleSetName</span></span>
<span data-ttu-id="552d6-286">Bu cmdlet 'in oluşturduğu VMSS 'nin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="552d6-286">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="552d6-287">-Onay</span><span class="sxs-lookup"><span data-stu-id="552d6-287">-Confirm</span></span>
<span data-ttu-id="552d6-288">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="552d6-288">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="552d6-289">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="552d6-289">-WhatIf</span></span>
<span data-ttu-id="552d6-290">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="552d6-290">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="552d6-291">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="552d6-291">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="552d6-292">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="552d6-292">CommonParameters</span></span>
<span data-ttu-id="552d6-293">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="552d6-293">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="552d6-294">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="552d6-294">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="552d6-295">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="552d6-295">INPUTS</span></span>

### <span data-ttu-id="552d6-296">System. String</span><span class="sxs-lookup"><span data-stu-id="552d6-296">System.String</span></span>

### <span data-ttu-id="552d6-297">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="552d6-297">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="552d6-298">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="552d6-298">System.Boolean</span></span>

## <span data-ttu-id="552d6-299">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="552d6-299">OUTPUTS</span></span>

### <span data-ttu-id="552d6-300">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="552d6-300">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="552d6-301">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="552d6-301">NOTES</span></span>

## <span data-ttu-id="552d6-302">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="552d6-302">RELATED LINKS</span></span>

[<span data-ttu-id="552d6-303">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="552d6-303">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="552d6-304">Yeni-AzVmss</span><span class="sxs-lookup"><span data-stu-id="552d6-304">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="552d6-305">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="552d6-305">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="552d6-306">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="552d6-306">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="552d6-307">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="552d6-307">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="552d6-308">Başlangıç-AzVmss</span><span class="sxs-lookup"><span data-stu-id="552d6-308">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="552d6-309">Dur-AzVmss</span><span class="sxs-lookup"><span data-stu-id="552d6-309">Stop-AzVmss</span></span>](./Stop-AzVmss.md)


