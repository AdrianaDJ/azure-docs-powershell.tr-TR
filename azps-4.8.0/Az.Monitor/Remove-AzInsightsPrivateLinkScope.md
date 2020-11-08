---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 358eb796a156949520cf8cf0c073ee08a6537e2f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267272"
---
# <span data-ttu-id="ff377-101">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="ff377-101">Remove-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="ff377-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff377-102">SYNOPSIS</span></span>
<span data-ttu-id="ff377-103">özel bağlantı kapsamını silme</span><span class="sxs-lookup"><span data-stu-id="ff377-103">delete private link scope</span></span>

## <span data-ttu-id="ff377-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ff377-104">SYNTAX</span></span>

### <span data-ttu-id="ff377-105">ByResourceNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ff377-105">ByResourceNameParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff377-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="ff377-106">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff377-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff377-107">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff377-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ff377-108">DESCRIPTION</span></span>
<span data-ttu-id="ff377-109">özel bağlantı kapsamını silme</span><span class="sxs-lookup"><span data-stu-id="ff377-109">delete private link scope</span></span>

## <span data-ttu-id="ff377-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ff377-110">EXAMPLES</span></span>

### <span data-ttu-id="ff377-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ff377-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="ff377-112">"scope_name" kaynak grubu altındaki "rg_name" adlı özel bağlantı kapsamını silme</span><span class="sxs-lookup"><span data-stu-id="ff377-112">delete private link scope with name "scope_name" under resource group "rg_name"</span></span>

### <span data-ttu-id="ff377-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="ff377-113">Example 2</span></span>
```powershell
Remove-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name"
```

<span data-ttu-id="ff377-114">Kaynak kimliğiyle özel bağlantı kapsamını silme</span><span class="sxs-lookup"><span data-stu-id="ff377-114">delete private link scope with resource Id</span></span>

### <span data-ttu-id="ff377-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="ff377-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Remove-AzInsightsPrivateLinkScope
```

<span data-ttu-id="ff377-116">özel bağlantı kapsamını giriş özel bağlantı kapsamı nesnesiyle silme</span><span class="sxs-lookup"><span data-stu-id="ff377-116">delete private link scope with input private link scope object</span></span>

## <span data-ttu-id="ff377-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ff377-117">PARAMETERS</span></span>

### <span data-ttu-id="ff377-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff377-118">-DefaultProfile</span></span>
<span data-ttu-id="ff377-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ff377-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff377-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff377-120">-InputObject</span></span>
<span data-ttu-id="ff377-121">Psmik ıtorprivatelinkscope</span><span class="sxs-lookup"><span data-stu-id="ff377-121">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="ff377-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="ff377-122">-Name</span></span>
<span data-ttu-id="ff377-123">Özel bağlantı kapsamı adı</span><span class="sxs-lookup"><span data-stu-id="ff377-123">Private Link Scope Name</span></span>

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

### <span data-ttu-id="ff377-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff377-124">-ResourceGroupName</span></span>
<span data-ttu-id="ff377-125">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="ff377-125">Resource Group Name</span></span>

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

### <span data-ttu-id="ff377-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ff377-126">-ResourceId</span></span>
<span data-ttu-id="ff377-127">Kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="ff377-127">Resource Id</span></span>

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

### <span data-ttu-id="ff377-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="ff377-128">-Confirm</span></span>
<span data-ttu-id="ff377-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ff377-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff377-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff377-130">-WhatIf</span></span>
<span data-ttu-id="ff377-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ff377-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff377-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ff377-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff377-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff377-133">CommonParameters</span></span>
<span data-ttu-id="ff377-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ff377-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff377-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ff377-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff377-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ff377-136">INPUTS</span></span>

### <span data-ttu-id="ff377-137">Microsoft. Azure. Commands. Insights. OutputClasses. Psmte ıtorprivatelinkscope</span><span class="sxs-lookup"><span data-stu-id="ff377-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="ff377-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ff377-138">System.String</span></span>

## <span data-ttu-id="ff377-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ff377-139">OUTPUTS</span></span>

### <span data-ttu-id="ff377-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ff377-140">System.Boolean</span></span>

## <span data-ttu-id="ff377-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ff377-141">NOTES</span></span>

## <span data-ttu-id="ff377-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ff377-142">RELATED LINKS</span></span>
