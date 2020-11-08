---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: f3d00ba82bbafce42cca49c60d443cd244f83df3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097348"
---
# <span data-ttu-id="107b3-101">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="107b3-101">Get-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="107b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="107b3-102">SYNOPSIS</span></span>
<span data-ttu-id="107b3-103">Özel bağlantı kapsamlı kaynak için al</span><span class="sxs-lookup"><span data-stu-id="107b3-103">Get for private link scoped resource</span></span>

## <span data-ttu-id="107b3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="107b3-104">SYNTAX</span></span>

### <span data-ttu-id="107b3-105">ByScopeParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="107b3-105">ByScopeParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="107b3-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="107b3-106">ByInputObjectParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource [-Name <String>] -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="107b3-107">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="107b3-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="107b3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="107b3-108">DESCRIPTION</span></span>
<span data-ttu-id="107b3-109">Özel bağlantı kapsamlı kaynak için Get veya liste, kapsam dışı kaynak Log Analytics çalışma alanı veya Application Insights bileşeni olabilir</span><span class="sxs-lookup"><span data-stu-id="107b3-109">Get or list for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="107b3-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="107b3-110">EXAMPLES</span></span>

### <span data-ttu-id="107b3-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="107b3-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name"
```

<span data-ttu-id="107b3-112">"Scope_name" özel bağlantı kapsamı altındaki kapsamlı kaynak kaynağı</span><span class="sxs-lookup"><span data-stu-id="107b3-112">List scoped resource under private link scope "scope_name"</span></span>

### <span data-ttu-id="107b3-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="107b3-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="107b3-114">"Scoped_resource_name" adlı "scope_name" özel bağlantı kapsamında kapsam kaynağı alın</span><span class="sxs-lookup"><span data-stu-id="107b3-114">Get scoped resource under private link scope "scope_name" with name "scoped_resource_name"</span></span>

## <span data-ttu-id="107b3-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="107b3-115">PARAMETERS</span></span>

### <span data-ttu-id="107b3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="107b3-116">-DefaultProfile</span></span>
<span data-ttu-id="107b3-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="107b3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="107b3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="107b3-118">-InputObject</span></span>
<span data-ttu-id="107b3-119">Psmik ıtorprivatelinkscope</span><span class="sxs-lookup"><span data-stu-id="107b3-119">PSMonitorPrivateLinkScope</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="107b3-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="107b3-120">-Name</span></span>
<span data-ttu-id="107b3-121">Kapsamlı kaynak adı</span><span class="sxs-lookup"><span data-stu-id="107b3-121">Scoped resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet, ByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="107b3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="107b3-122">-ResourceGroupName</span></span>
<span data-ttu-id="107b3-123">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="107b3-123">Resource Group Name</span></span>

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

### <span data-ttu-id="107b3-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="107b3-124">-ResourceId</span></span>
<span data-ttu-id="107b3-125">Kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="107b3-125">Resource Id</span></span>

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

### <span data-ttu-id="107b3-126">-Kapsamadı</span><span class="sxs-lookup"><span data-stu-id="107b3-126">-ScopeName</span></span>
<span data-ttu-id="107b3-127">Özel bağlantı kapsamı adı</span><span class="sxs-lookup"><span data-stu-id="107b3-127">Private Link Scope Name</span></span>

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

### <span data-ttu-id="107b3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="107b3-128">CommonParameters</span></span>
<span data-ttu-id="107b3-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="107b3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="107b3-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="107b3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="107b3-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="107b3-131">INPUTS</span></span>

### <span data-ttu-id="107b3-132">System. String</span><span class="sxs-lookup"><span data-stu-id="107b3-132">System.String</span></span>

## <span data-ttu-id="107b3-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="107b3-133">OUTPUTS</span></span>

### <span data-ttu-id="107b3-134">icrosoft. Azure. Commands. Insights. OutputClasses. Psmiçıtorprivatelinkscopedresource</span><span class="sxs-lookup"><span data-stu-id="107b3-134">icrosoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="107b3-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="107b3-135">NOTES</span></span>

## <span data-ttu-id="107b3-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="107b3-136">RELATED LINKS</span></span>
