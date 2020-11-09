---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
ms.openlocfilehash: 974e30d9a287d18293515c019b0032bf36f15b51
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325714"
---
# <span data-ttu-id="835e5-101">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="835e5-101">Start-AzApplicationGateway</span></span>

## <span data-ttu-id="835e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="835e5-102">SYNOPSIS</span></span>
<span data-ttu-id="835e5-103">Uygulama ağ geçidi başlatır.</span><span class="sxs-lookup"><span data-stu-id="835e5-103">Starts an application gateway.</span></span>

## <span data-ttu-id="835e5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="835e5-104">SYNTAX</span></span>

```
Start-AzApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="835e5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="835e5-105">DESCRIPTION</span></span>
<span data-ttu-id="835e5-106">**Start-AzApplicationGateway** cmdlet 'ı bir Azure Application Gateway başlatır</span><span class="sxs-lookup"><span data-stu-id="835e5-106">The **Start-AzApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="835e5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="835e5-107">EXAMPLES</span></span>

### <span data-ttu-id="835e5-108">Example1: uygulama ağ geçidini başlatma</span><span class="sxs-lookup"><span data-stu-id="835e5-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="835e5-109">Bu komut, $AppGw değişkeninde depolanan uygulama ağ geçidini başlatır.</span><span class="sxs-lookup"><span data-stu-id="835e5-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="835e5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="835e5-110">PARAMETERS</span></span>

### <span data-ttu-id="835e5-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="835e5-111">-ApplicationGateway</span></span>
<span data-ttu-id="835e5-112">Bu cmdlet 'in başladığı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="835e5-112">Specifies the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="835e5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="835e5-113">-DefaultProfile</span></span>
<span data-ttu-id="835e5-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="835e5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="835e5-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="835e5-115">CommonParameters</span></span>
<span data-ttu-id="835e5-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="835e5-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="835e5-117">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="835e5-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="835e5-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="835e5-118">INPUTS</span></span>

### <span data-ttu-id="835e5-119">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="835e5-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="835e5-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="835e5-120">OUTPUTS</span></span>

### <span data-ttu-id="835e5-121">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="835e5-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="835e5-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="835e5-122">NOTES</span></span>

## <span data-ttu-id="835e5-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="835e5-123">RELATED LINKS</span></span>

[<span data-ttu-id="835e5-124">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="835e5-124">Stop-AzApplicationGateway</span></span>](./Stop-AzApplicationGateway.md)


