---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 5f5509da60351216a5ea004eae59e551a74e601a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275860"
---
# <span data-ttu-id="37600-101">Remove-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="37600-101">Remove-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="37600-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37600-102">SYNOPSIS</span></span>
<span data-ttu-id="37600-103">Düğüm türünü veya düğüm türü içindeki belirli düğümleri kaldırın.</span><span class="sxs-lookup"><span data-stu-id="37600-103">Remove the node type or specific nodes within the node type.</span></span>

## <span data-ttu-id="37600-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="37600-104">SYNTAX</span></span>

### <span data-ttu-id="37600-105">DeleteNodeTypeByObj (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="37600-105">DeleteNodeTypeByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37600-106">DeleteNodeTypeByName</span><span class="sxs-lookup"><span data-stu-id="37600-106">DeleteNodeTypeByName</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37600-107">DeleteNodeByName</span><span class="sxs-lookup"><span data-stu-id="37600-107">DeleteNodeByName</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-ForceRemoveNode] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37600-108">DeleteNodeByObj</span><span class="sxs-lookup"><span data-stu-id="37600-108">DeleteNodeByObj</span></span>
```
Remove-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> -NodeName <String[]>
 [-ForceRemoveNode] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37600-109">Deletenodetypebyıd</span><span class="sxs-lookup"><span data-stu-id="37600-109">DeleteNodeTypeById</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37600-110">Deletenodebyıd</span><span class="sxs-lookup"><span data-stu-id="37600-110">DeleteNodeById</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceId] <String> -NodeName <String[]> [-ForceRemoveNode]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37600-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="37600-111">DESCRIPTION</span></span>
<span data-ttu-id="37600-112">Düğüm türünü veya düğüm türü içindeki belirli düğümleri kaldırın.</span><span class="sxs-lookup"><span data-stu-id="37600-112">Remove the node type or specific nodes within the node type.</span></span> <span data-ttu-id="37600-113">Paremter-DüğümAdı kullanılırsa yalnızca belirtilen düğümler kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="37600-113">If the paremter -NodeName is used then only nodes specified will be removed.</span></span>

## <span data-ttu-id="37600-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="37600-114">EXAMPLES</span></span>

### <span data-ttu-id="37600-115">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="37600-115">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt2"
Remove-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName
```

<span data-ttu-id="37600-116">Düğüm türünü kaldır.</span><span class="sxs-lookup"><span data-stu-id="37600-116">Remove node type.</span></span>

### <span data-ttu-id="37600-117">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="37600-117">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt2"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeType
```

<span data-ttu-id="37600-118">Boru ile düğüm türünü kaldırın.</span><span class="sxs-lookup"><span data-stu-id="37600-118">Remove node type, with piping.</span></span>

### <span data-ttu-id="37600-119">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="37600-119">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Remove-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -NodeName nt1_0, nt1_3
```

<span data-ttu-id="37600-120">Düğüm türünden 2 düğümü kaldırma.</span><span class="sxs-lookup"><span data-stu-id="37600-120">Remove 2 nodes from the node type.</span></span>

### <span data-ttu-id="37600-121">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="37600-121">Example 4</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeType -NodeName nt1_0, nt1_3
```

<span data-ttu-id="37600-122">Düğüm türünden 2 düğümü, boruları ile kaldırın.</span><span class="sxs-lookup"><span data-stu-id="37600-122">Remove 2 nodes from the node type, with piping.</span></span>

## <span data-ttu-id="37600-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="37600-123">PARAMETERS</span></span>

### <span data-ttu-id="37600-124">-Iş</span><span class="sxs-lookup"><span data-stu-id="37600-124">-AsJob</span></span>
<span data-ttu-id="37600-125">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="37600-125">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="37600-126">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="37600-126">-ClusterName</span></span>
<span data-ttu-id="37600-127">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="37600-127">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteNodeTypeByName, DeleteNodeByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37600-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37600-128">-DefaultProfile</span></span>
<span data-ttu-id="37600-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="37600-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37600-130">-ForceRemoveNode</span><span class="sxs-lookup"><span data-stu-id="37600-130">-ForceRemoveNode</span></span>
<span data-ttu-id="37600-131">Bu bayrak kullanıldığında, hizmet yapısı düğümleri devre dışı bırakmasa bile kaldırma işlemi zorlanır.</span><span class="sxs-lookup"><span data-stu-id="37600-131">Using this flag will force the removal even if service fabric is unable to disable the nodes.</span></span>
<span data-ttu-id="37600-132">Bu durum, düğümlerde durum bilgisi olan iş yükleri çalışıyorsa veri kaybına neden olabileceğinden ya da opeardan sonra yeterli tohum düğümü olmazsa kümeyi aşağı</span><span class="sxs-lookup"><span data-stu-id="37600-132">Use with caution as this might cause data loss if stateful workloads are running on the nodes, or might bring the cluster down if there are not enough seed nodes after the opearion.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DeleteNodeByName, DeleteNodeByObj, DeleteNodeById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37600-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37600-133">-InputObject</span></span>
<span data-ttu-id="37600-134">Düğüm türü kaynağı</span><span class="sxs-lookup"><span data-stu-id="37600-134">Node type resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType
Parameter Sets: DeleteNodeTypeByObj, DeleteNodeByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37600-135">-Ad</span><span class="sxs-lookup"><span data-stu-id="37600-135">-Name</span></span>
<span data-ttu-id="37600-136">Düğüm türünün adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="37600-136">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteNodeTypeByName, DeleteNodeByName
Aliases: NodeTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37600-137">-DüğümAdı</span><span class="sxs-lookup"><span data-stu-id="37600-137">-NodeName</span></span>
<span data-ttu-id="37600-138">İşlemin düğüm adlarının listesi.</span><span class="sxs-lookup"><span data-stu-id="37600-138">List of node names for the operation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: DeleteNodeByName, DeleteNodeByObj, DeleteNodeById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37600-139">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="37600-139">-PassThru</span></span>
<span data-ttu-id="37600-140">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="37600-140">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="37600-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37600-141">-ResourceGroupName</span></span>
<span data-ttu-id="37600-142">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="37600-142">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteNodeTypeByName, DeleteNodeByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37600-143">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="37600-143">-ResourceId</span></span>
<span data-ttu-id="37600-144">Düğüm türü kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="37600-144">Node type resource id</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteNodeTypeById, DeleteNodeById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37600-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="37600-145">-Confirm</span></span>
<span data-ttu-id="37600-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="37600-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37600-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37600-147">-WhatIf</span></span>
<span data-ttu-id="37600-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="37600-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37600-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="37600-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37600-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37600-150">CommonParameters</span></span>
<span data-ttu-id="37600-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="37600-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37600-152">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="37600-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37600-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="37600-153">INPUTS</span></span>

### <span data-ttu-id="37600-154">System. String</span><span class="sxs-lookup"><span data-stu-id="37600-154">System.String</span></span>

## <span data-ttu-id="37600-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="37600-155">OUTPUTS</span></span>

### <span data-ttu-id="37600-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="37600-156">System.Boolean</span></span>

## <span data-ttu-id="37600-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="37600-157">NOTES</span></span>

## <span data-ttu-id="37600-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="37600-158">RELATED LINKS</span></span>
