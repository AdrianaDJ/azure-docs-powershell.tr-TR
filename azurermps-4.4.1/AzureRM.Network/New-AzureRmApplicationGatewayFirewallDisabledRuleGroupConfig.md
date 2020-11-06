---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig.md
ms.openlocfilehash: 6ea379b1ad1629dc0ba3e7d747256c86153c651d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594618"
---
# <span data-ttu-id="789d9-101">New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig</span><span class="sxs-lookup"><span data-stu-id="789d9-101">New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>

## <span data-ttu-id="789d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="789d9-102">SYNOPSIS</span></span>
<span data-ttu-id="789d9-103">Devre dışı bırakılmış yeni bir kural grubu yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="789d9-103">Creates a new disabled rule group configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="789d9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="789d9-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName <String>
 [-Rules <System.Collections.Generic.List`1[System.Int32]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="789d9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="789d9-105">DESCRIPTION</span></span>
<span data-ttu-id="789d9-106">**New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet 'i, yeni devre dışı bir kural grubu yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="789d9-106">The **New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="789d9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="789d9-107">EXAMPLES</span></span>

### <span data-ttu-id="789d9-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="789d9-108">Example 1</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
```

<span data-ttu-id="789d9-109">Bu komut, kural 942130 ile "Istek-942-uygulama-SALDıRı-SQLI" adlı kural grubu için yeni bir devre dışı kural grubu yapılandırması oluşturur ve 942140 kuralı devre dışı bırakılıyor.</span><span class="sxs-lookup"><span data-stu-id="789d9-109">The command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span> <span data-ttu-id="789d9-110">Yeni devre dışı bırakılan kural grubu yapılandırması $disabledRuleGroup 1 ' ye kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="789d9-110">The new disabled rule group configuration is saved in $disabledRuleGroup1.</span></span>

## <span data-ttu-id="789d9-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="789d9-111">PARAMETERS</span></span>

### <span data-ttu-id="789d9-112">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="789d9-112">-RuleGroupName</span></span>
<span data-ttu-id="789d9-113">Devre dışı bırakılacak kural grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="789d9-113">The name of the rule group that will be disabled.</span></span>

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

### <span data-ttu-id="789d9-114">-Kurallar</span><span class="sxs-lookup"><span data-stu-id="789d9-114">-Rules</span></span>
<span data-ttu-id="789d9-115">Devre dışı bırakılacak kuralların listesi.</span><span class="sxs-lookup"><span data-stu-id="789d9-115">The list of rules that will be disabled.</span></span>
<span data-ttu-id="789d9-116">Null ise, kural grubundaki tüm kurallar devre dışı bırakılır.</span><span class="sxs-lookup"><span data-stu-id="789d9-116">If null, all rules of the rule group will be disabled.</span></span>

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

### <span data-ttu-id="789d9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="789d9-117">-DefaultProfile</span></span>
<span data-ttu-id="789d9-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="789d9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="789d9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="789d9-119">CommonParameters</span></span>
<span data-ttu-id="789d9-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="789d9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="789d9-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="789d9-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="789d9-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="789d9-122">INPUTS</span></span>

### <span data-ttu-id="789d9-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="789d9-123">None</span></span>

## <span data-ttu-id="789d9-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="789d9-124">OUTPUTS</span></span>

### <span data-ttu-id="789d9-125">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayFirewallDisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="789d9-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span></span>

## <span data-ttu-id="789d9-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="789d9-126">NOTES</span></span>

## <span data-ttu-id="789d9-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="789d9-127">RELATED LINKS</span></span>

[<span data-ttu-id="789d9-128">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="789d9-128">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="789d9-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="789d9-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

