---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynatrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRuleCollection.md
ms.openlocfilehash: 010fd83d8b8e26e67e35afcc54b03ca0c1a5bd5a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277275"
---
# <span data-ttu-id="10cde-101">New-AzFirewallPolicyNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="10cde-101">New-AzFirewallPolicyNatRuleCollection</span></span>

## <span data-ttu-id="10cde-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10cde-102">SYNOPSIS</span></span>
<span data-ttu-id="10cde-103">Yeni Azure Güvenlik Duvarı Ilkesi oluşturma NAT kural koleksiyonu</span><span class="sxs-lookup"><span data-stu-id="10cde-103">Create a new Azure Firewall Policy Nat Rule Collection</span></span>

## <span data-ttu-id="10cde-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="10cde-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNatRuleCollection -Name <String> -Priority <UInt32>
 -Rule <PSAzureFirewallPolicyNetworkRule> -ActionType <String> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10cde-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="10cde-105">DESCRIPTION</span></span>
<span data-ttu-id="10cde-106">**New-AzFirewallPolicyNatRuleCollection** cmdlet 'i, bir Azure Güvenlik Duvarı Ilkesi için NAT kural koleksiyonu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="10cde-106">The **New-AzFirewallPolicyNatRuleCollection** cmdlet creates a Nat rule collection for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="10cde-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="10cde-107">EXAMPLES</span></span>

### <span data-ttu-id="10cde-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="10cde-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRuleCollection -Name NatRule1 -Priority 200 -Rule $netRule1 -ActionType "Dnat" -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="10cde-109">Bu örnek, bir ağ kuralıyla NAT kural koleksiyonu oluşturur</span><span class="sxs-lookup"><span data-stu-id="10cde-109">This example creates a nat rule collection with a network rule</span></span>

## <span data-ttu-id="10cde-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="10cde-110">PARAMETERS</span></span>

### <span data-ttu-id="10cde-111">-ActionType</span><span class="sxs-lookup"><span data-stu-id="10cde-111">-ActionType</span></span>
<span data-ttu-id="10cde-112">Kural eyleminin türü</span><span class="sxs-lookup"><span data-stu-id="10cde-112">The type of the rule action</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Dnat

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10cde-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10cde-113">-DefaultProfile</span></span>
<span data-ttu-id="10cde-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="10cde-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10cde-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="10cde-115">-Name</span></span>
<span data-ttu-id="10cde-116">Ağ kuralı koleksiyonunun adı</span><span class="sxs-lookup"><span data-stu-id="10cde-116">The name of the Network Rule Collection</span></span>

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

### <span data-ttu-id="10cde-117">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="10cde-117">-Priority</span></span>
<span data-ttu-id="10cde-118">Kural koleksiyonunun önceliği</span><span class="sxs-lookup"><span data-stu-id="10cde-118">The priority of the rule collection</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10cde-119">-Kural</span><span class="sxs-lookup"><span data-stu-id="10cde-119">-Rule</span></span>
<span data-ttu-id="10cde-120">Ağ kuralları listesi</span><span class="sxs-lookup"><span data-stu-id="10cde-120">The list of network rules</span></span>

```yaml
Type: PSAzureFirewallPolicyNetworkRule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10cde-121">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="10cde-121">-TranslatedAddress</span></span>
<span data-ttu-id="10cde-122">Bu NAT kuralı için çevrilen adres</span><span class="sxs-lookup"><span data-stu-id="10cde-122">The translated address for this NAT rule</span></span>

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

### <span data-ttu-id="10cde-123">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="10cde-123">-TranslatedPort</span></span>
<span data-ttu-id="10cde-124">Bu NAT kuralı için çevrilen bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="10cde-124">The translated port for this NAT rule</span></span>

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

### <span data-ttu-id="10cde-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="10cde-125">-Confirm</span></span>
<span data-ttu-id="10cde-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="10cde-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10cde-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10cde-127">-WhatIf</span></span>
<span data-ttu-id="10cde-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="10cde-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10cde-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="10cde-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10cde-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10cde-130">CommonParameters</span></span>
<span data-ttu-id="10cde-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="10cde-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10cde-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="10cde-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10cde-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="10cde-133">INPUTS</span></span>

### <span data-ttu-id="10cde-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="10cde-134">None</span></span>

## <span data-ttu-id="10cde-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="10cde-135">OUTPUTS</span></span>

### <span data-ttu-id="10cde-136">Microsoft. Azure. Commands. Network. model. PSAzureFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="10cde-136">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="10cde-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="10cde-137">NOTES</span></span>

## <span data-ttu-id="10cde-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="10cde-138">RELATED LINKS</span></span>
