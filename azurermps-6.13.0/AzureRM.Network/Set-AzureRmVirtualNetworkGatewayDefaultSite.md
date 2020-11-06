---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 9c0eec0f38929efe188d8ab0ba8e30d31a16b717
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589413"
---
# <span data-ttu-id="a7371-101">Set-AzureRmVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="a7371-101">Set-AzureRmVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="a7371-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7371-102">SYNOPSIS</span></span>
<span data-ttu-id="a7371-103">Sanal ağ geçidi için varsayılan siteyi ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a7371-103">Sets the default site for a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7371-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a7371-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7371-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a7371-105">DESCRIPTION</span></span>
<span data-ttu-id="a7371-106">**Set-AzureRmVirtualNetworkGatewayDefaultSite** cmdlet 'i sanal ağ geçidine Zorlanmış tünel varsayılan sitesi atar.</span><span class="sxs-lookup"><span data-stu-id="a7371-106">The **Set-AzureRmVirtualNetworkGatewayDefaultSite** cmdlet assigns a forced tunneling default site to a virtual network gateway.</span></span>
<span data-ttu-id="a7371-107">Zorlamalı tünel, Azure sanal makinelerden şirket içi ağınıza Internet 'e bağlı trafik yönlendirmenize yol sunar; Bu, göndermeden önce trafiği incelemenizi ve denetlemenizi kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="a7371-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="a7371-108">Zorlamalı tünel, sanal özel ağ (VPN) tüneli kullanılarak yürütülür; Bu tünel, varsayılan bir site gerektirir, tüm Azure Internet 'e bağlı trafiğin yönlendirileceği yerel ağ geçidi.</span><span class="sxs-lookup"><span data-stu-id="a7371-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="a7371-109">**Set-AzureRmVirtualNetworkGatewayDefaultSite** ağ geçidine atanmış olan varsayılan siteyi değiştirmek için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="a7371-109">**Set-AzureRmVirtualNetworkGatewayDefaultSite** provides a way to change the default site assigned to a gateway.</span></span>

## <span data-ttu-id="a7371-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a7371-110">EXAMPLES</span></span>

### <span data-ttu-id="a7371-111">Örnek 1: sanal ağ ağ geçidine varsayılan site atama</span><span class="sxs-lookup"><span data-stu-id="a7371-111">Example 1: Assign a default site to a virtual network gateway</span></span>
```
PS C:\>$LocalGateway = Get-AzureRmLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzureRmVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

<span data-ttu-id="a7371-112">Bu örnek, ContosoVirtualGateway adlı sanal ağ geçidine varsayılan bir site atar.</span><span class="sxs-lookup"><span data-stu-id="a7371-112">This example assigns a default site to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="a7371-113">İlk komut, ContosoLocalGateway adlı yerel bir ağ geçidine nesne başvurusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a7371-113">The first command creates an object reference to a local gateway named ContosoLocalGateway.</span></span>
<span data-ttu-id="a7371-114">$LocalGateway adlı değişkende depolanan bu nesne başvurusu, varsayılan site olarak yapılandırılacak ağ geçidini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="a7371-114">This object reference that is stored in the variable named $LocalGateway represents the gateway to be configured as the default site .</span></span>
<span data-ttu-id="a7371-115">İkinci komut, sanal ağ geçidi için bir nesne başvurusu oluşturur ve sonucu $VirtualGateway adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="a7371-115">The second command then creates an object reference to the virtual network gateway and stores the result in the variable named $VirtualGateway.</span></span>
<span data-ttu-id="a7371-116">Üçüncü komut, varsayılan siteyi ContosoVirtualGateway 'e atamak için **set-AzureRmVirtualNetworkGatewayDefaultSite** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="a7371-116">The third command uses the **Set-AzureRmVirtualNetworkGatewayDefaultSite** cmdlet to assign the default site to ContosoVirtualGateway.</span></span>

## <span data-ttu-id="a7371-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a7371-117">PARAMETERS</span></span>

### <span data-ttu-id="a7371-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7371-118">-DefaultProfile</span></span>
<span data-ttu-id="a7371-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a7371-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7371-120">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="a7371-120">-GatewayDefaultSite</span></span>
<span data-ttu-id="a7371-121">Belirtilen sanal ağın varsayılan sitesi olarak atanacak yerel ağ ağ geçidinin nesne başvurusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a7371-121">Specifies an object reference to the local network gateway to be assigned as the default site for the specified virtual network.</span></span>
<span data-ttu-id="a7371-122">Yerel ağ geçidine nesne başvurusu oluşturmak için Get-AzureRmLocalNetworkGateway cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a7371-122">You can use the Get-AzureRmLocalNetworkGateway cmdlet to create an object reference to a local gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7371-123">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a7371-123">-VirtualNetworkGateway</span></span>
<span data-ttu-id="a7371-124">Varsayılan sitenin atanacağı sanal ağ ağ geçidi 'ne yönelik bir nesne başvurusu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a7371-124">Specifies an object reference to the virtual network gateway where the default site will be assigned.</span></span>
<span data-ttu-id="a7371-125">**Get-AzureRmVirtualNetworkGateway** 'i kullanarak ve ağ geçidinin adını belirterek sanal ağ geçidi 'ne nesne başvurusu oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a7371-125">You can create an object reference to a virtual network gateway by using the **Get-AzureRmVirtualNetworkGateway** and specifying the name of the gateway.</span></span>
<span data-ttu-id="a7371-126">Değişken $VirtualGateway, *Virtualnetworkgateway* parametresinin parametre değeri olarak kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="a7371-126">The variable $VirtualGateway can then be used as the parameter value for the *VirtualNetworkGateway* parameter:</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7371-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7371-127">CommonParameters</span></span>
<span data-ttu-id="a7371-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a7371-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7371-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7371-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7371-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a7371-130">INPUTS</span></span>

### <span data-ttu-id="a7371-131">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a7371-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="a7371-132">Parametreler: VirtualNetworkGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a7371-132">Parameters: VirtualNetworkGateway (ByValue)</span></span>

### <span data-ttu-id="a7371-133">Microsoft. Azure. Commands. Network. model. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a7371-133">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="a7371-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a7371-134">OUTPUTS</span></span>

### <span data-ttu-id="a7371-135">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a7371-135">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="a7371-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a7371-136">NOTES</span></span>

## <span data-ttu-id="a7371-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a7371-137">RELATED LINKS</span></span>

[<span data-ttu-id="a7371-138">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a7371-138">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="a7371-139">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a7371-139">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="a7371-140">Remove-AzureRmVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="a7371-140">Remove-AzureRmVirtualNetworkGatewayDefaultSite</span></span>](./Remove-AzureRmVirtualNetworkGatewayDefaultSite.md)


