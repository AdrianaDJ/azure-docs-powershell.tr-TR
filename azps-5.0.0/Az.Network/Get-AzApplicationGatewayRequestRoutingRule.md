---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 57A6DB40-43EC-402C-9784-06817ECD99B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 75666d2f897adeda4031b03309979366949a0040
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279987"
---
# <span data-ttu-id="09c55-101">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="09c55-101">Get-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="09c55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09c55-102">SYNOPSIS</span></span>
<span data-ttu-id="09c55-103">Uygulama ağ geçidinin istek yönlendirme kuralını alır.</span><span class="sxs-lookup"><span data-stu-id="09c55-103">Gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="09c55-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="09c55-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRequestRoutingRule [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09c55-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="09c55-105">DESCRIPTION</span></span>
<span data-ttu-id="09c55-106">**Get-AzApplicationGatewayRequestRoutingRule** cmdlet 'i, bir uygulama ağ geçidinin istek yönlendirme kuralını alır.</span><span class="sxs-lookup"><span data-stu-id="09c55-106">The **Get-AzApplicationGatewayRequestRoutingRule** cmdlet gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="09c55-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="09c55-107">EXAMPLES</span></span>

### <span data-ttu-id="09c55-108">Örnek 1: belirli bir istek yönlendirme kuralı alma</span><span class="sxs-lookup"><span data-stu-id="09c55-108">Example 1: Get a specific request routing rule</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRequestRoutingRule -"Rule01" -ApplicationGateway $AppGW
```

<span data-ttu-id="09c55-109">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve sonucu $AppGW adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="09c55-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="09c55-110">İkinci komut, $AppGW adlı değişkende depolanan uygulama ağ geçidinden Rule01 adındaki istek yönlendirme kuralını alır.</span><span class="sxs-lookup"><span data-stu-id="09c55-110">The second command gets the request routing rule named Rule01 from the Application Gateway stored in the variable named $AppGW.</span></span>

### <span data-ttu-id="09c55-111">Örnek 2: istek yönlendirme kuralları listesini alma</span><span class="sxs-lookup"><span data-stu-id="09c55-111">Example 2: Get a list of request routing rules</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rules = Get-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGW
```

<span data-ttu-id="09c55-112">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve sonucu $AppGW adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="09c55-112">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="09c55-113">İkinci komut, $AppGW adlı değişkende depolanan uygulama ağ geçidinden gelen istek yönlendirme kuralları listesini alır.</span><span class="sxs-lookup"><span data-stu-id="09c55-113">The second command gets a list of request routing rules from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="09c55-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="09c55-114">PARAMETERS</span></span>

### <span data-ttu-id="09c55-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="09c55-115">-ApplicationGateway</span></span>
<span data-ttu-id="09c55-116">İsteğin yönlendirme kuralını içeren uygulama ağ geçidi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="09c55-116">Specifies the application gateway object that contains request routing rule.</span></span>

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

### <span data-ttu-id="09c55-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09c55-117">-DefaultProfile</span></span>
<span data-ttu-id="09c55-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="09c55-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09c55-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="09c55-119">-Name</span></span>
<span data-ttu-id="09c55-120">Bu cmdlet 'in aldığı istek yönlendirme kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="09c55-120">Specifies the name of the request routing rule which this cmdlet gets.</span></span>

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

### <span data-ttu-id="09c55-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09c55-121">CommonParameters</span></span>
<span data-ttu-id="09c55-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="09c55-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09c55-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="09c55-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09c55-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="09c55-124">INPUTS</span></span>

### <span data-ttu-id="09c55-125">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="09c55-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="09c55-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="09c55-126">OUTPUTS</span></span>

### <span data-ttu-id="09c55-127">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="09c55-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="09c55-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="09c55-128">NOTES</span></span>

## <span data-ttu-id="09c55-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="09c55-129">RELATED LINKS</span></span>

[<span data-ttu-id="09c55-130">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="09c55-130">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="09c55-131">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="09c55-131">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="09c55-132">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="09c55-132">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="09c55-133">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="09c55-133">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


