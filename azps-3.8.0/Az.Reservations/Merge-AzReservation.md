---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/merge-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Merge-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Merge-AzReservation.md
ms.openlocfilehash: fc0b04049184334c59a38226e031342fc29207b2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096789"
---
# <span data-ttu-id="41aec-101">Merge-AzReservation</span><span class="sxs-lookup"><span data-stu-id="41aec-101">Merge-AzReservation</span></span>

## <span data-ttu-id="41aec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41aec-102">SYNOPSIS</span></span>
<span data-ttu-id="41aec-103">İki `Reservation` s birleştirir.</span><span class="sxs-lookup"><span data-stu-id="41aec-103">Merges two `Reservation`s.</span></span>

## <span data-ttu-id="41aec-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="41aec-104">SYNTAX</span></span>

### <span data-ttu-id="41aec-105">CommandLine (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="41aec-105">CommandLine (Default)</span></span>
```
Merge-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41aec-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="41aec-106">PipeObject</span></span>
```
Merge-AzReservation -Reservation <PSReservation[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41aec-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="41aec-107">DESCRIPTION</span></span>
<span data-ttu-id="41aec-108">Belirtilen `Reservation` s 'yi yeni olarak birleştirin `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="41aec-108">Merge the specified `Reservation`s into a new `Reservation`.</span></span> <span data-ttu-id="41aec-109">Birleştirilen iki `Reservation` s aynı özelliklere sahip olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="41aec-109">The two `Reservation`s being merged must have same properties.</span></span>

## <span data-ttu-id="41aec-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="41aec-110">EXAMPLES</span></span>

### <span data-ttu-id="41aec-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="41aec-111">Example 1</span></span>
```
PS C:\> Merge-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111","11111111-0000-0000-0000-1111111111"
```

<span data-ttu-id="41aec-112">`Reservation`Belirtilen iki`Reservation`</span><span class="sxs-lookup"><span data-stu-id="41aec-112">Merge the two specified `Reservation`s into one `Reservation`</span></span>

## <span data-ttu-id="41aec-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="41aec-113">PARAMETERS</span></span>

### <span data-ttu-id="41aec-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41aec-114">-DefaultProfile</span></span>
<span data-ttu-id="41aec-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="41aec-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41aec-116">-Ayırma</span><span class="sxs-lookup"><span data-stu-id="41aec-116">-Reservation</span></span>
<span data-ttu-id="41aec-117">Birleştirilecek iki Rezervıd 'in virgülle ayrılmış dizeleri</span><span class="sxs-lookup"><span data-stu-id="41aec-117">Comma-separated strings of two ReservationIds to merge</span></span>

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

### <span data-ttu-id="41aec-118">-Rezervationıd</span><span class="sxs-lookup"><span data-stu-id="41aec-118">-ReservationId</span></span>
<span data-ttu-id="41aec-119">`ReservationOrder`Bu iki `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="41aec-119">ReservationOrderId for the `ReservationOrder` that contains the two `Reservation`s</span></span>

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

### <span data-ttu-id="41aec-120">-Rezervationorderıd</span><span class="sxs-lookup"><span data-stu-id="41aec-120">-ReservationOrderId</span></span>
<span data-ttu-id="41aec-121">{{Fill Rezervno açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="41aec-121">{{Fill ReservationOrderId Description}}</span></span>

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

### <span data-ttu-id="41aec-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="41aec-122">-Confirm</span></span>
<span data-ttu-id="41aec-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="41aec-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41aec-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41aec-124">-WhatIf</span></span>
<span data-ttu-id="41aec-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="41aec-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="41aec-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="41aec-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41aec-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41aec-127">CommonParameters</span></span>
<span data-ttu-id="41aec-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="41aec-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41aec-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="41aec-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41aec-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="41aec-130">INPUTS</span></span>

### <span data-ttu-id="41aec-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="41aec-131">None</span></span>

## <span data-ttu-id="41aec-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="41aec-132">OUTPUTS</span></span>

### <span data-ttu-id="41aec-133">Microsoft. Azure. Commands. Reservation. modeller. Psreservatıon</span><span class="sxs-lookup"><span data-stu-id="41aec-133">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="41aec-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="41aec-134">NOTES</span></span>

## <span data-ttu-id="41aec-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="41aec-135">RELATED LINKS</span></span>
