---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40198C86-A4EB-494A-86D5-DF632518EB95
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 9eaaa8ae6ec4be7a1096bfd9de4a3e20c0cb5ff1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760744"
---
# <span data-ttu-id="0e137-101">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="0e137-101">Add-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="0e137-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e137-102">SYNOPSIS</span></span>
<span data-ttu-id="0e137-103">Uygulama ağ geçidine ön uç bağlantı noktası ekler.</span><span class="sxs-lookup"><span data-stu-id="0e137-103">Adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="0e137-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0e137-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e137-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0e137-105">DESCRIPTION</span></span>
<span data-ttu-id="0e137-106">**Add-Azapplicationgatewayfrontenvseçport** cmdlet 'i uygulama ağ geçidine ön uç bağlantı noktası ekler.</span><span class="sxs-lookup"><span data-stu-id="0e137-106">The **Add-AzApplicationGatewayFrontendPort** cmdlet adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="0e137-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0e137-107">EXAMPLES</span></span>

### <span data-ttu-id="0e137-108">Örnek 1: uygulama ağ geçidine ön uç bağlantı noktası ekleme</span><span class="sxs-lookup"><span data-stu-id="0e137-108">Example 1: Add a front-end port to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="0e137-109">İlk komut, ApplicationGateway01 adındaki kaynak grubuna ait olan ResourceGroup01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="0e137-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="0e137-110">İkinci komut $AppGw 'da depolanan uygulama ağ geçidi için ön uç bağlantı noktası olarak 80 bağlantı noktası ekler ve bağlantı noktası FrontEndPort01.</span><span class="sxs-lookup"><span data-stu-id="0e137-110">The second command adds port 80 as a front-end port for the application gateway stored in $AppGw and names the port FrontEndPort01.</span></span>

## <span data-ttu-id="0e137-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0e137-111">PARAMETERS</span></span>

### <span data-ttu-id="0e137-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0e137-112">-ApplicationGateway</span></span>
<span data-ttu-id="0e137-113">Bu cmdlet 'in ön uç bağlantı noktası eklediği uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e137-113">Specifies the application gateway to which this cmdlet adds a front-end port.</span></span>

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

### <span data-ttu-id="0e137-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e137-114">-DefaultProfile</span></span>
<span data-ttu-id="0e137-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0e137-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e137-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="0e137-116">-Name</span></span>
<span data-ttu-id="0e137-117">Ön uç bağlantı noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e137-117">Specifies the name of the front-end port.</span></span>

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

### <span data-ttu-id="0e137-118">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="0e137-118">-Port</span></span>
<span data-ttu-id="0e137-119">Bağlantı noktası numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e137-119">Specifies the port number.</span></span>

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

### <span data-ttu-id="0e137-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e137-120">CommonParameters</span></span>
<span data-ttu-id="0e137-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0e137-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e137-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e137-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e137-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0e137-123">INPUTS</span></span>

### <span data-ttu-id="0e137-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0e137-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0e137-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0e137-125">OUTPUTS</span></span>

### <span data-ttu-id="0e137-126">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0e137-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0e137-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0e137-127">NOTES</span></span>

## <span data-ttu-id="0e137-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0e137-128">RELATED LINKS</span></span>

[<span data-ttu-id="0e137-129">Get-Azapplicationgatewayfrontenvseçport</span><span class="sxs-lookup"><span data-stu-id="0e137-129">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="0e137-130">Yeni-Azapplicationgatewayfrontenvseçport</span><span class="sxs-lookup"><span data-stu-id="0e137-130">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="0e137-131">Remove-Azapplicationgatewayfrontenvseçport</span><span class="sxs-lookup"><span data-stu-id="0e137-131">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="0e137-132">Set-Azapplicationgatewayfrontenvseçport</span><span class="sxs-lookup"><span data-stu-id="0e137-132">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


