---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C71C486E-34EB-42B5-B38A-D85B7DAA2F74
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
ms.openlocfilehash: 54a5d6dc737bc0bd6a7f1d236ce855b2a08dca6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594964"
---
# <span data-ttu-id="bc7db-101">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="bc7db-101">New-AzureBatchPool</span></span>

## <span data-ttu-id="bc7db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc7db-102">SYNOPSIS</span></span>
<span data-ttu-id="bc7db-103">Toplu Iş hizmetinde havuz oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bc7db-103">Creates a pool in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc7db-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bc7db-104">SYNTAX</span></span>

### <span data-ttu-id="bc7db-105">Cloudserviceandtargetadanmış (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bc7db-105">CloudServiceAndTargetDedicated (Default)</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-ResizeTimeout <TimeSpan>] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
 [-MaxTasksPerComputeNode <Int32>] [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 [-UserAccount <PSUserAccount[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc7db-106">Virtualmachineandtargetadanmış</span><span class="sxs-lookup"><span data-stu-id="bc7db-106">VirtualMachineAndTargetDedicated</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-ResizeTimeout <TimeSpan>] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
 [-MaxTasksPerComputeNode <Int32>] [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] [-UserAccount <PSUserAccount[]>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bc7db-107">CloudServiceAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="bc7db-107">CloudServiceAndAutoScale</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 [-UserAccount <PSUserAccount[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc7db-108">VirtualMachineAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="bc7db-108">VirtualMachineAndAutoScale</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] [-UserAccount <PSUserAccount[]>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bc7db-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="bc7db-109">DESCRIPTION</span></span>
<span data-ttu-id="bc7db-110">**New-AzureBatchPool** cmdlet 'ı, *batchcontext* parametresinde belirtilen hesap altında Azure Batch hizmetinde bir havuz oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bc7db-110">The **New-AzureBatchPool** cmdlet creates a pool in the Azure Batch service under the account specified by the *BatchContext* parameter.</span></span>

## <span data-ttu-id="bc7db-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bc7db-111">EXAMPLES</span></span>

### <span data-ttu-id="bc7db-112">Örnek 1: Targetadanmış parametre kümesini kullanarak yeni havuz oluşturma</span><span class="sxs-lookup"><span data-stu-id="bc7db-112">Example 1: Create a new pool using the TargetDedicated parameter set</span></span>
```
PS C:\>New-AzureBatchPool -Id "MyPool" -VirtualMachineSize "Small" -OSFamily "4" -TargetOSVersion "*" -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

<span data-ttu-id="bc7db-113">Bu komut, Targetadanmış parametre kümesini kullanarak KIMLIĞI MyPool ile yeni bir havuz oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bc7db-113">This command creates a new pool with ID MyPool using the TargetDedicated parameter set.</span></span>
<span data-ttu-id="bc7db-114">Hedef ayırma üç COMPUTE düğümlerdir.</span><span class="sxs-lookup"><span data-stu-id="bc7db-114">The target allocation is three compute nodes.</span></span>
<span data-ttu-id="bc7db-115">Havuz, Aile dörtte en son işletim sistemi sürümüyle görüntülü küçük sanal makineleri kullanacak şekilde yapılandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="bc7db-115">The pool is configured to use small virtual machines imaged with the latest operating system version of family four.</span></span>

### <span data-ttu-id="bc7db-116">Örnek 2: otomatik ölçeklendirme parametre kümesini kullanarak yeni havuz oluşturma</span><span class="sxs-lookup"><span data-stu-id="bc7db-116">Example 2: Create a new pool using the AutoScale parameter set</span></span>
```
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -OSFamily "4" -TargetOSVersion "*" -AutoScaleFormula '$TargetDedicated=2;' -BatchContext $Context
```

<span data-ttu-id="bc7db-117">Bu komut otomatik ölçeklendirme parametre kümesini kullanarak KIMLIK AutoScalePool ile yeni bir havuz oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bc7db-117">This command creates a new pool with ID AutoScalePool using the AutoScale parameter set.</span></span>
<span data-ttu-id="bc7db-118">Havuz, Aile dördünü en son işletim sistemi sürümü ile görüntülü küçük sanal makineleri kullanacak şekilde yapılandırılmıştır ve hedef sayısı, otomatik ölçeklendirme formülüyle belirlenir.</span><span class="sxs-lookup"><span data-stu-id="bc7db-118">The pool is configured to use small virtual machines imaged with the latest operating system version of family four, and the target number of compute nodes are determined by the Autoscale formula.</span></span>

### <span data-ttu-id="bc7db-119">Örnek 3: alt ağda düğümleri bulunan havuz oluşturma</span><span class="sxs-lookup"><span data-stu-id="bc7db-119">Example 3: Create a pool with nodes in a subnet</span></span>
```
PS C:\>$networkConfig = New-Object Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration
PS C:\>$networkConfig.SubnetId = "/subscriptions/{subscription}/resourceGroups/{group}/providers/{provider}/virtualNetworks/{network}/subnets/{subnet}"
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -OSFamily "4" -TargetDedicatedComputeNodes 3 -NetworkConfiguration $networkConfig -BatchContext $Context
```

### <span data-ttu-id="bc7db-120">Örnek 4: özel kullanıcı hesaplarıyla havuz oluşturma</span><span class="sxs-lookup"><span data-stu-id="bc7db-120">Example 4: Create a pool with custom user accounts</span></span>
```
PS C:\>$userAccount = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserAccount -ArgumentList @("myaccount", "mypassword")
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -OSFamily "4" -TargetDedicatedComputeNodes 3 -UserAccount $userAccount
```

## <span data-ttu-id="bc7db-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bc7db-121">PARAMETERS</span></span>

### <span data-ttu-id="bc7db-122">-Applicationlisansları</span><span class="sxs-lookup"><span data-stu-id="bc7db-122">-ApplicationLicenses</span></span>
<span data-ttu-id="bc7db-123">Toplu hizmet, havuzdaki her bir işlem düğümünde kullanılabilir olacak uygulama lisanslarının listesi.</span><span class="sxs-lookup"><span data-stu-id="bc7db-123">The list of application licenses the Batch service will make available on each compute node in the pool.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: ApplicationLicense

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc7db-124">-Applicationpackagereferfer</span><span class="sxs-lookup"><span data-stu-id="bc7db-124">-ApplicationPackageReferences</span></span>
```yaml
Type: PSApplicationPackageReference[]
Parameter Sets: (All)
Aliases: ApplicationPackageReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc7db-125">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="bc7db-125">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="bc7db-126">Havuz boyutu otomatik ölçeklendirme formülüne göre otomatik olarak düzeltilecek kadar geçen süreyi dakika cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc7db-126">Specifies the amount of time, in minutes, that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="bc7db-127">Varsayılan değer 15 dakikadır ve en az değer 5 dakikadır.</span><span class="sxs-lookup"><span data-stu-id="bc7db-127">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: CloudServiceAndAutoScale, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc7db-128">-Otomatik ölçek formülü</span><span class="sxs-lookup"><span data-stu-id="bc7db-128">-AutoScaleFormula</span></span>
<span data-ttu-id="bc7db-129">Havuzu otomatik olarak ölçeklendirme formülünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc7db-129">Specifies the formula for automatically scaling the pool.</span></span>

```yaml
Type: String
Parameter Sets: CloudServiceAndAutoScale, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc7db-130">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="bc7db-130">-BatchContext</span></span>
<span data-ttu-id="bc7db-131">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc7db-131">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="bc7db-132">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="bc7db-132">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="bc7db-133">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="bc7db-133">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="bc7db-134">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="bc7db-134">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="bc7db-135">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="bc7db-135">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc7db-136">-Certificatereferde</span><span class="sxs-lookup"><span data-stu-id="bc7db-136">-CertificateReferences</span></span>
<span data-ttu-id="bc7db-137">Havuz ile ilişkili sertifikaları belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc7db-137">Specifies certificates associated with the pool.</span></span>
<span data-ttu-id="bc7db-138">Toplu Iş hizmeti, havuzun her bir COMPUTE düğümüne başvurulan sertifikaları yükler.</span><span class="sxs-lookup"><span data-stu-id="bc7db-138">The Batch service installs the referenced certificates on each compute node of the pool.</span></span>

```yaml
Type: PSCertificateReference[]
Parameter Sets: (All)
Aliases: CertificateReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc7db-139">-CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="bc7db-139">-CloudServiceConfiguration</span></span>
<span data-ttu-id="bc7db-140">Azure bulut hizmeti platformuna dayalı bir havuzun yapılandırma ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc7db-140">Specifies configuration settings for a pool based on the Azure cloud service platform.</span></span>

```yaml
Type: PSCloudServiceConfiguration
Parameter Sets: CloudServiceAndTargetDedicated, CloudServiceAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc7db-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc7db-141">-DefaultProfile</span></span>
<span data-ttu-id="bc7db-142">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bc7db-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc7db-143">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="bc7db-143">-DisplayName</span></span>
<span data-ttu-id="bc7db-144">Havuzun görünen adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc7db-144">Specifies the display name of the pool.</span></span>

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

### <span data-ttu-id="bc7db-145">-ID</span><span class="sxs-lookup"><span data-stu-id="bc7db-145">-Id</span></span>
<span data-ttu-id="bc7db-146">Oluşturulacak havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc7db-146">Specifies the ID of the pool to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc7db-147">-Intercomputenodecommunicationenabled</span><span class="sxs-lookup"><span data-stu-id="bc7db-147">-InterComputeNodeCommunicationEnabled</span></span>
<span data-ttu-id="bc7db-148">Bu cmdlet 'in adanmış işlem düğümleri arasında doğrudan iletişim için havuzu ayarlamadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bc7db-148">Indicates that this cmdlet sets up the pool for direct communication between dedicated compute nodes.</span></span>

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

### <span data-ttu-id="bc7db-149">-MaxTasksPerComputeNode</span><span class="sxs-lookup"><span data-stu-id="bc7db-149">-MaxTasksPerComputeNode</span></span>
<span data-ttu-id="bc7db-150">Tek bir işlem düğümünde çalıştırılabilecek en fazla görev sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc7db-150">Specifies the maximum number of tasks that can run on a single compute node.</span></span>

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

### <span data-ttu-id="bc7db-151">-Metadata</span><span class="sxs-lookup"><span data-stu-id="bc7db-151">-Metadata</span></span>
<span data-ttu-id="bc7db-152">Yeni havuza eklemek için meta verileri anahtar/değer çiftleri olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc7db-152">Specifies the metadata, as key/value pairs, to add to the new pool.</span></span>
<span data-ttu-id="bc7db-153">Anahtar, meta veri adıdır.</span><span class="sxs-lookup"><span data-stu-id="bc7db-153">The key is the metadata name.</span></span>
<span data-ttu-id="bc7db-154">Değer, meta veri değeridir.</span><span class="sxs-lookup"><span data-stu-id="bc7db-154">The value is the metadata value.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc7db-155">-NetworkConfiguration</span><span class="sxs-lookup"><span data-stu-id="bc7db-155">-NetworkConfiguration</span></span>
<span data-ttu-id="bc7db-156">Havuzun ağ yapılandırması.</span><span class="sxs-lookup"><span data-stu-id="bc7db-156">The network configuration for the pool.</span></span>

```yaml
Type: PSNetworkConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc7db-157">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="bc7db-157">-ResizeTimeout</span></span>
<span data-ttu-id="bc7db-158">Havuza işlem düğümleri tahsis etmek için zaman aşımını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc7db-158">Specifies the time-out for allocating compute nodes to the pool.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc7db-159">-StartTask</span><span class="sxs-lookup"><span data-stu-id="bc7db-159">-StartTask</span></span>
<span data-ttu-id="bc7db-160">Havuzun başlangıç görevi belirtimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc7db-160">Specifies the start task specification for the pool.</span></span>
<span data-ttu-id="bc7db-161">Başlangıç görevi, bir hesaplama düğümü havuza katıldığında veya hesaplama düğümü yeniden başlatıldığında veya yeniden başlatıldığında çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="bc7db-161">The start task is run when a compute node joins the pool, or when the compute node is rebooted or reimaged.</span></span>

```yaml
Type: PSStartTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc7db-162">-TARGETTE</span><span class="sxs-lookup"><span data-stu-id="bc7db-162">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="bc7db-163">Havuza ayrılacak adanmış işlem düğümlerinin hedef sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc7db-163">Specifies the target number of dedicated compute nodes to allocate to the pool.</span></span>

```yaml
Type: Int32
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: TargetDedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc7db-164">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="bc7db-164">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="bc7db-165">Havuza ayrılacak düşük öncelikli işlem düğümlerinin hedef sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc7db-165">Specifies the target number of low-priority compute nodes to allocate to the pool.</span></span>

```yaml
Type: Int32
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc7db-166">-TaskSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="bc7db-166">-TaskSchedulingPolicy</span></span>
<span data-ttu-id="bc7db-167">ComputeNodeFillType gibi görev zamanlama ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc7db-167">Specifies the task scheduling policy, such as the ComputeNodeFillType.</span></span>

```yaml
Type: PSTaskSchedulingPolicy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc7db-168">-Kullanıcıhesabı</span><span class="sxs-lookup"><span data-stu-id="bc7db-168">-UserAccount</span></span>
<span data-ttu-id="bc7db-169">Havuzdaki her düğümde oluşturulacak Kullanıcı hesaplarının listesi.</span><span class="sxs-lookup"><span data-stu-id="bc7db-169">The list of user accounts to be created on each node in the pool.</span></span>

```yaml
Type: PSUserAccount[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc7db-170">-VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="bc7db-170">-VirtualMachineConfiguration</span></span>
<span data-ttu-id="bc7db-171">Sanal makineler Altyapısındaki bir havuzun yapılandırma ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc7db-171">Specifies configuration settings for a pool on the virtual machines infrastructure.</span></span>

```yaml
Type: PSVirtualMachineConfiguration
Parameter Sets: VirtualMachineAndTargetDedicated, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc7db-172">-Virtualınines</span><span class="sxs-lookup"><span data-stu-id="bc7db-172">-VirtualMachineSize</span></span>
<span data-ttu-id="bc7db-173">Havuzdaki sanal makinelerin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc7db-173">Specifies the size of the virtual machines in the pool.</span></span>
<span data-ttu-id="bc7db-174">Sanal makine boyutları hakkında daha fazla bilgi için bkz: sanal makinelerin boyutları https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ ( https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) Microsoft Azure sitesinde).</span><span class="sxs-lookup"><span data-stu-id="bc7db-174">For more information about virtual machine sizes, see Sizes for virtual machineshttps://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ (https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) in the Microsoft Azure site.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc7db-175">-Onay</span><span class="sxs-lookup"><span data-stu-id="bc7db-175">-Confirm</span></span>
<span data-ttu-id="bc7db-176">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bc7db-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc7db-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc7db-177">-WhatIf</span></span>
<span data-ttu-id="bc7db-178">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bc7db-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc7db-179">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bc7db-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc7db-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc7db-180">CommonParameters</span></span>
<span data-ttu-id="bc7db-181">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bc7db-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc7db-182">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc7db-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc7db-183">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bc7db-183">INPUTS</span></span>

### <span data-ttu-id="bc7db-184">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="bc7db-184">BatchAccountContext</span></span>
<span data-ttu-id="bc7db-185">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="bc7db-185">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="bc7db-186">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bc7db-186">OUTPUTS</span></span>

## <span data-ttu-id="bc7db-187">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bc7db-187">NOTES</span></span>

## <span data-ttu-id="bc7db-188">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bc7db-188">RELATED LINKS</span></span>

[<span data-ttu-id="bc7db-189">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="bc7db-189">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="bc7db-190">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="bc7db-190">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="bc7db-191">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="bc7db-191">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="bc7db-192">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="bc7db-192">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


