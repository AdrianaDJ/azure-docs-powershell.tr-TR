---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6A278F91-C078-4DD4-82D0-2E4FA549A089
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermroutetable
schema: 2.0.0
ms.openlocfilehash: 9ba23a33e82e003413172240264ef8485b12d4e0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939909"
---
# <span data-ttu-id="a6d10-101">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="a6d10-101">New-AzureRmRouteTable</span></span>

## <span data-ttu-id="a6d10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6d10-102">SYNOPSIS</span></span>
<span data-ttu-id="a6d10-103">Yol tablosu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a6d10-103">Creates a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6d10-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a6d10-104">SYNTAX</span></span>

```
New-AzureRmRouteTable -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Route <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRoute]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6d10-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a6d10-105">DESCRIPTION</span></span>
<span data-ttu-id="a6d10-106">**New-AzureRmRouteTable** cmdlet 'ı bir Azure yol tablosu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a6d10-106">The **New-AzureRmRouteTable** cmdlet creates an Azure route table.</span></span>

## <span data-ttu-id="a6d10-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a6d10-107">EXAMPLES</span></span>

### <span data-ttu-id="a6d10-108">Örnek 1: yol içeren bir yol tablosu oluşturma</span><span class="sxs-lookup"><span data-stu-id="a6d10-108">Example 1: Create a route table that contains a route</span></span>
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

<span data-ttu-id="a6d10-109">İlk komut, New-AzureRmRouteConfig cmdlet 'ini kullanarak Route07 adlı bir yol oluşturur ve $Route değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a6d10-109">The first command creates a route named Route07 by using the New-AzureRmRouteConfig cmdlet, and then stores it in the $Route variable.</span></span> <span data-ttu-id="a6d10-110">Bu yol paketleri yerel sanal ağa iletir.</span><span class="sxs-lookup"><span data-stu-id="a6d10-110">This route forwards packets to the local virtual network.</span></span>

<span data-ttu-id="a6d10-111">İkinci komut RouteTable01 adlı bir yol tablosu oluşturur ve $Route depolanan yolu yeni tabloya ekler.</span><span class="sxs-lookup"><span data-stu-id="a6d10-111">The second command creates a route table named RouteTable01, and adds the route stored in $Route to the new table.</span></span> <span data-ttu-id="a6d10-112">Komut, tablonun ait olduğu kaynak grubunu ve tablonun konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6d10-112">The command specifies the resource group to which the table belongs and the location for the table.</span></span>

## <span data-ttu-id="a6d10-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a6d10-113">PARAMETERS</span></span>

### <span data-ttu-id="a6d10-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="a6d10-114">-AsJob</span></span>
<span data-ttu-id="a6d10-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="a6d10-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a6d10-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6d10-116">-DefaultProfile</span></span>
<span data-ttu-id="a6d10-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a6d10-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6d10-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a6d10-118">-Force</span></span>
<span data-ttu-id="a6d10-119">Aynı ada sahip bir yol tablosu var olsa bile bu cmdlet 'in bir yol tablosu oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="a6d10-119">Indicates that this cmdlet creates a route table even if a route table that has the same name already exists.</span></span>

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

### <span data-ttu-id="a6d10-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="a6d10-120">-Location</span></span>
<span data-ttu-id="a6d10-121">Bu cmdlet 'in yol tablosu oluşturduğu Azure bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6d10-121">Specifies the Azure region in which this cmdlet creates a route table.</span></span>
<span data-ttu-id="a6d10-122">Daha fazla bilgi için bkz [.](https://azure.microsoft.com/en-us/regions/)</span><span class="sxs-lookup"><span data-stu-id="a6d10-122">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions/).</span></span>

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

### <span data-ttu-id="a6d10-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="a6d10-123">-Name</span></span>
<span data-ttu-id="a6d10-124">Yol tablosu için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6d10-124">Specifies a name for the route table.</span></span>

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

### <span data-ttu-id="a6d10-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6d10-125">-ResourceGroupName</span></span>
<span data-ttu-id="a6d10-126">Bu cmdlet 'in yol tablosu oluştururken kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6d10-126">Specifies the name of the resource group in which this cmdlet creates a route table.</span></span>

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

### <span data-ttu-id="a6d10-127">-Route</span><span class="sxs-lookup"><span data-stu-id="a6d10-127">-Route</span></span>
<span data-ttu-id="a6d10-128">Yol tablosuyla ilişkilendirilecek bir **yol** nesneleri dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6d10-128">Specifies an array of **Route** objects to associate with the route table.</span></span>

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

### <span data-ttu-id="a6d10-129">Etiketli</span><span class="sxs-lookup"><span data-stu-id="a6d10-129">-Tag</span></span>
<span data-ttu-id="a6d10-130">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="a6d10-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a6d10-131">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="a6d10-131">For example:</span></span>

<span data-ttu-id="a6d10-132">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="a6d10-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a6d10-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="a6d10-133">-Confirm</span></span>
<span data-ttu-id="a6d10-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a6d10-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6d10-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6d10-135">-WhatIf</span></span>
<span data-ttu-id="a6d10-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a6d10-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6d10-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a6d10-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6d10-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6d10-138">CommonParameters</span></span>
<span data-ttu-id="a6d10-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a6d10-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6d10-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6d10-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6d10-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a6d10-141">INPUTS</span></span>

## <span data-ttu-id="a6d10-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a6d10-142">OUTPUTS</span></span>

### <span data-ttu-id="a6d10-143">Microsoft. Azure. Commands. Network. modeller. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="a6d10-143">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="a6d10-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a6d10-144">NOTES</span></span>

## <span data-ttu-id="a6d10-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a6d10-145">RELATED LINKS</span></span>

[<span data-ttu-id="a6d10-146">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="a6d10-146">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="a6d10-147">Yeni-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="a6d10-147">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="a6d10-148">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="a6d10-148">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)

[<span data-ttu-id="a6d10-149">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="a6d10-149">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)
