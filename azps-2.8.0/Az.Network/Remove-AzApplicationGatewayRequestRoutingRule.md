---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CC033DA8-FACC-44E2-82F9-E30FADBF8926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: bd99eac2ecd36039685dde53730f250754318bc7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932307"
---
# <span data-ttu-id="8da10-101">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8da10-101">Remove-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="8da10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8da10-102">SYNOPSIS</span></span>
<span data-ttu-id="8da10-103">Uygulama ağ geçidinden istek yönlendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8da10-103">Removes a request routing rule from an application gateway.</span></span>

## <span data-ttu-id="8da10-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8da10-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRequestRoutingRule -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8da10-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8da10-105">DESCRIPTION</span></span>
<span data-ttu-id="8da10-106">**Remove-AzApplicationGatewayRequestRoutingRule** cmdlet 'ı bir Azure uygulama ağ geçidinden istek yönlendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8da10-106">The **Remove-AzApplicationGatewayRequestRoutingRule** cmdlet removes a request routing rule from an Azure application gateway.</span></span>

## <span data-ttu-id="8da10-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8da10-107">EXAMPLES</span></span>

### <span data-ttu-id="8da10-108">Örnek 1: uygulama ağ geçidinden istek yönlendirme kuralını kaldırma</span><span class="sxs-lookup"><span data-stu-id="8da10-108">Example 1: Remove a request routing rule from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule02"
```

<span data-ttu-id="8da10-109">İlk komut bir uygulama ağ geçidi alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="8da10-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="8da10-110">İkinci komut, $AppGw depolanan uygulama ağ geçidinden Rule02 adındaki istek yönlendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8da10-110">The second command removes the request routing rule named Rule02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="8da10-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8da10-111">PARAMETERS</span></span>

### <span data-ttu-id="8da10-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8da10-112">-ApplicationGateway</span></span>
<span data-ttu-id="8da10-113">İstek yönlendirme kuralının kaldırılacağı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8da10-113">Specifies the application gateway from which to remove a request routing rule.</span></span>

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

### <span data-ttu-id="8da10-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8da10-114">-DefaultProfile</span></span>
<span data-ttu-id="8da10-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8da10-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8da10-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="8da10-116">-Name</span></span>
<span data-ttu-id="8da10-117">Bu cmdlet 'in kaldırıldığı istek yönlendirme kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8da10-117">Specifies the name of the request routing rule for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="8da10-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8da10-118">CommonParameters</span></span>
<span data-ttu-id="8da10-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8da10-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8da10-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8da10-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8da10-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8da10-121">INPUTS</span></span>

### <span data-ttu-id="8da10-122">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8da10-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8da10-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8da10-123">OUTPUTS</span></span>

### <span data-ttu-id="8da10-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8da10-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="8da10-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8da10-125">NOTES</span></span>

## <span data-ttu-id="8da10-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8da10-126">RELATED LINKS</span></span>

[<span data-ttu-id="8da10-127">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8da10-127">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="8da10-128">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8da10-128">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="8da10-129">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8da10-129">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="8da10-130">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="8da10-130">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


