---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablewafruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
ms.openlocfilehash: e550d00d1d952fb372db81ec87a35c701d6dedde
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93931812"
---
# <span data-ttu-id="bb35c-101">Get-AzApplicationGatewayAvailableWafRuleSet</span><span class="sxs-lookup"><span data-stu-id="bb35c-101">Get-AzApplicationGatewayAvailableWafRuleSet</span></span>

## <span data-ttu-id="bb35c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb35c-102">SYNOPSIS</span></span>
<span data-ttu-id="bb35c-103">Kullanılabilir tüm Web uygulaması güvenlik duvarı kural kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="bb35c-103">Gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="bb35c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bb35c-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableWafRuleSet [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb35c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bb35c-105">DESCRIPTION</span></span>
<span data-ttu-id="bb35c-106">**Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet 'i kullanılabilir tüm Web uygulaması güvenlik duvarı kural kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="bb35c-106">The **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="bb35c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bb35c-107">EXAMPLES</span></span>

### <span data-ttu-id="bb35c-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bb35c-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzApplicationGatewayAvailableWafRuleSet
```

<span data-ttu-id="bb35c-109">Bu komut, kullanılabilen tüm Web uygulaması güvenlik duvarı kural kümelerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="bb35c-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="bb35c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bb35c-110">PARAMETERS</span></span>

### <span data-ttu-id="bb35c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb35c-111">-DefaultProfile</span></span>
<span data-ttu-id="bb35c-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bb35c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb35c-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb35c-113">CommonParameters</span></span>
<span data-ttu-id="bb35c-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bb35c-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb35c-115">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bb35c-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb35c-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bb35c-116">INPUTS</span></span>

### <span data-ttu-id="bb35c-117">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="bb35c-117">None</span></span>

## <span data-ttu-id="bb35c-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bb35c-118">OUTPUTS</span></span>

### <span data-ttu-id="bb35c-119">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="bb35c-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="bb35c-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bb35c-120">NOTES</span></span>
<span data-ttu-id="bb35c-121">**List-AzApplicationGatewayAvailableWafRuleSets** , **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet 'inin diğer adıdır.</span><span class="sxs-lookup"><span data-stu-id="bb35c-121">**List-AzApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet.</span></span>

## <span data-ttu-id="bb35c-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bb35c-122">RELATED LINKS</span></span>
