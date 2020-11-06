---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6E967F9C-949E-4485-9B57-FC4F523D5DC9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteConfig.md
ms.openlocfilehash: a86e5346078bd1a8c9be924cdeac3b94fab907dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589227"
---
# <span data-ttu-id="cdc97-101">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="cdc97-101">Set-AzureRmRouteConfig</span></span>

## <span data-ttu-id="cdc97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdc97-102">SYNOPSIS</span></span>
<span data-ttu-id="cdc97-103">Bir yolun hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="cdc97-103">Sets the goal state for a route.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cdc97-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cdc97-104">SYNTAX</span></span>

```
Set-AzureRmRouteConfig -Name <String> -RouteTable <PSRouteTable> [-AddressPrefix <String>]
 -NextHopType <String> [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cdc97-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cdc97-105">DESCRIPTION</span></span>
<span data-ttu-id="cdc97-106">**Set-AzureRmRouteConfig** cmdlet 'ı bir Azure rotası için hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="cdc97-106">The **Set-AzureRmRouteConfig** cmdlet sets the goal state for an Azure route.</span></span>

## <span data-ttu-id="cdc97-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cdc97-107">EXAMPLES</span></span>

### <span data-ttu-id="cdc97-108">Örnek 1: Rotayı değiştirme</span><span class="sxs-lookup"><span data-stu-id="cdc97-108">Example 1: Modify a route</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Set-AzureRmRouteConfig -Name "Route02" -AddressPrefix 10.4.0.0/16 -NextHopType VnetLocal | Set-AzureRmRouteTable
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

<span data-ttu-id="cdc97-109">Bu komut, Get-AzureRmRouteTable cmdlet 'ini kullanarak RouteTable01 adındaki yol tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="cdc97-109">This command gets the route table named RouteTable01 by using the Get-AzureRmRouteTable cmdlet.</span></span>
<span data-ttu-id="cdc97-110">Komut, ardışık düzen işlecini kullanarak bu tabloyu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="cdc97-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="cdc97-111">Geçerli cmdlet Route02 adlı yolu değiştirir ve sonucu, değişiklikleri yansıtmak üzere tabloyu güncelleştiren **-AzureRmRouteTable** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="cdc97-111">The current cmdlet modifies the route named Route02, and then passes the result to the **Set-AzureRmRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="cdc97-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cdc97-112">PARAMETERS</span></span>

### <span data-ttu-id="cdc97-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="cdc97-113">-AddressPrefix</span></span>
<span data-ttu-id="cdc97-114">Yolun uygulandığı hedefi sınıfsız etki alanları arası yönlendirme (CıDR) biçiminde belirtir.</span><span class="sxs-lookup"><span data-stu-id="cdc97-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="cdc97-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="cdc97-115">-Name</span></span>
<span data-ttu-id="cdc97-116">Bu cmdlet 'in değiştirdiği yolun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cdc97-116">Specifies the name of the route that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="cdc97-117">-Nexthopıpaddress</span><span class="sxs-lookup"><span data-stu-id="cdc97-117">-NextHopIpAddress</span></span>
<span data-ttu-id="cdc97-118">Azure sanal ağınıza eklediğiniz sanal bir gereç IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cdc97-118">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="cdc97-119">Bu yol paketleri bu adrese iletir.</span><span class="sxs-lookup"><span data-stu-id="cdc97-119">This route forwards packets to that address.</span></span>
<span data-ttu-id="cdc97-120">Bu parametreyi yalnızca *Nexthoptype* parametresi Için VirtualAppliance değerini belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="cdc97-120">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="cdc97-121">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="cdc97-121">-NextHopType</span></span>
<span data-ttu-id="cdc97-122">Bu yolun paketleri nasıl iletildiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cdc97-122">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="cdc97-123">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="cdc97-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cdc97-124">İnternete.</span><span class="sxs-lookup"><span data-stu-id="cdc97-124">Internet.</span></span>
<span data-ttu-id="cdc97-125">Azure tarafından sağlanan varsayılan Internet ağ geçidi.</span><span class="sxs-lookup"><span data-stu-id="cdc97-125">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="cdc97-126">Yabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cdc97-126">None.</span></span>
<span data-ttu-id="cdc97-127">Bu değeri belirtirseniz, yol paketleri iletmez.</span><span class="sxs-lookup"><span data-stu-id="cdc97-127">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="cdc97-128">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="cdc97-128">VirtualAppliance.</span></span>
<span data-ttu-id="cdc97-129">Azure sanal ağınıza eklediğiniz sanal bir gereç.</span><span class="sxs-lookup"><span data-stu-id="cdc97-129">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="cdc97-130">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="cdc97-130">VirtualNetworkGateway.</span></span>
<span data-ttu-id="cdc97-131">Azureserver-to-sunucuya sanal özel ağ geçidi.</span><span class="sxs-lookup"><span data-stu-id="cdc97-131">An Azureserver-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="cdc97-132">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="cdc97-132">VnetLocal.</span></span>
<span data-ttu-id="cdc97-133">Yerel sanal ağ.</span><span class="sxs-lookup"><span data-stu-id="cdc97-133">The local virtual network.</span></span>
<span data-ttu-id="cdc97-134">Aynı sanal ağda iki alt ağınız varsa 10.1.0.0/16 ve 10.2.0.0/16, diğer alt ağa iletilecek her alt ağ için VnetLocal değerini seçin.</span><span class="sxs-lookup"><span data-stu-id="cdc97-134">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="cdc97-135">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="cdc97-135">-RouteTable</span></span>
<span data-ttu-id="cdc97-136">Bu yolun ilişkili olduğu yol tablosunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="cdc97-136">Specifies the route table with which this route is associated.</span></span>

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

### <span data-ttu-id="cdc97-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdc97-137">-DefaultProfile</span></span>
<span data-ttu-id="cdc97-138">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cdc97-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cdc97-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdc97-139">CommonParameters</span></span>
<span data-ttu-id="cdc97-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cdc97-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdc97-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdc97-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdc97-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cdc97-142">INPUTS</span></span>

### <span data-ttu-id="cdc97-143">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="cdc97-143">PSRouteTable</span></span>
<span data-ttu-id="cdc97-144">' RouteTable ' parametresi ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="cdc97-144">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="cdc97-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cdc97-145">OUTPUTS</span></span>

### <span data-ttu-id="cdc97-146">Microsoft. Azure. Commands. Network. modeller. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="cdc97-146">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="cdc97-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cdc97-147">NOTES</span></span>

## <span data-ttu-id="cdc97-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cdc97-148">RELATED LINKS</span></span>

[<span data-ttu-id="cdc97-149">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="cdc97-149">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="cdc97-150">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="cdc97-150">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="cdc97-151">Yeni-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="cdc97-151">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="cdc97-152">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="cdc97-152">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)


