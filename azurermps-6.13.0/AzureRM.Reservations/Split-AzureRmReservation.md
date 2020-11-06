---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/split-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Split-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Split-AzureRmReservation.md
ms.openlocfilehash: bc1fba5c7fa7e01a3c2461907a214809e175f3ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587175"
---
# <span data-ttu-id="2c99d-101">Split-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="2c99d-101">Split-AzureRmReservation</span></span>

## <span data-ttu-id="2c99d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c99d-102">SYNOPSIS</span></span>
<span data-ttu-id="2c99d-103">Bölünmüş bir `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="2c99d-103">Split a `Reservation`.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c99d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2c99d-104">SYNTAX</span></span>

### <span data-ttu-id="2c99d-105">CommandLine (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2c99d-105">CommandLine (Default)</span></span>
```
Split-AzureRmReservation -ReservationOrderId <Guid> -ReservationId <Guid> -Quantity <Int32[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c99d-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="2c99d-106">PipeObject</span></span>
```
Split-AzureRmReservation -Quantity <Int32[]> -Reservation <PSReservation>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c99d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2c99d-107">DESCRIPTION</span></span>
<span data-ttu-id="2c99d-108">`Reservation` `Reservation` Belirtilen miktar dağılımına sahip iki s öğesine bölün.</span><span class="sxs-lookup"><span data-stu-id="2c99d-108">Split a `Reservation` into two `Reservation`s with specified quantity distribution.</span></span>

## <span data-ttu-id="2c99d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2c99d-109">EXAMPLES</span></span>

### <span data-ttu-id="2c99d-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2c99d-110">Example 1</span></span>
```
PS C:\> Split-AzureRmReservation -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111" -Quantities 2,3
```

<span data-ttu-id="2c99d-111">Belirtilen `Reservation` miktarları iki şekilde belirtilen `Reservation` değerlerle bölün</span><span class="sxs-lookup"><span data-stu-id="2c99d-111">Split the specified `Reservation` into two `Reservation`s with the corresponding quantities</span></span>

## <span data-ttu-id="2c99d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2c99d-112">PARAMETERS</span></span>

### <span data-ttu-id="2c99d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c99d-113">-DefaultProfile</span></span>
<span data-ttu-id="2c99d-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2c99d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c99d-115">-Miktar</span><span class="sxs-lookup"><span data-stu-id="2c99d-115">-Quantity</span></span>
<span data-ttu-id="2c99d-116">İki s, miktar alanı için virgülle ayrılmış tamsayılar `Reservation`</span><span class="sxs-lookup"><span data-stu-id="2c99d-116">Comma-separated integers for quantity field of the two `Reservation`s</span></span>

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

### <span data-ttu-id="2c99d-117">-Ayırma</span><span class="sxs-lookup"><span data-stu-id="2c99d-117">-Reservation</span></span>
<span data-ttu-id="2c99d-118">İçin yöneltme nesnesi parametresi `Reservation`</span><span class="sxs-lookup"><span data-stu-id="2c99d-118">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="2c99d-119">-Rezervationıd</span><span class="sxs-lookup"><span data-stu-id="2c99d-119">-ReservationId</span></span>
<span data-ttu-id="2c99d-120">`Reservation`Bölüneceği yer</span><span class="sxs-lookup"><span data-stu-id="2c99d-120">Id of the `Reservation` to split</span></span>

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

### <span data-ttu-id="2c99d-121">-Rezervationorderıd</span><span class="sxs-lookup"><span data-stu-id="2c99d-121">-ReservationOrderId</span></span>
<span data-ttu-id="2c99d-122">`ReservationOrder` `Reservation` Kullanıcının bölmek istediğini içeren ID</span><span class="sxs-lookup"><span data-stu-id="2c99d-122">Id of the `ReservationOrder` that contains the `Reservation` that user wants to split</span></span>

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

### <span data-ttu-id="2c99d-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="2c99d-123">-Confirm</span></span>
<span data-ttu-id="2c99d-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2c99d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c99d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c99d-125">-WhatIf</span></span>
<span data-ttu-id="2c99d-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2c99d-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c99d-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2c99d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c99d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c99d-128">CommonParameters</span></span>
<span data-ttu-id="2c99d-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2c99d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c99d-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c99d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c99d-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2c99d-131">INPUTS</span></span>

### <span data-ttu-id="2c99d-132">Microsoft. Azure. Commands. Reservation. modeller. Psreservatıon</span><span class="sxs-lookup"><span data-stu-id="2c99d-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>
<span data-ttu-id="2c99d-133">Parametreler: Reservation (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2c99d-133">Parameters: Reservation (ByValue)</span></span>

## <span data-ttu-id="2c99d-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2c99d-134">OUTPUTS</span></span>

### <span data-ttu-id="2c99d-135">Microsoft. Azure. Commands. Reservation. modeller. Psreservatıon</span><span class="sxs-lookup"><span data-stu-id="2c99d-135">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="2c99d-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2c99d-136">NOTES</span></span>

## <span data-ttu-id="2c99d-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2c99d-137">RELATED LINKS</span></span>
