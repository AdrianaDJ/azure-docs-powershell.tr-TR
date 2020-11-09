---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
ms.openlocfilehash: 15faf94ae7e0afac7200423dcd36d8edf2964c21
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324376"
---
# <span data-ttu-id="1b578-101">Get-AzReservationOrder</span><span class="sxs-lookup"><span data-stu-id="1b578-101">Get-AzReservationOrder</span></span>

## <span data-ttu-id="1b578-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b578-102">SYNOPSIS</span></span>
<span data-ttu-id="1b578-103">Al `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="1b578-103">Get `ReservationOrder`</span></span>

## <span data-ttu-id="1b578-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1b578-104">SYNTAX</span></span>

```
Get-AzReservationOrder [-ReservationOrderId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1b578-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1b578-105">DESCRIPTION</span></span>
<span data-ttu-id="1b578-106">`ReservationOrder`Kullanıcının geçerli kiracıda erişimi olan tüm s listesi.</span><span class="sxs-lookup"><span data-stu-id="1b578-106">List of all the `ReservationOrder`s that the user has access to in the current tenant.</span></span> <span data-ttu-id="1b578-107">Rezervdeğer = parametre ayarlanmışsa, bu belirli Rezervtalebi siparişini alın.</span><span class="sxs-lookup"><span data-stu-id="1b578-107">If ReservationOrderId parameter is set, get that specific ReservationOrder.</span></span>

## <span data-ttu-id="1b578-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1b578-108">EXAMPLES</span></span>

### <span data-ttu-id="1b578-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1b578-109">Example 1</span></span>
```
PS C:\> Get-AzReservationOrder
```

<span data-ttu-id="1b578-110">`ReservationOrder`Kullanıcının geçerli kiracıya erişiminin olduğu tüm liste</span><span class="sxs-lookup"><span data-stu-id="1b578-110">List all `ReservationOrder` that the user has access to in the current tenant</span></span>

### <span data-ttu-id="1b578-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="1b578-111">Example 2</span></span>
```
PS C:\> Get-AzReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="1b578-112">`ReservationOrder`Belirtilen Rezervorderıd siparişiyle birlikte</span><span class="sxs-lookup"><span data-stu-id="1b578-112">Get `ReservationOrder` with the specified ReservationOrderId</span></span>

## <span data-ttu-id="1b578-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1b578-113">PARAMETERS</span></span>

### <span data-ttu-id="1b578-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b578-114">-DefaultProfile</span></span>
<span data-ttu-id="1b578-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1b578-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b578-116">-Rezervationorderıd</span><span class="sxs-lookup"><span data-stu-id="1b578-116">-ReservationOrderId</span></span>
<span data-ttu-id="1b578-117">Kullanıcının görmek istediği belirli Rezervsırası kodu</span><span class="sxs-lookup"><span data-stu-id="1b578-117">Id of the specific ReservationOrder that user wants to see</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b578-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b578-118">CommonParameters</span></span>
<span data-ttu-id="1b578-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1b578-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b578-120">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1b578-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b578-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1b578-121">INPUTS</span></span>

### <span data-ttu-id="1b578-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1b578-122">None</span></span>

## <span data-ttu-id="1b578-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1b578-123">OUTPUTS</span></span>

### <span data-ttu-id="1b578-124">Microsoft. Azure. Commands. rezervasyonlar. modeller. Psrezervationorderpage</span><span class="sxs-lookup"><span data-stu-id="1b578-124">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

### <span data-ttu-id="1b578-125">Microsoft. Azure. Commands. rezervasyonlar. model. psrezerv</span><span class="sxs-lookup"><span data-stu-id="1b578-125">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

## <span data-ttu-id="1b578-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1b578-126">NOTES</span></span>

## <span data-ttu-id="1b578-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1b578-127">RELATED LINKS</span></span>
