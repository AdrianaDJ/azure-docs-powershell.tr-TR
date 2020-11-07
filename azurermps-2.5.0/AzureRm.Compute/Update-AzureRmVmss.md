---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermvmss
schema: 2.0.0
ms.openlocfilehash: 544af56c5e1ff72a3b23c3dcf89af36f7d74eff2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939151"
---
# <span data-ttu-id="52d2d-101">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="52d2d-101">Update-AzureRmVmss</span></span>

## <span data-ttu-id="52d2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52d2d-102">SYNOPSIS</span></span>
<span data-ttu-id="52d2d-103">Bir VMSUBNET 'in durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="52d2d-103">Updates the state of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52d2d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="52d2d-104">SYNTAX</span></span>

### <span data-ttu-id="52d2d-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="52d2d-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-ImageReferenceSku <String>]
 [-ManagedDiskStorageAccountType <StorageAccountTypes>] [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-Overprovision <Boolean>] [-MaxBatchInstancePercent <Int32>]
 [-TimeZone <String>] [-BootDiagnosticsStorageUri <String>] [-AutomaticOSUpgrade <Boolean>]
 [-SinglePlacementGroup <Boolean>] [-CustomData <String>] [-UpgradePolicyMode <UpgradeMode>]
 [-ImageReferenceId <String>] [-DisablePasswordAuthentication <Boolean>] [-Tag <Hashtable>]
 [-PlanName <String>] [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-ImageReferencePublisher <String>]
 [-PlanProduct <String>] [-VhdContainer <String[]>] [-ImageUri <String>] [-SkuTier <String>]
 [-EnableAutomaticUpdate <Boolean>] [-LicenseType <String>] [-SkuName <String>] [-PlanPromotionCode <String>]
 [-MaxUnhealthyInstancePercent <Int32>] [-SkuCapacity <Int32>] [-OsDiskWriteAccelerator <Boolean>]
 [-ImageReferenceOffer <String>] [-PauseTimeBetweenBatches <String>] [-OsDiskCaching <CachingTypes>]
 [-ImageReferenceVersion <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="52d2d-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="52d2d-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-ImageReferenceSku <String>] [-IdentityId <String[]>]
 [-ManagedDiskStorageAccountType <StorageAccountTypes>] [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-Overprovision <Boolean>] [-MaxBatchInstancePercent <Int32>]
 [-TimeZone <String>] [-BootDiagnosticsStorageUri <String>] [-AutomaticOSUpgrade <Boolean>]
 [-SinglePlacementGroup <Boolean>] [-CustomData <String>] [-UpgradePolicyMode <UpgradeMode>]
 [-ImageReferenceId <String>] [-DisablePasswordAuthentication <Boolean>] [-Tag <Hashtable>]
 [-PlanName <String>] [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-ImageReferencePublisher <String>]
 [-PlanProduct <String>] [-VhdContainer <String[]>] [-ImageUri <String>] [-SkuTier <String>]
 [-EnableAutomaticUpdate <Boolean>] [-LicenseType <String>] -IdentityType <ResourceIdentityType>
 [-SkuName <String>] [-PlanPromotionCode <String>] [-MaxUnhealthyInstancePercent <Int32>]
 [-SkuCapacity <Int32>] [-OsDiskWriteAccelerator <Boolean>] [-ImageReferenceOffer <String>]
 [-PauseTimeBetweenBatches <String>] [-OsDiskCaching <CachingTypes>] [-ImageReferenceVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52d2d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="52d2d-107">DESCRIPTION</span></span>
<span data-ttu-id="52d2d-108">**Update-AzureRmVmss** cmdlet 'ı sanal makine ölçek kümesi 'nın (VMSS) durumunu yerel BIR VMSS nesnesinin durumuna güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="52d2d-108">The **Update-AzureRmVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="52d2d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="52d2d-109">EXAMPLES</span></span>

### <span data-ttu-id="52d2d-110">Örnek 1: bir VMSS durumunu yerel bir VMSS nesnesinin durumuna güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="52d2d-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzureRmVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="52d2d-111">Bu komut, Group001 adındaki kaynak grubuna ait olan VMSS001 adındaki VMSS 'nin durumunu yerel bir VMSS nesnesinin durumuna güncelleştirir $LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="52d2d-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="52d2d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="52d2d-112">PARAMETERS</span></span>

### <span data-ttu-id="52d2d-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="52d2d-113">-AsJob</span></span>
<span data-ttu-id="52d2d-114">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="52d2d-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="52d2d-115">-Automaticosupgrad</span><span class="sxs-lookup"><span data-stu-id="52d2d-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="52d2d-116">Resmin daha yeni bir sürümü kullanılabilir hale geldiğinde, bir yerde ölçeklendirme kümesi örneklerine otomatik olarak işletim sistemi yükseltmeleri uygulanıp uygulanmayacağı.</span><span class="sxs-lookup"><span data-stu-id="52d2d-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d2d-117">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="52d2d-117">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="52d2d-118">Sanal makine ölçek kümesinde önyükleme tanılaması 'nın etkinleştirilmesi gerekip gerekmediği.</span><span class="sxs-lookup"><span data-stu-id="52d2d-118">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d2d-119">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="52d2d-119">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="52d2d-120">Konsol çıkışını ve ekran görüntüsünü yerleştirmek için kullanılacak depolama hesabının URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="52d2d-120">URI of the storage account to use for placing the console output and screenshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d2d-121">-CustomData</span><span class="sxs-lookup"><span data-stu-id="52d2d-121">-CustomData</span></span>
<span data-ttu-id="52d2d-122">Özel verilerin Base-64 kodlu dizesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="52d2d-122">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="52d2d-123">Bu, sanal makinede dosya olarak kaydedilmiş bir ikili diziye çözülür.</span><span class="sxs-lookup"><span data-stu-id="52d2d-123">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="52d2d-124">İkili dizinin en fazla uzunluğu 65535 bayttır.</span><span class="sxs-lookup"><span data-stu-id="52d2d-124">The maximum length of the binary array is 65535 bytes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d2d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52d2d-125">-DefaultProfile</span></span>
<span data-ttu-id="52d2d-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="52d2d-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52d2d-127">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="52d2d-127">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="52d2d-128">Bu cmdlet 'in Linux OS için parola kimlik doğrulamasını devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="52d2d-128">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d2d-129">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="52d2d-129">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="52d2d-130">VMSS 'deki Windows sanal makinelerinin otomatik güncelleştirmeler için etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="52d2d-130">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d2d-131">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="52d2d-131">-IdentityId</span></span>
<span data-ttu-id="52d2d-132">Sanal makine ölçek kümesiyle ilişkili kullanıcı kimliklerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="52d2d-132">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="52d2d-133">Kullanıcı kimliği başvuruları formda ARM kaynak kimlikleri olacaktır: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="52d2d-133">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d2d-134">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="52d2d-134">-IdentityType</span></span>
<span data-ttu-id="52d2d-135">Sanal makine ölçek kümesi için kullanılan kimlik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="52d2d-135">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="52d2d-136">' Systemassigneduserın ' türü, örtülü olarak oluşturulmuş bir kimlik ve Kullanıcı tarafından atanan kimlikler kümesini içerir.</span><span class="sxs-lookup"><span data-stu-id="52d2d-136">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="52d2d-137">' None ' türü, sanal makine ölçek kümesindeki tüm kimlikleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="52d2d-137">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="52d2d-138">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="52d2d-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="52d2d-139">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="52d2d-139">SystemAssigned</span></span>
- <span data-ttu-id="52d2d-140">Kullanıcı tarafından atanmış</span><span class="sxs-lookup"><span data-stu-id="52d2d-140">UserAssigned</span></span>
- <span data-ttu-id="52d2d-141">Systemassigneduseratandı</span><span class="sxs-lookup"><span data-stu-id="52d2d-141">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="52d2d-142">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="52d2d-142">None</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d2d-143">-Imagereferenceıd</span><span class="sxs-lookup"><span data-stu-id="52d2d-143">-ImageReferenceId</span></span>
<span data-ttu-id="52d2d-144">Resim başvuru KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="52d2d-144">Specifies the image reference ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d2d-145">-Imagereferenceteklif</span><span class="sxs-lookup"><span data-stu-id="52d2d-145">-ImageReferenceOffer</span></span>
<span data-ttu-id="52d2d-146">Sanal makine görüntüsünün (Vmımage) teklifinin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="52d2d-146">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="52d2d-147">Resim teklifi edinmek için Get-AzureRmVMImageOffer cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="52d2d-147">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d2d-148">-Imagereferencepublisher</span><span class="sxs-lookup"><span data-stu-id="52d2d-148">-ImageReferencePublisher</span></span>
<span data-ttu-id="52d2d-149">Vmımage yayımcısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="52d2d-149">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="52d2d-150">Yayımcı edinmek için Get-AzureRmVMImagePublisher cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="52d2d-150">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d2d-151">-Imagereferencesku</span><span class="sxs-lookup"><span data-stu-id="52d2d-151">-ImageReferenceSku</span></span>
<span data-ttu-id="52d2d-152">VMImage SKU 'SU belirtir.</span><span class="sxs-lookup"><span data-stu-id="52d2d-152">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="52d2d-153">STB 'ler almak için Get-AzureRmVMImageSku cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="52d2d-153">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d2d-154">-Imagereferenceversion</span><span class="sxs-lookup"><span data-stu-id="52d2d-154">-ImageReferenceVersion</span></span>
<span data-ttu-id="52d2d-155">VMImage sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="52d2d-155">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="52d2d-156">En son sürümü kullanmak için belirli bir sürüm yerine en son sürümünü belirtin.</span><span class="sxs-lookup"><span data-stu-id="52d2d-156">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d2d-157">-Imageurı</span><span class="sxs-lookup"><span data-stu-id="52d2d-157">-ImageUri</span></span>
<span data-ttu-id="52d2d-158">Kullanıcı görüntüsü için blob URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="52d2d-158">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="52d2d-159">VMSS, Kullanıcı görüntüsünün aynı kapsayıcısında bir işletim sistemi diski oluşturur.</span><span class="sxs-lookup"><span data-stu-id="52d2d-159">VMSS creates an operating system disk in the same container of the user image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d2d-160">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="52d2d-160">-LicenseType</span></span>
<span data-ttu-id="52d2d-161">Kendi lisans senaryonuzu verecek lisans türünü belirtin.</span><span class="sxs-lookup"><span data-stu-id="52d2d-161">Specify the license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d2d-162">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="52d2d-162">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="52d2d-163">Yönetilen disk için depolama hesabı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="52d2d-163">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="52d2d-164">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="52d2d-164">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="52d2d-165">Standartlrs</span><span class="sxs-lookup"><span data-stu-id="52d2d-165">StandardLRS</span></span>
- <span data-ttu-id="52d2d-166">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="52d2d-166">PremiumLRS</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d2d-167">-Maxbatchınstancepercent</span><span class="sxs-lookup"><span data-stu-id="52d2d-167">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="52d2d-168">Tek bir toplu işlemde çalışırken yükseltme tarafından aynı anda Yükseltilecek toplam sanal makine örneklerinin en yüksek yüzdesi.</span><span class="sxs-lookup"><span data-stu-id="52d2d-168">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="52d2d-169">Bu en yüksek düzeyde, önceki veya gelecekteki toplu işlemdeki sağlıksız örnekler, daha yüksek güvenilirlik sağlamak amacıyla toplu işteki örneklerin yüzdesine neden olabilir.</span><span class="sxs-lookup"><span data-stu-id="52d2d-169">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="52d2d-170">Değer belirtilmezse, 20 olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="52d2d-170">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d2d-171">-Maxunhealthyınstancepercent</span><span class="sxs-lookup"><span data-stu-id="52d2d-171">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="52d2d-172">Ölçek kümesindeki toplam sanal makine örneklerinin, yükseltilme sonucu olarak, yükseltme sonucu olan veya çalışırken yükseltme iptal edilmeden önce sanal makine durumu denetimleri tarafından sağlıksız bir durumda bulunabildiği en yüksek oranı.</span><span class="sxs-lookup"><span data-stu-id="52d2d-172">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="52d2d-173">Bu kısıtlama, toplu işlem başlatılmadan önce işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="52d2d-173">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="52d2d-174">Değer belirtilmezse, 20 olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="52d2d-174">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d2d-175">-Maxunhealthyyükseltildi Dedınstancepercent</span><span class="sxs-lookup"><span data-stu-id="52d2d-175">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="52d2d-176">Sağlıksız durumda olabilecek en yüksek yükseltilmiş sanal makine örneği yüzdesi.</span><span class="sxs-lookup"><span data-stu-id="52d2d-176">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="52d2d-177">Bu denetim her toplu iş yükseltildikten sonra gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="52d2d-177">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="52d2d-178">Bu yüzde aşılırsa, çalışırken güncelleştirme iptal edilir.</span><span class="sxs-lookup"><span data-stu-id="52d2d-178">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="52d2d-179">Değer belirtilmezse, 20 olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="52d2d-179">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d2d-180">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="52d2d-180">-OsDiskCaching</span></span>
<span data-ttu-id="52d2d-181">İşletim sistemi diskinin önbelleğe alma modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="52d2d-181">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="52d2d-182">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="52d2d-182">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="52d2d-183">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="52d2d-183">None</span></span>
- <span data-ttu-id="52d2d-184">Özelliğinin</span><span class="sxs-lookup"><span data-stu-id="52d2d-184">ReadOnly</span></span>
- <span data-ttu-id="52d2d-185">Yazma</span><span class="sxs-lookup"><span data-stu-id="52d2d-185">ReadWrite</span></span>

<span data-ttu-id="52d2d-186">Varsayılan değer ReadWrite değeridir.</span><span class="sxs-lookup"><span data-stu-id="52d2d-186">The default value is ReadWrite.</span></span>
<span data-ttu-id="52d2d-187">Önbellek değerini değiştirirseniz cmdlet sanal makineyi yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="52d2d-187">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>

<span data-ttu-id="52d2d-188">Bu ayar, diskin tutarlılığını ve performansını etkiler.</span><span class="sxs-lookup"><span data-stu-id="52d2d-188">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d2d-189">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="52d2d-189">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="52d2d-190">İşletim sistemi diskinde WriteAccelerator 'in etkinleştirilip etkinleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="52d2d-190">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d2d-191">-Overprovision</span><span class="sxs-lookup"><span data-stu-id="52d2d-191">-Overprovision</span></span>
<span data-ttu-id="52d2d-192">Cmdlet 'in VMSS 'yi içerip içermediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="52d2d-192">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d2d-193">-Pausetimebetweentoplu Işler</span><span class="sxs-lookup"><span data-stu-id="52d2d-193">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="52d2d-194">Bir toplu işteki tüm sanal makinelerin güncelleştirmesini tamamlama ve sonraki toplu işlemi başlatma arasındaki bekleme süresi.</span><span class="sxs-lookup"><span data-stu-id="52d2d-194">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="52d2d-195">Süre ISO 8601 biçiminde belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="52d2d-195">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="52d2d-196">Varsayılan değer 0 saniyedir (PT0S).</span><span class="sxs-lookup"><span data-stu-id="52d2d-196">The default value is 0 seconds (PT0S).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d2d-197">-PlanName</span><span class="sxs-lookup"><span data-stu-id="52d2d-197">-PlanName</span></span>
<span data-ttu-id="52d2d-198">Plan adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="52d2d-198">Specifies the plan name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d2d-199">-Planürün</span><span class="sxs-lookup"><span data-stu-id="52d2d-199">-PlanProduct</span></span>
<span data-ttu-id="52d2d-200">Plan ürünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="52d2d-200">Specifies the plan product.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d2d-201">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="52d2d-201">-PlanPromotionCode</span></span>
<span data-ttu-id="52d2d-202">Plan promosyon kodunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="52d2d-202">Specifies the plan promotion code.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d2d-203">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="52d2d-203">-PlanPublisher</span></span>
<span data-ttu-id="52d2d-204">Publisher planı 'nı belirtir.</span><span class="sxs-lookup"><span data-stu-id="52d2d-204">Specifies the plan publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d2d-205">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="52d2d-205">-ProvisionVMAgent</span></span>
<span data-ttu-id="52d2d-206">VMSS 'deki Windows sanal makinelerinde sanal makine aracısının sağlanması gerekip gerekmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="52d2d-206">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d2d-207">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52d2d-207">-ResourceGroupName</span></span>
<span data-ttu-id="52d2d-208">VMSS 'nin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="52d2d-208">Specifies the name of the resource group the VMSS belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52d2d-209">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="52d2d-209">-SinglePlacementGroup</span></span>
<span data-ttu-id="52d2d-210">Tek yerleşim grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="52d2d-210">Specifies the single placement group.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d2d-211">-Skukapasitesi</span><span class="sxs-lookup"><span data-stu-id="52d2d-211">-SkuCapacity</span></span>
<span data-ttu-id="52d2d-212">VMSS 'deki örneklerin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="52d2d-212">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d2d-213">-SkuName</span><span class="sxs-lookup"><span data-stu-id="52d2d-213">-SkuName</span></span>
<span data-ttu-id="52d2d-214">Tüm VMSS örneklerinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="52d2d-214">Specifies the size of all the instances of VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d2d-215">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="52d2d-215">-SkuTier</span></span>
<span data-ttu-id="52d2d-216">VMSS 'nin katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="52d2d-216">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="52d2d-217">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="52d2d-217">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="52d2d-218">Ardından</span><span class="sxs-lookup"><span data-stu-id="52d2d-218">Standard</span></span>
- <span data-ttu-id="52d2d-219">Ana</span><span class="sxs-lookup"><span data-stu-id="52d2d-219">Basic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d2d-220">Etiketli</span><span class="sxs-lookup"><span data-stu-id="52d2d-220">-Tag</span></span>
<span data-ttu-id="52d2d-221">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="52d2d-221">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="52d2d-222">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="52d2d-222">For example:</span></span>

<span data-ttu-id="52d2d-223">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="52d2d-223">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d2d-224">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="52d2d-224">-TimeZone</span></span>
<span data-ttu-id="52d2d-225">Windows işletim sisteminin saat dilimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="52d2d-225">Specifies the time zone for Windows OS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d2d-226">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="52d2d-226">-UpgradePolicyMode</span></span>
<span data-ttu-id="52d2d-227">Belirtilen ölçek kümesindeki sanal makinelere yükseltme modu.</span><span class="sxs-lookup"><span data-stu-id="52d2d-227">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="52d2d-228">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="52d2d-228">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="52d2d-229">Otomatik</span><span class="sxs-lookup"><span data-stu-id="52d2d-229">Automatic</span></span>
- <span data-ttu-id="52d2d-230">El ile</span><span class="sxs-lookup"><span data-stu-id="52d2d-230">Manual</span></span>
- <span data-ttu-id="52d2d-231">Melerdeki</span><span class="sxs-lookup"><span data-stu-id="52d2d-231">Rolling</span></span>

```yaml
Type: UpgradeMode
Parameter Sets: (All)
Aliases: 
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d2d-232">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="52d2d-232">-VhdContainer</span></span>
<span data-ttu-id="52d2d-233">VMSS işletim sistemi disklerini depolamak için kullanılan kapsayıcı URL 'Lerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="52d2d-233">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d2d-234">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="52d2d-234">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="52d2d-235">Yerel bir VMSS nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="52d2d-235">Specifies a local VMSS object.</span></span>
<span data-ttu-id="52d2d-236">Bir VMSS nesnesi edinmek için Get-AzureRmVmss cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="52d2d-236">To obtain a VMSS object, use the Get-AzureRmVmss cmdlet.</span></span>
<span data-ttu-id="52d2d-237">Bu sanal makine nesnesi, VMSS 'nin güncelleştirilmiş durumunu içerir.</span><span class="sxs-lookup"><span data-stu-id="52d2d-237">This virtual machine object contains the updated state for the VMSS.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52d2d-238">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="52d2d-238">-VMScaleSetName</span></span>
<span data-ttu-id="52d2d-239">Bu cmdlet 'in oluşturduğu VMSS 'nin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="52d2d-239">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52d2d-240">-Onay</span><span class="sxs-lookup"><span data-stu-id="52d2d-240">-Confirm</span></span>
<span data-ttu-id="52d2d-241">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="52d2d-241">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d2d-242">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52d2d-242">-WhatIf</span></span>
<span data-ttu-id="52d2d-243">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="52d2d-243">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="52d2d-244">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="52d2d-244">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52d2d-245">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52d2d-245">CommonParameters</span></span>
<span data-ttu-id="52d2d-246">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="52d2d-246">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52d2d-247">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52d2d-247">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52d2d-248">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="52d2d-248">INPUTS</span></span>

### <span data-ttu-id="52d2d-249">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="52d2d-249">VirtualMachineScaleSet</span></span>
<span data-ttu-id="52d2d-250">' VirtualMachineScaleSet ' parametresi ardışık düzen için ' VirtualMachineScaleSet ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="52d2d-250">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="52d2d-251">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="52d2d-251">OUTPUTS</span></span>

### <span data-ttu-id="52d2d-252">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="52d2d-252">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="52d2d-253">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="52d2d-253">NOTES</span></span>

## <span data-ttu-id="52d2d-254">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="52d2d-254">RELATED LINKS</span></span>

[<span data-ttu-id="52d2d-255">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="52d2d-255">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="52d2d-256">Yeni-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="52d2d-256">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="52d2d-257">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="52d2d-257">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="52d2d-258">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="52d2d-258">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="52d2d-259">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="52d2d-259">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="52d2d-260">Başlangıç-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="52d2d-260">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="52d2d-261">Dur-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="52d2d-261">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)


