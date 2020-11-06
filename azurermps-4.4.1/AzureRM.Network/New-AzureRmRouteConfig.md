---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 356764CF-A860-432A-907A-9058CEB2BF8E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteConfig.md
ms.openlocfilehash: bb51d5bfb1ccc81aa10c7aecc4d7a255fc0f60d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589258"
---
# <span data-ttu-id="c07c1-101">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c07c1-101">New-AzureRmRouteConfig</span></span>

## <span data-ttu-id="c07c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c07c1-102">SYNOPSIS</span></span>
<span data-ttu-id="c07c1-103">Yol tablosu için bir yol oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c07c1-103">Creates a route for a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c07c1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c07c1-104">SYNTAX</span></span>

```
New-AzureRmRouteConfig -Name <String> [-AddressPrefix <String>] -NextHopType <String>
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c07c1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c07c1-105">DESCRIPTION</span></span>
<span data-ttu-id="c07c1-106">**Yeni-AzureRmRouteConfig** cmdlet 'i Azure yol tablosu için bir yol oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c07c1-106">The **New-AzureRmRouteConfig** cmdlet creates a route for an Azure route table.</span></span>

## <span data-ttu-id="c07c1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c07c1-107">EXAMPLES</span></span>

### <span data-ttu-id="c07c1-108">Örnek 1: yol oluşturma</span><span class="sxs-lookup"><span data-stu-id="c07c1-108">Example 1: Create a route</span></span>
```
PS C:\>$Route = New-AzureRmRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> $Route
Name              : Route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

<span data-ttu-id="c07c1-109">İlk komut Route07 adlı bir yol oluşturur ve $Route değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c07c1-109">The first command creates a route named Route07, and then stores it in the $Route variable.</span></span>
<span data-ttu-id="c07c1-110">Bu yol paketleri yerel sanal ağa iletir.</span><span class="sxs-lookup"><span data-stu-id="c07c1-110">This route forwards packets to the local virtual network.</span></span>

<span data-ttu-id="c07c1-111">İkinci komut yolun özelliklerini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="c07c1-111">The second command displays the properties of the route.</span></span>

## <span data-ttu-id="c07c1-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c07c1-112">PARAMETERS</span></span>

### <span data-ttu-id="c07c1-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c07c1-113">-AddressPrefix</span></span>
<span data-ttu-id="c07c1-114">Yolun uygulandığı hedefi sınıfsız etki alanları arası yönlendirme (CıDR) biçiminde belirtir.</span><span class="sxs-lookup"><span data-stu-id="c07c1-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="c07c1-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="c07c1-115">-Name</span></span>
<span data-ttu-id="c07c1-116">Yol için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="c07c1-116">Specifies a name for the route.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c07c1-117">-Nexthopıpaddress</span><span class="sxs-lookup"><span data-stu-id="c07c1-117">-NextHopIpAddress</span></span>
<span data-ttu-id="c07c1-118">AzureVirtual ağınıza eklediğiniz sanal bir gereç IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c07c1-118">Specifies the IP address of a virtual appliance that you add to your Azurevirtual network.</span></span>
<span data-ttu-id="c07c1-119">Bu yol paketleri bu adrese iletir.</span><span class="sxs-lookup"><span data-stu-id="c07c1-119">This route forwards packets to that address.</span></span>
<span data-ttu-id="c07c1-120">Bu parametreyi yalnızca *Nexthoptype* parametresi Için VirtualAppliance değerini belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="c07c1-120">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="c07c1-121">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="c07c1-121">-NextHopType</span></span>
<span data-ttu-id="c07c1-122">Bu yolun paketleri nasıl iletildiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c07c1-122">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="c07c1-123">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c07c1-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c07c1-124">İnternete.</span><span class="sxs-lookup"><span data-stu-id="c07c1-124">Internet.</span></span>
<span data-ttu-id="c07c1-125">Azure tarafından sağlanan varsayılan Internet ağ geçidi.</span><span class="sxs-lookup"><span data-stu-id="c07c1-125">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="c07c1-126">Yabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c07c1-126">None.</span></span>
<span data-ttu-id="c07c1-127">Bu değeri belirtirseniz, yol paketleri iletmez.</span><span class="sxs-lookup"><span data-stu-id="c07c1-127">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="c07c1-128">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="c07c1-128">VirtualAppliance.</span></span>
<span data-ttu-id="c07c1-129">Azure sanal ağınıza eklediğiniz sanal bir gereç.</span><span class="sxs-lookup"><span data-stu-id="c07c1-129">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="c07c1-130">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="c07c1-130">VirtualNetworkGateway.</span></span>
<span data-ttu-id="c07c1-131">Azure sunucudan sunucuya sanal özel ağ geçidi.</span><span class="sxs-lookup"><span data-stu-id="c07c1-131">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="c07c1-132">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="c07c1-132">VnetLocal.</span></span>
<span data-ttu-id="c07c1-133">Yerel sanal ağ.</span><span class="sxs-lookup"><span data-stu-id="c07c1-133">The local virtual network.</span></span>
<span data-ttu-id="c07c1-134">Aynı sanal ağda iki alt ağınız varsa 10.1.0.0/16 ve 10.2.0.0/16, diğer alt ağa iletilecek her alt ağ için VnetLocal değerini seçin.</span><span class="sxs-lookup"><span data-stu-id="c07c1-134">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Internet, None, VirtualAppliance, VirtualNetworkGateway, VnetLocal

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c07c1-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c07c1-135">-DefaultProfile</span></span>
<span data-ttu-id="c07c1-136">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c07c1-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c07c1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c07c1-137">CommonParameters</span></span>
<span data-ttu-id="c07c1-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c07c1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c07c1-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c07c1-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c07c1-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c07c1-140">INPUTS</span></span>

## <span data-ttu-id="c07c1-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c07c1-141">OUTPUTS</span></span>

### <span data-ttu-id="c07c1-142">Microsoft. Azure. Commands. Network. modeller. PSRoute</span><span class="sxs-lookup"><span data-stu-id="c07c1-142">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="c07c1-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c07c1-143">NOTES</span></span>

## <span data-ttu-id="c07c1-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c07c1-144">RELATED LINKS</span></span>

[<span data-ttu-id="c07c1-145">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c07c1-145">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="c07c1-146">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c07c1-146">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="c07c1-147">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c07c1-147">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="c07c1-148">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c07c1-148">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


