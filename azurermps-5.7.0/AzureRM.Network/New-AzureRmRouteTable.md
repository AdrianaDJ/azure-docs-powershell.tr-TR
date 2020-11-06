---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6A278F91-C078-4DD4-82D0-2E4FA549A089
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteTable.md
ms.openlocfilehash: a311d64fbdb086ca1d52ab5a1db725e278c6cc16
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592950"
---
# <span data-ttu-id="519e2-101">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="519e2-101">New-AzureRmRouteTable</span></span>

## <span data-ttu-id="519e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="519e2-102">SYNOPSIS</span></span>
<span data-ttu-id="519e2-103">Yol tablosu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="519e2-103">Creates a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="519e2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="519e2-104">SYNTAX</span></span>

```
New-AzureRmRouteTable -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Route <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRoute]>]
 [-DisableBgpRoutePropagation] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="519e2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="519e2-105">DESCRIPTION</span></span>
<span data-ttu-id="519e2-106">**New-AzureRmRouteTable** cmdlet 'ı bir Azure yol tablosu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="519e2-106">The **New-AzureRmRouteTable** cmdlet creates an Azure route table.</span></span>

## <span data-ttu-id="519e2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="519e2-107">EXAMPLES</span></span>

### <span data-ttu-id="519e2-108">Örnek 1: yol içeren bir yol tablosu oluşturma</span><span class="sxs-lookup"><span data-stu-id="519e2-108">Example 1: Create a route table that contains a route</span></span>
```
PS C:\>$Route = New-AzureRmRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> New-AzureRmRouteTable -Name "RouteTable01" -ResourceGroupName "ResourceGroup11" -Location "EASTUS" -Route $Route
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

<span data-ttu-id="519e2-109">İlk komut, New-AzureRmRouteConfig cmdlet 'ini kullanarak Route07 adlı bir yol oluşturur ve $Route değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="519e2-109">The first command creates a route named Route07 by using the New-AzureRmRouteConfig cmdlet, and then stores it in the $Route variable.</span></span> <span data-ttu-id="519e2-110">Bu yol paketleri yerel sanal ağa iletir.</span><span class="sxs-lookup"><span data-stu-id="519e2-110">This route forwards packets to the local virtual network.</span></span>

<span data-ttu-id="519e2-111">İkinci komut RouteTable01 adlı bir yol tablosu oluşturur ve $Route depolanan yolu yeni tabloya ekler.</span><span class="sxs-lookup"><span data-stu-id="519e2-111">The second command creates a route table named RouteTable01, and adds the route stored in $Route to the new table.</span></span> <span data-ttu-id="519e2-112">Komut, tablonun ait olduğu kaynak grubunu ve tablonun konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="519e2-112">The command specifies the resource group to which the table belongs and the location for the table.</span></span>

## <span data-ttu-id="519e2-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="519e2-113">PARAMETERS</span></span>

### <span data-ttu-id="519e2-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="519e2-114">-AsJob</span></span>
<span data-ttu-id="519e2-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="519e2-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="519e2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="519e2-116">-DefaultProfile</span></span>
<span data-ttu-id="519e2-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="519e2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="519e2-118">-Disablebgprouteyayma</span><span class="sxs-lookup"><span data-stu-id="519e2-118">-DisableBgpRoutePropagation</span></span>
<span data-ttu-id="519e2-119">BGP Route otomatik yaymayı devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="519e2-119">Disable BGP Route auto propagation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="519e2-120">-Force</span><span class="sxs-lookup"><span data-stu-id="519e2-120">-Force</span></span>
<span data-ttu-id="519e2-121">Aynı ada sahip bir yol tablosu var olsa bile bu cmdlet 'in bir yol tablosu oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="519e2-121">Indicates that this cmdlet creates a route table even if a route table that has the same name already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="519e2-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="519e2-122">-Location</span></span>
<span data-ttu-id="519e2-123">Bu cmdlet 'in yol tablosu oluşturduğu Azure bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="519e2-123">Specifies the Azure region in which this cmdlet creates a route table.</span></span>
<span data-ttu-id="519e2-124">Daha fazla bilgi için bkz [.](https://azure.microsoft.com/en-us/regions/)</span><span class="sxs-lookup"><span data-stu-id="519e2-124">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions/).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="519e2-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="519e2-125">-Name</span></span>
<span data-ttu-id="519e2-126">Yol tablosu için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="519e2-126">Specifies a name for the route table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="519e2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="519e2-127">-ResourceGroupName</span></span>
<span data-ttu-id="519e2-128">Bu cmdlet 'in yol tablosu oluştururken kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="519e2-128">Specifies the name of the resource group in which this cmdlet creates a route table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="519e2-129">-Route</span><span class="sxs-lookup"><span data-stu-id="519e2-129">-Route</span></span>
<span data-ttu-id="519e2-130">Yol tablosuyla ilişkilendirilecek bir **yol** nesneleri dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="519e2-130">Specifies an array of **Route** objects to associate with the route table.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRoute]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="519e2-131">Etiketli</span><span class="sxs-lookup"><span data-stu-id="519e2-131">-Tag</span></span>
<span data-ttu-id="519e2-132">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="519e2-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="519e2-133">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="519e2-133">For example:</span></span>

<span data-ttu-id="519e2-134">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="519e2-134">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="519e2-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="519e2-135">-Confirm</span></span>
<span data-ttu-id="519e2-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="519e2-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="519e2-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="519e2-137">-WhatIf</span></span>
<span data-ttu-id="519e2-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="519e2-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="519e2-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="519e2-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="519e2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="519e2-140">CommonParameters</span></span>
<span data-ttu-id="519e2-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="519e2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="519e2-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="519e2-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="519e2-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="519e2-143">INPUTS</span></span>

### <span data-ttu-id="519e2-144">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="519e2-144">None</span></span>
<span data-ttu-id="519e2-145">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="519e2-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="519e2-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="519e2-146">OUTPUTS</span></span>

### <span data-ttu-id="519e2-147">Microsoft. Azure. Commands. Network. modeller. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="519e2-147">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="519e2-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="519e2-148">NOTES</span></span>

## <span data-ttu-id="519e2-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="519e2-149">RELATED LINKS</span></span>

[<span data-ttu-id="519e2-150">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="519e2-150">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="519e2-151">Yeni-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="519e2-151">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="519e2-152">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="519e2-152">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)

[<span data-ttu-id="519e2-153">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="519e2-153">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)
