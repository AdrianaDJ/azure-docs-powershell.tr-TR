---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationcatalog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationCatalog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationCatalog.md
ms.openlocfilehash: 6f1eb79b7c740cae437e28af8153a4c14532871e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274690"
---
# <span data-ttu-id="c0b9d-101">Get-AzReservationCatalog</span><span class="sxs-lookup"><span data-stu-id="c0b9d-101">Get-AzReservationCatalog</span></span>

## <span data-ttu-id="c0b9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0b9d-102">SYNOPSIS</span></span>
<span data-ttu-id="c0b9d-103">Kullanılabilir rezervasyonların kataloğunu alma</span><span class="sxs-lookup"><span data-stu-id="c0b9d-103">Get the catalog of available reservations</span></span>

## <span data-ttu-id="c0b9d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c0b9d-104">SYNTAX</span></span>

```
Get-AzReservationCatalog [-SubscriptionId <Guid>] -ReservedResourceType <String> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0b9d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c0b9d-105">DESCRIPTION</span></span>
<span data-ttu-id="c0b9d-106">Belirtilen Azure aboneliği için ayrılan örnek satın alma için sağlanan bölgeleri ve STB 'leri edinin.</span><span class="sxs-lookup"><span data-stu-id="c0b9d-106">Get the regions and skus that are available for Reserved Instance purchase for the specified Azure subscription.</span></span>

## <span data-ttu-id="c0b9d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c0b9d-107">EXAMPLES</span></span>

### <span data-ttu-id="c0b9d-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c0b9d-108">Example 1</span></span>
```
PS C:\> Get-AzReservationCatalog -ReservedResourceType VirtualMachines -Location westus
```

<span data-ttu-id="c0b9d-109">Varsayılan abonelik için westus 'de VirtualMachines kataloğunu alma</span><span class="sxs-lookup"><span data-stu-id="c0b9d-109">Get the VirtualMachines catalog in westus for the default subscription</span></span>

### <span data-ttu-id="c0b9d-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="c0b9d-110">Example 2</span></span>
```
PS C:\> Get-AzReservationCatalog -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservedResourceType SuseLinux
```

<span data-ttu-id="c0b9d-111">Belirtilen abonelik için SuseLinux kataloğunu alma</span><span class="sxs-lookup"><span data-stu-id="c0b9d-111">Get the SuseLinux catalog for the specified subscription</span></span>

## <span data-ttu-id="c0b9d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c0b9d-112">PARAMETERS</span></span>

### <span data-ttu-id="c0b9d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0b9d-113">-DefaultProfile</span></span>
<span data-ttu-id="c0b9d-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c0b9d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0b9d-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="c0b9d-115">-Location</span></span>
<span data-ttu-id="c0b9d-116">Katalogda ayrılan kaynakların konumunu belirtir</span><span class="sxs-lookup"><span data-stu-id="c0b9d-116">Specifies the location of the reserved resources in the catalog</span></span>

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

### <span data-ttu-id="c0b9d-117">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="c0b9d-117">-ReservedResourceType</span></span>
<span data-ttu-id="c0b9d-118">Katalogda ayrılan kaynakların türünü belirtir</span><span class="sxs-lookup"><span data-stu-id="c0b9d-118">Specifies the type of the reserved resources in the catalog</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0b9d-119">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="c0b9d-119">-SubscriptionId</span></span>
<span data-ttu-id="c0b9d-120">Aboneliğin kimliği</span><span class="sxs-lookup"><span data-stu-id="c0b9d-120">Id of the subscription</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0b9d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0b9d-121">CommonParameters</span></span>
<span data-ttu-id="c0b9d-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c0b9d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0b9d-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c0b9d-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0b9d-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c0b9d-124">INPUTS</span></span>

### <span data-ttu-id="c0b9d-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c0b9d-125">None</span></span>

## <span data-ttu-id="c0b9d-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c0b9d-126">OUTPUTS</span></span>

### <span data-ttu-id="c0b9d-127">Microsoft. Azure. Commands. rezervasyonlar. modeller. PSCatalog</span><span class="sxs-lookup"><span data-stu-id="c0b9d-127">Microsoft.Azure.Commands.Reservations.Models.PSCatalog</span></span>

## <span data-ttu-id="c0b9d-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c0b9d-128">NOTES</span></span>

## <span data-ttu-id="c0b9d-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c0b9d-129">RELATED LINKS</span></span>
