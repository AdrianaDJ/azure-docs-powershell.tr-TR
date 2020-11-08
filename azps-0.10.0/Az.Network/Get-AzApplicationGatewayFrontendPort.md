---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4518D2A9-7DE7-4617-86E0-7778B8CFE48C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: be1e70538aae66b05bdff5b06859cfb2f30681ea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935588"
---
# <span data-ttu-id="5c22a-101">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5c22a-101">Get-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="5c22a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c22a-102">SYNOPSIS</span></span>
<span data-ttu-id="5c22a-103">Uygulama ağ geçidinin ön uç bağlantı noktasını alır.</span><span class="sxs-lookup"><span data-stu-id="5c22a-103">Gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="5c22a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5c22a-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendPort [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c22a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5c22a-105">DESCRIPTION</span></span>
<span data-ttu-id="5c22a-106">**Get-Azapplicationgatewayfrontenvseçport** cmdlet 'i, uygulama ağ geçidinin ön uç bağlantı noktasını alır.</span><span class="sxs-lookup"><span data-stu-id="5c22a-106">The **Get-AzApplicationGatewayFrontendPort** cmdlet gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="5c22a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5c22a-107">EXAMPLES</span></span>

### <span data-ttu-id="5c22a-108">Örnek 1: belirtilen ön uç bağlantı noktasını alma</span><span class="sxs-lookup"><span data-stu-id="5c22a-108">Example 1: Get a specified front-end port</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPort = Get-AzApplicationGatewayFrontendIPort -Name "FrontEndPort01" -ApplicationGateway $AppGw
```

<span data-ttu-id="5c22a-109">İlk komut, ResourceGroup01 adındaki kaynak grubundan ApplicationGateway01 adlı bir uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="5c22a-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="5c22a-110">İkinci komut, $AppGw FrontEndPort01 adındaki ön uç bağlantı noktasını alır ve $FrontEndPort değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="5c22a-110">The second command gets the front-end port named FrontEndPort01 from $AppGw and stores it in the $FrontEndPort variable.</span></span>

### <span data-ttu-id="5c22a-111">Örnek 2: ön uç bağlantı noktalarının listesini alma</span><span class="sxs-lookup"><span data-stu-id="5c22a-111">Example 2: Get a list of front-end ports</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPorts = Get-AzApplicationGatewayFrontendIPort  -ApplicationGateway $AppGw
```

<span data-ttu-id="5c22a-112">İlk komut, ResourceGroup01 adındaki kaynak grubundan ApplicationGateway01 adlı bir uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="5c22a-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="5c22a-113">İkinci komut $AppGw 'dan ön uç bağlantı noktalarının bir listesini alır ve $FrontEndPorts değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="5c22a-113">The second command gets a list of the front-end ports from $AppGw and stores it in the $FrontEndPorts variable.</span></span>

## <span data-ttu-id="5c22a-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5c22a-114">PARAMETERS</span></span>

### <span data-ttu-id="5c22a-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5c22a-115">-ApplicationGateway</span></span>
<span data-ttu-id="5c22a-116">Ön uç bağlantı noktasını içeren uygulama ağ geçidi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c22a-116">Specifies the application gateway object that contains the front-end port.</span></span>

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

### <span data-ttu-id="5c22a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c22a-117">-DefaultProfile</span></span>
<span data-ttu-id="5c22a-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5c22a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c22a-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="5c22a-119">-Name</span></span>
<span data-ttu-id="5c22a-120">Alınacak ön uç bağlantı noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c22a-120">Specifies the name of the front-end port to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c22a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c22a-121">CommonParameters</span></span>
<span data-ttu-id="5c22a-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5c22a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c22a-123">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c22a-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c22a-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5c22a-124">INPUTS</span></span>

### <span data-ttu-id="5c22a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="5c22a-125">System.String</span></span>

## <span data-ttu-id="5c22a-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5c22a-126">OUTPUTS</span></span>

### <span data-ttu-id="5c22a-127">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5c22a-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="5c22a-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5c22a-128">NOTES</span></span>

## <span data-ttu-id="5c22a-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5c22a-129">RELATED LINKS</span></span>

[<span data-ttu-id="5c22a-130">Add-Azapplicationgatewayfrontenvseçport</span><span class="sxs-lookup"><span data-stu-id="5c22a-130">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="5c22a-131">Yeni-Azapplicationgatewayfrontenvseçport</span><span class="sxs-lookup"><span data-stu-id="5c22a-131">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="5c22a-132">Remove-Azapplicationgatewayfrontenvseçport</span><span class="sxs-lookup"><span data-stu-id="5c22a-132">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="5c22a-133">Set-Azapplicationgatewayfrontenvseçport</span><span class="sxs-lookup"><span data-stu-id="5c22a-133">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)

