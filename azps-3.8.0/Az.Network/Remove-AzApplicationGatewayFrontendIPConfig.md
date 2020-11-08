---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 289B761C-1A1D-46D2-8755-B6B6A4758EFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 8abfca99729dcbf99592a8efcb191e6a7883e3b4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94095837"
---
# <span data-ttu-id="683f7-101">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="683f7-101">Remove-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="683f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="683f7-102">SYNOPSIS</span></span>
<span data-ttu-id="683f7-103">Uygulama ağ geçidinden ön uç IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="683f7-103">Removes a front-end IP configuration from an application gateway.</span></span>

## <span data-ttu-id="683f7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="683f7-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendIPConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="683f7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="683f7-105">DESCRIPTION</span></span>
<span data-ttu-id="683f7-106">**Remove-Azapplicationgatewayfrontendıconfıg** cmdlet 'ı bir Azure uygulama ağ geçidinden ön uç IP 'yi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="683f7-106">The **Remove-AzApplicationGatewayFrontendIPConfig** cmdlet removes frontend IP from an Azure application gateway.</span></span>

## <span data-ttu-id="683f7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="683f7-107">EXAMPLES</span></span>

### <span data-ttu-id="683f7-108">Örnek 1: ön uç IP yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="683f7-108">Example 1: Remove a front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIP02"
```

<span data-ttu-id="683f7-109">İlk komut ApplicationGateway01 adındaki bir uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="683f7-109">The first command gets an application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="683f7-110">İkinci komut, $AppGw depolanan uygulama ağ geçidinden FrontEndIP02 adlı ön uç IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="683f7-110">The second command removes the front-end IP configuration named FrontEndIP02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="683f7-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="683f7-111">PARAMETERS</span></span>

### <span data-ttu-id="683f7-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="683f7-112">-ApplicationGateway</span></span>
<span data-ttu-id="683f7-113">Ön uç IP yapılandırmasının kaldırılacağı bir uygulama ağ geçidi belirtir.</span><span class="sxs-lookup"><span data-stu-id="683f7-113">Specifies an application gateway from which to remove a front-end IP configuration.</span></span>

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

### <span data-ttu-id="683f7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="683f7-114">-DefaultProfile</span></span>
<span data-ttu-id="683f7-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="683f7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="683f7-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="683f7-116">-Name</span></span>
<span data-ttu-id="683f7-117">Kaldırılacak ön uç IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="683f7-117">Specifies the name of a front-end IP configuration to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="683f7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="683f7-118">CommonParameters</span></span>
<span data-ttu-id="683f7-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="683f7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="683f7-120">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="683f7-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="683f7-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="683f7-121">INPUTS</span></span>

### <span data-ttu-id="683f7-122">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="683f7-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="683f7-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="683f7-123">OUTPUTS</span></span>

### <span data-ttu-id="683f7-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="683f7-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="683f7-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="683f7-125">NOTES</span></span>

## <span data-ttu-id="683f7-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="683f7-126">RELATED LINKS</span></span>

[<span data-ttu-id="683f7-127">Add-Azapplicationgatewayfrontendıconfıg yapılandırması</span><span class="sxs-lookup"><span data-stu-id="683f7-127">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="683f7-128">Get-Azapplicationgatewayfrontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="683f7-128">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="683f7-129">Yeni-Azapplicationgatewayfrontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="683f7-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="683f7-130">Set-Azapplicationgatewayfrontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="683f7-130">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


