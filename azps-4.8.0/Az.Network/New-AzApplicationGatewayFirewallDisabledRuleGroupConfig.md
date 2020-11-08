---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewalldisabledrulegroupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
ms.openlocfilehash: 5eafcfc825b710e31954e247e4114d0f90e97c41
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268507"
---
# <span data-ttu-id="70bf4-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span><span class="sxs-lookup"><span data-stu-id="70bf4-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>

## <span data-ttu-id="70bf4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70bf4-102">SYNOPSIS</span></span>
<span data-ttu-id="70bf4-103">Devre dışı bırakılmış yeni bir kural grubu yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="70bf4-103">Creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="70bf4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="70bf4-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName <String> [-Rules <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70bf4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="70bf4-105">DESCRIPTION</span></span>
<span data-ttu-id="70bf4-106">**Yeni-AzApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet 'i, yeni devre dışı bir kural grubu yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="70bf4-106">The **New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="70bf4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="70bf4-107">EXAMPLES</span></span>

### <span data-ttu-id="70bf4-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="70bf4-108">Example 1</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
```

<span data-ttu-id="70bf4-109">Bu komut, kural 942130 ile "Istek-942-uygulama-SALDıRı-SQLI" adlı kural grubu için yeni bir devre dışı kural grubu yapılandırması oluşturur ve 942140 kuralı devre dışı bırakılıyor.</span><span class="sxs-lookup"><span data-stu-id="70bf4-109">The command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span> <span data-ttu-id="70bf4-110">Yeni devre dışı bırakılan kural grubu yapılandırması $disabledRuleGroup 1 ' ye kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="70bf4-110">The new disabled rule group configuration is saved in $disabledRuleGroup1.</span></span>

## <span data-ttu-id="70bf4-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="70bf4-111">PARAMETERS</span></span>

### <span data-ttu-id="70bf4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70bf4-112">-DefaultProfile</span></span>
<span data-ttu-id="70bf4-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="70bf4-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70bf4-114">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="70bf4-114">-RuleGroupName</span></span>
<span data-ttu-id="70bf4-115">Devre dışı bırakılacak kural grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="70bf4-115">The name of the rule group that will be disabled.</span></span>

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

### <span data-ttu-id="70bf4-116">-Kurallar</span><span class="sxs-lookup"><span data-stu-id="70bf4-116">-Rules</span></span>
<span data-ttu-id="70bf4-117">Devre dışı bırakılacak kuralların listesi.</span><span class="sxs-lookup"><span data-stu-id="70bf4-117">The list of rules that will be disabled.</span></span>
<span data-ttu-id="70bf4-118">Null ise, kural grubundaki tüm kurallar devre dışı bırakılır.</span><span class="sxs-lookup"><span data-stu-id="70bf4-118">If null, all rules of the rule group will be disabled.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70bf4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70bf4-119">CommonParameters</span></span>
<span data-ttu-id="70bf4-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="70bf4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70bf4-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70bf4-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70bf4-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="70bf4-122">INPUTS</span></span>

### <span data-ttu-id="70bf4-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="70bf4-123">None</span></span>

## <span data-ttu-id="70bf4-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="70bf4-124">OUTPUTS</span></span>

### <span data-ttu-id="70bf4-125">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayFirewallDisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="70bf4-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span></span>

## <span data-ttu-id="70bf4-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="70bf4-126">NOTES</span></span>

## <span data-ttu-id="70bf4-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="70bf4-127">RELATED LINKS</span></span>

[<span data-ttu-id="70bf4-128">Yeni-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="70bf4-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="70bf4-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="70bf4-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

