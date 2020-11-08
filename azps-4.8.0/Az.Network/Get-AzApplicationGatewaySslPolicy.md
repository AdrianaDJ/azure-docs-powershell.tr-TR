---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 3e7e9559761bce69473511fbd6cdb94d635e13c9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267968"
---
# <span data-ttu-id="a14e0-101">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="a14e0-101">Get-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="a14e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a14e0-102">SYNOPSIS</span></span>
<span data-ttu-id="a14e0-103">Uygulama ağ geçidinin SSL ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="a14e0-103">Gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="a14e0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a14e0-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a14e0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a14e0-105">DESCRIPTION</span></span>
<span data-ttu-id="a14e0-106">**Get-AzApplicationGatewaySslPolicy** cmdlet 'i, bir uygulama ağ geçidinin SSL ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="a14e0-106">The **Get-AzApplicationGatewaySslPolicy** cmdlet gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="a14e0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a14e0-107">EXAMPLES</span></span>

### <span data-ttu-id="a14e0-108">2</span><span class="sxs-lookup"><span data-stu-id="a14e0-108">1:</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="a14e0-109">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve sonucu $AppGW adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="a14e0-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="a14e0-110">İkinci komut, $AppGW adlı değişkende depolanan uygulama ağ geçidinden SSL ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="a14e0-110">The second command gets the ssl policy from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="a14e0-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a14e0-111">PARAMETERS</span></span>

### <span data-ttu-id="a14e0-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a14e0-112">-ApplicationGateway</span></span>
<span data-ttu-id="a14e0-113">Bu cmdlet 'in aldığı SSL ilkesinin uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a14e0-113">Specifies the application gateway of the SSL policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a14e0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a14e0-114">-DefaultProfile</span></span>
<span data-ttu-id="a14e0-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a14e0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a14e0-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a14e0-116">CommonParameters</span></span>
<span data-ttu-id="a14e0-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a14e0-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a14e0-118">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a14e0-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a14e0-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a14e0-119">INPUTS</span></span>

### <span data-ttu-id="a14e0-120">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a14e0-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a14e0-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a14e0-121">OUTPUTS</span></span>

### <span data-ttu-id="a14e0-122">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="a14e0-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="a14e0-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a14e0-123">NOTES</span></span>
* <span data-ttu-id="a14e0-124">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="a14e0-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="a14e0-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a14e0-125">RELATED LINKS</span></span>

[<span data-ttu-id="a14e0-126">Yeni-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="a14e0-126">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="a14e0-127">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="a14e0-127">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


