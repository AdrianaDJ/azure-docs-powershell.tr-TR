---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
ms.openlocfilehash: f6a989a206c6fabf8e64cc82fb07741983f144c5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108903"
---
# <span data-ttu-id="8fddd-101">New-AzFirewallPolicyNatRule</span><span class="sxs-lookup"><span data-stu-id="8fddd-101">New-AzFirewallPolicyNatRule</span></span>

## <span data-ttu-id="8fddd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fddd-102">SYNOPSIS</span></span>
<span data-ttu-id="8fddd-103">Yeni Azure Güvenlik Duvarı Ilkesi NAT kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="8fddd-103">Create a new Azure Firewall Policy NAT Rule</span></span>

## <span data-ttu-id="8fddd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8fddd-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> -DestinationPort <String[]>
 -Protocols <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fddd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8fddd-105">DESCRIPTION</span></span>
<span data-ttu-id="8fddd-106">**New-AzFirewallPolicyNatRule** cmdlet 'i, bir Azure Güvenlik Duvarı ILKESI için NAT kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8fddd-106">The **New-AzFirewallPolicyNatRule** cmdlet creates a NAT rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="8fddd-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8fddd-107">EXAMPLES</span></span>

### <span data-ttu-id="8fddd-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8fddd-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRule -Name NatRule1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress 10.20.30.40 -DestinationPort 1000 -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="8fddd-109">Bu örnek, kaynak adresi, protokol, hedef adres, hedef bağlantı noktası, çevrilen adres ve çevrilen bağlantı noktası içeren bir NAT kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8fddd-109">This example creates a NAT rule with the source address, protocol, destination address, destination port, translated address, and translated port.</span></span>

## <span data-ttu-id="8fddd-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8fddd-110">PARAMETERS</span></span>

### <span data-ttu-id="8fddd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fddd-111">-DefaultProfile</span></span>
<span data-ttu-id="8fddd-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8fddd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fddd-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="8fddd-113">-Name</span></span>
<span data-ttu-id="8fddd-114">NAT kural koleksiyonunun adı</span><span class="sxs-lookup"><span data-stu-id="8fddd-114">The name of the NAT Rule Collection</span></span>

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

### <span data-ttu-id="8fddd-115">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="8fddd-115">-Description</span></span>
<span data-ttu-id="8fddd-116">Kuralın açıklaması</span><span class="sxs-lookup"><span data-stu-id="8fddd-116">The description of the rule</span></span>

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

### <span data-ttu-id="8fddd-117">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="8fddd-117">-DestinationAddress</span></span>
<span data-ttu-id="8fddd-118">Kuralın hedef adresleri.</span><span class="sxs-lookup"><span data-stu-id="8fddd-118">The destination addresses of the rule.</span></span> <span data-ttu-id="8fddd-119">Bu, güvenlik duvarının ortak IP 'si olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="8fddd-119">This has to be Public IP of the Firewall.</span></span>

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

### <span data-ttu-id="8fddd-120">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="8fddd-120">-DestinationPort</span></span>
<span data-ttu-id="8fddd-121">Kuralın hedef bağlantı noktaları</span><span class="sxs-lookup"><span data-stu-id="8fddd-121">The destination ports of the rule</span></span>

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

### <span data-ttu-id="8fddd-122">-Protokoller</span><span class="sxs-lookup"><span data-stu-id="8fddd-122">-Protocols</span></span>
<span data-ttu-id="8fddd-123">Kuralın protokolleri</span><span class="sxs-lookup"><span data-stu-id="8fddd-123">The protocols of the rule</span></span>

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

### <span data-ttu-id="8fddd-124">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="8fddd-124">-SourceAddress</span></span>
<span data-ttu-id="8fddd-125">Kuralın kaynak adresleri</span><span class="sxs-lookup"><span data-stu-id="8fddd-125">The source addresses of the rule</span></span>

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

### <span data-ttu-id="8fddd-126">-Sourceıpgroup</span><span class="sxs-lookup"><span data-stu-id="8fddd-126">-SourceIpGroup</span></span>
<span data-ttu-id="8fddd-127">Kuralın kaynak IP grupları</span><span class="sxs-lookup"><span data-stu-id="8fddd-127">The source ipgroups of the rule</span></span>

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

### <span data-ttu-id="8fddd-128">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="8fddd-128">-TranslatedAddress</span></span>
<span data-ttu-id="8fddd-129">Bu NAT kuralı için çevrilen adres</span><span class="sxs-lookup"><span data-stu-id="8fddd-129">The translated address for this NAT rule</span></span>

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

### <span data-ttu-id="8fddd-130">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="8fddd-130">-TranslatedPort</span></span>
<span data-ttu-id="8fddd-131">Bu NAT kuralı için çevrilen bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="8fddd-131">The translated port for this NAT rule</span></span>

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

### <span data-ttu-id="8fddd-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="8fddd-132">-Confirm</span></span>
<span data-ttu-id="8fddd-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8fddd-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fddd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fddd-134">-WhatIf</span></span>
<span data-ttu-id="8fddd-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8fddd-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fddd-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8fddd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fddd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fddd-137">CommonParameters</span></span>
<span data-ttu-id="8fddd-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8fddd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fddd-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8fddd-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fddd-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8fddd-140">INPUTS</span></span>

### <span data-ttu-id="8fddd-141">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="8fddd-141">None</span></span>

## <span data-ttu-id="8fddd-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8fddd-142">OUTPUTS</span></span>

### <span data-ttu-id="8fddd-143">Microsoft. Azure. Commands. Network. model. PSAzureFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="8fddd-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="8fddd-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8fddd-144">NOTES</span></span>

## <span data-ttu-id="8fddd-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8fddd-145">RELATED LINKS</span></span>
