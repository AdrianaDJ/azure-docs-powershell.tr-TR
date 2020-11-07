---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/merge-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Merge-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Merge-AzReservation.md
ms.openlocfilehash: 8974a8a0bf8230b630a848e922527bc0b08bdb02
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932613"
---
# <span data-ttu-id="7851d-101">Merge-AzReservation</span><span class="sxs-lookup"><span data-stu-id="7851d-101">Merge-AzReservation</span></span>

## <span data-ttu-id="7851d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7851d-102">SYNOPSIS</span></span>
<span data-ttu-id="7851d-103">İki `Reservation` s birleştirir.</span><span class="sxs-lookup"><span data-stu-id="7851d-103">Merges two `Reservation`s.</span></span>

## <span data-ttu-id="7851d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7851d-104">SYNTAX</span></span>

### <span data-ttu-id="7851d-105">CommandLine (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7851d-105">CommandLine (Default)</span></span>
```
Merge-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7851d-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="7851d-106">PipeObject</span></span>
```
Merge-AzReservation -Reservation <PSReservation[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7851d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7851d-107">DESCRIPTION</span></span>
<span data-ttu-id="7851d-108">Belirtilen `Reservation` s 'yi yeni olarak birleştirin `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="7851d-108">Merge the specified `Reservation`s into a new `Reservation`.</span></span> <span data-ttu-id="7851d-109">Birleştirilen iki `Reservation` s aynı özelliklere sahip olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7851d-109">The two `Reservation`s being merged must have same properties.</span></span>

## <span data-ttu-id="7851d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7851d-110">EXAMPLES</span></span>

### <span data-ttu-id="7851d-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7851d-111">Example 1</span></span>
```
PS C:\> Merge-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111","11111111-0000-0000-0000-1111111111"
```

<span data-ttu-id="7851d-112">`Reservation`Belirtilen iki`Reservation`</span><span class="sxs-lookup"><span data-stu-id="7851d-112">Merge the two specified `Reservation`s into one `Reservation`</span></span>

## <span data-ttu-id="7851d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7851d-113">PARAMETERS</span></span>

### <span data-ttu-id="7851d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7851d-114">-DefaultProfile</span></span>
<span data-ttu-id="7851d-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7851d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7851d-116">-Ayırma</span><span class="sxs-lookup"><span data-stu-id="7851d-116">-Reservation</span></span>
<span data-ttu-id="7851d-117">Birleştirilecek iki Rezervıd 'in virgülle ayrılmış dizeleri</span><span class="sxs-lookup"><span data-stu-id="7851d-117">Comma-separated strings of two ReservationIds to merge</span></span>

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

### <span data-ttu-id="7851d-118">-Rezervationıd</span><span class="sxs-lookup"><span data-stu-id="7851d-118">-ReservationId</span></span>
<span data-ttu-id="7851d-119">`ReservationOrder`Bu iki `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="7851d-119">ReservationOrderId for the `ReservationOrder` that contains the two `Reservation`s</span></span>

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

### <span data-ttu-id="7851d-120">-Rezervationorderıd</span><span class="sxs-lookup"><span data-stu-id="7851d-120">-ReservationOrderId</span></span>
<span data-ttu-id="7851d-121">{{Fill Rezervno açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="7851d-121">{{Fill ReservationOrderId Description}}</span></span>

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

### <span data-ttu-id="7851d-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="7851d-122">-Confirm</span></span>
<span data-ttu-id="7851d-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7851d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7851d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7851d-124">-WhatIf</span></span>
<span data-ttu-id="7851d-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7851d-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7851d-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7851d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7851d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7851d-127">CommonParameters</span></span>
<span data-ttu-id="7851d-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7851d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7851d-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7851d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7851d-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7851d-130">INPUTS</span></span>

### <span data-ttu-id="7851d-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7851d-131">None</span></span>

## <span data-ttu-id="7851d-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7851d-132">OUTPUTS</span></span>

### <span data-ttu-id="7851d-133">Microsoft. Azure. Commands. Reservation. modeller. Psreservatıon</span><span class="sxs-lookup"><span data-stu-id="7851d-133">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="7851d-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7851d-134">NOTES</span></span>

## <span data-ttu-id="7851d-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7851d-135">RELATED LINKS</span></span>