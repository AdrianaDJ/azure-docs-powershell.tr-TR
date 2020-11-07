---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 03285628-6BD3-4F2F-8129-E3CAE4C70EC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzRouteConfig.md
ms.openlocfilehash: fe079282d85b5aea8ebedcf69504fbb0e3dab04b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936614"
---
# <span data-ttu-id="43095-101">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="43095-101">Remove-AzRouteConfig</span></span>

## <span data-ttu-id="43095-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43095-102">SYNOPSIS</span></span>
<span data-ttu-id="43095-103">Yol tablosundan bir yol kaldırır.</span><span class="sxs-lookup"><span data-stu-id="43095-103">Removes a route from a route table.</span></span>

## <span data-ttu-id="43095-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="43095-104">SYNTAX</span></span>

```
Remove-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43095-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="43095-105">DESCRIPTION</span></span>
<span data-ttu-id="43095-106">**Remove-AzRouteConfig** cmdlet 'i Azure yol tablosundan bir yol kaldırır.</span><span class="sxs-lookup"><span data-stu-id="43095-106">The **Remove-AzRouteConfig** cmdlet removes a route from an Azure route table.</span></span>

## <span data-ttu-id="43095-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="43095-107">EXAMPLES</span></span>

### <span data-ttu-id="43095-108">Örnek 1: rotayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="43095-108">Example 1: Remove a route</span></span>
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

<span data-ttu-id="43095-109">Bu komut, **Get-AzRouteTable** cmdlet 'Ini kullanarak RouteTable01 adlı yol tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="43095-109">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="43095-110">Komut, ardışık düzen işlecini kullanarak bu tabloyu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="43095-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="43095-111">Current cmdlet Route02 adlı yolu kaldırın ve sonucu, değişiklikleri yansıtmak üzere tabloyu güncelleştiren **-AzRouteTable** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="43095-111">The current cmdlet remove the route named Route02, and the passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>
<span data-ttu-id="43095-112">Tablo artık Route02 adlı yolu içermez.</span><span class="sxs-lookup"><span data-stu-id="43095-112">The table no longer contains the route named Route02.</span></span>

## <span data-ttu-id="43095-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="43095-113">PARAMETERS</span></span>

### <span data-ttu-id="43095-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43095-114">-DefaultProfile</span></span>
<span data-ttu-id="43095-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="43095-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43095-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="43095-116">-Name</span></span>
<span data-ttu-id="43095-117">Bu cmdlet 'in kaldırıldığı yolun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="43095-117">Specifies the name of the route that this cmdlet removes.</span></span>

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

### <span data-ttu-id="43095-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="43095-118">-RouteTable</span></span>
<span data-ttu-id="43095-119">Bu cmdlet 'in sildiği rotayı içeren yol tablosunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="43095-119">Specifies the route table that contains the route that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="43095-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="43095-120">-Confirm</span></span>
<span data-ttu-id="43095-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="43095-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43095-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43095-122">-WhatIf</span></span>
<span data-ttu-id="43095-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="43095-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="43095-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="43095-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43095-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43095-125">CommonParameters</span></span>
<span data-ttu-id="43095-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="43095-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43095-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43095-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43095-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="43095-128">INPUTS</span></span>

### <span data-ttu-id="43095-129">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="43095-129">PSRouteTable</span></span>
<span data-ttu-id="43095-130">' RouteTable ' parametresi ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="43095-130">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="43095-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="43095-131">OUTPUTS</span></span>

### <span data-ttu-id="43095-132">Microsoft. Azure. Commands. Network. modeller. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="43095-132">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="43095-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="43095-133">NOTES</span></span>

## <span data-ttu-id="43095-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="43095-134">RELATED LINKS</span></span>

[<span data-ttu-id="43095-135">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="43095-135">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="43095-136">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="43095-136">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="43095-137">Yeni-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="43095-137">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="43095-138">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="43095-138">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


