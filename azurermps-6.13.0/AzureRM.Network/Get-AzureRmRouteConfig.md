---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteConfig.md
ms.openlocfilehash: dd23891bc56ac2eb8fce30708d9a72055a567bf3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589499"
---
# <span data-ttu-id="ba57d-101">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="ba57d-101">Get-AzureRmRouteConfig</span></span>

## <span data-ttu-id="ba57d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba57d-102">SYNOPSIS</span></span>
<span data-ttu-id="ba57d-103">Yol tablosundaki yolları alır.</span><span class="sxs-lookup"><span data-stu-id="ba57d-103">Gets routes from a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba57d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ba57d-104">SYNTAX</span></span>

```
Get-AzureRmRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba57d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ba57d-105">DESCRIPTION</span></span>
<span data-ttu-id="ba57d-106">**Get-AzureRmRouteConfig** cmdlet 'ı bir Azure yol tablosundan yollar alır.</span><span class="sxs-lookup"><span data-stu-id="ba57d-106">The **Get-AzureRmRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="ba57d-107">Bir yolu ada göre belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ba57d-107">You can specify a route by name.</span></span>

## <span data-ttu-id="ba57d-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ba57d-108">EXAMPLES</span></span>

### <span data-ttu-id="ba57d-109">Örnek 1: yol tablosu alma</span><span class="sxs-lookup"><span data-stu-id="ba57d-109">Example 1: Get a route table</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Get-AzureRmRouteConfig -Name "Route07"
Name              : route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

<span data-ttu-id="ba57d-110">Bu komut, **Get-AzureRmRouteTable** cmdlet 'Ini kullanarak RouteTable01 adındaki yol tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="ba57d-110">This command gets the route table named RouteTable01 by using the **Get-AzureRmRouteTable** cmdlet.</span></span>
<span data-ttu-id="ba57d-111">Komut, ardışık düzen işlecini kullanarak bu tabloyu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="ba57d-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ba57d-112">Current cmdlet, RouteTable01 adındaki yol tablosundaki Route07 adındaki rotayı alır.</span><span class="sxs-lookup"><span data-stu-id="ba57d-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="ba57d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ba57d-113">PARAMETERS</span></span>

### <span data-ttu-id="ba57d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba57d-114">-DefaultProfile</span></span>
<span data-ttu-id="ba57d-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ba57d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba57d-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="ba57d-116">-Name</span></span>
<span data-ttu-id="ba57d-117">Bu cmdlet 'in aldığı yolun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba57d-117">Specifies the name of the route that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ba57d-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="ba57d-118">-RouteTable</span></span>
<span data-ttu-id="ba57d-119">Bu cmdlet 'in yolları aldığı yol tablosunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ba57d-119">Specifies the route table from which this cmdlet gets routes.</span></span>

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

### <span data-ttu-id="ba57d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba57d-120">CommonParameters</span></span>
<span data-ttu-id="ba57d-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ba57d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba57d-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba57d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba57d-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ba57d-123">INPUTS</span></span>

### <span data-ttu-id="ba57d-124">Microsoft. Azure. Commands. Network. modeller. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="ba57d-124">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="ba57d-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ba57d-125">OUTPUTS</span></span>

### <span data-ttu-id="ba57d-126">Microsoft. Azure. Commands. Network. modeller. PSRoute</span><span class="sxs-lookup"><span data-stu-id="ba57d-126">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="ba57d-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ba57d-127">NOTES</span></span>

## <span data-ttu-id="ba57d-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ba57d-128">RELATED LINKS</span></span>

[<span data-ttu-id="ba57d-129">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="ba57d-129">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="ba57d-130">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="ba57d-130">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="ba57d-131">Yeni-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="ba57d-131">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="ba57d-132">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="ba57d-132">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="ba57d-133">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="ba57d-133">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


