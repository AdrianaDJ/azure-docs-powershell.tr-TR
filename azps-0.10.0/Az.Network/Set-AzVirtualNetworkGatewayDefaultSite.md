---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 560053ca6b5e49ffcef8dbb6ee4b0ba32f3ed276
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936506"
---
# <span data-ttu-id="b767c-101">Set-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="b767c-101">Set-AzVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="b767c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b767c-102">SYNOPSIS</span></span>
<span data-ttu-id="b767c-103">Sanal ağ geçidi için varsayılan siteyi ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b767c-103">Sets the default site for a virtual network gateway.</span></span>

## <span data-ttu-id="b767c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b767c-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b767c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b767c-105">DESCRIPTION</span></span>
<span data-ttu-id="b767c-106">**Set-AzVirtualNetworkGatewayDefaultSite** cmdlet 'i, bir sanal ağ geçidine zorunlu tünelleme varsayılan sitesi atar.</span><span class="sxs-lookup"><span data-stu-id="b767c-106">The **Set-AzVirtualNetworkGatewayDefaultSite** cmdlet assigns a forced tunneling default site to a virtual network gateway.</span></span>
<span data-ttu-id="b767c-107">Zorlamalı tünel, Azure sanal makinelerden şirket içi ağınıza Internet 'e bağlı trafik yönlendirmenize yol sunar; Bu, göndermeden önce trafiği incelemenizi ve denetlemenizi kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="b767c-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="b767c-108">Zorlamalı tünel, sanal özel ağ (VPN) tüneli kullanılarak yürütülür; Bu tünel, varsayılan bir site gerektirir, tüm Azure Internet 'e bağlı trafiğin yönlendirileceği yerel ağ geçidi.</span><span class="sxs-lookup"><span data-stu-id="b767c-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="b767c-109">**Set-AzVirtualNetworkGatewayDefaultSite** bir ağ geçidine atanmış olan varsayılan siteyi değiştirmek için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="b767c-109">**Set-AzVirtualNetworkGatewayDefaultSite** provides a way to change the default site assigned to a gateway.</span></span>

## <span data-ttu-id="b767c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b767c-110">EXAMPLES</span></span>

### <span data-ttu-id="b767c-111">Örnek 1: sanal ağ ağ geçidine varsayılan site atama</span><span class="sxs-lookup"><span data-stu-id="b767c-111">Example 1: Assign a default site to a virtual network gateway</span></span>
```
PS C:\>$LocalGateway = Get-AzLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

<span data-ttu-id="b767c-112">Bu örnek, ContosoVirtualGateway adlı sanal ağ geçidine varsayılan bir site atar.</span><span class="sxs-lookup"><span data-stu-id="b767c-112">This example assigns a default site to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="b767c-113">İlk komut, ContosoLocalGateway adlı yerel bir ağ geçidine nesne başvurusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b767c-113">The first command creates an object reference to a local gateway named ContosoLocalGateway.</span></span>
<span data-ttu-id="b767c-114">$LocalGateway adlı değişkende depolanan bu nesne başvurusu, varsayılan site olarak yapılandırılacak ağ geçidini temsil eder</span><span class="sxs-lookup"><span data-stu-id="b767c-114">This object reference that is stored in the variable named $LocalGateway represents the gateway to be configured as the default site</span></span>

<span data-ttu-id="b767c-115">.</span><span class="sxs-lookup"><span data-stu-id="b767c-115">.</span></span>
<span data-ttu-id="b767c-116">İkinci komut, sanal ağ geçidi için bir nesne başvurusu oluşturur ve sonucu $VirtualGateway adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="b767c-116">The second command then creates an object reference to the virtual network gateway and stores the result in the variable named $VirtualGateway.</span></span>

<span data-ttu-id="b767c-117">Üçüncü komut, varsayılan siteyi ContosoVirtualGateway 'e atamak için **set-AzVirtualNetworkGatewayDefaultSite** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="b767c-117">The third command uses the **Set-AzVirtualNetworkGatewayDefaultSite** cmdlet to assign the default site to ContosoVirtualGateway.</span></span>

## <span data-ttu-id="b767c-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b767c-118">PARAMETERS</span></span>

### <span data-ttu-id="b767c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b767c-119">-DefaultProfile</span></span>
<span data-ttu-id="b767c-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b767c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b767c-121">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="b767c-121">-GatewayDefaultSite</span></span>
<span data-ttu-id="b767c-122">Belirtilen sanal ağın varsayılan sitesi olarak atanacak yerel ağ ağ geçidinin nesne başvurusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b767c-122">Specifies an object reference to the local network gateway to be assigned as the default site for the specified virtual network.</span></span>
<span data-ttu-id="b767c-123">Yerel ağ geçidine nesne başvurusu oluşturmak için Get-AzLocalNetworkGateway cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b767c-123">You can use the Get-AzLocalNetworkGateway cmdlet to create an object reference to a local gateway.</span></span>

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

### <span data-ttu-id="b767c-124">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b767c-124">-VirtualNetworkGateway</span></span>
<span data-ttu-id="b767c-125">Varsayılan sitenin atanacağı sanal ağ ağ geçidi 'ne yönelik bir nesne başvurusu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b767c-125">Specifies an object reference to the virtual network gateway where the default site will be assigned.</span></span>
<span data-ttu-id="b767c-126">**Get-AzVirtualNetworkGateway** 'i kullanarak ve ağ geçidinin adını belirterek sanal ağ geçidi 'ne nesne başvurusu oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b767c-126">You can create an object reference to a virtual network gateway by using the **Get-AzVirtualNetworkGateway** and specifying the name of the gateway.</span></span>

<span data-ttu-id="b767c-127">Değişken $VirtualGateway, *Virtualnetworkgateway* parametresinin parametre değeri olarak kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="b767c-127">The variable $VirtualGateway can then be used as the parameter value for the *VirtualNetworkGateway* parameter:</span></span>

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

### <span data-ttu-id="b767c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b767c-128">CommonParameters</span></span>
<span data-ttu-id="b767c-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b767c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b767c-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b767c-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b767c-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b767c-131">INPUTS</span></span>

###  
<span data-ttu-id="b767c-132">Bu cmdlet, **Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway** nesnesinin ardışık olarak birleştirilmiş örneklerini kabul eder.</span><span class="sxs-lookup"><span data-stu-id="b767c-132">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="b767c-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b767c-133">OUTPUTS</span></span>

###  
<span data-ttu-id="b767c-134">Bu cmdlet, **Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway** nesnesinin varolan örneklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="b767c-134">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="b767c-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b767c-135">NOTES</span></span>

## <span data-ttu-id="b767c-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b767c-136">RELATED LINKS</span></span>

[<span data-ttu-id="b767c-137">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b767c-137">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="b767c-138">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b767c-138">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="b767c-139">Remove-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="b767c-139">Remove-AzVirtualNetworkGatewayDefaultSite</span></span>](./Remove-AzVirtualNetworkGatewayDefaultSite.md)


