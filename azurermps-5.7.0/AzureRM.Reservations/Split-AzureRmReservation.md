---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/split-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Split-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Split-AzureRmReservation.md
ms.openlocfilehash: 89c19f2c61604f3c38ba8cc9679f956d68df3179
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589699"
---
# <span data-ttu-id="79fd0-101">Split-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="79fd0-101">Split-AzureRmReservation</span></span>

## <span data-ttu-id="79fd0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79fd0-102">SYNOPSIS</span></span>
<span data-ttu-id="79fd0-103">Bölünmüş bir `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="79fd0-103">Split a `Reservation`.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79fd0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="79fd0-104">SYNTAX</span></span>

### <span data-ttu-id="79fd0-105">CommandLine (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="79fd0-105">CommandLine (Default)</span></span>
```
Split-AzureRmReservation -ReservationOrderId <String> -ReservationId <String> -Quantity <Nullable`1[]>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79fd0-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="79fd0-106">PipeObject</span></span>
```
Split-AzureRmReservation -Quantity <Nullable`1[]> -Reservation <PSReservation> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="79fd0-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="79fd0-107">DESCRIPTION</span></span>
<span data-ttu-id="79fd0-108">`Reservation` `Reservation` Belirtilen miktar dağılımına sahip iki s öğesine bölün.</span><span class="sxs-lookup"><span data-stu-id="79fd0-108">Split a `Reservation` into two `Reservation`s with specified quantity distribution.</span></span>

## <span data-ttu-id="79fd0-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="79fd0-109">EXAMPLES</span></span>

### <span data-ttu-id="79fd0-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="79fd0-110">Example 1</span></span>
```
PS C:\> Split-AzureRmReservation -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111" -Quantities 2,3
```

<span data-ttu-id="79fd0-111">Belirtilen `Reservation` miktarları iki şekilde belirtilen `Reservation` değerlerle bölün</span><span class="sxs-lookup"><span data-stu-id="79fd0-111">Split the specified `Reservation` into two `Reservation`s with the corresponding quantities</span></span>

## <span data-ttu-id="79fd0-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="79fd0-112">PARAMETERS</span></span>

### <span data-ttu-id="79fd0-113">-Miktar</span><span class="sxs-lookup"><span data-stu-id="79fd0-113">-Quantity</span></span>
<span data-ttu-id="79fd0-114">İki s, miktar alanı için virgülle ayrılmış tamsayılar `Reservation`</span><span class="sxs-lookup"><span data-stu-id="79fd0-114">Comma-separated integers for quantity field of the two `Reservation`s</span></span>

```yaml
Type: Nullable`1[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79fd0-115">-Ayırma</span><span class="sxs-lookup"><span data-stu-id="79fd0-115">-Reservation</span></span>
<span data-ttu-id="79fd0-116">İçin yöneltme nesnesi parametresi `Reservation`</span><span class="sxs-lookup"><span data-stu-id="79fd0-116">Pipe object parameter for `Reservation`</span></span>

```yaml
Type: PSReservation
Parameter Sets: PipeObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79fd0-117">-Rezervationıd</span><span class="sxs-lookup"><span data-stu-id="79fd0-117">-ReservationId</span></span>
<span data-ttu-id="79fd0-118">`Reservation`Bölüneceği yer</span><span class="sxs-lookup"><span data-stu-id="79fd0-118">Id of the `Reservation` to split</span></span>

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

### <span data-ttu-id="79fd0-119">-Rezervationorderıd</span><span class="sxs-lookup"><span data-stu-id="79fd0-119">-ReservationOrderId</span></span>
<span data-ttu-id="79fd0-120">`ReservationOrder` `Reservation` Kullanıcının bölmek istediğini içeren ID</span><span class="sxs-lookup"><span data-stu-id="79fd0-120">Id of the `ReservationOrder` that contains the `Reservation` that user wants to split</span></span>

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

### <span data-ttu-id="79fd0-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="79fd0-121">-Confirm</span></span>
<span data-ttu-id="79fd0-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="79fd0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79fd0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79fd0-123">-WhatIf</span></span>
<span data-ttu-id="79fd0-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="79fd0-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="79fd0-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="79fd0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79fd0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79fd0-126">CommonParameters</span></span>
<span data-ttu-id="79fd0-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="79fd0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79fd0-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79fd0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79fd0-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="79fd0-129">INPUTS</span></span>

### <span data-ttu-id="79fd0-130">Microsoft. Azure. Commands. Reservation. modeller. Psreservatıon</span><span class="sxs-lookup"><span data-stu-id="79fd0-130">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="79fd0-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="79fd0-131">OUTPUTS</span></span>

### <span data-ttu-id="79fd0-132">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Reservation. modeller. PSReservation, Microsoft. Azure. Commands. Reservation, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="79fd0-132">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Reservations.Models.PSReservation, Microsoft.Azure.Commands.Reservations, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="79fd0-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="79fd0-133">NOTES</span></span>

## <span data-ttu-id="79fd0-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="79fd0-134">RELATED LINKS</span></span>

