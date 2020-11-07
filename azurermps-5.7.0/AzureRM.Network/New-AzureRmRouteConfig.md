---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 356764CF-A860-432A-907A-9058CEB2BF8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteConfig.md
ms.openlocfilehash: 98e3bf7f76475b451d3a8f6509e311d9d861f691
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764431"
---
# <span data-ttu-id="40960-101">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="40960-101">New-AzureRmRouteConfig</span></span>

## <span data-ttu-id="40960-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40960-102">SYNOPSIS</span></span>
<span data-ttu-id="40960-103">Yol tablosu için bir yol oluşturur.</span><span class="sxs-lookup"><span data-stu-id="40960-103">Creates a route for a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40960-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="40960-104">SYNTAX</span></span>

```
New-AzureRmRouteConfig [-AddressPrefix <String>] [-NextHopType <String>] [-NextHopIpAddress <String>]
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40960-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="40960-105">DESCRIPTION</span></span>
<span data-ttu-id="40960-106">**Yeni-AzureRmRouteConfig** cmdlet 'i Azure yol tablosu için bir yol oluşturur.</span><span class="sxs-lookup"><span data-stu-id="40960-106">The **New-AzureRmRouteConfig** cmdlet creates a route for an Azure route table.</span></span>

## <span data-ttu-id="40960-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="40960-107">EXAMPLES</span></span>

### <span data-ttu-id="40960-108">Örnek 1: yol oluşturma</span><span class="sxs-lookup"><span data-stu-id="40960-108">Example 1: Create a route</span></span>
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

<span data-ttu-id="40960-109">İlk komut Route07 adlı bir yol oluşturur ve $Route değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="40960-109">The first command creates a route named Route07, and then stores it in the $Route variable.</span></span>
<span data-ttu-id="40960-110">Bu yol paketleri yerel sanal ağa iletir.</span><span class="sxs-lookup"><span data-stu-id="40960-110">This route forwards packets to the local virtual network.</span></span>

<span data-ttu-id="40960-111">İkinci komut yolun özelliklerini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="40960-111">The second command displays the properties of the route.</span></span>

## <span data-ttu-id="40960-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="40960-112">PARAMETERS</span></span>

### <span data-ttu-id="40960-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="40960-113">-AddressPrefix</span></span>
<span data-ttu-id="40960-114">Yolun uygulandığı hedefi sınıfsız etki alanları arası yönlendirme (CıDR) biçiminde belirtir.</span><span class="sxs-lookup"><span data-stu-id="40960-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40960-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40960-115">-DefaultProfile</span></span>
<span data-ttu-id="40960-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="40960-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40960-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="40960-117">-Name</span></span>
<span data-ttu-id="40960-118">Yol için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="40960-118">Specifies a name for the route.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40960-119">-Nexthopıpaddress</span><span class="sxs-lookup"><span data-stu-id="40960-119">-NextHopIpAddress</span></span>
<span data-ttu-id="40960-120">AzureVirtual ağınıza eklediğiniz sanal bir gereç IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="40960-120">Specifies the IP address of a virtual appliance that you add to your Azurevirtual network.</span></span>
<span data-ttu-id="40960-121">Bu yol paketleri bu adrese iletir.</span><span class="sxs-lookup"><span data-stu-id="40960-121">This route forwards packets to that address.</span></span>
<span data-ttu-id="40960-122">Bu parametreyi yalnızca *Nexthoptype* parametresi Için VirtualAppliance değerini belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="40960-122">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40960-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="40960-123">-NextHopType</span></span>
<span data-ttu-id="40960-124">Bu yolun paketleri nasıl iletildiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="40960-124">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="40960-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="40960-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="40960-126">İnternete.</span><span class="sxs-lookup"><span data-stu-id="40960-126">Internet.</span></span>
<span data-ttu-id="40960-127">Azure tarafından sağlanan varsayılan Internet ağ geçidi.</span><span class="sxs-lookup"><span data-stu-id="40960-127">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="40960-128">Yabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="40960-128">None.</span></span>
<span data-ttu-id="40960-129">Bu değeri belirtirseniz, yol paketleri iletmez.</span><span class="sxs-lookup"><span data-stu-id="40960-129">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="40960-130">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="40960-130">VirtualAppliance.</span></span>
<span data-ttu-id="40960-131">Azure sanal ağınıza eklediğiniz sanal bir gereç.</span><span class="sxs-lookup"><span data-stu-id="40960-131">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="40960-132">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="40960-132">VirtualNetworkGateway.</span></span>
<span data-ttu-id="40960-133">Azure sunucudan sunucuya sanal özel ağ geçidi.</span><span class="sxs-lookup"><span data-stu-id="40960-133">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="40960-134">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="40960-134">VnetLocal.</span></span>
<span data-ttu-id="40960-135">Yerel sanal ağ.</span><span class="sxs-lookup"><span data-stu-id="40960-135">The local virtual network.</span></span>
<span data-ttu-id="40960-136">Aynı sanal ağda iki alt ağınız varsa 10.1.0.0/16 ve 10.2.0.0/16, diğer alt ağa iletilecek her alt ağ için VnetLocal değerini seçin.</span><span class="sxs-lookup"><span data-stu-id="40960-136">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40960-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="40960-137">-Confirm</span></span>
<span data-ttu-id="40960-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="40960-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40960-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40960-139">-WhatIf</span></span>
<span data-ttu-id="40960-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="40960-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="40960-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="40960-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40960-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40960-142">CommonParameters</span></span>
<span data-ttu-id="40960-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="40960-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40960-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40960-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40960-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="40960-145">INPUTS</span></span>

### <span data-ttu-id="40960-146">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="40960-146">None</span></span>
<span data-ttu-id="40960-147">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="40960-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="40960-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="40960-148">OUTPUTS</span></span>

### <span data-ttu-id="40960-149">Microsoft. Azure. Commands. Network. modeller. PSRoute</span><span class="sxs-lookup"><span data-stu-id="40960-149">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="40960-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="40960-150">NOTES</span></span>

## <span data-ttu-id="40960-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="40960-151">RELATED LINKS</span></span>

[<span data-ttu-id="40960-152">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="40960-152">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="40960-153">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="40960-153">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="40960-154">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="40960-154">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="40960-155">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="40960-155">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


