---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrder.md
ms.openlocfilehash: 0dc5eba8b498be7814ae74eca6953a5cadb01f22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589700"
---
# <span data-ttu-id="7684c-101">Get-AzureRmReservationOrder</span><span class="sxs-lookup"><span data-stu-id="7684c-101">Get-AzureRmReservationOrder</span></span>

## <span data-ttu-id="7684c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7684c-102">SYNOPSIS</span></span>
<span data-ttu-id="7684c-103">Al `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="7684c-103">Get `ReservationOrder`</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7684c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7684c-104">SYNTAX</span></span>

```
Get-AzureRmReservationOrder [-ReservationOrderId <String>] [<CommonParameters>]
```

## <span data-ttu-id="7684c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7684c-105">DESCRIPTION</span></span>
<span data-ttu-id="7684c-106">`ReservationOrder`Kullanıcının geçerli kiracıda erişimi olan tüm s listesi.</span><span class="sxs-lookup"><span data-stu-id="7684c-106">List of all the `ReservationOrder`s that the user has access to in the current tenant.</span></span> <span data-ttu-id="7684c-107">Rezervdeğer = parametre ayarlanmışsa, bu belirli Rezervtalebi siparişini alın.</span><span class="sxs-lookup"><span data-stu-id="7684c-107">If ReservationOrderId parameter is set, get that specific ReservationOrder.</span></span>

## <span data-ttu-id="7684c-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7684c-108">EXAMPLES</span></span>

### <span data-ttu-id="7684c-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7684c-109">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationOrder
```

<span data-ttu-id="7684c-110">`ReservationOrder`Kullanıcının geçerli kiracıya erişiminin olduğu tüm liste</span><span class="sxs-lookup"><span data-stu-id="7684c-110">List all `ReservationOrder` that the user has access to in the current tenant</span></span>

### <span data-ttu-id="7684c-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="7684c-111">Example 2</span></span>
```
PS C:\> Get-AzureRmReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="7684c-112">`ReservationOrder`Belirtilen Rezervorderıd siparişiyle birlikte</span><span class="sxs-lookup"><span data-stu-id="7684c-112">Get `ReservationOrder` with the specified ReservationOrderId</span></span>

## <span data-ttu-id="7684c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7684c-113">PARAMETERS</span></span>

### <span data-ttu-id="7684c-114">-Rezervationorderıd</span><span class="sxs-lookup"><span data-stu-id="7684c-114">-ReservationOrderId</span></span>
<span data-ttu-id="7684c-115">Kullanıcının görmek istediği belirli Rezervsırası kodu</span><span class="sxs-lookup"><span data-stu-id="7684c-115">Id of the specific ReservationOrder that user wants to see</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7684c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7684c-116">CommonParameters</span></span>
<span data-ttu-id="7684c-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7684c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7684c-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7684c-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7684c-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7684c-119">INPUTS</span></span>

### <span data-ttu-id="7684c-120">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7684c-120">None</span></span>

## <span data-ttu-id="7684c-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7684c-121">OUTPUTS</span></span>

### <span data-ttu-id="7684c-122">Microsoft. Azure. Commands. rezervasyonlar. modeller. Psrezervationorderpage</span><span class="sxs-lookup"><span data-stu-id="7684c-122">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>
<span data-ttu-id="7684c-123">Microsoft. Azure. Commands. rezervasyonlar. model. psrezerv</span><span class="sxs-lookup"><span data-stu-id="7684c-123">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

## <span data-ttu-id="7684c-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7684c-124">NOTES</span></span>

## <span data-ttu-id="7684c-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7684c-125">RELATED LINKS</span></span>

