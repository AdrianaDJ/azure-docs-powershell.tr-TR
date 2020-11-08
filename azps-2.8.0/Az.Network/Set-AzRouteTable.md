---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE2A30A-6DF8-4C4C-8348-C3C1CD4D0146
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteTable.md
ms.openlocfilehash: ba8fc7809bc9cea8ea34dbc4d15816134e8d7e13
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932743"
---
# <span data-ttu-id="c89aa-101">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="c89aa-101">Set-AzRouteTable</span></span>

## <span data-ttu-id="c89aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c89aa-102">SYNOPSIS</span></span>
<span data-ttu-id="c89aa-103">Yol tablosunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c89aa-103">Updates a route table.</span></span>

## <span data-ttu-id="c89aa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c89aa-104">SYNTAX</span></span>

```
Set-AzRouteTable -RouteTable <PSRouteTable> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c89aa-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c89aa-105">DESCRIPTION</span></span>
<span data-ttu-id="c89aa-106">**Set-AzRouteTable** cmdlet 'i bir yol tablosunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c89aa-106">The **Set-AzRouteTable** cmdlet updates a route table.</span></span>

## <span data-ttu-id="c89aa-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c89aa-107">EXAMPLES</span></span>

### <span data-ttu-id="c89aa-108">Örnek 1: yol yapılandırması ekleyerek yol tablosunu güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="c89aa-108">Example 1: Update a route table by adding route configuration to it</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Add-AzRouteConfig -Name "Route07" -AddressPrefix 10.2.0.0/16 -NextHopType "VnetLocal" | Set-AzRouteTable
Name              : RouteTable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/RouteTable01
Etag              : W/"f13e1bc8-d41f-44d0-882d-b8b5a1134f59"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "Route07",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/RouteTables/RouteTable01/routes/Route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "Route07",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/RouteTables/RouteTable01/routes/Route07",
                        "AddressPrefix": "10.2.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "Route13",
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

<span data-ttu-id="c89aa-109">Bu komut, Get-AzRouteTable cmdlet 'i kullanarak RouteTable01 adındaki yol tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="c89aa-109">This command gets the route table named RouteTable01 by using Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="c89aa-110">Komut, ardışık düzen işlecini kullanarak bu tabloyu Add-AzRouteConfig cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="c89aa-110">The command passes that table to the Add-AzRouteConfig cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c89aa-111">**Add-AzRouteConfig** , Route07 adlı yolu ekler ve sonucu, değişiklikleri yansıtacak şekilde tabloyu güncelleştiren geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="c89aa-111">**Add-AzRouteConfig** adds the route named Route07, and then passes the result to the current cmdlet, which updates the table to reflect your changes.</span></span>

### <span data-ttu-id="c89aa-112">Örnek 2: yol tablosunu değiştirme</span><span class="sxs-lookup"><span data-stu-id="c89aa-112">Example 2: Modify route table</span></span>

```
PS C:\> $rt = Get-AzRouteTable -ResourceGroupName "rgName" -Name "rtName"
PS C:\> $rt.DisableBgpRoutePropagation
False
PS C:\> $rt.DisableBgpRoutePropagation = $true
PS C:\> Set-AzRouteTable -RouteTable $rt
PS C:\> $rt = Get-AzRouteTable -ResourceGroupName "rgName" -Name "rtName"
PS C:\> $rt.DisableBgpRoutePropagation
True
```

<span data-ttu-id="c89aa-113">İlk komut rtName adındaki yol tablosunu alır ve $rt değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c89aa-113">The first command gets the route table named rtName and stores it in the $rt variable.</span></span>
<span data-ttu-id="c89aa-114">İkinci komut, Disablebgprouteyayma değerini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="c89aa-114">The second command displays the value of DisableBgpRoutePropagation.</span></span>
<span data-ttu-id="c89aa-115">Disablebgprouteyaymanın üçüncü komut güncelleştirme değeri.</span><span class="sxs-lookup"><span data-stu-id="c89aa-115">The third command updates value of DisableBgpRoutePropagation.</span></span>
<span data-ttu-id="c89aa-116">Dördüncü komut sunucudaki yol tablosunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c89aa-116">The fourth command updates route table on the server.</span></span>
<span data-ttu-id="c89aa-117">Beşinci komut, güncelleştirilmiş yol tablosunu alır ve $rt değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c89aa-117">The fifth command gets updated route table and stores it in the $rt variable.</span></span>
<span data-ttu-id="c89aa-118">Altıncı komut, Disablebgprouteyayma değerini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="c89aa-118">The sixth command displays the value of DisableBgpRoutePropagation.</span></span>

## <span data-ttu-id="c89aa-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c89aa-119">PARAMETERS</span></span>

### <span data-ttu-id="c89aa-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="c89aa-120">-AsJob</span></span>
<span data-ttu-id="c89aa-121">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="c89aa-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c89aa-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c89aa-122">-DefaultProfile</span></span>
<span data-ttu-id="c89aa-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c89aa-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c89aa-124">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="c89aa-124">-RouteTable</span></span>
<span data-ttu-id="c89aa-125">Yol tablosunun ayarlanması gereken durumu temsil eden bir yol tablosu nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="c89aa-125">Specifies a route table object representing the state to which the route table should be set.</span></span>

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

### <span data-ttu-id="c89aa-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="c89aa-126">-Confirm</span></span>
<span data-ttu-id="c89aa-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c89aa-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c89aa-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c89aa-128">-WhatIf</span></span>
<span data-ttu-id="c89aa-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c89aa-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c89aa-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c89aa-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c89aa-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c89aa-131">CommonParameters</span></span>
<span data-ttu-id="c89aa-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c89aa-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c89aa-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c89aa-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c89aa-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c89aa-134">INPUTS</span></span>

### <span data-ttu-id="c89aa-135">Microsoft. Azure. Commands. Network. modeller. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="c89aa-135">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="c89aa-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c89aa-136">OUTPUTS</span></span>

### <span data-ttu-id="c89aa-137">Microsoft. Azure. Commands. Network. modeller. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="c89aa-137">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="c89aa-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c89aa-138">NOTES</span></span>

## <span data-ttu-id="c89aa-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c89aa-139">RELATED LINKS</span></span>

[<span data-ttu-id="c89aa-140">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c89aa-140">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="c89aa-141">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="c89aa-141">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="c89aa-142">Yeni-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="c89aa-142">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="c89aa-143">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="c89aa-143">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)

