---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6E967F9C-949E-4485-9B57-FC4F523D5DC9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteConfig.md
ms.openlocfilehash: d96f65586162eac330aa6309476dd00aea152920
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098564"
---
# <span data-ttu-id="d89ed-101">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="d89ed-101">Set-AzRouteConfig</span></span>

## <span data-ttu-id="d89ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d89ed-102">SYNOPSIS</span></span>
<span data-ttu-id="d89ed-103">Yol yapılandırmasını bir rota tablosu için güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d89ed-103">Updates a route configuration for a route table.</span></span>

## <span data-ttu-id="d89ed-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d89ed-104">SYNTAX</span></span>

```
Set-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d89ed-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d89ed-105">DESCRIPTION</span></span>
<span data-ttu-id="d89ed-106">**Set-AzRouteConfig** cmdlet 'i, yol için bir yol yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d89ed-106">The **Set-AzRouteConfig** cmdlet updates a route configuration for a route table.</span></span>

## <span data-ttu-id="d89ed-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d89ed-107">EXAMPLES</span></span>

### <span data-ttu-id="d89ed-108">Örnek 1: Rotayı değiştirme</span><span class="sxs-lookup"><span data-stu-id="d89ed-108">Example 1: Modify a route</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Set-AzRouteConfig -Name "Route02" -AddressPrefix 10.4.0.0/16 -NextHopType VnetLocal | Set-AzRouteTable
Name              : Routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/RouteTable01
Etag              : W/"58c2922e-9efe-4554-a457-956ef44bc718"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "Route07",
                        "Etag": "W/\"58c2922e-9efe-4554-a457-956ef44bc718\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/Routetable01/routes/Route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "route02",
                        "Etag": "W/\"58c2922e-9efe-4554-a457-956ef44bc718\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route02",
                        "AddressPrefix": "10.4.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="d89ed-109">Bu komut, Get-AzRouteTable cmdlet 'ini kullanarak RouteTable01 adındaki yol tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="d89ed-109">This command gets the route table named RouteTable01 by using the Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="d89ed-110">Komut, ardışık düzen işlecini kullanarak bu tabloyu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="d89ed-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d89ed-111">Geçerli cmdlet Route02 adlı yolu değiştirir ve sonucu, değişiklikleri yansıtmak üzere tabloyu güncelleştiren **-AzRouteTable** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="d89ed-111">The current cmdlet modifies the route named Route02, and then passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="d89ed-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d89ed-112">PARAMETERS</span></span>

### <span data-ttu-id="d89ed-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="d89ed-113">-AddressPrefix</span></span>
<span data-ttu-id="d89ed-114">Yolun uygulandığı hedefi sınıfsız etki alanları arası yönlendirme (CıDR) biçiminde belirtir.</span><span class="sxs-lookup"><span data-stu-id="d89ed-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="d89ed-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d89ed-115">-DefaultProfile</span></span>
<span data-ttu-id="d89ed-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d89ed-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d89ed-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="d89ed-117">-Name</span></span>
<span data-ttu-id="d89ed-118">Bu cmdlet 'in değiştirdiği yolun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d89ed-118">Specifies the name of the route that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d89ed-119">-Nexthopıpaddress</span><span class="sxs-lookup"><span data-stu-id="d89ed-119">-NextHopIpAddress</span></span>
<span data-ttu-id="d89ed-120">Azure sanal ağınıza eklediğiniz sanal bir gereç IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d89ed-120">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="d89ed-121">Bu yol paketleri bu adrese iletir.</span><span class="sxs-lookup"><span data-stu-id="d89ed-121">This route forwards packets to that address.</span></span>
<span data-ttu-id="d89ed-122">Bu parametreyi yalnızca *Nexthoptype* parametresi Için VirtualAppliance değerini belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="d89ed-122">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="d89ed-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="d89ed-123">-NextHopType</span></span>
<span data-ttu-id="d89ed-124">Bu yolun paketleri nasıl iletildiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d89ed-124">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="d89ed-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="d89ed-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d89ed-126">İnternete.</span><span class="sxs-lookup"><span data-stu-id="d89ed-126">Internet.</span></span>
<span data-ttu-id="d89ed-127">Azure tarafından sağlanan varsayılan Internet ağ geçidi.</span><span class="sxs-lookup"><span data-stu-id="d89ed-127">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="d89ed-128">Yabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d89ed-128">None.</span></span>
<span data-ttu-id="d89ed-129">Bu değeri belirtirseniz, yol paketleri iletmez.</span><span class="sxs-lookup"><span data-stu-id="d89ed-129">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="d89ed-130">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="d89ed-130">VirtualAppliance.</span></span>
<span data-ttu-id="d89ed-131">Azure sanal ağınıza eklediğiniz sanal bir gereç.</span><span class="sxs-lookup"><span data-stu-id="d89ed-131">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="d89ed-132">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="d89ed-132">VirtualNetworkGateway.</span></span>
<span data-ttu-id="d89ed-133">Azureserver-to-sunucuya sanal özel ağ geçidi.</span><span class="sxs-lookup"><span data-stu-id="d89ed-133">An Azureserver-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="d89ed-134">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="d89ed-134">VnetLocal.</span></span>
<span data-ttu-id="d89ed-135">Yerel sanal ağ.</span><span class="sxs-lookup"><span data-stu-id="d89ed-135">The local virtual network.</span></span>
<span data-ttu-id="d89ed-136">Aynı sanal ağda iki alt ağınız varsa 10.1.0.0/16 ve 10.2.0.0/16, diğer alt ağa iletilecek her alt ağ için VnetLocal değerini seçin.</span><span class="sxs-lookup"><span data-stu-id="d89ed-136">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="d89ed-137">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="d89ed-137">-RouteTable</span></span>
<span data-ttu-id="d89ed-138">Bu yolun ilişkili olduğu yol tablosunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d89ed-138">Specifies the route table with which this route is associated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d89ed-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="d89ed-139">-Confirm</span></span>
<span data-ttu-id="d89ed-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d89ed-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d89ed-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d89ed-141">-WhatIf</span></span>
<span data-ttu-id="d89ed-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d89ed-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d89ed-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d89ed-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d89ed-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d89ed-144">CommonParameters</span></span>
<span data-ttu-id="d89ed-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d89ed-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d89ed-146">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d89ed-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d89ed-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d89ed-147">INPUTS</span></span>

### <span data-ttu-id="d89ed-148">Microsoft. Azure. Commands. Network. modeller. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="d89ed-148">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="d89ed-149">System. String</span><span class="sxs-lookup"><span data-stu-id="d89ed-149">System.String</span></span>

## <span data-ttu-id="d89ed-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d89ed-150">OUTPUTS</span></span>

### <span data-ttu-id="d89ed-151">Microsoft. Azure. Commands. Network. modeller. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="d89ed-151">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="d89ed-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d89ed-152">NOTES</span></span>

## <span data-ttu-id="d89ed-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d89ed-153">RELATED LINKS</span></span>

[<span data-ttu-id="d89ed-154">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="d89ed-154">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="d89ed-155">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="d89ed-155">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="d89ed-156">Yeni-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="d89ed-156">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="d89ed-157">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="d89ed-157">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

