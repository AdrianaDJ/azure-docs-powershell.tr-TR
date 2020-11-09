---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/disable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddon.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddon.md
ms.openlocfilehash: 0fca409546822ef596897adbbf755a1a4ae43e38
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94326065"
---
# <span data-ttu-id="0a9ef-101">Disable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="0a9ef-101">Disable-AzAksAddOn</span></span>

## <span data-ttu-id="0a9ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a9ef-102">SYNOPSIS</span></span>
<span data-ttu-id="0a9ef-103">Tüm eklentileri devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="0a9ef-103">Disable the addons for aks.</span></span>

## <span data-ttu-id="0a9ef-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0a9ef-104">SYNTAX</span></span>

### <span data-ttu-id="0a9ef-105">defaultParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0a9ef-105">defaultParameterSet (Default)</span></span>
```
Disable-AzAksAddOn [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a9ef-106">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="0a9ef-106">InputObjectParameterSet</span></span>
```
Disable-AzAksAddOn -ClusterObject <PSKubernetesCluster> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a9ef-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0a9ef-107">DESCRIPTION</span></span>
<span data-ttu-id="0a9ef-108">Tüm eklentileri devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="0a9ef-108">Disable the addons for aks.</span></span>

## <span data-ttu-id="0a9ef-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0a9ef-109">EXAMPLES</span></span>

### <span data-ttu-id="0a9ef-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0a9ef-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Disable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard
```

<span data-ttu-id="0a9ef-111">Eklentileri `HttpApplicationRouting` , `Monitoring` , `AzurePolicy` , `VirtualNode` ve gibi eklentileri devre dışı bırakın `KubeDashboard` .</span><span class="sxs-lookup"><span data-stu-id="0a9ef-111">Disable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="0a9ef-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0a9ef-112">PARAMETERS</span></span>

### <span data-ttu-id="0a9ef-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="0a9ef-113">-ClusterName</span></span>
<span data-ttu-id="0a9ef-114">Kubernetes yönetilen küme adı.</span><span class="sxs-lookup"><span data-stu-id="0a9ef-114">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a9ef-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="0a9ef-115">-ClusterObject</span></span>
<span data-ttu-id="0a9ef-116">Normalde ardışık düzen aracılığıyla iletilen bir PSKubernetesCluster nesnesi.</span><span class="sxs-lookup"><span data-stu-id="0a9ef-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a9ef-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a9ef-117">-DefaultProfile</span></span>
<span data-ttu-id="0a9ef-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0a9ef-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a9ef-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="0a9ef-119">-Name</span></span>
<span data-ttu-id="0a9ef-120">Kubernetes yönetilen küme adı.</span><span class="sxs-lookup"><span data-stu-id="0a9ef-120">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a9ef-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a9ef-121">-ResourceGroupName</span></span>
<span data-ttu-id="0a9ef-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="0a9ef-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a9ef-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="0a9ef-123">-Confirm</span></span>
<span data-ttu-id="0a9ef-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0a9ef-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a9ef-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a9ef-125">-WhatIf</span></span>
<span data-ttu-id="0a9ef-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0a9ef-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a9ef-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0a9ef-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a9ef-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a9ef-128">CommonParameters</span></span>
<span data-ttu-id="0a9ef-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0a9ef-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a9ef-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0a9ef-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a9ef-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0a9ef-131">INPUTS</span></span>

### <span data-ttu-id="0a9ef-132">Microsoft. Azure. Commands. aks. modeller. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="0a9ef-132">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="0a9ef-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0a9ef-133">System.String</span></span>

## <span data-ttu-id="0a9ef-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0a9ef-134">OUTPUTS</span></span>

### <span data-ttu-id="0a9ef-135">Microsoft. Azure. Commands. aks. modeller. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="0a9ef-135">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="0a9ef-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0a9ef-136">NOTES</span></span>

## <span data-ttu-id="0a9ef-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0a9ef-137">RELATED LINKS</span></span>
