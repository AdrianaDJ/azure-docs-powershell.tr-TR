---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
ms.openlocfilehash: c3cf6ce07ab746806181af917f656d27c6ffbbaa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324628"
---
# <span data-ttu-id="ecdac-101">New-AzFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ecdac-101">New-AzFirewallNetworkRule</span></span>

## <span data-ttu-id="ecdac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecdac-102">SYNOPSIS</span></span>
<span data-ttu-id="ecdac-103">Güvenlik Duvarı ağ kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ecdac-103">Creates a Firewall Network Rule.</span></span>

## <span data-ttu-id="ecdac-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ecdac-104">SYNTAX</span></span>

```
New-AzFirewallNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] [-DestinationAddress <String[]>] [-DestinationIpGroup <String[]>]
 [-DestinationFqdn <String[]>] -DestinationPort <String[]> -Protocol <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecdac-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ecdac-105">DESCRIPTION</span></span>
<span data-ttu-id="ecdac-106">**New-AzFirewallNetworkRule** cmdlet 'ı, Azure Güvenlik Duvarı için bir ağ kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ecdac-106">The **New-AzFirewallNetworkRule** cmdlet creates an network rule for Azure Firewall.</span></span>

## <span data-ttu-id="ecdac-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ecdac-107">EXAMPLES</span></span>

### <span data-ttu-id="ecdac-108">Örnek 1: tüm TCP trafiği için kural oluşturma</span><span class="sxs-lookup"><span data-stu-id="ecdac-108">Example 1: Create a rule for all TCP traffic</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "all-tcp-traffic" -Description "Rule for all TCP traffic" -Protocol TCP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
```

<span data-ttu-id="ecdac-109">Bu örnekte tüm TCP trafiği için bir kural oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="ecdac-109">This example creates a rule for all TCP traffic.</span></span> <span data-ttu-id="ecdac-110">Kullanıcı, ilişkili olduğu kural koleksiyonuna dayalı bir kural için trafiğin izin verilip verilmeyeceğini veya reddedildiğini kabul eder.</span><span class="sxs-lookup"><span data-stu-id="ecdac-110">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="ecdac-111">Örnek 2:10.0.0.0 ile 60.1.5.0 arasında tüm TCP trafiği için bir kural oluşturun: 4040</span><span class="sxs-lookup"><span data-stu-id="ecdac-111">Example 2: Create a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
```

<span data-ttu-id="ecdac-112">Bu örnekte, 10.0.0.0 ile 60.1.5.0:4040 arasındaki tüm TCP trafiği için bir kural oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="ecdac-112">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="ecdac-113">Kullanıcı, ilişkili olduğu kural koleksiyonuna dayalı bir kural için trafiğin izin verilip verilmeyeceğini veya reddedildiğini kabul eder.</span><span class="sxs-lookup"><span data-stu-id="ecdac-113">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="ecdac-114">Örnek 3: herhangi bir kaynaktan 10.0.0.0/16 adresine giden tüm TCP ve ıCMP trafiği için bir kural oluşturma</span><span class="sxs-lookup"><span data-stu-id="ecdac-114">Example 3: Create a rule for all TCP and ICMP traffic from any source to 10.0.0.0/16</span></span>
```powershell
$rule = New-AzFirewallNetworkRule -Name "tcp-and-icmp-rule" -Description "Rule for all TCP and ICMP traffic from any source to 10.0.0.0/16" -Protocol TCP,ICMP -SourceAddress * -DestinationAddress "10.0.0.0/16" -DestinationPort *
```

<span data-ttu-id="ecdac-115">Bu örnekte, herhangi bir kaynaktan 10.0.0.0/16 adresine giden tüm TCP trafiği için bir kural oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="ecdac-115">This example creates a rule for all TCP traffic from any source to 10.0.0.0/16.</span></span> <span data-ttu-id="ecdac-116">Kullanıcı, ilişkili olduğu kural koleksiyonuna dayalı bir kural için trafiğin izin verilip verilmeyeceğini veya reddedildiğini kabul eder.</span><span class="sxs-lookup"><span data-stu-id="ecdac-116">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

## <span data-ttu-id="ecdac-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ecdac-117">PARAMETERS</span></span>

### <span data-ttu-id="ecdac-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecdac-118">-DefaultProfile</span></span>
<span data-ttu-id="ecdac-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ecdac-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecdac-120">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="ecdac-120">-Description</span></span>
<span data-ttu-id="ecdac-121">Bu kural için isteğe bağlı bir açıklama belirtin.</span><span class="sxs-lookup"><span data-stu-id="ecdac-121">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="ecdac-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="ecdac-122">-DestinationAddress</span></span>
<span data-ttu-id="ecdac-123">Kuralın hedef adresleri</span><span class="sxs-lookup"><span data-stu-id="ecdac-123">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="ecdac-124">-DestinationFqdn</span><span class="sxs-lookup"><span data-stu-id="ecdac-124">-DestinationFqdn</span></span>
<span data-ttu-id="ecdac-125">Kuralın hedef FQDN 'SI</span><span class="sxs-lookup"><span data-stu-id="ecdac-125">The destination FQDN of the rule</span></span>

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

### <span data-ttu-id="ecdac-126">-Destinationıpgroup</span><span class="sxs-lookup"><span data-stu-id="ecdac-126">-DestinationIpGroup</span></span>
<span data-ttu-id="ecdac-127">Kuralın hedef ipgrubu</span><span class="sxs-lookup"><span data-stu-id="ecdac-127">The destination ipgroup of the rule</span></span>

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

### <span data-ttu-id="ecdac-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="ecdac-128">-DestinationPort</span></span>
<span data-ttu-id="ecdac-129">Kuralın hedef bağlantı noktaları</span><span class="sxs-lookup"><span data-stu-id="ecdac-129">The destination ports of the rule</span></span>

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

### <span data-ttu-id="ecdac-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="ecdac-130">-Name</span></span>
<span data-ttu-id="ecdac-131">Bu ağ kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ecdac-131">Specifies the name of this network rule.</span></span> <span data-ttu-id="ecdac-132">Ad, bir kural koleksiyonunun içinde benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ecdac-132">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="ecdac-133">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="ecdac-133">-Protocol</span></span>
<span data-ttu-id="ecdac-134">Bu kurala göre filtre uygulanacak trafik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ecdac-134">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="ecdac-135">Olası değerler TCP, UDP, ıCMP ve Any değerleridir.</span><span class="sxs-lookup"><span data-stu-id="ecdac-135">Possible values are TCP, UDP, ICMP and Any.</span></span>

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

### <span data-ttu-id="ecdac-136">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="ecdac-136">-SourceAddress</span></span>
<span data-ttu-id="ecdac-137">Kuralın kaynak adresleri</span><span class="sxs-lookup"><span data-stu-id="ecdac-137">The source addresses of the rule</span></span>

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

### <span data-ttu-id="ecdac-138">-Sourceıpgroup</span><span class="sxs-lookup"><span data-stu-id="ecdac-138">-SourceIpGroup</span></span>
<span data-ttu-id="ecdac-139">Kuralın kaynak ıpgroup 'u</span><span class="sxs-lookup"><span data-stu-id="ecdac-139">The source ipgroup of the rule</span></span>

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

### <span data-ttu-id="ecdac-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="ecdac-140">-Confirm</span></span>
<span data-ttu-id="ecdac-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ecdac-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecdac-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecdac-142">-WhatIf</span></span>
<span data-ttu-id="ecdac-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ecdac-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecdac-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ecdac-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecdac-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecdac-145">CommonParameters</span></span>
<span data-ttu-id="ecdac-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ecdac-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecdac-147">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecdac-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecdac-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ecdac-148">INPUTS</span></span>

### <span data-ttu-id="ecdac-149">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ecdac-149">None</span></span>

## <span data-ttu-id="ecdac-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ecdac-150">OUTPUTS</span></span>

### <span data-ttu-id="ecdac-151">Microsoft. Azure. Commands. Network. model. PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ecdac-151">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="ecdac-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ecdac-152">NOTES</span></span>

## <span data-ttu-id="ecdac-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ecdac-153">RELATED LINKS</span></span>

[<span data-ttu-id="ecdac-154">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="ecdac-154">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)

[<span data-ttu-id="ecdac-155">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="ecdac-155">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="ecdac-156">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="ecdac-156">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
