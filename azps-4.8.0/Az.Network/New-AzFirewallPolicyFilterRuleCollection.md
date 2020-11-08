---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyfilterrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyFilterRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyFilterRuleCollection.md
ms.openlocfilehash: d5871a9e1a99a27cc0b2728ca3638a0548f42fc6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274835"
---
# <span data-ttu-id="d51be-101">New-AzFirewallPolicyFilterRuleCollection</span><span class="sxs-lookup"><span data-stu-id="d51be-101">New-AzFirewallPolicyFilterRuleCollection</span></span>

## <span data-ttu-id="d51be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d51be-102">SYNOPSIS</span></span>
<span data-ttu-id="d51be-103">Yeni Azure Güvenlik Duvarı Ilkesi filtre kuralı koleksiyonu oluşturma</span><span class="sxs-lookup"><span data-stu-id="d51be-103">Create a new Azure Firewall Policy Filter Rule Collection</span></span>

## <span data-ttu-id="d51be-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d51be-104">SYNTAX</span></span>

```
New-AzFirewallPolicyFilterRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallPolicyRule[]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d51be-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d51be-105">DESCRIPTION</span></span>
<span data-ttu-id="d51be-106">**New-AzFirewallPolicyFilterRuleCollection** cmdlet 'ı Azure Güvenlik Duvarı Ilkesi için filtre kuralı koleksiyonu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d51be-106">The **New-AzFirewallPolicyFilterRuleCollection** cmdlet creates a Filter rule collection for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="d51be-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d51be-107">EXAMPLES</span></span>

### <span data-ttu-id="d51be-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d51be-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyFilterRuleCollection -Name FR1 -Priority 400 -Rule $appRule1 ,$appRule2 -ActionType "Allow"
```

<span data-ttu-id="d51be-109">Bu örnekte, 2 kural koşulu içeren bir filtre kuralı oluşturulur</span><span class="sxs-lookup"><span data-stu-id="d51be-109">This example creates a Filter rule with 2 rule conditions</span></span>

## <span data-ttu-id="d51be-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d51be-110">PARAMETERS</span></span>

### <span data-ttu-id="d51be-111">-ActionType</span><span class="sxs-lookup"><span data-stu-id="d51be-111">-ActionType</span></span>
<span data-ttu-id="d51be-112">Kural koleksiyonunun eylemi</span><span class="sxs-lookup"><span data-stu-id="d51be-112">The action of the rule collection</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d51be-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d51be-113">-DefaultProfile</span></span>
<span data-ttu-id="d51be-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d51be-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d51be-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="d51be-115">-Name</span></span>
<span data-ttu-id="d51be-116">Uygulama kuralı koleksiyonunun adı</span><span class="sxs-lookup"><span data-stu-id="d51be-116">The name of the Application Rule Collection</span></span>

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

### <span data-ttu-id="d51be-117">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="d51be-117">-Priority</span></span>
<span data-ttu-id="d51be-118">Kural koleksiyonunun önceliği</span><span class="sxs-lookup"><span data-stu-id="d51be-118">The priority of the rule collection</span></span>

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

### <span data-ttu-id="d51be-119">-Kural</span><span class="sxs-lookup"><span data-stu-id="d51be-119">-Rule</span></span>
<span data-ttu-id="d51be-120">Uygulama kuralları listesi</span><span class="sxs-lookup"><span data-stu-id="d51be-120">The list of application rules</span></span>

```yaml
Type: PSAzureFirewallPolicyRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d51be-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="d51be-121">-Confirm</span></span>
<span data-ttu-id="d51be-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d51be-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d51be-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d51be-123">-WhatIf</span></span>
<span data-ttu-id="d51be-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d51be-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d51be-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d51be-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d51be-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d51be-126">CommonParameters</span></span>
<span data-ttu-id="d51be-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d51be-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d51be-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d51be-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d51be-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d51be-129">INPUTS</span></span>

### <span data-ttu-id="d51be-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d51be-130">None</span></span>

## <span data-ttu-id="d51be-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d51be-131">OUTPUTS</span></span>

### <span data-ttu-id="d51be-132">Microsoft. Azure. Commands. Network. model. PSAzureFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="d51be-132">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="d51be-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d51be-133">NOTES</span></span>

## <span data-ttu-id="d51be-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d51be-134">RELATED LINKS</span></span>
