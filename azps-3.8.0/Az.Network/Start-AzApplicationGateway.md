---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
ms.openlocfilehash: 974e30d9a287d18293515c019b0032bf36f15b51
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937431"
---
# <span data-ttu-id="80b52-101">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="80b52-101">Start-AzApplicationGateway</span></span>

## <span data-ttu-id="80b52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80b52-102">SYNOPSIS</span></span>
<span data-ttu-id="80b52-103">Uygulama ağ geçidi başlatır.</span><span class="sxs-lookup"><span data-stu-id="80b52-103">Starts an application gateway.</span></span>

## <span data-ttu-id="80b52-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="80b52-104">SYNTAX</span></span>

```
Start-AzApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80b52-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="80b52-105">DESCRIPTION</span></span>
<span data-ttu-id="80b52-106">**Start-AzApplicationGateway** cmdlet 'ı bir Azure Application Gateway başlatır</span><span class="sxs-lookup"><span data-stu-id="80b52-106">The **Start-AzApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="80b52-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="80b52-107">EXAMPLES</span></span>

### <span data-ttu-id="80b52-108">Example1: uygulama ağ geçidini başlatma</span><span class="sxs-lookup"><span data-stu-id="80b52-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="80b52-109">Bu komut, $AppGw değişkeninde depolanan uygulama ağ geçidini başlatır.</span><span class="sxs-lookup"><span data-stu-id="80b52-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="80b52-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="80b52-110">PARAMETERS</span></span>

### <span data-ttu-id="80b52-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="80b52-111">-ApplicationGateway</span></span>
<span data-ttu-id="80b52-112">Bu cmdlet 'in başladığı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="80b52-112">Specifies the application gateway that this cmdlet starts.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80b52-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80b52-113">-DefaultProfile</span></span>
<span data-ttu-id="80b52-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="80b52-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80b52-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80b52-115">CommonParameters</span></span>
<span data-ttu-id="80b52-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="80b52-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80b52-117">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80b52-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80b52-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="80b52-118">INPUTS</span></span>

### <span data-ttu-id="80b52-119">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="80b52-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="80b52-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="80b52-120">OUTPUTS</span></span>

### <span data-ttu-id="80b52-121">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="80b52-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="80b52-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="80b52-122">NOTES</span></span>

## <span data-ttu-id="80b52-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="80b52-123">RELATED LINKS</span></span>

[<span data-ttu-id="80b52-124">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="80b52-124">Stop-AzApplicationGateway</span></span>](./Stop-AzApplicationGateway.md)

