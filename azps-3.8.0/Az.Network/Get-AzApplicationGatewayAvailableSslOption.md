---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablessloption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
ms.openlocfilehash: f2175583aaaf3af04120e22e32db79d7b20f1e30
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103583"
---
# <span data-ttu-id="89b86-101">Get-AzApplicationGatewayAvailableSslOption</span><span class="sxs-lookup"><span data-stu-id="89b86-101">Get-AzApplicationGatewayAvailableSslOption</span></span>

## <span data-ttu-id="89b86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89b86-102">SYNOPSIS</span></span>
<span data-ttu-id="89b86-103">Uygulama ağ geçidi için SSL ilkesi ile ilgili tüm SSL seçeneklerini alır.</span><span class="sxs-lookup"><span data-stu-id="89b86-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

## <span data-ttu-id="89b86-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="89b86-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableSslOption [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89b86-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="89b86-105">DESCRIPTION</span></span>
<span data-ttu-id="89b86-106">**Get-AzApplicationGatewayAvailableSslOption** cmdlet 'i SSL ilkesi için kullanılabilir tüm SSL seçeneklerini alır</span><span class="sxs-lookup"><span data-stu-id="89b86-106">The **Get-AzApplicationGatewayAvailableSslOption** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="89b86-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="89b86-107">EXAMPLES</span></span>

### <span data-ttu-id="89b86-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="89b86-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzApplicationGatewayAvailableSslOption
```

<span data-ttu-id="89b86-109">Bu komut, SSL ilkesi için kullanılabilir tüm SSL seçeneklerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="89b86-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="89b86-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="89b86-110">PARAMETERS</span></span>

### <span data-ttu-id="89b86-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89b86-111">-DefaultProfile</span></span>
<span data-ttu-id="89b86-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="89b86-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89b86-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89b86-113">CommonParameters</span></span>
<span data-ttu-id="89b86-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="89b86-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89b86-115">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="89b86-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89b86-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="89b86-116">INPUTS</span></span>

### <span data-ttu-id="89b86-117">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="89b86-117">None</span></span>

## <span data-ttu-id="89b86-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="89b86-118">OUTPUTS</span></span>

### <span data-ttu-id="89b86-119">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="89b86-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="89b86-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="89b86-120">NOTES</span></span>

## <span data-ttu-id="89b86-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="89b86-121">RELATED LINKS</span></span>
