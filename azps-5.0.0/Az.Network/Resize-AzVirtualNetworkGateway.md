---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/resize-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
ms.openlocfilehash: dd48af6a0f20cafea5911adb629a83323faa94a6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325240"
---
# <span data-ttu-id="7a34f-101">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7a34f-101">Resize-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="7a34f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a34f-102">SYNOPSIS</span></span>
<span data-ttu-id="7a34f-103">Var olan bir sanal ağ ağ geçidini yeniden boyutlandırır.</span><span class="sxs-lookup"><span data-stu-id="7a34f-103">Resizes an existing virtual network gateway.</span></span>

## <span data-ttu-id="7a34f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7a34f-104">SYNTAX</span></span>

```
Resize-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a34f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7a34f-105">DESCRIPTION</span></span>
<span data-ttu-id="7a34f-106">**Resize-AzVirtualNetworkGateway** cmdlet 'i, sanal ağ geçidi için hisse senedi BIRIMINI (SKU) değiştirmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="7a34f-106">The **Resize-AzVirtualNetworkGateway** cmdlet enables you to change the stock-keeping unit (SKU) for a virtual network gateway.</span></span>
<span data-ttu-id="7a34f-107">STB 'ler, üretilen iş ve izin verilen en fazla IP tüneli sayısı dahil olmak üzere, ağ geçidinin özelliklerini belirler.</span><span class="sxs-lookup"><span data-stu-id="7a34f-107">SKUs determine the capabilities of a gateway, including such things as throughput and the maximum number of IP tunnels that are allowed.</span></span>
<span data-ttu-id="7a34f-108">Azure temel, standart, yüksek performanslı, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ STB 'leri (bazen küçük, orta ve büyük STB 'ler olarak adlandırılır) destekler.</span><span class="sxs-lookup"><span data-stu-id="7a34f-108">Azure supports Basic, Standard, High-Performance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ SKUs (sometimes referred to as Small, Medium, and Large SKUs).</span></span>
<span data-ttu-id="7a34f-109">Her SKU türünün özellikleri hakkında ayrıntılı bilgi için bkz https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .</span><span class="sxs-lookup"><span data-stu-id="7a34f-109">For detailed information about the capabilities of each SKU type, see https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/.</span></span>
<span data-ttu-id="7a34f-110">STB 'Ların, yeteneklerin yanı sıra fiyatlandırmayla farklı olmasına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="7a34f-110">Keep in mind that SKUs differ in pricing as well as capabilities.</span></span>
<span data-ttu-id="7a34f-111">Daha fazla bilgi için bkz https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .</span><span class="sxs-lookup"><span data-stu-id="7a34f-111">For more information, see https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/.</span></span>

## <span data-ttu-id="7a34f-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7a34f-112">EXAMPLES</span></span>

### <span data-ttu-id="7a34f-113">Örnek 1: sanal ağ geçidi boyutunu değiştirme</span><span class="sxs-lookup"><span data-stu-id="7a34f-113">Example 1: Change the size of a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

<span data-ttu-id="7a34f-114">Bu örnekte, ContosoVirtualGateway adındaki sanal ağ geçidinin boyutu değişir.</span><span class="sxs-lookup"><span data-stu-id="7a34f-114">This example changes the size of a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="7a34f-115">İlk komut, ContosoVirtualGateway için bir nesne başvurusu oluşturur; Bu nesne başvurusu $Gateway adlı bir değişkende depolanır.</span><span class="sxs-lookup"><span data-stu-id="7a34f-115">The first command creates an object reference to ContosoVirtualGateway; this object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="7a34f-116">İkinci komut daha sonra *Gatewaysku* özelliğini temel olarak ayarlamak için **Resize-AzVirtualNetworkGateway** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="7a34f-116">The second command then uses the **Resize-AzVirtualNetworkGateway** cmdlet to set the *GatewaySku* property to Basic.</span></span>

## <span data-ttu-id="7a34f-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7a34f-117">PARAMETERS</span></span>

### <span data-ttu-id="7a34f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a34f-118">-DefaultProfile</span></span>
<span data-ttu-id="7a34f-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7a34f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a34f-120">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="7a34f-120">-GatewaySku</span></span>
<span data-ttu-id="7a34f-121">Yeni ağ geçidi SKU türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a34f-121">Specifies the new type of gateway SKU.</span></span>
<span data-ttu-id="7a34f-122">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="7a34f-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7a34f-123">Ana</span><span class="sxs-lookup"><span data-stu-id="7a34f-123">Basic</span></span>
- <span data-ttu-id="7a34f-124">Ardından</span><span class="sxs-lookup"><span data-stu-id="7a34f-124">Standard</span></span>
- <span data-ttu-id="7a34f-125">Yüksek performans</span><span class="sxs-lookup"><span data-stu-id="7a34f-125">High Performance</span></span>
- <span data-ttu-id="7a34f-126">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="7a34f-126">VpnGw1</span></span>
- <span data-ttu-id="7a34f-127">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="7a34f-127">VpnGw2</span></span>
- <span data-ttu-id="7a34f-128">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="7a34f-128">VpnGw3</span></span>
- <span data-ttu-id="7a34f-129">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="7a34f-129">VpnGw1AZ</span></span> 
- <span data-ttu-id="7a34f-130">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="7a34f-130">VpnGw2AZ</span></span> 
- <span data-ttu-id="7a34f-131">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="7a34f-131">VpnGw3AZ</span></span> 
- <span data-ttu-id="7a34f-132">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="7a34f-132">ErGw1AZ</span></span> 
- <span data-ttu-id="7a34f-133">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="7a34f-133">ErGw2AZ</span></span> 
- <span data-ttu-id="7a34f-134">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="7a34f-134">ErGw3AZ</span></span> 

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

### <span data-ttu-id="7a34f-135">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7a34f-135">-VirtualNetworkGateway</span></span>
<span data-ttu-id="7a34f-136">Yeniden boyutlandırılacak sanal ağ geçidi 'nin nesne başvurusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a34f-136">Specifies an object reference to the virtual network gateway to be resized.</span></span>
<span data-ttu-id="7a34f-137">Bu nesne başvurusunu oluşturmak için Get-AzVirtualNetworkGateway kullanarak ağ geçidinin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="7a34f-137">You can create this object reference by using the Get-AzVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="7a34f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a34f-138">CommonParameters</span></span>
<span data-ttu-id="7a34f-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7a34f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a34f-140">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a34f-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a34f-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7a34f-141">INPUTS</span></span>

### <span data-ttu-id="7a34f-142">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7a34f-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="7a34f-143">System. String</span><span class="sxs-lookup"><span data-stu-id="7a34f-143">System.String</span></span>

## <span data-ttu-id="7a34f-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7a34f-144">OUTPUTS</span></span>

### <span data-ttu-id="7a34f-145">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7a34f-145">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="7a34f-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7a34f-146">NOTES</span></span>
<span data-ttu-id="7a34f-147">Temel/standart/üst performans SKU 'larından yeni VpnGw1/VpnGw2/VpnGw3 SKU 'Larını yeniden boyutlandıramazsınız.</span><span class="sxs-lookup"><span data-stu-id="7a34f-147">You cannot resize from Basic/Standard/HighPerformance SKUs to the new VpnGw1/VpnGw2/VpnGw3 SKUs.</span></span> <span data-ttu-id="7a34f-148">Diğer yeniden boyutlandırmayı VpnGw1AZ/VpnGw2AZ/VpnGw3AZ veya ErGw1AZ/ErGw2AZ/ErGw3AZ.</span><span class="sxs-lookup"><span data-stu-id="7a34f-148">Further resize is not allowed from/to VpnGw1AZ/VpnGw2AZ/VpnGw3AZ or ErGw1AZ/ErGw2AZ/ErGw3AZ.</span></span> <span data-ttu-id="7a34f-149">Yeniden boyutlandırma yalnızca STB ' serisi ' içinde, VpnGw1AZ VpnGw2AZ/VpnGw3AZ olarak yeniden boyutlandırılabilir ve ErGw2AZ/ErGw3AZ olarak yeniden boyutlandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="7a34f-149">Resize is allowed only within the SKU 'series' e.g VpnGw1AZ can be resized to/from VpnGw2AZ/VpnGw3AZ and ErGw1AZ can be resized to/from ErGw2AZ/ErGw3AZ.</span></span> <span data-ttu-id="7a34f-150"> https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngatewaysYönergeler için bkz.</span><span class="sxs-lookup"><span data-stu-id="7a34f-150">See https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways for instructions.</span></span>

## <span data-ttu-id="7a34f-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7a34f-151">RELATED LINKS</span></span>

[<span data-ttu-id="7a34f-152">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7a34f-152">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="7a34f-153">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7a34f-153">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="7a34f-154">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7a34f-154">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="7a34f-155">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7a34f-155">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="7a34f-156">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7a34f-156">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)

[<span data-ttu-id="7a34f-157">Get-AzVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="7a34f-157">Get-AzVpnClientPackage</span></span>](./Get-AzVpnClientPackage.md)

[<span data-ttu-id="7a34f-158">Set-AzVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="7a34f-158">Set-AzVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)
