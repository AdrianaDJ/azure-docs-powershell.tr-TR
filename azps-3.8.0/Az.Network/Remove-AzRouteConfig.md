---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 03285628-6BD3-4F2F-8129-E3CAE4C70EC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteConfig.md
ms.openlocfilehash: 57ef72599cdb0500a9903aeb09f67437fe5cc2f6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103993"
---
# <span data-ttu-id="94e4d-101">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="94e4d-101">Remove-AzRouteConfig</span></span>

## <span data-ttu-id="94e4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94e4d-102">SYNOPSIS</span></span>
<span data-ttu-id="94e4d-103">Yol tablosundan bir yol kaldırır.</span><span class="sxs-lookup"><span data-stu-id="94e4d-103">Removes a route from a route table.</span></span>

## <span data-ttu-id="94e4d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="94e4d-104">SYNTAX</span></span>

```
Remove-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94e4d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="94e4d-105">DESCRIPTION</span></span>
<span data-ttu-id="94e4d-106">**Remove-AzRouteConfig** cmdlet 'i Azure yol tablosundan bir yol kaldırır.</span><span class="sxs-lookup"><span data-stu-id="94e4d-106">The **Remove-AzRouteConfig** cmdlet removes a route from an Azure route table.</span></span>

## <span data-ttu-id="94e4d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="94e4d-107">EXAMPLES</span></span>

### <span data-ttu-id="94e4d-108">Örnek 1: rotayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="94e4d-108">Example 1: Remove a route</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Remove-AzRouteConfig -Name "Route02" | Set-AzRouteTable
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

<span data-ttu-id="94e4d-109">Bu komut, **Get-AzRouteTable** cmdlet 'Ini kullanarak RouteTable01 adlı yol tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="94e4d-109">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="94e4d-110">Komut, ardışık düzen işlecini kullanarak bu tabloyu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="94e4d-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="94e4d-111">Current cmdlet Route02 adlı yolu kaldırın ve sonucu, değişiklikleri yansıtmak üzere tabloyu güncelleştiren **-AzRouteTable** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="94e4d-111">The current cmdlet remove the route named Route02, and the passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>
<span data-ttu-id="94e4d-112">Tablo artık Route02 adlı yolu içermez.</span><span class="sxs-lookup"><span data-stu-id="94e4d-112">The table no longer contains the route named Route02.</span></span>

## <span data-ttu-id="94e4d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="94e4d-113">PARAMETERS</span></span>

### <span data-ttu-id="94e4d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94e4d-114">-DefaultProfile</span></span>
<span data-ttu-id="94e4d-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="94e4d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94e4d-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="94e4d-116">-Name</span></span>
<span data-ttu-id="94e4d-117">Bu cmdlet 'in kaldırıldığı yolun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="94e4d-117">Specifies the name of the route that this cmdlet removes.</span></span>

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

### <span data-ttu-id="94e4d-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="94e4d-118">-RouteTable</span></span>
<span data-ttu-id="94e4d-119">Bu cmdlet 'in sildiği rotayı içeren yol tablosunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="94e4d-119">Specifies the route table that contains the route that this cmdlet deletes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94e4d-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="94e4d-120">-Confirm</span></span>
<span data-ttu-id="94e4d-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="94e4d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94e4d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94e4d-122">-WhatIf</span></span>
<span data-ttu-id="94e4d-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="94e4d-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="94e4d-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="94e4d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94e4d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94e4d-125">CommonParameters</span></span>
<span data-ttu-id="94e4d-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="94e4d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94e4d-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94e4d-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94e4d-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="94e4d-128">INPUTS</span></span>

### <span data-ttu-id="94e4d-129">Microsoft. Azure. Commands. Network. modeller. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="94e4d-129">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="94e4d-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="94e4d-130">OUTPUTS</span></span>

### <span data-ttu-id="94e4d-131">Microsoft. Azure. Commands. Network. modeller. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="94e4d-131">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="94e4d-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="94e4d-132">NOTES</span></span>

## <span data-ttu-id="94e4d-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="94e4d-133">RELATED LINKS</span></span>

[<span data-ttu-id="94e4d-134">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="94e4d-134">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="94e4d-135">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="94e4d-135">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="94e4d-136">Yeni-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="94e4d-136">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="94e4d-137">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="94e4d-137">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


