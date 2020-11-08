---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C71C486E-34EB-42B5-B38A-D85B7DAA2F74
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchPool.md
ms.openlocfilehash: def1c315a99592ca584baa10194e7b9238984506
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "94107214"
---
# <span data-ttu-id="da779-101">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="da779-101">New-AzBatchPool</span></span>

## <span data-ttu-id="da779-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da779-102">SYNOPSIS</span></span>
<span data-ttu-id="da779-103">Toplu Iş hizmetinde havuz oluşturur.</span><span class="sxs-lookup"><span data-stu-id="da779-103">Creates a pool in the Batch service.</span></span>

## <span data-ttu-id="da779-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="da779-104">SYNTAX</span></span>

### <span data-ttu-id="da779-105">Cloudserviceandtargetadanmış (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="da779-105">CloudServiceAndTargetDedicated (Default)</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>] [-ResizeTimeout <TimeSpan>]
 [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
 [-MaxTasksPerComputeNode <Int32>] [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 [-MountConfiguration <PSMountConfiguration[]>] [-UserAccount <PSUserAccount[]>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="da779-106">Virtualmachineandtargetadanmış</span><span class="sxs-lookup"><span data-stu-id="da779-106">VirtualMachineAndTargetDedicated</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>] [-ResizeTimeout <TimeSpan>]
 [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
 [-MaxTasksPerComputeNode <Int32>] [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] [-MountConfiguration <PSMountConfiguration[]>]
 [-UserAccount <PSUserAccount[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da779-107">CloudServiceAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="da779-107">CloudServiceAndAutoScale</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 [-MountConfiguration <PSMountConfiguration[]>] [-UserAccount <PSUserAccount[]>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="da779-108">VirtualMachineAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="da779-108">VirtualMachineAndAutoScale</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] [-MountConfiguration <PSMountConfiguration[]>]
 [-UserAccount <PSUserAccount[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da779-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="da779-109">DESCRIPTION</span></span>
<span data-ttu-id="da779-110">**New-AzBatchPool** cmdlet 'ı, Azure Batch hizmetinde *batchcontext* parametresinde belirtilen hesap altında bir havuz oluşturur.</span><span class="sxs-lookup"><span data-stu-id="da779-110">The **New-AzBatchPool** cmdlet creates a pool in the Azure Batch service under the account specified by the *BatchContext* parameter.</span></span>

## <span data-ttu-id="da779-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="da779-111">EXAMPLES</span></span>

### <span data-ttu-id="da779-112">Örnek 1: CloudServiceConfiguration kullanarak Targetadanmış parametre kümesini kullanarak yeni havuz oluşturma</span><span class="sxs-lookup"><span data-stu-id="da779-112">Example 1: Create a new pool using the TargetDedicated parameter set using CloudServiceConfiguration</span></span>
```
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSCloudServiceConfiguration" -ArgumentList @(4,"*")
PS C:\>New-AzBatchPool -Id "MyPool" -VirtualMachineSize "STANDARD_D1_V2" -CloudServiceConfiguration $configuration  -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

<span data-ttu-id="da779-113">Havuz, Aile dörtte işletim sistemi sürümü ile STANDARD_D1_V2 sanal makineleri kullanacak şekilde yapılandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="da779-113">The pool is configured to use STANDARD_D1_V2 virtual machines with operating system version of family four.</span></span>

### <span data-ttu-id="da779-114">Örnek 2: VirtualMachineConfiguration kullanarak Targetadanmış parametre kümesini kullanarak yeni bir havuz oluşturma</span><span class="sxs-lookup"><span data-stu-id="da779-114">Example 2: Create a new pool using the TargetDedicated parameter set using VirtualMachineConfiguration</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>New-AzBatchPool -Id "MyPool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

<span data-ttu-id="da779-115">Bu komut, Targetadanmış parametre kümesini kullanarak KIMLIĞI MyPool ile yeni bir havuz oluşturur.</span><span class="sxs-lookup"><span data-stu-id="da779-115">This command creates a new pool with ID MyPool using the TargetDedicated parameter set.</span></span>
<span data-ttu-id="da779-116">Hedef ayırma üç COMPUTE düğümlerdir.</span><span class="sxs-lookup"><span data-stu-id="da779-116">The target allocation is three compute nodes.</span></span>
<span data-ttu-id="da779-117">Havuz, Windows-2016-Datacenter işletim sistemi görüntüsüyle STANDARD_D1_V2 sanal makineleri kullanacak şekilde yapılandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="da779-117">The pool is configured to use STANDARD_D1_V2 virtual machines with the Windows-2016-Datacenter operating system image.</span></span>

### <span data-ttu-id="da779-118">Örnek 3: otomatik ölçeklendirme parametre kümesini kullanarak yeni havuz oluşturma</span><span class="sxs-lookup"><span data-stu-id="da779-118">Example 3: Create a new pool using the AutoScale parameter set</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -AutoScaleFormula '$TargetDedicated=2;' -BatchContext $Context
```

<span data-ttu-id="da779-119">Bu komut otomatik ölçeklendirme parametre kümesini kullanarak KIMLIK AutoScalePool ile yeni bir havuz oluşturur.</span><span class="sxs-lookup"><span data-stu-id="da779-119">This command creates a new pool with ID AutoScalePool using the AutoScale parameter set.</span></span>
<span data-ttu-id="da779-120">Havuz, Windows-2016-Datacenter işletim sistemi görüntüsüyle STANDARD_D1_V2 sanal makineleri kullanacak şekilde yapılandırılmıştır ve hedef sayısı hedef sayısı otomatik ölçeklendirme formülüyle belirlenir.</span><span class="sxs-lookup"><span data-stu-id="da779-120">The pool is configured to use STANDARD_D1_V2 virtual machines with the Windows-2016-Datacenter operating system image, and the target number of compute nodes are determined by the Autoscale formula.</span></span>

### <span data-ttu-id="da779-121">Örnek 4: alt ağda düğümleri bulunan havuz oluşturma</span><span class="sxs-lookup"><span data-stu-id="da779-121">Example 4: Create a pool with nodes in a subnet</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>$networkConfig = New-Object Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration
PS C:\>$networkConfig.SubnetId = "/subscriptions/{subscription}/resourceGroups/{group}/providers/{provider}/virtualNetworks/{network}/subnets/{subnet}"
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -NetworkConfiguration $networkConfig -BatchContext $Context
```

### <span data-ttu-id="da779-122">Örnek 5: özel kullanıcı hesaplarıyla havuz oluşturma</span><span class="sxs-lookup"><span data-stu-id="da779-122">Example 5: Create a pool with custom user accounts</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>$userAccount = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserAccount -ArgumentList @("myaccount", "mypassword")
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -UserAccount $userAccount
```

## <span data-ttu-id="da779-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="da779-123">PARAMETERS</span></span>

### <span data-ttu-id="da779-124">-Applicationlisansları</span><span class="sxs-lookup"><span data-stu-id="da779-124">-ApplicationLicenses</span></span>
<span data-ttu-id="da779-125">Toplu hizmet, havuzdaki her bir işlem düğümünde kullanılabilir olacak uygulama lisanslarının listesi.</span><span class="sxs-lookup"><span data-stu-id="da779-125">The list of application licenses the Batch service will make available on each compute node in the pool.</span></span>

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

### <span data-ttu-id="da779-126">-Applicationpackagereferfer</span><span class="sxs-lookup"><span data-stu-id="da779-126">-ApplicationPackageReferences</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: (All)
Aliases: ApplicationPackageReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da779-127">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="da779-127">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="da779-128">Havuz boyutu otomatik ölçeklendirme formülüne göre otomatik olarak düzeltilecek kadar geçen süreyi dakika cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="da779-128">Specifies the amount of time, in minutes, that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="da779-129">Varsayılan değer 15 dakikadır ve en az değer 5 dakikadır.</span><span class="sxs-lookup"><span data-stu-id="da779-129">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="da779-130">-Otomatik ölçek formülü</span><span class="sxs-lookup"><span data-stu-id="da779-130">-AutoScaleFormula</span></span>
<span data-ttu-id="da779-131">Havuzu otomatik olarak ölçeklendirme formülünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="da779-131">Specifies the formula for automatically scaling the pool.</span></span>

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

### <span data-ttu-id="da779-132">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="da779-132">-BatchContext</span></span>
<span data-ttu-id="da779-133">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="da779-133">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="da779-134">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="da779-134">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="da779-135">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKey cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="da779-135">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="da779-136">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="da779-136">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="da779-137">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="da779-137">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="da779-138">-Certificatereferde</span><span class="sxs-lookup"><span data-stu-id="da779-138">-CertificateReferences</span></span>
<span data-ttu-id="da779-139">Havuz ile ilişkili sertifikaları belirtir.</span><span class="sxs-lookup"><span data-stu-id="da779-139">Specifies certificates associated with the pool.</span></span>
<span data-ttu-id="da779-140">Toplu Iş hizmeti, havuzun her bir COMPUTE düğümüne başvurulan sertifikaları yükler.</span><span class="sxs-lookup"><span data-stu-id="da779-140">The Batch service installs the referenced certificates on each compute node of the pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCertificateReference[]
Parameter Sets: (All)
Aliases: CertificateReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da779-141">-CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="da779-141">-CloudServiceConfiguration</span></span>
<span data-ttu-id="da779-142">Azure bulut hizmeti platformuna dayalı bir havuzun yapılandırma ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="da779-142">Specifies configuration settings for a pool based on the Azure cloud service platform.</span></span>

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

### <span data-ttu-id="da779-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da779-143">-DefaultProfile</span></span>
<span data-ttu-id="da779-144">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="da779-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da779-145">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="da779-145">-DisplayName</span></span>
<span data-ttu-id="da779-146">Havuzun görünen adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="da779-146">Specifies the display name of the pool.</span></span>

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

### <span data-ttu-id="da779-147">-ID</span><span class="sxs-lookup"><span data-stu-id="da779-147">-Id</span></span>
<span data-ttu-id="da779-148">Oluşturulacak havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="da779-148">Specifies the ID of the pool to create.</span></span>

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

### <span data-ttu-id="da779-149">-Intercomputenodecommunicationenabled</span><span class="sxs-lookup"><span data-stu-id="da779-149">-InterComputeNodeCommunicationEnabled</span></span>
<span data-ttu-id="da779-150">Bu cmdlet 'in adanmış işlem düğümleri arasında doğrudan iletişim için havuzu ayarlamadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="da779-150">Indicates that this cmdlet sets up the pool for direct communication between dedicated compute nodes.</span></span>

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

### <span data-ttu-id="da779-151">-MaxTasksPerComputeNode</span><span class="sxs-lookup"><span data-stu-id="da779-151">-MaxTasksPerComputeNode</span></span>
<span data-ttu-id="da779-152">Tek bir işlem düğümünde çalıştırılabilecek en fazla görev sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="da779-152">Specifies the maximum number of tasks that can run on a single compute node.</span></span>

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

### <span data-ttu-id="da779-153">-Metadata</span><span class="sxs-lookup"><span data-stu-id="da779-153">-Metadata</span></span>
<span data-ttu-id="da779-154">Yeni havuza eklemek için meta verileri anahtar/değer çiftleri olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="da779-154">Specifies the metadata, as key/value pairs, to add to the new pool.</span></span>
<span data-ttu-id="da779-155">Anahtar, meta veri adıdır.</span><span class="sxs-lookup"><span data-stu-id="da779-155">The key is the metadata name.</span></span>
<span data-ttu-id="da779-156">Değer, meta veri değeridir.</span><span class="sxs-lookup"><span data-stu-id="da779-156">The value is the metadata value.</span></span>

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

### <span data-ttu-id="da779-157">-Mountyapılandırması</span><span class="sxs-lookup"><span data-stu-id="da779-157">-MountConfiguration</span></span>
<span data-ttu-id="da779-158">Havuzdaki her düğüme takılacak dosya sistemlerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="da779-158">A list of file systems to mount on each node in the pool.</span></span> <span data-ttu-id="da779-159">Bu, Azure dosyalarını, NFS, CIFS/SMB ve Blobsigortası destekler.</span><span class="sxs-lookup"><span data-stu-id="da779-159">This supports Azure Files, NFS, CIFS/SMB, and Blobfuse.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSMountConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da779-160">-NetworkConfiguration</span><span class="sxs-lookup"><span data-stu-id="da779-160">-NetworkConfiguration</span></span>
<span data-ttu-id="da779-161">Havuzun ağ yapılandırması.</span><span class="sxs-lookup"><span data-stu-id="da779-161">The network configuration for the pool.</span></span>

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

### <span data-ttu-id="da779-162">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="da779-162">-ResizeTimeout</span></span>
<span data-ttu-id="da779-163">Havuza işlem düğümleri tahsis etmek için zaman aşımını belirtir.</span><span class="sxs-lookup"><span data-stu-id="da779-163">Specifies the time-out for allocating compute nodes to the pool.</span></span>

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

### <span data-ttu-id="da779-164">-StartTask</span><span class="sxs-lookup"><span data-stu-id="da779-164">-StartTask</span></span>
<span data-ttu-id="da779-165">Havuzun başlangıç görevi belirtimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="da779-165">Specifies the start task specification for the pool.</span></span>
<span data-ttu-id="da779-166">Başlangıç görevi, bir hesaplama düğümü havuza katıldığında veya hesaplama düğümü yeniden başlatıldığında veya yeniden başlatıldığında çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="da779-166">The start task is run when a compute node joins the pool, or when the compute node is rebooted or reimaged.</span></span>

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

### <span data-ttu-id="da779-167">-TARGETTE</span><span class="sxs-lookup"><span data-stu-id="da779-167">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="da779-168">Havuza ayrılacak adanmış işlem düğümlerinin hedef sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="da779-168">Specifies the target number of dedicated compute nodes to allocate to the pool.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: TargetDedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da779-169">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="da779-169">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="da779-170">Havuza ayrılacak düşük öncelikli işlem düğümlerinin hedef sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="da779-170">Specifies the target number of low-priority compute nodes to allocate to the pool.</span></span>

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

### <span data-ttu-id="da779-171">-TaskSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="da779-171">-TaskSchedulingPolicy</span></span>
<span data-ttu-id="da779-172">ComputeNodeFillType gibi görev zamanlama ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="da779-172">Specifies the task scheduling policy, such as the ComputeNodeFillType.</span></span>

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

### <span data-ttu-id="da779-173">-Kullanıcıhesabı</span><span class="sxs-lookup"><span data-stu-id="da779-173">-UserAccount</span></span>
<span data-ttu-id="da779-174">Havuzdaki her düğümde oluşturulacak Kullanıcı hesaplarının listesi.</span><span class="sxs-lookup"><span data-stu-id="da779-174">The list of user accounts to be created on each node in the pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSUserAccount[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da779-175">-VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="da779-175">-VirtualMachineConfiguration</span></span>
<span data-ttu-id="da779-176">Sanal makineler Altyapısındaki bir havuzun yapılandırma ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="da779-176">Specifies configuration settings for a pool on the virtual machines infrastructure.</span></span>

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

### <span data-ttu-id="da779-177">-Virtualınines</span><span class="sxs-lookup"><span data-stu-id="da779-177">-VirtualMachineSize</span></span>
<span data-ttu-id="da779-178">Havuzdaki sanal makinelerin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="da779-178">Specifies the size of the virtual machines in the pool.</span></span>
<span data-ttu-id="da779-179">Sanal makine boyutları hakkında daha fazla bilgi için bkz: sanal makinelerin boyutları https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ ( https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) Microsoft Azure sitesinde).</span><span class="sxs-lookup"><span data-stu-id="da779-179">For more information about virtual machine sizes, see Sizes for virtual machineshttps://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ (https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) in the Microsoft Azure site.</span></span>

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

### <span data-ttu-id="da779-180">-Onay</span><span class="sxs-lookup"><span data-stu-id="da779-180">-Confirm</span></span>
<span data-ttu-id="da779-181">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="da779-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da779-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da779-182">-WhatIf</span></span>
<span data-ttu-id="da779-183">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="da779-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da779-184">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="da779-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da779-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da779-185">CommonParameters</span></span>
<span data-ttu-id="da779-186">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="da779-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da779-187">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="da779-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da779-188">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="da779-188">INPUTS</span></span>

### <span data-ttu-id="da779-189">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="da779-189">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="da779-190">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="da779-190">OUTPUTS</span></span>

### <span data-ttu-id="da779-191">System. void</span><span class="sxs-lookup"><span data-stu-id="da779-191">System.Void</span></span>

## <span data-ttu-id="da779-192">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="da779-192">NOTES</span></span>

## <span data-ttu-id="da779-193">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="da779-193">RELATED LINKS</span></span>

[<span data-ttu-id="da779-194">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="da779-194">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="da779-195">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="da779-195">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="da779-196">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="da779-196">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="da779-197">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="da779-197">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


