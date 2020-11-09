---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
ms.openlocfilehash: d66a684b6cd9b26aa9d616a74a4d2eaabaa891ff
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323734"
---
# <span data-ttu-id="59624-101">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="59624-101">New-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="59624-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59624-102">SYNOPSIS</span></span>
<span data-ttu-id="59624-103">Yol filtresi için bir yol filtre kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="59624-103">Creates a route filter rule for a route filter.</span></span>

## <span data-ttu-id="59624-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="59624-104">SYNTAX</span></span>

```
New-AzRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59624-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="59624-105">DESCRIPTION</span></span>
<span data-ttu-id="59624-106">New-AzRouteFilterRuleConfig cmdlet 'i Azure yol filtresi için bir yol filtresi kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="59624-106">The New-AzRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="59624-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="59624-107">EXAMPLES</span></span>

### <span data-ttu-id="59624-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="59624-108">Example 1</span></span>
```powershell
PS C:\> $rule1 = New-AzRouteFilterRuleConfig -Name "Rule01" -Access "Allow" -RouteFilterRuleType "Community" -CommunityList "12076:5040"
```

<span data-ttu-id="59624-109">Komut yeni bir yol filtresi kuralı oluşturur ve bunu $rule 1 değişkenine depolar.</span><span class="sxs-lookup"><span data-stu-id="59624-109">The command creates a new route filter rule and stores it in variable $rule1.</span></span>

## <span data-ttu-id="59624-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="59624-110">PARAMETERS</span></span>

### <span data-ttu-id="59624-111">-Access</span><span class="sxs-lookup"><span data-stu-id="59624-111">-Access</span></span>
<span data-ttu-id="59624-112">Yol filtresi kuralı erişimi.</span><span class="sxs-lookup"><span data-stu-id="59624-112">Access for route filter rule.</span></span>
<span data-ttu-id="59624-113">Geçerli değerler Izin ver veya Reddet.</span><span class="sxs-lookup"><span data-stu-id="59624-113">Valid values are Allow or Deny.</span></span>

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

### <span data-ttu-id="59624-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="59624-114">-CommunityList</span></span>
<span data-ttu-id="59624-115">Yol süzgecinin filtrelendirilecektir topluluk değeri listesi</span><span class="sxs-lookup"><span data-stu-id="59624-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="59624-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59624-116">-DefaultProfile</span></span>
<span data-ttu-id="59624-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="59624-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59624-118">-Force</span><span class="sxs-lookup"><span data-stu-id="59624-118">-Force</span></span>
<span data-ttu-id="59624-119">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="59624-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="59624-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="59624-120">-Name</span></span>
<span data-ttu-id="59624-121">Yol filtresi kuralı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="59624-121">Specifies a name for the route filter rule.</span></span>

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

### <span data-ttu-id="59624-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="59624-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="59624-123">Yol filtre kuralı türü.</span><span class="sxs-lookup"><span data-stu-id="59624-123">Route Filter Rule Type.</span></span>
<span data-ttu-id="59624-124">Geçerli değerler: topluluk</span><span class="sxs-lookup"><span data-stu-id="59624-124">Valid values are: Community</span></span>

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

### <span data-ttu-id="59624-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="59624-125">-Confirm</span></span>
<span data-ttu-id="59624-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="59624-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59624-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59624-127">-WhatIf</span></span>
<span data-ttu-id="59624-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="59624-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="59624-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="59624-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59624-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59624-130">CommonParameters</span></span>
<span data-ttu-id="59624-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="59624-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59624-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59624-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59624-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="59624-133">INPUTS</span></span>

### <span data-ttu-id="59624-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="59624-134">None</span></span>

## <span data-ttu-id="59624-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="59624-135">OUTPUTS</span></span>

### <span data-ttu-id="59624-136">Microsoft. Azure. Commands. Network. model. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="59624-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="59624-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="59624-137">NOTES</span></span>
<span data-ttu-id="59624-138">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="59624-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="59624-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="59624-139">RELATED LINKS</span></span>

[<span data-ttu-id="59624-140">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="59624-140">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="59624-141">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="59624-141">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="59624-142">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="59624-142">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="59624-143">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="59624-143">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="59624-144">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="59624-144">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="59624-145">Yeni-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="59624-145">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="59624-146">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="59624-146">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="59624-147">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="59624-147">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
