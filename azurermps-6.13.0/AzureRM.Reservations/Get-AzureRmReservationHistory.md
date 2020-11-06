---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationHistory.md
ms.openlocfilehash: 3149e2fa0ef748d11583919161555805d54f5efc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595065"
---
# <span data-ttu-id="050bb-101">Get-AzureRmReservationHistory</span><span class="sxs-lookup"><span data-stu-id="050bb-101">Get-AzureRmReservationHistory</span></span>

## <span data-ttu-id="050bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="050bb-102">SYNOPSIS</span></span>
<span data-ttu-id="050bb-103">`Reservation`Düzeltme geçmişi alın.</span><span class="sxs-lookup"><span data-stu-id="050bb-103">Get `Reservation` revision history.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="050bb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="050bb-104">SYNTAX</span></span>

### <span data-ttu-id="050bb-105">CommandLine (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="050bb-105">CommandLine (Default)</span></span>
```
Get-AzureRmReservationHistory -ReservationOrderId <Guid> -ReservationId <Guid>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="050bb-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="050bb-106">PipeObject</span></span>
```
Get-AzureRmReservationHistory -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="050bb-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="050bb-107">DESCRIPTION</span></span>
<span data-ttu-id="050bb-108">İçin tüm düzeltmelerin listesi `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="050bb-108">List of all the revisions for the `Reservation`.</span></span>

## <span data-ttu-id="050bb-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="050bb-109">EXAMPLES</span></span>

### <span data-ttu-id="050bb-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="050bb-110">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationHistory -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="050bb-111">Belirli bir ayırmanın düzeltme geçmişini alma</span><span class="sxs-lookup"><span data-stu-id="050bb-111">Get the revision history of the specific reservation</span></span>

## <span data-ttu-id="050bb-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="050bb-112">PARAMETERS</span></span>

### <span data-ttu-id="050bb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="050bb-113">-DefaultProfile</span></span>
<span data-ttu-id="050bb-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="050bb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="050bb-115">-Ayırma</span><span class="sxs-lookup"><span data-stu-id="050bb-115">-Reservation</span></span>
<span data-ttu-id="050bb-116">S için kanal nesnesi parametresi `Reservation`</span><span class="sxs-lookup"><span data-stu-id="050bb-116">Pipe object parameter for `Reservation`s</span></span>

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

### <span data-ttu-id="050bb-117">-Rezervationıd</span><span class="sxs-lookup"><span data-stu-id="050bb-117">-ReservationId</span></span>
<span data-ttu-id="050bb-118">`Reservation`Hangi geçmişin gösterileceğini belirten Rezervkimliği</span><span class="sxs-lookup"><span data-stu-id="050bb-118">ReservationId of the `Reservation` of which history is to be shown</span></span>

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

### <span data-ttu-id="050bb-119">-Rezervationorderıd</span><span class="sxs-lookup"><span data-stu-id="050bb-119">-ReservationOrderId</span></span>
<span data-ttu-id="050bb-120">İçin `ReservationOrder` , `Reservation`</span><span class="sxs-lookup"><span data-stu-id="050bb-120">ReservationOrderId for the `ReservationOrder` that contains the `Reservation`</span></span>

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

### <span data-ttu-id="050bb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="050bb-121">CommonParameters</span></span>
<span data-ttu-id="050bb-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="050bb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="050bb-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="050bb-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="050bb-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="050bb-124">INPUTS</span></span>

### <span data-ttu-id="050bb-125">System. Guid</span><span class="sxs-lookup"><span data-stu-id="050bb-125">System.Guid</span></span>

### <span data-ttu-id="050bb-126">Microsoft. Azure. Commands. Reservation. modeller. Psreservatıon</span><span class="sxs-lookup"><span data-stu-id="050bb-126">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>
<span data-ttu-id="050bb-127">Parametreler: Reservation (ByValue)</span><span class="sxs-lookup"><span data-stu-id="050bb-127">Parameters: Reservation (ByValue)</span></span>

## <span data-ttu-id="050bb-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="050bb-128">OUTPUTS</span></span>

### <span data-ttu-id="050bb-129">Microsoft. Azure. Commands. rezervasyonlar. modeller. Psrezervationpage</span><span class="sxs-lookup"><span data-stu-id="050bb-129">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

## <span data-ttu-id="050bb-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="050bb-130">NOTES</span></span>

## <span data-ttu-id="050bb-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="050bb-131">RELATED LINKS</span></span>
