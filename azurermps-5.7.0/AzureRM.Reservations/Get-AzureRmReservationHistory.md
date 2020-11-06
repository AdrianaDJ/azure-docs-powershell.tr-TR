---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationHistory.md
ms.openlocfilehash: 75ff92efe1a37e55396da7dc6d644408952ed179
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592416"
---
# <span data-ttu-id="b0a9d-101">Get-AzureRmReservationHistory</span><span class="sxs-lookup"><span data-stu-id="b0a9d-101">Get-AzureRmReservationHistory</span></span>

## <span data-ttu-id="b0a9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0a9d-102">SYNOPSIS</span></span>
<span data-ttu-id="b0a9d-103">`Reservation`Düzeltme geçmişi alın.</span><span class="sxs-lookup"><span data-stu-id="b0a9d-103">Get `Reservation` revision history.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0a9d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b0a9d-104">SYNTAX</span></span>

### <span data-ttu-id="b0a9d-105">CommandLine (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b0a9d-105">CommandLine (Default)</span></span>
```
Get-AzureRmReservationHistory -ReservationOrderId <String> -ReservationId <String> [<CommonParameters>]
```

### <span data-ttu-id="b0a9d-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="b0a9d-106">PipeObject</span></span>
```
Get-AzureRmReservationHistory -Reservation <PSReservation> [<CommonParameters>]
```

## <span data-ttu-id="b0a9d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b0a9d-107">DESCRIPTION</span></span>
<span data-ttu-id="b0a9d-108">İçin tüm düzeltmelerin listesi `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="b0a9d-108">List of all the revisions for the `Reservation`.</span></span>

## <span data-ttu-id="b0a9d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b0a9d-109">EXAMPLES</span></span>

### <span data-ttu-id="b0a9d-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b0a9d-110">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationHistory -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="b0a9d-111">Belirli bir ayırmanın düzeltme geçmişini alma</span><span class="sxs-lookup"><span data-stu-id="b0a9d-111">Get the revision history of the specific reservation</span></span>

## <span data-ttu-id="b0a9d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b0a9d-112">PARAMETERS</span></span>

### <span data-ttu-id="b0a9d-113">-Ayırma</span><span class="sxs-lookup"><span data-stu-id="b0a9d-113">-Reservation</span></span>
<span data-ttu-id="b0a9d-114">S için kanal nesnesi parametresi `Reservation`</span><span class="sxs-lookup"><span data-stu-id="b0a9d-114">Pipe object parameter for `Reservation`s</span></span>

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

### <span data-ttu-id="b0a9d-115">-Rezervationıd</span><span class="sxs-lookup"><span data-stu-id="b0a9d-115">-ReservationId</span></span>
<span data-ttu-id="b0a9d-116">`Reservation`Hangi geçmişin gösterileceğini belirten Rezervkimliği</span><span class="sxs-lookup"><span data-stu-id="b0a9d-116">ReservationId of the `Reservation` of which history is to be shown</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0a9d-117">-Rezervationorderıd</span><span class="sxs-lookup"><span data-stu-id="b0a9d-117">-ReservationOrderId</span></span>
<span data-ttu-id="b0a9d-118">İçin `ReservationOrder` , `Reservation`</span><span class="sxs-lookup"><span data-stu-id="b0a9d-118">ReservationOrderId for the `ReservationOrder` that contains the `Reservation`</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0a9d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0a9d-119">CommonParameters</span></span>
<span data-ttu-id="b0a9d-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b0a9d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0a9d-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0a9d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0a9d-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b0a9d-122">INPUTS</span></span>

### <span data-ttu-id="b0a9d-123">System. String</span><span class="sxs-lookup"><span data-stu-id="b0a9d-123">System.String</span></span>
<span data-ttu-id="b0a9d-124">Microsoft. Azure. Commands. Reservation. modeller. Psreservatıon</span><span class="sxs-lookup"><span data-stu-id="b0a9d-124">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="b0a9d-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b0a9d-125">OUTPUTS</span></span>

### <span data-ttu-id="b0a9d-126">Microsoft. Azure. Commands. rezervasyonlar. modeller. Psrezervationpage</span><span class="sxs-lookup"><span data-stu-id="b0a9d-126">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

## <span data-ttu-id="b0a9d-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b0a9d-127">NOTES</span></span>

## <span data-ttu-id="b0a9d-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b0a9d-128">RELATED LINKS</span></span>

