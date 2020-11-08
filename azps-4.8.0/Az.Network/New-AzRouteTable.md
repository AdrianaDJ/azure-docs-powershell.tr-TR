---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6A278F91-C078-4DD4-82D0-2E4FA549A089
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteTable.md
ms.openlocfilehash: e7e0b58dfd4ac925110c5f666bc7c360cc222983
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108896"
---
# <span data-ttu-id="51460-101">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="51460-101">New-AzRouteTable</span></span>

## <span data-ttu-id="51460-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51460-102">SYNOPSIS</span></span>
<span data-ttu-id="51460-103">Yol tablosu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="51460-103">Creates a route table.</span></span>

## <span data-ttu-id="51460-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="51460-104">SYNTAX</span></span>

```
New-AzRouteTable -ResourceGroupName <String> -Name <String> [-DisableBgpRoutePropagation] -Location <String>
 [-Tag <Hashtable>] [-Route <PSRoute[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51460-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="51460-105">DESCRIPTION</span></span>
<span data-ttu-id="51460-106">**New-AzRouteTable** cmdlet 'ı bir Azure yol tablosu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="51460-106">The **New-AzRouteTable** cmdlet creates an Azure route table.</span></span>

## <span data-ttu-id="51460-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="51460-107">EXAMPLES</span></span>

### <span data-ttu-id="51460-108">Örnek 1: yol içeren bir yol tablosu oluşturma</span><span class="sxs-lookup"><span data-stu-id="51460-108">Example 1: Create a route table that contains a route</span></span>
```
PS C:\>$Route = New-AzRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> New-AzRouteTable -Name "RouteTable01" -ResourceGroupName "ResourceGroup11" -Location "EASTUS" -Route $Route
Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/myroutetable
Etag              : W/"db5f4e12-3f34-465b-92dd-0ab3bf6fc274"
ProvisioningState : Succeeded
Tags              :
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"db5f4e12-3f34-465b-92dd-0ab3bf6fc274\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null,
                        "ProvisioningState": "Succeeded"
                      }
                    ]
Subnets           : []
```

<span data-ttu-id="51460-109">İlk komut, New-AzRouteConfig cmdlet 'ini kullanarak Route07 adlı bir yol oluşturur ve $Route değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="51460-109">The first command creates a route named Route07 by using the New-AzRouteConfig cmdlet, and then stores it in the $Route variable.</span></span> <span data-ttu-id="51460-110">Bu yol paketleri yerel sanal ağa iletir.</span><span class="sxs-lookup"><span data-stu-id="51460-110">This route forwards packets to the local virtual network.</span></span>
<span data-ttu-id="51460-111">İkinci komut RouteTable01 adlı bir yol tablosu oluşturur ve $Route depolanan yolu yeni tabloya ekler.</span><span class="sxs-lookup"><span data-stu-id="51460-111">The second command creates a route table named RouteTable01, and adds the route stored in $Route to the new table.</span></span> <span data-ttu-id="51460-112">Komut, tablonun ait olduğu kaynak grubunu ve tablonun konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="51460-112">The command specifies the resource group to which the table belongs and the location for the table.</span></span>

## <span data-ttu-id="51460-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="51460-113">PARAMETERS</span></span>

### <span data-ttu-id="51460-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="51460-114">-AsJob</span></span>
<span data-ttu-id="51460-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="51460-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51460-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51460-116">-DefaultProfile</span></span>
<span data-ttu-id="51460-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="51460-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51460-118">-Disablebgprouteyayma</span><span class="sxs-lookup"><span data-stu-id="51460-118">-DisableBgpRoutePropagation</span></span>
<span data-ttu-id="51460-119">BGP Route otomatik yaymayı devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="51460-119">Disable BGP Route auto propagation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51460-120">-Force</span><span class="sxs-lookup"><span data-stu-id="51460-120">-Force</span></span>
<span data-ttu-id="51460-121">Aynı ada sahip bir yol tablosu var olsa bile bu cmdlet 'in bir yol tablosu oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="51460-121">Indicates that this cmdlet creates a route table even if a route table that has the same name already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51460-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="51460-122">-Location</span></span>
<span data-ttu-id="51460-123">Bu cmdlet 'in yol tablosu oluşturduğu Azure bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="51460-123">Specifies the Azure region in which this cmdlet creates a route table.</span></span>
<span data-ttu-id="51460-124">Daha fazla bilgi için bkz [.](http://azure.microsoft.com/en-us/regions/)</span><span class="sxs-lookup"><span data-stu-id="51460-124">For more information, see [Azure Regions](http://azure.microsoft.com/en-us/regions/).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51460-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="51460-125">-Name</span></span>
<span data-ttu-id="51460-126">Yol tablosu için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="51460-126">Specifies a name for the route table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51460-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51460-127">-ResourceGroupName</span></span>
<span data-ttu-id="51460-128">Bu cmdlet 'in yol tablosu oluştururken kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="51460-128">Specifies the name of the resource group in which this cmdlet creates a route table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51460-129">-Route</span><span class="sxs-lookup"><span data-stu-id="51460-129">-Route</span></span>
<span data-ttu-id="51460-130">Yol tablosuyla ilişkilendirilecek bir **yol** nesneleri dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="51460-130">Specifies an array of **Route** objects to associate with the route table.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRoute[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51460-131">Etiketli</span><span class="sxs-lookup"><span data-stu-id="51460-131">-Tag</span></span>
<span data-ttu-id="51460-132">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="51460-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="51460-133">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="51460-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51460-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="51460-134">-Confirm</span></span>
<span data-ttu-id="51460-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="51460-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51460-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51460-136">-WhatIf</span></span>
<span data-ttu-id="51460-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="51460-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51460-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="51460-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51460-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51460-139">CommonParameters</span></span>
<span data-ttu-id="51460-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="51460-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51460-141">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51460-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51460-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="51460-142">INPUTS</span></span>

### <span data-ttu-id="51460-143">System. String</span><span class="sxs-lookup"><span data-stu-id="51460-143">System.String</span></span>

### <span data-ttu-id="51460-144">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="51460-144">System.Collections.Hashtable</span></span>

### <span data-ttu-id="51460-145">Microsoft. Azure. Commands. Network. modeller. PSRoute []</span><span class="sxs-lookup"><span data-stu-id="51460-145">Microsoft.Azure.Commands.Network.Models.PSRoute[]</span></span>

## <span data-ttu-id="51460-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="51460-146">OUTPUTS</span></span>

### <span data-ttu-id="51460-147">Microsoft. Azure. Commands. Network. modeller. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="51460-147">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="51460-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="51460-148">NOTES</span></span>

## <span data-ttu-id="51460-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="51460-149">RELATED LINKS</span></span>

[<span data-ttu-id="51460-150">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="51460-150">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="51460-151">Yeni-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="51460-151">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="51460-152">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="51460-152">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)

[<span data-ttu-id="51460-153">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="51460-153">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)
