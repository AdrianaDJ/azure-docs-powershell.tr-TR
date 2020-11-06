---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1CE2A30A-6DF8-4C4C-8348-C3C1CD4D0146
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteTable.md
ms.openlocfilehash: e525580d7384eef6b7fa7518fc6ddc5707a010ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590721"
---
# <span data-ttu-id="0d777-101">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="0d777-101">Set-AzureRmRouteTable</span></span>

## <span data-ttu-id="0d777-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d777-102">SYNOPSIS</span></span>
<span data-ttu-id="0d777-103">Yol tablosunun hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="0d777-103">Sets the goal state for a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d777-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0d777-104">SYNTAX</span></span>

```
Set-AzureRmRouteTable -RouteTable <PSRouteTable> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0d777-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0d777-105">DESCRIPTION</span></span>
<span data-ttu-id="0d777-106">**Set-AzureRmRouteTable** cmdlet 'ı bir Azure yol tablosunun hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="0d777-106">The **Set-AzureRmRouteTable** cmdlet sets the goal state for an Azure route table.</span></span>

## <span data-ttu-id="0d777-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0d777-107">EXAMPLES</span></span>

### <span data-ttu-id="0d777-108">Örnek 1: yol ekleme ve yol tablosunun hedef durumunu ayarlama</span><span class="sxs-lookup"><span data-stu-id="0d777-108">Example 1: Add a route and then set the goal state of the route table</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Add-AzureRmRouteConfig -Name "Route07" -AddressPrefix 10.2.0.0/16 -NextHopType "VnetLocal" | Set-AzureRmRouteTable
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

<span data-ttu-id="0d777-109">Bu komut, Get-AzureRmRouteTable cmdlet 'i kullanarak RouteTable01 adındaki yol tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="0d777-109">This command gets the route table named RouteTable01 by using Get-AzureRmRouteTable cmdlet.</span></span>
<span data-ttu-id="0d777-110">Komut, ardışık düzen işlecini kullanarak bu tabloyu Add-AzureRmRouteConfig cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="0d777-110">The command passes that table to the Add-AzureRmRouteConfig cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0d777-111">**Add-AzureRmRouteConfig** , Route07 adlı yolu ekler ve sonucu, değişiklikleri yansıtacak şekilde tabloyu güncelleştiren geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="0d777-111">**Add-AzureRmRouteConfig** adds the route named Route07, and then passes the result to the current cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="0d777-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0d777-112">PARAMETERS</span></span>

### <span data-ttu-id="0d777-113">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="0d777-113">-RouteTable</span></span>
<span data-ttu-id="0d777-114">Bu cmdlet 'in yol tablosunu ayarladığı hedef durumu temsil eden bir yol tablosu nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d777-114">Specifies a route table object that represents the goal state to which this cmdlet sets the route table.</span></span>

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

### <span data-ttu-id="0d777-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d777-115">-DefaultProfile</span></span>
<span data-ttu-id="0d777-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0d777-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d777-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d777-117">CommonParameters</span></span>
<span data-ttu-id="0d777-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0d777-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d777-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d777-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d777-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0d777-120">INPUTS</span></span>

### <span data-ttu-id="0d777-121">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="0d777-121">PSRouteTable</span></span>
<span data-ttu-id="0d777-122">' RouteTable ' parametresi ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="0d777-122">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="0d777-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0d777-123">OUTPUTS</span></span>

### <span data-ttu-id="0d777-124">Microsoft. Azure. Commands. Network. modeller. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="0d777-124">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="0d777-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0d777-125">NOTES</span></span>

## <span data-ttu-id="0d777-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0d777-126">RELATED LINKS</span></span>

[<span data-ttu-id="0d777-127">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="0d777-127">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="0d777-128">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="0d777-128">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="0d777-129">Yeni-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="0d777-129">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="0d777-130">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="0d777-130">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)


