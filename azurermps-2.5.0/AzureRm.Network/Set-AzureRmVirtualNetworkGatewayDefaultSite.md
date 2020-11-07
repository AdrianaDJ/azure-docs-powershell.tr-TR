---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewaydefaultsite
schema: 2.0.0
ms.openlocfilehash: 463951ca6b6679671f330a3ddb0f9460a878a3d3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939686"
---
# <span data-ttu-id="a3db1-101">Set-AzureRmVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="a3db1-101">Set-AzureRmVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="a3db1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3db1-102">SYNOPSIS</span></span>
<span data-ttu-id="a3db1-103">Sanal ağ geçidi için varsayılan siteyi ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a3db1-103">Sets the default site for a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3db1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a3db1-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3db1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a3db1-105">DESCRIPTION</span></span>
<span data-ttu-id="a3db1-106">**Set-AzureRmVirtualNetworkGatewayDefaultSite** cmdlet 'i sanal ağ geçidine Zorlanmış tünel varsayılan sitesi atar.</span><span class="sxs-lookup"><span data-stu-id="a3db1-106">The **Set-AzureRmVirtualNetworkGatewayDefaultSite** cmdlet assigns a forced tunneling default site to a virtual network gateway.</span></span>
<span data-ttu-id="a3db1-107">Zorlamalı tünel, Azure sanal makinelerden şirket içi ağınıza Internet 'e bağlı trafik yönlendirmenize yol sunar; Bu, göndermeden önce trafiği incelemenizi ve denetlemenizi kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="a3db1-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="a3db1-108">Zorlamalı tünel, sanal özel ağ (VPN) tüneli kullanılarak yürütülür; Bu tünel, varsayılan bir site gerektirir, tüm Azure Internet 'e bağlı trafiğin yönlendirileceği yerel ağ geçidi.</span><span class="sxs-lookup"><span data-stu-id="a3db1-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="a3db1-109">**Set-AzureRmVirtualNetworkGatewayDefaultSite** ağ geçidine atanmış olan varsayılan siteyi değiştirmek için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="a3db1-109">**Set-AzureRmVirtualNetworkGatewayDefaultSite** provides a way to change the default site assigned to a gateway.</span></span>

## <span data-ttu-id="a3db1-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a3db1-110">EXAMPLES</span></span>

### <span data-ttu-id="a3db1-111">Örnek 1: sanal ağ ağ geçidine varsayılan site atama</span><span class="sxs-lookup"><span data-stu-id="a3db1-111">Example 1: Assign a default site to a virtual network gateway</span></span>
```
PS C:\>$LocalGateway = Get-AzureRmLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzureRmVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

<span data-ttu-id="a3db1-112">Bu örnek, ContosoVirtualGateway adlı sanal ağ geçidine varsayılan bir site atar.</span><span class="sxs-lookup"><span data-stu-id="a3db1-112">This example assigns a default site to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="a3db1-113">İlk komut, ContosoLocalGateway adlı yerel bir ağ geçidine nesne başvurusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a3db1-113">The first command creates an object reference to a local gateway named ContosoLocalGateway.</span></span>
<span data-ttu-id="a3db1-114">$LocalGateway adlı değişkende depolanan bu nesne başvurusu, varsayılan site olarak yapılandırılacak ağ geçidini temsil eder</span><span class="sxs-lookup"><span data-stu-id="a3db1-114">This object reference that is stored in the variable named $LocalGateway represents the gateway to be configured as the default site</span></span>

<span data-ttu-id="a3db1-115">.</span><span class="sxs-lookup"><span data-stu-id="a3db1-115">.</span></span>
<span data-ttu-id="a3db1-116">İkinci komut, sanal ağ geçidi için bir nesne başvurusu oluşturur ve sonucu $VirtualGateway adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="a3db1-116">The second command then creates an object reference to the virtual network gateway and stores the result in the variable named $VirtualGateway.</span></span>

<span data-ttu-id="a3db1-117">Üçüncü komut, varsayılan siteyi ContosoVirtualGateway 'e atamak için **set-AzureRmVirtualNetworkGatewayDefaultSite** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="a3db1-117">The third command uses the **Set-AzureRmVirtualNetworkGatewayDefaultSite** cmdlet to assign the default site to ContosoVirtualGateway.</span></span>

## <span data-ttu-id="a3db1-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a3db1-118">PARAMETERS</span></span>

### <span data-ttu-id="a3db1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3db1-119">-DefaultProfile</span></span>
<span data-ttu-id="a3db1-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a3db1-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3db1-121">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="a3db1-121">-GatewayDefaultSite</span></span>
<span data-ttu-id="a3db1-122">Belirtilen sanal ağın varsayılan sitesi olarak atanacak yerel ağ ağ geçidinin nesne başvurusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3db1-122">Specifies an object reference to the local network gateway to be assigned as the default site for the specified virtual network.</span></span>
<span data-ttu-id="a3db1-123">Yerel ağ geçidine nesne başvurusu oluşturmak için Get-AzureRmLocalNetworkGateway cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a3db1-123">You can use the Get-AzureRmLocalNetworkGateway cmdlet to create an object reference to a local gateway.</span></span>

```yaml
Type: PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3db1-124">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a3db1-124">-VirtualNetworkGateway</span></span>
<span data-ttu-id="a3db1-125">Varsayılan sitenin atanacağı sanal ağ ağ geçidi 'ne yönelik bir nesne başvurusu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3db1-125">Specifies an object reference to the virtual network gateway where the default site will be assigned.</span></span>
<span data-ttu-id="a3db1-126">**Get-AzureRmVirtualNetworkGateway** 'i kullanarak ve ağ geçidinin adını belirterek sanal ağ geçidi 'ne nesne başvurusu oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a3db1-126">You can create an object reference to a virtual network gateway by using the **Get-AzureRmVirtualNetworkGateway** and specifying the name of the gateway.</span></span>

<span data-ttu-id="a3db1-127">Değişken $VirtualGateway, *Virtualnetworkgateway* parametresinin parametre değeri olarak kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="a3db1-127">The variable $VirtualGateway can then be used as the parameter value for the *VirtualNetworkGateway* parameter:</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3db1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3db1-128">CommonParameters</span></span>
<span data-ttu-id="a3db1-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a3db1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3db1-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3db1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3db1-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a3db1-131">INPUTS</span></span>

###  
<span data-ttu-id="a3db1-132">Bu cmdlet, **Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway** nesnesinin ardışık olarak birleştirilmiş örneklerini kabul eder.</span><span class="sxs-lookup"><span data-stu-id="a3db1-132">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="a3db1-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a3db1-133">OUTPUTS</span></span>

###  
<span data-ttu-id="a3db1-134">Bu cmdlet, **Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway** nesnesinin varolan örneklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a3db1-134">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="a3db1-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a3db1-135">NOTES</span></span>

## <span data-ttu-id="a3db1-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a3db1-136">RELATED LINKS</span></span>

[<span data-ttu-id="a3db1-137">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a3db1-137">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="a3db1-138">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a3db1-138">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="a3db1-139">Remove-AzureRmVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="a3db1-139">Remove-AzureRmVirtualNetworkGatewayDefaultSite</span></span>](./Remove-AzureRmVirtualNetworkGatewayDefaultSite.md)


