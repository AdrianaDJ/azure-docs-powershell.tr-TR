---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/split-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
ms.openlocfilehash: b879b5b47c752a331f0c2d70a6d37e57b113d816
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097335"
---
# <span data-ttu-id="12293-101">Split-AzReservation</span><span class="sxs-lookup"><span data-stu-id="12293-101">Split-AzReservation</span></span>

## <span data-ttu-id="12293-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12293-102">SYNOPSIS</span></span>
<span data-ttu-id="12293-103">Bölünmüş bir `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="12293-103">Split a `Reservation`.</span></span>

## <span data-ttu-id="12293-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="12293-104">SYNTAX</span></span>

### <span data-ttu-id="12293-105">CommandLine (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="12293-105">CommandLine (Default)</span></span>
```
Split-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -Quantity <Int32[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12293-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="12293-106">PipeObject</span></span>
```
Split-AzReservation -Quantity <Int32[]> -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12293-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="12293-107">DESCRIPTION</span></span>
<span data-ttu-id="12293-108">`Reservation` `Reservation` Belirtilen miktar dağılımına sahip iki s öğesine bölün.</span><span class="sxs-lookup"><span data-stu-id="12293-108">Split a `Reservation` into two `Reservation`s with specified quantity distribution.</span></span>

## <span data-ttu-id="12293-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="12293-109">EXAMPLES</span></span>

### <span data-ttu-id="12293-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="12293-110">Example 1</span></span>
```
PS C:\> Split-AzReservation -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111" -Quantities 2,3
```

<span data-ttu-id="12293-111">Belirtilen `Reservation` miktarları iki şekilde belirtilen `Reservation` değerlerle bölün</span><span class="sxs-lookup"><span data-stu-id="12293-111">Split the specified `Reservation` into two `Reservation`s with the corresponding quantities</span></span>

## <span data-ttu-id="12293-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="12293-112">PARAMETERS</span></span>

### <span data-ttu-id="12293-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12293-113">-DefaultProfile</span></span>
<span data-ttu-id="12293-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="12293-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12293-115">-Miktar</span><span class="sxs-lookup"><span data-stu-id="12293-115">-Quantity</span></span>
<span data-ttu-id="12293-116">İki s, miktar alanı için virgülle ayrılmış tamsayılar `Reservation`</span><span class="sxs-lookup"><span data-stu-id="12293-116">Comma-separated integers for quantity field of the two `Reservation`s</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12293-117">-Ayırma</span><span class="sxs-lookup"><span data-stu-id="12293-117">-Reservation</span></span>
<span data-ttu-id="12293-118">İçin yöneltme nesnesi parametresi `Reservation`</span><span class="sxs-lookup"><span data-stu-id="12293-118">Pipe object parameter for `Reservation`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservation
Parameter Sets: PipeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12293-119">-Rezervationıd</span><span class="sxs-lookup"><span data-stu-id="12293-119">-ReservationId</span></span>
<span data-ttu-id="12293-120">`Reservation`Bölüneceği yer</span><span class="sxs-lookup"><span data-stu-id="12293-120">Id of the `Reservation` to split</span></span>

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

### <span data-ttu-id="12293-121">-Rezervationorderıd</span><span class="sxs-lookup"><span data-stu-id="12293-121">-ReservationOrderId</span></span>
<span data-ttu-id="12293-122">`ReservationOrder` `Reservation` Kullanıcının bölmek istediğini içeren ID</span><span class="sxs-lookup"><span data-stu-id="12293-122">Id of the `ReservationOrder` that contains the `Reservation` that user wants to split</span></span>

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

### <span data-ttu-id="12293-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="12293-123">-Confirm</span></span>
<span data-ttu-id="12293-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="12293-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12293-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12293-125">-WhatIf</span></span>
<span data-ttu-id="12293-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="12293-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="12293-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="12293-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12293-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12293-128">CommonParameters</span></span>
<span data-ttu-id="12293-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="12293-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12293-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="12293-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12293-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="12293-131">INPUTS</span></span>

### <span data-ttu-id="12293-132">Microsoft. Azure. Commands. Reservation. modeller. Psreservatıon</span><span class="sxs-lookup"><span data-stu-id="12293-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="12293-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="12293-133">OUTPUTS</span></span>

### <span data-ttu-id="12293-134">Microsoft. Azure. Commands. Reservation. modeller. Psreservatıon</span><span class="sxs-lookup"><span data-stu-id="12293-134">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="12293-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="12293-135">NOTES</span></span>

## <span data-ttu-id="12293-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="12293-136">RELATED LINKS</span></span>