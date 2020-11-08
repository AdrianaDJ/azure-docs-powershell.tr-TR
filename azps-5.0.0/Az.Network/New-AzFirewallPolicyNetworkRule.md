---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
ms.openlocfilehash: 1cd87ecefdb2216e7fb77ffcaaf487fa13a5a565
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278319"
---
# <span data-ttu-id="5b40c-101">New-AzFirewallPolicyNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5b40c-101">New-AzFirewallPolicyNetworkRule</span></span>

## <span data-ttu-id="5b40c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b40c-102">SYNOPSIS</span></span>
<span data-ttu-id="5b40c-103">Yeni Azure Güvenlik Duvarı Ilkesi ağ kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="5b40c-103">Create a new Azure Firewall Policy Network Rule</span></span>

## <span data-ttu-id="5b40c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5b40c-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> [-DestinationIpGroup <String[]>]
 -DestinationPort <String[]> [-DestinationFqdn <String[]>] -Protocols <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b40c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5b40c-105">DESCRIPTION</span></span>
<span data-ttu-id="5b40c-106">**New-AzFirewallPolicyNetworkRule** cmdlet 'i, bir Azure Güvenlik Duvarı Ilkesi için ağ kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5b40c-106">The **New-AzFirewallPolicyNetworkRule** cmdlet creates a Network rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="5b40c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5b40c-107">EXAMPLES</span></span>

### <span data-ttu-id="5b40c-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5b40c-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNetworkRule -Name NRC1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress * -DestinationPort *
```

<span data-ttu-id="5b40c-109">Bu örnekte kaynak adresi, protokol, hedef adresi ve hedef bağlantı noktası içeren bir ağ kuralı oluşturulur</span><span class="sxs-lookup"><span data-stu-id="5b40c-109">This example creates an network rule with the source address, protocol , destination address and destination port</span></span>

## <span data-ttu-id="5b40c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5b40c-110">PARAMETERS</span></span>

### <span data-ttu-id="5b40c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b40c-111">-DefaultProfile</span></span>
<span data-ttu-id="5b40c-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5b40c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b40c-113">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="5b40c-113">-Description</span></span>
<span data-ttu-id="5b40c-114">Kuralın açıklaması</span><span class="sxs-lookup"><span data-stu-id="5b40c-114">The description of the rule</span></span>

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

### <span data-ttu-id="5b40c-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="5b40c-115">-DestinationAddress</span></span>
<span data-ttu-id="5b40c-116">Kuralın hedef adresleri</span><span class="sxs-lookup"><span data-stu-id="5b40c-116">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="5b40c-117">-DestinationFqdn</span><span class="sxs-lookup"><span data-stu-id="5b40c-117">-DestinationFqdn</span></span>
<span data-ttu-id="5b40c-118">Kuralın hedef FQDN 'SI</span><span class="sxs-lookup"><span data-stu-id="5b40c-118">The destination FQDN of the rule</span></span>

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

### <span data-ttu-id="5b40c-119">-Destinationıpgroup</span><span class="sxs-lookup"><span data-stu-id="5b40c-119">-DestinationIpGroup</span></span>
<span data-ttu-id="5b40c-120">Kuralın hedef IP grupları</span><span class="sxs-lookup"><span data-stu-id="5b40c-120">The destination ipgroups of the rule</span></span>

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

### <span data-ttu-id="5b40c-121">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="5b40c-121">-DestinationPort</span></span>
<span data-ttu-id="5b40c-122">Kuralın hedef bağlantı noktaları</span><span class="sxs-lookup"><span data-stu-id="5b40c-122">The destination ports of the rule</span></span>

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

### <span data-ttu-id="5b40c-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="5b40c-123">-Name</span></span>
<span data-ttu-id="5b40c-124">Ağ kuralının adı</span><span class="sxs-lookup"><span data-stu-id="5b40c-124">The name of the Network Rule</span></span>

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

### <span data-ttu-id="5b40c-125">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="5b40c-125">-Protocol</span></span>
<span data-ttu-id="5b40c-126">Kuralın protokolleri</span><span class="sxs-lookup"><span data-stu-id="5b40c-126">The protocols of the rule</span></span>

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

### <span data-ttu-id="5b40c-127">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="5b40c-127">-SourceAddress</span></span>
<span data-ttu-id="5b40c-128">Kuralın kaynak adresleri</span><span class="sxs-lookup"><span data-stu-id="5b40c-128">The source addresses of the rule</span></span>

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

### <span data-ttu-id="5b40c-129">-Sourceıpgroup</span><span class="sxs-lookup"><span data-stu-id="5b40c-129">-SourceIpGroup</span></span>
<span data-ttu-id="5b40c-130">Kuralın kaynak IP grupları</span><span class="sxs-lookup"><span data-stu-id="5b40c-130">The source ipgroups of the rule</span></span>

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

### <span data-ttu-id="5b40c-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="5b40c-131">-Confirm</span></span>
<span data-ttu-id="5b40c-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5b40c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b40c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b40c-133">-WhatIf</span></span>
<span data-ttu-id="5b40c-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5b40c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b40c-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5b40c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b40c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b40c-136">CommonParameters</span></span>
<span data-ttu-id="5b40c-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5b40c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b40c-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5b40c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b40c-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5b40c-139">INPUTS</span></span>

### <span data-ttu-id="5b40c-140">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5b40c-140">None</span></span>

## <span data-ttu-id="5b40c-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5b40c-141">OUTPUTS</span></span>

### <span data-ttu-id="5b40c-142">Microsoft. Azure. Commands. Network. model. PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5b40c-142">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="5b40c-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5b40c-143">NOTES</span></span>

## <span data-ttu-id="5b40c-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5b40c-144">RELATED LINKS</span></span>
