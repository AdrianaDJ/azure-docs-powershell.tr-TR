---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricService.md
ms.openlocfilehash: 5a17b7197399ac51afccfbc5b00a77e0d2bca727
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932427"
---
# <span data-ttu-id="54d03-101">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="54d03-101">New-AzServiceFabricService</span></span>

## <span data-ttu-id="54d03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54d03-102">SYNOPSIS</span></span>
<span data-ttu-id="54d03-103">Belirtilen uygulama ve küme altında yeni hizmet yapısı hizmeti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="54d03-103">Create new service fabric service under the specified application and cluster.</span></span>

## <span data-ttu-id="54d03-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="54d03-104">SYNTAX</span></span>

### <span data-ttu-id="54d03-105">Stateless-Singleton (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="54d03-105">Stateless-Singleton (Default)</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeSingleton] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="54d03-106">Stateless-UniformInt64Range</span><span class="sxs-lookup"><span data-stu-id="54d03-106">Stateless-UniformInt64Range</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeUniformInt64] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="54d03-107">Stateless-Named</span><span class="sxs-lookup"><span data-stu-id="54d03-107">Stateless-Named</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeNamed] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54d03-108">Stateful-Singleton</span><span class="sxs-lookup"><span data-stu-id="54d03-108">Stateful-Singleton</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeSingleton]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54d03-109">Stateful-UniformInt64Range</span><span class="sxs-lookup"><span data-stu-id="54d03-109">Stateful-UniformInt64Range</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeUniformInt64]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54d03-110">Stateful-Named</span><span class="sxs-lookup"><span data-stu-id="54d03-110">Stateful-Named</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeNamed]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54d03-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="54d03-111">DESCRIPTION</span></span>
<span data-ttu-id="54d03-112">Bu cmdlet, belirtilen uygulama altında durumsuz veya durumlu hizmetler oluşturmaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="54d03-112">This cmdlet allows to creating  stateless or stateful services under the specified application.</span></span> <span data-ttu-id="54d03-113">Hizmet uygulama bildiriminde çıkmalı ve tür bildirimdeki ile aynı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="54d03-113">The service should exit in the application manifest and the type should be the same as the one in the manifest.</span></span> <span data-ttu-id="54d03-114">Uygulama adı, hizmet adının bir öneki olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="54d03-114">The application name should be a prefix of the service name.</span></span>

## <span data-ttu-id="54d03-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="54d03-115">EXAMPLES</span></span>

### <span data-ttu-id="54d03-116">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="54d03-116">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService1"
PS C:\> $serviceTypeName = "testStateless"
PS C:\> New-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName -Type $serviceTypeName -Stateless -InstanceCount -1 -PartitionSchemaSingleton -Verbose
```

<span data-ttu-id="54d03-117">Bu örnek, örnek sayısı-1 (tüm düğümlerde) ile "testApp ~ testService1" yeni bir durumsuz hizmet oluşturur.</span><span class="sxs-lookup"><span data-stu-id="54d03-117">This example will create a new stateless service "testApp~testService1" with instance count -1 (on all the nodes).</span></span>

### <span data-ttu-id="54d03-118">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="54d03-118">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService2"
PS C:\> $serviceTypeName = "testStatefulType"
PS C:\> New-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName -Type $serviceTypeName -Stateful -TargetReplicaSetSize 3 MinReplicaSetSize 5
```

<span data-ttu-id="54d03-119">Bu örnek, 5 düğümün hedefi olan yeni bir "testApp ~ testService2" hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="54d03-119">This example will create a new stateful service "testApp~testService2" with a target of 5 nodes.</span></span>

## <span data-ttu-id="54d03-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="54d03-120">PARAMETERS</span></span>

### <span data-ttu-id="54d03-121">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="54d03-121">-ApplicationName</span></span>
<span data-ttu-id="54d03-122">Uygulamanın adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="54d03-122">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54d03-123">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="54d03-123">-ClusterName</span></span>
<span data-ttu-id="54d03-124">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="54d03-124">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="54d03-125">-DefaultMoveCost</span><span class="sxs-lookup"><span data-stu-id="54d03-125">-DefaultMoveCost</span></span>
<span data-ttu-id="54d03-126">Taşıma için varsayılan maliyeti belirtin.</span><span class="sxs-lookup"><span data-stu-id="54d03-126">Specify the default cost for a move.</span></span>
<span data-ttu-id="54d03-127">Daha yüksek maliyetler, küme kaynak yöneticisi 'nin, kümeyi bakiyeyle</span><span class="sxs-lookup"><span data-stu-id="54d03-127">Higher costs make it less likely that the Cluster Resource Manager will move the replica when trying to balance the cluster</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.MoveCostEnum
Parameter Sets: (All)
Aliases:
Accepted values: Zero, Low, Medium, High

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54d03-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54d03-128">-DefaultProfile</span></span>
<span data-ttu-id="54d03-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="54d03-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54d03-130">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="54d03-130">-InstanceCount</span></span>
<span data-ttu-id="54d03-131">Hizmetin örnek sayımını belirtme</span><span class="sxs-lookup"><span data-stu-id="54d03-131">Specify the instance count for the service</span></span>

```yaml
Type: System.Int32
Parameter Sets: Stateless-Singleton, Stateless-UniformInt64Range, Stateless-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54d03-132">-MinReplicaSetSize</span><span class="sxs-lookup"><span data-stu-id="54d03-132">-MinReplicaSetSize</span></span>
<span data-ttu-id="54d03-133">Hizmetin en küçük çoğaltma kümesi boyutunu belirtme</span><span class="sxs-lookup"><span data-stu-id="54d03-133">Specify the min replica set size for the service</span></span>

```yaml
Type: System.Int32
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54d03-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="54d03-134">-Name</span></span>
<span data-ttu-id="54d03-135">Hizmetin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="54d03-135">Specify the name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54d03-136">-Bölümdüzeni</span><span class="sxs-lookup"><span data-stu-id="54d03-136">-PartitionSchemeNamed</span></span>
<span data-ttu-id="54d03-137">Hizmetin adlandırılmış bölüm düzenini kullandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="54d03-137">Indicates that the service uses the named partition scheme.</span></span>
<span data-ttu-id="54d03-138">Bu modeli kullanan hizmetlerin, genellikle sınırlanmış şekilde, sınırlanmış bir şekilde ayarlanmış verileri vardır.</span><span class="sxs-lookup"><span data-stu-id="54d03-138">Services using this model usually have data that can be bucketed, within a bounded set.</span></span>
<span data-ttu-id="54d03-139">Adlandırılmış bölüm anahtarları olarak kullanılan veri alanlarının bazı yaygın örnekleri bölgeler, posta kodları, müşteri grupları veya diğer iş sınırları olabilir.</span><span class="sxs-lookup"><span data-stu-id="54d03-139">Some common examples of data fields used as named partition keys would be regions, postal codes, customer groups, or other business boundaries.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateless-Named, Stateful-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54d03-140">-Bölümdüzeni</span><span class="sxs-lookup"><span data-stu-id="54d03-140">-PartitionSchemeSingleton</span></span>
<span data-ttu-id="54d03-141">Hizmetin tek bölüm düzeni kullandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="54d03-141">Indicates that the service uses the singleton partition scheme.</span></span>
<span data-ttu-id="54d03-142">Tek bölümler genellikle hizmet ek yönlendirme gerektirmezse kullanılır.</span><span class="sxs-lookup"><span data-stu-id="54d03-142">Singleton partitions are typically used when the service does not require any additional routing.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateless-Singleton, Stateful-Singleton
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54d03-143">-PartitionSchemeUniformInt64</span><span class="sxs-lookup"><span data-stu-id="54d03-143">-PartitionSchemeUniformInt64</span></span>
<span data-ttu-id="54d03-144">Hizmetin, UniformInt64 bölüm düzenini kullandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="54d03-144">Indicates that the service uses the UniformInt64 partition scheme.</span></span>
<span data-ttu-id="54d03-145">Bu, her bölümün bir int64 anahtar aralığına sahip olduğu anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="54d03-145">This means that each partition owns a range of int64 keys.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateless-UniformInt64Range, Stateful-UniformInt64Range
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54d03-146">-QuorumLossWaitDuration</span><span class="sxs-lookup"><span data-stu-id="54d03-146">-QuorumLossWaitDuration</span></span>
<span data-ttu-id="54d03-147">Hizmetin çekirdek kaybı bekleme süresini belirtme</span><span class="sxs-lookup"><span data-stu-id="54d03-147">Specify the quorum loss wait duration for the service</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54d03-148">-ReplicaRestartWaitDuration</span><span class="sxs-lookup"><span data-stu-id="54d03-148">-ReplicaRestartWaitDuration</span></span>
<span data-ttu-id="54d03-149">Hizmetin çoğaltma yeniden başlatma bekleme süresini belirtme</span><span class="sxs-lookup"><span data-stu-id="54d03-149">Specify the replica restart wait duration for the service</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54d03-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54d03-150">-ResourceGroupName</span></span>
<span data-ttu-id="54d03-151">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="54d03-151">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="54d03-152">-Standda Replicakeepduration</span><span class="sxs-lookup"><span data-stu-id="54d03-152">-StandByReplicaKeepDuration</span></span>
<span data-ttu-id="54d03-153">Hizmetin beklemeye göre çoğaltma süresini belirtme</span><span class="sxs-lookup"><span data-stu-id="54d03-153">Specify the stand by replica duration for the service</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54d03-154">-Stateful</span><span class="sxs-lookup"><span data-stu-id="54d03-154">-Stateful</span></span>
<span data-ttu-id="54d03-155">Durumlu hizmet için kullanma</span><span class="sxs-lookup"><span data-stu-id="54d03-155">Use for stateful service</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54d03-156">-Durumsuz</span><span class="sxs-lookup"><span data-stu-id="54d03-156">-Stateless</span></span>
<span data-ttu-id="54d03-157">Durumsuz hizmet için kullanma</span><span class="sxs-lookup"><span data-stu-id="54d03-157">Use for stateless service</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateless-Singleton, Stateless-UniformInt64Range, Stateless-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54d03-158">-TargetReplicaSetSize</span><span class="sxs-lookup"><span data-stu-id="54d03-158">-TargetReplicaSetSize</span></span>
<span data-ttu-id="54d03-159">Hizmetin hedef çoğaltma kümesi boyutunu belirtme</span><span class="sxs-lookup"><span data-stu-id="54d03-159">Specify the target replica set size for the service</span></span>

```yaml
Type: System.Int32
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54d03-160">-Tür</span><span class="sxs-lookup"><span data-stu-id="54d03-160">-Type</span></span>
<span data-ttu-id="54d03-161">Uygulama bildiriminde bulunması gereken uygulamanın hizmet türü adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="54d03-161">Specify the service type name of the application, should exist in the application manifest.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceType

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54d03-162">-Onay</span><span class="sxs-lookup"><span data-stu-id="54d03-162">-Confirm</span></span>
<span data-ttu-id="54d03-163">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="54d03-163">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54d03-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54d03-164">-WhatIf</span></span>
<span data-ttu-id="54d03-165">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="54d03-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54d03-166">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="54d03-166">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54d03-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54d03-167">CommonParameters</span></span>
<span data-ttu-id="54d03-168">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="54d03-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54d03-169">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54d03-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54d03-170">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="54d03-170">INPUTS</span></span>

### <span data-ttu-id="54d03-171">System. String</span><span class="sxs-lookup"><span data-stu-id="54d03-171">System.String</span></span>

## <span data-ttu-id="54d03-172">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="54d03-172">OUTPUTS</span></span>

### <span data-ttu-id="54d03-173">Microsoft. Azure. Commands. ServiceFabric. modeller. PSService</span><span class="sxs-lookup"><span data-stu-id="54d03-173">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="54d03-174">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="54d03-174">NOTES</span></span>

## <span data-ttu-id="54d03-175">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="54d03-175">RELATED LINKS</span></span>