---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/remove-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksNodePool.md
ms.openlocfilehash: 13bc647a0b2cbbc415c12aabb9e14016e3d34149
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266161"
---
# <span data-ttu-id="07cf2-101">Remove-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="07cf2-101">Remove-AzAksNodePool</span></span>

## <span data-ttu-id="07cf2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07cf2-102">SYNOPSIS</span></span>
<span data-ttu-id="07cf2-103">Yönetilen kümeden düğüm havuzunu silme.</span><span class="sxs-lookup"><span data-stu-id="07cf2-103">Delete node pool from managed cluster.</span></span>

## <span data-ttu-id="07cf2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="07cf2-104">SYNTAX</span></span>

### <span data-ttu-id="07cf2-105">GroupNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="07cf2-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAksNodePool [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07cf2-106">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="07cf2-106">InputObjectParameterSet</span></span>
```
Remove-AzAksNodePool -InputObject <PSNodePool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07cf2-107">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="07cf2-107">IdParameterSet</span></span>
```
Remove-AzAksNodePool [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07cf2-108">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="07cf2-108">ParentObjectParameterSet</span></span>
```
Remove-AzAksNodePool [-Name] <String> -ClusterObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07cf2-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="07cf2-109">DESCRIPTION</span></span>
<span data-ttu-id="07cf2-110">Yönetilen kümeden düğüm havuzunu silme.</span><span class="sxs-lookup"><span data-stu-id="07cf2-110">Delete node pool from managed cluster.</span></span>

## <span data-ttu-id="07cf2-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="07cf2-111">EXAMPLES</span></span>

### <span data-ttu-id="07cf2-112">Belirtilen düğüm havuzunu silme</span><span class="sxs-lookup"><span data-stu-id="07cf2-112">Delete specified node pool</span></span>
```powershell
PS C:\> Remove-AzAksNodePool -ResourceGroupName myResourceGroup -CulsterName myCluster -Name winpool
```

## <span data-ttu-id="07cf2-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="07cf2-113">PARAMETERS</span></span>

### <span data-ttu-id="07cf2-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="07cf2-114">-AsJob</span></span>
<span data-ttu-id="07cf2-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="07cf2-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="07cf2-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="07cf2-116">-ClusterName</span></span>
<span data-ttu-id="07cf2-117">Yönetilen Kubernetes kümeniz adı</span><span class="sxs-lookup"><span data-stu-id="07cf2-117">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07cf2-118">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="07cf2-118">-ClusterObject</span></span>
<span data-ttu-id="07cf2-119">Küme nesnesi.</span><span class="sxs-lookup"><span data-stu-id="07cf2-119">The cluster object.</span></span>

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

### <span data-ttu-id="07cf2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07cf2-120">-DefaultProfile</span></span>
<span data-ttu-id="07cf2-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="07cf2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07cf2-122">-Force</span><span class="sxs-lookup"><span data-stu-id="07cf2-122">-Force</span></span>
<span data-ttu-id="07cf2-123">Düğüm havuzunu sormadan kaldırma</span><span class="sxs-lookup"><span data-stu-id="07cf2-123">Remove node pool without prompt</span></span>

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

### <span data-ttu-id="07cf2-124">-ID</span><span class="sxs-lookup"><span data-stu-id="07cf2-124">-Id</span></span>
<span data-ttu-id="07cf2-125">Yönetilen Kubernetes kümesindeki bir düğüm havuzunun kimliği</span><span class="sxs-lookup"><span data-stu-id="07cf2-125">Id of an node pool in managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07cf2-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07cf2-126">-InputObject</span></span>
<span data-ttu-id="07cf2-127">Normalde ardışık düzen aracılığıyla iletilen PSAgentPool nesnesi.</span><span class="sxs-lookup"><span data-stu-id="07cf2-127">A PSAgentPool object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="07cf2-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="07cf2-128">-Name</span></span>
<span data-ttu-id="07cf2-129">Düğüm havuzunuzun adı</span><span class="sxs-lookup"><span data-stu-id="07cf2-129">Name of your node pool</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet, ParentObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07cf2-130">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="07cf2-130">-PassThru</span></span>
<span data-ttu-id="07cf2-131">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="07cf2-131">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="07cf2-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07cf2-132">-ResourceGroupName</span></span>
<span data-ttu-id="07cf2-133">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="07cf2-133">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07cf2-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="07cf2-134">-Confirm</span></span>
<span data-ttu-id="07cf2-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="07cf2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07cf2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07cf2-136">-WhatIf</span></span>
<span data-ttu-id="07cf2-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="07cf2-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07cf2-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="07cf2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07cf2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07cf2-139">CommonParameters</span></span>
<span data-ttu-id="07cf2-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="07cf2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07cf2-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="07cf2-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07cf2-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="07cf2-142">INPUTS</span></span>

### <span data-ttu-id="07cf2-143">Microsoft. Azure. Commands. aks. modeller. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="07cf2-143">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="07cf2-144">System. String</span><span class="sxs-lookup"><span data-stu-id="07cf2-144">System.String</span></span>

## <span data-ttu-id="07cf2-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="07cf2-145">OUTPUTS</span></span>

### <span data-ttu-id="07cf2-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="07cf2-146">System.Boolean</span></span>

## <span data-ttu-id="07cf2-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="07cf2-147">NOTES</span></span>

## <span data-ttu-id="07cf2-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="07cf2-148">RELATED LINKS</span></span>
