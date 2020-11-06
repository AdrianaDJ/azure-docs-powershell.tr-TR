---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F01CB88A-49E7-41D8-B4E7-F1A4DCDC6B84
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySku.md
ms.openlocfilehash: 09639badc9ac96525456b7a9556c8e2afa7ebf2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589981"
---
# <span data-ttu-id="493e1-101">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="493e1-101">Get-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="493e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="493e1-102">SYNOPSIS</span></span>
<span data-ttu-id="493e1-103">Uygulama ağ geçidi SKU 'YU alır.</span><span class="sxs-lookup"><span data-stu-id="493e1-103">Gets the SKU of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="493e1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="493e1-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySku -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="493e1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="493e1-105">DESCRIPTION</span></span>
<span data-ttu-id="493e1-106">**Get-AzureRmApplicationGatewaySku** cmdlet 'i, bir uygulama ağ geçidinin stok tutma BIRIMINI (SKU) alır.</span><span class="sxs-lookup"><span data-stu-id="493e1-106">The **Get-AzureRmApplicationGatewaySku** cmdlet gets the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="493e1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="493e1-107">EXAMPLES</span></span>

### <span data-ttu-id="493e1-108">Örnek 1: uygulama ağ geçidi SKU 'SU alma</span><span class="sxs-lookup"><span data-stu-id="493e1-108">Example 1: Get an application gateway SKU</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SKU = Get-AzureRmApplicationGatewaySku -ApplicationGateway $AppGW
```

<span data-ttu-id="493e1-109">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve sonucu $AppGW adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="493e1-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="493e1-110">İkinci komut, ApplicationGateway01 adındaki bir uygulama ağ geçidinin SKU 'SU alır ve sonucu $SKU adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="493e1-110">The second command gets the SKU of an application gateway named ApplicationGateway01 and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="493e1-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="493e1-111">PARAMETERS</span></span>

### <span data-ttu-id="493e1-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="493e1-112">-ApplicationGateway</span></span>
<span data-ttu-id="493e1-113">Uygulama ağ geçidi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="493e1-113">Specifies the application gateway object.</span></span>

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

### <span data-ttu-id="493e1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="493e1-114">-DefaultProfile</span></span>
<span data-ttu-id="493e1-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="493e1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="493e1-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="493e1-116">CommonParameters</span></span>
<span data-ttu-id="493e1-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="493e1-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="493e1-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="493e1-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="493e1-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="493e1-119">INPUTS</span></span>

### <span data-ttu-id="493e1-120">System. String</span><span class="sxs-lookup"><span data-stu-id="493e1-120">System.String</span></span>

## <span data-ttu-id="493e1-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="493e1-121">OUTPUTS</span></span>

### <span data-ttu-id="493e1-122">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="493e1-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="493e1-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="493e1-123">NOTES</span></span>

## <span data-ttu-id="493e1-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="493e1-124">RELATED LINKS</span></span>

[<span data-ttu-id="493e1-125">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="493e1-125">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="493e1-126">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="493e1-126">Set-AzureRmApplicationGatewaySku</span></span>](./Set-AzureRmApplicationGatewaySku.md)


