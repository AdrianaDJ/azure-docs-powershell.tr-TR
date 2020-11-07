---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationHistory.md
ms.openlocfilehash: cfc7ab08904f007f874e1b45fd6d27a5712abee9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938133"
---
# <span data-ttu-id="e4c72-101">Get-AzReservationHistory</span><span class="sxs-lookup"><span data-stu-id="e4c72-101">Get-AzReservationHistory</span></span>

## <span data-ttu-id="e4c72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4c72-102">SYNOPSIS</span></span>
<span data-ttu-id="e4c72-103">`Reservation`Düzeltme geçmişi alın.</span><span class="sxs-lookup"><span data-stu-id="e4c72-103">Get `Reservation` revision history.</span></span>

## <span data-ttu-id="e4c72-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e4c72-104">SYNTAX</span></span>

### <span data-ttu-id="e4c72-105">CommandLine (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e4c72-105">CommandLine (Default)</span></span>
```
Get-AzReservationHistory -ReservationOrderId <Guid> -ReservationId <Guid>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4c72-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="e4c72-106">PipeObject</span></span>
```
Get-AzReservationHistory -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e4c72-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e4c72-107">DESCRIPTION</span></span>
<span data-ttu-id="e4c72-108">İçin tüm düzeltmelerin listesi `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="e4c72-108">List of all the revisions for the `Reservation`.</span></span>

## <span data-ttu-id="e4c72-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e4c72-109">EXAMPLES</span></span>

### <span data-ttu-id="e4c72-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e4c72-110">Example 1</span></span>
```
PS C:\> Get-AzReservationHistory -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="e4c72-111">Belirli bir ayırmanın düzeltme geçmişini alma</span><span class="sxs-lookup"><span data-stu-id="e4c72-111">Get the revision history of the specific reservation</span></span>

## <span data-ttu-id="e4c72-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e4c72-112">PARAMETERS</span></span>

### <span data-ttu-id="e4c72-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4c72-113">-DefaultProfile</span></span>
<span data-ttu-id="e4c72-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e4c72-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4c72-115">-Ayırma</span><span class="sxs-lookup"><span data-stu-id="e4c72-115">-Reservation</span></span>
<span data-ttu-id="e4c72-116">S için kanal nesnesi parametresi `Reservation`</span><span class="sxs-lookup"><span data-stu-id="e4c72-116">Pipe object parameter for `Reservation`s</span></span>

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

### <span data-ttu-id="e4c72-117">-Rezervationıd</span><span class="sxs-lookup"><span data-stu-id="e4c72-117">-ReservationId</span></span>
<span data-ttu-id="e4c72-118">`Reservation`Hangi geçmişin gösterileceğini belirten Rezervkimliği</span><span class="sxs-lookup"><span data-stu-id="e4c72-118">ReservationId of the `Reservation` of which history is to be shown</span></span>

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

### <span data-ttu-id="e4c72-119">-Rezervationorderıd</span><span class="sxs-lookup"><span data-stu-id="e4c72-119">-ReservationOrderId</span></span>
<span data-ttu-id="e4c72-120">İçin `ReservationOrder` , `Reservation`</span><span class="sxs-lookup"><span data-stu-id="e4c72-120">ReservationOrderId for the `ReservationOrder` that contains the `Reservation`</span></span>

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

### <span data-ttu-id="e4c72-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4c72-121">CommonParameters</span></span>
<span data-ttu-id="e4c72-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e4c72-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4c72-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e4c72-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4c72-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e4c72-124">INPUTS</span></span>

### <span data-ttu-id="e4c72-125">System. Guid</span><span class="sxs-lookup"><span data-stu-id="e4c72-125">System.Guid</span></span>

### <span data-ttu-id="e4c72-126">Microsoft. Azure. Commands. Reservation. modeller. Psreservatıon</span><span class="sxs-lookup"><span data-stu-id="e4c72-126">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="e4c72-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e4c72-127">OUTPUTS</span></span>

### <span data-ttu-id="e4c72-128">Microsoft. Azure. Commands. rezervasyonlar. modeller. Psrezervationpage</span><span class="sxs-lookup"><span data-stu-id="e4c72-128">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

## <span data-ttu-id="e4c72-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e4c72-129">NOTES</span></span>

## <span data-ttu-id="e4c72-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e4c72-130">RELATED LINKS</span></span>
