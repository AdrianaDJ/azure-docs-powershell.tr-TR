---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40198C86-A4EB-494A-86D5-DF632518EB95
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: e0ca615d856e7905127c488c17c039b23051cc0a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935662"
---
# <span data-ttu-id="9c635-101">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="9c635-101">Add-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="9c635-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c635-102">SYNOPSIS</span></span>
<span data-ttu-id="9c635-103">Uygulama ağ geçidine ön uç bağlantı noktası ekler.</span><span class="sxs-lookup"><span data-stu-id="9c635-103">Adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="9c635-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9c635-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c635-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9c635-105">DESCRIPTION</span></span>
<span data-ttu-id="9c635-106">**Add-Azapplicationgatewayfrontenvseçport** cmdlet 'i uygulama ağ geçidine ön uç bağlantı noktası ekler.</span><span class="sxs-lookup"><span data-stu-id="9c635-106">The **Add-AzApplicationGatewayFrontendPort** cmdlet adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="9c635-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9c635-107">EXAMPLES</span></span>

### <span data-ttu-id="9c635-108">Örnek 1: uygulama ağ geçidine ön uç bağlantı noktası ekleme</span><span class="sxs-lookup"><span data-stu-id="9c635-108">Example 1: Add a front-end port to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $ AppGw = Add-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="9c635-109">İlk komut, ApplicationGateway01 adındaki kaynak grubuna ait olan ResourceGroup01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="9c635-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="9c635-110">İkinci komut $AppGw 'da depolanan uygulama ağ geçidi için ön uç bağlantı noktası olarak 80 bağlantı noktası ekler ve bağlantı noktası FrontEndPort01.</span><span class="sxs-lookup"><span data-stu-id="9c635-110">The second command adds port 80 as a front-end port for the application gateway stored in $AppGw and names the port FrontEndPort01.</span></span>

## <span data-ttu-id="9c635-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9c635-111">PARAMETERS</span></span>

### <span data-ttu-id="9c635-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9c635-112">-ApplicationGateway</span></span>
<span data-ttu-id="9c635-113">Bu cmdlet 'in ön uç bağlantı noktası eklediği uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c635-113">Specifies the application gateway to which this cmdlet adds a front-end port.</span></span>

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

### <span data-ttu-id="9c635-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c635-114">-DefaultProfile</span></span>
<span data-ttu-id="9c635-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9c635-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c635-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="9c635-116">-Name</span></span>
<span data-ttu-id="9c635-117">Ön uç bağlantı noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c635-117">Specifies the name of the front-end port.</span></span>

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

### <span data-ttu-id="9c635-118">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="9c635-118">-Port</span></span>
<span data-ttu-id="9c635-119">Bağlantı noktası numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c635-119">Specifies the port number.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c635-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c635-120">CommonParameters</span></span>
<span data-ttu-id="9c635-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9c635-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c635-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c635-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c635-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9c635-123">INPUTS</span></span>

### <span data-ttu-id="9c635-124">System. String</span><span class="sxs-lookup"><span data-stu-id="9c635-124">System.String</span></span>

## <span data-ttu-id="9c635-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9c635-125">OUTPUTS</span></span>

### <span data-ttu-id="9c635-126">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9c635-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9c635-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9c635-127">NOTES</span></span>

## <span data-ttu-id="9c635-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9c635-128">RELATED LINKS</span></span>

[<span data-ttu-id="9c635-129">Get-Azapplicationgatewayfrontenvseçport</span><span class="sxs-lookup"><span data-stu-id="9c635-129">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="9c635-130">Yeni-Azapplicationgatewayfrontenvseçport</span><span class="sxs-lookup"><span data-stu-id="9c635-130">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="9c635-131">Remove-Azapplicationgatewayfrontenvseçport</span><span class="sxs-lookup"><span data-stu-id="9c635-131">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="9c635-132">Set-Azapplicationgatewayfrontenvseçport</span><span class="sxs-lookup"><span data-stu-id="9c635-132">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


