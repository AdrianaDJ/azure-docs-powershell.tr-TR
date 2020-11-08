---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
ms.openlocfilehash: f97b9ac971a4eec1945ae4418332e7d6ff74c71c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098562"
---
# <span data-ttu-id="98b18-101">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="98b18-101">Set-AzRouteFilter</span></span>

## <span data-ttu-id="98b18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98b18-102">SYNOPSIS</span></span>
<span data-ttu-id="98b18-103">Bir yol filtresi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="98b18-103">Updates a route filter.</span></span>

## <span data-ttu-id="98b18-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="98b18-104">SYNTAX</span></span>

```
Set-AzRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98b18-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="98b18-105">DESCRIPTION</span></span>
<span data-ttu-id="98b18-106">**Set-AzApplicationGateway** cmdlet 'i bir yol filtresini güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="98b18-106">The **Set-AzApplicationGateway** cmdlet updates a route filter</span></span>

## <span data-ttu-id="98b18-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="98b18-107">EXAMPLES</span></span>

### <span data-ttu-id="98b18-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="98b18-108">Example 1</span></span>
```powershell
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="98b18-109">Bu komut, $rf değişkenindeki ayarlar ile yol filtresini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="98b18-109">This command updates the route filter with settings in the $rf variable.</span></span>

## <span data-ttu-id="98b18-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="98b18-110">PARAMETERS</span></span>

### <span data-ttu-id="98b18-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="98b18-111">-AsJob</span></span>
<span data-ttu-id="98b18-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="98b18-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="98b18-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98b18-113">-DefaultProfile</span></span>
<span data-ttu-id="98b18-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="98b18-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98b18-115">-Force</span><span class="sxs-lookup"><span data-stu-id="98b18-115">-Force</span></span>
<span data-ttu-id="98b18-116">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="98b18-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="98b18-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="98b18-117">-RouteFilter</span></span>
<span data-ttu-id="98b18-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="98b18-118">The RouteFilter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98b18-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="98b18-119">-Confirm</span></span>
<span data-ttu-id="98b18-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="98b18-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98b18-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98b18-121">-WhatIf</span></span>
<span data-ttu-id="98b18-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="98b18-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="98b18-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="98b18-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98b18-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98b18-124">CommonParameters</span></span>
<span data-ttu-id="98b18-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="98b18-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98b18-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98b18-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98b18-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="98b18-127">INPUTS</span></span>

### <span data-ttu-id="98b18-128">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="98b18-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="98b18-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="98b18-129">OUTPUTS</span></span>

### <span data-ttu-id="98b18-130">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="98b18-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="98b18-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="98b18-131">NOTES</span></span>

## <span data-ttu-id="98b18-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="98b18-132">RELATED LINKS</span></span>

[<span data-ttu-id="98b18-133">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="98b18-133">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="98b18-134">Yeni-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="98b18-134">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="98b18-135">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="98b18-135">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="98b18-136">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="98b18-136">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="98b18-137">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="98b18-137">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="98b18-138">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="98b18-138">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="98b18-139">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="98b18-139">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="98b18-140">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="98b18-140">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)