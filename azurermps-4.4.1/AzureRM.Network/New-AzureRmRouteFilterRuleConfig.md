---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: 3c3e20762bcf8e48fc3f01d750419493a81ca8aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762435"
---
# <span data-ttu-id="9b808-101">New-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9b808-101">New-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="9b808-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b808-102">SYNOPSIS</span></span>
<span data-ttu-id="9b808-103">Yol filtresi için bir yol filtre kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9b808-103">Creates a route filter rule for a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b808-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9b808-104">SYNTAX</span></span>

```
New-AzureRmRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b808-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9b808-105">DESCRIPTION</span></span>
<span data-ttu-id="9b808-106">New-AzureRmRouteFilterRuleConfig cmdlet 'i Azure yol filtresi için bir yol filtresi kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9b808-106">The New-AzureRmRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="9b808-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9b808-107">EXAMPLES</span></span>

### <span data-ttu-id="9b808-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9b808-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="9b808-109">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="9b808-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="9b808-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9b808-110">PARAMETERS</span></span>

### <span data-ttu-id="9b808-111">-Access</span><span class="sxs-lookup"><span data-stu-id="9b808-111">-Access</span></span>
<span data-ttu-id="9b808-112">Yol filtresi kuralı erişimi.</span><span class="sxs-lookup"><span data-stu-id="9b808-112">Access for route filter rule.</span></span>
<span data-ttu-id="9b808-113">Geçerli değerler Izin ver veya Reddet.</span><span class="sxs-lookup"><span data-stu-id="9b808-113">Valid values are Allow or Deny.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b808-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="9b808-114">-CommunityList</span></span>
<span data-ttu-id="9b808-115">Yol süzgecinin filtrelendirilecektir topluluk değeri listesi</span><span class="sxs-lookup"><span data-stu-id="9b808-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="9b808-116">-Force</span><span class="sxs-lookup"><span data-stu-id="9b808-116">-Force</span></span>
<span data-ttu-id="9b808-117">Kaynağın üzerine yazılsın mı?</span><span class="sxs-lookup"><span data-stu-id="9b808-117">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="9b808-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="9b808-118">-Name</span></span>
<span data-ttu-id="9b808-119">Yol filtresi kuralı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="9b808-119">Specifies a name for the route filter rule.</span></span>

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

### <span data-ttu-id="9b808-120">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="9b808-120">-RouteFilterRuleType</span></span>
<span data-ttu-id="9b808-121">Yol filtre kuralı türü.</span><span class="sxs-lookup"><span data-stu-id="9b808-121">Route Filter Rule Type.</span></span>
<span data-ttu-id="9b808-122">Geçerli değerler: topluluk</span><span class="sxs-lookup"><span data-stu-id="9b808-122">Valid values are: Community</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b808-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="9b808-123">-Confirm</span></span>
<span data-ttu-id="9b808-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9b808-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b808-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b808-125">-WhatIf</span></span>
<span data-ttu-id="9b808-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9b808-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9b808-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9b808-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b808-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b808-128">-DefaultProfile</span></span>
<span data-ttu-id="9b808-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9b808-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b808-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b808-130">CommonParameters</span></span>
<span data-ttu-id="9b808-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9b808-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b808-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b808-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b808-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9b808-133">INPUTS</span></span>

## <span data-ttu-id="9b808-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9b808-134">OUTPUTS</span></span>

### <span data-ttu-id="9b808-135">Microsoft. Azure. Commands. Network. model. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="9b808-135">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="9b808-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9b808-136">NOTES</span></span>
<span data-ttu-id="9b808-137">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="9b808-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="9b808-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9b808-138">RELATED LINKS</span></span>

[<span data-ttu-id="9b808-139">Add-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9b808-139">Add-AzureRmRouteFilterRuleConfig</span></span>](./Add-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="9b808-140">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9b808-140">Get-AzureRmRouteFilterRuleConfig</span></span>](./Get-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="9b808-141">Remove-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9b808-141">Remove-AzureRmRouteFilterRuleConfig</span></span>](./Remove-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="9b808-142">Set-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9b808-142">Set-AzureRmRouteFilterRuleConfig</span></span>](./Set-AzureRmRouteFilterRuleConfig.md)

