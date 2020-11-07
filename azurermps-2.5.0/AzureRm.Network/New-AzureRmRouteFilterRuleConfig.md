---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermroutefilterruleconfig
schema: 2.0.0
ms.openlocfilehash: 2309d49dcd91ddefbcbe0e40379a759d50d5ba2a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939910"
---
# <span data-ttu-id="b5670-101">New-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b5670-101">New-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="b5670-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5670-102">SYNOPSIS</span></span>
<span data-ttu-id="b5670-103">Yol filtresi için bir yol filtre kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b5670-103">Creates a route filter rule for a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5670-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b5670-104">SYNTAX</span></span>

```
New-AzureRmRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5670-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b5670-105">DESCRIPTION</span></span>
<span data-ttu-id="b5670-106">New-AzureRmRouteFilterRuleConfig cmdlet 'i Azure yol filtresi için bir yol filtresi kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b5670-106">The New-AzureRmRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="b5670-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b5670-107">EXAMPLES</span></span>

### <span data-ttu-id="b5670-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b5670-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="b5670-109">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="b5670-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="b5670-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b5670-110">PARAMETERS</span></span>

### <span data-ttu-id="b5670-111">-Access</span><span class="sxs-lookup"><span data-stu-id="b5670-111">-Access</span></span>
<span data-ttu-id="b5670-112">Yol filtresi kuralı erişimi.</span><span class="sxs-lookup"><span data-stu-id="b5670-112">Access for route filter rule.</span></span>
<span data-ttu-id="b5670-113">Geçerli değerler Izin ver veya Reddet.</span><span class="sxs-lookup"><span data-stu-id="b5670-113">Valid values are Allow or Deny.</span></span>

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

### <span data-ttu-id="b5670-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="b5670-114">-CommunityList</span></span>
<span data-ttu-id="b5670-115">Yol süzgecinin filtrelendirilecektir topluluk değeri listesi</span><span class="sxs-lookup"><span data-stu-id="b5670-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="b5670-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5670-116">-DefaultProfile</span></span>
<span data-ttu-id="b5670-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b5670-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5670-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b5670-118">-Force</span></span>
<span data-ttu-id="b5670-119">Kaynağın üzerine yazılsın mı?</span><span class="sxs-lookup"><span data-stu-id="b5670-119">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="b5670-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="b5670-120">-Name</span></span>
<span data-ttu-id="b5670-121">Yol filtresi kuralı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5670-121">Specifies a name for the route filter rule.</span></span>

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

### <span data-ttu-id="b5670-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="b5670-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="b5670-123">Yol filtre kuralı türü.</span><span class="sxs-lookup"><span data-stu-id="b5670-123">Route Filter Rule Type.</span></span>
<span data-ttu-id="b5670-124">Geçerli değerler: topluluk</span><span class="sxs-lookup"><span data-stu-id="b5670-124">Valid values are: Community</span></span>

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

### <span data-ttu-id="b5670-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="b5670-125">-Confirm</span></span>
<span data-ttu-id="b5670-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b5670-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5670-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5670-127">-WhatIf</span></span>
<span data-ttu-id="b5670-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b5670-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b5670-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b5670-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5670-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5670-130">CommonParameters</span></span>
<span data-ttu-id="b5670-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b5670-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5670-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5670-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5670-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b5670-133">INPUTS</span></span>

## <span data-ttu-id="b5670-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b5670-134">OUTPUTS</span></span>

### <span data-ttu-id="b5670-135">Microsoft. Azure. Commands. Network. model. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="b5670-135">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="b5670-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b5670-136">NOTES</span></span>
<span data-ttu-id="b5670-137">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="b5670-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="b5670-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b5670-138">RELATED LINKS</span></span>

[<span data-ttu-id="b5670-139">Add-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b5670-139">Add-AzureRmRouteFilterRuleConfig</span></span>](./Add-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="b5670-140">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b5670-140">Get-AzureRmRouteFilterRuleConfig</span></span>](./Get-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="b5670-141">Remove-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b5670-141">Remove-AzureRmRouteFilterRuleConfig</span></span>](./Remove-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="b5670-142">Set-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b5670-142">Set-AzureRmRouteFilterRuleConfig</span></span>](./Set-AzureRmRouteFilterRuleConfig.md)

