---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayavailablewafrulesets
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableWafRuleSets.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableWafRuleSets.md
ms.openlocfilehash: fb16474d8a23f528aaaeb498ced4fa5a3e952236
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/21/2020
ms.locfileid: "93595208"
---
# <span data-ttu-id="24241-101">Get-AzureRmApplicationGatewayAvailableWafRuleSets</span><span class="sxs-lookup"><span data-stu-id="24241-101">Get-AzureRmApplicationGatewayAvailableWafRuleSets</span></span>

## <span data-ttu-id="24241-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24241-102">SYNOPSIS</span></span>
<span data-ttu-id="24241-103">Kullanılabilir tüm Web uygulaması güvenlik duvarı kural kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="24241-103">Gets all available web application firewall rule sets.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24241-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="24241-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAvailableWafRuleSets [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="24241-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="24241-105">DESCRIPTION</span></span>
<span data-ttu-id="24241-106">**Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet 'i kullanılabilir tüm Web uygulaması güvenlik duvarı kural kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="24241-106">The **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="24241-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="24241-107">EXAMPLES</span></span>

### <span data-ttu-id="24241-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="24241-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzureRmApplicationGatewayAvailableWafRuleSets
```

<span data-ttu-id="24241-109">Bu komut, kullanılabilen tüm Web uygulaması güvenlik duvarı kural kümelerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="24241-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="24241-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="24241-110">PARAMETERS</span></span>

### <span data-ttu-id="24241-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24241-111">-DefaultProfile</span></span>
<span data-ttu-id="24241-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="24241-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24241-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24241-113">CommonParameters</span></span>
<span data-ttu-id="24241-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="24241-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24241-115">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24241-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24241-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="24241-116">INPUTS</span></span>

### <span data-ttu-id="24241-117">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="24241-117">None</span></span>

## <span data-ttu-id="24241-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="24241-118">OUTPUTS</span></span>

### <span data-ttu-id="24241-119">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="24241-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="24241-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="24241-120">NOTES</span></span>
<span data-ttu-id="24241-121">**List-AzureRmApplicationGatewayAvailableWafRuleSets** , **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet 'inin diğer adıdır.</span><span class="sxs-lookup"><span data-stu-id="24241-121">**List-AzureRmApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet.</span></span>

## <span data-ttu-id="24241-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="24241-122">RELATED LINKS</span></span>

