---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservation.md
ms.openlocfilehash: 1003dcf38815be8daba8b0e218dbca430a89f9e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587180"
---
# <span data-ttu-id="d5aaf-101">Get-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="d5aaf-101">Get-AzureRmReservation</span></span>

## <span data-ttu-id="d5aaf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5aaf-102">SYNOPSIS</span></span>
<span data-ttu-id="d5aaf-103">`Reservation`Belirli bir ayırma emrinde s alın</span><span class="sxs-lookup"><span data-stu-id="d5aaf-103">Get `Reservation`s in a given reservation Order</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5aaf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d5aaf-104">SYNTAX</span></span>

### <span data-ttu-id="d5aaf-105">CommandLine (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d5aaf-105">CommandLine (Default)</span></span>
```
Get-AzureRmReservation -ReservationOrderId <Guid> [-ReservationId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5aaf-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="d5aaf-106">PipeObject</span></span>
```
Get-AzureRmReservation [-ReservationOrder <PSReservationOrder>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d5aaf-107">PagePipeObject</span><span class="sxs-lookup"><span data-stu-id="d5aaf-107">PagePipeObject</span></span>
```
Get-AzureRmReservation [-ReservationOrderPage <PSReservationOrderPage>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5aaf-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d5aaf-108">DESCRIPTION</span></span>
<span data-ttu-id="d5aaf-109">`Reservation`Tek bir `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="d5aaf-109">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="d5aaf-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d5aaf-110">EXAMPLES</span></span>

### <span data-ttu-id="d5aaf-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d5aaf-111">Example 1</span></span>
```
PS C:\> Get-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="d5aaf-112">`Reservation`Belirtilen içinde liste s `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="d5aaf-112">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="d5aaf-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d5aaf-113">Example 2</span></span>
```
PS C:\> Get-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="d5aaf-114">Belirli `Reservation` Ayrıntılar edinin.</span><span class="sxs-lookup"><span data-stu-id="d5aaf-114">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="d5aaf-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d5aaf-115">PARAMETERS</span></span>

### <span data-ttu-id="d5aaf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5aaf-116">-DefaultProfile</span></span>
<span data-ttu-id="d5aaf-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d5aaf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5aaf-118">-Rezervationıd</span><span class="sxs-lookup"><span data-stu-id="d5aaf-118">-ReservationId</span></span>
<span data-ttu-id="d5aaf-119">`Reservation`Bakılacak yer</span><span class="sxs-lookup"><span data-stu-id="d5aaf-119">Id of the `Reservation` to look at</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5aaf-120">-Rezervde</span><span class="sxs-lookup"><span data-stu-id="d5aaf-120">-ReservationOrder</span></span>
<span data-ttu-id="d5aaf-121">İçin yöneltme nesnesi parametresi `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="d5aaf-121">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder
Parameter Sets: PipeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5aaf-122">-Rezervationorderıd</span><span class="sxs-lookup"><span data-stu-id="d5aaf-122">-ReservationOrderId</span></span>
<span data-ttu-id="d5aaf-123">`ReservationOrder`, `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="d5aaf-123">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="d5aaf-124">Gerekli.</span><span class="sxs-lookup"><span data-stu-id="d5aaf-124">Required.</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5aaf-125">-Rezervationorderpage</span><span class="sxs-lookup"><span data-stu-id="d5aaf-125">-ReservationOrderPage</span></span>
<span data-ttu-id="d5aaf-126">İçin yöneltme nesnesi parametresi `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="d5aaf-126">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage
Parameter Sets: PagePipeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5aaf-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5aaf-127">CommonParameters</span></span>
<span data-ttu-id="d5aaf-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d5aaf-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5aaf-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5aaf-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5aaf-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d5aaf-130">INPUTS</span></span>

### <span data-ttu-id="d5aaf-131">System. Guid</span><span class="sxs-lookup"><span data-stu-id="d5aaf-131">System.Guid</span></span>

### <span data-ttu-id="d5aaf-132">Microsoft. Azure. Commands. rezervasyonlar. model. psrezerv</span><span class="sxs-lookup"><span data-stu-id="d5aaf-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>
<span data-ttu-id="d5aaf-133">Parametreler: Rezervsayısı (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d5aaf-133">Parameters: ReservationOrder (ByValue)</span></span>

### <span data-ttu-id="d5aaf-134">Microsoft. Azure. Commands. rezervasyonlar. modeller. Psrezervationorderpage</span><span class="sxs-lookup"><span data-stu-id="d5aaf-134">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>
<span data-ttu-id="d5aaf-135">Parametreler: Rezervsayısı (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d5aaf-135">Parameters: ReservationOrderPage (ByValue)</span></span>

## <span data-ttu-id="d5aaf-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d5aaf-136">OUTPUTS</span></span>

### <span data-ttu-id="d5aaf-137">Microsoft. Azure. Commands. rezervasyonlar. modeller. Psrezervationpage</span><span class="sxs-lookup"><span data-stu-id="d5aaf-137">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

### <span data-ttu-id="d5aaf-138">Microsoft. Azure. Commands. Reservation. modeller. Psreservatıon</span><span class="sxs-lookup"><span data-stu-id="d5aaf-138">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="d5aaf-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d5aaf-139">NOTES</span></span>

## <span data-ttu-id="d5aaf-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d5aaf-140">RELATED LINKS</span></span>
