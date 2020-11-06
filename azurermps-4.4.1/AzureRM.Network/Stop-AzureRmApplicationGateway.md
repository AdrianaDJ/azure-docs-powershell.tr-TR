---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmApplicationGateway.md
ms.openlocfilehash: 6c2de883a797c445105edddfc562bc2d494fd234
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587830"
---
# <span data-ttu-id="b2cbf-101">Stop-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b2cbf-101">Stop-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="b2cbf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2cbf-102">SYNOPSIS</span></span>
<span data-ttu-id="b2cbf-103">Uygulama ağ geçidini durdurur</span><span class="sxs-lookup"><span data-stu-id="b2cbf-103">Stops an application gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2cbf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b2cbf-104">SYNTAX</span></span>

```
Stop-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2cbf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b2cbf-105">DESCRIPTION</span></span>
<span data-ttu-id="b2cbf-106">**Stop-AzureRmApplicationGateway** cmdlet 'i bir uygulama ağ geçidini durdurur.</span><span class="sxs-lookup"><span data-stu-id="b2cbf-106">The **Stop-AzureRmApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="b2cbf-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b2cbf-107">EXAMPLES</span></span>

### <span data-ttu-id="b2cbf-108">Örnek 1: uygulama ağ geçidini durdurma</span><span class="sxs-lookup"><span data-stu-id="b2cbf-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="b2cbf-109">Bu komut $AppGw değişkeninde depolanan uygulama ağ geçidini durdurur.</span><span class="sxs-lookup"><span data-stu-id="b2cbf-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="b2cbf-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b2cbf-110">PARAMETERS</span></span>

### <span data-ttu-id="b2cbf-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b2cbf-111">-ApplicationGateway</span></span>
<span data-ttu-id="b2cbf-112">Bu cmdlet 'in durdurduğu uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b2cbf-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="b2cbf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2cbf-113">-DefaultProfile</span></span>
<span data-ttu-id="b2cbf-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b2cbf-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2cbf-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2cbf-115">CommonParameters</span></span>
<span data-ttu-id="b2cbf-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b2cbf-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2cbf-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2cbf-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2cbf-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b2cbf-118">INPUTS</span></span>

### <span data-ttu-id="b2cbf-119">System. String</span><span class="sxs-lookup"><span data-stu-id="b2cbf-119">System.String</span></span>

## <span data-ttu-id="b2cbf-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b2cbf-120">OUTPUTS</span></span>

### <span data-ttu-id="b2cbf-121">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b2cbf-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b2cbf-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b2cbf-122">NOTES</span></span>

## <span data-ttu-id="b2cbf-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b2cbf-123">RELATED LINKS</span></span>

[<span data-ttu-id="b2cbf-124">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b2cbf-124">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="b2cbf-125">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b2cbf-125">New-AzureRmApplicationGateway</span></span>](./New-AzureRmApplicationGateway.md)

[<span data-ttu-id="b2cbf-126">Remove-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b2cbf-126">Remove-AzureRmApplicationGateway</span></span>](./Remove-AzureRmApplicationGateway.md)

[<span data-ttu-id="b2cbf-127">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b2cbf-127">Set-AzureRmApplicationGateway</span></span>](./Set-AzureRmApplicationGateway.md)

[<span data-ttu-id="b2cbf-128">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b2cbf-128">Start-AzureRmApplicationGateway</span></span>](./Start-AzureRmApplicationGateway.md)


