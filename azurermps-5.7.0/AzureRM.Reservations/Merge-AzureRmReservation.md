---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/merge-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Merge-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Merge-AzureRmReservation.md
ms.openlocfilehash: 1f5b0c6a743c9ed26864144cf8df21917bc2ac45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589698"
---
# <span data-ttu-id="35946-101">Merge-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="35946-101">Merge-AzureRmReservation</span></span>

## <span data-ttu-id="35946-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35946-102">SYNOPSIS</span></span>
<span data-ttu-id="35946-103">İki `Reservation` s birleştirir.</span><span class="sxs-lookup"><span data-stu-id="35946-103">Merges two `Reservation`s.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35946-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="35946-104">SYNTAX</span></span>

### <span data-ttu-id="35946-105">CommandLine (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="35946-105">CommandLine (Default)</span></span>
```
Merge-AzureRmReservation -ReservationOrderId <String> -ReservationId <String[]> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="35946-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="35946-106">PipeObject</span></span>
```
Merge-AzureRmReservation -Reservation <PSReservation[]> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35946-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="35946-107">DESCRIPTION</span></span>
<span data-ttu-id="35946-108">Belirtilen `Reservation` s 'yi yeni olarak birleştirin `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="35946-108">Merge the specified `Reservation`s into a new `Reservation`.</span></span> <span data-ttu-id="35946-109">Birleştirilen iki `Reservation` s aynı özelliklere sahip olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="35946-109">The two `Reservation`s being merged must have same properties.</span></span>

## <span data-ttu-id="35946-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="35946-110">EXAMPLES</span></span>

### <span data-ttu-id="35946-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="35946-111">Example 1</span></span>
```
PS C:\> Merge-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111","11111111-0000-0000-0000-1111111111"
```

<span data-ttu-id="35946-112">`Reservation`Belirtilen iki`Reservation`</span><span class="sxs-lookup"><span data-stu-id="35946-112">Merge the two specified `Reservation`s into one `Reservation`</span></span>

## <span data-ttu-id="35946-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="35946-113">PARAMETERS</span></span>

### <span data-ttu-id="35946-114">-Ayırma</span><span class="sxs-lookup"><span data-stu-id="35946-114">-Reservation</span></span>
<span data-ttu-id="35946-115">Birleştirilecek iki Rezervıd 'in virgülle ayrılmış dizeleri</span><span class="sxs-lookup"><span data-stu-id="35946-115">Comma-separated strings of two ReservationIds to merge</span></span>

```yaml
Type: PSReservation[]
Parameter Sets: PipeObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35946-116">-Rezervationıd</span><span class="sxs-lookup"><span data-stu-id="35946-116">-ReservationId</span></span>
<span data-ttu-id="35946-117">`ReservationOrder`Bu iki `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="35946-117">ReservationOrderId for the `ReservationOrder` that contains the two `Reservation`s</span></span>

```yaml
Type: String[]
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35946-118">-Rezervationorderıd</span><span class="sxs-lookup"><span data-stu-id="35946-118">-ReservationOrderId</span></span>
<span data-ttu-id="35946-119">{{Fill Rezervno açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="35946-119">{{Fill ReservationOrderId Description}}</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35946-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="35946-120">-Confirm</span></span>
<span data-ttu-id="35946-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="35946-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35946-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35946-122">-WhatIf</span></span>
<span data-ttu-id="35946-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="35946-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="35946-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="35946-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35946-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35946-125">CommonParameters</span></span>
<span data-ttu-id="35946-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="35946-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35946-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35946-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35946-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="35946-128">INPUTS</span></span>

### <span data-ttu-id="35946-129">Microsoft. Azure. Commands. Reservation. modeller. PSReservation []</span><span class="sxs-lookup"><span data-stu-id="35946-129">Microsoft.Azure.Commands.Reservations.Models.PSReservation[]</span></span>

## <span data-ttu-id="35946-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="35946-130">OUTPUTS</span></span>

### <span data-ttu-id="35946-131">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Reservation. modeller. PSReservation, Microsoft. Azure. Commands. Reservation, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="35946-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Reservations.Models.PSReservation, Microsoft.Azure.Commands.Reservations, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="35946-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="35946-132">NOTES</span></span>

## <span data-ttu-id="35946-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="35946-133">RELATED LINKS</span></span>

