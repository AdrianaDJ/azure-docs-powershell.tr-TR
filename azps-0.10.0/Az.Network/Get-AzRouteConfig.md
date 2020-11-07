---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteConfig.md
ms.openlocfilehash: a5b80a15711314d5acc4f0288c1fd0304da772fc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935489"
---
# <span data-ttu-id="97b9d-101">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="97b9d-101">Get-AzRouteConfig</span></span>

## <span data-ttu-id="97b9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97b9d-102">SYNOPSIS</span></span>
<span data-ttu-id="97b9d-103">Yol tablosundaki yolları alır.</span><span class="sxs-lookup"><span data-stu-id="97b9d-103">Gets routes from a route table.</span></span>

## <span data-ttu-id="97b9d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="97b9d-104">SYNTAX</span></span>

```
Get-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="97b9d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="97b9d-105">DESCRIPTION</span></span>
<span data-ttu-id="97b9d-106">**Get-AzRouteConfig** cmdlet 'ı bir Azure yol tablosundan gelen yolları alır.</span><span class="sxs-lookup"><span data-stu-id="97b9d-106">The **Get-AzRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="97b9d-107">Bir yolu ada göre belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="97b9d-107">You can specify a route by name.</span></span>

## <span data-ttu-id="97b9d-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="97b9d-108">EXAMPLES</span></span>

### <span data-ttu-id="97b9d-109">Örnek 1: yol tablosu alma</span><span class="sxs-lookup"><span data-stu-id="97b9d-109">Example 1: Get a route table</span></span>
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

<span data-ttu-id="97b9d-110">Bu komut, **Get-AzRouteTable** cmdlet 'Ini kullanarak RouteTable01 adlı yol tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="97b9d-110">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="97b9d-111">Komut, ardışık düzen işlecini kullanarak bu tabloyu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="97b9d-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="97b9d-112">Current cmdlet, RouteTable01 adındaki yol tablosundaki Route07 adındaki rotayı alır.</span><span class="sxs-lookup"><span data-stu-id="97b9d-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="97b9d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="97b9d-113">PARAMETERS</span></span>

### <span data-ttu-id="97b9d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97b9d-114">-DefaultProfile</span></span>
<span data-ttu-id="97b9d-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="97b9d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97b9d-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="97b9d-116">-Name</span></span>
<span data-ttu-id="97b9d-117">Bu cmdlet 'in aldığı yolun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="97b9d-117">Specifies the name of the route that this cmdlet gets.</span></span>

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

### <span data-ttu-id="97b9d-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="97b9d-118">-RouteTable</span></span>
<span data-ttu-id="97b9d-119">Bu cmdlet 'in yolları aldığı yol tablosunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="97b9d-119">Specifies the route table from which this cmdlet gets routes.</span></span>

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

### <span data-ttu-id="97b9d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97b9d-120">CommonParameters</span></span>
<span data-ttu-id="97b9d-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="97b9d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97b9d-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97b9d-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97b9d-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="97b9d-123">INPUTS</span></span>

### <span data-ttu-id="97b9d-124">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="97b9d-124">PSRouteTable</span></span>
<span data-ttu-id="97b9d-125">' RouteTable ' parametresi ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="97b9d-125">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="97b9d-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="97b9d-126">OUTPUTS</span></span>

### <span data-ttu-id="97b9d-127">Microsoft. Azure. Commands. Network. modeller. PSRoute</span><span class="sxs-lookup"><span data-stu-id="97b9d-127">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="97b9d-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="97b9d-128">NOTES</span></span>

## <span data-ttu-id="97b9d-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="97b9d-129">RELATED LINKS</span></span>

[<span data-ttu-id="97b9d-130">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="97b9d-130">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="97b9d-131">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="97b9d-131">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="97b9d-132">Yeni-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="97b9d-132">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="97b9d-133">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="97b9d-133">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="97b9d-134">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="97b9d-134">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


