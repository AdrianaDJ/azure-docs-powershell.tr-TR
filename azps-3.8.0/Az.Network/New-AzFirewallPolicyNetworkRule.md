---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
ms.openlocfilehash: b4cbc404139cd56e75f03c5cb19cb9b761576e39
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097295"
---
# <span data-ttu-id="3a20d-101">New-AzFirewallPolicyNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3a20d-101">New-AzFirewallPolicyNetworkRule</span></span>

## <span data-ttu-id="3a20d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a20d-102">SYNOPSIS</span></span>
<span data-ttu-id="3a20d-103">Yeni Azure Güvenlik Duvarı Ilkesi ağ kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="3a20d-103">Create a new Azure Firewall Policy Network Rule</span></span>

## <span data-ttu-id="3a20d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3a20d-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocols <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a20d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3a20d-105">DESCRIPTION</span></span>
<span data-ttu-id="3a20d-106">**New-AzFirewallPolicyNetworkRule** cmdlet 'i, bir Azure Güvenlik Duvarı Ilkesi için ağ kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3a20d-106">The **New-AzFirewallPolicyNetworkRule** cmdlet creates a Network rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="3a20d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3a20d-107">EXAMPLES</span></span>

### <span data-ttu-id="3a20d-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3a20d-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNetworkRule -Name NRC1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress * -DestinationPort *
```

<span data-ttu-id="3a20d-109">Bu örnekte kaynak adresi, protokol, hedef adresi ve hedef bağlantı noktası içeren bir ağ kuralı oluşturulur</span><span class="sxs-lookup"><span data-stu-id="3a20d-109">This example creates an network rule with the source address, protocol , destination address and destination port</span></span>

## <span data-ttu-id="3a20d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3a20d-110">PARAMETERS</span></span>

### <span data-ttu-id="3a20d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a20d-111">-DefaultProfile</span></span>
<span data-ttu-id="3a20d-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3a20d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a20d-113">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="3a20d-113">-Description</span></span>
<span data-ttu-id="3a20d-114">Kuralın açıklaması</span><span class="sxs-lookup"><span data-stu-id="3a20d-114">The description of the rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a20d-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="3a20d-115">-DestinationAddress</span></span>
<span data-ttu-id="3a20d-116">Kuralın hedef adresleri</span><span class="sxs-lookup"><span data-stu-id="3a20d-116">The destination addresses of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a20d-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="3a20d-117">-DestinationPort</span></span>
<span data-ttu-id="3a20d-118">Kuralın hedef bağlantı noktaları</span><span class="sxs-lookup"><span data-stu-id="3a20d-118">The destination ports of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a20d-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="3a20d-119">-Name</span></span>
<span data-ttu-id="3a20d-120">Ağ kuralının adı</span><span class="sxs-lookup"><span data-stu-id="3a20d-120">The name of the Network Rule</span></span>

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

### <span data-ttu-id="3a20d-121">-Protokoller</span><span class="sxs-lookup"><span data-stu-id="3a20d-121">-Protocols</span></span>
<span data-ttu-id="3a20d-122">Kuralın protokolleri</span><span class="sxs-lookup"><span data-stu-id="3a20d-122">The protocols of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP, ICMP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a20d-123">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="3a20d-123">-SourceAddress</span></span>
<span data-ttu-id="3a20d-124">Kuralın kaynak adresleri</span><span class="sxs-lookup"><span data-stu-id="3a20d-124">The source addresses of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a20d-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="3a20d-125">-Confirm</span></span>
<span data-ttu-id="3a20d-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3a20d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a20d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a20d-127">-WhatIf</span></span>
<span data-ttu-id="3a20d-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3a20d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a20d-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3a20d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a20d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a20d-130">CommonParameters</span></span>
<span data-ttu-id="3a20d-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3a20d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a20d-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3a20d-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a20d-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3a20d-133">INPUTS</span></span>

### <span data-ttu-id="3a20d-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3a20d-134">None</span></span>

## <span data-ttu-id="3a20d-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3a20d-135">OUTPUTS</span></span>

### <span data-ttu-id="3a20d-136">Microsoft. Azure. Commands. Network. model. PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3a20d-136">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="3a20d-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3a20d-137">NOTES</span></span>

## <span data-ttu-id="3a20d-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3a20d-138">RELATED LINKS</span></span>
