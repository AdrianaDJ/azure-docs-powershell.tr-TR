---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE2A30A-6DF8-4C4C-8348-C3C1CD4D0146
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzRouteTable.md
ms.openlocfilehash: 531c2724289e90f92bf14347518d53b6208be932
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936507"
---
# <span data-ttu-id="7baac-101">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="7baac-101">Set-AzRouteTable</span></span>

## <span data-ttu-id="7baac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7baac-102">SYNOPSIS</span></span>
<span data-ttu-id="7baac-103">Yol tablosunun hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7baac-103">Sets the goal state for a route table.</span></span>

## <span data-ttu-id="7baac-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7baac-104">SYNTAX</span></span>

```
Set-AzRouteTable -RouteTable <PSRouteTable> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7baac-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7baac-105">DESCRIPTION</span></span>
<span data-ttu-id="7baac-106">**Set-AzRouteTable** cmdlet 'ı bir Azure yol tablosunun hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7baac-106">The **Set-AzRouteTable** cmdlet sets the goal state for an Azure route table.</span></span>

## <span data-ttu-id="7baac-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7baac-107">EXAMPLES</span></span>

### <span data-ttu-id="7baac-108">Örnek 1: yol ekleme ve yol tablosunun hedef durumunu ayarlama</span><span class="sxs-lookup"><span data-stu-id="7baac-108">Example 1: Add a route and then set the goal state of the route table</span></span>
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

<span data-ttu-id="7baac-109">Bu komut, Get-AzRouteTable cmdlet 'i kullanarak RouteTable01 adındaki yol tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="7baac-109">This command gets the route table named RouteTable01 by using Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="7baac-110">Komut, ardışık düzen işlecini kullanarak bu tabloyu Add-AzRouteConfig cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="7baac-110">The command passes that table to the Add-AzRouteConfig cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7baac-111">**Add-AzRouteConfig** , Route07 adlı yolu ekler ve sonucu, değişiklikleri yansıtacak şekilde tabloyu güncelleştiren geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="7baac-111">**Add-AzRouteConfig** adds the route named Route07, and then passes the result to the current cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="7baac-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7baac-112">PARAMETERS</span></span>

### <span data-ttu-id="7baac-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="7baac-113">-AsJob</span></span>
<span data-ttu-id="7baac-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="7baac-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7baac-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7baac-115">-DefaultProfile</span></span>
<span data-ttu-id="7baac-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7baac-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7baac-117">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="7baac-117">-RouteTable</span></span>
<span data-ttu-id="7baac-118">Bu cmdlet 'in yol tablosunu ayarladığı hedef durumu temsil eden bir yol tablosu nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="7baac-118">Specifies a route table object that represents the goal state to which this cmdlet sets the route table.</span></span>

```yaml
Type: PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7baac-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="7baac-119">-Confirm</span></span>
<span data-ttu-id="7baac-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7baac-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7baac-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7baac-121">-WhatIf</span></span>
<span data-ttu-id="7baac-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7baac-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7baac-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7baac-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7baac-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7baac-124">CommonParameters</span></span>
<span data-ttu-id="7baac-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7baac-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7baac-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7baac-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7baac-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7baac-127">INPUTS</span></span>

### <span data-ttu-id="7baac-128">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="7baac-128">PSRouteTable</span></span>
<span data-ttu-id="7baac-129">' RouteTable ' parametresi ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="7baac-129">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="7baac-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7baac-130">OUTPUTS</span></span>

### <span data-ttu-id="7baac-131">Microsoft. Azure. Commands. Network. modeller. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="7baac-131">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="7baac-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7baac-132">NOTES</span></span>

## <span data-ttu-id="7baac-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7baac-133">RELATED LINKS</span></span>

[<span data-ttu-id="7baac-134">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="7baac-134">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="7baac-135">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="7baac-135">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="7baac-136">Yeni-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="7baac-136">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="7baac-137">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="7baac-137">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)

