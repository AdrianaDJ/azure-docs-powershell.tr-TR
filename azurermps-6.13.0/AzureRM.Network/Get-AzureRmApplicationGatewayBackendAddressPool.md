---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4B2066B6-51D7-46D8-8A72-1A232B3E6589
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 05e71fc334ae45f8a74a4afbeaa33be5816b6532
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593215"
---
# <span data-ttu-id="f11f0-101">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f11f0-101">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="f11f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f11f0-102">SYNOPSIS</span></span>
<span data-ttu-id="f11f0-103">Uygulama ağ geçidi için bir arka uç adres havuzu alır.</span><span class="sxs-lookup"><span data-stu-id="f11f0-103">Gets a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f11f0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f11f0-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayBackendAddressPool [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f11f0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f11f0-105">DESCRIPTION</span></span>

## <span data-ttu-id="f11f0-106">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f11f0-106">EXAMPLES</span></span>

### <span data-ttu-id="f11f0-107">Örnek 1: belirtilen arka uç sunucu havuzunu alma</span><span class="sxs-lookup"><span data-stu-id="f11f0-107">Example 1: Get a specified back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPool = Get-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -ApplicationGateway $AppGw
```

<span data-ttu-id="f11f0-108">İlk komut, ResourceGroup01 adındaki kaynak grubundaki ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f11f0-108">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f11f0-109">İkinci komut, Pool01 adlı $AppGw ilişkili arka uç adres havuzunu alır ve $BackendPool değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f11f0-109">The second command gets the back-end address pool associated with $AppGw named Pool01 and stores it in the $BackendPool variable.</span></span>

### <span data-ttu-id="f11f0-110">Örnek 2: arka uç sunucu havuzunun listesini alma</span><span class="sxs-lookup"><span data-stu-id="f11f0-110">Example 2: Get a list of back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPools = Get-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw
```

<span data-ttu-id="f11f0-111">İlk komut, ResourceGroup01 adındaki kaynak grubundaki ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f11f0-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f11f0-112">İkinci komut $AppGw ilişkili arka uç adresi havuzlarının bir listesini alır ve listeyi $BackendPools değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f11f0-112">The second command gets a list of the back-end address pools associated with $AppGw, and stores the list in the $BackendPools variable.</span></span>

## <span data-ttu-id="f11f0-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f11f0-113">PARAMETERS</span></span>

### <span data-ttu-id="f11f0-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f11f0-114">-ApplicationGateway</span></span>
<span data-ttu-id="f11f0-115">**Get-AzureRmApplicationGatewayBackendAddressPool** cmdlet 'i bir uygulama ağ geçidi için arka uç adres havuzu alır.</span><span class="sxs-lookup"><span data-stu-id="f11f0-115">The **Get-AzureRmApplicationGatewayBackendAddressPool** cmdlet gets a back-end address pool for an application gateway.</span></span>

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

### <span data-ttu-id="f11f0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f11f0-116">-DefaultProfile</span></span>
<span data-ttu-id="f11f0-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f11f0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f11f0-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="f11f0-118">-Name</span></span>
<span data-ttu-id="f11f0-119">Bu cmdlet 'in aldığı arka uç adres havuzunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f11f0-119">Specifies the name of the back-end address pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f11f0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f11f0-120">CommonParameters</span></span>
<span data-ttu-id="f11f0-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f11f0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f11f0-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f11f0-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f11f0-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f11f0-123">INPUTS</span></span>

### <span data-ttu-id="f11f0-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f11f0-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="f11f0-125">Parametreler: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f11f0-125">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="f11f0-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f11f0-126">OUTPUTS</span></span>

### <span data-ttu-id="f11f0-127">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f11f0-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="f11f0-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f11f0-128">NOTES</span></span>

## <span data-ttu-id="f11f0-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f11f0-129">RELATED LINKS</span></span>

[<span data-ttu-id="f11f0-130">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f11f0-130">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="f11f0-131">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f11f0-131">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="f11f0-132">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f11f0-132">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="f11f0-133">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f11f0-133">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)

