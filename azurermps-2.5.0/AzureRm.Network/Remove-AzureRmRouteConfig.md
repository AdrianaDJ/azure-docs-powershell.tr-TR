---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 03285628-6BD3-4F2F-8129-E3CAE4C70EC8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermrouteconfig
schema: 2.0.0
ms.openlocfilehash: c5117fc961a93395991055eff2d404b5b8c6c051
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940033"
---
# <span data-ttu-id="2de80-101">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="2de80-101">Remove-AzureRmRouteConfig</span></span>

## <span data-ttu-id="2de80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2de80-102">SYNOPSIS</span></span>
<span data-ttu-id="2de80-103">Yol tablosundan bir yol kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2de80-103">Removes a route from a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2de80-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2de80-104">SYNTAX</span></span>

```
Remove-AzureRmRouteConfig -RouteTable <PSRouteTable> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2de80-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2de80-105">DESCRIPTION</span></span>
<span data-ttu-id="2de80-106">**Remove-AzureRmRouteConfig** cmdlet 'i Azure yol tablosundan bir yol kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2de80-106">The **Remove-AzureRmRouteConfig** cmdlet removes a route from an Azure route table.</span></span>

## <span data-ttu-id="2de80-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2de80-107">EXAMPLES</span></span>

### <span data-ttu-id="2de80-108">Örnek 1: rotayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="2de80-108">Example 1: Remove a route</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Remove-AzureRmRouteConfig -Name "Route02" | Set-AzureRmRouteTable
Name              : RouteTable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/RouteTable01
Etag              : W/"47099b62-60ec-4bc1-b87b-fad56cb8bed1"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "Route07",
                        "Etag": "W/\"47099b62-60ec-4bc1-b87b-fad56cb8bed1\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/RouteTable01/routes/Route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="2de80-109">Bu komut, **Get-AzureRmRouteTable** cmdlet 'Ini kullanarak RouteTable01 adındaki yol tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="2de80-109">This command gets the route table named RouteTable01 by using the **Get-AzureRmRouteTable** cmdlet.</span></span>
<span data-ttu-id="2de80-110">Komut, ardışık düzen işlecini kullanarak bu tabloyu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="2de80-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2de80-111">Current cmdlet Route02 adlı yolu kaldırın ve sonucu, değişiklikleri yansıtmak üzere tabloyu güncelleştiren **-AzureRmRouteTable** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="2de80-111">The current cmdlet remove the route named Route02, and the passes the result to the **Set-AzureRmRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>
<span data-ttu-id="2de80-112">Tablo artık Route02 adlı yolu içermez.</span><span class="sxs-lookup"><span data-stu-id="2de80-112">The table no longer contains the route named Route02.</span></span>

## <span data-ttu-id="2de80-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2de80-113">PARAMETERS</span></span>

### <span data-ttu-id="2de80-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2de80-114">-DefaultProfile</span></span>
<span data-ttu-id="2de80-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2de80-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2de80-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="2de80-116">-Name</span></span>
<span data-ttu-id="2de80-117">Bu cmdlet 'in kaldırıldığı yolun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2de80-117">Specifies the name of the route that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2de80-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="2de80-118">-RouteTable</span></span>
<span data-ttu-id="2de80-119">Bu cmdlet 'in sildiği rotayı içeren yol tablosunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2de80-119">Specifies the route table that contains the route that this cmdlet deletes.</span></span>

```yaml
Type: PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2de80-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="2de80-120">-Confirm</span></span>
<span data-ttu-id="2de80-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2de80-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2de80-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2de80-122">-WhatIf</span></span>
<span data-ttu-id="2de80-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2de80-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2de80-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2de80-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2de80-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2de80-125">CommonParameters</span></span>
<span data-ttu-id="2de80-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2de80-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2de80-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2de80-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2de80-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2de80-128">INPUTS</span></span>

### <span data-ttu-id="2de80-129">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="2de80-129">PSRouteTable</span></span>
<span data-ttu-id="2de80-130">' RouteTable ' parametresi ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="2de80-130">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="2de80-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2de80-131">OUTPUTS</span></span>

### <span data-ttu-id="2de80-132">Microsoft. Azure. Commands. Network. modeller. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="2de80-132">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="2de80-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2de80-133">NOTES</span></span>

## <span data-ttu-id="2de80-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2de80-134">RELATED LINKS</span></span>

[<span data-ttu-id="2de80-135">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="2de80-135">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="2de80-136">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="2de80-136">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="2de80-137">Yeni-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="2de80-137">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="2de80-138">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="2de80-138">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


