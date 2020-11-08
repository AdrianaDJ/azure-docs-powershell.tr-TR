---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
ms.openlocfilehash: 1cd87ecefdb2216e7fb77ffcaaf487fa13a5a565
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266001"
---
# <span data-ttu-id="e87fc-101">New-AzFirewallPolicyNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e87fc-101">New-AzFirewallPolicyNetworkRule</span></span>

## <span data-ttu-id="e87fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e87fc-102">SYNOPSIS</span></span>
<span data-ttu-id="e87fc-103">Yeni Azure Güvenlik Duvarı Ilkesi ağ kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="e87fc-103">Create a new Azure Firewall Policy Network Rule</span></span>

## <span data-ttu-id="e87fc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e87fc-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> [-DestinationIpGroup <String[]>]
 -DestinationPort <String[]> [-DestinationFqdn <String[]>] -Protocols <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e87fc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e87fc-105">DESCRIPTION</span></span>
<span data-ttu-id="e87fc-106">**New-AzFirewallPolicyNetworkRule** cmdlet 'i, bir Azure Güvenlik Duvarı Ilkesi için ağ kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e87fc-106">The **New-AzFirewallPolicyNetworkRule** cmdlet creates a Network rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="e87fc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e87fc-107">EXAMPLES</span></span>

### <span data-ttu-id="e87fc-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e87fc-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNetworkRule -Name NRC1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress * -DestinationPort *
```

<span data-ttu-id="e87fc-109">Bu örnekte kaynak adresi, protokol, hedef adresi ve hedef bağlantı noktası içeren bir ağ kuralı oluşturulur</span><span class="sxs-lookup"><span data-stu-id="e87fc-109">This example creates an network rule with the source address, protocol , destination address and destination port</span></span>

## <span data-ttu-id="e87fc-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e87fc-110">PARAMETERS</span></span>

### <span data-ttu-id="e87fc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e87fc-111">-DefaultProfile</span></span>
<span data-ttu-id="e87fc-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e87fc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e87fc-113">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="e87fc-113">-Description</span></span>
<span data-ttu-id="e87fc-114">Kuralın açıklaması</span><span class="sxs-lookup"><span data-stu-id="e87fc-114">The description of the rule</span></span>

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

### <span data-ttu-id="e87fc-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="e87fc-115">-DestinationAddress</span></span>
<span data-ttu-id="e87fc-116">Kuralın hedef adresleri</span><span class="sxs-lookup"><span data-stu-id="e87fc-116">The destination addresses of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e87fc-117">-DestinationFqdn</span><span class="sxs-lookup"><span data-stu-id="e87fc-117">-DestinationFqdn</span></span>
<span data-ttu-id="e87fc-118">Kuralın hedef FQDN 'SI</span><span class="sxs-lookup"><span data-stu-id="e87fc-118">The destination FQDN of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e87fc-119">-Destinationıpgroup</span><span class="sxs-lookup"><span data-stu-id="e87fc-119">-DestinationIpGroup</span></span>
<span data-ttu-id="e87fc-120">Kuralın hedef IP grupları</span><span class="sxs-lookup"><span data-stu-id="e87fc-120">The destination ipgroups of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e87fc-121">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="e87fc-121">-DestinationPort</span></span>
<span data-ttu-id="e87fc-122">Kuralın hedef bağlantı noktaları</span><span class="sxs-lookup"><span data-stu-id="e87fc-122">The destination ports of the rule</span></span>

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

### <span data-ttu-id="e87fc-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="e87fc-123">-Name</span></span>
<span data-ttu-id="e87fc-124">Ağ kuralının adı</span><span class="sxs-lookup"><span data-stu-id="e87fc-124">The name of the Network Rule</span></span>

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

### <span data-ttu-id="e87fc-125">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="e87fc-125">-Protocol</span></span>
<span data-ttu-id="e87fc-126">Kuralın protokolleri</span><span class="sxs-lookup"><span data-stu-id="e87fc-126">The protocols of the rule</span></span>

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

### <span data-ttu-id="e87fc-127">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="e87fc-127">-SourceAddress</span></span>
<span data-ttu-id="e87fc-128">Kuralın kaynak adresleri</span><span class="sxs-lookup"><span data-stu-id="e87fc-128">The source addresses of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e87fc-129">-Sourceıpgroup</span><span class="sxs-lookup"><span data-stu-id="e87fc-129">-SourceIpGroup</span></span>
<span data-ttu-id="e87fc-130">Kuralın kaynak IP grupları</span><span class="sxs-lookup"><span data-stu-id="e87fc-130">The source ipgroups of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e87fc-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="e87fc-131">-Confirm</span></span>
<span data-ttu-id="e87fc-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e87fc-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e87fc-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e87fc-133">-WhatIf</span></span>
<span data-ttu-id="e87fc-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e87fc-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e87fc-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e87fc-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e87fc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e87fc-136">CommonParameters</span></span>
<span data-ttu-id="e87fc-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e87fc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e87fc-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e87fc-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e87fc-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e87fc-139">INPUTS</span></span>

### <span data-ttu-id="e87fc-140">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e87fc-140">None</span></span>

## <span data-ttu-id="e87fc-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e87fc-141">OUTPUTS</span></span>

### <span data-ttu-id="e87fc-142">Microsoft. Azure. Commands. Network. model. PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e87fc-142">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="e87fc-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e87fc-143">NOTES</span></span>

## <span data-ttu-id="e87fc-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e87fc-144">RELATED LINKS</span></span>
