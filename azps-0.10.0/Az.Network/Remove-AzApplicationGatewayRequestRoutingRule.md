---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CC033DA8-FACC-44E2-82F9-E30FADBF8926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 3c034f3bbbd5edc77fb6f43c291b8bf7ca27cd38
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935319"
---
# <span data-ttu-id="81550-101">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="81550-101">Remove-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="81550-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81550-102">SYNOPSIS</span></span>
<span data-ttu-id="81550-103">Uygulama ağ geçidinden istek yönlendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="81550-103">Removes a request routing rule from an application gateway.</span></span>

## <span data-ttu-id="81550-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="81550-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRequestRoutingRule -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81550-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="81550-105">DESCRIPTION</span></span>
<span data-ttu-id="81550-106">**Remove-AzApplicationGatewayRequestRoutingRule** cmdlet 'ı bir Azure uygulama ağ geçidinden istek yönlendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="81550-106">The **Remove-AzApplicationGatewayRequestRoutingRule** cmdlet removes a request routing rule from an Azure application gateway.</span></span>

## <span data-ttu-id="81550-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="81550-107">EXAMPLES</span></span>

### <span data-ttu-id="81550-108">Örnek 1: uygulama ağ geçidinden istek yönlendirme kuralını kaldırma</span><span class="sxs-lookup"><span data-stu-id="81550-108">Example 1: Remove a request routing rule from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule02"
```

<span data-ttu-id="81550-109">İlk komut bir uygulama ağ geçidi alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="81550-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="81550-110">İkinci komut, $AppGw depolanan uygulama ağ geçidinden Rule02 adındaki istek yönlendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="81550-110">The second command removes the request routing rule named Rule02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="81550-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="81550-111">PARAMETERS</span></span>

### <span data-ttu-id="81550-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="81550-112">-ApplicationGateway</span></span>
<span data-ttu-id="81550-113">İstek yönlendirme kuralının kaldırılacağı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="81550-113">Specifies the application gateway from which to remove a request routing rule.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81550-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81550-114">-DefaultProfile</span></span>
<span data-ttu-id="81550-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="81550-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81550-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="81550-116">-Name</span></span>
<span data-ttu-id="81550-117">Bu cmdlet 'in kaldırıldığı istek yönlendirme kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="81550-117">Specifies the name of the request routing rule for which this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81550-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81550-118">CommonParameters</span></span>
<span data-ttu-id="81550-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="81550-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81550-120">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81550-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81550-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="81550-121">INPUTS</span></span>

### <span data-ttu-id="81550-122">System. String</span><span class="sxs-lookup"><span data-stu-id="81550-122">System.String</span></span>

## <span data-ttu-id="81550-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="81550-123">OUTPUTS</span></span>

### <span data-ttu-id="81550-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="81550-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="81550-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="81550-125">NOTES</span></span>

## <span data-ttu-id="81550-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="81550-126">RELATED LINKS</span></span>

[<span data-ttu-id="81550-127">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="81550-127">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="81550-128">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="81550-128">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="81550-129">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="81550-129">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="81550-130">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="81550-130">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


