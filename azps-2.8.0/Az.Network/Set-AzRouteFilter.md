---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
ms.openlocfilehash: ab0da083957fe18d1bb30d0b3d08d33515d0ff13
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932748"
---
# <span data-ttu-id="4b08d-101">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4b08d-101">Set-AzRouteFilter</span></span>

## <span data-ttu-id="4b08d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b08d-102">SYNOPSIS</span></span>
<span data-ttu-id="4b08d-103">Bir yol filtresi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4b08d-103">Updates a route filter.</span></span>

## <span data-ttu-id="4b08d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4b08d-104">SYNTAX</span></span>

```
Set-AzRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b08d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4b08d-105">DESCRIPTION</span></span>
<span data-ttu-id="4b08d-106">**Set-AzApplicationGateway** cmdlet 'i bir yol filtresini güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="4b08d-106">The **Set-AzApplicationGateway** cmdlet updates a route filter</span></span>

## <span data-ttu-id="4b08d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4b08d-107">EXAMPLES</span></span>

### <span data-ttu-id="4b08d-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4b08d-108">Example 1</span></span>
```powershell
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="4b08d-109">Bu komut, $rf değişkenindeki ayarlar ile yol filtresini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4b08d-109">This command updates the route filter with settings in the $rf variable.</span></span>

## <span data-ttu-id="4b08d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4b08d-110">PARAMETERS</span></span>

### <span data-ttu-id="4b08d-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="4b08d-111">-AsJob</span></span>
<span data-ttu-id="4b08d-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="4b08d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4b08d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b08d-113">-DefaultProfile</span></span>
<span data-ttu-id="4b08d-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4b08d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b08d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4b08d-115">-Force</span></span>
<span data-ttu-id="4b08d-116">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="4b08d-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="4b08d-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="4b08d-117">-RouteFilter</span></span>
<span data-ttu-id="4b08d-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="4b08d-118">The RouteFilter</span></span>

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

### <span data-ttu-id="4b08d-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="4b08d-119">-Confirm</span></span>
<span data-ttu-id="4b08d-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4b08d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b08d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b08d-121">-WhatIf</span></span>
<span data-ttu-id="4b08d-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4b08d-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4b08d-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4b08d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b08d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b08d-124">CommonParameters</span></span>
<span data-ttu-id="4b08d-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4b08d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b08d-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b08d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b08d-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4b08d-127">INPUTS</span></span>

### <span data-ttu-id="4b08d-128">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4b08d-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="4b08d-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4b08d-129">OUTPUTS</span></span>

### <span data-ttu-id="4b08d-130">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4b08d-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="4b08d-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4b08d-131">NOTES</span></span>

## <span data-ttu-id="4b08d-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4b08d-132">RELATED LINKS</span></span>

[<span data-ttu-id="4b08d-133">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4b08d-133">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="4b08d-134">Yeni-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4b08d-134">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="4b08d-135">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4b08d-135">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="4b08d-136">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4b08d-136">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="4b08d-137">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4b08d-137">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="4b08d-138">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4b08d-138">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="4b08d-139">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4b08d-139">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="4b08d-140">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4b08d-140">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
