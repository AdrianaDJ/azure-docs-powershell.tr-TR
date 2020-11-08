---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4B2066B6-51D7-46D8-8A72-1A232B3E6589
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: b10863cf5e4af09ded0e98dbed76aff37dc48677
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935601"
---
# <span data-ttu-id="879ea-101">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="879ea-101">Get-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="879ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="879ea-102">SYNOPSIS</span></span>
<span data-ttu-id="879ea-103">Uygulama ağ geçidi için bir arka uç adres havuzu alır.</span><span class="sxs-lookup"><span data-stu-id="879ea-103">Gets a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="879ea-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="879ea-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendAddressPool [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="879ea-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="879ea-105">DESCRIPTION</span></span>

## <span data-ttu-id="879ea-106">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="879ea-106">EXAMPLES</span></span>

### <span data-ttu-id="879ea-107">Örnek 1: belirtilen arka uç sunucu havuzunu alma</span><span class="sxs-lookup"><span data-stu-id="879ea-107">Example 1: Get a specified back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPool = Get-AzApplicationGatewayBackendAddressPool -Name "Pool01" -ApplicationGateway $AppGw
```

<span data-ttu-id="879ea-108">İlk komut, ResourceGroup01 adındaki kaynak grubundaki ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="879ea-108">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="879ea-109">İkinci komut, Pool01 adlı $AppGw ilişkili arka uç adres havuzunu alır ve $BackendPool değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="879ea-109">The second command gets the back-end address pool associated with $AppGw named Pool01 and stores it in the $BackendPool variable.</span></span>

### <span data-ttu-id="879ea-110">Örnek 2: arka uç sunucu havuzunun listesini alma</span><span class="sxs-lookup"><span data-stu-id="879ea-110">Example 2: Get a list of back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPools = Get-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw
```

<span data-ttu-id="879ea-111">İlk komut, ResourceGroup01 adındaki kaynak grubundaki ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="879ea-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="879ea-112">İkinci komut $AppGw ilişkili arka uç adresi havuzlarının bir listesini alır ve listeyi $BackendPools değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="879ea-112">The second command gets a list of the back-end address pools associated with $AppGw, and stores the list in the $BackendPools variable.</span></span>

## <span data-ttu-id="879ea-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="879ea-113">PARAMETERS</span></span>

### <span data-ttu-id="879ea-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="879ea-114">-ApplicationGateway</span></span>
<span data-ttu-id="879ea-115">**Get-AzApplicationGatewayBackendAddressPool** cmdlet 'i bir uygulama ağ geçidi için arka uç adres havuzunu alır.</span><span class="sxs-lookup"><span data-stu-id="879ea-115">The **Get-AzApplicationGatewayBackendAddressPool** cmdlet gets a back-end address pool for an application gateway.</span></span>

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

### <span data-ttu-id="879ea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="879ea-116">-DefaultProfile</span></span>
<span data-ttu-id="879ea-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="879ea-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="879ea-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="879ea-118">-Name</span></span>
<span data-ttu-id="879ea-119">Bu cmdlet 'in aldığı arka uç adres havuzunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="879ea-119">Specifies the name of the back-end address pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="879ea-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="879ea-120">CommonParameters</span></span>
<span data-ttu-id="879ea-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="879ea-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="879ea-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="879ea-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="879ea-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="879ea-123">INPUTS</span></span>

### <span data-ttu-id="879ea-124">System. String</span><span class="sxs-lookup"><span data-stu-id="879ea-124">System.String</span></span>

## <span data-ttu-id="879ea-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="879ea-125">OUTPUTS</span></span>

### <span data-ttu-id="879ea-126">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="879ea-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="879ea-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="879ea-127">NOTES</span></span>

## <span data-ttu-id="879ea-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="879ea-128">RELATED LINKS</span></span>

[<span data-ttu-id="879ea-129">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="879ea-129">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="879ea-130">Yeni-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="879ea-130">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="879ea-131">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="879ea-131">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="879ea-132">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="879ea-132">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)

