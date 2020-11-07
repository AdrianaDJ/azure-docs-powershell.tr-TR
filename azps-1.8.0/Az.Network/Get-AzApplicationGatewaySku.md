---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F01CB88A-49E7-41D8-B4E7-F1A4DCDC6B84
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
ms.openlocfilehash: d12628390729f94c10e634e84a6373fd6368b46c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760636"
---
# <span data-ttu-id="223ad-101">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="223ad-101">Get-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="223ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="223ad-102">SYNOPSIS</span></span>
<span data-ttu-id="223ad-103">Uygulama ağ geçidi SKU 'YU alır.</span><span class="sxs-lookup"><span data-stu-id="223ad-103">Gets the SKU of an application gateway.</span></span>

## <span data-ttu-id="223ad-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="223ad-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="223ad-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="223ad-105">DESCRIPTION</span></span>
<span data-ttu-id="223ad-106">**Get-AzApplicationGatewaySku** cmdlet 'i, bir uygulama ağ geçidinin stok tutma BIRIMINI (SKU) alır.</span><span class="sxs-lookup"><span data-stu-id="223ad-106">The **Get-AzApplicationGatewaySku** cmdlet gets the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="223ad-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="223ad-107">EXAMPLES</span></span>

### <span data-ttu-id="223ad-108">Örnek 1: uygulama ağ geçidi SKU 'SU alma</span><span class="sxs-lookup"><span data-stu-id="223ad-108">Example 1: Get an application gateway SKU</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SKU = Get-AzApplicationGatewaySku -ApplicationGateway $AppGW
```

<span data-ttu-id="223ad-109">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve sonucu $AppGW adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="223ad-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="223ad-110">İkinci komut, ApplicationGateway01 adındaki bir uygulama ağ geçidinin SKU 'SU alır ve sonucu $SKU adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="223ad-110">The second command gets the SKU of an application gateway named ApplicationGateway01 and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="223ad-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="223ad-111">PARAMETERS</span></span>

### <span data-ttu-id="223ad-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="223ad-112">-ApplicationGateway</span></span>
<span data-ttu-id="223ad-113">Uygulama ağ geçidi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="223ad-113">Specifies the application gateway object.</span></span>

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

### <span data-ttu-id="223ad-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="223ad-114">-DefaultProfile</span></span>
<span data-ttu-id="223ad-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="223ad-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="223ad-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="223ad-116">CommonParameters</span></span>
<span data-ttu-id="223ad-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="223ad-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="223ad-118">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="223ad-118">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="223ad-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="223ad-119">INPUTS</span></span>

### <span data-ttu-id="223ad-120">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="223ad-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="223ad-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="223ad-121">OUTPUTS</span></span>

### <span data-ttu-id="223ad-122">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="223ad-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="223ad-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="223ad-123">NOTES</span></span>

## <span data-ttu-id="223ad-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="223ad-124">RELATED LINKS</span></span>

[<span data-ttu-id="223ad-125">Yeni-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="223ad-125">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="223ad-126">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="223ad-126">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)

