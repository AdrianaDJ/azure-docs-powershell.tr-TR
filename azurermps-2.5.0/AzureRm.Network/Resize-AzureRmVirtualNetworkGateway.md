---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/resize-azurermvirtualnetworkgateway
schema: 2.0.0
ms.openlocfilehash: 0a3dea2b706f7efcdc76b48175df225e2974728c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940021"
---
# <span data-ttu-id="8c824-101">Resize-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8c824-101">Resize-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="8c824-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c824-102">SYNOPSIS</span></span>
<span data-ttu-id="8c824-103">Var olan bir sanal ağ ağ geçidini yeniden boyutlandırır.</span><span class="sxs-lookup"><span data-stu-id="8c824-103">Resizes an existing virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c824-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8c824-104">SYNTAX</span></span>

```
Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c824-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8c824-105">DESCRIPTION</span></span>
<span data-ttu-id="8c824-106">**Resize-AzureRmVirtualNetworkGateway** cmdlet 'i, sanal ağ geçidi için hisse senedi BIRIMINI (SKU) değiştirmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="8c824-106">The **Resize-AzureRmVirtualNetworkGateway** cmdlet enables you to change the stock-keeping unit (SKU) for a virtual network gateway.</span></span>
<span data-ttu-id="8c824-107">STB 'ler, üretilen iş ve izin verilen en fazla IP tüneli sayısı dahil olmak üzere, ağ geçidinin özelliklerini belirler.</span><span class="sxs-lookup"><span data-stu-id="8c824-107">SKUs determine the capabilities of a gateway, including such things as throughput and the maximum number of IP tunnels that are allowed.</span></span>
<span data-ttu-id="8c824-108">Azure temel, standart, yüksek performanslı, VpnGw1, VpnGw2 ve VpnGw3 SKU 'Larını (bazen küçük, orta ve büyük STB 'ler olarak da adlandırılır) destekler.</span><span class="sxs-lookup"><span data-stu-id="8c824-108">Azure supports Basic, Standard, High-Performance, VpnGw1, VpnGw2 and VpnGw3 SKUs (sometimes referred to as Small, Medium, and Large SKUs).</span></span>
<span data-ttu-id="8c824-109">Her SKU türünün özellikleri hakkında ayrıntılı bilgi için bkz https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .</span><span class="sxs-lookup"><span data-stu-id="8c824-109">For detailed information about the capabilities of each SKU type, see https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/.</span></span>

<span data-ttu-id="8c824-110">STB 'Ların, yeteneklerin yanı sıra fiyatlandırmayla farklı olmasına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="8c824-110">Keep in mind that SKUs differ in pricing as well as capabilities.</span></span>
<span data-ttu-id="8c824-111">Daha fazla bilgi için bkz https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .</span><span class="sxs-lookup"><span data-stu-id="8c824-111">For more information, see https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/.</span></span>

## <span data-ttu-id="8c824-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8c824-112">EXAMPLES</span></span>

### <span data-ttu-id="8c824-113">Örnek 1: sanal ağ geçidi boyutunu değiştirme</span><span class="sxs-lookup"><span data-stu-id="8c824-113">Example 1: Change the size of a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

<span data-ttu-id="8c824-114">Bu örnekte, ContosoVirtualGateway adındaki sanal ağ geçidinin boyutu değişir.</span><span class="sxs-lookup"><span data-stu-id="8c824-114">This example changes the size of a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="8c824-115">İlk komut, ContosoVirtualGateway için bir nesne başvurusu oluşturur; Bu nesne başvurusu $Gateway adlı bir değişkende depolanır.</span><span class="sxs-lookup"><span data-stu-id="8c824-115">The first command creates an object reference to ContosoVirtualGateway; this object reference is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="8c824-116">İkinci komut daha sonra *Gatewaysku* özelliğini temel olarak ayarlamak için **Resize-AzureRmVirtualNetworkGateway** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="8c824-116">The second command then uses the **Resize-AzureRmVirtualNetworkGateway** cmdlet to set the *GatewaySku* property to Basic.</span></span>

## <span data-ttu-id="8c824-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8c824-117">PARAMETERS</span></span>

### <span data-ttu-id="8c824-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c824-118">-DefaultProfile</span></span>
<span data-ttu-id="8c824-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8c824-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c824-120">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="8c824-120">-GatewaySku</span></span>
<span data-ttu-id="8c824-121">Yeni ağ geçidi SKU türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="8c824-121">Specifies the new type of gateway SKU.</span></span>
<span data-ttu-id="8c824-122">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="8c824-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8c824-123">Ana</span><span class="sxs-lookup"><span data-stu-id="8c824-123">Basic</span></span>
- <span data-ttu-id="8c824-124">Ardından</span><span class="sxs-lookup"><span data-stu-id="8c824-124">Standard</span></span>
- <span data-ttu-id="8c824-125">Yüksek performans</span><span class="sxs-lookup"><span data-stu-id="8c824-125">High Performance</span></span>
- <span data-ttu-id="8c824-126">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="8c824-126">VpnGw1</span></span>
- <span data-ttu-id="8c824-127">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="8c824-127">VpnGw2</span></span>
- <span data-ttu-id="8c824-128">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="8c824-128">VpnGw3</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c824-129">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8c824-129">-VirtualNetworkGateway</span></span>
<span data-ttu-id="8c824-130">Yeniden boyutlandırılacak sanal ağ geçidi 'nin nesne başvurusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8c824-130">Specifies an object reference to the virtual network gateway to be resized.</span></span>
<span data-ttu-id="8c824-131">Bu nesne başvurusunu oluşturmak için Get-AzureRmVirtualNetworkGateway kullanarak ağ geçidinin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="8c824-131">You can create this object reference by using the Get-AzureRmVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="8c824-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c824-132">CommonParameters</span></span>
<span data-ttu-id="8c824-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8c824-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c824-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c824-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c824-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8c824-135">INPUTS</span></span>

###  
<span data-ttu-id="8c824-136">Bu cmdlet, **Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway** nesnesinin ardışık olarak birleştirilmiş örneklerini kabul eder.</span><span class="sxs-lookup"><span data-stu-id="8c824-136">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="8c824-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8c824-137">OUTPUTS</span></span>

###  
<span data-ttu-id="8c824-138">Bu cmdlet, **Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway** nesnesinin varolan örneklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="8c824-138">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="8c824-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8c824-139">NOTES</span></span>
<span data-ttu-id="8c824-140">Temel/standart/üst performans SKU 'larından yeni VpnGw1/VpnGw2/VpnGw3 SKU 'Larını yeniden boyutlandıramazsınız.</span><span class="sxs-lookup"><span data-stu-id="8c824-140">You cannot resize from Basic/Standard/HighPerformance SKUs to the new VpnGw1/VpnGw2/VpnGw3 SKUs.</span></span> <span data-ttu-id="8c824-141"> https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngatewaysYönergeler için bkz.</span><span class="sxs-lookup"><span data-stu-id="8c824-141">See https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways for instructions.</span></span>

## <span data-ttu-id="8c824-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8c824-142">RELATED LINKS</span></span>

[<span data-ttu-id="8c824-143">Get-AzureRmVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="8c824-143">Get-AzureRmVpnClientPackage</span></span>](./Get-AzureRmVpnClientPackage.md)

[<span data-ttu-id="8c824-144">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8c824-144">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="8c824-145">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="8c824-145">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md)


