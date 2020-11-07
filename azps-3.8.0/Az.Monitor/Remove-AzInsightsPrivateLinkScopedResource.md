---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: cd71f1561525f166736b708caf4905fdefd443ce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937281"
---
# <span data-ttu-id="e5e50-101">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="e5e50-101">Remove-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="e5e50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5e50-102">SYNOPSIS</span></span>
<span data-ttu-id="e5e50-103">özel bağlantı kapsamlı kaynak için silme</span><span class="sxs-lookup"><span data-stu-id="e5e50-103">delete for private link scoped resource</span></span>

## <span data-ttu-id="e5e50-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e5e50-104">SYNTAX</span></span>

### <span data-ttu-id="e5e50-105">ByScopeParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e5e50-105">ByScopeParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5e50-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5e50-106">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -Name <String> -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5e50-107">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="e5e50-107">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5e50-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e5e50-108">DESCRIPTION</span></span>
<span data-ttu-id="e5e50-109">özel bağlantı kapsamlı kaynak için silme</span><span class="sxs-lookup"><span data-stu-id="e5e50-109">delete for private link scoped resource</span></span>

## <span data-ttu-id="e5e50-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e5e50-110">EXAMPLES</span></span>

### <span data-ttu-id="e5e50-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e5e50-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="e5e50-112">özel bağlantı kapsamlı kaynağı silme</span><span class="sxs-lookup"><span data-stu-id="e5e50-112">delete private link scoped resource</span></span>

## <span data-ttu-id="e5e50-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e5e50-113">PARAMETERS</span></span>

### <span data-ttu-id="e5e50-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5e50-114">-DefaultProfile</span></span>
<span data-ttu-id="e5e50-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e5e50-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5e50-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5e50-116">-InputObject</span></span>
<span data-ttu-id="e5e50-117">Psmik ıtorprivatelinkscope</span><span class="sxs-lookup"><span data-stu-id="e5e50-117">PSMonitorPrivateLinkScope</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5e50-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="e5e50-118">-Name</span></span>
<span data-ttu-id="e5e50-119">Kapsamlı kaynak adı</span><span class="sxs-lookup"><span data-stu-id="e5e50-119">Scoped resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet, ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5e50-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5e50-120">-ResourceGroupName</span></span>
<span data-ttu-id="e5e50-121">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="e5e50-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5e50-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e5e50-122">-ResourceId</span></span>
<span data-ttu-id="e5e50-123">Kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="e5e50-123">Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5e50-124">-Kapsamadı</span><span class="sxs-lookup"><span data-stu-id="e5e50-124">-ScopeName</span></span>
<span data-ttu-id="e5e50-125">Özel bağlantı kapsamı adı</span><span class="sxs-lookup"><span data-stu-id="e5e50-125">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5e50-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="e5e50-126">-Confirm</span></span>
<span data-ttu-id="e5e50-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e5e50-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5e50-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5e50-128">-WhatIf</span></span>
<span data-ttu-id="e5e50-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e5e50-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5e50-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e5e50-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5e50-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5e50-131">CommonParameters</span></span>
<span data-ttu-id="e5e50-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e5e50-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5e50-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e5e50-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5e50-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e5e50-134">INPUTS</span></span>

### <span data-ttu-id="e5e50-135">Microsoft. Azure. Commands. Insights. OutputClasses. Psmte ıtorprivatelinkscope</span><span class="sxs-lookup"><span data-stu-id="e5e50-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="e5e50-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e5e50-136">System.String</span></span>

## <span data-ttu-id="e5e50-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e5e50-137">OUTPUTS</span></span>

### <span data-ttu-id="e5e50-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e5e50-138">System.Boolean</span></span>

## <span data-ttu-id="e5e50-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e5e50-139">NOTES</span></span>

## <span data-ttu-id="e5e50-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e5e50-140">RELATED LINKS</span></span>
