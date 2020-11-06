---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/resize-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Resize-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Resize-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 0a8a5c4084813bac74ea907575d2bd26c3d8c5f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593940"
---
# <span data-ttu-id="7e848-101">Resize-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7e848-101">Resize-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="7e848-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e848-102">SYNOPSIS</span></span>
<span data-ttu-id="7e848-103">Var olan bir sanal ağ ağ geçidini yeniden boyutlandırır.</span><span class="sxs-lookup"><span data-stu-id="7e848-103">Resizes an existing virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e848-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7e848-104">SYNTAX</span></span>

```
Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e848-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7e848-105">DESCRIPTION</span></span>
<span data-ttu-id="7e848-106">**Resize-AzureRmVirtualNetworkGateway** cmdlet 'i, sanal ağ geçidi için hisse senedi BIRIMINI (SKU) değiştirmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="7e848-106">The **Resize-AzureRmVirtualNetworkGateway** cmdlet enables you to change the stock-keeping unit (SKU) for a virtual network gateway.</span></span>
<span data-ttu-id="7e848-107">STB 'ler, üretilen iş ve izin verilen en fazla IP tüneli sayısı dahil olmak üzere, ağ geçidinin özelliklerini belirler.</span><span class="sxs-lookup"><span data-stu-id="7e848-107">SKUs determine the capabilities of a gateway, including such things as throughput and the maximum number of IP tunnels that are allowed.</span></span>
<span data-ttu-id="7e848-108">Azure temel, standart, yüksek performanslı, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ STB 'leri (bazen küçük, orta ve büyük STB 'ler olarak adlandırılır) destekler.</span><span class="sxs-lookup"><span data-stu-id="7e848-108">Azure supports Basic, Standard, High-Performance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ SKUs (sometimes referred to as Small, Medium, and Large SKUs).</span></span>
<span data-ttu-id="7e848-109">Her SKU türünün özellikleri hakkında ayrıntılı bilgi için bkz https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .</span><span class="sxs-lookup"><span data-stu-id="7e848-109">For detailed information about the capabilities of each SKU type, see https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/.</span></span>
<span data-ttu-id="7e848-110">STB 'Ların, yeteneklerin yanı sıra fiyatlandırmayla farklı olmasına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="7e848-110">Keep in mind that SKUs differ in pricing as well as capabilities.</span></span>
<span data-ttu-id="7e848-111">Daha fazla bilgi için bkz https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .</span><span class="sxs-lookup"><span data-stu-id="7e848-111">For more information, see https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/.</span></span>

## <span data-ttu-id="7e848-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7e848-112">EXAMPLES</span></span>

### <span data-ttu-id="7e848-113">Örnek 1: sanal ağ geçidi boyutunu değiştirme</span><span class="sxs-lookup"><span data-stu-id="7e848-113">Example 1: Change the size of a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

<span data-ttu-id="7e848-114">Bu örnekte, ContosoVirtualGateway adındaki sanal ağ geçidinin boyutu değişir.</span><span class="sxs-lookup"><span data-stu-id="7e848-114">This example changes the size of a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="7e848-115">İlk komut, ContosoVirtualGateway için bir nesne başvurusu oluşturur; Bu nesne başvurusu $Gateway adlı bir değişkende depolanır.</span><span class="sxs-lookup"><span data-stu-id="7e848-115">The first command creates an object reference to ContosoVirtualGateway; this object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="7e848-116">İkinci komut daha sonra *Gatewaysku* özelliğini temel olarak ayarlamak için **Resize-AzureRmVirtualNetworkGateway** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="7e848-116">The second command then uses the **Resize-AzureRmVirtualNetworkGateway** cmdlet to set the *GatewaySku* property to Basic.</span></span>

## <span data-ttu-id="7e848-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7e848-117">PARAMETERS</span></span>

### <span data-ttu-id="7e848-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e848-118">-DefaultProfile</span></span>
<span data-ttu-id="7e848-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7e848-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e848-120">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="7e848-120">-GatewaySku</span></span>
<span data-ttu-id="7e848-121">Yeni ağ geçidi SKU türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e848-121">Specifies the new type of gateway SKU.</span></span>
<span data-ttu-id="7e848-122">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="7e848-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7e848-123">Ana</span><span class="sxs-lookup"><span data-stu-id="7e848-123">Basic</span></span>
- <span data-ttu-id="7e848-124">Ardından</span><span class="sxs-lookup"><span data-stu-id="7e848-124">Standard</span></span>
- <span data-ttu-id="7e848-125">Yüksek performans</span><span class="sxs-lookup"><span data-stu-id="7e848-125">High Performance</span></span>
- <span data-ttu-id="7e848-126">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="7e848-126">VpnGw1</span></span>
- <span data-ttu-id="7e848-127">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="7e848-127">VpnGw2</span></span>
- <span data-ttu-id="7e848-128">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="7e848-128">VpnGw3</span></span>
- <span data-ttu-id="7e848-129">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="7e848-129">VpnGw1AZ</span></span> 
- <span data-ttu-id="7e848-130">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="7e848-130">VpnGw2AZ</span></span> 
- <span data-ttu-id="7e848-131">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="7e848-131">VpnGw3AZ</span></span> 
- <span data-ttu-id="7e848-132">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="7e848-132">ErGw1AZ</span></span> 
- <span data-ttu-id="7e848-133">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="7e848-133">ErGw2AZ</span></span> 
- <span data-ttu-id="7e848-134">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="7e848-134">ErGw3AZ</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e848-135">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7e848-135">-VirtualNetworkGateway</span></span>
<span data-ttu-id="7e848-136">Yeniden boyutlandırılacak sanal ağ geçidi 'nin nesne başvurusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7e848-136">Specifies an object reference to the virtual network gateway to be resized.</span></span>
<span data-ttu-id="7e848-137">Bu nesne başvurusunu oluşturmak için Get-AzureRmVirtualNetworkGateway kullanarak ağ geçidinin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="7e848-137">You can create this object reference by using the Get-AzureRmVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="7e848-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e848-138">CommonParameters</span></span>
<span data-ttu-id="7e848-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7e848-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e848-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e848-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e848-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7e848-141">INPUTS</span></span>

### <span data-ttu-id="7e848-142">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7e848-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="7e848-143">Parametreler: VirtualNetworkGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7e848-143">Parameters: VirtualNetworkGateway (ByValue)</span></span>

### <span data-ttu-id="7e848-144">System. String</span><span class="sxs-lookup"><span data-stu-id="7e848-144">System.String</span></span>

## <span data-ttu-id="7e848-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7e848-145">OUTPUTS</span></span>

### <span data-ttu-id="7e848-146">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7e848-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="7e848-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7e848-147">NOTES</span></span>
<span data-ttu-id="7e848-148">Temel/standart/üst performans SKU 'larından yeni VpnGw1/VpnGw2/VpnGw3 SKU 'Larını yeniden boyutlandıramazsınız.</span><span class="sxs-lookup"><span data-stu-id="7e848-148">You cannot resize from Basic/Standard/HighPerformance SKUs to the new VpnGw1/VpnGw2/VpnGw3 SKUs.</span></span> <span data-ttu-id="7e848-149">Diğer yeniden boyutlandırmayı VpnGw1AZ/VpnGw2AZ/VpnGw3AZ veya ErGw1AZ/ErGw2AZ/ErGw3AZ.</span><span class="sxs-lookup"><span data-stu-id="7e848-149">Further resize is not allowed from/to VpnGw1AZ/VpnGw2AZ/VpnGw3AZ or ErGw1AZ/ErGw2AZ/ErGw3AZ.</span></span> <span data-ttu-id="7e848-150">Yeniden boyutlandırma yalnızca STB ' serisi ' içinde, VpnGw1AZ VpnGw2AZ/VpnGw3AZ olarak yeniden boyutlandırılabilir ve ErGw2AZ/ErGw3AZ olarak yeniden boyutlandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="7e848-150">Resize is allowed only within the SKU 'series' e.g VpnGw1AZ can be resized to/from VpnGw2AZ/VpnGw3AZ and ErGw1AZ can be resized to/from ErGw2AZ/ErGw3AZ.</span></span> <span data-ttu-id="7e848-151"> https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngatewaysYönergeler için bkz.</span><span class="sxs-lookup"><span data-stu-id="7e848-151">See https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways for instructions.</span></span>

## <span data-ttu-id="7e848-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7e848-152">RELATED LINKS</span></span>

[<span data-ttu-id="7e848-153">Get-AzureRmVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="7e848-153">Get-AzureRmVpnClientPackage</span></span>](./Get-AzureRmVpnClientPackage.md)

[<span data-ttu-id="7e848-154">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7e848-154">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="7e848-155">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="7e848-155">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md)


