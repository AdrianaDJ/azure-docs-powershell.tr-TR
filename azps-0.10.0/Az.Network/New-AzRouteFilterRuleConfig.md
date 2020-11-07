---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 6f8943fb4e75c96a97ad2b7f128d671a8be7c906
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935362"
---
# <span data-ttu-id="dc631-101">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dc631-101">New-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="dc631-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc631-102">SYNOPSIS</span></span>
<span data-ttu-id="dc631-103">Yol filtresi için bir yol filtre kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dc631-103">Creates a route filter rule for a route filter.</span></span>

## <span data-ttu-id="dc631-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dc631-104">SYNTAX</span></span>

```
New-AzRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc631-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dc631-105">DESCRIPTION</span></span>
<span data-ttu-id="dc631-106">New-AzRouteFilterRuleConfig cmdlet 'i Azure yol filtresi için bir yol filtresi kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dc631-106">The New-AzRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="dc631-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dc631-107">EXAMPLES</span></span>

### <span data-ttu-id="dc631-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dc631-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="dc631-109">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="dc631-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="dc631-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dc631-110">PARAMETERS</span></span>

### <span data-ttu-id="dc631-111">-Access</span><span class="sxs-lookup"><span data-stu-id="dc631-111">-Access</span></span>
<span data-ttu-id="dc631-112">Yol filtresi kuralı erişimi.</span><span class="sxs-lookup"><span data-stu-id="dc631-112">Access for route filter rule.</span></span>
<span data-ttu-id="dc631-113">Geçerli değerler Izin ver veya Reddet.</span><span class="sxs-lookup"><span data-stu-id="dc631-113">Valid values are Allow or Deny.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc631-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="dc631-114">-CommunityList</span></span>
<span data-ttu-id="dc631-115">Yol süzgecinin filtrelendirilecektir topluluk değeri listesi</span><span class="sxs-lookup"><span data-stu-id="dc631-115">The list of community value that route filter will filter on</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc631-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc631-116">-DefaultProfile</span></span>
<span data-ttu-id="dc631-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dc631-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc631-118">-Force</span><span class="sxs-lookup"><span data-stu-id="dc631-118">-Force</span></span>
<span data-ttu-id="dc631-119">Kaynağın üzerine yazılsın mı?</span><span class="sxs-lookup"><span data-stu-id="dc631-119">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc631-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="dc631-120">-Name</span></span>
<span data-ttu-id="dc631-121">Yol filtresi kuralı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="dc631-121">Specifies a name for the route filter rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc631-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="dc631-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="dc631-123">Yol filtre kuralı türü.</span><span class="sxs-lookup"><span data-stu-id="dc631-123">Route Filter Rule Type.</span></span>
<span data-ttu-id="dc631-124">Geçerli değerler: topluluk</span><span class="sxs-lookup"><span data-stu-id="dc631-124">Valid values are: Community</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc631-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="dc631-125">-Confirm</span></span>
<span data-ttu-id="dc631-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dc631-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc631-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc631-127">-WhatIf</span></span>
<span data-ttu-id="dc631-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dc631-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dc631-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dc631-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc631-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc631-130">CommonParameters</span></span>
<span data-ttu-id="dc631-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dc631-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc631-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc631-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc631-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dc631-133">INPUTS</span></span>

## <span data-ttu-id="dc631-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dc631-134">OUTPUTS</span></span>

### <span data-ttu-id="dc631-135">Microsoft. Azure. Commands. Network. model. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="dc631-135">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="dc631-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dc631-136">NOTES</span></span>
<span data-ttu-id="dc631-137">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="dc631-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="dc631-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dc631-138">RELATED LINKS</span></span>

[<span data-ttu-id="dc631-139">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dc631-139">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="dc631-140">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dc631-140">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="dc631-141">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dc631-141">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="dc631-142">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dc631-142">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

