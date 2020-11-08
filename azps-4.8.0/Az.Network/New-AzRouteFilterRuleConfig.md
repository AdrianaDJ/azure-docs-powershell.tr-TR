---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
ms.openlocfilehash: d66a684b6cd9b26aa9d616a74a4d2eaabaa891ff
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267034"
---
# <span data-ttu-id="0b133-101">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0b133-101">New-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="0b133-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b133-102">SYNOPSIS</span></span>
<span data-ttu-id="0b133-103">Yol filtresi için bir yol filtre kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0b133-103">Creates a route filter rule for a route filter.</span></span>

## <span data-ttu-id="0b133-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0b133-104">SYNTAX</span></span>

```
New-AzRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b133-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0b133-105">DESCRIPTION</span></span>
<span data-ttu-id="0b133-106">New-AzRouteFilterRuleConfig cmdlet 'i Azure yol filtresi için bir yol filtresi kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0b133-106">The New-AzRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="0b133-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0b133-107">EXAMPLES</span></span>

### <span data-ttu-id="0b133-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0b133-108">Example 1</span></span>
```powershell
PS C:\> $rule1 = New-AzRouteFilterRuleConfig -Name "Rule01" -Access "Allow" -RouteFilterRuleType "Community" -CommunityList "12076:5040"
```

<span data-ttu-id="0b133-109">Komut yeni bir yol filtresi kuralı oluşturur ve bunu $rule 1 değişkenine depolar.</span><span class="sxs-lookup"><span data-stu-id="0b133-109">The command creates a new route filter rule and stores it in variable $rule1.</span></span>

## <span data-ttu-id="0b133-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0b133-110">PARAMETERS</span></span>

### <span data-ttu-id="0b133-111">-Access</span><span class="sxs-lookup"><span data-stu-id="0b133-111">-Access</span></span>
<span data-ttu-id="0b133-112">Yol filtresi kuralı erişimi.</span><span class="sxs-lookup"><span data-stu-id="0b133-112">Access for route filter rule.</span></span>
<span data-ttu-id="0b133-113">Geçerli değerler Izin ver veya Reddet.</span><span class="sxs-lookup"><span data-stu-id="0b133-113">Valid values are Allow or Deny.</span></span>

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

### <span data-ttu-id="0b133-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="0b133-114">-CommunityList</span></span>
<span data-ttu-id="0b133-115">Yol süzgecinin filtrelendirilecektir topluluk değeri listesi</span><span class="sxs-lookup"><span data-stu-id="0b133-115">The list of community value that route filter will filter on</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b133-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b133-116">-DefaultProfile</span></span>
<span data-ttu-id="0b133-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0b133-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b133-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0b133-118">-Force</span></span>
<span data-ttu-id="0b133-119">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="0b133-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="0b133-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="0b133-120">-Name</span></span>
<span data-ttu-id="0b133-121">Yol filtresi kuralı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b133-121">Specifies a name for the route filter rule.</span></span>

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

### <span data-ttu-id="0b133-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="0b133-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="0b133-123">Yol filtre kuralı türü.</span><span class="sxs-lookup"><span data-stu-id="0b133-123">Route Filter Rule Type.</span></span>
<span data-ttu-id="0b133-124">Geçerli değerler: topluluk</span><span class="sxs-lookup"><span data-stu-id="0b133-124">Valid values are: Community</span></span>

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

### <span data-ttu-id="0b133-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="0b133-125">-Confirm</span></span>
<span data-ttu-id="0b133-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0b133-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b133-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b133-127">-WhatIf</span></span>
<span data-ttu-id="0b133-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0b133-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0b133-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0b133-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b133-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b133-130">CommonParameters</span></span>
<span data-ttu-id="0b133-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0b133-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b133-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b133-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b133-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0b133-133">INPUTS</span></span>

### <span data-ttu-id="0b133-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0b133-134">None</span></span>

## <span data-ttu-id="0b133-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0b133-135">OUTPUTS</span></span>

### <span data-ttu-id="0b133-136">Microsoft. Azure. Commands. Network. model. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="0b133-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="0b133-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0b133-137">NOTES</span></span>
<span data-ttu-id="0b133-138">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="0b133-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="0b133-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0b133-139">RELATED LINKS</span></span>

[<span data-ttu-id="0b133-140">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0b133-140">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="0b133-141">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0b133-141">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="0b133-142">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0b133-142">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="0b133-143">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0b133-143">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="0b133-144">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0b133-144">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="0b133-145">Yeni-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0b133-145">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="0b133-146">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0b133-146">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="0b133-147">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0b133-147">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
