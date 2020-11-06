---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayavailablewafrulesets
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableWafRuleSets.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableWafRuleSets.md
ms.openlocfilehash: d5e65b90c818102f2cb61997f0e5ff08640d6395
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588074"
---
# <span data-ttu-id="1e2b6-101">Get-AzureRmApplicationGatewayAvailableWafRuleSets</span><span class="sxs-lookup"><span data-stu-id="1e2b6-101">Get-AzureRmApplicationGatewayAvailableWafRuleSets</span></span>

## <span data-ttu-id="1e2b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e2b6-102">SYNOPSIS</span></span>
<span data-ttu-id="1e2b6-103">Kullanılabilir tüm Web uygulaması güvenlik duvarı kural kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="1e2b6-103">Gets all available web application firewall rule sets.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e2b6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1e2b6-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAvailableWafRuleSets [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1e2b6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1e2b6-105">DESCRIPTION</span></span>
<span data-ttu-id="1e2b6-106">**Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet 'i kullanılabilir tüm Web uygulaması güvenlik duvarı kural kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="1e2b6-106">The **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="1e2b6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1e2b6-107">EXAMPLES</span></span>

### <span data-ttu-id="1e2b6-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1e2b6-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzureRmApplicationGatewayAvailableWafRuleSets
```

<span data-ttu-id="1e2b6-109">Bu komut, kullanılabilen tüm Web uygulaması güvenlik duvarı kural kümelerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="1e2b6-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="1e2b6-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1e2b6-110">PARAMETERS</span></span>

### <span data-ttu-id="1e2b6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e2b6-111">-DefaultProfile</span></span>
<span data-ttu-id="1e2b6-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1e2b6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e2b6-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e2b6-113">CommonParameters</span></span>
<span data-ttu-id="1e2b6-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1e2b6-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e2b6-115">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e2b6-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e2b6-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1e2b6-116">INPUTS</span></span>

### <span data-ttu-id="1e2b6-117">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1e2b6-117">None</span></span>

## <span data-ttu-id="1e2b6-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1e2b6-118">OUTPUTS</span></span>

### <span data-ttu-id="1e2b6-119">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="1e2b6-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="1e2b6-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1e2b6-120">NOTES</span></span>
<span data-ttu-id="1e2b6-121">**List-AzureRmApplicationGatewayAvailableWafRuleSets** , **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet 'inin diğer adıdır.</span><span class="sxs-lookup"><span data-stu-id="1e2b6-121">**List-AzureRmApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet.</span></span>

## <span data-ttu-id="1e2b6-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1e2b6-122">RELATED LINKS</span></span>
