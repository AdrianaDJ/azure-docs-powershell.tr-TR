---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: fd4dc0dd771029951da4ae375141cc526301de34
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274427"
---
# <span data-ttu-id="a9be7-101">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="a9be7-101">New-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="a9be7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9be7-102">SYNOPSIS</span></span>
<span data-ttu-id="a9be7-103">özel bağlantı kapsamlı kaynak için oluşturma</span><span class="sxs-lookup"><span data-stu-id="a9be7-103">create for private link scoped resource</span></span>

## <span data-ttu-id="a9be7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a9be7-104">SYNTAX</span></span>

### <span data-ttu-id="a9be7-105">ByResourceNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a9be7-105">ByResourceNameParameterSet (Default)</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -ResourceGroupName <String>
 -ScopeName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a9be7-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9be7-106">ByInputObjectParameterSet</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -Name <String>
 -InputObject <PSMonitorPrivateLinkScope> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a9be7-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a9be7-107">DESCRIPTION</span></span>
<span data-ttu-id="a9be7-108">özel bağlantı kapsamlı kaynak için oluşturma, kapsam dışı kaynak Log Analytics çalışma alanı veya Application Insights bileşeni olabilir</span><span class="sxs-lookup"><span data-stu-id="a9be7-108">create for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="a9be7-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a9be7-109">EXAMPLES</span></span>

### <span data-ttu-id="a9be7-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a9be7-110">Example 1</span></span>
```powershell
$ai = Get-AzApplicationInsights -ResourceGroupName "rg_name" -Name "ai_name"

New-AzInsightsPrivateLinkScopedResource -LinkedResourceId $ai.Id -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="a9be7-111">"scoped_resource_name ai_name" kapsam kaynağı oluşturma</span><span class="sxs-lookup"><span data-stu-id="a9be7-111">create scoped resource "scoped_resource_name" linked to application insights component "ai_name"</span></span>

## <span data-ttu-id="a9be7-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a9be7-112">PARAMETERS</span></span>

### <span data-ttu-id="a9be7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9be7-113">-DefaultProfile</span></span>
<span data-ttu-id="a9be7-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a9be7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9be7-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9be7-115">-InputObject</span></span>
<span data-ttu-id="a9be7-116">Psmik ıtorprivatelinkscope</span><span class="sxs-lookup"><span data-stu-id="a9be7-116">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="a9be7-117">-Linkedresourceıd</span><span class="sxs-lookup"><span data-stu-id="a9be7-117">-LinkedResourceId</span></span>
<span data-ttu-id="a9be7-118">Bağlanılacak LA/AI kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="a9be7-118">LA/AI Resource Id to Link</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9be7-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="a9be7-119">-Name</span></span>
<span data-ttu-id="a9be7-120">Kapsamlı kaynak adı</span><span class="sxs-lookup"><span data-stu-id="a9be7-120">Scoped resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9be7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9be7-121">-ResourceGroupName</span></span>
<span data-ttu-id="a9be7-122">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="a9be7-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9be7-123">-Kapsamadı</span><span class="sxs-lookup"><span data-stu-id="a9be7-123">-ScopeName</span></span>
<span data-ttu-id="a9be7-124">Özel bağlantı kapsamı adı</span><span class="sxs-lookup"><span data-stu-id="a9be7-124">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9be7-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="a9be7-125">-Confirm</span></span>
<span data-ttu-id="a9be7-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a9be7-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9be7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9be7-127">-WhatIf</span></span>
<span data-ttu-id="a9be7-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a9be7-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9be7-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a9be7-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9be7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9be7-130">CommonParameters</span></span>
<span data-ttu-id="a9be7-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a9be7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9be7-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a9be7-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9be7-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a9be7-133">INPUTS</span></span>

### <span data-ttu-id="a9be7-134">Microsoft. Azure. Commands. Insights. OutputClasses. Psmte ıtorprivatelinkscope</span><span class="sxs-lookup"><span data-stu-id="a9be7-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="a9be7-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a9be7-135">System.String</span></span>

## <span data-ttu-id="a9be7-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a9be7-136">OUTPUTS</span></span>

### <span data-ttu-id="a9be7-137">Microsoft. Azure. Commands. Insights. OutputClasses. Psmiçıtorprivatelinkscopedresource</span><span class="sxs-lookup"><span data-stu-id="a9be7-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="a9be7-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a9be7-138">NOTES</span></span>

## <span data-ttu-id="a9be7-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a9be7-139">RELATED LINKS</span></span>
