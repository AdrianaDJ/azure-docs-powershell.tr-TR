---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azstaticroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzStaticRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzStaticRoute.md
ms.openlocfilehash: e4d9b8cd09aa1bf1528de1cd2179a76e7907e82b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109460"
---
# <span data-ttu-id="acd7a-101">New-AzStaticRoute</span><span class="sxs-lookup"><span data-stu-id="acd7a-101">New-AzStaticRoute</span></span>

## <span data-ttu-id="acd7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acd7a-102">SYNOPSIS</span></span>
<span data-ttu-id="acd7a-103">RoutingConfiguration nesnesine eklenebilecek bir StaticRoute nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="acd7a-103">Creates a StaticRoute object which can then be added to a RoutingConfiguration object.</span></span>

## <span data-ttu-id="acd7a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="acd7a-104">SYNTAX</span></span>

```powershell
New-AzStaticRoute -Name <String> -AddressPrefix <String[]> -NextHopIpAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acd7a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="acd7a-105">DESCRIPTION</span></span>
<span data-ttu-id="acd7a-106">StaticRoute nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="acd7a-106">Creates a StaticRoute object.</span></span>

## <span data-ttu-id="acd7a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="acd7a-107">EXAMPLES</span></span>

### <span data-ttu-id="acd7a-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="acd7a-108">Example 1</span></span>
```powershell
PS C:\> New-AzStaticRoute -Name "route1" -AddressPrefix @("10.20.0.0/16", "10.30.0.0/16") -NextHopIpAddress "10.90.0.5"

Name   AddressPrefixes              NextHopIpAddress
----   ---------------              ----------------
route1 {10.20.0.0/16, 10.30.0.0/16} 10.90.0.5
```

<span data-ttu-id="acd7a-109">Yukarıdaki komut, RoutingConfiguration nesnesine eklenebilen bir StaticRoute nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="acd7a-109">The above command will create a StaticRoute object which can then be added to a RoutingConfiguration object.</span></span>

## <span data-ttu-id="acd7a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="acd7a-110">PARAMETERS</span></span>

### <span data-ttu-id="acd7a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acd7a-111">-DefaultProfile</span></span>
<span data-ttu-id="acd7a-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="acd7a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acd7a-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="acd7a-113">-AddressPrefix</span></span>
<span data-ttu-id="acd7a-114">Adres önekleri listesi.</span><span class="sxs-lookup"><span data-stu-id="acd7a-114">List of address prefixes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acd7a-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="acd7a-115">-Name</span></span>
<span data-ttu-id="acd7a-116">Yol adı.</span><span class="sxs-lookup"><span data-stu-id="acd7a-116">The route name.</span></span>

```yaml
Type: String
Parameter Sets: (all)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acd7a-117">-Nexthopıpaddress</span><span class="sxs-lookup"><span data-stu-id="acd7a-117">-NextHopIpAddress</span></span>
<span data-ttu-id="acd7a-118">Sonraki atlama IP adresi.</span><span class="sxs-lookup"><span data-stu-id="acd7a-118">The next hop ip address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acd7a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acd7a-119">CommonParameters</span></span>
<span data-ttu-id="acd7a-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="acd7a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acd7a-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="acd7a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acd7a-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="acd7a-122">INPUTS</span></span>

### <span data-ttu-id="acd7a-123">System. String</span><span class="sxs-lookup"><span data-stu-id="acd7a-123">System.String</span></span>

## <span data-ttu-id="acd7a-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="acd7a-124">OUTPUTS</span></span>

### <span data-ttu-id="acd7a-125">Microsoft. Azure. Commands. Network. modeller. PSStaticRoute</span><span class="sxs-lookup"><span data-stu-id="acd7a-125">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span></span>

## <span data-ttu-id="acd7a-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="acd7a-126">NOTES</span></span>

## <span data-ttu-id="acd7a-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="acd7a-127">RELATED LINKS</span></span>

[<span data-ttu-id="acd7a-128">Yeni-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="acd7a-128">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
