---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D41EDAC-17D9-494B-8336-67906F4E1E81
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 30f47cf6e345710da0e0d626929f65a33490e246
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103553"
---
# <span data-ttu-id="cc7cf-101">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="cc7cf-101">Get-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="cc7cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc7cf-102">SYNOPSIS</span></span>
<span data-ttu-id="cc7cf-103">Uygulama ağ geçidinin HTTP dinleyicisini alır.</span><span class="sxs-lookup"><span data-stu-id="cc7cf-103">Gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="cc7cf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cc7cf-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayHttpListener [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc7cf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cc7cf-105">DESCRIPTION</span></span>
<span data-ttu-id="cc7cf-106">**Get-AzApplicationGatewayHttpListener** cmdlet 'i, bir uygulama ağ geçidinin HTTP dinleyicisini alır.</span><span class="sxs-lookup"><span data-stu-id="cc7cf-106">The **Get-AzApplicationGatewayHttpListener** cmdlet gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="cc7cf-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cc7cf-107">EXAMPLES</span></span>

### <span data-ttu-id="cc7cf-108">Örnek 1: belirli bir HTTP dinleyicisi alma</span><span class="sxs-lookup"><span data-stu-id="cc7cf-108">Example 1: Get a specific HTTP listener</span></span>
```
PS C:\>$Appgw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listener = Get-AzApplicationGatewayHttpListener -Name "Listener01" -ApplicationGateway $Appgw
```

<span data-ttu-id="cc7cf-109">Bu komut, Listener01 adlı bir HTTP dinleyicisi alır.</span><span class="sxs-lookup"><span data-stu-id="cc7cf-109">This command gets an HTTP listener named Listener01.</span></span>

### <span data-ttu-id="cc7cf-110">Örnek 2: HTTP dinleyicilerinin listesini alma</span><span class="sxs-lookup"><span data-stu-id="cc7cf-110">Example 2: Get a list of HTTP listeners</span></span>
```
PS C:\>$Appgw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listeners = Get-AzApplicationGatewayHttpListener -ApplicationGateway $Appgw
```

<span data-ttu-id="cc7cf-111">Bu komut, HTTP dinleyicilerinin bir listesini alır.</span><span class="sxs-lookup"><span data-stu-id="cc7cf-111">This command gets a list of HTTP listeners.</span></span>

## <span data-ttu-id="cc7cf-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cc7cf-112">PARAMETERS</span></span>

### <span data-ttu-id="cc7cf-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cc7cf-113">-ApplicationGateway</span></span>
<span data-ttu-id="cc7cf-114">HTTP dinleyicisini içeren uygulama ağ geçidi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cc7cf-114">Specifies the application gateway object that contains the HTTP listener.</span></span>

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

### <span data-ttu-id="cc7cf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc7cf-115">-DefaultProfile</span></span>
<span data-ttu-id="cc7cf-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cc7cf-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc7cf-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="cc7cf-117">-Name</span></span>
<span data-ttu-id="cc7cf-118">Bu cmdlet 'in aldığı HTTP dinleyicisi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cc7cf-118">Specifies the name of the HTTP listener which this cmdlet gets.</span></span>

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

### <span data-ttu-id="cc7cf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc7cf-119">CommonParameters</span></span>
<span data-ttu-id="cc7cf-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cc7cf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc7cf-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="cc7cf-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc7cf-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cc7cf-122">INPUTS</span></span>

### <span data-ttu-id="cc7cf-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cc7cf-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cc7cf-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cc7cf-124">OUTPUTS</span></span>

### <span data-ttu-id="cc7cf-125">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="cc7cf-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="cc7cf-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cc7cf-126">NOTES</span></span>

## <span data-ttu-id="cc7cf-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cc7cf-127">RELATED LINKS</span></span>

[<span data-ttu-id="cc7cf-128">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="cc7cf-128">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="cc7cf-129">Yeni-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="cc7cf-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="cc7cf-130">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="cc7cf-130">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="cc7cf-131">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="cc7cf-131">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


