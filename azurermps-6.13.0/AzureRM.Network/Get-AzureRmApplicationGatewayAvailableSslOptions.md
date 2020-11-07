---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayavailablessloptions
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableSslOptions.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableSslOptions.md
ms.openlocfilehash: 157093dc382b4f56ac7759a9b32b42c8b2488d90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764940"
---
# <span data-ttu-id="b05d2-101">Get-AzureRmApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="b05d2-101">Get-AzureRmApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="b05d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b05d2-102">SYNOPSIS</span></span>
<span data-ttu-id="b05d2-103">Uygulama ağ geçidi için SSL ilkesi ile ilgili tüm SSL seçeneklerini alır.</span><span class="sxs-lookup"><span data-stu-id="b05d2-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b05d2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b05d2-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAvailableSslOptions [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b05d2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b05d2-105">DESCRIPTION</span></span>
<span data-ttu-id="b05d2-106">**Get-AzureRmApplicationGatewayAvailableSslOptions** cmdlet 'i SSL ilkesi için tüm kullanılabilir SSL seçeneklerini alır</span><span class="sxs-lookup"><span data-stu-id="b05d2-106">The **Get-AzureRmApplicationGatewayAvailableSslOptions** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="b05d2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b05d2-107">EXAMPLES</span></span>

### <span data-ttu-id="b05d2-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b05d2-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzureRmApplicationGatewayAvailableSslOptions
```

<span data-ttu-id="b05d2-109">Bu komut, SSL ilkesi için kullanılabilir tüm SSL seçeneklerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="b05d2-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="b05d2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b05d2-110">PARAMETERS</span></span>

### <span data-ttu-id="b05d2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b05d2-111">-DefaultProfile</span></span>
<span data-ttu-id="b05d2-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b05d2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b05d2-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b05d2-113">CommonParameters</span></span>
<span data-ttu-id="b05d2-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b05d2-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b05d2-115">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b05d2-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b05d2-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b05d2-116">INPUTS</span></span>

### <span data-ttu-id="b05d2-117">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b05d2-117">None</span></span>

## <span data-ttu-id="b05d2-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b05d2-118">OUTPUTS</span></span>

### <span data-ttu-id="b05d2-119">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="b05d2-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="b05d2-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b05d2-120">NOTES</span></span>

## <span data-ttu-id="b05d2-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b05d2-121">RELATED LINKS</span></span>
