---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/enable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddon.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddon.md
ms.openlocfilehash: de4453129ee626ac7eeeaa20fa14c1068011c001
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277898"
---
# <span data-ttu-id="b7385-101">Enable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="b7385-101">Enable-AzAksAddOn</span></span>

## <span data-ttu-id="b7385-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7385-102">SYNOPSIS</span></span>
<span data-ttu-id="b7385-103">Eklentiler için eklentiler 'i etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="b7385-103">Enable the addons for aks.</span></span>

## <span data-ttu-id="b7385-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b7385-104">SYNTAX</span></span>

### <span data-ttu-id="b7385-105">defaultParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b7385-105">defaultParameterSet (Default)</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] [-ResourceGroupName] <String>
 [-ClusterName] <String> [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b7385-106">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="b7385-106">InputObjectParameterSet</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] -ClusterObject <PSKubernetesCluster>
 [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7385-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b7385-107">DESCRIPTION</span></span>
<span data-ttu-id="b7385-108">Eklentiler için eklentiler 'i etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="b7385-108">Enable the addons for aks.</span></span>

## <span data-ttu-id="b7385-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b7385-109">EXAMPLES</span></span>

### <span data-ttu-id="b7385-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b7385-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Enable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard -WorkspaceResourceId xxxxx/xxxx -SubnetName subnet
```

<span data-ttu-id="b7385-111">Eklentileri `HttpApplicationRouting` , `Monitoring` , `AzurePolicy` ve gibi eklentileri etkinleştirin `VirtualNode` `KubeDashboard` .</span><span class="sxs-lookup"><span data-stu-id="b7385-111">Enable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="b7385-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b7385-112">PARAMETERS</span></span>

### <span data-ttu-id="b7385-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b7385-113">-ClusterName</span></span>
<span data-ttu-id="b7385-114">Kubernetes yönetilen küme adı.</span><span class="sxs-lookup"><span data-stu-id="b7385-114">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="b7385-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="b7385-115">-ClusterObject</span></span>
<span data-ttu-id="b7385-116">Normalde ardışık düzen aracılığıyla iletilen bir PSKubernetesCluster nesnesi.</span><span class="sxs-lookup"><span data-stu-id="b7385-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="b7385-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7385-117">-DefaultProfile</span></span>
<span data-ttu-id="b7385-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b7385-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7385-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="b7385-119">-Name</span></span>
<span data-ttu-id="b7385-120">Kubernetes yönetilen küme adı.</span><span class="sxs-lookup"><span data-stu-id="b7385-120">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="b7385-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7385-121">-ResourceGroupName</span></span>
<span data-ttu-id="b7385-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b7385-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="b7385-123">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="b7385-123">-SubnetName</span></span>
<span data-ttu-id="b7385-124">VirtualNode 'un alt ağ adı.</span><span class="sxs-lookup"><span data-stu-id="b7385-124">Subnet name of VirtualNode.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7385-125">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="b7385-125">-WorkspaceResourceId</span></span>
<span data-ttu-id="b7385-126">Çalışma alanının kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="b7385-126">Resource Id of the workspace of Monitoring.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7385-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="b7385-127">-Confirm</span></span>
<span data-ttu-id="b7385-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b7385-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7385-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7385-129">-WhatIf</span></span>
<span data-ttu-id="b7385-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b7385-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7385-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b7385-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7385-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7385-132">CommonParameters</span></span>
<span data-ttu-id="b7385-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b7385-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7385-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b7385-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7385-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b7385-135">INPUTS</span></span>

### <span data-ttu-id="b7385-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b7385-136">System.String</span></span>

### <span data-ttu-id="b7385-137">Microsoft. Azure. Commands. aks. modeller. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="b7385-137">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="b7385-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b7385-138">OUTPUTS</span></span>

### <span data-ttu-id="b7385-139">Microsoft. Azure. Commands. aks. modeller. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="b7385-139">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="b7385-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b7385-140">NOTES</span></span>

## <span data-ttu-id="b7385-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b7385-141">RELATED LINKS</span></span>
