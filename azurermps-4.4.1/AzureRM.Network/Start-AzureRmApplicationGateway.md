---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmApplicationGateway.md
ms.openlocfilehash: 8d6f52401544d723f7f5303aa45722d828a6ac59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587831"
---
# <span data-ttu-id="3ff9e-101">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3ff9e-101">Start-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="3ff9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ff9e-102">SYNOPSIS</span></span>
<span data-ttu-id="3ff9e-103">Uygulama ağ geçidi başlatır.</span><span class="sxs-lookup"><span data-stu-id="3ff9e-103">Starts an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ff9e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3ff9e-104">SYNTAX</span></span>

```
Start-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ff9e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3ff9e-105">DESCRIPTION</span></span>
<span data-ttu-id="3ff9e-106">**Start-AzureRmApplicationGateway** cmdlet 'ı bir Azure Application Gateway başlatır</span><span class="sxs-lookup"><span data-stu-id="3ff9e-106">The **Start-AzureRmApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="3ff9e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3ff9e-107">EXAMPLES</span></span>

### <span data-ttu-id="3ff9e-108">Example1: uygulama ağ geçidini başlatma</span><span class="sxs-lookup"><span data-stu-id="3ff9e-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="3ff9e-109">Bu komut, $AppGw değişkeninde depolanan uygulama ağ geçidini başlatır.</span><span class="sxs-lookup"><span data-stu-id="3ff9e-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="3ff9e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3ff9e-110">PARAMETERS</span></span>

### <span data-ttu-id="3ff9e-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3ff9e-111">-ApplicationGateway</span></span>
<span data-ttu-id="3ff9e-112">Bu cmdlet 'in başladığı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ff9e-112">Specifies the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="3ff9e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ff9e-113">-DefaultProfile</span></span>
<span data-ttu-id="3ff9e-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3ff9e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ff9e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ff9e-115">CommonParameters</span></span>
<span data-ttu-id="3ff9e-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3ff9e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ff9e-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ff9e-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ff9e-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3ff9e-118">INPUTS</span></span>

### <span data-ttu-id="3ff9e-119">System. String</span><span class="sxs-lookup"><span data-stu-id="3ff9e-119">System.String</span></span>

## <span data-ttu-id="3ff9e-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3ff9e-120">OUTPUTS</span></span>

### <span data-ttu-id="3ff9e-121">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3ff9e-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3ff9e-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3ff9e-122">NOTES</span></span>

## <span data-ttu-id="3ff9e-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3ff9e-123">RELATED LINKS</span></span>

[<span data-ttu-id="3ff9e-124">Stop-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3ff9e-124">Stop-AzureRmApplicationGateway</span></span>](./Stop-AzureRmApplicationGateway.md)


