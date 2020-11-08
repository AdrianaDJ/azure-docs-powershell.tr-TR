---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4518D2A9-7DE7-4617-86E0-7778B8CFE48C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 404a9ff22f6b6af480e167c5a4f958b9ac4b5d52
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280003"
---
# <span data-ttu-id="09e70-101">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="09e70-101">Get-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="09e70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09e70-102">SYNOPSIS</span></span>
<span data-ttu-id="09e70-103">Uygulama ağ geçidinin ön uç bağlantı noktasını alır.</span><span class="sxs-lookup"><span data-stu-id="09e70-103">Gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="09e70-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="09e70-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendPort [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09e70-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="09e70-105">DESCRIPTION</span></span>
<span data-ttu-id="09e70-106">**Get-Azapplicationgatewayfrontenvseçport** cmdlet 'i, uygulama ağ geçidinin ön uç bağlantı noktasını alır.</span><span class="sxs-lookup"><span data-stu-id="09e70-106">The **Get-AzApplicationGatewayFrontendPort** cmdlet gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="09e70-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="09e70-107">EXAMPLES</span></span>

### <span data-ttu-id="09e70-108">Örnek 1: belirtilen ön uç bağlantı noktasını alma</span><span class="sxs-lookup"><span data-stu-id="09e70-108">Example 1: Get a specified front-end port</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPort = Get-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -ApplicationGateway $AppGw
```

<span data-ttu-id="09e70-109">İlk komut, ResourceGroup01 adındaki kaynak grubundan ApplicationGateway01 adlı bir uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="09e70-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="09e70-110">İkinci komut, $AppGw FrontEndPort01 adındaki ön uç bağlantı noktasını alır ve $FrontEndPort değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="09e70-110">The second command gets the front-end port named FrontEndPort01 from $AppGw and stores it in the $FrontEndPort variable.</span></span>

### <span data-ttu-id="09e70-111">Örnek 2: ön uç bağlantı noktalarının listesini alma</span><span class="sxs-lookup"><span data-stu-id="09e70-111">Example 2: Get a list of front-end ports</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPorts = Get-AzApplicationGatewayFrontendPort  -ApplicationGateway $AppGw
```

<span data-ttu-id="09e70-112">İlk komut, ResourceGroup01 adındaki kaynak grubundan ApplicationGateway01 adlı bir uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="09e70-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="09e70-113">İkinci komut $AppGw 'dan ön uç bağlantı noktalarının bir listesini alır ve $FrontEndPorts değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="09e70-113">The second command gets a list of the front-end ports from $AppGw and stores it in the $FrontEndPorts variable.</span></span>

## <span data-ttu-id="09e70-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="09e70-114">PARAMETERS</span></span>

### <span data-ttu-id="09e70-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="09e70-115">-ApplicationGateway</span></span>
<span data-ttu-id="09e70-116">Ön uç bağlantı noktasını içeren uygulama ağ geçidi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="09e70-116">Specifies the application gateway object that contains the front-end port.</span></span>

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

### <span data-ttu-id="09e70-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09e70-117">-DefaultProfile</span></span>
<span data-ttu-id="09e70-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="09e70-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09e70-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="09e70-119">-Name</span></span>
<span data-ttu-id="09e70-120">Alınacak ön uç bağlantı noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="09e70-120">Specifies the name of the front-end port to get.</span></span>

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

### <span data-ttu-id="09e70-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09e70-121">CommonParameters</span></span>
<span data-ttu-id="09e70-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="09e70-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09e70-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="09e70-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09e70-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="09e70-124">INPUTS</span></span>

### <span data-ttu-id="09e70-125">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="09e70-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="09e70-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="09e70-126">OUTPUTS</span></span>

### <span data-ttu-id="09e70-127">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="09e70-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="09e70-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="09e70-128">NOTES</span></span>

## <span data-ttu-id="09e70-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="09e70-129">RELATED LINKS</span></span>

[<span data-ttu-id="09e70-130">Add-Azapplicationgatewayfrontenvseçport</span><span class="sxs-lookup"><span data-stu-id="09e70-130">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="09e70-131">Yeni-Azapplicationgatewayfrontenvseçport</span><span class="sxs-lookup"><span data-stu-id="09e70-131">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="09e70-132">Remove-Azapplicationgatewayfrontenvseçport</span><span class="sxs-lookup"><span data-stu-id="09e70-132">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="09e70-133">Set-Azapplicationgatewayfrontenvseçport</span><span class="sxs-lookup"><span data-stu-id="09e70-133">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


