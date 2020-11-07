---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/merge-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Merge-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Merge-AzureRmReservation.md
ms.openlocfilehash: 6428e4df850d2806939f5d9f8d4e115698e91fb1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762289"
---
# <span data-ttu-id="f05cf-101">Merge-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="f05cf-101">Merge-AzureRmReservation</span></span>

## <span data-ttu-id="f05cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f05cf-102">SYNOPSIS</span></span>
<span data-ttu-id="f05cf-103">İki `Reservation` s birleştirir.</span><span class="sxs-lookup"><span data-stu-id="f05cf-103">Merges two `Reservation`s.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f05cf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f05cf-104">SYNTAX</span></span>

### <span data-ttu-id="f05cf-105">CommandLine (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f05cf-105">CommandLine (Default)</span></span>
```
Merge-AzureRmReservation -ReservationOrderId <Guid> -ReservationId <Guid[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f05cf-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="f05cf-106">PipeObject</span></span>
```
Merge-AzureRmReservation -Reservation <PSReservation[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f05cf-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f05cf-107">DESCRIPTION</span></span>
<span data-ttu-id="f05cf-108">Belirtilen `Reservation` s 'yi yeni olarak birleştirin `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="f05cf-108">Merge the specified `Reservation`s into a new `Reservation`.</span></span> <span data-ttu-id="f05cf-109">Birleştirilen iki `Reservation` s aynı özelliklere sahip olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f05cf-109">The two `Reservation`s being merged must have same properties.</span></span>

## <span data-ttu-id="f05cf-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f05cf-110">EXAMPLES</span></span>

### <span data-ttu-id="f05cf-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f05cf-111">Example 1</span></span>
```
PS C:\> Merge-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111","11111111-0000-0000-0000-1111111111"
```

<span data-ttu-id="f05cf-112">`Reservation`Belirtilen iki`Reservation`</span><span class="sxs-lookup"><span data-stu-id="f05cf-112">Merge the two specified `Reservation`s into one `Reservation`</span></span>

## <span data-ttu-id="f05cf-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f05cf-113">PARAMETERS</span></span>

### <span data-ttu-id="f05cf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f05cf-114">-DefaultProfile</span></span>
<span data-ttu-id="f05cf-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f05cf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f05cf-116">-Ayırma</span><span class="sxs-lookup"><span data-stu-id="f05cf-116">-Reservation</span></span>
<span data-ttu-id="f05cf-117">Birleştirilecek iki Rezervıd 'in virgülle ayrılmış dizeleri</span><span class="sxs-lookup"><span data-stu-id="f05cf-117">Comma-separated strings of two ReservationIds to merge</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservation[]
Parameter Sets: PipeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f05cf-118">-Rezervationıd</span><span class="sxs-lookup"><span data-stu-id="f05cf-118">-ReservationId</span></span>
<span data-ttu-id="f05cf-119">`ReservationOrder`Bu iki `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="f05cf-119">ReservationOrderId for the `ReservationOrder` that contains the two `Reservation`s</span></span>

```yaml
Type: System.Guid[]
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f05cf-120">-Rezervationorderıd</span><span class="sxs-lookup"><span data-stu-id="f05cf-120">-ReservationOrderId</span></span>
<span data-ttu-id="f05cf-121">{{Fill Rezervno açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="f05cf-121">{{Fill ReservationOrderId Description}}</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f05cf-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="f05cf-122">-Confirm</span></span>
<span data-ttu-id="f05cf-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f05cf-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f05cf-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f05cf-124">-WhatIf</span></span>
<span data-ttu-id="f05cf-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f05cf-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f05cf-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f05cf-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f05cf-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f05cf-127">CommonParameters</span></span>
<span data-ttu-id="f05cf-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f05cf-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f05cf-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f05cf-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f05cf-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f05cf-130">INPUTS</span></span>

### <span data-ttu-id="f05cf-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f05cf-131">None</span></span>

## <span data-ttu-id="f05cf-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f05cf-132">OUTPUTS</span></span>

### <span data-ttu-id="f05cf-133">Microsoft. Azure. Commands. Reservation. modeller. Psreservatıon</span><span class="sxs-lookup"><span data-stu-id="f05cf-133">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="f05cf-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f05cf-134">NOTES</span></span>

## <span data-ttu-id="f05cf-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f05cf-135">RELATED LINKS</span></span>