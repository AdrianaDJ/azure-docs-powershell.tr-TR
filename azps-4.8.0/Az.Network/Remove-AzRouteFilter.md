---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
ms.openlocfilehash: dc6af2cb623e2d2d67b337e3a6e3ff27b5aebd69
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267016"
---
# <span data-ttu-id="f9abe-101">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f9abe-101">Remove-AzRouteFilter</span></span>

## <span data-ttu-id="f9abe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9abe-102">SYNOPSIS</span></span>
<span data-ttu-id="f9abe-103">Yol süzgecini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f9abe-103">Removes a route filter.</span></span>

## <span data-ttu-id="f9abe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f9abe-104">SYNTAX</span></span>

```
Remove-AzRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9abe-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f9abe-105">DESCRIPTION</span></span>
<span data-ttu-id="f9abe-106">**Remove-AzRouteFilter** cmdlet 'i bir yol süzgecini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f9abe-106">The **Remove-AzRouteFilter** cmdlet removes a route filter.</span></span>

## <span data-ttu-id="f9abe-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f9abe-107">EXAMPLES</span></span>

### <span data-ttu-id="f9abe-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f9abe-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f9abe-109">Komut, ResourceGroup01 adındaki kaynak grubundaki RouteFilter01 adındaki yol filtresini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f9abe-109">The command removes the route filter named RouteFilter01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="f9abe-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f9abe-110">PARAMETERS</span></span>

### <span data-ttu-id="f9abe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9abe-111">-DefaultProfile</span></span>
<span data-ttu-id="f9abe-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f9abe-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9abe-113">-Force</span><span class="sxs-lookup"><span data-stu-id="f9abe-113">-Force</span></span>
<span data-ttu-id="f9abe-114">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="f9abe-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f9abe-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="f9abe-115">-Name</span></span>
<span data-ttu-id="f9abe-116">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="f9abe-116">The resource name.</span></span>

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

### <span data-ttu-id="f9abe-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f9abe-117">-PassThru</span></span>
<span data-ttu-id="f9abe-118">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="f9abe-118">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="f9abe-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9abe-119">-ResourceGroupName</span></span>
<span data-ttu-id="f9abe-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f9abe-120">The resource group name.</span></span>

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

### <span data-ttu-id="f9abe-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="f9abe-121">-Confirm</span></span>
<span data-ttu-id="f9abe-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f9abe-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9abe-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9abe-123">-WhatIf</span></span>
<span data-ttu-id="f9abe-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f9abe-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9abe-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f9abe-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9abe-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9abe-126">CommonParameters</span></span>
<span data-ttu-id="f9abe-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f9abe-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9abe-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9abe-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9abe-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f9abe-129">INPUTS</span></span>

### <span data-ttu-id="f9abe-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f9abe-130">System.String</span></span>

## <span data-ttu-id="f9abe-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f9abe-131">OUTPUTS</span></span>

### <span data-ttu-id="f9abe-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f9abe-132">System.Boolean</span></span>

## <span data-ttu-id="f9abe-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f9abe-133">NOTES</span></span>

## <span data-ttu-id="f9abe-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f9abe-134">RELATED LINKS</span></span>

[<span data-ttu-id="f9abe-135">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f9abe-135">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="f9abe-136">Yeni-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f9abe-136">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="f9abe-137">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f9abe-137">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="f9abe-138">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f9abe-138">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="f9abe-139">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f9abe-139">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="f9abe-140">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f9abe-140">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="f9abe-141">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f9abe-141">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="f9abe-142">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f9abe-142">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
