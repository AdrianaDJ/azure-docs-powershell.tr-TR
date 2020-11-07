---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayavailablewafrulesets
schema: 2.0.0
ms.openlocfilehash: 83ee8e673271079690c24691f22badfe5193ba50
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939348"
---
# <span data-ttu-id="e5229-101">Get-AzureRmApplicationGatewayAvailableWafRuleSets</span><span class="sxs-lookup"><span data-stu-id="e5229-101">Get-AzureRmApplicationGatewayAvailableWafRuleSets</span></span>

## <span data-ttu-id="e5229-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5229-102">SYNOPSIS</span></span>
<span data-ttu-id="e5229-103">Kullanılabilir tüm Web uygulaması güvenlik duvarı kural kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="e5229-103">Gets all available web application firewall rule sets.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5229-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e5229-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAvailableWafRuleSets [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e5229-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e5229-105">DESCRIPTION</span></span>
<span data-ttu-id="e5229-106">**Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet 'i kullanılabilir tüm Web uygulaması güvenlik duvarı kural kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="e5229-106">The **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="e5229-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e5229-107">EXAMPLES</span></span>

### <span data-ttu-id="e5229-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e5229-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzureRmApplicationGatewayAvailableWafRuleSets
```

<span data-ttu-id="e5229-109">Bu komut, kullanılabilen tüm Web uygulaması güvenlik duvarı kural kümelerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="e5229-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="e5229-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e5229-110">PARAMETERS</span></span>

### <span data-ttu-id="e5229-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5229-111">-DefaultProfile</span></span>
<span data-ttu-id="e5229-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e5229-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5229-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5229-113">CommonParameters</span></span>
<span data-ttu-id="e5229-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e5229-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5229-115">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5229-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5229-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e5229-116">INPUTS</span></span>

### <span data-ttu-id="e5229-117">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e5229-117">None</span></span>

## <span data-ttu-id="e5229-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e5229-118">OUTPUTS</span></span>

### <span data-ttu-id="e5229-119">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="e5229-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="e5229-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e5229-120">NOTES</span></span>
<span data-ttu-id="e5229-121">**List-AzureRmApplicationGatewayAvailableWafRuleSets** , **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet 'inin diğer adıdır.</span><span class="sxs-lookup"><span data-stu-id="e5229-121">**List-AzureRmApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet.</span></span>

## <span data-ttu-id="e5229-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e5229-122">RELATED LINKS</span></span>

