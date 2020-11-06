---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmVmss.md
ms.openlocfilehash: d2ecc5799319dcbc9b2e3710c186ffd7ebc09c64
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592025"
---
# <span data-ttu-id="be331-101">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="be331-101">Update-AzureRmVmss</span></span>

## <span data-ttu-id="be331-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be331-102">SYNOPSIS</span></span>
<span data-ttu-id="be331-103">Bir VMSUBNET 'in durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="be331-103">Updates the state of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be331-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="be331-104">SYNTAX</span></span>

### <span data-ttu-id="be331-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="be331-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-ImageReferenceSku <String>]
 [-ManagedDiskStorageAccountType <String>] [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-Overprovision <Boolean>] [-MaxBatchInstancePercent <Int32>]
 [-TimeZone <String>] [-BootDiagnosticsStorageUri <String>] [-AutomaticOSUpgrade <Boolean>]
 [-DisableAutoRollback <Boolean>] [-SinglePlacementGroup <Boolean>] [-CustomData <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-ImageReferenceId <String>] [-DisablePasswordAuthentication <Boolean>]
 [-Tag <Hashtable>] [-PlanName <String>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-ImageReferencePublisher <String>] [-PlanProduct <String>] [-VhdContainer <String[]>] [-ImageUri <String>]
 [-SkuTier <String>] [-EnableAutomaticUpdate <Boolean>] [-LicenseType <String>] [-SkuName <String>]
 [-PlanPromotionCode <String>] [-MaxUnhealthyInstancePercent <Int32>] [-SkuCapacity <Int32>]
 [-OsDiskWriteAccelerator <Boolean>] [-ImageReferenceOffer <String>] [-PauseTimeBetweenBatches <String>]
 [-OsDiskCaching <CachingTypes>] [-ImageReferenceVersion <String>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be331-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="be331-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-ImageReferenceSku <String>] [-IdentityId <String[]>]
 [-ManagedDiskStorageAccountType <String>] [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-Overprovision <Boolean>] [-MaxBatchInstancePercent <Int32>]
 [-TimeZone <String>] [-BootDiagnosticsStorageUri <String>] [-AutomaticOSUpgrade <Boolean>]
 [-DisableAutoRollback <Boolean>] [-SinglePlacementGroup <Boolean>] [-CustomData <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-ImageReferenceId <String>] [-DisablePasswordAuthentication <Boolean>]
 [-Tag <Hashtable>] [-PlanName <String>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-ImageReferencePublisher <String>] [-PlanProduct <String>] [-VhdContainer <String[]>] [-ImageUri <String>]
 [-SkuTier <String>] [-EnableAutomaticUpdate <Boolean>] [-LicenseType <String>]
 -IdentityType <ResourceIdentityType> [-SkuName <String>] [-PlanPromotionCode <String>]
 [-MaxUnhealthyInstancePercent <Int32>] [-SkuCapacity <Int32>] [-OsDiskWriteAccelerator <Boolean>]
 [-ImageReferenceOffer <String>] [-PauseTimeBetweenBatches <String>] [-OsDiskCaching <CachingTypes>]
 [-ImageReferenceVersion <String>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be331-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="be331-107">DESCRIPTION</span></span>
<span data-ttu-id="be331-108">**Update-AzureRmVmss** cmdlet 'ı sanal makine ölçek kümesi 'nın (VMSS) durumunu yerel BIR VMSS nesnesinin durumuna güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="be331-108">The **Update-AzureRmVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="be331-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="be331-109">EXAMPLES</span></span>

### <span data-ttu-id="be331-110">Örnek 1: bir VMSS durumunu yerel bir VMSS nesnesinin durumuna güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="be331-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzureRmVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="be331-111">Bu komut, Group001 adındaki kaynak grubuna ait olan VMSS001 adındaki VMSS 'nin durumunu yerel bir VMSS nesnesinin durumuna güncelleştirir $LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="be331-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="be331-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="be331-112">PARAMETERS</span></span>

### <span data-ttu-id="be331-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="be331-113">-AsJob</span></span>
<span data-ttu-id="be331-114">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="be331-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="be331-115">-Automaticosupgrad</span><span class="sxs-lookup"><span data-stu-id="be331-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="be331-116">Resmin daha yeni bir sürümü kullanılabilir hale geldiğinde, bir yerde ölçeklendirme kümesi örneklerine otomatik olarak işletim sistemi yükseltmeleri uygulanıp uygulanmayacağı.</span><span class="sxs-lookup"><span data-stu-id="be331-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="be331-117">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="be331-117">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="be331-118">Sanal makine ölçek kümesinde önyükleme tanılaması 'nın etkinleştirilmesi gerekip gerekmediği.</span><span class="sxs-lookup"><span data-stu-id="be331-118">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="be331-119">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="be331-119">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="be331-120">Konsol çıkışını ve ekran görüntüsünü yerleştirmek için kullanılacak depolama hesabının URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="be331-120">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="be331-121">-CustomData</span><span class="sxs-lookup"><span data-stu-id="be331-121">-CustomData</span></span>
<span data-ttu-id="be331-122">Özel verilerin Base-64 kodlu dizesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="be331-122">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="be331-123">Bu, sanal makinede dosya olarak kaydedilmiş bir ikili diziye çözülür.</span><span class="sxs-lookup"><span data-stu-id="be331-123">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="be331-124">İkili dizinin en fazla uzunluğu 65535 bayttır.</span><span class="sxs-lookup"><span data-stu-id="be331-124">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="be331-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be331-125">-DefaultProfile</span></span>
<span data-ttu-id="be331-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="be331-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be331-127">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="be331-127">-DisableAutoRollback</span></span>
<span data-ttu-id="be331-128">Otomatik OS yükseltme Ilkesi için otomatik geri almayı devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="be331-128">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="be331-129">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="be331-129">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="be331-130">Bu cmdlet 'in Linux OS için parola kimlik doğrulamasını devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="be331-130">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

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

### <span data-ttu-id="be331-131">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="be331-131">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="be331-132">VMSS 'deki Windows sanal makinelerinin otomatik güncelleştirmeler için etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="be331-132">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="be331-133">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="be331-133">-IdentityId</span></span>
<span data-ttu-id="be331-134">Sanal makine ölçek kümesiyle ilişkili kullanıcı kimliklerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="be331-134">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="be331-135">Kullanıcı kimliği başvuruları formda ARM kaynak kimlikleri olacaktır: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="be331-135">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="be331-136">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="be331-136">-IdentityType</span></span>
<span data-ttu-id="be331-137">Sanal makine ölçek kümesi için kullanılan kimlik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="be331-137">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="be331-138">' Systemassigneduserın ' türü, örtülü olarak oluşturulmuş bir kimlik ve Kullanıcı tarafından atanan kimlikler kümesini içerir.</span><span class="sxs-lookup"><span data-stu-id="be331-138">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="be331-139">' None ' türü, sanal makine ölçek kümesindeki tüm kimlikleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="be331-139">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="be331-140">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="be331-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="be331-141">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="be331-141">SystemAssigned</span></span>
- <span data-ttu-id="be331-142">Kullanıcı tarafından atanmış</span><span class="sxs-lookup"><span data-stu-id="be331-142">UserAssigned</span></span>
- <span data-ttu-id="be331-143">Systemassigneduseratandı</span><span class="sxs-lookup"><span data-stu-id="be331-143">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="be331-144">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="be331-144">None</span></span>

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

### <span data-ttu-id="be331-145">-Imagereferenceıd</span><span class="sxs-lookup"><span data-stu-id="be331-145">-ImageReferenceId</span></span>
<span data-ttu-id="be331-146">Resim başvuru KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="be331-146">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="be331-147">-Imagereferenceteklif</span><span class="sxs-lookup"><span data-stu-id="be331-147">-ImageReferenceOffer</span></span>
<span data-ttu-id="be331-148">Sanal makine görüntüsünün (Vmımage) teklifinin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="be331-148">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="be331-149">Resim teklifi edinmek için Get-AzureRmVMImageOffer cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="be331-149">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="be331-150">-Imagereferencepublisher</span><span class="sxs-lookup"><span data-stu-id="be331-150">-ImageReferencePublisher</span></span>
<span data-ttu-id="be331-151">Vmımage yayımcısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="be331-151">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="be331-152">Yayımcı edinmek için Get-AzureRmVMImagePublisher cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="be331-152">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="be331-153">-Imagereferencesku</span><span class="sxs-lookup"><span data-stu-id="be331-153">-ImageReferenceSku</span></span>
<span data-ttu-id="be331-154">VMImage SKU 'SU belirtir.</span><span class="sxs-lookup"><span data-stu-id="be331-154">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="be331-155">STB 'ler almak için Get-AzureRmVMImageSku cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="be331-155">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="be331-156">-Imagereferenceversion</span><span class="sxs-lookup"><span data-stu-id="be331-156">-ImageReferenceVersion</span></span>
<span data-ttu-id="be331-157">VMImage sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="be331-157">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="be331-158">En son sürümü kullanmak için belirli bir sürüm yerine en son sürümünü belirtin.</span><span class="sxs-lookup"><span data-stu-id="be331-158">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="be331-159">-Imageurı</span><span class="sxs-lookup"><span data-stu-id="be331-159">-ImageUri</span></span>
<span data-ttu-id="be331-160">Kullanıcı görüntüsü için blob URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="be331-160">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="be331-161">VMSS, Kullanıcı görüntüsünün aynı kapsayıcısında bir işletim sistemi diski oluşturur.</span><span class="sxs-lookup"><span data-stu-id="be331-161">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="be331-162">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="be331-162">-LicenseType</span></span>
<span data-ttu-id="be331-163">Kendi lisans senaryonuzu verecek lisans türünü belirtin.</span><span class="sxs-lookup"><span data-stu-id="be331-163">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="be331-164">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="be331-164">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="be331-165">Yönetilen disk için depolama hesabı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="be331-165">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="be331-166">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="be331-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="be331-167">Standartlrs</span><span class="sxs-lookup"><span data-stu-id="be331-167">StandardLRS</span></span>
- <span data-ttu-id="be331-168">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="be331-168">PremiumLRS</span></span>

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

### <span data-ttu-id="be331-169">-Maxbatchınstancepercent</span><span class="sxs-lookup"><span data-stu-id="be331-169">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="be331-170">Tek bir toplu işlemde çalışırken yükseltme tarafından aynı anda Yükseltilecek toplam sanal makine örneklerinin en yüksek yüzdesi.</span><span class="sxs-lookup"><span data-stu-id="be331-170">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="be331-171">Bu en yüksek düzeyde, önceki veya gelecekteki toplu işlemdeki sağlıksız örnekler, daha yüksek güvenilirlik sağlamak amacıyla toplu işteki örneklerin yüzdesine neden olabilir.</span><span class="sxs-lookup"><span data-stu-id="be331-171">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="be331-172">Değer belirtilmezse, 20 olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="be331-172">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="be331-173">-Maxunhealthyınstancepercent</span><span class="sxs-lookup"><span data-stu-id="be331-173">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="be331-174">Ölçek kümesindeki toplam sanal makine örneklerinin, yükseltilme sonucu olarak, yükseltme sonucu olan veya çalışırken yükseltme iptal edilmeden önce sanal makine durumu denetimleri tarafından sağlıksız bir durumda bulunabildiği en yüksek oranı.</span><span class="sxs-lookup"><span data-stu-id="be331-174">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="be331-175">Bu kısıtlama, toplu işlem başlatılmadan önce işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="be331-175">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="be331-176">Değer belirtilmezse, 20 olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="be331-176">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="be331-177">-Maxunhealthyyükseltildi Dedınstancepercent</span><span class="sxs-lookup"><span data-stu-id="be331-177">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="be331-178">Sağlıksız durumda olabilecek en yüksek yükseltilmiş sanal makine örneği yüzdesi.</span><span class="sxs-lookup"><span data-stu-id="be331-178">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="be331-179">Bu denetim her toplu iş yükseltildikten sonra gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="be331-179">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="be331-180">Bu yüzde aşılırsa, çalışırken güncelleştirme iptal edilir.</span><span class="sxs-lookup"><span data-stu-id="be331-180">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="be331-181">Değer belirtilmezse, 20 olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="be331-181">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="be331-182">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="be331-182">-OsDiskCaching</span></span>
<span data-ttu-id="be331-183">İşletim sistemi diskinin önbelleğe alma modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="be331-183">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="be331-184">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="be331-184">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="be331-185">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="be331-185">None</span></span>
- <span data-ttu-id="be331-186">Özelliğinin</span><span class="sxs-lookup"><span data-stu-id="be331-186">ReadOnly</span></span>
- <span data-ttu-id="be331-187">ReadWrite varsayılan değer ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="be331-187">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="be331-188">Önbellek değerini değiştirirseniz cmdlet sanal makineyi yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="be331-188">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="be331-189">Bu ayar, diskin tutarlılığını ve performansını etkiler.</span><span class="sxs-lookup"><span data-stu-id="be331-189">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="be331-190">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="be331-190">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="be331-191">İşletim sistemi diskinde WriteAccelerator 'in etkinleştirilip etkinleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="be331-191">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="be331-192">-Overprovision</span><span class="sxs-lookup"><span data-stu-id="be331-192">-Overprovision</span></span>
<span data-ttu-id="be331-193">Cmdlet 'in VMSS 'yi içerip içermediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="be331-193">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="be331-194">-Pausetimebetweentoplu Işler</span><span class="sxs-lookup"><span data-stu-id="be331-194">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="be331-195">Bir toplu işteki tüm sanal makinelerin güncelleştirmesini tamamlama ve sonraki toplu işlemi başlatma arasındaki bekleme süresi.</span><span class="sxs-lookup"><span data-stu-id="be331-195">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="be331-196">Süre ISO 8601 biçiminde belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="be331-196">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="be331-197">Varsayılan değer 0 saniyedir (PT0S).</span><span class="sxs-lookup"><span data-stu-id="be331-197">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="be331-198">-PlanName</span><span class="sxs-lookup"><span data-stu-id="be331-198">-PlanName</span></span>
<span data-ttu-id="be331-199">Plan adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="be331-199">Specifies the plan name.</span></span>

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

### <span data-ttu-id="be331-200">-Planürün</span><span class="sxs-lookup"><span data-stu-id="be331-200">-PlanProduct</span></span>
<span data-ttu-id="be331-201">Plan ürünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="be331-201">Specifies the plan product.</span></span>

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

### <span data-ttu-id="be331-202">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="be331-202">-PlanPromotionCode</span></span>
<span data-ttu-id="be331-203">Plan promosyon kodunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="be331-203">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="be331-204">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="be331-204">-PlanPublisher</span></span>
<span data-ttu-id="be331-205">Publisher planı 'nı belirtir.</span><span class="sxs-lookup"><span data-stu-id="be331-205">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="be331-206">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="be331-206">-ProvisionVMAgent</span></span>
<span data-ttu-id="be331-207">VMSS 'deki Windows sanal makinelerinde sanal makine aracısının sağlanması gerekip gerekmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="be331-207">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="be331-208">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be331-208">-ResourceGroupName</span></span>
<span data-ttu-id="be331-209">VMSS 'nin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="be331-209">Specifies the name of the resource group the VMSS belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be331-210">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="be331-210">-SinglePlacementGroup</span></span>
<span data-ttu-id="be331-211">Tek yerleşim grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="be331-211">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="be331-212">-Skukapasitesi</span><span class="sxs-lookup"><span data-stu-id="be331-212">-SkuCapacity</span></span>
<span data-ttu-id="be331-213">VMSS 'deki örneklerin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="be331-213">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="be331-214">-SkuName</span><span class="sxs-lookup"><span data-stu-id="be331-214">-SkuName</span></span>
<span data-ttu-id="be331-215">Tüm VMSS örneklerinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="be331-215">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="be331-216">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="be331-216">-SkuTier</span></span>
<span data-ttu-id="be331-217">VMSS 'nin katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="be331-217">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="be331-218">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="be331-218">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="be331-219">Ardından</span><span class="sxs-lookup"><span data-stu-id="be331-219">Standard</span></span>
- <span data-ttu-id="be331-220">Ana</span><span class="sxs-lookup"><span data-stu-id="be331-220">Basic</span></span>

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

### <span data-ttu-id="be331-221">Etiketli</span><span class="sxs-lookup"><span data-stu-id="be331-221">-Tag</span></span>
<span data-ttu-id="be331-222">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="be331-222">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="be331-223">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="be331-223">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="be331-224">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="be331-224">-TimeZone</span></span>
<span data-ttu-id="be331-225">Windows işletim sisteminin saat dilimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="be331-225">Specifies the time zone for Windows OS.</span></span>

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

### <span data-ttu-id="be331-226">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="be331-226">-UltraSSDEnabled</span></span>
<span data-ttu-id="be331-227">Sanal makine ölçek kümesinde UltraSSD_LRS depolama hesabı türüne sahip bir veya birden çok yönetilen veri diskine sahip olan bir veya birden çok yönetilen veri diski</span><span class="sxs-lookup"><span data-stu-id="be331-227">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="be331-228">Depolama hesap türü UltraSSD_LRS yönetilen diskler yalnızca bu özellik etkinse bir VMSUBNET 'e eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="be331-228">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="be331-229">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="be331-229">-UpgradePolicyMode</span></span>
<span data-ttu-id="be331-230">Belirtilen ölçek kümesindeki sanal makinelere yükseltme modu.</span><span class="sxs-lookup"><span data-stu-id="be331-230">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="be331-231">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="be331-231">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="be331-232">Otomatik</span><span class="sxs-lookup"><span data-stu-id="be331-232">Automatic</span></span>
- <span data-ttu-id="be331-233">El ile</span><span class="sxs-lookup"><span data-stu-id="be331-233">Manual</span></span>
- <span data-ttu-id="be331-234">Melerdeki</span><span class="sxs-lookup"><span data-stu-id="be331-234">Rolling</span></span>

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

### <span data-ttu-id="be331-235">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="be331-235">-VhdContainer</span></span>
<span data-ttu-id="be331-236">VMSS işletim sistemi disklerini depolamak için kullanılan kapsayıcı URL 'Lerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="be331-236">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="be331-237">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="be331-237">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="be331-238">Yerel bir VMSS nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="be331-238">Specifies a local VMSS object.</span></span>
<span data-ttu-id="be331-239">Bir VMSS nesnesi edinmek için Get-AzureRmVmss cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="be331-239">To obtain a VMSS object, use the Get-AzureRmVmss cmdlet.</span></span>
<span data-ttu-id="be331-240">Bu sanal makine nesnesi, VMSS 'nin güncelleştirilmiş durumunu içerir.</span><span class="sxs-lookup"><span data-stu-id="be331-240">This virtual machine object contains the updated state for the VMSS.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be331-241">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="be331-241">-VMScaleSetName</span></span>
<span data-ttu-id="be331-242">Bu cmdlet 'in oluşturduğu VMSS 'nin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="be331-242">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be331-243">-Onay</span><span class="sxs-lookup"><span data-stu-id="be331-243">-Confirm</span></span>
<span data-ttu-id="be331-244">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="be331-244">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be331-245">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be331-245">-WhatIf</span></span>
<span data-ttu-id="be331-246">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="be331-246">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be331-247">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="be331-247">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be331-248">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be331-248">CommonParameters</span></span>
<span data-ttu-id="be331-249">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="be331-249">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be331-250">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be331-250">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be331-251">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="be331-251">INPUTS</span></span>

### <span data-ttu-id="be331-252">System. String</span><span class="sxs-lookup"><span data-stu-id="be331-252">System.String</span></span>

### <span data-ttu-id="be331-253">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="be331-253">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>
<span data-ttu-id="be331-254">Parametreler: VirtualMachineScaleSet (ByValue)</span><span class="sxs-lookup"><span data-stu-id="be331-254">Parameters: VirtualMachineScaleSet (ByValue)</span></span>

## <span data-ttu-id="be331-255">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="be331-255">OUTPUTS</span></span>

### <span data-ttu-id="be331-256">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="be331-256">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="be331-257">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="be331-257">NOTES</span></span>

## <span data-ttu-id="be331-258">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="be331-258">RELATED LINKS</span></span>

[<span data-ttu-id="be331-259">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="be331-259">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="be331-260">Yeni-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="be331-260">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="be331-261">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="be331-261">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="be331-262">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="be331-262">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="be331-263">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="be331-263">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="be331-264">Başlangıç-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="be331-264">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="be331-265">Dur-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="be331-265">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)


