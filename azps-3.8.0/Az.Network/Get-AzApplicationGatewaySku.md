---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F01CB88A-49E7-41D8-B4E7-F1A4DCDC6B84
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
ms.openlocfilehash: c8bd4a0070aa0e5635fad7cb20a627a7d23f5922
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937819"
---
# <span data-ttu-id="897a9-101">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="897a9-101">Get-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="897a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="897a9-102">SYNOPSIS</span></span>
<span data-ttu-id="897a9-103">Uygulama ağ geçidi SKU 'YU alır.</span><span class="sxs-lookup"><span data-stu-id="897a9-103">Gets the SKU of an application gateway.</span></span>

## <span data-ttu-id="897a9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="897a9-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="897a9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="897a9-105">DESCRIPTION</span></span>
<span data-ttu-id="897a9-106">**Get-AzApplicationGatewaySku** cmdlet 'i, bir uygulama ağ geçidinin stok tutma BIRIMINI (SKU) alır.</span><span class="sxs-lookup"><span data-stu-id="897a9-106">The **Get-AzApplicationGatewaySku** cmdlet gets the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="897a9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="897a9-107">EXAMPLES</span></span>

### <span data-ttu-id="897a9-108">Örnek 1: uygulama ağ geçidi SKU 'SU alma</span><span class="sxs-lookup"><span data-stu-id="897a9-108">Example 1: Get an application gateway SKU</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SKU = Get-AzApplicationGatewaySku -ApplicationGateway $AppGW
```

<span data-ttu-id="897a9-109">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve sonucu $AppGW adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="897a9-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="897a9-110">İkinci komut, ApplicationGateway01 adındaki bir uygulama ağ geçidinin SKU 'SU alır ve sonucu $SKU adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="897a9-110">The second command gets the SKU of an application gateway named ApplicationGateway01 and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="897a9-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="897a9-111">PARAMETERS</span></span>

### <span data-ttu-id="897a9-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="897a9-112">-ApplicationGateway</span></span>
<span data-ttu-id="897a9-113">Uygulama ağ geçidi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="897a9-113">Specifies the application gateway object.</span></span>

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

### <span data-ttu-id="897a9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="897a9-114">-DefaultProfile</span></span>
<span data-ttu-id="897a9-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="897a9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="897a9-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="897a9-116">CommonParameters</span></span>
<span data-ttu-id="897a9-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="897a9-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="897a9-118">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="897a9-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="897a9-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="897a9-119">INPUTS</span></span>

### <span data-ttu-id="897a9-120">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="897a9-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="897a9-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="897a9-121">OUTPUTS</span></span>

### <span data-ttu-id="897a9-122">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="897a9-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="897a9-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="897a9-123">NOTES</span></span>

## <span data-ttu-id="897a9-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="897a9-124">RELATED LINKS</span></span>

[<span data-ttu-id="897a9-125">Yeni-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="897a9-125">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="897a9-126">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="897a9-126">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


