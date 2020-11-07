---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablessloption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
ms.openlocfilehash: 04a24ee5148782f4a15aa5b93ffb937ad312ccfb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760668"
---
# <span data-ttu-id="33400-101">Get-AzApplicationGatewayAvailableSslOption</span><span class="sxs-lookup"><span data-stu-id="33400-101">Get-AzApplicationGatewayAvailableSslOption</span></span>

## <span data-ttu-id="33400-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33400-102">SYNOPSIS</span></span>
<span data-ttu-id="33400-103">Uygulama ağ geçidi için SSL ilkesi ile ilgili tüm SSL seçeneklerini alır.</span><span class="sxs-lookup"><span data-stu-id="33400-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

## <span data-ttu-id="33400-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="33400-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableSslOption [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33400-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="33400-105">DESCRIPTION</span></span>
<span data-ttu-id="33400-106">**Get-AzApplicationGatewayAvailableSslOption** cmdlet 'i SSL ilkesi için kullanılabilir tüm SSL seçeneklerini alır</span><span class="sxs-lookup"><span data-stu-id="33400-106">The **Get-AzApplicationGatewayAvailableSslOption** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="33400-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="33400-107">EXAMPLES</span></span>

### <span data-ttu-id="33400-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="33400-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzApplicationGatewayAvailableSslOption
```

<span data-ttu-id="33400-109">Bu komut, SSL ilkesi için kullanılabilir tüm SSL seçeneklerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="33400-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="33400-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="33400-110">PARAMETERS</span></span>

### <span data-ttu-id="33400-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33400-111">-DefaultProfile</span></span>
<span data-ttu-id="33400-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="33400-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33400-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33400-113">CommonParameters</span></span>
<span data-ttu-id="33400-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="33400-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33400-115">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="33400-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33400-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="33400-116">INPUTS</span></span>

### <span data-ttu-id="33400-117">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="33400-117">None</span></span>

## <span data-ttu-id="33400-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="33400-118">OUTPUTS</span></span>

### <span data-ttu-id="33400-119">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="33400-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="33400-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="33400-120">NOTES</span></span>

## <span data-ttu-id="33400-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="33400-121">RELATED LINKS</span></span>
