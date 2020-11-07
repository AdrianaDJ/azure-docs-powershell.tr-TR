---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: 382c4cd1b189e0dc95edd4824dec58a280dbb889
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939682"
---
# <span data-ttu-id="c77b2-101">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c77b2-101">Start-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="c77b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c77b2-102">SYNOPSIS</span></span>
<span data-ttu-id="c77b2-103">Uygulama ağ geçidi başlatır.</span><span class="sxs-lookup"><span data-stu-id="c77b2-103">Starts an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c77b2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c77b2-104">SYNTAX</span></span>

```
Start-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c77b2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c77b2-105">DESCRIPTION</span></span>
<span data-ttu-id="c77b2-106">**Start-AzureRmApplicationGateway** cmdlet 'ı bir Azure Application Gateway başlatır</span><span class="sxs-lookup"><span data-stu-id="c77b2-106">The **Start-AzureRmApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="c77b2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c77b2-107">EXAMPLES</span></span>

### <span data-ttu-id="c77b2-108">Example1: uygulama ağ geçidini başlatma</span><span class="sxs-lookup"><span data-stu-id="c77b2-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="c77b2-109">Bu komut, $AppGw değişkeninde depolanan uygulama ağ geçidini başlatır.</span><span class="sxs-lookup"><span data-stu-id="c77b2-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="c77b2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c77b2-110">PARAMETERS</span></span>

### <span data-ttu-id="c77b2-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c77b2-111">-ApplicationGateway</span></span>
<span data-ttu-id="c77b2-112">Bu cmdlet 'in başladığı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c77b2-112">Specifies the application gateway that this cmdlet starts.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c77b2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c77b2-113">-DefaultProfile</span></span>
<span data-ttu-id="c77b2-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c77b2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c77b2-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c77b2-115">CommonParameters</span></span>
<span data-ttu-id="c77b2-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c77b2-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c77b2-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c77b2-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c77b2-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c77b2-118">INPUTS</span></span>

### <span data-ttu-id="c77b2-119">System. String</span><span class="sxs-lookup"><span data-stu-id="c77b2-119">System.String</span></span>

## <span data-ttu-id="c77b2-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c77b2-120">OUTPUTS</span></span>

### <span data-ttu-id="c77b2-121">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c77b2-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c77b2-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c77b2-122">NOTES</span></span>

## <span data-ttu-id="c77b2-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c77b2-123">RELATED LINKS</span></span>

[<span data-ttu-id="c77b2-124">Stop-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c77b2-124">Stop-AzureRmApplicationGateway</span></span>](./Stop-AzureRmApplicationGateway.md)


