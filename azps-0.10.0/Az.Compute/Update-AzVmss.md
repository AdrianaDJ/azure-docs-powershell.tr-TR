---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: 5e3bafbc667cc0e26eb6469e681ca9355b4f307f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936805"
---
# <span data-ttu-id="8a058-101">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8a058-101">Update-AzVmss</span></span>

## <span data-ttu-id="8a058-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a058-102">SYNOPSIS</span></span>
<span data-ttu-id="8a058-103">Bir VMSUBNET 'in durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="8a058-103">Updates the state of a VMSS.</span></span>

## <span data-ttu-id="8a058-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8a058-104">SYNTAX</span></span>

### <span data-ttu-id="8a058-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8a058-105">DefaultParameter (Default)</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
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

### <span data-ttu-id="8a058-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a058-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
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

## <span data-ttu-id="8a058-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8a058-107">DESCRIPTION</span></span>
<span data-ttu-id="8a058-108">**Update-AzVmss** cmdlet 'ı sanal makine ölçek kümesi 'nın (VMSS) durumunu yerel BIR VMSS nesnesinin durumuna güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="8a058-108">The **Update-AzVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="8a058-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8a058-109">EXAMPLES</span></span>

### <span data-ttu-id="8a058-110">Örnek 1: bir VMSS durumunu yerel bir VMSS nesnesinin durumuna güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="8a058-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="8a058-111">Bu komut, Group001 adındaki kaynak grubuna ait olan VMSS001 adındaki VMSS 'nin durumunu yerel bir VMSS nesnesinin durumuna güncelleştirir $LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="8a058-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="8a058-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8a058-112">PARAMETERS</span></span>

### <span data-ttu-id="8a058-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="8a058-113">-AsJob</span></span>
<span data-ttu-id="8a058-114">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="8a058-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="8a058-115">-Automaticosupgrad</span><span class="sxs-lookup"><span data-stu-id="8a058-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="8a058-116">Resmin daha yeni bir sürümü kullanılabilir hale geldiğinde, bir yerde ölçeklendirme kümesi örneklerine otomatik olarak işletim sistemi yükseltmeleri uygulanıp uygulanmayacağı.</span><span class="sxs-lookup"><span data-stu-id="8a058-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="8a058-117">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="8a058-117">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="8a058-118">Sanal makine ölçek kümesinde önyükleme tanılaması 'nın etkinleştirilmesi gerekip gerekmediği.</span><span class="sxs-lookup"><span data-stu-id="8a058-118">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="8a058-119">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="8a058-119">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="8a058-120">Konsol çıkışını ve ekran görüntüsünü yerleştirmek için kullanılacak depolama hesabının URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="8a058-120">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="8a058-121">-CustomData</span><span class="sxs-lookup"><span data-stu-id="8a058-121">-CustomData</span></span>
<span data-ttu-id="8a058-122">Özel verilerin Base-64 kodlu dizesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a058-122">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="8a058-123">Bu, sanal makinede dosya olarak kaydedilmiş bir ikili diziye çözülür.</span><span class="sxs-lookup"><span data-stu-id="8a058-123">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="8a058-124">İkili dizinin en fazla uzunluğu 65535 bayttır.</span><span class="sxs-lookup"><span data-stu-id="8a058-124">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="8a058-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a058-125">-DefaultProfile</span></span>
<span data-ttu-id="8a058-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8a058-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a058-127">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="8a058-127">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="8a058-128">Bu cmdlet 'in Linux OS için parola kimlik doğrulamasını devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8a058-128">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

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

### <span data-ttu-id="8a058-129">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="8a058-129">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="8a058-130">VMSS 'deki Windows sanal makinelerinin otomatik güncelleştirmeler için etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="8a058-130">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="8a058-131">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="8a058-131">-IdentityId</span></span>
<span data-ttu-id="8a058-132">Sanal makine ölçek kümesiyle ilişkili kullanıcı kimliklerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a058-132">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="8a058-133">Kullanıcı kimliği başvuruları formda ARM kaynak kimlikleri olacaktır: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="8a058-133">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="8a058-134">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="8a058-134">-IdentityType</span></span>
<span data-ttu-id="8a058-135">Sanal makine ölçek kümesi için kullanılan kimlik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a058-135">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="8a058-136">' Systemassigneduserın ' türü, örtülü olarak oluşturulmuş bir kimlik ve Kullanıcı tarafından atanan kimlikler kümesini içerir.</span><span class="sxs-lookup"><span data-stu-id="8a058-136">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="8a058-137">' None ' türü, sanal makine ölçek kümesindeki tüm kimlikleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8a058-137">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="8a058-138">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="8a058-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8a058-139">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="8a058-139">SystemAssigned</span></span>
- <span data-ttu-id="8a058-140">Kullanıcı tarafından atanmış</span><span class="sxs-lookup"><span data-stu-id="8a058-140">UserAssigned</span></span>
- <span data-ttu-id="8a058-141">Systemassigneduseratandı</span><span class="sxs-lookup"><span data-stu-id="8a058-141">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="8a058-142">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="8a058-142">None</span></span>

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

### <span data-ttu-id="8a058-143">-Imagereferenceıd</span><span class="sxs-lookup"><span data-stu-id="8a058-143">-ImageReferenceId</span></span>
<span data-ttu-id="8a058-144">Resim başvuru KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a058-144">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="8a058-145">-Imagereferenceteklif</span><span class="sxs-lookup"><span data-stu-id="8a058-145">-ImageReferenceOffer</span></span>
<span data-ttu-id="8a058-146">Sanal makine görüntüsünün (Vmımage) teklifinin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a058-146">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="8a058-147">Resim teklifi edinmek için Get-AzVMImageOffer cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8a058-147">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="8a058-148">-Imagereferencepublisher</span><span class="sxs-lookup"><span data-stu-id="8a058-148">-ImageReferencePublisher</span></span>
<span data-ttu-id="8a058-149">Vmımage yayımcısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a058-149">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="8a058-150">Yayımcı edinmek için Get-AzVMImagePublisher cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8a058-150">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="8a058-151">-Imagereferencesku</span><span class="sxs-lookup"><span data-stu-id="8a058-151">-ImageReferenceSku</span></span>
<span data-ttu-id="8a058-152">VMImage SKU 'SU belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a058-152">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="8a058-153">STB 'ler almak için Get-AzVMImageSku cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8a058-153">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="8a058-154">-Imagereferenceversion</span><span class="sxs-lookup"><span data-stu-id="8a058-154">-ImageReferenceVersion</span></span>
<span data-ttu-id="8a058-155">VMImage sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a058-155">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="8a058-156">En son sürümü kullanmak için belirli bir sürüm yerine en son sürümünü belirtin.</span><span class="sxs-lookup"><span data-stu-id="8a058-156">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="8a058-157">-Imageurı</span><span class="sxs-lookup"><span data-stu-id="8a058-157">-ImageUri</span></span>
<span data-ttu-id="8a058-158">Kullanıcı görüntüsü için blob URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a058-158">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="8a058-159">VMSS, Kullanıcı görüntüsünün aynı kapsayıcısında bir işletim sistemi diski oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8a058-159">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="8a058-160">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="8a058-160">-LicenseType</span></span>
<span data-ttu-id="8a058-161">Kendi lisans senaryonuzu verecek lisans türünü belirtin.</span><span class="sxs-lookup"><span data-stu-id="8a058-161">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="8a058-162">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="8a058-162">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="8a058-163">Yönetilen disk için depolama hesabı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a058-163">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="8a058-164">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="8a058-164">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8a058-165">Standartlrs</span><span class="sxs-lookup"><span data-stu-id="8a058-165">StandardLRS</span></span>
- <span data-ttu-id="8a058-166">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="8a058-166">PremiumLRS</span></span>

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

### <span data-ttu-id="8a058-167">-Maxbatchınstancepercent</span><span class="sxs-lookup"><span data-stu-id="8a058-167">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="8a058-168">Tek bir toplu işlemde çalışırken yükseltme tarafından aynı anda Yükseltilecek toplam sanal makine örneklerinin en yüksek yüzdesi.</span><span class="sxs-lookup"><span data-stu-id="8a058-168">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="8a058-169">Bu en yüksek düzeyde, önceki veya gelecekteki toplu işlemdeki sağlıksız örnekler, daha yüksek güvenilirlik sağlamak amacıyla toplu işteki örneklerin yüzdesine neden olabilir.</span><span class="sxs-lookup"><span data-stu-id="8a058-169">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="8a058-170">Değer belirtilmezse, 20 olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="8a058-170">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="8a058-171">-Maxunhealthyınstancepercent</span><span class="sxs-lookup"><span data-stu-id="8a058-171">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="8a058-172">Ölçek kümesindeki toplam sanal makine örneklerinin, yükseltilme sonucu olarak, yükseltme sonucu olan veya çalışırken yükseltme iptal edilmeden önce sanal makine durumu denetimleri tarafından sağlıksız bir durumda bulunabildiği en yüksek oranı.</span><span class="sxs-lookup"><span data-stu-id="8a058-172">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="8a058-173">Bu kısıtlama, toplu işlem başlatılmadan önce işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="8a058-173">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="8a058-174">Değer belirtilmezse, 20 olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="8a058-174">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="8a058-175">-Maxunhealthyyükseltildi Dedınstancepercent</span><span class="sxs-lookup"><span data-stu-id="8a058-175">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="8a058-176">Sağlıksız durumda olabilecek en yüksek yükseltilmiş sanal makine örneği yüzdesi.</span><span class="sxs-lookup"><span data-stu-id="8a058-176">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="8a058-177">Bu denetim her toplu iş yükseltildikten sonra gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="8a058-177">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="8a058-178">Bu yüzde aşılırsa, çalışırken güncelleştirme iptal edilir.</span><span class="sxs-lookup"><span data-stu-id="8a058-178">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="8a058-179">Değer belirtilmezse, 20 olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="8a058-179">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="8a058-180">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="8a058-180">-OsDiskCaching</span></span>
<span data-ttu-id="8a058-181">İşletim sistemi diskinin önbelleğe alma modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a058-181">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="8a058-182">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="8a058-182">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8a058-183">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="8a058-183">None</span></span>
- <span data-ttu-id="8a058-184">Özelliğinin</span><span class="sxs-lookup"><span data-stu-id="8a058-184">ReadOnly</span></span>
- <span data-ttu-id="8a058-185">Yazma</span><span class="sxs-lookup"><span data-stu-id="8a058-185">ReadWrite</span></span>

<span data-ttu-id="8a058-186">Varsayılan değer ReadWrite değeridir.</span><span class="sxs-lookup"><span data-stu-id="8a058-186">The default value is ReadWrite.</span></span>
<span data-ttu-id="8a058-187">Önbellek değerini değiştirirseniz cmdlet sanal makineyi yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="8a058-187">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>

<span data-ttu-id="8a058-188">Bu ayar, diskin tutarlılığını ve performansını etkiler.</span><span class="sxs-lookup"><span data-stu-id="8a058-188">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="8a058-189">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="8a058-189">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="8a058-190">İşletim sistemi diskinde WriteAccelerator 'in etkinleştirilip etkinleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a058-190">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="8a058-191">-Overprovision</span><span class="sxs-lookup"><span data-stu-id="8a058-191">-Overprovision</span></span>
<span data-ttu-id="8a058-192">Cmdlet 'in VMSS 'yi içerip içermediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="8a058-192">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="8a058-193">-Pausetimebetweentoplu Işler</span><span class="sxs-lookup"><span data-stu-id="8a058-193">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="8a058-194">Bir toplu işteki tüm sanal makinelerin güncelleştirmesini tamamlama ve sonraki toplu işlemi başlatma arasındaki bekleme süresi.</span><span class="sxs-lookup"><span data-stu-id="8a058-194">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="8a058-195">Süre ISO 8601 biçiminde belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="8a058-195">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="8a058-196">Varsayılan değer 0 saniyedir (PT0S).</span><span class="sxs-lookup"><span data-stu-id="8a058-196">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="8a058-197">-PlanName</span><span class="sxs-lookup"><span data-stu-id="8a058-197">-PlanName</span></span>
<span data-ttu-id="8a058-198">Plan adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a058-198">Specifies the plan name.</span></span>

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

### <span data-ttu-id="8a058-199">-Planürün</span><span class="sxs-lookup"><span data-stu-id="8a058-199">-PlanProduct</span></span>
<span data-ttu-id="8a058-200">Plan ürünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a058-200">Specifies the plan product.</span></span>

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

### <span data-ttu-id="8a058-201">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="8a058-201">-PlanPromotionCode</span></span>
<span data-ttu-id="8a058-202">Plan promosyon kodunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a058-202">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="8a058-203">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="8a058-203">-PlanPublisher</span></span>
<span data-ttu-id="8a058-204">Publisher planı 'nı belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a058-204">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="8a058-205">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="8a058-205">-ProvisionVMAgent</span></span>
<span data-ttu-id="8a058-206">VMSS 'deki Windows sanal makinelerinde sanal makine aracısının sağlanması gerekip gerekmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="8a058-206">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="8a058-207">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a058-207">-ResourceGroupName</span></span>
<span data-ttu-id="8a058-208">VMSS 'nin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a058-208">Specifies the name of the resource group the VMSS belongs to.</span></span>

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

### <span data-ttu-id="8a058-209">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="8a058-209">-SinglePlacementGroup</span></span>
<span data-ttu-id="8a058-210">Tek yerleşim grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a058-210">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="8a058-211">-Skukapasitesi</span><span class="sxs-lookup"><span data-stu-id="8a058-211">-SkuCapacity</span></span>
<span data-ttu-id="8a058-212">VMSS 'deki örneklerin sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a058-212">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="8a058-213">-SkuName</span><span class="sxs-lookup"><span data-stu-id="8a058-213">-SkuName</span></span>
<span data-ttu-id="8a058-214">Tüm VMSS örneklerinin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a058-214">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="8a058-215">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="8a058-215">-SkuTier</span></span>
<span data-ttu-id="8a058-216">VMSS 'nin katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a058-216">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="8a058-217">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="8a058-217">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8a058-218">Ardından</span><span class="sxs-lookup"><span data-stu-id="8a058-218">Standard</span></span>
- <span data-ttu-id="8a058-219">Ana</span><span class="sxs-lookup"><span data-stu-id="8a058-219">Basic</span></span>

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

### <span data-ttu-id="8a058-220">Etiketli</span><span class="sxs-lookup"><span data-stu-id="8a058-220">-Tag</span></span>
<span data-ttu-id="8a058-221">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="8a058-221">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8a058-222">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="8a058-222">For example:</span></span>

<span data-ttu-id="8a058-223">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="8a058-223">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="8a058-224">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="8a058-224">-TimeZone</span></span>
<span data-ttu-id="8a058-225">Windows işletim sisteminin saat dilimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a058-225">Specifies the time zone for Windows OS.</span></span>

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

### <span data-ttu-id="8a058-226">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="8a058-226">-UpgradePolicyMode</span></span>
<span data-ttu-id="8a058-227">Belirtilen ölçek kümesindeki sanal makinelere yükseltme modu.</span><span class="sxs-lookup"><span data-stu-id="8a058-227">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="8a058-228">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="8a058-228">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8a058-229">Otomatik</span><span class="sxs-lookup"><span data-stu-id="8a058-229">Automatic</span></span>
- <span data-ttu-id="8a058-230">El ile</span><span class="sxs-lookup"><span data-stu-id="8a058-230">Manual</span></span>
- <span data-ttu-id="8a058-231">Melerdeki</span><span class="sxs-lookup"><span data-stu-id="8a058-231">Rolling</span></span>

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

### <span data-ttu-id="8a058-232">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="8a058-232">-VhdContainer</span></span>
<span data-ttu-id="8a058-233">VMSS işletim sistemi disklerini depolamak için kullanılan kapsayıcı URL 'Lerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a058-233">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="8a058-234">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8a058-234">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="8a058-235">Yerel bir VMSS nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a058-235">Specifies a local VMSS object.</span></span>
<span data-ttu-id="8a058-236">Bir VMSS nesnesi edinmek için Get-AzVmss cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8a058-236">To obtain a VMSS object, use the Get-AzVmss cmdlet.</span></span>
<span data-ttu-id="8a058-237">Bu sanal makine nesnesi, VMSS 'nin güncelleştirilmiş durumunu içerir.</span><span class="sxs-lookup"><span data-stu-id="8a058-237">This virtual machine object contains the updated state for the VMSS.</span></span>

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

### <span data-ttu-id="8a058-238">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="8a058-238">-VMScaleSetName</span></span>
<span data-ttu-id="8a058-239">Bu cmdlet 'in oluşturduğu VMSS 'nin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a058-239">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="8a058-240">-Onay</span><span class="sxs-lookup"><span data-stu-id="8a058-240">-Confirm</span></span>
<span data-ttu-id="8a058-241">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8a058-241">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a058-242">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a058-242">-WhatIf</span></span>
<span data-ttu-id="8a058-243">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8a058-243">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="8a058-244">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8a058-244">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a058-245">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a058-245">CommonParameters</span></span>
<span data-ttu-id="8a058-246">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8a058-246">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a058-247">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a058-247">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a058-248">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8a058-248">INPUTS</span></span>

### <span data-ttu-id="8a058-249">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8a058-249">VirtualMachineScaleSet</span></span>
<span data-ttu-id="8a058-250">' VirtualMachineScaleSet ' parametresi ardışık düzen için ' VirtualMachineScaleSet ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="8a058-250">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="8a058-251">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8a058-251">OUTPUTS</span></span>

### <span data-ttu-id="8a058-252">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8a058-252">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="8a058-253">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8a058-253">NOTES</span></span>

## <span data-ttu-id="8a058-254">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8a058-254">RELATED LINKS</span></span>

[<span data-ttu-id="8a058-255">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8a058-255">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="8a058-256">Yeni-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8a058-256">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="8a058-257">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8a058-257">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="8a058-258">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8a058-258">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="8a058-259">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8a058-259">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="8a058-260">Başlangıç-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8a058-260">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="8a058-261">Dur-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8a058-261">Stop-AzVmss</span></span>](./Stop-AzVmss.md)


