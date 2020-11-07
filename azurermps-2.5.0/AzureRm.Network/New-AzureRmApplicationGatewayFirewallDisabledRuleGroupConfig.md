---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayfirewalldisabledrulegroupconfig
schema: 2.0.0
ms.openlocfilehash: 4e62a6c8820f9a9e6465c74746d589b343d99898
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939295"
---
# <span data-ttu-id="07e9c-101">New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig</span><span class="sxs-lookup"><span data-stu-id="07e9c-101">New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>

## <span data-ttu-id="07e9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07e9c-102">SYNOPSIS</span></span>
<span data-ttu-id="07e9c-103">Devre dışı bırakılmış yeni bir kural grubu yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="07e9c-103">Creates a new disabled rule group configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07e9c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="07e9c-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName <String>
 [-Rules <System.Collections.Generic.List`1[System.Int32]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="07e9c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="07e9c-105">DESCRIPTION</span></span>
<span data-ttu-id="07e9c-106">**New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet 'i, yeni devre dışı bir kural grubu yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="07e9c-106">The **New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="07e9c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="07e9c-107">EXAMPLES</span></span>

### <span data-ttu-id="07e9c-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="07e9c-108">Example 1</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
```

<span data-ttu-id="07e9c-109">Bu komut, kural 942130 ile "Istek-942-uygulama-SALDıRı-SQLI" adlı kural grubu için yeni bir devre dışı kural grubu yapılandırması oluşturur ve 942140 kuralı devre dışı bırakılıyor.</span><span class="sxs-lookup"><span data-stu-id="07e9c-109">The command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span> <span data-ttu-id="07e9c-110">Yeni devre dışı bırakılan kural grubu yapılandırması $disabledRuleGroup 1 ' ye kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="07e9c-110">The new disabled rule group configuration is saved in $disabledRuleGroup1.</span></span>

## <span data-ttu-id="07e9c-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="07e9c-111">PARAMETERS</span></span>

### <span data-ttu-id="07e9c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07e9c-112">-DefaultProfile</span></span>
<span data-ttu-id="07e9c-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="07e9c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07e9c-114">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="07e9c-114">-RuleGroupName</span></span>
<span data-ttu-id="07e9c-115">Devre dışı bırakılacak kural grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="07e9c-115">The name of the rule group that will be disabled.</span></span>

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

### <span data-ttu-id="07e9c-116">-Kurallar</span><span class="sxs-lookup"><span data-stu-id="07e9c-116">-Rules</span></span>
<span data-ttu-id="07e9c-117">Devre dışı bırakılacak kuralların listesi.</span><span class="sxs-lookup"><span data-stu-id="07e9c-117">The list of rules that will be disabled.</span></span>
<span data-ttu-id="07e9c-118">Null ise, kural grubundaki tüm kurallar devre dışı bırakılır.</span><span class="sxs-lookup"><span data-stu-id="07e9c-118">If null, all rules of the rule group will be disabled.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07e9c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07e9c-119">CommonParameters</span></span>
<span data-ttu-id="07e9c-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="07e9c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07e9c-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07e9c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07e9c-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="07e9c-122">INPUTS</span></span>

### <span data-ttu-id="07e9c-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="07e9c-123">None</span></span>

## <span data-ttu-id="07e9c-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="07e9c-124">OUTPUTS</span></span>

### <span data-ttu-id="07e9c-125">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayFirewallDisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="07e9c-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span></span>

## <span data-ttu-id="07e9c-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="07e9c-126">NOTES</span></span>

## <span data-ttu-id="07e9c-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="07e9c-127">RELATED LINKS</span></span>

[<span data-ttu-id="07e9c-128">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="07e9c-128">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="07e9c-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="07e9c-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

