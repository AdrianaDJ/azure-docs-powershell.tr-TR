---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 356764CF-A860-432A-907A-9058CEB2BF8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteConfig.md
ms.openlocfilehash: 83f6f44af262719c9ed9fb5cae818bc6b70d5c2b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098729"
---
# <span data-ttu-id="a0043-101">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="a0043-101">New-AzRouteConfig</span></span>

## <span data-ttu-id="a0043-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0043-102">SYNOPSIS</span></span>
<span data-ttu-id="a0043-103">Yol tablosu için bir yol oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a0043-103">Creates a route for a route table.</span></span>

## <span data-ttu-id="a0043-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a0043-104">SYNTAX</span></span>

```
New-AzRouteConfig [-Name <String>] [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a0043-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a0043-105">DESCRIPTION</span></span>
<span data-ttu-id="a0043-106">**New-AzRouteConfig** cmdlet 'i Azure yol tablosu için bir yol oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a0043-106">The **New-AzRouteConfig** cmdlet creates a route for an Azure route table.</span></span>

## <span data-ttu-id="a0043-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a0043-107">EXAMPLES</span></span>

### <span data-ttu-id="a0043-108">Örnek 1: yol oluşturma</span><span class="sxs-lookup"><span data-stu-id="a0043-108">Example 1: Create a route</span></span>
```
PS C:\>$Route = New-AzRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> $Route
Name              : Route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

<span data-ttu-id="a0043-109">İlk komut Route07 adlı bir yol oluşturur ve $Route değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a0043-109">The first command creates a route named Route07, and then stores it in the $Route variable.</span></span>
<span data-ttu-id="a0043-110">Bu yol paketleri yerel sanal ağa iletir.</span><span class="sxs-lookup"><span data-stu-id="a0043-110">This route forwards packets to the local virtual network.</span></span>
<span data-ttu-id="a0043-111">İkinci komut yolun özelliklerini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="a0043-111">The second command displays the properties of the route.</span></span>

## <span data-ttu-id="a0043-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a0043-112">PARAMETERS</span></span>

### <span data-ttu-id="a0043-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a0043-113">-AddressPrefix</span></span>
<span data-ttu-id="a0043-114">Yolun uygulandığı hedefi sınıfsız etki alanları arası yönlendirme (CıDR) biçiminde belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0043-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0043-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0043-115">-DefaultProfile</span></span>
<span data-ttu-id="a0043-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a0043-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0043-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="a0043-117">-Name</span></span>
<span data-ttu-id="a0043-118">Yol için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0043-118">Specifies a name for the route.</span></span>

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

### <span data-ttu-id="a0043-119">-Nexthopıpaddress</span><span class="sxs-lookup"><span data-stu-id="a0043-119">-NextHopIpAddress</span></span>
<span data-ttu-id="a0043-120">AzureVirtual ağınıza eklediğiniz sanal bir gereç IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0043-120">Specifies the IP address of a virtual appliance that you add to your Azurevirtual network.</span></span>
<span data-ttu-id="a0043-121">Bu yol paketleri bu adrese iletir.</span><span class="sxs-lookup"><span data-stu-id="a0043-121">This route forwards packets to that address.</span></span>
<span data-ttu-id="a0043-122">Bu parametreyi yalnızca *Nexthoptype* parametresi Için VirtualAppliance değerini belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="a0043-122">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0043-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="a0043-123">-NextHopType</span></span>
<span data-ttu-id="a0043-124">Bu yolun paketleri nasıl iletildiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0043-124">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="a0043-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="a0043-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a0043-126">İnternete.</span><span class="sxs-lookup"><span data-stu-id="a0043-126">Internet.</span></span>
<span data-ttu-id="a0043-127">Azure tarafından sağlanan varsayılan Internet ağ geçidi.</span><span class="sxs-lookup"><span data-stu-id="a0043-127">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="a0043-128">Yabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a0043-128">None.</span></span>
<span data-ttu-id="a0043-129">Bu değeri belirtirseniz, yol paketleri iletmez.</span><span class="sxs-lookup"><span data-stu-id="a0043-129">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="a0043-130">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="a0043-130">VirtualAppliance.</span></span>
<span data-ttu-id="a0043-131">Azure sanal ağınıza eklediğiniz sanal bir gereç.</span><span class="sxs-lookup"><span data-stu-id="a0043-131">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="a0043-132">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="a0043-132">VirtualNetworkGateway.</span></span>
<span data-ttu-id="a0043-133">Azure sunucudan sunucuya sanal özel ağ geçidi.</span><span class="sxs-lookup"><span data-stu-id="a0043-133">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="a0043-134">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="a0043-134">VnetLocal.</span></span>
<span data-ttu-id="a0043-135">Yerel sanal ağ.</span><span class="sxs-lookup"><span data-stu-id="a0043-135">The local virtual network.</span></span>
<span data-ttu-id="a0043-136">Aynı sanal ağda iki alt ağınız varsa 10.1.0.0/16 ve 10.2.0.0/16, diğer alt ağa iletilecek her alt ağ için VnetLocal değerini seçin.</span><span class="sxs-lookup"><span data-stu-id="a0043-136">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0043-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="a0043-137">-Confirm</span></span>
<span data-ttu-id="a0043-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a0043-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0043-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0043-139">-WhatIf</span></span>
<span data-ttu-id="a0043-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a0043-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a0043-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a0043-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0043-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0043-142">CommonParameters</span></span>
<span data-ttu-id="a0043-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a0043-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0043-144">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0043-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0043-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a0043-145">INPUTS</span></span>

### <span data-ttu-id="a0043-146">System. String</span><span class="sxs-lookup"><span data-stu-id="a0043-146">System.String</span></span>

## <span data-ttu-id="a0043-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a0043-147">OUTPUTS</span></span>

### <span data-ttu-id="a0043-148">Microsoft. Azure. Commands. Network. modeller. PSRoute</span><span class="sxs-lookup"><span data-stu-id="a0043-148">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="a0043-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a0043-149">NOTES</span></span>

## <span data-ttu-id="a0043-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a0043-150">RELATED LINKS</span></span>

[<span data-ttu-id="a0043-151">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="a0043-151">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="a0043-152">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="a0043-152">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="a0043-153">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="a0043-153">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="a0043-154">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="a0043-154">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)

