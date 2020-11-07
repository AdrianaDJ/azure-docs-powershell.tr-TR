---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 40198C86-A4EB-494A-86D5-DF632518EB95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: c9be5f69fc210f68ceb90cfe2e21f5afab164b6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592468"
---
# <span data-ttu-id="861a4-101">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="861a4-101">Add-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="861a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="861a4-102">SYNOPSIS</span></span>
<span data-ttu-id="861a4-103">Uygulama ağ geçidine ön uç bağlantı noktası ekler.</span><span class="sxs-lookup"><span data-stu-id="861a4-103">Adds a front-end port to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="861a4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="861a4-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="861a4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="861a4-105">DESCRIPTION</span></span>
<span data-ttu-id="861a4-106">**Add-AzureRmApplicationGatewayFrontendPort** cmdlet 'i uygulama ağ geçidine ön uç bağlantı noktası ekler.</span><span class="sxs-lookup"><span data-stu-id="861a4-106">The **Add-AzureRmApplicationGatewayFrontendPort** cmdlet adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="861a4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="861a4-107">EXAMPLES</span></span>

### <span data-ttu-id="861a4-108">Örnek 1: uygulama ağ geçidine ön uç bağlantı noktası ekleme</span><span class="sxs-lookup"><span data-stu-id="861a4-108">Example 1: Add a front-end port to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $ AppGw = Add-AzureRmApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="861a4-109">İlk komut, ApplicationGateway01 adındaki kaynak grubuna ait olan ResourceGroup01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="861a4-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="861a4-110">İkinci komut $AppGw 'da depolanan uygulama ağ geçidi için ön uç bağlantı noktası olarak 80 bağlantı noktası ekler ve bağlantı noktası FrontEndPort01.</span><span class="sxs-lookup"><span data-stu-id="861a4-110">The second command adds port 80 as a front-end port for the application gateway stored in $AppGw and names the port FrontEndPort01.</span></span>

## <span data-ttu-id="861a4-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="861a4-111">PARAMETERS</span></span>

### <span data-ttu-id="861a4-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="861a4-112">-ApplicationGateway</span></span>
<span data-ttu-id="861a4-113">Bu cmdlet 'in ön uç bağlantı noktası eklediği uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="861a4-113">Specifies the application gateway to which this cmdlet adds a front-end port.</span></span>

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

### <span data-ttu-id="861a4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="861a4-114">-DefaultProfile</span></span>
<span data-ttu-id="861a4-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="861a4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="861a4-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="861a4-116">-Name</span></span>
<span data-ttu-id="861a4-117">Ön uç bağlantı noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="861a4-117">Specifies the name of the front-end port.</span></span>

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

### <span data-ttu-id="861a4-118">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="861a4-118">-Port</span></span>
<span data-ttu-id="861a4-119">Bağlantı noktası numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="861a4-119">Specifies the port number.</span></span>

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

### <span data-ttu-id="861a4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="861a4-120">CommonParameters</span></span>
<span data-ttu-id="861a4-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="861a4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="861a4-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="861a4-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="861a4-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="861a4-123">INPUTS</span></span>

### <span data-ttu-id="861a4-124">System. String</span><span class="sxs-lookup"><span data-stu-id="861a4-124">System.String</span></span>

## <span data-ttu-id="861a4-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="861a4-125">OUTPUTS</span></span>

### <span data-ttu-id="861a4-126">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="861a4-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="861a4-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="861a4-127">NOTES</span></span>

## <span data-ttu-id="861a4-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="861a4-128">RELATED LINKS</span></span>

[<span data-ttu-id="861a4-129">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="861a4-129">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="861a4-130">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="861a4-130">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="861a4-131">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="861a4-131">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="861a4-132">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="861a4-132">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)

