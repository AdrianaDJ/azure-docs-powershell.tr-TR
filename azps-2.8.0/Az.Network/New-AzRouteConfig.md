---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 356764CF-A860-432A-907A-9058CEB2BF8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteConfig.md
ms.openlocfilehash: 07b7d0decd196fba9cbf0a813af4d252d01dfc8c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918211"
---
# <span data-ttu-id="65632-101">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="65632-101">New-AzRouteConfig</span></span>

## <span data-ttu-id="65632-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65632-102">SYNOPSIS</span></span>
<span data-ttu-id="65632-103">Yol tablosu için bir yol oluşturur.</span><span class="sxs-lookup"><span data-stu-id="65632-103">Creates a route for a route table.</span></span>

## <span data-ttu-id="65632-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="65632-104">SYNTAX</span></span>

```
New-AzRouteConfig [-Name <String>] [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="65632-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="65632-105">DESCRIPTION</span></span>
<span data-ttu-id="65632-106">**New-AzRouteConfig** cmdlet 'i Azure yol tablosu için bir yol oluşturur.</span><span class="sxs-lookup"><span data-stu-id="65632-106">The **New-AzRouteConfig** cmdlet creates a route for an Azure route table.</span></span>

## <span data-ttu-id="65632-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="65632-107">EXAMPLES</span></span>

### <span data-ttu-id="65632-108">Örnek 1: yol oluşturma</span><span class="sxs-lookup"><span data-stu-id="65632-108">Example 1: Create a route</span></span>
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

<span data-ttu-id="65632-109">İlk komut Route07 adlı bir yol oluşturur ve $Route değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="65632-109">The first command creates a route named Route07, and then stores it in the $Route variable.</span></span>
<span data-ttu-id="65632-110">Bu yol paketleri yerel sanal ağa iletir.</span><span class="sxs-lookup"><span data-stu-id="65632-110">This route forwards packets to the local virtual network.</span></span>
<span data-ttu-id="65632-111">İkinci komut yolun özelliklerini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="65632-111">The second command displays the properties of the route.</span></span>

## <span data-ttu-id="65632-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="65632-112">PARAMETERS</span></span>

### <span data-ttu-id="65632-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="65632-113">-AddressPrefix</span></span>
<span data-ttu-id="65632-114">Yolun uygulandığı hedefi sınıfsız etki alanları arası yönlendirme (CıDR) biçiminde belirtir.</span><span class="sxs-lookup"><span data-stu-id="65632-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="65632-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65632-115">-DefaultProfile</span></span>
<span data-ttu-id="65632-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="65632-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65632-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="65632-117">-Name</span></span>
<span data-ttu-id="65632-118">Yol için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="65632-118">Specifies a name for the route.</span></span>

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

### <span data-ttu-id="65632-119">-Nexthopıpaddress</span><span class="sxs-lookup"><span data-stu-id="65632-119">-NextHopIpAddress</span></span>
<span data-ttu-id="65632-120">AzureVirtual ağınıza eklediğiniz sanal bir gereç IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="65632-120">Specifies the IP address of a virtual appliance that you add to your Azurevirtual network.</span></span>
<span data-ttu-id="65632-121">Bu yol paketleri bu adrese iletir.</span><span class="sxs-lookup"><span data-stu-id="65632-121">This route forwards packets to that address.</span></span>
<span data-ttu-id="65632-122">Bu parametreyi yalnızca *Nexthoptype* parametresi Için VirtualAppliance değerini belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="65632-122">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="65632-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="65632-123">-NextHopType</span></span>
<span data-ttu-id="65632-124">Bu yolun paketleri nasıl iletildiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="65632-124">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="65632-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="65632-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="65632-126">İnternete.</span><span class="sxs-lookup"><span data-stu-id="65632-126">Internet.</span></span>
<span data-ttu-id="65632-127">Azure tarafından sağlanan varsayılan Internet ağ geçidi.</span><span class="sxs-lookup"><span data-stu-id="65632-127">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="65632-128">Yabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="65632-128">None.</span></span>
<span data-ttu-id="65632-129">Bu değeri belirtirseniz, yol paketleri iletmez.</span><span class="sxs-lookup"><span data-stu-id="65632-129">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="65632-130">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="65632-130">VirtualAppliance.</span></span>
<span data-ttu-id="65632-131">Azure sanal ağınıza eklediğiniz sanal bir gereç.</span><span class="sxs-lookup"><span data-stu-id="65632-131">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="65632-132">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="65632-132">VirtualNetworkGateway.</span></span>
<span data-ttu-id="65632-133">Azure sunucudan sunucuya sanal özel ağ geçidi.</span><span class="sxs-lookup"><span data-stu-id="65632-133">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="65632-134">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="65632-134">VnetLocal.</span></span>
<span data-ttu-id="65632-135">Yerel sanal ağ.</span><span class="sxs-lookup"><span data-stu-id="65632-135">The local virtual network.</span></span>
<span data-ttu-id="65632-136">Aynı sanal ağda iki alt ağınız varsa 10.1.0.0/16 ve 10.2.0.0/16, diğer alt ağa iletilecek her alt ağ için VnetLocal değerini seçin.</span><span class="sxs-lookup"><span data-stu-id="65632-136">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="65632-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="65632-137">-Confirm</span></span>
<span data-ttu-id="65632-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="65632-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65632-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65632-139">-WhatIf</span></span>
<span data-ttu-id="65632-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="65632-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="65632-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="65632-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65632-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65632-142">CommonParameters</span></span>
<span data-ttu-id="65632-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="65632-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65632-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65632-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65632-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="65632-145">INPUTS</span></span>

### <span data-ttu-id="65632-146">System. String</span><span class="sxs-lookup"><span data-stu-id="65632-146">System.String</span></span>

## <span data-ttu-id="65632-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="65632-147">OUTPUTS</span></span>

### <span data-ttu-id="65632-148">Microsoft. Azure. Commands. Network. modeller. PSRoute</span><span class="sxs-lookup"><span data-stu-id="65632-148">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="65632-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="65632-149">NOTES</span></span>

## <span data-ttu-id="65632-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="65632-150">RELATED LINKS</span></span>

[<span data-ttu-id="65632-151">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="65632-151">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="65632-152">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="65632-152">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="65632-153">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="65632-153">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="65632-154">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="65632-154">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


