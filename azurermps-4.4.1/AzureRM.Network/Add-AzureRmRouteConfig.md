---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C868DFA4-8A9D-4108-B88B-ACD7F100A63C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteConfig.md
ms.openlocfilehash: 7b28c50cfc53fee03d5715697a88e9356ea7664b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593079"
---
# <span data-ttu-id="c7a67-101">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c7a67-101">Add-AzureRmRouteConfig</span></span>

## <span data-ttu-id="c7a67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7a67-102">SYNOPSIS</span></span>
<span data-ttu-id="c7a67-103">Yol tablosuna bir yol ekler.</span><span class="sxs-lookup"><span data-stu-id="c7a67-103">Adds a route to a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7a67-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c7a67-104">SYNTAX</span></span>

```
Add-AzureRmRouteConfig -Name <String> -RouteTable <PSRouteTable> [-AddressPrefix <String>]
 -NextHopType <String> [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c7a67-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c7a67-105">DESCRIPTION</span></span>
<span data-ttu-id="c7a67-106">**Add-AzureRmRouteConfig** cmdlet 'i Azure yönlendirme tablosuna bir yol ekler.</span><span class="sxs-lookup"><span data-stu-id="c7a67-106">The **Add-AzureRmRouteConfig** cmdlet adds a route to an Azure route table.</span></span>

## <span data-ttu-id="c7a67-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c7a67-107">EXAMPLES</span></span>

### <span data-ttu-id="c7a67-108">Örnek 1: yol tablosuna yol ekleme</span><span class="sxs-lookup"><span data-stu-id="c7a67-108">Example 1: Add a route to a route table</span></span>
```
PS C:\>$RouteTable = Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
PS C:\> Add-AzureRmRouteConfig -Name "Route13" -AddressPrefix 10.3.0.0/16 -NextHopType "VnetLocal" -RouteTable $RouteTable
```

<span data-ttu-id="c7a67-109">İlk komut, Get-AzureRmRouteTable cmdlet 'ini kullanarak RouteTable01 adlı bir yol tablosu alır.</span><span class="sxs-lookup"><span data-stu-id="c7a67-109">The first command gets a route table named RouteTable01 by using the Get-AzureRmRouteTable cmdlet.</span></span>
<span data-ttu-id="c7a67-110">Komut, tabloyu $RouteTable değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c7a67-110">The command stores the table in the $RouteTable variable.</span></span>

<span data-ttu-id="c7a67-111">İkinci komut, $RouteTable depolanan yol tablosuna Route13 adlı bir yol ekler.</span><span class="sxs-lookup"><span data-stu-id="c7a67-111">The second command adds a route named Route13 to the route table stored in $RouteTable.</span></span>
<span data-ttu-id="c7a67-112">Bu yol paketleri yerel sanal ağa iletir.</span><span class="sxs-lookup"><span data-stu-id="c7a67-112">This route forwards packets to the local virtual network.</span></span>

### <span data-ttu-id="c7a67-113">Örnek 2: ardışık düzeni kullanarak bir yol tablosuna yol ekleme</span><span class="sxs-lookup"><span data-stu-id="c7a67-113">Example 2: Add a route to a route table by using the pipeline</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Add-AzureRmRouteConfig -Name "Route02" -AddressPrefix 10.2.0.0/16 -NextHopType VnetLocal | Set-AzureRmRouteTable
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

<span data-ttu-id="c7a67-114">Bu komut, **Get-AzureRmRouteTable** kullanarak RouteTable01 adlı yol tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="c7a67-114">This command gets the route table named RouteTable01 by using **Get-AzureRmRouteTable**.</span></span>
<span data-ttu-id="c7a67-115">Komut, ardışık düzen işlecini kullanarak bu tabloyu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="c7a67-115">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c7a67-116">Geçerli cmdlet Route02 adlı rotayı ekler ve sonucu, değişiklikleri yansıtmak üzere tabloyu güncelleştiren **-AzureRmRouteTable** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="c7a67-116">The current cmdlet adds the route named Route02, and then passes the result to the **Set-AzureRmRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="c7a67-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c7a67-117">PARAMETERS</span></span>

### <span data-ttu-id="c7a67-118">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c7a67-118">-AddressPrefix</span></span>
<span data-ttu-id="c7a67-119">Yolun uygulandığı hedefi sınıfsız etki alanları arası yönlendirme (CıDR) biçiminde belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7a67-119">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="c7a67-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="c7a67-120">-Name</span></span>
<span data-ttu-id="c7a67-121">Yol tablosuna eklenecek yolun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7a67-121">Specifies a name of the route to add to the route table.</span></span>

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

### <span data-ttu-id="c7a67-122">-Nexthopıpaddress</span><span class="sxs-lookup"><span data-stu-id="c7a67-122">-NextHopIpAddress</span></span>
<span data-ttu-id="c7a67-123">Azure sanal ağınıza eklediğiniz sanal bir gereç IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7a67-123">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="c7a67-124">Bu yol paketleri bu adrese iletir.</span><span class="sxs-lookup"><span data-stu-id="c7a67-124">This route forwards packets to that address.</span></span>
<span data-ttu-id="c7a67-125">Bu parametreyi yalnızca *Nexthoptype* parametresi Için VirtualAppliance değerini belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="c7a67-125">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="c7a67-126">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="c7a67-126">-NextHopType</span></span>
<span data-ttu-id="c7a67-127">Bu yolun paketleri nasıl iletildiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7a67-127">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="c7a67-128">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c7a67-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c7a67-129">İnternete.</span><span class="sxs-lookup"><span data-stu-id="c7a67-129">Internet.</span></span>
<span data-ttu-id="c7a67-130">Azure tarafından sağlanan varsayılan Internet ağ geçidi.</span><span class="sxs-lookup"><span data-stu-id="c7a67-130">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="c7a67-131">Yabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7a67-131">None.</span></span>
<span data-ttu-id="c7a67-132">Bu değeri belirtirseniz, yol paketleri iletmez.</span><span class="sxs-lookup"><span data-stu-id="c7a67-132">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="c7a67-133">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="c7a67-133">VirtualAppliance.</span></span>
<span data-ttu-id="c7a67-134">Azure sanal ağınıza eklediğiniz sanal bir gereç.</span><span class="sxs-lookup"><span data-stu-id="c7a67-134">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="c7a67-135">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="c7a67-135">VirtualNetworkGateway.</span></span>
<span data-ttu-id="c7a67-136">Azure sunucudan sunucuya sanal özel ağ geçidi.</span><span class="sxs-lookup"><span data-stu-id="c7a67-136">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="c7a67-137">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="c7a67-137">VnetLocal.</span></span>
<span data-ttu-id="c7a67-138">Yerel sanal ağ.</span><span class="sxs-lookup"><span data-stu-id="c7a67-138">The local virtual network.</span></span>
<span data-ttu-id="c7a67-139">Aynı sanal ağda iki alt ağınız varsa 10.1.0.0/16 ve 10.2.0.0/16, diğer alt ağa iletilecek her alt ağ için VnetLocal değerini seçin.</span><span class="sxs-lookup"><span data-stu-id="c7a67-139">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="c7a67-140">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="c7a67-140">-RouteTable</span></span>
<span data-ttu-id="c7a67-141">Bu cmdlet 'in yol eklediği yol tablosunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7a67-141">Specifies the route table to which this cmdlet adds a route.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7a67-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7a67-142">-DefaultProfile</span></span>
<span data-ttu-id="c7a67-143">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c7a67-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7a67-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7a67-144">CommonParameters</span></span>
<span data-ttu-id="c7a67-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c7a67-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7a67-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7a67-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7a67-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c7a67-147">INPUTS</span></span>

### <span data-ttu-id="c7a67-148">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="c7a67-148">PSRouteTable</span></span>
<span data-ttu-id="c7a67-149">' RouteTable ' parametresi ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="c7a67-149">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="c7a67-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c7a67-150">OUTPUTS</span></span>

### <span data-ttu-id="c7a67-151">Microsoft. Azure. Commands. Network. modeller. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="c7a67-151">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="c7a67-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c7a67-152">NOTES</span></span>

## <span data-ttu-id="c7a67-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c7a67-153">RELATED LINKS</span></span>

[<span data-ttu-id="c7a67-154">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c7a67-154">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="c7a67-155">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="c7a67-155">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="c7a67-156">Yeni-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c7a67-156">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="c7a67-157">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c7a67-157">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="c7a67-158">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c7a67-158">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)

[<span data-ttu-id="c7a67-159">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="c7a67-159">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)


