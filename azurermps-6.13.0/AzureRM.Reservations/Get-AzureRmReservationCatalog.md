---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationcatalog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationCatalog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationCatalog.md
ms.openlocfilehash: 155310764ea540d9062df8ae8f37171bc6f73066
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588393"
---
# <span data-ttu-id="3cd3a-101">Get-AzureRmReservationCatalog</span><span class="sxs-lookup"><span data-stu-id="3cd3a-101">Get-AzureRmReservationCatalog</span></span>

## <span data-ttu-id="3cd3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cd3a-102">SYNOPSIS</span></span>
<span data-ttu-id="3cd3a-103">Kullanılabilir rezervasyonların kataloğunu alma</span><span class="sxs-lookup"><span data-stu-id="3cd3a-103">Get the catalog of available reservations</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3cd3a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3cd3a-104">SYNTAX</span></span>

```
Get-AzureRmReservationCatalog [-SubscriptionId <Guid>] -ReservedResourceType <String> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3cd3a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3cd3a-105">DESCRIPTION</span></span>
<span data-ttu-id="3cd3a-106">Belirtilen Azure aboneliği için ayrılan örnek satın alma için sağlanan bölgeleri ve STB 'leri edinin.</span><span class="sxs-lookup"><span data-stu-id="3cd3a-106">Get the regions and skus that are available for Reserved Instance purchase for the specified Azure subscription.</span></span>

## <span data-ttu-id="3cd3a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3cd3a-107">EXAMPLES</span></span>

### <span data-ttu-id="3cd3a-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3cd3a-108">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationCatalog -ReservedResourceType VirtualMachines -Location westus
```

<span data-ttu-id="3cd3a-109">Varsayılan abonelik için westus 'de VirtualMachines kataloğunu alma</span><span class="sxs-lookup"><span data-stu-id="3cd3a-109">Get the VirtualMachines catalog in westus for the default subscription</span></span>

### <span data-ttu-id="3cd3a-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="3cd3a-110">Example 2</span></span>
```
PS C:\> Get-AzureRmReservationCatalog -SubscriptionId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservedResourceType SuseLinux
```

<span data-ttu-id="3cd3a-111">Belirtilen abonelik için SuseLinux kataloğunu alma</span><span class="sxs-lookup"><span data-stu-id="3cd3a-111">Get the SuseLinux catalog for the specified subscription</span></span>

## <span data-ttu-id="3cd3a-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3cd3a-112">PARAMETERS</span></span>

### <span data-ttu-id="3cd3a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cd3a-113">-DefaultProfile</span></span>
<span data-ttu-id="3cd3a-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3cd3a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cd3a-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="3cd3a-115">-Location</span></span>
<span data-ttu-id="3cd3a-116">Katalogda ayrılan kaynakların konumunu belirtir</span><span class="sxs-lookup"><span data-stu-id="3cd3a-116">Specifies the location of the reserved resources in the catalog</span></span>

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

### <span data-ttu-id="3cd3a-117">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="3cd3a-117">-ReservedResourceType</span></span>
<span data-ttu-id="3cd3a-118">Katalogda ayrılan kaynakların türünü belirtir</span><span class="sxs-lookup"><span data-stu-id="3cd3a-118">Specifies the type of the reserved resources in the catalog</span></span>

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

### <span data-ttu-id="3cd3a-119">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="3cd3a-119">-SubscriptionId</span></span>
<span data-ttu-id="3cd3a-120">Aboneliğin kimliği</span><span class="sxs-lookup"><span data-stu-id="3cd3a-120">Id of the subscription</span></span>

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

### <span data-ttu-id="3cd3a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cd3a-121">CommonParameters</span></span>
<span data-ttu-id="3cd3a-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3cd3a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cd3a-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cd3a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cd3a-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3cd3a-124">INPUTS</span></span>

### <span data-ttu-id="3cd3a-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3cd3a-125">None</span></span>

## <span data-ttu-id="3cd3a-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3cd3a-126">OUTPUTS</span></span>

### <span data-ttu-id="3cd3a-127">Microsoft. Azure. Commands. rezervasyonlar. modeller. PSCatalog</span><span class="sxs-lookup"><span data-stu-id="3cd3a-127">Microsoft.Azure.Commands.Reservations.Models.PSCatalog</span></span>

## <span data-ttu-id="3cd3a-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3cd3a-128">NOTES</span></span>

## <span data-ttu-id="3cd3a-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3cd3a-129">RELATED LINKS</span></span>
