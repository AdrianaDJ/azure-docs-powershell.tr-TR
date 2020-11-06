---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6A278F91-C078-4DD4-82D0-2E4FA549A089
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteTable.md
ms.openlocfilehash: f4ef683b65967fe694713b7990d23eb173f02163
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589249"
---
# <span data-ttu-id="e8550-101">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="e8550-101">New-AzureRmRouteTable</span></span>

## <span data-ttu-id="e8550-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8550-102">SYNOPSIS</span></span>
<span data-ttu-id="e8550-103">Yol tablosu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e8550-103">Creates a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8550-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e8550-104">SYNTAX</span></span>

```
New-AzureRmRouteTable -Name <String> -ResourceGroupName <String> -Location <String>
 [-Route <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRoute]>]
 [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e8550-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e8550-105">DESCRIPTION</span></span>
<span data-ttu-id="e8550-106">**New-AzureRmRouteTable** cmdlet 'ı bir Azure yol tablosu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e8550-106">The **New-AzureRmRouteTable** cmdlet creates an Azure route table.</span></span>

## <span data-ttu-id="e8550-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e8550-107">EXAMPLES</span></span>

### <span data-ttu-id="e8550-108">Örnek 1: yol içeren bir yol tablosu oluşturma</span><span class="sxs-lookup"><span data-stu-id="e8550-108">Example 1: Create a route table that contains a route</span></span>
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

<span data-ttu-id="e8550-109">İlk komut, New-AzureRmRouteConfig cmdlet 'ini kullanarak Route07 adlı bir yol oluşturur ve $Route değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="e8550-109">The first command creates a route named Route07 by using the New-AzureRmRouteConfig cmdlet, and then stores it in the $Route variable.</span></span> <span data-ttu-id="e8550-110">Bu yol paketleri yerel sanal ağa iletir.</span><span class="sxs-lookup"><span data-stu-id="e8550-110">This route forwards packets to the local virtual network.</span></span>

<span data-ttu-id="e8550-111">İkinci komut RouteTable01 adlı bir yol tablosu oluşturur ve $Route depolanan yolu yeni tabloya ekler.</span><span class="sxs-lookup"><span data-stu-id="e8550-111">The second command creates a route table named RouteTable01, and adds the route stored in $Route to the new table.</span></span> <span data-ttu-id="e8550-112">Komut, tablonun ait olduğu kaynak grubunu ve tablonun konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8550-112">The command specifies the resource group to which the table belongs and the location for the table.</span></span>

## <span data-ttu-id="e8550-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e8550-113">PARAMETERS</span></span>

### <span data-ttu-id="e8550-114">-Force</span><span class="sxs-lookup"><span data-stu-id="e8550-114">-Force</span></span>
<span data-ttu-id="e8550-115">Aynı ada sahip bir yol tablosu var olsa bile bu cmdlet 'in bir yol tablosu oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="e8550-115">Indicates that this cmdlet creates a route table even if a route table that has the same name already exists.</span></span>

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

### <span data-ttu-id="e8550-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="e8550-116">-Location</span></span>
<span data-ttu-id="e8550-117">Bu cmdlet 'in yol tablosu oluşturduğu Azure bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8550-117">Specifies the Azure region in which this cmdlet creates a route table.</span></span>
<span data-ttu-id="e8550-118">Daha fazla bilgi için bkz [.](https://azure.microsoft.com/en-us/regions/)</span><span class="sxs-lookup"><span data-stu-id="e8550-118">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions/).</span></span>

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

### <span data-ttu-id="e8550-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="e8550-119">-Name</span></span>
<span data-ttu-id="e8550-120">Yol tablosu için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8550-120">Specifies a name for the route table.</span></span>

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

### <span data-ttu-id="e8550-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8550-121">-ResourceGroupName</span></span>
<span data-ttu-id="e8550-122">Bu cmdlet 'in yol tablosu oluştururken kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8550-122">Specifies the name of the resource group in which this cmdlet creates a route table.</span></span>

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

### <span data-ttu-id="e8550-123">-Route</span><span class="sxs-lookup"><span data-stu-id="e8550-123">-Route</span></span>
<span data-ttu-id="e8550-124">Yol tablosuyla ilişkilendirilecek bir **yol** nesneleri dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8550-124">Specifies an array of **Route** objects to associate with the route table.</span></span>

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

### <span data-ttu-id="e8550-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="e8550-125">-Tag</span></span>
<span data-ttu-id="e8550-126">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="e8550-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e8550-127">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="e8550-127">For example:</span></span>

<span data-ttu-id="e8550-128">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="e8550-128">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e8550-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="e8550-129">-Confirm</span></span>
<span data-ttu-id="e8550-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e8550-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8550-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8550-131">-WhatIf</span></span>
<span data-ttu-id="e8550-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e8550-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8550-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e8550-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8550-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8550-134">-DefaultProfile</span></span>
<span data-ttu-id="e8550-135">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e8550-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8550-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8550-136">CommonParameters</span></span>
<span data-ttu-id="e8550-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e8550-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8550-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8550-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8550-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e8550-139">INPUTS</span></span>

## <span data-ttu-id="e8550-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e8550-140">OUTPUTS</span></span>

### <span data-ttu-id="e8550-141">Microsoft. Azure. Commands. Network. modeller. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="e8550-141">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="e8550-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e8550-142">NOTES</span></span>

## <span data-ttu-id="e8550-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e8550-143">RELATED LINKS</span></span>

[<span data-ttu-id="e8550-144">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="e8550-144">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="e8550-145">Yeni-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="e8550-145">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="e8550-146">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="e8550-146">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)

[<span data-ttu-id="e8550-147">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="e8550-147">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)
