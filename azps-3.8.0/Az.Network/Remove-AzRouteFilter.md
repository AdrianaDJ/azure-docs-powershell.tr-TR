---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
ms.openlocfilehash: dc6af2cb623e2d2d67b337e3a6e3ff27b5aebd69
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103988"
---
# <span data-ttu-id="c6477-101">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c6477-101">Remove-AzRouteFilter</span></span>

## <span data-ttu-id="c6477-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6477-102">SYNOPSIS</span></span>
<span data-ttu-id="c6477-103">Yol süzgecini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c6477-103">Removes a route filter.</span></span>

## <span data-ttu-id="c6477-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c6477-104">SYNTAX</span></span>

```
Remove-AzRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6477-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c6477-105">DESCRIPTION</span></span>
<span data-ttu-id="c6477-106">**Remove-AzRouteFilter** cmdlet 'i bir yol süzgecini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c6477-106">The **Remove-AzRouteFilter** cmdlet removes a route filter.</span></span>

## <span data-ttu-id="c6477-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c6477-107">EXAMPLES</span></span>

### <span data-ttu-id="c6477-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c6477-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="c6477-109">Komut, ResourceGroup01 adındaki kaynak grubundaki RouteFilter01 adındaki yol filtresini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c6477-109">The command removes the route filter named RouteFilter01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="c6477-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c6477-110">PARAMETERS</span></span>

### <span data-ttu-id="c6477-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6477-111">-DefaultProfile</span></span>
<span data-ttu-id="c6477-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c6477-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6477-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c6477-113">-Force</span></span>
<span data-ttu-id="c6477-114">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="c6477-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c6477-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="c6477-115">-Name</span></span>
<span data-ttu-id="c6477-116">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="c6477-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6477-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c6477-117">-PassThru</span></span>
<span data-ttu-id="c6477-118">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="c6477-118">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="c6477-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6477-119">-ResourceGroupName</span></span>
<span data-ttu-id="c6477-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="c6477-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6477-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="c6477-121">-Confirm</span></span>
<span data-ttu-id="c6477-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c6477-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6477-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6477-123">-WhatIf</span></span>
<span data-ttu-id="c6477-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c6477-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6477-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c6477-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6477-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6477-126">CommonParameters</span></span>
<span data-ttu-id="c6477-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c6477-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6477-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6477-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6477-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c6477-129">INPUTS</span></span>

### <span data-ttu-id="c6477-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c6477-130">System.String</span></span>

## <span data-ttu-id="c6477-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c6477-131">OUTPUTS</span></span>

### <span data-ttu-id="c6477-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c6477-132">System.Boolean</span></span>

## <span data-ttu-id="c6477-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c6477-133">NOTES</span></span>

## <span data-ttu-id="c6477-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c6477-134">RELATED LINKS</span></span>

[<span data-ttu-id="c6477-135">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c6477-135">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="c6477-136">Yeni-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c6477-136">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="c6477-137">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c6477-137">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="c6477-138">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c6477-138">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="c6477-139">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c6477-139">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="c6477-140">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c6477-140">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="c6477-141">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c6477-141">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="c6477-142">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c6477-142">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
