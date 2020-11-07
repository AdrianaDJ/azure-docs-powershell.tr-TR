---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteConfig.md
ms.openlocfilehash: 195ff0f8da8af5408f9b7ad2bffdd35507b10d1b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93931718"
---
# <span data-ttu-id="d032a-101">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="d032a-101">Get-AzRouteConfig</span></span>

## <span data-ttu-id="d032a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d032a-102">SYNOPSIS</span></span>
<span data-ttu-id="d032a-103">Yol tablosundaki yolları alır.</span><span class="sxs-lookup"><span data-stu-id="d032a-103">Gets routes from a route table.</span></span>

## <span data-ttu-id="d032a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d032a-104">SYNTAX</span></span>

```
Get-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d032a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d032a-105">DESCRIPTION</span></span>
<span data-ttu-id="d032a-106">**Get-AzRouteConfig** cmdlet 'ı bir Azure yol tablosundan gelen yolları alır.</span><span class="sxs-lookup"><span data-stu-id="d032a-106">The **Get-AzRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="d032a-107">Bir yolu ada göre belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d032a-107">You can specify a route by name.</span></span>

## <span data-ttu-id="d032a-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d032a-108">EXAMPLES</span></span>

### <span data-ttu-id="d032a-109">Örnek 1: yol tablosu alma</span><span class="sxs-lookup"><span data-stu-id="d032a-109">Example 1: Get a route table</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Get-AzRouteConfig -Name "Route07"
Name              : route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

<span data-ttu-id="d032a-110">Bu komut, **Get-AzRouteTable** cmdlet 'Ini kullanarak RouteTable01 adlı yol tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="d032a-110">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="d032a-111">Komut, ardışık düzen işlecini kullanarak bu tabloyu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="d032a-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d032a-112">Current cmdlet, RouteTable01 adındaki yol tablosundaki Route07 adındaki rotayı alır.</span><span class="sxs-lookup"><span data-stu-id="d032a-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="d032a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d032a-113">PARAMETERS</span></span>

### <span data-ttu-id="d032a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d032a-114">-DefaultProfile</span></span>
<span data-ttu-id="d032a-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d032a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d032a-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="d032a-116">-Name</span></span>
<span data-ttu-id="d032a-117">Bu cmdlet 'in aldığı yolun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d032a-117">Specifies the name of the route that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d032a-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="d032a-118">-RouteTable</span></span>
<span data-ttu-id="d032a-119">Bu cmdlet 'in yolları aldığı yol tablosunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d032a-119">Specifies the route table from which this cmdlet gets routes.</span></span>

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

### <span data-ttu-id="d032a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d032a-120">CommonParameters</span></span>
<span data-ttu-id="d032a-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d032a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d032a-122">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d032a-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d032a-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d032a-123">INPUTS</span></span>

### <span data-ttu-id="d032a-124">Microsoft. Azure. Commands. Network. modeller. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="d032a-124">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="d032a-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d032a-125">OUTPUTS</span></span>

### <span data-ttu-id="d032a-126">Microsoft. Azure. Commands. Network. modeller. PSRoute</span><span class="sxs-lookup"><span data-stu-id="d032a-126">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="d032a-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d032a-127">NOTES</span></span>

## <span data-ttu-id="d032a-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d032a-128">RELATED LINKS</span></span>

[<span data-ttu-id="d032a-129">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="d032a-129">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="d032a-130">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="d032a-130">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="d032a-131">Yeni-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="d032a-131">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="d032a-132">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="d032a-132">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="d032a-133">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="d032a-133">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


