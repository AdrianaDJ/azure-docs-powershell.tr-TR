---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 85C0A1C3-FC6D-496A-B6B5-8DC2A73B8032
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: cdc1535532aad26ad4e3ee67e5fdd822ee3480e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917959"
---
# <span data-ttu-id="8d2d0-101">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="8d2d0-101">Set-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="8d2d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d2d0-102">SYNOPSIS</span></span>
<span data-ttu-id="8d2d0-103">Uygulama ağ geçidi için ön uç bağlantı noktasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="8d2d0-103">Modifies a front-end port for an application gateway.</span></span>

## <span data-ttu-id="8d2d0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8d2d0-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d2d0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8d2d0-105">DESCRIPTION</span></span>
<span data-ttu-id="8d2d0-106">**Set-Azapplicationgatewayfrontenvseçport** cmdlet 'i, uygulama ağ geçidi için ön uç bağlantı noktasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="8d2d0-106">The **Set-AzApplicationGatewayFrontendPort** cmdlet modifies a front-end port for an application gateway.</span></span>

## <span data-ttu-id="8d2d0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8d2d0-107">EXAMPLES</span></span>

### <span data-ttu-id="8d2d0-108">Örnek 1: uygulama ağ geçidi ön uç bağlantı noktasını 80 olarak ayarlama</span><span class="sxs-lookup"><span data-stu-id="8d2d0-108">Example 1: Set an application gateway front-end port to 80</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="8d2d0-109">İlk komut, ApplicationGateway01 adındaki kaynak grubuna ait olan ResourceGroup01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="8d2d0-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="8d2d0-110">İkinci komut, FrontEndPort01 adlı ön uç bağlantı noktası için bağlantı noktası 80 'ı kullanmak için $AppGw ağ geçidini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="8d2d0-110">The second command modifies the gateway in $AppGw to use port 80 for the front-end port named FrontEndPort01.</span></span>

## <span data-ttu-id="8d2d0-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8d2d0-111">PARAMETERS</span></span>

### <span data-ttu-id="8d2d0-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8d2d0-112">-ApplicationGateway</span></span>
<span data-ttu-id="8d2d0-113">Bu cmdlet 'in ön uç bağlantı noktasını ilişkilendiren uygulama ağ geçidi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d2d0-113">Specifies the application gateway object with which this cmdlet associates the front-end port.</span></span>

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

### <span data-ttu-id="8d2d0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d2d0-114">-DefaultProfile</span></span>
<span data-ttu-id="8d2d0-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8d2d0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d2d0-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="8d2d0-116">-Name</span></span>
<span data-ttu-id="8d2d0-117">Değiştirilecek ön uç bağlantı noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d2d0-117">Specifies the name of the front-end port to modify.</span></span>

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

### <span data-ttu-id="8d2d0-118">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="8d2d0-118">-Port</span></span>
<span data-ttu-id="8d2d0-119">Ön uç bağlantı noktası için kullanılacak bağlantı noktası numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8d2d0-119">Specifies the port number to use for the front-end port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d2d0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d2d0-120">CommonParameters</span></span>
<span data-ttu-id="8d2d0-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8d2d0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d2d0-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d2d0-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d2d0-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8d2d0-123">INPUTS</span></span>

### <span data-ttu-id="8d2d0-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8d2d0-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8d2d0-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8d2d0-125">OUTPUTS</span></span>

### <span data-ttu-id="8d2d0-126">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8d2d0-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8d2d0-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8d2d0-127">NOTES</span></span>

## <span data-ttu-id="8d2d0-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8d2d0-128">RELATED LINKS</span></span>

[<span data-ttu-id="8d2d0-129">Add-Azapplicationgatewayfrontenvseçport</span><span class="sxs-lookup"><span data-stu-id="8d2d0-129">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="8d2d0-130">Get-Azapplicationgatewayfrontenvseçport</span><span class="sxs-lookup"><span data-stu-id="8d2d0-130">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="8d2d0-131">Yeni-Azapplicationgatewayfrontenvseçport</span><span class="sxs-lookup"><span data-stu-id="8d2d0-131">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="8d2d0-132">Remove-Azapplicationgatewayfrontenvseçport</span><span class="sxs-lookup"><span data-stu-id="8d2d0-132">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)
