---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C868DFA4-8A9D-4108-B88B-ACD7F100A63C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteConfig.md
ms.openlocfilehash: 567796aaca3ac9d932319211f2b8ad1abbfdf161
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760695"
---
# <span data-ttu-id="95b77-101">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="95b77-101">Add-AzRouteConfig</span></span>

## <span data-ttu-id="95b77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95b77-102">SYNOPSIS</span></span>
<span data-ttu-id="95b77-103">Yol tablosuna bir yol ekler.</span><span class="sxs-lookup"><span data-stu-id="95b77-103">Adds a route to a route table.</span></span>

## <span data-ttu-id="95b77-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="95b77-104">SYNTAX</span></span>

```
Add-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="95b77-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="95b77-105">DESCRIPTION</span></span>
<span data-ttu-id="95b77-106">**Add-AzRouteConfig** cmdlet 'i Azure yol tablosuna bir yol ekler.</span><span class="sxs-lookup"><span data-stu-id="95b77-106">The **Add-AzRouteConfig** cmdlet adds a route to an Azure route table.</span></span>

## <span data-ttu-id="95b77-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="95b77-107">EXAMPLES</span></span>

### <span data-ttu-id="95b77-108">Örnek 1: yol tablosuna yol ekleme</span><span class="sxs-lookup"><span data-stu-id="95b77-108">Example 1: Add a route to a route table</span></span>
```
PS C:\>$RouteTable = Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
PS C:\> Add-AzRouteConfig -Name "Route13" -AddressPrefix 10.3.0.0/16 -NextHopType "VnetLocal" -RouteTable $RouteTable
```

<span data-ttu-id="95b77-109">İlk komut, Get-AzRouteTable cmdlet 'ini kullanarak RouteTable01 adlı bir yol tablosu alır.</span><span class="sxs-lookup"><span data-stu-id="95b77-109">The first command gets a route table named RouteTable01 by using the Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="95b77-110">Komut, tabloyu $RouteTable değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="95b77-110">The command stores the table in the $RouteTable variable.</span></span>
<span data-ttu-id="95b77-111">İkinci komut, $RouteTable depolanan yol tablosuna Route13 adlı bir yol ekler.</span><span class="sxs-lookup"><span data-stu-id="95b77-111">The second command adds a route named Route13 to the route table stored in $RouteTable.</span></span>
<span data-ttu-id="95b77-112">Bu yol paketleri yerel sanal ağa iletir.</span><span class="sxs-lookup"><span data-stu-id="95b77-112">This route forwards packets to the local virtual network.</span></span>

### <span data-ttu-id="95b77-113">Örnek 2: ardışık düzeni kullanarak bir yol tablosuna yol ekleme</span><span class="sxs-lookup"><span data-stu-id="95b77-113">Example 2: Add a route to a route table by using the pipeline</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Add-AzRouteConfig -Name "Route02" -AddressPrefix 10.2.0.0/16 -NextHopType VnetLocal | Set-AzRouteTable
Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/routetable01
Etag              : W/"f13e1bc8-d41f-44d0-882d-b8b5a1134f59"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "route02",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route02",
                        "AddressPrefix": "10.2.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "route13",
                        "Etag": null, 
                        "Id": null, 
                        "AddressPrefix": "10.3.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": null
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="95b77-114">Bu komut, **Get-AzRouteTable** kullanarak RouteTable01 adındaki yol tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="95b77-114">This command gets the route table named RouteTable01 by using **Get-AzRouteTable**.</span></span>
<span data-ttu-id="95b77-115">Komut, ardışık düzen işlecini kullanarak bu tabloyu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="95b77-115">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="95b77-116">Current cmdlet Route02 adlı yolu ekler ve sonucu, değişiklikleri yansıtmak üzere tabloyu güncelleştiren **-AzRouteTable** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="95b77-116">The current cmdlet adds the route named Route02, and then passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="95b77-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="95b77-117">PARAMETERS</span></span>

### <span data-ttu-id="95b77-118">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="95b77-118">-AddressPrefix</span></span>
<span data-ttu-id="95b77-119">Yolun uygulandığı hedefi sınıfsız etki alanları arası yönlendirme (CıDR) biçiminde belirtir.</span><span class="sxs-lookup"><span data-stu-id="95b77-119">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="95b77-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95b77-120">-DefaultProfile</span></span>
<span data-ttu-id="95b77-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="95b77-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95b77-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="95b77-122">-Name</span></span>
<span data-ttu-id="95b77-123">Yol tablosuna eklenecek yolun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="95b77-123">Specifies a name of the route to add to the route table.</span></span>

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

### <span data-ttu-id="95b77-124">-Nexthopıpaddress</span><span class="sxs-lookup"><span data-stu-id="95b77-124">-NextHopIpAddress</span></span>
<span data-ttu-id="95b77-125">Azure sanal ağınıza eklediğiniz sanal bir gereç IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="95b77-125">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="95b77-126">Bu yol paketleri bu adrese iletir.</span><span class="sxs-lookup"><span data-stu-id="95b77-126">This route forwards packets to that address.</span></span>
<span data-ttu-id="95b77-127">Bu parametreyi yalnızca *Nexthoptype* parametresi Için VirtualAppliance değerini belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="95b77-127">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="95b77-128">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="95b77-128">-NextHopType</span></span>
<span data-ttu-id="95b77-129">Bu yolun paketleri nasıl iletildiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="95b77-129">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="95b77-130">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="95b77-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="95b77-131">İnternete.</span><span class="sxs-lookup"><span data-stu-id="95b77-131">Internet.</span></span>
<span data-ttu-id="95b77-132">Azure tarafından sağlanan varsayılan Internet ağ geçidi.</span><span class="sxs-lookup"><span data-stu-id="95b77-132">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="95b77-133">Yabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="95b77-133">None.</span></span>
<span data-ttu-id="95b77-134">Bu değeri belirtirseniz, yol paketleri iletmez.</span><span class="sxs-lookup"><span data-stu-id="95b77-134">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="95b77-135">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="95b77-135">VirtualAppliance.</span></span>
<span data-ttu-id="95b77-136">Azure sanal ağınıza eklediğiniz sanal bir gereç.</span><span class="sxs-lookup"><span data-stu-id="95b77-136">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="95b77-137">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="95b77-137">VirtualNetworkGateway.</span></span>
<span data-ttu-id="95b77-138">Azure sunucudan sunucuya sanal özel ağ geçidi.</span><span class="sxs-lookup"><span data-stu-id="95b77-138">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="95b77-139">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="95b77-139">VnetLocal.</span></span>
<span data-ttu-id="95b77-140">Yerel sanal ağ.</span><span class="sxs-lookup"><span data-stu-id="95b77-140">The local virtual network.</span></span>
<span data-ttu-id="95b77-141">Aynı sanal ağda iki alt ağınız varsa 10.1.0.0/16 ve 10.2.0.0/16, diğer alt ağa iletilecek her alt ağ için VnetLocal değerini seçin.</span><span class="sxs-lookup"><span data-stu-id="95b77-141">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="95b77-142">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="95b77-142">-RouteTable</span></span>
<span data-ttu-id="95b77-143">Bu cmdlet 'in yol eklediği yol tablosunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="95b77-143">Specifies the route table to which this cmdlet adds a route.</span></span>

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

### <span data-ttu-id="95b77-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="95b77-144">-Confirm</span></span>
<span data-ttu-id="95b77-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="95b77-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95b77-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95b77-146">-WhatIf</span></span>
<span data-ttu-id="95b77-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="95b77-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="95b77-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="95b77-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95b77-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95b77-149">CommonParameters</span></span>
<span data-ttu-id="95b77-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="95b77-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95b77-151">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95b77-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95b77-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="95b77-152">INPUTS</span></span>

### <span data-ttu-id="95b77-153">Microsoft. Azure. Commands. Network. modeller. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="95b77-153">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="95b77-154">System. String</span><span class="sxs-lookup"><span data-stu-id="95b77-154">System.String</span></span>

## <span data-ttu-id="95b77-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="95b77-155">OUTPUTS</span></span>

### <span data-ttu-id="95b77-156">Microsoft. Azure. Commands. Network. modeller. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="95b77-156">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="95b77-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="95b77-157">NOTES</span></span>

## <span data-ttu-id="95b77-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="95b77-158">RELATED LINKS</span></span>

[<span data-ttu-id="95b77-159">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="95b77-159">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="95b77-160">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="95b77-160">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="95b77-161">Yeni-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="95b77-161">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="95b77-162">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="95b77-162">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="95b77-163">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="95b77-163">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)

[<span data-ttu-id="95b77-164">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="95b77-164">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


