---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRule.md
ms.openlocfilehash: 06cac261d368dfafa19b96b42945ed9cda613122
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760336"
---
# <span data-ttu-id="d9df7-101">New-AzFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d9df7-101">New-AzFirewallNetworkRule</span></span>

## <span data-ttu-id="d9df7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9df7-102">SYNOPSIS</span></span>
<span data-ttu-id="d9df7-103">Güvenlik Duvarı ağ kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d9df7-103">Creates a Firewall Network Rule.</span></span>

## <span data-ttu-id="d9df7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d9df7-104">SYNTAX</span></span>

```
New-AzFirewallNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9df7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d9df7-105">DESCRIPTION</span></span>
<span data-ttu-id="d9df7-106">**New-AzFirewallNetworkRule** cmdlet 'ı, Azure Güvenlik Duvarı için bir ağ kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d9df7-106">The **New-AzFirewallNetworkRule** cmdlet creates an network rule for Azure Firewall.</span></span>

## <span data-ttu-id="d9df7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d9df7-107">EXAMPLES</span></span>

### <span data-ttu-id="d9df7-108">1: tüm TCP trafiği için bir kural oluşturma</span><span class="sxs-lookup"><span data-stu-id="d9df7-108">1:  Create a rule for all TCP traffic</span></span>
```
$rule = New-AzFirewallNetworkRule -Name "all-tcp-traffic" -Description "Rule for all TCP traffic" -Protocol TCP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
```

<span data-ttu-id="d9df7-109">Bu örnekte tüm TCP trafiği için bir kural oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="d9df7-109">This example creates a rule for all TCP traffic.</span></span> <span data-ttu-id="d9df7-110">Kullanıcı, ilişkili olduğu kural koleksiyonuna dayalı bir kural için trafiğin izin verilip verilmeyeceğini veya reddedildiğini kabul eder.</span><span class="sxs-lookup"><span data-stu-id="d9df7-110">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="d9df7-111">2:10.0.0.0 ile 60.1.5.0 arasında tüm TCP trafiği için bir kural oluşturun: 4040</span><span class="sxs-lookup"><span data-stu-id="d9df7-111">2:  Create a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040</span></span>
```
$rule = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
```

<span data-ttu-id="d9df7-112">Bu örnekte, 10.0.0.0 ile 60.1.5.0:4040 arasındaki tüm TCP trafiği için bir kural oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="d9df7-112">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="d9df7-113">Kullanıcı, ilişkili olduğu kural koleksiyonuna dayalı bir kural için trafiğin izin verilip verilmeyeceğini veya reddedildiğini kabul eder.</span><span class="sxs-lookup"><span data-stu-id="d9df7-113">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="d9df7-114">3: herhangi bir kaynaktan 10.0.0.0/16 adresine giden tüm TCP ve ıCMP trafiği için bir kural oluşturun</span><span class="sxs-lookup"><span data-stu-id="d9df7-114">3: Create a rule for all TCP and ICMP traffic from any source to 10.0.0.0/16</span></span>
```
$rule = New-AzFirewallNetworkRule -Name "tcp-and-icmp-rule" -Description "Rule for all TCP and ICMP traffic from any source to 10.0.0.0/16" -Protocol TCP,ICMP -SourceAddress * -DestinationAddress "10.0.0.0/16" -DestinationPort *
```

<span data-ttu-id="d9df7-115">Bu örnekte, 10.0.0.0 ile 60.1.5.0:4040 arasındaki tüm TCP trafiği için bir kural oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="d9df7-115">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="d9df7-116">Kullanıcı, ilişkili olduğu kural koleksiyonuna dayalı bir kural için trafiğin izin verilip verilmeyeceğini veya reddedildiğini kabul eder.</span><span class="sxs-lookup"><span data-stu-id="d9df7-116">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

## <span data-ttu-id="d9df7-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d9df7-117">PARAMETERS</span></span>

### <span data-ttu-id="d9df7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9df7-118">-DefaultProfile</span></span>
<span data-ttu-id="d9df7-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d9df7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9df7-120">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="d9df7-120">-Description</span></span>
<span data-ttu-id="d9df7-121">Bu kural için isteğe bağlı bir açıklama belirtin.</span><span class="sxs-lookup"><span data-stu-id="d9df7-121">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="d9df7-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="d9df7-122">-DestinationAddress</span></span>
<span data-ttu-id="d9df7-123">Kuralın hedef adresleri</span><span class="sxs-lookup"><span data-stu-id="d9df7-123">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="d9df7-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="d9df7-124">-DestinationPort</span></span>
<span data-ttu-id="d9df7-125">Kuralın hedef bağlantı noktaları</span><span class="sxs-lookup"><span data-stu-id="d9df7-125">The destination ports of the rule</span></span>

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

### <span data-ttu-id="d9df7-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="d9df7-126">-Name</span></span>
<span data-ttu-id="d9df7-127">Bu ağ kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9df7-127">Specifies the name of this network rule.</span></span> <span data-ttu-id="d9df7-128">Ad, bir kural koleksiyonunun içinde benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d9df7-128">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="d9df7-129">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="d9df7-129">-Protocol</span></span>
<span data-ttu-id="d9df7-130">Bu kurala göre filtre uygulanacak trafik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9df7-130">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="d9df7-131">Olası değerler TCP, UDP, ıCMP ve Any değerleridir.</span><span class="sxs-lookup"><span data-stu-id="d9df7-131">Possible values are TCP, UDP, ICMP and Any.</span></span>

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

### <span data-ttu-id="d9df7-132">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="d9df7-132">-SourceAddress</span></span>
<span data-ttu-id="d9df7-133">Kuralın kaynak adresleri</span><span class="sxs-lookup"><span data-stu-id="d9df7-133">The source addresses of the rule</span></span>

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

### <span data-ttu-id="d9df7-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="d9df7-134">-Confirm</span></span>
<span data-ttu-id="d9df7-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d9df7-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9df7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9df7-136">-WhatIf</span></span>
<span data-ttu-id="d9df7-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d9df7-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9df7-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d9df7-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9df7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9df7-139">CommonParameters</span></span>
<span data-ttu-id="d9df7-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d9df7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9df7-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9df7-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9df7-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d9df7-142">INPUTS</span></span>

### <span data-ttu-id="d9df7-143">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d9df7-143">None</span></span>

## <span data-ttu-id="d9df7-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d9df7-144">OUTPUTS</span></span>

### <span data-ttu-id="d9df7-145">Microsoft. Azure. Commands. Network. model. PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d9df7-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="d9df7-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d9df7-146">NOTES</span></span>

## <span data-ttu-id="d9df7-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d9df7-147">RELATED LINKS</span></span>

[<span data-ttu-id="d9df7-148">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="d9df7-148">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)

[<span data-ttu-id="d9df7-149">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d9df7-149">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="d9df7-150">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d9df7-150">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
