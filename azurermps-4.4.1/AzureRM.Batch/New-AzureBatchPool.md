---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C71C486E-34EB-42B5-B38A-D85B7DAA2F74
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
ms.openlocfilehash: 3a9534ea2fd0f1bcfc17f9eb5df63b25f7760f2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591148"
---
# <span data-ttu-id="58673-101">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="58673-101">New-AzureBatchPool</span></span>

## <span data-ttu-id="58673-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58673-102">SYNOPSIS</span></span>
<span data-ttu-id="58673-103">Toplu Iş hizmetinde havuz oluşturur.</span><span class="sxs-lookup"><span data-stu-id="58673-103">Creates a pool in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58673-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="58673-104">SYNTAX</span></span>

### <span data-ttu-id="58673-105">Cloudserviceandtargetadanmış (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="58673-105">CloudServiceAndTargetDedicated (Default)</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-ResizeTimeout <TimeSpan>] [-TargetDedicated <Int32>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="58673-106">Virtualmachineandtargetadanmış</span><span class="sxs-lookup"><span data-stu-id="58673-106">VirtualMachineAndTargetDedicated</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-ResizeTimeout <TimeSpan>] [-TargetDedicated <Int32>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58673-107">CloudServiceAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="58673-107">CloudServiceAndAutoScale</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="58673-108">VirtualMachineAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="58673-108">VirtualMachineAndAutoScale</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58673-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="58673-109">DESCRIPTION</span></span>
<span data-ttu-id="58673-110">**New-AzureBatchPool** cmdlet 'ı, *batchcontext* parametresinde belirtilen hesap altında Azure Batch hizmetinde bir havuz oluşturur.</span><span class="sxs-lookup"><span data-stu-id="58673-110">The **New-AzureBatchPool** cmdlet creates a pool in the Azure Batch service under the account specified by the *BatchContext* parameter.</span></span>

## <span data-ttu-id="58673-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="58673-111">EXAMPLES</span></span>

### <span data-ttu-id="58673-112">Örnek 1: Targetadanmış parametre kümesini kullanarak yeni havuz oluşturma</span><span class="sxs-lookup"><span data-stu-id="58673-112">Example 1: Create a new pool using the TargetDedicated parameter set</span></span>
```
PS C:\>New-AzureBatchPool -Id "MyPool" -VirtualMachineSize "Small" -OSFamily "4" -TargetOSVersion "*" -TargetDedicated 3 -BatchContext $Context
```

<span data-ttu-id="58673-113">Bu komut, Targetadanmış parametre kümesini kullanarak KIMLIĞI MyPool ile yeni bir havuz oluşturur.</span><span class="sxs-lookup"><span data-stu-id="58673-113">This command creates a new pool with ID MyPool using the TargetDedicated parameter set.</span></span>
<span data-ttu-id="58673-114">Hedef ayırma üç COMPUTE düğümlerdir.</span><span class="sxs-lookup"><span data-stu-id="58673-114">The target allocation is three compute nodes.</span></span>
<span data-ttu-id="58673-115">Havuz, Aile dörtte en son işletim sistemi sürümüyle görüntülü küçük sanal makineleri kullanacak şekilde yapılandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="58673-115">The pool is configured to use small virtual machines imaged with the latest operating system version of family four.</span></span>

### <span data-ttu-id="58673-116">Örnek 2: otomatik ölçeklendirme parametre kümesini kullanarak yeni havuz oluşturma</span><span class="sxs-lookup"><span data-stu-id="58673-116">Example 2: Create a new pool using the AutoScale parameter set</span></span>
```
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -OSFamily "4" -TargetOSVersion "*" -AutoScaleFormula '$TargetDedicated=2;' -BatchContext $Context
```

<span data-ttu-id="58673-117">Bu komut otomatik ölçeklendirme parametre kümesini kullanarak KIMLIK AutoScalePool ile yeni bir havuz oluşturur.</span><span class="sxs-lookup"><span data-stu-id="58673-117">This command creates a new pool with ID AutoScalePool using the AutoScale parameter set.</span></span>
<span data-ttu-id="58673-118">Havuz, Aile dördünü en son işletim sistemi sürümü ile görüntülü küçük sanal makineleri kullanacak şekilde yapılandırılmıştır ve hedef sayısı, otomatik ölçeklendirme formülüyle belirlenir.</span><span class="sxs-lookup"><span data-stu-id="58673-118">The pool is configured to use small virtual machines imaged with the latest operating system version of family four, and the target number of compute nodes are determined by the Autoscale formula.</span></span>

## <span data-ttu-id="58673-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="58673-119">PARAMETERS</span></span>

### <span data-ttu-id="58673-120">-Applicationpackagereferfer</span><span class="sxs-lookup"><span data-stu-id="58673-120">-ApplicationPackageReferences</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58673-121">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="58673-121">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="58673-122">Havuz boyutu otomatik ölçeklendirme formülüne göre otomatik olarak düzeltilecek kadar geçen süreyi dakika cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="58673-122">Specifies the amount of time, in minutes, that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="58673-123">Varsayılan değer 15 dakikadır ve en az değer 5 dakikadır.</span><span class="sxs-lookup"><span data-stu-id="58673-123">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: CloudServiceAndAutoScale, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58673-124">-Otomatik ölçek formülü</span><span class="sxs-lookup"><span data-stu-id="58673-124">-AutoScaleFormula</span></span>
<span data-ttu-id="58673-125">Havuzu otomatik olarak ölçeklendirme formülünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="58673-125">Specifies the formula for automatically scaling the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: CloudServiceAndAutoScale, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58673-126">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="58673-126">-BatchContext</span></span>
<span data-ttu-id="58673-127">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="58673-127">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="58673-128">Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** nesnesi edinmek için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="58673-128">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58673-129">-Certificatereferde</span><span class="sxs-lookup"><span data-stu-id="58673-129">-CertificateReferences</span></span>
<span data-ttu-id="58673-130">Havuz ile ilişkili sertifikaları belirtir.</span><span class="sxs-lookup"><span data-stu-id="58673-130">Specifies certificates associated with the pool.</span></span>
<span data-ttu-id="58673-131">Toplu Iş hizmeti, havuzun her bir COMPUTE düğümüne başvurulan sertifikaları yükler.</span><span class="sxs-lookup"><span data-stu-id="58673-131">The Batch service installs the referenced certificates on each compute node of the pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCertificateReference[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58673-132">-CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="58673-132">-CloudServiceConfiguration</span></span>
<span data-ttu-id="58673-133">Azure bulut hizmeti platformuna dayalı bir havuzun yapılandırma ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="58673-133">Specifies configuration settings for a pool based on the Azure cloud service platform.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudServiceConfiguration
Parameter Sets: CloudServiceAndTargetDedicated, CloudServiceAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58673-134">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="58673-134">-DisplayName</span></span>
<span data-ttu-id="58673-135">Havuzun görünen adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="58673-135">Specifies the display name of the pool.</span></span>

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

### <span data-ttu-id="58673-136">-ID</span><span class="sxs-lookup"><span data-stu-id="58673-136">-Id</span></span>
<span data-ttu-id="58673-137">Oluşturulacak havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="58673-137">Specifies the ID of the pool to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58673-138">-Intercomputenodecommunicationenabled</span><span class="sxs-lookup"><span data-stu-id="58673-138">-InterComputeNodeCommunicationEnabled</span></span>
<span data-ttu-id="58673-139">Bu cmdlet 'in adanmış işlem düğümleri arasında doğrudan iletişim için havuzu ayarlamadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="58673-139">Indicates that this cmdlet sets up the pool for direct communication between dedicated compute nodes.</span></span>

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

### <span data-ttu-id="58673-140">-MaxTasksPerComputeNode</span><span class="sxs-lookup"><span data-stu-id="58673-140">-MaxTasksPerComputeNode</span></span>
<span data-ttu-id="58673-141">Tek bir işlem düğümünde çalıştırılabilecek en fazla görev sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="58673-141">Specifies the maximum number of tasks that can run on a single compute node.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58673-142">-Metadata</span><span class="sxs-lookup"><span data-stu-id="58673-142">-Metadata</span></span>
<span data-ttu-id="58673-143">Yeni havuza eklemek için meta verileri anahtar/değer çiftleri olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="58673-143">Specifies the metadata, as key/value pairs, to add to the new pool.</span></span>
<span data-ttu-id="58673-144">Anahtar, meta veri adıdır.</span><span class="sxs-lookup"><span data-stu-id="58673-144">The key is the metadata name.</span></span>
<span data-ttu-id="58673-145">Değer, meta veri değeridir.</span><span class="sxs-lookup"><span data-stu-id="58673-145">The value is the metadata value.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58673-146">-NetworkConfiguration</span><span class="sxs-lookup"><span data-stu-id="58673-146">-NetworkConfiguration</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58673-147">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="58673-147">-ResizeTimeout</span></span>
<span data-ttu-id="58673-148">Havuza işlem düğümleri tahsis etmek için zaman aşımını belirtir.</span><span class="sxs-lookup"><span data-stu-id="58673-148">Specifies the time-out for allocating compute nodes to the pool.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58673-149">-StartTask</span><span class="sxs-lookup"><span data-stu-id="58673-149">-StartTask</span></span>
<span data-ttu-id="58673-150">Havuzun başlangıç görevi belirtimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="58673-150">Specifies the start task specification for the pool.</span></span>
<span data-ttu-id="58673-151">Başlangıç görevi, bir hesaplama düğümü havuza katıldığında veya hesaplama düğümü yeniden başlatıldığında veya yeniden başlatıldığında çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="58673-151">The start task is run when a compute node joins the pool, or when the compute node is rebooted or reimaged.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSStartTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58673-152">-Targetadanmış</span><span class="sxs-lookup"><span data-stu-id="58673-152">-TargetDedicated</span></span>
<span data-ttu-id="58673-153">Havuza ayrılacak olan işlem düğümlerinin hedef sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="58673-153">Specifies the target number of compute nodes to allocate to the pool.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58673-154">-TaskSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="58673-154">-TaskSchedulingPolicy</span></span>
<span data-ttu-id="58673-155">ComputeNodeFillType gibi görev zamanlama ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="58673-155">Specifies the task scheduling policy, such as the ComputeNodeFillType.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSTaskSchedulingPolicy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58673-156">-VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="58673-156">-VirtualMachineConfiguration</span></span>
<span data-ttu-id="58673-157">Sanal makineler Altyapısındaki bir havuzun yapılandırma ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="58673-157">Specifies configuration settings for a pool on the virtual machines infrastructure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration
Parameter Sets: VirtualMachineAndTargetDedicated, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58673-158">-Virtualınines</span><span class="sxs-lookup"><span data-stu-id="58673-158">-VirtualMachineSize</span></span>
<span data-ttu-id="58673-159">Havuzdaki sanal makinelerin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="58673-159">Specifies the size of the virtual machines in the pool.</span></span>
<span data-ttu-id="58673-160">Sanal makine boyutları hakkında daha fazla bilgi için bkz: sanal makinelerin boyutları https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ ( https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) Microsoft Azure sitesinde).</span><span class="sxs-lookup"><span data-stu-id="58673-160">For more information about virtual machine sizes, see Sizes for virtual machineshttps://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ (https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) in the Microsoft Azure site.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58673-161">-Onay</span><span class="sxs-lookup"><span data-stu-id="58673-161">-Confirm</span></span>
<span data-ttu-id="58673-162">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="58673-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58673-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58673-163">-WhatIf</span></span>
<span data-ttu-id="58673-164">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="58673-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58673-165">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="58673-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58673-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58673-166">-DefaultProfile</span></span>
<span data-ttu-id="58673-167">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="58673-167">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58673-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58673-168">CommonParameters</span></span>
<span data-ttu-id="58673-169">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="58673-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58673-170">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58673-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58673-171">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="58673-171">INPUTS</span></span>

### <span data-ttu-id="58673-172">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="58673-172">BatchAccountContext</span></span>
<span data-ttu-id="58673-173">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="58673-173">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="58673-174">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="58673-174">OUTPUTS</span></span>

## <span data-ttu-id="58673-175">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="58673-175">NOTES</span></span>

## <span data-ttu-id="58673-176">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="58673-176">RELATED LINKS</span></span>

[<span data-ttu-id="58673-177">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="58673-177">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="58673-178">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="58673-178">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="58673-179">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="58673-179">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="58673-180">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="58673-180">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


