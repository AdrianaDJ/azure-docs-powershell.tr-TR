---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azlegacypeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzLegacyPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzLegacyPeering.md
ms.openlocfilehash: 9a2fcb87b05d4478ab7b3e3490feae92fd727ce7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932865"
---
# <span data-ttu-id="8dad2-101">Get-AzLegacyPeering</span><span class="sxs-lookup"><span data-stu-id="8dad2-101">Get-AzLegacyPeering</span></span>

## <span data-ttu-id="8dad2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8dad2-102">SYNOPSIS</span></span>
<span data-ttu-id="8dad2-103">Eski eşleme kaynaklarını Azure Kaynak Yönetimi (ARM) kaynaklarına dönüştürmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8dad2-103">Used to Convert Legacy Peering resources to Azure Resource Management (ARM) Resources.</span></span> 

## <span data-ttu-id="8dad2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8dad2-104">SYNTAX</span></span>

```
Get-AzLegacyPeering [-PeeringLocation] <String> [-Kind] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8dad2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8dad2-105">DESCRIPTION</span></span>
<span data-ttu-id="8dad2-106">Bu komut, Azure Kaynak Yönetimi (ARM) kaynaklarına dönüştürecekleri eski eşleme kaynaklarını görüntülemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8dad2-106">The command is used to view legacy Peering resources which all you to convert them to Azure Resource Management (ARM) Resources.</span></span>

## <span data-ttu-id="8dad2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8dad2-107">EXAMPLES</span></span>

### <span data-ttu-id="8dad2-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8dad2-108">Example 1</span></span>
```powershell
PS C:> Get-AzLegacyPeering -PeeringLocation "Seattle" -Kind Direct

Name                       :
Sku                        : Basic_Direct_Free
Kind                       : Direct
PeeringLocation            : Seattle
UseForPeeringService       : False
PeerAsn.Id                 :
Connection                 : ------------------------
PeeringDBFacilityId        : 71
SessionPrefixIPv4          : 173.205.50.236/30
PeerSessionIPv4Address     : 173.205.50.237
MicrosoftIPv4Address       : 173.205.50.238
SessionStateV4             : Established
MaxPrefixesAdvertisedV4    : 20000
SessionPrefixIPv6          : 2001:668:0:3:ffff:0:adcd:32ec/126
PeerSessionIPv6Address     : 2001:668:0:3:ffff:0:adcd:32ed
MicrosoftIPv6Address       : 2001:668:0:3:ffff:0:adcd:32ee
SessionStateV6             : Established
MaxPrefixesAdvertisedV6    : 2000
ConnectionState            : Active
BandwidthInMbps            : 0
ProvisionedBandwidthInMbps : 20000
ProvisioningState          : Succeeded
```

<span data-ttu-id="8dad2-109">Seattle için eski eşlemeyi alır</span><span class="sxs-lookup"><span data-stu-id="8dad2-109">Gets the legacy peering for Seattle</span></span>

## <span data-ttu-id="8dad2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8dad2-110">PARAMETERS</span></span>

### <span data-ttu-id="8dad2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dad2-111">-DefaultProfile</span></span>
<span data-ttu-id="8dad2-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8dad2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8dad2-113">-Tür</span><span class="sxs-lookup"><span data-stu-id="8dad2-113">-Kind</span></span>
<span data-ttu-id="8dad2-114">Tüm eşleme kaynağını türe göre gösterir.</span><span class="sxs-lookup"><span data-stu-id="8dad2-114">Shows all Peering resource by Kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dad2-115">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="8dad2-115">-PeeringLocation</span></span>
<span data-ttu-id="8dad2-116">Tüm eşleme kaynağını türe göre gösterir.</span><span class="sxs-lookup"><span data-stu-id="8dad2-116">Shows all Peering resource by Kind.</span></span>

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

### <span data-ttu-id="8dad2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dad2-117">CommonParameters</span></span>
<span data-ttu-id="8dad2-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8dad2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dad2-119">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8dad2-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dad2-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8dad2-120">INPUTS</span></span>

### <span data-ttu-id="8dad2-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="8dad2-121">None</span></span>

## <span data-ttu-id="8dad2-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8dad2-122">OUTPUTS</span></span>

### <span data-ttu-id="8dad2-123">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8dad2-123">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="8dad2-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8dad2-124">NOTES</span></span>

## <span data-ttu-id="8dad2-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8dad2-125">RELATED LINKS</span></span>
