---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/update-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 93e97906fc7e985d522f5af9d678392741a9022b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937263"
---
# <span data-ttu-id="49976-101">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="49976-101">Update-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="49976-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49976-102">SYNOPSIS</span></span>
<span data-ttu-id="49976-103">Özel bağlantı kapsamı güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="49976-103">Update for private link scope</span></span>

## <span data-ttu-id="49976-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="49976-104">SYNTAX</span></span>

### <span data-ttu-id="49976-105">ByResourceNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="49976-105">ByResourceNameParameterSet (Default)</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49976-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="49976-106">ByResourceIdParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceId <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49976-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="49976-107">ByInputObjectParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49976-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="49976-108">DESCRIPTION</span></span>
<span data-ttu-id="49976-109">Özel bağlantı kapsamı güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="49976-109">Update for private link scope</span></span>

## <span data-ttu-id="49976-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="49976-110">EXAMPLES</span></span>

### <span data-ttu-id="49976-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="49976-111">Example 1</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" -Tags "key:value"
```

<span data-ttu-id="49976-112">"rg_name" kaynak grubu altındaki "scope_name" adlı özel bağlantı kapsamını "anahtar: değer" olarak güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="49976-112">update private link scope with name "scope_name" under resource group "rg_name" to use tag "key:value"</span></span>

### <span data-ttu-id="49976-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="49976-113">Example 2</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name" -Tags "key:value"
```

<span data-ttu-id="49976-114">özel bağlantı kapsamını kaynak kimliğiyle güncelleştirmek için "anahtar: değer" etiketini kullanma</span><span class="sxs-lookup"><span data-stu-id="49976-114">update private link scope with resource Id to use tag "key:value"</span></span>

### <span data-ttu-id="49976-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="49976-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Update-AzInsightsPrivateLinkScope -Tags "key:value"
```

<span data-ttu-id="49976-116">özel bağlantı kapsamını giriş özel bağlantı kapsamı nesnesiyle "anahtar: değer" etiketini kullanacak şekilde Güncelleştir</span><span class="sxs-lookup"><span data-stu-id="49976-116">update private link scope with input private link scope object to use tag "key:value"</span></span>

## <span data-ttu-id="49976-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="49976-117">PARAMETERS</span></span>

### <span data-ttu-id="49976-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49976-118">-DefaultProfile</span></span>
<span data-ttu-id="49976-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="49976-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49976-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49976-120">-InputObject</span></span>
<span data-ttu-id="49976-121">Psmik ıtorprivatelinkscope</span><span class="sxs-lookup"><span data-stu-id="49976-121">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="49976-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="49976-122">-Name</span></span>
<span data-ttu-id="49976-123">Özel bağlantı kapsamı adı</span><span class="sxs-lookup"><span data-stu-id="49976-123">Private Link Scope Name</span></span>

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

### <span data-ttu-id="49976-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49976-124">-ResourceGroupName</span></span>
<span data-ttu-id="49976-125">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="49976-125">Resource Group Name</span></span>

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

### <span data-ttu-id="49976-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="49976-126">-ResourceId</span></span>
<span data-ttu-id="49976-127">Kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="49976-127">Resource Id</span></span>

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

### <span data-ttu-id="49976-128">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="49976-128">-Tags</span></span>
<span data-ttu-id="49976-129">Akıllı</span><span class="sxs-lookup"><span data-stu-id="49976-129">Tags</span></span>

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

### <span data-ttu-id="49976-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="49976-130">-Confirm</span></span>
<span data-ttu-id="49976-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="49976-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49976-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49976-132">-WhatIf</span></span>
<span data-ttu-id="49976-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="49976-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49976-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="49976-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49976-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49976-135">CommonParameters</span></span>
<span data-ttu-id="49976-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="49976-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49976-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="49976-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49976-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="49976-138">INPUTS</span></span>

### <span data-ttu-id="49976-139">Microsoft. Azure. Commands. Insights. OutputClasses. Psmte ıtorprivatelinkscope</span><span class="sxs-lookup"><span data-stu-id="49976-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="49976-140">System. String</span><span class="sxs-lookup"><span data-stu-id="49976-140">System.String</span></span>

## <span data-ttu-id="49976-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="49976-141">OUTPUTS</span></span>

### <span data-ttu-id="49976-142">Microsoft. Azure. Commands. Insights. OutputClasses. Psmte ıtorprivatelinkscope</span><span class="sxs-lookup"><span data-stu-id="49976-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="49976-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="49976-143">NOTES</span></span>

## <span data-ttu-id="49976-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="49976-144">RELATED LINKS</span></span>