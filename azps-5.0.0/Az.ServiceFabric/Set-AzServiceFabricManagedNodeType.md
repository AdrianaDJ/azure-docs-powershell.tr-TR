---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: b0d22b0cb017c40dc0d1b0328f540b7774ca991b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276712"
---
# <span data-ttu-id="1d27f-101">Set-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="1d27f-101">Set-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="1d27f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d27f-102">SYNOPSIS</span></span>
<span data-ttu-id="1d27f-103">Düğüm türü kaynak özelliklerini ayarlar ya da-Reimage parametresi</span><span class="sxs-lookup"><span data-stu-id="1d27f-103">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span>

## <span data-ttu-id="1d27f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1d27f-104">SYNTAX</span></span>

### <span data-ttu-id="1d27f-105">ByObj (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1d27f-105">ByObj (Default)</span></span>
```
Set-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d27f-106">Withparambyname</span><span class="sxs-lookup"><span data-stu-id="1d27f-106">WithParamsByName</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-AsJob] [-InstanceCount <Int32>] [-ApplicationStartPort <Int32>] [-ApplicationEndPort <Int32>]
 [-EphemeralStartPort <Int32>] [-EphemeralEndPort <Int32>] [-Capacity <Hashtable>]
 [-PlacementProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1d27f-107">Reımagebyname</span><span class="sxs-lookup"><span data-stu-id="1d27f-107">ReimageByName</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-Reimage] [-ForceReimage] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d27f-108">Parametre</span><span class="sxs-lookup"><span data-stu-id="1d27f-108">WithParamsById</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d27f-109">Reımagebyıd</span><span class="sxs-lookup"><span data-stu-id="1d27f-109">ReimageById</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceId] <String> -NodeName <String[]> [-Reimage] [-ForceReimage]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d27f-110">Reımagebyobj</span><span class="sxs-lookup"><span data-stu-id="1d27f-110">ReimageByObj</span></span>
```
Set-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> -NodeName <String[]> [-Reimage]
 [-ForceReimage] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1d27f-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="1d27f-111">DESCRIPTION</span></span>
<span data-ttu-id="1d27f-112">Düğüm türü kaynak özelliklerini ayarlar ya da-Reimage parametresi</span><span class="sxs-lookup"><span data-stu-id="1d27f-112">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span> <span data-ttu-id="1d27f-113">Reimgae işleminde, VM 'leri yeniden yazdırmadan ve geri gelmeleri için yeniden etkinleşmeden önce hizmet yapısı düğümleri devre dışı bırakılır.</span><span class="sxs-lookup"><span data-stu-id="1d27f-113">On reimgae operation the service fabric nodes will be disabled before reimaging the vms and enabled them back again once they come back.</span></span> <span data-ttu-id="1d27f-114">Bu birincil düğüm türlerinde yapıldığında, aynı anda tüm düğümlerin yeniden görüntüsü olabileceğinden biraz zaman alabilir.</span><span class="sxs-lookup"><span data-stu-id="1d27f-114">If this is done on primary node types it might take a while as it might not reimage all the nodes at the same time.</span></span> <span data-ttu-id="1d27f-115">Use-Forcereımage, hizmet yapısı düğümleri devre dışı bırakmasa da işlemi zorla, ancak durum bilgisi olan iş yükleri düğümde çalışıyorsa veri kaybına yol açabilir.</span><span class="sxs-lookup"><span data-stu-id="1d27f-115">Use -ForceReimage force the operation even if service fabric is unable to disable the nodes but use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

## <span data-ttu-id="1d27f-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1d27f-116">EXAMPLES</span></span>

### <span data-ttu-id="1d27f-117">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1d27f-117">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -name $NodeTypeName -InstanceCount 6 -Verbose
```

<span data-ttu-id="1d27f-118">Düğüm türünün örnek sayımını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="1d27f-118">Update the instance count of the node type.</span></span>

### <span data-ttu-id="1d27f-119">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="1d27f-119">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -name $NodeTypeName -PlacementProperty @{NodeColor="Red";SomeProperty="6";} -Verbose
```

<span data-ttu-id="1d27f-120">Düğüm türünün yerleşim özellikleri</span><span class="sxs-lookup"><span data-stu-id="1d27f-120">Update placement properites of the node type.</span></span> <span data-ttu-id="1d27f-121">Bu, varsa eski yerleşim özellikleri üzerine yazılır.</span><span class="sxs-lookup"><span data-stu-id="1d27f-121">This will overwrite older placement properites if any.</span></span>

### <span data-ttu-id="1d27f-122">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="1d27f-122">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -Reimage -NodeName nt1_0, nt1_3
```

<span data-ttu-id="1d27f-123">Düğüm türündeki ReImage node 0 ve 3.</span><span class="sxs-lookup"><span data-stu-id="1d27f-123">Reimage node 0 and 3 on the node type.</span></span>

### <span data-ttu-id="1d27f-124">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="1d27f-124">Example 4</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType.VmInstanceCount = 6
$nodeType | Set-AzServiceFabricManagedNodeType
```

<span data-ttu-id="1d27f-125">Boru ile düğüm türünün örnek sayımını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="1d27f-125">Update the instance count of the node type, with piping.</span></span>

## <span data-ttu-id="1d27f-126">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1d27f-126">PARAMETERS</span></span>

### <span data-ttu-id="1d27f-127">-ApplicationEndPort</span><span class="sxs-lookup"><span data-stu-id="1d27f-127">-ApplicationEndPort</span></span>
<span data-ttu-id="1d27f-128">Bir bağlantı noktası aralığının uygulama uç bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="1d27f-128">Application End port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d27f-129">-ApplicationStartPort</span><span class="sxs-lookup"><span data-stu-id="1d27f-129">-ApplicationStartPort</span></span>
<span data-ttu-id="1d27f-130">Uygulama başlangıç bağlantı noktası bir bağlantı noktası aralığının başlangıç noktası.</span><span class="sxs-lookup"><span data-stu-id="1d27f-130">Application start port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d27f-131">-Iş</span><span class="sxs-lookup"><span data-stu-id="1d27f-131">-AsJob</span></span>
<span data-ttu-id="1d27f-132">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="1d27f-132">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="1d27f-133">-Kapasite</span><span class="sxs-lookup"><span data-stu-id="1d27f-133">-Capacity</span></span>
<span data-ttu-id="1d27f-134">Kapasite türündeki düğümlere anahtar/değer çiftleri olarak uygulanan kapasite etiketleri, bu etiketleri kullanarak düğümün ne kadar kaynak olduğunu anlayabilir.</span><span class="sxs-lookup"><span data-stu-id="1d27f-134">Capacity tags applied to the nodes in the node type as key/value pairs, the cluster resource manager uses these tags to understand how much resource a node has.</span></span> <span data-ttu-id="1d27f-135">Bunu güncelleştirmek geçerli değerleri geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="1d27f-135">Updating this will override the current values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d27f-136">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1d27f-136">-ClusterName</span></span>
<span data-ttu-id="1d27f-137">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="1d27f-137">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: WithParamsByName, ReimageByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d27f-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d27f-138">-DefaultProfile</span></span>
<span data-ttu-id="1d27f-139">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1d27f-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d27f-140">-EphemeralEndPort</span><span class="sxs-lookup"><span data-stu-id="1d27f-140">-EphemeralEndPort</span></span>
<span data-ttu-id="1d27f-141">Bir bağlantı noktası aralığının kısa ömürlü uç noktası.</span><span class="sxs-lookup"><span data-stu-id="1d27f-141">Ephemeral end port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d27f-142">-EphemeralStartPort</span><span class="sxs-lookup"><span data-stu-id="1d27f-142">-EphemeralStartPort</span></span>
<span data-ttu-id="1d27f-143">Bir bağlantı noktası aralığının kısa başlangıç bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="1d27f-143">Ephemeral start port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d27f-144">-ForceReimage</span><span class="sxs-lookup"><span data-stu-id="1d27f-144">-ForceReimage</span></span>
<span data-ttu-id="1d27f-145">Bu bayrak kullanıldığında, hizmet yapısı düğümleri devre dışı bırakmasa bile kaldırma işlemi zorlanır.</span><span class="sxs-lookup"><span data-stu-id="1d27f-145">Using this flag will force the removal even if service fabric is unable to disable the nodes.</span></span>
<span data-ttu-id="1d27f-146">Bu, düğümde durum bilgisi olan iş yükleri çalışıyorsa veri kaybına neden olabileceğinden dikkatli kullanın.</span><span class="sxs-lookup"><span data-stu-id="1d27f-146">Use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ReimageByName, ReimageById, ReimageByObj
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d27f-147">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d27f-147">-InputObject</span></span>
<span data-ttu-id="1d27f-148">Düğüm türü kaynağı</span><span class="sxs-lookup"><span data-stu-id="1d27f-148">Node type resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType
Parameter Sets: ByObj, ReimageByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d27f-149">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="1d27f-149">-InstanceCount</span></span>
<span data-ttu-id="1d27f-150">Düğüm türündeki düğümlerin sayısı.</span><span class="sxs-lookup"><span data-stu-id="1d27f-150">The number of nodes in the node type.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d27f-151">-Ad</span><span class="sxs-lookup"><span data-stu-id="1d27f-151">-Name</span></span>
<span data-ttu-id="1d27f-152">Düğüm türünün adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="1d27f-152">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: WithParamsByName, ReimageByName
Aliases: NodeTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d27f-153">-DüğümAdı</span><span class="sxs-lookup"><span data-stu-id="1d27f-153">-NodeName</span></span>
<span data-ttu-id="1d27f-154">İşlemin düğüm adlarının listesi.</span><span class="sxs-lookup"><span data-stu-id="1d27f-154">List of node names for the operation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ReimageByName, ReimageById, ReimageByObj
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d27f-155">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1d27f-155">-PassThru</span></span>
<span data-ttu-id="1d27f-156">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="1d27f-156">{{ Fill PassThru Description }}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ReimageByName, ReimageById, ReimageByObj
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d27f-157">-PlacementProperty</span><span class="sxs-lookup"><span data-stu-id="1d27f-157">-PlacementProperty</span></span>
<span data-ttu-id="1d27f-158">Düğüm türündeki düğümlere uygulanan yerleştirme etiketleri, belirli hizmetlerin (iş yükünün) çalıştırılacağı yeri belirtmek için kullanılabilen anahtar/değer çiftleri olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1d27f-158">Placement tags applied to nodes in the node type as key/value pairs, which can be used to indicate where certain services (workload) should run.</span></span> <span data-ttu-id="1d27f-159">Bunu güncelleştirmek geçerli değerleri geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="1d27f-159">Updating this will override the current values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d27f-160">-Yeniden görüntü</span><span class="sxs-lookup"><span data-stu-id="1d27f-160">-Reimage</span></span>
<span data-ttu-id="1d27f-161">Düğüm türündeki düğümleri yeniden görüntü olarak belirtin.</span><span class="sxs-lookup"><span data-stu-id="1d27f-161">Specify to reimage nodes on the node type.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ReimageByName, ReimageById, ReimageByObj
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d27f-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d27f-162">-ResourceGroupName</span></span>
<span data-ttu-id="1d27f-163">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="1d27f-163">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: WithParamsByName, ReimageByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d27f-164">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1d27f-164">-ResourceId</span></span>
<span data-ttu-id="1d27f-165">Düğüm türü kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="1d27f-165">Node type resource id</span></span>

```yaml
Type: System.String
Parameter Sets: WithParamsById, ReimageById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d27f-166">-Onay</span><span class="sxs-lookup"><span data-stu-id="1d27f-166">-Confirm</span></span>
<span data-ttu-id="1d27f-167">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1d27f-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d27f-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d27f-168">-WhatIf</span></span>
<span data-ttu-id="1d27f-169">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1d27f-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d27f-170">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1d27f-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d27f-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d27f-171">CommonParameters</span></span>
<span data-ttu-id="1d27f-172">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1d27f-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d27f-173">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1d27f-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d27f-174">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1d27f-174">INPUTS</span></span>

### <span data-ttu-id="1d27f-175">System. String</span><span class="sxs-lookup"><span data-stu-id="1d27f-175">System.String</span></span>

## <span data-ttu-id="1d27f-176">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1d27f-176">OUTPUTS</span></span>

### <span data-ttu-id="1d27f-177">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1d27f-177">System.Boolean</span></span>

## <span data-ttu-id="1d27f-178">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1d27f-178">NOTES</span></span>

## <span data-ttu-id="1d27f-179">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1d27f-179">RELATED LINKS</span></span>
