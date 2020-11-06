---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNetworkRule.md
ms.openlocfilehash: 1100e42934c493bf8aea30e7372acc683b46b60b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588467"
---
# <span data-ttu-id="044dc-101">New-AzureRmFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="044dc-101">New-AzureRmFirewallNetworkRule</span></span>

## <span data-ttu-id="044dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="044dc-102">SYNOPSIS</span></span>
<span data-ttu-id="044dc-103">Güvenlik Duvarı ağ kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="044dc-103">Creates a Firewall Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="044dc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="044dc-104">SYNTAX</span></span>

```
New-AzureRmFirewallNetworkRule -Name <String> [-Description <String>]
 -SourceAddress <System.Collections.Generic.List`1[System.String]>
 -DestinationAddress <System.Collections.Generic.List`1[System.String]>
 -DestinationPort <System.Collections.Generic.List`1[System.String]>
 -Protocol <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="044dc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="044dc-105">DESCRIPTION</span></span>
<span data-ttu-id="044dc-106">**New-AzureRmFirewallNetworkRule** cmdlet 'ı, Azure Güvenlik Duvarı için bir ağ kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="044dc-106">The **New-AzureRmFirewallNetworkRule** cmdlet creates an network rule for Azure Firewall.</span></span>

## <span data-ttu-id="044dc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="044dc-107">EXAMPLES</span></span>

### <span data-ttu-id="044dc-108">1: tüm TCP trafiği için bir kural oluşturma</span><span class="sxs-lookup"><span data-stu-id="044dc-108">1:  Create a rule for all TCP traffic</span></span>
```
$rule = New-AzureRmFirewallNetworkRule -Name "all-tcp-traffic" -Description "Rule for all TCP traffic" -Protocol TCP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
```

<span data-ttu-id="044dc-109">Bu örnekte tüm TCP trafiği için bir kural oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="044dc-109">This example creates a rule for all TCP traffic.</span></span> <span data-ttu-id="044dc-110">Kullanıcı, ilişkili olduğu kural koleksiyonuna dayalı bir kural için trafiğin izin verilip verilmeyeceğini veya reddedildiğini kabul eder.</span><span class="sxs-lookup"><span data-stu-id="044dc-110">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="044dc-111">2:10.0.0.0 ile 60.1.5.0 arasında tüm TCP trafiği için bir kural oluşturun: 4040</span><span class="sxs-lookup"><span data-stu-id="044dc-111">2:  Create a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040</span></span>
```
$rule = New-AzureRmFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
```

<span data-ttu-id="044dc-112">Bu örnekte, 10.0.0.0 ile 60.1.5.0:4040 arasındaki tüm TCP trafiği için bir kural oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="044dc-112">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="044dc-113">Kullanıcı, ilişkili olduğu kural koleksiyonuna dayalı bir kural için trafiğin izin verilip verilmeyeceğini veya reddedildiğini kabul eder.</span><span class="sxs-lookup"><span data-stu-id="044dc-113">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

### <span data-ttu-id="044dc-114">3: herhangi bir kaynaktan 10.0.0.0/16 adresine giden tüm TCP ve ıCMP trafiği için bir kural oluşturun</span><span class="sxs-lookup"><span data-stu-id="044dc-114">3: Create a rule for all TCP and ICMP traffic from any source to 10.0.0.0/16</span></span>
```
$rule = New-AzureRmFirewallNetworkRule -Name "tcp-and-icmp-rule" -Description "Rule for all TCP and ICMP traffic from any source to 10.0.0.0/16" -Protocol TCP,ICMP -SourceAddress * -DestinationAddress "10.0.0.0/16" -DestinationPort *
```

<span data-ttu-id="044dc-115">Bu örnekte, 10.0.0.0 ile 60.1.5.0:4040 arasındaki tüm TCP trafiği için bir kural oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="044dc-115">This example creates a rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span> <span data-ttu-id="044dc-116">Kullanıcı, ilişkili olduğu kural koleksiyonuna dayalı bir kural için trafiğin izin verilip verilmeyeceğini veya reddedildiğini kabul eder.</span><span class="sxs-lookup"><span data-stu-id="044dc-116">User enforces whether traffic will be allowed or denied for a rule based on the rule collection it is associated with.</span></span>

## <span data-ttu-id="044dc-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="044dc-117">PARAMETERS</span></span>

### <span data-ttu-id="044dc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="044dc-118">-DefaultProfile</span></span>
<span data-ttu-id="044dc-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="044dc-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="044dc-120">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="044dc-120">-Description</span></span>
<span data-ttu-id="044dc-121">Bu kural için isteğe bağlı bir açıklama belirtin.</span><span class="sxs-lookup"><span data-stu-id="044dc-121">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="044dc-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="044dc-122">-DestinationAddress</span></span>
<span data-ttu-id="044dc-123">Kuralın hedef adresleri</span><span class="sxs-lookup"><span data-stu-id="044dc-123">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="044dc-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="044dc-124">-DestinationPort</span></span>
<span data-ttu-id="044dc-125">Kuralın hedef bağlantı noktaları</span><span class="sxs-lookup"><span data-stu-id="044dc-125">The destination ports of the rule</span></span>

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

### <span data-ttu-id="044dc-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="044dc-126">-Name</span></span>
<span data-ttu-id="044dc-127">Bu ağ kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="044dc-127">Specifies the name of this network rule.</span></span> <span data-ttu-id="044dc-128">Ad, bir kural koleksiyonunun içinde benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="044dc-128">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="044dc-129">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="044dc-129">-Protocol</span></span>
<span data-ttu-id="044dc-130">Bu kurala göre filtre uygulanacak trafik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="044dc-130">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="044dc-131">Olası değerler TCP, UDP, ıCMP ve Any değerleridir.</span><span class="sxs-lookup"><span data-stu-id="044dc-131">Possible values are TCP, UDP, ICMP and Any.</span></span>

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

### <span data-ttu-id="044dc-132">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="044dc-132">-SourceAddress</span></span>
<span data-ttu-id="044dc-133">Kuralın kaynak adresleri</span><span class="sxs-lookup"><span data-stu-id="044dc-133">The source addresses of the rule</span></span>

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

### <span data-ttu-id="044dc-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="044dc-134">-Confirm</span></span>
<span data-ttu-id="044dc-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="044dc-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="044dc-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="044dc-136">-WhatIf</span></span>
<span data-ttu-id="044dc-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="044dc-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="044dc-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="044dc-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="044dc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="044dc-139">CommonParameters</span></span>
<span data-ttu-id="044dc-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="044dc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="044dc-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="044dc-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="044dc-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="044dc-142">INPUTS</span></span>

### <span data-ttu-id="044dc-143">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="044dc-143">None</span></span>
<span data-ttu-id="044dc-144">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="044dc-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="044dc-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="044dc-145">OUTPUTS</span></span>

### <span data-ttu-id="044dc-146">Microsoft. Azure. Commands. Network. model. PSFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="044dc-146">Microsoft.Azure.Commands.Network.Models.PSFirewallNetworkRule</span></span>

## <span data-ttu-id="044dc-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="044dc-147">NOTES</span></span>

## <span data-ttu-id="044dc-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="044dc-148">RELATED LINKS</span></span>

[<span data-ttu-id="044dc-149">New-AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="044dc-149">New-AzureRmFirewallNetworkRuleCollection</span></span>](./New-AzureRmFirewallNetworkRuleCollection.md)

[<span data-ttu-id="044dc-150">Yeni-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="044dc-150">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="044dc-151">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="044dc-151">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)
