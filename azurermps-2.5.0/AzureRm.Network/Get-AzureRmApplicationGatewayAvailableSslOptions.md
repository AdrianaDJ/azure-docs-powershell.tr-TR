---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayavailablessloptions
schema: 2.0.0
ms.openlocfilehash: 023b2a43114fe47b50956e7f4626a75706e914f5
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939349"
---
# <span data-ttu-id="fd30a-101">Get-AzureRmApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="fd30a-101">Get-AzureRmApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="fd30a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd30a-102">SYNOPSIS</span></span>
<span data-ttu-id="fd30a-103">Uygulama ağ geçidi için SSL ilkesi ile ilgili tüm SSL seçeneklerini alır.</span><span class="sxs-lookup"><span data-stu-id="fd30a-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd30a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fd30a-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAvailableSslOptions [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fd30a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fd30a-105">DESCRIPTION</span></span>
<span data-ttu-id="fd30a-106">**Get-AzureRmApplicationGatewayAvailableSslOptions** cmdlet 'i SSL ilkesi için tüm kullanılabilir SSL seçeneklerini alır</span><span class="sxs-lookup"><span data-stu-id="fd30a-106">The **Get-AzureRmApplicationGatewayAvailableSslOptions** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="fd30a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fd30a-107">EXAMPLES</span></span>

### <span data-ttu-id="fd30a-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fd30a-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzureRmApplicationGatewayAvailableSslOptions
```

<span data-ttu-id="fd30a-109">Bu komut, SSL ilkesi için kullanılabilir tüm SSL seçeneklerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="fd30a-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="fd30a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fd30a-110">PARAMETERS</span></span>

### <span data-ttu-id="fd30a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd30a-111">-DefaultProfile</span></span>
<span data-ttu-id="fd30a-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fd30a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd30a-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd30a-113">CommonParameters</span></span>
<span data-ttu-id="fd30a-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fd30a-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd30a-115">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd30a-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd30a-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fd30a-116">INPUTS</span></span>

### <span data-ttu-id="fd30a-117">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="fd30a-117">None</span></span>

## <span data-ttu-id="fd30a-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fd30a-118">OUTPUTS</span></span>

### <span data-ttu-id="fd30a-119">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="fd30a-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="fd30a-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fd30a-120">NOTES</span></span>

## <span data-ttu-id="fd30a-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fd30a-121">RELATED LINKS</span></span>

