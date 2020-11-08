---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 3e89e807acfb2507834686574931011bf398c76c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276537"
---
# <span data-ttu-id="61411-101">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="61411-101">New-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="61411-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61411-102">SYNOPSIS</span></span>
<span data-ttu-id="61411-103">Yeni düğüm türü kaynağı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="61411-103">Create new node type resource.</span></span>

## <span data-ttu-id="61411-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="61411-104">SYNTAX</span></span>

```
New-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -InstanceCount <Int32> [-Primary] [-DiskSize <Int32>] [-ApplicationStartPort <Int32>]
 [-ApplicationEndPort <Int32>] [-EphemeralStartPort <Int32>] [-EphemeralEndPort <Int32>] [-VmSize <String>]
 [-VmImagePublisher <String>] [-VmImageOffer <String>] [-VmImageSku <String>] [-VmImageVersion <String>]
 [-Capacity <Hashtable>] [-PlacementProperty <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61411-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="61411-105">DESCRIPTION</span></span>
<span data-ttu-id="61411-106">Belirli bir küme için yeni düğüm türü kaynağı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="61411-106">Create new node type resource for an specific cluster.</span></span>

## <span data-ttu-id="61411-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="61411-107">EXAMPLES</span></span>

### <span data-ttu-id="61411-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="61411-108">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
New-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName -Primary -InstanceCount 3
```

<span data-ttu-id="61411-109">3 düğümlü birincil düğüm türü oluşturun.</span><span class="sxs-lookup"><span data-stu-id="61411-109">Create primary node type with 3 nodes.</span></span>

### <span data-ttu-id="61411-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="61411-110">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
New-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName -InstanceCount 5 -Primary -PlacementProperty @{NodeColor="Green";SomeProperty="5";} -Capacity @{ClientConnections="65536";} -ApplicationStartPort 20575 -ApplicationEndPort 20605 -EphemeralStartPort 20606 -EphemeralEndPort 20861
```

<span data-ttu-id="61411-111">5 düğümle birincil düğüm türü oluşturun ve yerleştirme özelliklerini, kapasiteleri, uygulama ve kısa ömürlü bağlantı noktalarını belirtin.</span><span class="sxs-lookup"><span data-stu-id="61411-111">Create primary node type with 5 nodes and specifying placement properties, capacities, application and ephemeral ports.</span></span>

## <span data-ttu-id="61411-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="61411-112">PARAMETERS</span></span>

### <span data-ttu-id="61411-113">-ApplicationEndPort</span><span class="sxs-lookup"><span data-stu-id="61411-113">-ApplicationEndPort</span></span>
<span data-ttu-id="61411-114">Bir bağlantı noktası aralığının uygulama uç bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="61411-114">Application End port of a range of ports.</span></span>

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

### <span data-ttu-id="61411-115">-ApplicationStartPort</span><span class="sxs-lookup"><span data-stu-id="61411-115">-ApplicationStartPort</span></span>
<span data-ttu-id="61411-116">Uygulama başlangıç bağlantı noktası bir bağlantı noktası aralığının başlangıç noktası.</span><span class="sxs-lookup"><span data-stu-id="61411-116">Application start port of a range of ports.</span></span>

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

### <span data-ttu-id="61411-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="61411-117">-AsJob</span></span>
<span data-ttu-id="61411-118">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="61411-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="61411-119">-Kapasite</span><span class="sxs-lookup"><span data-stu-id="61411-119">-Capacity</span></span>
<span data-ttu-id="61411-120">Kapasite türündeki düğümlere anahtar/değer çiftleri olarak uygulanan kapasite etiketleri, bu etiketleri kullanarak düğümün ne kadar kaynak olduğunu anlayabilir.</span><span class="sxs-lookup"><span data-stu-id="61411-120">Capacity tags applied to the nodes in the node type as key/value pairs, the cluster resource manager uses these tags to understand how much resource a node has.</span></span>
<span data-ttu-id="61411-121">Bunu güncelleştirmek geçerli değerleri geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="61411-121">Updating this will override the current values.</span></span>

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

### <span data-ttu-id="61411-122">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="61411-122">-ClusterName</span></span>
<span data-ttu-id="61411-123">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="61411-123">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="61411-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61411-124">-DefaultProfile</span></span>
<span data-ttu-id="61411-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="61411-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61411-126">-DiskSize</span><span class="sxs-lookup"><span data-stu-id="61411-126">-DiskSize</span></span>
<span data-ttu-id="61411-127">Her VM için, GBs 'daki düğüm türündeki disk boyutu.</span><span class="sxs-lookup"><span data-stu-id="61411-127">Disk size for each vm in the node type in GBs.</span></span>
<span data-ttu-id="61411-128">Varsayılan 100.</span><span class="sxs-lookup"><span data-stu-id="61411-128">Default 100.</span></span>

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

### <span data-ttu-id="61411-129">-EphemeralEndPort</span><span class="sxs-lookup"><span data-stu-id="61411-129">-EphemeralEndPort</span></span>
<span data-ttu-id="61411-130">Bir bağlantı noktası aralığının kısa ömürlü uç noktası.</span><span class="sxs-lookup"><span data-stu-id="61411-130">Ephemeral end port of a range of ports.</span></span>

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

### <span data-ttu-id="61411-131">-EphemeralStartPort</span><span class="sxs-lookup"><span data-stu-id="61411-131">-EphemeralStartPort</span></span>
<span data-ttu-id="61411-132">Bir bağlantı noktası aralığının kısa başlangıç bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="61411-132">Ephemeral start port of a range of ports.</span></span>

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

### <span data-ttu-id="61411-133">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="61411-133">-InstanceCount</span></span>
<span data-ttu-id="61411-134">Düğüm türündeki düğümlerin sayısı.</span><span class="sxs-lookup"><span data-stu-id="61411-134">The number of nodes in the node type.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61411-135">-Ad</span><span class="sxs-lookup"><span data-stu-id="61411-135">-Name</span></span>
<span data-ttu-id="61411-136">Düğüm türünün adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="61411-136">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NodeTypeName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61411-137">-PlacementProperty</span><span class="sxs-lookup"><span data-stu-id="61411-137">-PlacementProperty</span></span>
<span data-ttu-id="61411-138">Düğüm türündeki düğümlere uygulanan yerleştirme etiketleri, belirli hizmetlerin (iş yükünün) çalıştırılacağı yeri belirtmek için kullanılabilen anahtar/değer çiftleri olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="61411-138">Placement tags applied to nodes in the node type as key/value pairs, which can be used to indicate where certain services (workload) should run.</span></span>
<span data-ttu-id="61411-139">Bunu güncelleştirmek geçerli değerleri geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="61411-139">Updating this will override the current values.</span></span>

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

### <span data-ttu-id="61411-140">-Birincil</span><span class="sxs-lookup"><span data-stu-id="61411-140">-Primary</span></span>
<span data-ttu-id="61411-141">Düğüm türünün birincil olup olmadığını belirtin.</span><span class="sxs-lookup"><span data-stu-id="61411-141">Specify if the node type is primary.</span></span>
<span data-ttu-id="61411-142">Bu düğüm türünde Sistem Hizmetleri çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="61411-142">On this node type will run system services.</span></span>
<span data-ttu-id="61411-143">Yalnızca bir düğüm türü birincil olarak işaretlenmelidir.</span><span class="sxs-lookup"><span data-stu-id="61411-143">Only one node type should be marked as primary.</span></span>
<span data-ttu-id="61411-144">Var olan kümeler için birincil düğüm türü silinemez veya değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="61411-144">Primary node type cannot be deleted or changed for existing clusters.</span></span>

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

### <span data-ttu-id="61411-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61411-145">-ResourceGroupName</span></span>
<span data-ttu-id="61411-146">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="61411-146">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="61411-147">-Vmımageteklifini</span><span class="sxs-lookup"><span data-stu-id="61411-147">-VmImageOffer</span></span>
<span data-ttu-id="61411-148">Azure sanal makineler marketi görüntüsünün teklif türü.</span><span class="sxs-lookup"><span data-stu-id="61411-148">The offer type of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="61411-149">Varsayılan: WindowsServer.</span><span class="sxs-lookup"><span data-stu-id="61411-149">Default: WindowsServer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "WindowsServer"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61411-150">-Vmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="61411-150">-VmImagePublisher</span></span>
<span data-ttu-id="61411-151">Azure sanal makineler marketi görüntüsünün yayıncısı.</span><span class="sxs-lookup"><span data-stu-id="61411-151">The publisher of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="61411-152">Varsayılan: MicrosoftWindowsServer.</span><span class="sxs-lookup"><span data-stu-id="61411-152">Default: MicrosoftWindowsServer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "MicrosoftWindowsServer"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61411-153">-VmImageSku</span><span class="sxs-lookup"><span data-stu-id="61411-153">-VmImageSku</span></span>
<span data-ttu-id="61411-154">Azure sanal makineler marketi görüntüsünün SKU 'SU.</span><span class="sxs-lookup"><span data-stu-id="61411-154">The SKU of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="61411-155">Varsayılan: 2019-Datacenter.</span><span class="sxs-lookup"><span data-stu-id="61411-155">Default: 2019-Datacenter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "2019-Datacenter"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61411-156">-Vmımageversion</span><span class="sxs-lookup"><span data-stu-id="61411-156">-VmImageVersion</span></span>
<span data-ttu-id="61411-157">Azure sanal makineler marketi görüntüsünün sürümü.</span><span class="sxs-lookup"><span data-stu-id="61411-157">The version of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="61411-158">Varsayılan: en son.</span><span class="sxs-lookup"><span data-stu-id="61411-158">Default: latest.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "latest"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61411-159">-VmSize</span><span class="sxs-lookup"><span data-stu-id="61411-159">-VmSize</span></span>
<span data-ttu-id="61411-160">Havuzdaki sanal makinelerin boyutu.</span><span class="sxs-lookup"><span data-stu-id="61411-160">The size of virtual machines in the pool.</span></span>
<span data-ttu-id="61411-161">Havuzdaki tüm sanal makinelerin boyutu aynıdır.</span><span class="sxs-lookup"><span data-stu-id="61411-161">All virtual machines in a pool are the same size.</span></span>
<span data-ttu-id="61411-162">Varsayılan: Standard_D2.</span><span class="sxs-lookup"><span data-stu-id="61411-162">Default: Standard_D2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "Standard_D2"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61411-163">-Onay</span><span class="sxs-lookup"><span data-stu-id="61411-163">-Confirm</span></span>
<span data-ttu-id="61411-164">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="61411-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61411-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61411-165">-WhatIf</span></span>
<span data-ttu-id="61411-166">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="61411-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61411-167">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="61411-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61411-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61411-168">CommonParameters</span></span>
<span data-ttu-id="61411-169">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="61411-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61411-170">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="61411-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61411-171">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="61411-171">INPUTS</span></span>

### <span data-ttu-id="61411-172">System. String</span><span class="sxs-lookup"><span data-stu-id="61411-172">System.String</span></span>

## <span data-ttu-id="61411-173">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="61411-173">OUTPUTS</span></span>

### <span data-ttu-id="61411-174">Microsoft. Azure. Commands. ServiceFabric. modeller. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="61411-174">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="61411-175">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="61411-175">NOTES</span></span>

## <span data-ttu-id="61411-176">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="61411-176">RELATED LINKS</span></span>
