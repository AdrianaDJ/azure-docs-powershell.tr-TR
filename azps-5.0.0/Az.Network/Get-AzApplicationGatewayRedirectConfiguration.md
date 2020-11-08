---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 8a49bdeed095ee277d632559402c55ca3baf784c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279992"
---
# <span data-ttu-id="f6b6e-101">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6b6e-101">Get-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="f6b6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6b6e-102">SYNOPSIS</span></span>
<span data-ttu-id="f6b6e-103">Uygulama ağ geçidinden varolan bir yönlendirme yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="f6b6e-103">Gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="f6b6e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f6b6e-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRedirectConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6b6e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f6b6e-105">DESCRIPTION</span></span>
<span data-ttu-id="f6b6e-106">**Get-AzApplicationGatewayRedirectConfiguration** cmdlet 'ı, uygulama ağ geçidinden varolan bir yönlendirme yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="f6b6e-106">The **Get-AzApplicationGatewayRedirectConfiguration** cmdlet gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="f6b6e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f6b6e-107">EXAMPLES</span></span>

### <span data-ttu-id="f6b6e-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f6b6e-108">Example 1</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $RedirectConfig = Get-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -ApplicationGateway $AppGW
```

<span data-ttu-id="f6b6e-109">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve sonucu $AppGW adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="f6b6e-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="f6b6e-110">İkinci komut, $AppGW adlı değişkende depolanan uygulama ağ geçidinden Redirect01 adındaki yeniden yönlendirme yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="f6b6e-110">The second command gets the redirect configuration named Redirect01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="f6b6e-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f6b6e-111">PARAMETERS</span></span>

### <span data-ttu-id="f6b6e-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f6b6e-112">-ApplicationGateway</span></span>
<span data-ttu-id="f6b6e-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f6b6e-113">The applicationGateway</span></span>

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

### <span data-ttu-id="f6b6e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6b6e-114">-DefaultProfile</span></span>
<span data-ttu-id="f6b6e-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f6b6e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6b6e-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="f6b6e-116">-Name</span></span>
<span data-ttu-id="f6b6e-117">İstek yönlendirme kuralının adı</span><span class="sxs-lookup"><span data-stu-id="f6b6e-117">The name of the request routing rule</span></span>

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

### <span data-ttu-id="f6b6e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6b6e-118">CommonParameters</span></span>
<span data-ttu-id="f6b6e-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f6b6e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6b6e-120">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f6b6e-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6b6e-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f6b6e-121">INPUTS</span></span>

### <span data-ttu-id="f6b6e-122">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f6b6e-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f6b6e-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f6b6e-123">OUTPUTS</span></span>

### <span data-ttu-id="f6b6e-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6b6e-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="f6b6e-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f6b6e-125">NOTES</span></span>

## <span data-ttu-id="f6b6e-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f6b6e-126">RELATED LINKS</span></span>

[<span data-ttu-id="f6b6e-127">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6b6e-127">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="f6b6e-128">Yeni-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6b6e-128">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="f6b6e-129">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6b6e-129">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="f6b6e-130">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6b6e-130">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
