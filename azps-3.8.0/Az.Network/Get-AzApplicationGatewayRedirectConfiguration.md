---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 8a49bdeed095ee277d632559402c55ca3baf784c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937825"
---
# <span data-ttu-id="fae56-101">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="fae56-101">Get-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="fae56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fae56-102">SYNOPSIS</span></span>
<span data-ttu-id="fae56-103">Uygulama ağ geçidinden varolan bir yönlendirme yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="fae56-103">Gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="fae56-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fae56-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRedirectConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fae56-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fae56-105">DESCRIPTION</span></span>
<span data-ttu-id="fae56-106">**Get-AzApplicationGatewayRedirectConfiguration** cmdlet 'ı, uygulama ağ geçidinden varolan bir yönlendirme yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="fae56-106">The **Get-AzApplicationGatewayRedirectConfiguration** cmdlet gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="fae56-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fae56-107">EXAMPLES</span></span>

### <span data-ttu-id="fae56-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fae56-108">Example 1</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $RedirectConfig = Get-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -ApplicationGateway $AppGW
```

<span data-ttu-id="fae56-109">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve sonucu $AppGW adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="fae56-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="fae56-110">İkinci komut, $AppGW adlı değişkende depolanan uygulama ağ geçidinden Redirect01 adındaki yeniden yönlendirme yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="fae56-110">The second command gets the redirect configuration named Redirect01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="fae56-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fae56-111">PARAMETERS</span></span>

### <span data-ttu-id="fae56-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fae56-112">-ApplicationGateway</span></span>
<span data-ttu-id="fae56-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fae56-113">The applicationGateway</span></span>

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

### <span data-ttu-id="fae56-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fae56-114">-DefaultProfile</span></span>
<span data-ttu-id="fae56-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fae56-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fae56-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="fae56-116">-Name</span></span>
<span data-ttu-id="fae56-117">İstek yönlendirme kuralının adı</span><span class="sxs-lookup"><span data-stu-id="fae56-117">The name of the request routing rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fae56-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fae56-118">CommonParameters</span></span>
<span data-ttu-id="fae56-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fae56-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fae56-120">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="fae56-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fae56-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fae56-121">INPUTS</span></span>

### <span data-ttu-id="fae56-122">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fae56-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fae56-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fae56-123">OUTPUTS</span></span>

### <span data-ttu-id="fae56-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="fae56-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="fae56-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fae56-125">NOTES</span></span>

## <span data-ttu-id="fae56-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fae56-126">RELATED LINKS</span></span>

[<span data-ttu-id="fae56-127">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="fae56-127">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="fae56-128">Yeni-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="fae56-128">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="fae56-129">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="fae56-129">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="fae56-130">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="fae56-130">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)