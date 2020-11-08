---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedCluster.md
ms.openlocfilehash: 4636dc8f8c8efdf9dae5f7d2094fd3432528f043
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277021"
---
# <span data-ttu-id="d361a-101">Set-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="d361a-101">Set-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="d361a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d361a-102">SYNOPSIS</span></span>
<span data-ttu-id="d361a-103">Küme kaynağı özelliklerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d361a-103">Set cluster resource properties.</span></span>

## <span data-ttu-id="d361a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d361a-104">SYNTAX</span></span>

### <span data-ttu-id="d361a-105">ByObj (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d361a-105">ByObj (Default)</span></span>
```
Set-AzServiceFabricManagedCluster [-InputObject] <PSManagedCluster> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d361a-106">WithPramsByName</span><span class="sxs-lookup"><span data-stu-id="d361a-106">WithPramsByName</span></span>
```
Set-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-HttpGatewayConnectionPort <Int32>]
 [-ClientConnectionPort <Int32>] [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d361a-107">Binamebyid</span><span class="sxs-lookup"><span data-stu-id="d361a-107">ByNameById</span></span>
```
Set-AzServiceFabricManagedCluster [-ResourceId] <String> [-UpgradeMode <ClusterUpgradeMode>]
 [-CodeVersion <String>] [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>]
 [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d361a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d361a-108">DESCRIPTION</span></span>
<span data-ttu-id="d361a-109">Küme kaynağı özelliklerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d361a-109">Set cluster resource properties.</span></span>

## <span data-ttu-id="d361a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d361a-110">EXAMPLES</span></span>

### <span data-ttu-id="d361a-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d361a-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Update-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName -DnsName testnewdns -ClientConnectionPort 50000 -Verbose
```

<span data-ttu-id="d361a-112">Kümenin DNS adını ve istemci bağlantı bağlantı noktasını güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="d361a-112">Update dns name and client connection port for the cluster.</span></span>

### <span data-ttu-id="d361a-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d361a-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster.DnsName = "testnewdns"
$cluster.ClientConnectionPort = 50000
$cluster | Set-AzServiceFabricManagedCluster
```

<span data-ttu-id="d361a-114">Kümenin DNS adını ve istemci bağlantı bağlantı noktasını, boruları ile güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="d361a-114">Update dns name and client connection port for the cluster, with piping.</span></span>

## <span data-ttu-id="d361a-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d361a-115">PARAMETERS</span></span>

### <span data-ttu-id="d361a-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="d361a-116">-AsJob</span></span>
<span data-ttu-id="d361a-117">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="d361a-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d361a-118">-ClientConnectionPort</span><span class="sxs-lookup"><span data-stu-id="d361a-118">-ClientConnectionPort</span></span>
<span data-ttu-id="d361a-119">Kümeye yönelik istemci bağlantılarında kullanılan bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="d361a-119">Port used for client connections to the cluster.</span></span> <span data-ttu-id="d361a-120">Varsayılan: 19000.</span><span class="sxs-lookup"><span data-stu-id="d361a-120">Default: 19000.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d361a-121">-CodeVersion</span><span class="sxs-lookup"><span data-stu-id="d361a-121">-CodeVersion</span></span>
<span data-ttu-id="d361a-122">Küme kodu sürümü.</span><span class="sxs-lookup"><span data-stu-id="d361a-122">Cluster code version.</span></span> <span data-ttu-id="d361a-123">Yalnızca yükseltme modu El Ile olduğunda kullanın.</span><span class="sxs-lookup"><span data-stu-id="d361a-123">Only use if upgrade mode is Manual.</span></span>

```yaml
Type: System.String
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d361a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d361a-124">-DefaultProfile</span></span>
<span data-ttu-id="d361a-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d361a-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d361a-126">-DnsName</span><span class="sxs-lookup"><span data-stu-id="d361a-126">-DnsName</span></span>
<span data-ttu-id="d361a-127">Kümenin DNS adı.</span><span class="sxs-lookup"><span data-stu-id="d361a-127">Cluster's dns name.</span></span>

```yaml
Type: System.String
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d361a-128">-HttpGatewayConnectionPort</span><span class="sxs-lookup"><span data-stu-id="d361a-128">-HttpGatewayConnectionPort</span></span>
<span data-ttu-id="d361a-129">Kümenin http bağlantılarında kullanılan bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="d361a-129">Port used for http connections to the cluster.</span></span> <span data-ttu-id="d361a-130">Varsayılan: 19080.</span><span class="sxs-lookup"><span data-stu-id="d361a-130">Default: 19080.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d361a-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d361a-131">-InputObject</span></span>
<span data-ttu-id="d361a-132">Yönetilen küme kaynağı</span><span class="sxs-lookup"><span data-stu-id="d361a-132">Managed Cluster resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d361a-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="d361a-133">-Name</span></span>
<span data-ttu-id="d361a-134">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="d361a-134">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: WithPramsByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d361a-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d361a-135">-ResourceGroupName</span></span>
<span data-ttu-id="d361a-136">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="d361a-136">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: WithPramsByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d361a-137">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d361a-137">-ResourceId</span></span>
<span data-ttu-id="d361a-138">Yönetilen küme kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="d361a-138">Managed Cluster resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d361a-139">-Smarproxyenvseçpointport</span><span class="sxs-lookup"><span data-stu-id="d361a-139">-ReverseProxyEndpointPort</span></span>
<span data-ttu-id="d361a-140">Uç ara sunucu</span><span class="sxs-lookup"><span data-stu-id="d361a-140">Endpoint used by reverse proxy.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d361a-141">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="d361a-141">-UpgradeMode</span></span>
<span data-ttu-id="d361a-142">Küme kodu sürümü yükseltme modu.</span><span class="sxs-lookup"><span data-stu-id="d361a-142">Cluster code version upgrade mode.</span></span> <span data-ttu-id="d361a-143">Otomatik veya el Ile.</span><span class="sxs-lookup"><span data-stu-id="d361a-143">Automatic or Manual.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode]
Parameter Sets: WithPramsByName, ByNameById
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d361a-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="d361a-144">-Confirm</span></span>
<span data-ttu-id="d361a-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d361a-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d361a-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d361a-146">-WhatIf</span></span>
<span data-ttu-id="d361a-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d361a-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d361a-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d361a-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d361a-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d361a-149">CommonParameters</span></span>
<span data-ttu-id="d361a-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d361a-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d361a-151">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d361a-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d361a-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d361a-152">INPUTS</span></span>

### <span data-ttu-id="d361a-153">System. String</span><span class="sxs-lookup"><span data-stu-id="d361a-153">System.String</span></span>

## <span data-ttu-id="d361a-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d361a-154">OUTPUTS</span></span>

### <span data-ttu-id="d361a-155">Microsoft. Azure. Commands. ServiceFabric. modeller. PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="d361a-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="d361a-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d361a-156">NOTES</span></span>

## <span data-ttu-id="d361a-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d361a-157">RELATED LINKS</span></span>
