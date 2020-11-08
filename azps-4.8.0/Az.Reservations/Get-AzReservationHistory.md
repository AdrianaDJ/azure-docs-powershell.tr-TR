---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationHistory.md
ms.openlocfilehash: cfc7ab08904f007f874e1b45fd6d27a5712abee9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266472"
---
# <span data-ttu-id="e0bd1-101">Get-AzReservationHistory</span><span class="sxs-lookup"><span data-stu-id="e0bd1-101">Get-AzReservationHistory</span></span>

## <span data-ttu-id="e0bd1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0bd1-102">SYNOPSIS</span></span>
<span data-ttu-id="e0bd1-103">`Reservation`Düzeltme geçmişi alın.</span><span class="sxs-lookup"><span data-stu-id="e0bd1-103">Get `Reservation` revision history.</span></span>

## <span data-ttu-id="e0bd1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e0bd1-104">SYNTAX</span></span>

### <span data-ttu-id="e0bd1-105">CommandLine (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e0bd1-105">CommandLine (Default)</span></span>
```
Get-AzReservationHistory -ReservationOrderId <Guid> -ReservationId <Guid>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0bd1-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="e0bd1-106">PipeObject</span></span>
```
Get-AzReservationHistory -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e0bd1-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e0bd1-107">DESCRIPTION</span></span>
<span data-ttu-id="e0bd1-108">İçin tüm düzeltmelerin listesi `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="e0bd1-108">List of all the revisions for the `Reservation`.</span></span>

## <span data-ttu-id="e0bd1-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e0bd1-109">EXAMPLES</span></span>

### <span data-ttu-id="e0bd1-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e0bd1-110">Example 1</span></span>
```
PS C:\> Get-AzReservationHistory -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="e0bd1-111">Belirli bir ayırmanın düzeltme geçmişini alma</span><span class="sxs-lookup"><span data-stu-id="e0bd1-111">Get the revision history of the specific reservation</span></span>

## <span data-ttu-id="e0bd1-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e0bd1-112">PARAMETERS</span></span>

### <span data-ttu-id="e0bd1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0bd1-113">-DefaultProfile</span></span>
<span data-ttu-id="e0bd1-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e0bd1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0bd1-115">-Ayırma</span><span class="sxs-lookup"><span data-stu-id="e0bd1-115">-Reservation</span></span>
<span data-ttu-id="e0bd1-116">S için kanal nesnesi parametresi `Reservation`</span><span class="sxs-lookup"><span data-stu-id="e0bd1-116">Pipe object parameter for `Reservation`s</span></span>

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

### <span data-ttu-id="e0bd1-117">-Rezervationıd</span><span class="sxs-lookup"><span data-stu-id="e0bd1-117">-ReservationId</span></span>
<span data-ttu-id="e0bd1-118">`Reservation`Hangi geçmişin gösterileceğini belirten Rezervkimliği</span><span class="sxs-lookup"><span data-stu-id="e0bd1-118">ReservationId of the `Reservation` of which history is to be shown</span></span>

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

### <span data-ttu-id="e0bd1-119">-Rezervationorderıd</span><span class="sxs-lookup"><span data-stu-id="e0bd1-119">-ReservationOrderId</span></span>
<span data-ttu-id="e0bd1-120">İçin `ReservationOrder` , `Reservation`</span><span class="sxs-lookup"><span data-stu-id="e0bd1-120">ReservationOrderId for the `ReservationOrder` that contains the `Reservation`</span></span>

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

### <span data-ttu-id="e0bd1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0bd1-121">CommonParameters</span></span>
<span data-ttu-id="e0bd1-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e0bd1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0bd1-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e0bd1-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0bd1-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e0bd1-124">INPUTS</span></span>

### <span data-ttu-id="e0bd1-125">System. Guid</span><span class="sxs-lookup"><span data-stu-id="e0bd1-125">System.Guid</span></span>

### <span data-ttu-id="e0bd1-126">Microsoft. Azure. Commands. Reservation. modeller. Psreservatıon</span><span class="sxs-lookup"><span data-stu-id="e0bd1-126">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="e0bd1-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e0bd1-127">OUTPUTS</span></span>

### <span data-ttu-id="e0bd1-128">Microsoft. Azure. Commands. rezervasyonlar. modeller. Psrezervationpage</span><span class="sxs-lookup"><span data-stu-id="e0bd1-128">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

## <span data-ttu-id="e0bd1-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e0bd1-129">NOTES</span></span>

## <span data-ttu-id="e0bd1-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e0bd1-130">RELATED LINKS</span></span>
