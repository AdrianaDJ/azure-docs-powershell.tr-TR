---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewalldisabledrulegroupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
ms.openlocfilehash: 5eafcfc825b710e31954e247e4114d0f90e97c41
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104833"
---
# <span data-ttu-id="f1032-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span><span class="sxs-lookup"><span data-stu-id="f1032-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>

## <span data-ttu-id="f1032-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1032-102">SYNOPSIS</span></span>
<span data-ttu-id="f1032-103">Devre dışı bırakılmış yeni bir kural grubu yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f1032-103">Creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="f1032-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f1032-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName <String> [-Rules <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1032-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f1032-105">DESCRIPTION</span></span>
<span data-ttu-id="f1032-106">**Yeni-AzApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet 'i, yeni devre dışı bir kural grubu yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f1032-106">The **New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="f1032-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f1032-107">EXAMPLES</span></span>

### <span data-ttu-id="f1032-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f1032-108">Example 1</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
```

<span data-ttu-id="f1032-109">Bu komut, kural 942130 ile "Istek-942-uygulama-SALDıRı-SQLI" adlı kural grubu için yeni bir devre dışı kural grubu yapılandırması oluşturur ve 942140 kuralı devre dışı bırakılıyor.</span><span class="sxs-lookup"><span data-stu-id="f1032-109">The command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span> <span data-ttu-id="f1032-110">Yeni devre dışı bırakılan kural grubu yapılandırması $disabledRuleGroup 1 ' ye kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="f1032-110">The new disabled rule group configuration is saved in $disabledRuleGroup1.</span></span>

## <span data-ttu-id="f1032-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f1032-111">PARAMETERS</span></span>

### <span data-ttu-id="f1032-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1032-112">-DefaultProfile</span></span>
<span data-ttu-id="f1032-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f1032-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1032-114">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="f1032-114">-RuleGroupName</span></span>
<span data-ttu-id="f1032-115">Devre dışı bırakılacak kural grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f1032-115">The name of the rule group that will be disabled.</span></span>

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

### <span data-ttu-id="f1032-116">-Kurallar</span><span class="sxs-lookup"><span data-stu-id="f1032-116">-Rules</span></span>
<span data-ttu-id="f1032-117">Devre dışı bırakılacak kuralların listesi.</span><span class="sxs-lookup"><span data-stu-id="f1032-117">The list of rules that will be disabled.</span></span>
<span data-ttu-id="f1032-118">Null ise, kural grubundaki tüm kurallar devre dışı bırakılır.</span><span class="sxs-lookup"><span data-stu-id="f1032-118">If null, all rules of the rule group will be disabled.</span></span>

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

### <span data-ttu-id="f1032-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1032-119">CommonParameters</span></span>
<span data-ttu-id="f1032-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f1032-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1032-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1032-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1032-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f1032-122">INPUTS</span></span>

### <span data-ttu-id="f1032-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f1032-123">None</span></span>

## <span data-ttu-id="f1032-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f1032-124">OUTPUTS</span></span>

### <span data-ttu-id="f1032-125">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayFirewallDisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="f1032-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span></span>

## <span data-ttu-id="f1032-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f1032-126">NOTES</span></span>

## <span data-ttu-id="f1032-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f1032-127">RELATED LINKS</span></span>

[<span data-ttu-id="f1032-128">Yeni-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1032-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="f1032-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1032-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

