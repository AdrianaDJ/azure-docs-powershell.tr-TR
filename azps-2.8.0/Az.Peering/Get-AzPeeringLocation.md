---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringLocation.md
ms.openlocfilehash: cc8e0c5e4ce47b3157d5518ce1e5bc6b9919ff41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932862"
---
# <span data-ttu-id="2dfdf-101">Get-AzPeeringLocation</span><span class="sxs-lookup"><span data-stu-id="2dfdf-101">Get-AzPeeringLocation</span></span>

## <span data-ttu-id="2dfdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2dfdf-102">SYNOPSIS</span></span>
<span data-ttu-id="2dfdf-103">Microsoft tarafından sunulan eşleme konumlarını alır</span><span class="sxs-lookup"><span data-stu-id="2dfdf-103">Gets the Peering locations offered by Microsoft</span></span>

## <span data-ttu-id="2dfdf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2dfdf-104">SYNTAX</span></span>

### <span data-ttu-id="2dfdf-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2dfdf-105">Default (Default)</span></span>
```
Get-AzPeeringLocation [-Kind] <String> [-PeeringLocation <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2dfdf-106">LocationByFacilityId</span><span class="sxs-lookup"><span data-stu-id="2dfdf-106">LocationByFacilityId</span></span>
```
Get-AzPeeringLocation [-Kind] <String> [-PeeringDbFacilityId <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2dfdf-107">LocationByDirectType</span><span class="sxs-lookup"><span data-stu-id="2dfdf-107">LocationByDirectType</span></span>
```
Get-AzPeeringLocation [-Kind] <String> [-PeeringLocation <String>] [-DirectPeeringType] <String>
 [-PeeringDbFacilityId <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2dfdf-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2dfdf-108">DESCRIPTION</span></span>
<span data-ttu-id="2dfdf-109">Kullanıcıların ARM ile bağlanabileceği eşleme özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="2dfdf-109">Gets the Peering Facilities where users can connect with ARM.</span></span>

## <span data-ttu-id="2dfdf-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2dfdf-110">EXAMPLES</span></span>

### <span data-ttu-id="2dfdf-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2dfdf-111">Example 1</span></span>
```powershell
PS C:> Get-AzPeeringLocation -Kind Direct

#...More above
PeeringLocation       : Dublin
Address               : Unit 2, North West Business Park
Country               : IE
PeeringDBFacilityId   : 1065
PeeringDBFacilityLink : https://www.peeringdb.com/fac/1065
BandwidthOffers       : {10Gbps, 100Gbps}

PeeringLocation       : Frankfurt
Address               : Hanauer Landstrasse 298
Country               : DE
PeeringDBFacilityId   : 58
PeeringDBFacilityLink : https://www.peeringdb.com/fac/58
BandwidthOffers       : {10Gbps, 100Gbps}
#...More below
```

<span data-ttu-id="2dfdf-112">Uzun bir konum listesi.</span><span class="sxs-lookup"><span data-stu-id="2dfdf-112">Its a long list of locations.</span></span> <span data-ttu-id="2dfdf-113">Tüm doğrudan eşleme özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="2dfdf-113">Gets the all the Direct Peering Facilities.</span></span>

### <span data-ttu-id="2dfdf-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="2dfdf-114">Example 2</span></span>
```powershell
PS C:> Get-AzPeeringLocation -Kind Exchange -PeeringLocation "Honolulu" 

ExchangeName          : DRF IX
PeeringLocation       : Honolulu
Country               : US
PeeringDBFacilityId   : 267
PeeringDBFacilityLink : https://www.peeringdb.com/ix/267
MicrosoftIPv4Address  : 206.197.210.37
MicrosoftIPv6Address  : 2606:7c80:3375:50::37
FacilityIPv4Prefix    : 206.197.210.0/24
FacilityIPv6Prefix    : 2606:7c80:3375:50::/64
```

<span data-ttu-id="2dfdf-115">Honolulu için Exchange eşleme konumunu alır.</span><span class="sxs-lookup"><span data-stu-id="2dfdf-115">Gets the exchange peering location for Honolulu.</span></span> 

### <span data-ttu-id="2dfdf-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="2dfdf-116">Example 3</span></span>
```powershell
PS C:> Get-AzPeeringLocation -Kind Exchange -PeeringDbFacilityId 71 

ExchangeName          : NIX.CZ
PeeringLocation       : Prague
Country               : CZ
PeeringDBFacilityId   : 71
PeeringDBFacilityLink : https://www.peeringdb.com/ix/71
MicrosoftIPv4Address  : 91.210.16.115
MicrosoftIPv6Address  : 2001:7f8:14::6b:1
FacilityIPv4Prefix    : 91.210.16.0/22
FacilityIPv6Prefix    : 2001:7f8:14::/64
```

<span data-ttu-id="2dfdf-117">Eşleme olanağı kimliği 71 için Exchange eşleme konumunu alır.</span><span class="sxs-lookup"><span data-stu-id="2dfdf-117">Gets the exchange peering location for peering facility id 71.</span></span> 

## <span data-ttu-id="2dfdf-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2dfdf-118">PARAMETERS</span></span>

### <span data-ttu-id="2dfdf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dfdf-119">-DefaultProfile</span></span>
<span data-ttu-id="2dfdf-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2dfdf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2dfdf-121">-DirectPeeringType</span><span class="sxs-lookup"><span data-stu-id="2dfdf-121">-DirectPeeringType</span></span>
<span data-ttu-id="2dfdf-122">' Edge ', ' CDN ' ve ' Aktarım ' seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="2dfdf-122">Select 'Edge', 'CDN', and 'Transit'.</span></span>

```yaml
Type: System.String
Parameter Sets: LocationByDirectType
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dfdf-123">-Tür</span><span class="sxs-lookup"><span data-stu-id="2dfdf-123">-Kind</span></span>
<span data-ttu-id="2dfdf-124">Tüm eşleme kaynağını türe göre gösterir.</span><span class="sxs-lookup"><span data-stu-id="2dfdf-124">Shows all Peering resource by Kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dfdf-125">-PeeringDbFacilityId</span><span class="sxs-lookup"><span data-stu-id="2dfdf-125">-PeeringDbFacilityId</span></span>
<span data-ttu-id="2dfdf-126">PeeringDB.com tesis KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="2dfdf-126">The PeeringDB.com Facility ID</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: LocationByFacilityId, LocationByDirectType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dfdf-127">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="2dfdf-127">-PeeringLocation</span></span>
<span data-ttu-id="2dfdf-128">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="2dfdf-128">The location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, LocationByDirectType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dfdf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dfdf-129">CommonParameters</span></span>
<span data-ttu-id="2dfdf-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2dfdf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dfdf-131">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2dfdf-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dfdf-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2dfdf-132">INPUTS</span></span>

### <span data-ttu-id="2dfdf-133">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2dfdf-133">None</span></span>

## <span data-ttu-id="2dfdf-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2dfdf-134">OUTPUTS</span></span>

### <span data-ttu-id="2dfdf-135">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2dfdf-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringLocation</span></span>

## <span data-ttu-id="2dfdf-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2dfdf-136">NOTES</span></span>

## <span data-ttu-id="2dfdf-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2dfdf-137">RELATED LINKS</span></span>
