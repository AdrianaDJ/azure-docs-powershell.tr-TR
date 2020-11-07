---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-AzApplicationGatewayAvailableWafRuleSet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
ms.openlocfilehash: f8f8411a40ddbc4d0e2f0e4b508385717e0c4173
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935602"
---
# <span data-ttu-id="9e7d9-101">Get-AzApplicationGatewayAvailableWafRuleSet</span><span class="sxs-lookup"><span data-stu-id="9e7d9-101">Get-AzApplicationGatewayAvailableWafRuleSet</span></span>

## <span data-ttu-id="9e7d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e7d9-102">SYNOPSIS</span></span>
<span data-ttu-id="9e7d9-103">Kullanılabilir tüm Web uygulaması güvenlik duvarı kural kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="9e7d9-103">Gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="9e7d9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9e7d9-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableWafRuleSet [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e7d9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9e7d9-105">DESCRIPTION</span></span>
<span data-ttu-id="9e7d9-106">**Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet 'i kullanılabilir tüm Web uygulaması güvenlik duvarı kural kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="9e7d9-106">The **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="9e7d9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9e7d9-107">EXAMPLES</span></span>

### <span data-ttu-id="9e7d9-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9e7d9-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzApplicationGatewayAvailableWafRuleSet
```

<span data-ttu-id="9e7d9-109">Bu komut, kullanılabilen tüm Web uygulaması güvenlik duvarı kural kümelerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="9e7d9-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="9e7d9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9e7d9-110">PARAMETERS</span></span>

### <span data-ttu-id="9e7d9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e7d9-111">-DefaultProfile</span></span>
<span data-ttu-id="9e7d9-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9e7d9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e7d9-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e7d9-113">CommonParameters</span></span>
<span data-ttu-id="9e7d9-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9e7d9-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e7d9-115">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e7d9-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e7d9-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9e7d9-116">INPUTS</span></span>

### <span data-ttu-id="9e7d9-117">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="9e7d9-117">None</span></span>

## <span data-ttu-id="9e7d9-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9e7d9-118">OUTPUTS</span></span>

### <span data-ttu-id="9e7d9-119">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="9e7d9-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="9e7d9-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9e7d9-120">NOTES</span></span>
<span data-ttu-id="9e7d9-121">**List-AzApplicationGatewayAvailableWafRuleSet** , **Get-azapplicationgatewayavailablewafruleset** cmdlet 'inin diğer adıdır.</span><span class="sxs-lookup"><span data-stu-id="9e7d9-121">**List-AzApplicationGatewayAvailableWafRuleSet** is an alias for the **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet.</span></span>

## <span data-ttu-id="9e7d9-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9e7d9-122">RELATED LINKS</span></span>

