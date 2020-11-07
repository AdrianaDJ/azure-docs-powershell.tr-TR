---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4518D2A9-7DE7-4617-86E0-7778B8CFE48C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: 1f347545fd5bf53eeb5b083410c919ce1c602553
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763020"
---
# <span data-ttu-id="c3a70-101">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c3a70-101">Get-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="c3a70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3a70-102">SYNOPSIS</span></span>
<span data-ttu-id="c3a70-103">Uygulama ağ geçidinin ön uç bağlantı noktasını alır.</span><span class="sxs-lookup"><span data-stu-id="c3a70-103">Gets the front-end port of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3a70-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c3a70-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayFrontendPort [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3a70-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c3a70-105">DESCRIPTION</span></span>
<span data-ttu-id="c3a70-106">**Get-AzureRmApplicationGatewayFrontendPort** cmdlet 'i uygulama ağ geçidinin ön uç bağlantı noktasını alır.</span><span class="sxs-lookup"><span data-stu-id="c3a70-106">The **Get-AzureRmApplicationGatewayFrontendPort** cmdlet gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="c3a70-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c3a70-107">EXAMPLES</span></span>

### <span data-ttu-id="c3a70-108">Örnek 1: belirtilen ön uç bağlantı noktasını alma</span><span class="sxs-lookup"><span data-stu-id="c3a70-108">Example 1: Get a specified front-end port</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPort = Get-AzureRmApplicationGatewayFrontendIPort -Name "FrontEndPort01" -ApplicationGateway $AppGw
```

<span data-ttu-id="c3a70-109">İlk komut, ResourceGroup01 adındaki kaynak grubundan ApplicationGateway01 adlı bir uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c3a70-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c3a70-110">İkinci komut, $AppGw FrontEndPort01 adındaki ön uç bağlantı noktasını alır ve $FrontEndPort değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c3a70-110">The second command gets the front-end port named FrontEndPort01 from $AppGw and stores it in the $FrontEndPort variable.</span></span>

### <span data-ttu-id="c3a70-111">Örnek 2: ön uç bağlantı noktalarının listesini alma</span><span class="sxs-lookup"><span data-stu-id="c3a70-111">Example 2: Get a list of front-end ports</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPorts = Get-AzureRmApplicationGatewayFrontendIPort  -ApplicationGateway $AppGw
```

<span data-ttu-id="c3a70-112">İlk komut, ResourceGroup01 adındaki kaynak grubundan ApplicationGateway01 adlı bir uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c3a70-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c3a70-113">İkinci komut $AppGw 'dan ön uç bağlantı noktalarının bir listesini alır ve $FrontEndPorts değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c3a70-113">The second command gets a list of the front-end ports from $AppGw and stores it in the $FrontEndPorts variable.</span></span>

## <span data-ttu-id="c3a70-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c3a70-114">PARAMETERS</span></span>

### <span data-ttu-id="c3a70-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c3a70-115">-ApplicationGateway</span></span>
<span data-ttu-id="c3a70-116">Ön uç bağlantı noktasını içeren uygulama ağ geçidi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c3a70-116">Specifies the application gateway object that contains the front-end port.</span></span>

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

### <span data-ttu-id="c3a70-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3a70-117">-DefaultProfile</span></span>
<span data-ttu-id="c3a70-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c3a70-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3a70-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="c3a70-119">-Name</span></span>
<span data-ttu-id="c3a70-120">Alınacak ön uç bağlantı noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c3a70-120">Specifies the name of the front-end port to get.</span></span>

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

### <span data-ttu-id="c3a70-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3a70-121">CommonParameters</span></span>
<span data-ttu-id="c3a70-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c3a70-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3a70-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3a70-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3a70-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c3a70-124">INPUTS</span></span>

### <span data-ttu-id="c3a70-125">System. String</span><span class="sxs-lookup"><span data-stu-id="c3a70-125">System.String</span></span>

## <span data-ttu-id="c3a70-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c3a70-126">OUTPUTS</span></span>

### <span data-ttu-id="c3a70-127">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c3a70-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="c3a70-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c3a70-128">NOTES</span></span>

## <span data-ttu-id="c3a70-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c3a70-129">RELATED LINKS</span></span>

[<span data-ttu-id="c3a70-130">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c3a70-130">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="c3a70-131">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c3a70-131">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="c3a70-132">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c3a70-132">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="c3a70-133">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c3a70-133">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)


