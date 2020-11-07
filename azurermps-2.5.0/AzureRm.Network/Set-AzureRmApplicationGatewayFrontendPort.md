---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 85C0A1C3-FC6D-496A-B6B5-8DC2A73B8032
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayfrontendport
schema: 2.0.0
ms.openlocfilehash: 83c29e3c059664d7848fe66bd8ad7bcc005a8d47
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940009"
---
# <span data-ttu-id="6b076-101">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="6b076-101">Set-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="6b076-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b076-102">SYNOPSIS</span></span>
<span data-ttu-id="6b076-103">Uygulama ağ geçidi için ön uç bağlantı noktasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6b076-103">Modifies a front-end port for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b076-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6b076-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b076-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6b076-105">DESCRIPTION</span></span>
<span data-ttu-id="6b076-106">**Set-AzureRmApplicationGatewayFrontendPort** cmdlet 'i uygulama ağ geçidi için ön uç bağlantı noktasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6b076-106">The **Set-AzureRmApplicationGatewayFrontendPort** cmdlet modifies a front-end port for an application gateway.</span></span>

## <span data-ttu-id="6b076-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6b076-107">EXAMPLES</span></span>

### <span data-ttu-id="6b076-108">Örnek 1: uygulama ağ geçidi ön uç bağlantı noktasını 80 olarak ayarlama</span><span class="sxs-lookup"><span data-stu-id="6b076-108">Example 1: Set an application gateway front-end port to 80</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="6b076-109">İlk komut, ApplicationGateway01 adındaki kaynak grubuna ait olan ResourceGroup01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="6b076-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="6b076-110">İkinci komut, FrontEndPort01 adlı ön uç bağlantı noktası için bağlantı noktası 80 'ı kullanmak için $AppGw ağ geçidini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6b076-110">The second command modifies the gateway in $AppGw to use port 80 for the front-end port named FrontEndPort01.</span></span>

## <span data-ttu-id="6b076-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6b076-111">PARAMETERS</span></span>

### <span data-ttu-id="6b076-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6b076-112">-ApplicationGateway</span></span>
<span data-ttu-id="6b076-113">Bu cmdlet 'in ön uç bağlantı noktasını ilişkilendiren uygulama ağ geçidi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b076-113">Specifies the application gateway object with which this cmdlet associates the front-end port.</span></span>

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

### <span data-ttu-id="6b076-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b076-114">-DefaultProfile</span></span>
<span data-ttu-id="6b076-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6b076-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b076-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="6b076-116">-Name</span></span>
<span data-ttu-id="6b076-117">Değiştirilecek ön uç bağlantı noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b076-117">Specifies the name of the front-end port to modify.</span></span>

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

### <span data-ttu-id="6b076-118">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="6b076-118">-Port</span></span>
<span data-ttu-id="6b076-119">Ön uç bağlantı noktası için kullanılacak bağlantı noktası numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b076-119">Specifies the port number to use for the front-end port.</span></span>

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

### <span data-ttu-id="6b076-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b076-120">CommonParameters</span></span>
<span data-ttu-id="6b076-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6b076-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b076-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b076-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b076-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6b076-123">INPUTS</span></span>

### <span data-ttu-id="6b076-124">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6b076-124">PSApplicationGateway</span></span>
<span data-ttu-id="6b076-125">Parametre ' ApplicationGateway ', ardışık düzenin ' PSApplicationGateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="6b076-125">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="6b076-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6b076-126">OUTPUTS</span></span>

### <span data-ttu-id="6b076-127">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6b076-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6b076-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6b076-128">NOTES</span></span>

## <span data-ttu-id="6b076-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6b076-129">RELATED LINKS</span></span>

[<span data-ttu-id="6b076-130">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="6b076-130">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="6b076-131">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="6b076-131">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="6b076-132">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="6b076-132">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="6b076-133">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="6b076-133">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)
