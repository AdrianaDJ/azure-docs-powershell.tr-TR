---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: c8a482c4d3021e1dd5de30582d2dad501a20ed41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752628"
---
# <span data-ttu-id="ddd12-101">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ddd12-101">Update-AzVmss</span></span>

## <span data-ttu-id="ddd12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddd12-102">SYNOPSIS</span></span>
<span data-ttu-id="ddd12-103">Bir VMSUBNET 'in durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-103">Updates the state of a VMSS.</span></span>

## <span data-ttu-id="ddd12-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ddd12-104">SYNTAX</span></span>

### <span data-ttu-id="ddd12-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ddd12-105">DefaultParameter (Default)</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-BootDiagnosticsStorageUri <String>] [-CustomData <String>]
 [-DisableAutoRollback <Boolean>] [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticUpdate <Boolean>]
 [-ImageReferenceId <String>] [-ImageReferenceOffer <String>] [-ImageReferencePublisher <String>]
 [-ImageReferenceSku <String>] [-ImageReferenceVersion <String>] [-ImageUri <String>] [-LicenseType <String>]
 [-ManagedDiskStorageAccountType <String>] [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>]
 [-MaxUnhealthyInstancePercent <Int32>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-OsDiskCaching <CachingTypes>] [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>]
 [-PauseTimeBetweenBatches <String>] [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>] [-SinglePlacementGroup <Boolean>]
 [-SkuCapacity <Int32>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ddd12-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddd12-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-BootDiagnosticsStorageUri <String>] [-CustomData <String>]
 [-DisableAutoRollback <Boolean>] [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticUpdate <Boolean>]
 [-IdentityId <String[]>] -IdentityType <ResourceIdentityType> [-ImageReferenceId <String>]
 [-ImageReferenceOffer <String>] [-ImageReferencePublisher <String>] [-ImageReferenceSku <String>]
 [-ImageReferenceVersion <String>] [-ImageUri <String>] [-LicenseType <String>]
 [-ManagedDiskStorageAccountType <String>] [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>]
 [-MaxUnhealthyInstancePercent <Int32>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-OsDiskCaching <CachingTypes>] [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>]
 [-PauseTimeBetweenBatches <String>] [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>] [-SinglePlacementGroup <Boolean>]
 [-SkuCapacity <Int32>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ddd12-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ddd12-107">DESCRIPTION</span></span>
<span data-ttu-id="ddd12-108">**Update-AzVmss** cmdlet 'ı sanal makine ölçek kümesi 'nın (VMSS) durumunu yerel BIR VMSS nesnesinin durumuna güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-108">The **Update-AzVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="ddd12-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ddd12-109">EXAMPLES</span></span>

### <span data-ttu-id="ddd12-110">Örnek 1: bir VMSS durumunu yerel bir VMSS nesnesinin durumuna güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="ddd12-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="ddd12-111">Bu komut, Group001 adındaki kaynak grubuna ait olan VMSS001 adındaki VMSS 'nin durumunu yerel bir VMSS nesnesinin durumuna güncelleştirir $LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="ddd12-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="ddd12-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ddd12-112">PARAMETERS</span></span>

### <span data-ttu-id="ddd12-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="ddd12-113">-AsJob</span></span>
<span data-ttu-id="ddd12-114">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="ddd12-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="ddd12-115">-Automaticosupgrad</span><span class="sxs-lookup"><span data-stu-id="ddd12-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="ddd12-116">Resmin daha yeni bir sürümü kullanılabilir hale geldiğinde, bir yerde ölçeklendirme kümesi örneklerine otomatik olarak işletim sistemi yükseltmeleri uygulanıp uygulanmayacağı.</span><span class="sxs-lookup"><span data-stu-id="ddd12-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="ddd12-117">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="ddd12-117">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="ddd12-118">Sanal makine ölçek kümesinde önyükleme tanılaması 'nın etkinleştirilmesi gerekip gerekmediği.</span><span class="sxs-lookup"><span data-stu-id="ddd12-118">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="ddd12-119">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="ddd12-119">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="ddd12-120">Konsol çıkışını ve ekran görüntüsünü yerleştirmek için kullanılacak depolama hesabının URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="ddd12-120">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="ddd12-121">-CustomData</span><span class="sxs-lookup"><span data-stu-id="ddd12-121">-CustomData</span></span>
<span data-ttu-id="ddd12-122">Özel verilerin Base-64 kodlu dizesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-122">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="ddd12-123">Bu, sanal makinede dosya olarak kaydedilmiş bir ikili diziye çözülür.</span><span class="sxs-lookup"><span data-stu-id="ddd12-123">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="ddd12-124">İkili dizinin en fazla uzunluğu 65535 bayttır.</span><span class="sxs-lookup"><span data-stu-id="ddd12-124">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="ddd12-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddd12-125">-DefaultProfile</span></span>
<span data-ttu-id="ddd12-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ddd12-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddd12-127">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="ddd12-127">-DisableAutoRollback</span></span>
<span data-ttu-id="ddd12-128">Otomatik OS yükseltme Ilkesi için otomatik geri almayı devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="ddd12-128">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="ddd12-129">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="ddd12-129">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="ddd12-130">Bu cmdlet 'in Linux OS için parola kimlik doğrulamasını devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-130">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

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

### <span data-ttu-id="ddd12-131">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="ddd12-131">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="ddd12-132">VMSS 'deki Windows sanal makinelerinin otomatik güncelleştirmeler için etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-132">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="ddd12-133">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="ddd12-133">-IdentityId</span></span>
<span data-ttu-id="ddd12-134">Sanal makine ölçek kümesiyle ilişkili kullanıcı kimliklerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-134">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="ddd12-135">Kullanıcı kimliği başvuruları formda ARM kaynak kimlikleri olacaktır: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="ddd12-135">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="ddd12-136">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="ddd12-136">-IdentityType</span></span>
<span data-ttu-id="ddd12-137">Sanal makine ölçek kümesi için kullanılan kimlik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-137">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="ddd12-138">' Systemassigneduserın ' türü, örtülü olarak oluşturulmuş bir kimlik ve Kullanıcı tarafından atanan kimlikler kümesini içerir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-138">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="ddd12-139">' None ' türü, sanal makine ölçek kümesindeki tüm kimlikleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ddd12-139">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="ddd12-140">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ddd12-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ddd12-141">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="ddd12-141">SystemAssigned</span></span>
- <span data-ttu-id="ddd12-142">Kullanıcı tarafından atanmış</span><span class="sxs-lookup"><span data-stu-id="ddd12-142">UserAssigned</span></span>
- <span data-ttu-id="ddd12-143">Systemassigneduseratandı</span><span class="sxs-lookup"><span data-stu-id="ddd12-143">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="ddd12-144">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ddd12-144">None</span></span>

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

### <span data-ttu-id="ddd12-145">-Imagereferenceıd</span><span class="sxs-lookup"><span data-stu-id="ddd12-145">-ImageReferenceId</span></span>
<span data-ttu-id="ddd12-146">Resim başvuru KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-146">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="ddd12-147">-Imagereferenceteklif</span><span class="sxs-lookup"><span data-stu-id="ddd12-147">-ImageReferenceOffer</span></span>
<span data-ttu-id="ddd12-148">Sanal makine görüntüsünün (Vmımage) teklifinin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-148">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="ddd12-149">Resim teklifi edinmek için Get-AzVMImageOffer cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ddd12-149">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="ddd12-150">-Imagereferencepublisher</span><span class="sxs-lookup"><span data-stu-id="ddd12-150">-ImageReferencePublisher</span></span>
<span data-ttu-id="ddd12-151">Vmımage yayımcısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-151">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="ddd12-152">Yayımcı edinmek için Get-AzVMImagePublisher cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ddd12-152">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="ddd12-153">-Imagereferencesku</span><span class="sxs-lookup"><span data-stu-id="ddd12-153">-ImageReferenceSku</span></span>
<span data-ttu-id="ddd12-154">VMImage SKU 'SU belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-154">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="ddd12-155">STB 'ler almak için Get-AzVMImageSku cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ddd12-155">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="ddd12-156">-Imagereferenceversion</span><span class="sxs-lookup"><span data-stu-id="ddd12-156">-ImageReferenceVersion</span></span>
<span data-ttu-id="ddd12-157">VMImage sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-157">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="ddd12-158">En son sürümü kullanmak için belirli bir sürüm yerine en son sürümünü belirtin.</span><span class="sxs-lookup"><span data-stu-id="ddd12-158">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="ddd12-159">-Imageurı</span><span class="sxs-lookup"><span data-stu-id="ddd12-159">-ImageUri</span></span>
<span data-ttu-id="ddd12-160">Kullanıcı görüntüsü için blob URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-160">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="ddd12-161">VMSS, Kullanıcı görüntüsünün aynı kapsayıcısında bir işletim sistemi diski oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ddd12-161">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="ddd12-162">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="ddd12-162">-LicenseType</span></span>
<span data-ttu-id="ddd12-163">Kendi lisans senaryonuzu verecek lisans türünü belirtin.</span><span class="sxs-lookup"><span data-stu-id="ddd12-163">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="ddd12-164">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="ddd12-164">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="ddd12-165">Yönetilen disk için depolama hesabı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-165">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="ddd12-166">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ddd12-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ddd12-167">Standartlrs</span><span class="sxs-lookup"><span data-stu-id="ddd12-167">StandardLRS</span></span>
- <span data-ttu-id="ddd12-168">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="ddd12-168">PremiumLRS</span></span>

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

### <span data-ttu-id="ddd12-169">-Maxbatchınstancepercent</span><span class="sxs-lookup"><span data-stu-id="ddd12-169">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="ddd12-170">Tek bir toplu işlemde çalışırken yükseltme tarafından aynı anda Yükseltilecek toplam sanal makine örneklerinin en yüksek yüzdesi.</span><span class="sxs-lookup"><span data-stu-id="ddd12-170">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="ddd12-171">Bu en yüksek düzeyde, önceki veya gelecekteki toplu işlemdeki sağlıksız örnekler, daha yüksek güvenilirlik sağlamak amacıyla toplu işteki örneklerin yüzdesine neden olabilir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-171">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="ddd12-172">Değer belirtilmezse, 20 olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="ddd12-172">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="ddd12-173">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="ddd12-173">-MaxPrice</span></span>
<span data-ttu-id="ddd12-174">Düşük öncelikli VM/VMSS için ödemek istediğiniz en yüksek fiyatı belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-174">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="ddd12-175">Bu fiyat ABD doları cinsindendir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-175">This price is in US Dollars.</span></span> <span data-ttu-id="ddd12-176">Bu fiyat VM boyutu için geçerli düşük öncelik fiyatıyla karşılaştırılır.</span><span class="sxs-lookup"><span data-stu-id="ddd12-176">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="ddd12-177">Ayrıca, düşük öncelikli VM/VMSS oluşturma/güncelleştirme sırasında fiyatlar karşılaştırılır ve işlem yalnızca maxPrice geçerli düşük öncelik fiyatından büyükse başarıdır.</span><span class="sxs-lookup"><span data-stu-id="ddd12-177">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="ddd12-178">Geçerli düşük öncelik fiyatının VM/VMSS oluşturulduktan sonra maxPrice 'den fazla olması durumunda, maxPrice de düşük öncelikli VM/VMSS çıkarmak için kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="ddd12-178">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="ddd12-179">Olası değerler: sıfırdan büyük herhangi bir ondalık değer.</span><span class="sxs-lookup"><span data-stu-id="ddd12-179">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="ddd12-180">Örnek: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="ddd12-180">Example: 0.01538.</span></span>  <span data-ttu-id="ddd12-181">-1 düşük öncelikli VM/VMSS 'nin fiyat nedenlerinin çıkarılmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="ddd12-181">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="ddd12-182">Ayrıca, sizin sağlanmadıysa varsayılan en fazla fiyat-1 ' dir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-182">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="ddd12-183">-Maxunhealthyınstancepercent</span><span class="sxs-lookup"><span data-stu-id="ddd12-183">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="ddd12-184">Ölçek kümesindeki toplam sanal makine örneklerinin, yükseltilme sonucu olarak, yükseltme sonucu olan veya çalışırken yükseltme iptal edilmeden önce sanal makine durumu denetimleri tarafından sağlıksız bir durumda bulunabildiği en yüksek oranı.</span><span class="sxs-lookup"><span data-stu-id="ddd12-184">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="ddd12-185">Bu kısıtlama, toplu işlem başlatılmadan önce işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-185">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="ddd12-186">Değer belirtilmezse, 20 olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="ddd12-186">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="ddd12-187">-Maxunhealthyyükseltildi Dedınstancepercent</span><span class="sxs-lookup"><span data-stu-id="ddd12-187">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="ddd12-188">Sağlıksız durumda olabilecek en yüksek yükseltilmiş sanal makine örneği yüzdesi.</span><span class="sxs-lookup"><span data-stu-id="ddd12-188">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="ddd12-189">Bu denetim her toplu iş yükseltildikten sonra gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-189">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="ddd12-190">Bu yüzde aşılırsa, çalışırken güncelleştirme iptal edilir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-190">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="ddd12-191">Değer belirtilmezse, 20 olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="ddd12-191">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="ddd12-192">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="ddd12-192">-OsDiskCaching</span></span>
<span data-ttu-id="ddd12-193">İşletim sistemi diskinin önbelleğe alma modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-193">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="ddd12-194">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ddd12-194">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ddd12-195">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ddd12-195">None</span></span>
- <span data-ttu-id="ddd12-196">Özelliğinin</span><span class="sxs-lookup"><span data-stu-id="ddd12-196">ReadOnly</span></span>
- <span data-ttu-id="ddd12-197">ReadWrite varsayılan değer ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="ddd12-197">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="ddd12-198">Önbellek değerini değiştirirseniz cmdlet sanal makineyi yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="ddd12-198">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="ddd12-199">Bu ayar, diskin tutarlılığını ve performansını etkiler.</span><span class="sxs-lookup"><span data-stu-id="ddd12-199">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="ddd12-200">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="ddd12-200">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="ddd12-201">İşletim sistemi diskinde WriteAccelerator 'in etkinleştirilip etkinleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-201">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="ddd12-202">-Overprovision</span><span class="sxs-lookup"><span data-stu-id="ddd12-202">-Overprovision</span></span>
<span data-ttu-id="ddd12-203">Cmdlet 'in VMSS 'yi içerip içermediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-203">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="ddd12-204">-Pausetimebetweentoplu Işler</span><span class="sxs-lookup"><span data-stu-id="ddd12-204">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="ddd12-205">Bir toplu işteki tüm sanal makinelerin güncelleştirmesini tamamlama ve sonraki toplu işlemi başlatma arasındaki bekleme süresi.</span><span class="sxs-lookup"><span data-stu-id="ddd12-205">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="ddd12-206">Süre ISO 8601 biçiminde belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-206">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="ddd12-207">Varsayılan değer 0 saniyedir (PT0S).</span><span class="sxs-lookup"><span data-stu-id="ddd12-207">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="ddd12-208">-PlanName</span><span class="sxs-lookup"><span data-stu-id="ddd12-208">-PlanName</span></span>
<span data-ttu-id="ddd12-209">Plan adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-209">Specifies the plan name.</span></span>

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

### <span data-ttu-id="ddd12-210">-Planürün</span><span class="sxs-lookup"><span data-stu-id="ddd12-210">-PlanProduct</span></span>
<span data-ttu-id="ddd12-211">Plan ürünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-211">Specifies the plan product.</span></span>

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

### <span data-ttu-id="ddd12-212">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="ddd12-212">-PlanPromotionCode</span></span>
<span data-ttu-id="ddd12-213">Plan promosyon kodunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-213">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="ddd12-214">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="ddd12-214">-PlanPublisher</span></span>
<span data-ttu-id="ddd12-215">Publisher planı 'nı belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-215">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="ddd12-216">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="ddd12-216">-ProvisionVMAgent</span></span>
<span data-ttu-id="ddd12-217">VMSS 'deki Windows sanal makinelerinde sanal makine aracısının sağlanması gerekip gerekmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-217">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="ddd12-218">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddd12-218">-ResourceGroupName</span></span>
<span data-ttu-id="ddd12-219">VMSS 'nin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-219">Specifies the name of the resource group the VMSS belongs to.</span></span>

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

### <span data-ttu-id="ddd12-220">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="ddd12-220">-SinglePlacementGroup</span></span>
<span data-ttu-id="ddd12-221">Tek yerleşim grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-221">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="ddd12-222">-Skukapasitesi</span><span class="sxs-lookup"><span data-stu-id="ddd12-222">-SkuCapacity</span></span>
<span data-ttu-id="ddd12-223">VMSS 'deki örneklerin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-223">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="ddd12-224">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ddd12-224">-SkuName</span></span>
<span data-ttu-id="ddd12-225">Tüm VMSS örneklerinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-225">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="ddd12-226">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="ddd12-226">-SkuTier</span></span>
<span data-ttu-id="ddd12-227">VMSS 'nin katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-227">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="ddd12-228">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ddd12-228">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ddd12-229">Ardından</span><span class="sxs-lookup"><span data-stu-id="ddd12-229">Standard</span></span>
- <span data-ttu-id="ddd12-230">Ana</span><span class="sxs-lookup"><span data-stu-id="ddd12-230">Basic</span></span>

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

### <span data-ttu-id="ddd12-231">Etiketli</span><span class="sxs-lookup"><span data-stu-id="ddd12-231">-Tag</span></span>
<span data-ttu-id="ddd12-232">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="ddd12-232">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ddd12-233">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="ddd12-233">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ddd12-234">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="ddd12-234">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="ddd12-235">Yapılandırılabilir süre (dakika cinsinden) silinen bir sanal makinenin, etkinlik otomatik onaylanmadan (zaman aşımına uğramadan) önce zamanlanmış olayı sonlandırmasını sağlamak gerekecektir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-235">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

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

### <span data-ttu-id="ddd12-236">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="ddd12-236">-TerminateScheduledEvents</span></span>
<span data-ttu-id="ddd12-237">Zamanlanmış zamanlanmış olayının etkin veya devre dışı olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-237">Specifies whether the Terminate Scheduled event is enabled or disabled.</span></span>

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

### <span data-ttu-id="ddd12-238">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="ddd12-238">-TimeZone</span></span>
<span data-ttu-id="ddd12-239">Windows işletim sisteminin saat dilimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-239">Specifies the time zone for Windows OS.</span></span>

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

### <span data-ttu-id="ddd12-240">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="ddd12-240">-UltraSSDEnabled</span></span>
<span data-ttu-id="ddd12-241">Sanal makine ölçek kümesinde UltraSSD_LRS depolama hesabı türüne sahip bir veya birden çok yönetilen veri diskine sahip olan bir veya birden çok yönetilen veri diski</span><span class="sxs-lookup"><span data-stu-id="ddd12-241">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="ddd12-242">Depolama hesap türü UltraSSD_LRS yönetilen diskler yalnızca bu özellik etkinse bir VMSUBNET 'e eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-242">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="ddd12-243">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="ddd12-243">-UpgradePolicyMode</span></span>
<span data-ttu-id="ddd12-244">Belirtilen ölçek kümesindeki sanal makinelere yükseltme modu.</span><span class="sxs-lookup"><span data-stu-id="ddd12-244">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="ddd12-245">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ddd12-245">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ddd12-246">Otomatik</span><span class="sxs-lookup"><span data-stu-id="ddd12-246">Automatic</span></span>
- <span data-ttu-id="ddd12-247">El ile</span><span class="sxs-lookup"><span data-stu-id="ddd12-247">Manual</span></span>
- <span data-ttu-id="ddd12-248">Melerdeki</span><span class="sxs-lookup"><span data-stu-id="ddd12-248">Rolling</span></span>

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

### <span data-ttu-id="ddd12-249">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="ddd12-249">-VhdContainer</span></span>
<span data-ttu-id="ddd12-250">VMSS işletim sistemi disklerini depolamak için kullanılan kapsayıcı URL 'Lerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-250">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="ddd12-251">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ddd12-251">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="ddd12-252">Yerel bir VMSS nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-252">Specifies a local VMSS object.</span></span>
<span data-ttu-id="ddd12-253">Bir VMSS nesnesi edinmek için Get-AzVmss cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ddd12-253">To obtain a VMSS object, use the Get-AzVmss cmdlet.</span></span>
<span data-ttu-id="ddd12-254">Bu sanal makine nesnesi, VMSS 'nin güncelleştirilmiş durumunu içerir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-254">This virtual machine object contains the updated state for the VMSS.</span></span>

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

### <span data-ttu-id="ddd12-255">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="ddd12-255">-VMScaleSetName</span></span>
<span data-ttu-id="ddd12-256">Bu cmdlet 'in oluşturduğu VMSS 'nin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-256">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="ddd12-257">-Onay</span><span class="sxs-lookup"><span data-stu-id="ddd12-257">-Confirm</span></span>
<span data-ttu-id="ddd12-258">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ddd12-258">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddd12-259">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddd12-259">-WhatIf</span></span>
<span data-ttu-id="ddd12-260">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ddd12-260">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddd12-261">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ddd12-261">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddd12-262">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddd12-262">CommonParameters</span></span>
<span data-ttu-id="ddd12-263">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ddd12-263">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddd12-264">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ddd12-264">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddd12-265">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ddd12-265">INPUTS</span></span>

### <span data-ttu-id="ddd12-266">System. String</span><span class="sxs-lookup"><span data-stu-id="ddd12-266">System.String</span></span>

### <span data-ttu-id="ddd12-267">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ddd12-267">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="ddd12-268">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ddd12-268">System.Boolean</span></span>

## <span data-ttu-id="ddd12-269">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ddd12-269">OUTPUTS</span></span>

### <span data-ttu-id="ddd12-270">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ddd12-270">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="ddd12-271">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ddd12-271">NOTES</span></span>

## <span data-ttu-id="ddd12-272">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ddd12-272">RELATED LINKS</span></span>

[<span data-ttu-id="ddd12-273">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ddd12-273">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="ddd12-274">Yeni-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ddd12-274">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="ddd12-275">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ddd12-275">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="ddd12-276">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ddd12-276">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="ddd12-277">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ddd12-277">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="ddd12-278">Başlangıç-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ddd12-278">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="ddd12-279">Dur-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ddd12-279">Stop-AzVmss</span></span>](./Stop-AzVmss.md)


