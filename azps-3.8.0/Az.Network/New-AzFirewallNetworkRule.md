---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
ms.openlocfilehash: 31c066ce97502c43c9e93bdaf532ee63e701a18f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937290"
---
# <span data-ttu-id="d2ec9-101">New-AzFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d2ec9-101">New-AzFirewallNetworkRule</span></span>

## <span data-ttu-id="d2ec9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2ec9-102">SYNOPSIS</span></span>
<span data-ttu-id="d2ec9-103">Güvenlik Duvarı ağ kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d2ec9-103">Creates a Firewall Network Rule.</span></span>

## <span data-ttu-id="d2ec9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d2ec9-104">SYNTAX</span></span>

```
New-AzFirewallNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] [-DestinationAddress <String[]>] [-DestinationIpGroup <String[]>]
 [-DestinationFqdn <String[]>] -DestinationPort <String[]> -Protocol <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2ec9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d2ec9-105">DESCRIPTION</span></span>
<span data-ttu-id="d2ec9-106">**New-AzFirewallNetworkRule** cmdlet 'ı, Azure Güvenlik Duvarı için bir ağ kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d2ec9-106">The **New-AzFirewallNetworkRule** cmdlet creates an network rule for Azure Firewall.</span></span>

## <span data-ttu-id="d2ec9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d2ec9-107">EXAMPLES</span></span>

### <span data-ttu-id="d2ec9-108">1: tüm TCP trafiği için bir kural oluşturma</span><span class="sxs-lookup"><span data-stu-id="d2ec9-108">1:  Create a rule for all TCP traffic</span></span>
```
$rule = New-AzFirewallNetworkRule -Name "all-tcp-traffic" -Description "Rule for all TCP traffic" -Protocol TCP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
```

<span data-ttu-id="d2ec9-109">Bu örnekte tüm TCP trafiği için bir kural oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="d2ec9-109">This example creates a rule for all TCP traffic.</span></span> <span data-ttu-id="d2ec9-110">Kullanıcı, ilişkili olduğu kural koleksiyonuna dayalı bir kural için trafiğin izin verilip verilmeyeceğini veya reddedildiğini kabul eder.</span><span class="sxs-lookup"><span data-stu-id="d2ec9-110">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="d2ec9-111">2:10.0.0.0 ile 60.1.5.0 arasında tüm TCP trafiği için bir kural oluşturun: 4040</span><span class="sxs-lookup"><span data-stu-id="d2ec9-111">2:  Create a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040</span></span>
```
$rule = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
```

<span data-ttu-id="d2ec9-112">Bu örnekte, 10.0.0.0 ile 60.1.5.0:4040 arasındaki tüm TCP trafiği için bir kural oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="d2ec9-112">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="d2ec9-113">Kullanıcı, ilişkili olduğu kural koleksiyonuna dayalı bir kural için trafiğin izin verilip verilmeyeceğini veya reddedildiğini kabul eder.</span><span class="sxs-lookup"><span data-stu-id="d2ec9-113">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="d2ec9-114">3: herhangi bir kaynaktan 10.0.0.0/16 adresine giden tüm TCP ve ıCMP trafiği için bir kural oluşturun</span><span class="sxs-lookup"><span data-stu-id="d2ec9-114">3: Create a rule for all TCP and ICMP traffic from any source to 10.0.0.0/16</span></span>
```
$rule = New-AzFirewallNetworkRule -Name "tcp-and-icmp-rule" -Description "Rule for all TCP and ICMP traffic from any source to 10.0.0.0/16" -Protocol TCP,ICMP -SourceAddress * -DestinationAddress "10.0.0.0/16" -DestinationPort *
```

<span data-ttu-id="d2ec9-115">Bu örnekte, 10.0.0.0 ile 60.1.5.0:4040 arasındaki tüm TCP trafiği için bir kural oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="d2ec9-115">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="d2ec9-116">Kullanıcı, ilişkili olduğu kural koleksiyonuna dayalı bir kural için trafiğin izin verilip verilmeyeceğini veya reddedildiğini kabul eder.</span><span class="sxs-lookup"><span data-stu-id="d2ec9-116">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

## <span data-ttu-id="d2ec9-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d2ec9-117">PARAMETERS</span></span>

### <span data-ttu-id="d2ec9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2ec9-118">-DefaultProfile</span></span>
<span data-ttu-id="d2ec9-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d2ec9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2ec9-120">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="d2ec9-120">-Description</span></span>
<span data-ttu-id="d2ec9-121">Bu kural için isteğe bağlı bir açıklama belirtin.</span><span class="sxs-lookup"><span data-stu-id="d2ec9-121">Specifies an optional description of this rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2ec9-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="d2ec9-122">-DestinationAddress</span></span>
<span data-ttu-id="d2ec9-123">Kuralın hedef adresleri</span><span class="sxs-lookup"><span data-stu-id="d2ec9-123">The destination addresses of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2ec9-124">-DestinationFqdn</span><span class="sxs-lookup"><span data-stu-id="d2ec9-124">-DestinationFqdn</span></span>
<span data-ttu-id="d2ec9-125">Kuralın hedef FQDN 'SI</span><span class="sxs-lookup"><span data-stu-id="d2ec9-125">The destination FQDN of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2ec9-126">-Destinationıpgroup</span><span class="sxs-lookup"><span data-stu-id="d2ec9-126">-DestinationIpGroup</span></span>
<span data-ttu-id="d2ec9-127">Kuralın hedef ipgrubu</span><span class="sxs-lookup"><span data-stu-id="d2ec9-127">The destination ipgroup of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2ec9-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="d2ec9-128">-DestinationPort</span></span>
<span data-ttu-id="d2ec9-129">Kuralın hedef bağlantı noktaları</span><span class="sxs-lookup"><span data-stu-id="d2ec9-129">The destination ports of the rule</span></span>

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

### <span data-ttu-id="d2ec9-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="d2ec9-130">-Name</span></span>
<span data-ttu-id="d2ec9-131">Bu ağ kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d2ec9-131">Specifies the name of this network rule.</span></span> <span data-ttu-id="d2ec9-132">Ad, bir kural koleksiyonunun içinde benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d2ec9-132">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="d2ec9-133">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="d2ec9-133">-Protocol</span></span>
<span data-ttu-id="d2ec9-134">Bu kurala göre filtre uygulanacak trafik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="d2ec9-134">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="d2ec9-135">Olası değerler TCP, UDP, ıCMP ve Any değerleridir.</span><span class="sxs-lookup"><span data-stu-id="d2ec9-135">Possible values are TCP, UDP, ICMP and Any.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP, ICMP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2ec9-136">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="d2ec9-136">-SourceAddress</span></span>
<span data-ttu-id="d2ec9-137">Kuralın kaynak adresleri</span><span class="sxs-lookup"><span data-stu-id="d2ec9-137">The source addresses of the rule</span></span>

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

### <span data-ttu-id="d2ec9-138">-Sourceıpgroup</span><span class="sxs-lookup"><span data-stu-id="d2ec9-138">-SourceIpGroup</span></span>
<span data-ttu-id="d2ec9-139">Kuralın kaynak ıpgroup 'u</span><span class="sxs-lookup"><span data-stu-id="d2ec9-139">The source ipgroup of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2ec9-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="d2ec9-140">-Confirm</span></span>
<span data-ttu-id="d2ec9-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d2ec9-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2ec9-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2ec9-142">-WhatIf</span></span>
<span data-ttu-id="d2ec9-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d2ec9-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2ec9-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d2ec9-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2ec9-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2ec9-145">CommonParameters</span></span>
<span data-ttu-id="d2ec9-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d2ec9-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2ec9-147">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2ec9-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2ec9-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d2ec9-148">INPUTS</span></span>

### <span data-ttu-id="d2ec9-149">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d2ec9-149">None</span></span>

## <span data-ttu-id="d2ec9-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d2ec9-150">OUTPUTS</span></span>

### <span data-ttu-id="d2ec9-151">Microsoft. Azure. Commands. Network. model. PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d2ec9-151">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="d2ec9-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d2ec9-152">NOTES</span></span>

## <span data-ttu-id="d2ec9-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d2ec9-153">RELATED LINKS</span></span>

[<span data-ttu-id="d2ec9-154">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="d2ec9-154">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)

[<span data-ttu-id="d2ec9-155">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d2ec9-155">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="d2ec9-156">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d2ec9-156">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
