---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/update-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
ms.openlocfilehash: a3849a07f83cda8876acdf87015e8f2fc9fe81b5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266158"
---
# <span data-ttu-id="576fb-101">Update-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="576fb-101">Update-AzAksNodePool</span></span>

## <span data-ttu-id="576fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="576fb-102">SYNOPSIS</span></span>
<span data-ttu-id="576fb-103">Yönetilen kümedeki düğüm havuzunu güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="576fb-103">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="576fb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="576fb-104">SYNTAX</span></span>

### <span data-ttu-id="576fb-105">defaultParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="576fb-105">defaultParameterSet (Default)</span></span>
```
Update-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="576fb-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="576fb-106">ParentObjectParameterSet</span></span>
```
Update-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="576fb-107">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="576fb-107">InputObjectParameterSet</span></span>
```
Update-AzAksNodePool -InputObject <PSNodePool> [-AsJob] [-Force] [-KubernetesVersion <String>]
 [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="576fb-108">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="576fb-108">IdParameterSet</span></span>
```
Update-AzAksNodePool -Id <String> [-AsJob] [-Force] [-KubernetesVersion <String>] [-MinCount <Int32>]
 [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="576fb-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="576fb-109">DESCRIPTION</span></span>
<span data-ttu-id="576fb-110">Yönetilen kümedeki düğüm havuzunu güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="576fb-110">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="576fb-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="576fb-111">EXAMPLES</span></span>

### <span data-ttu-id="576fb-112">Belirtilen düğüm havuzu için en az sayımı 5 olarak değiştirme</span><span class="sxs-lookup"><span data-stu-id="576fb-112">Change minimun count to 5 for specified node pool</span></span>
```powershell
PS C:\> Update-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name linuxpool -MinCount 5
```

## <span data-ttu-id="576fb-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="576fb-113">PARAMETERS</span></span>

### <span data-ttu-id="576fb-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="576fb-114">-AsJob</span></span>
<span data-ttu-id="576fb-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="576fb-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="576fb-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="576fb-116">-ClusterName</span></span>
<span data-ttu-id="576fb-117">Yönetilen küme kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="576fb-117">The name of the managed cluster resource.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="576fb-118">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="576fb-118">-ClusterObject</span></span>
<span data-ttu-id="576fb-119">Cluster nesnesi</span><span class="sxs-lookup"><span data-stu-id="576fb-119">The cluster object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="576fb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="576fb-120">-DefaultProfile</span></span>
<span data-ttu-id="576fb-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="576fb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="576fb-122">-Enableautoölçeklendirme</span><span class="sxs-lookup"><span data-stu-id="576fb-122">-EnableAutoScaling</span></span>
<span data-ttu-id="576fb-123">Otomatik gizleme</span><span class="sxs-lookup"><span data-stu-id="576fb-123">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="576fb-124">-Force</span><span class="sxs-lookup"><span data-stu-id="576fb-124">-Force</span></span>
<span data-ttu-id="576fb-125">Düğüm havuzunu sormadan Güncelleştir</span><span class="sxs-lookup"><span data-stu-id="576fb-125">Update node pool without prompt</span></span>

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

### <span data-ttu-id="576fb-126">-ID</span><span class="sxs-lookup"><span data-stu-id="576fb-126">-Id</span></span>
<span data-ttu-id="576fb-127">Yönetilen Kubernetes kümesindeki bir düğüm havuzunun kimliği</span><span class="sxs-lookup"><span data-stu-id="576fb-127">Id of an node pool in managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="576fb-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="576fb-128">-InputObject</span></span>
<span data-ttu-id="576fb-129">Normalde ardışık düzen aracılığıyla iletilen PSAgentPool nesnesi.</span><span class="sxs-lookup"><span data-stu-id="576fb-129">A PSAgentPool object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSNodePool
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="576fb-130">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="576fb-130">-KubernetesVersion</span></span>
<span data-ttu-id="576fb-131">Küme oluştururken kullanılacak Kubernetes sürümü.</span><span class="sxs-lookup"><span data-stu-id="576fb-131">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="576fb-132">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="576fb-132">-MaxCount</span></span>
<span data-ttu-id="576fb-133">Otomatik ölçeklendirme için en fazla düğüm sayısı</span><span class="sxs-lookup"><span data-stu-id="576fb-133">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="576fb-134">-MinCount</span><span class="sxs-lookup"><span data-stu-id="576fb-134">-MinCount</span></span>
<span data-ttu-id="576fb-135">Otomatik ölçeklendirme için en az düğüm sayısı.</span><span class="sxs-lookup"><span data-stu-id="576fb-135">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="576fb-136">-Ad</span><span class="sxs-lookup"><span data-stu-id="576fb-136">-Name</span></span>
<span data-ttu-id="576fb-137">Düğüm havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="576fb-137">The name of the node pool.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet, ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="576fb-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="576fb-138">-ResourceGroupName</span></span>
<span data-ttu-id="576fb-139">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="576fb-139">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="576fb-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="576fb-140">-Confirm</span></span>
<span data-ttu-id="576fb-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="576fb-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="576fb-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="576fb-142">-WhatIf</span></span>
<span data-ttu-id="576fb-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="576fb-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="576fb-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="576fb-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="576fb-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="576fb-145">CommonParameters</span></span>
<span data-ttu-id="576fb-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="576fb-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="576fb-147">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="576fb-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="576fb-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="576fb-148">INPUTS</span></span>

### <span data-ttu-id="576fb-149">Microsoft. Azure. Commands. aks. modeller. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="576fb-149">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="576fb-150">System. String</span><span class="sxs-lookup"><span data-stu-id="576fb-150">System.String</span></span>

## <span data-ttu-id="576fb-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="576fb-151">OUTPUTS</span></span>

### <span data-ttu-id="576fb-152">Microsoft. Azure. Commands. aks. modeller. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="576fb-152">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="576fb-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="576fb-153">NOTES</span></span>

## <span data-ttu-id="576fb-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="576fb-154">RELATED LINKS</span></span>
