---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservationOrder.md
ms.openlocfilehash: 12e76c3412f54ba840528f9ff1a40acd388cd109
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588392"
---
# <span data-ttu-id="73ceb-101">Get-AzureRmReservationOrder</span><span class="sxs-lookup"><span data-stu-id="73ceb-101">Get-AzureRmReservationOrder</span></span>

## <span data-ttu-id="73ceb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73ceb-102">SYNOPSIS</span></span>
<span data-ttu-id="73ceb-103">Al `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="73ceb-103">Get `ReservationOrder`</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73ceb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="73ceb-104">SYNTAX</span></span>

```
Get-AzureRmReservationOrder [-ReservationOrderId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="73ceb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="73ceb-105">DESCRIPTION</span></span>
<span data-ttu-id="73ceb-106">`ReservationOrder`Kullanıcının geçerli kiracıda erişimi olan tüm s listesi.</span><span class="sxs-lookup"><span data-stu-id="73ceb-106">List of all the `ReservationOrder`s that the user has access to in the current tenant.</span></span> <span data-ttu-id="73ceb-107">Rezervdeğer = parametre ayarlanmışsa, bu belirli Rezervtalebi siparişini alın.</span><span class="sxs-lookup"><span data-stu-id="73ceb-107">If ReservationOrderId parameter is set, get that specific ReservationOrder.</span></span>

## <span data-ttu-id="73ceb-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="73ceb-108">EXAMPLES</span></span>

### <span data-ttu-id="73ceb-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="73ceb-109">Example 1</span></span>
```
PS C:\> Get-AzureRmReservationOrder
```

<span data-ttu-id="73ceb-110">`ReservationOrder`Kullanıcının geçerli kiracıya erişiminin olduğu tüm liste</span><span class="sxs-lookup"><span data-stu-id="73ceb-110">List all `ReservationOrder` that the user has access to in the current tenant</span></span>

### <span data-ttu-id="73ceb-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="73ceb-111">Example 2</span></span>
```
PS C:\> Get-AzureRmReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="73ceb-112">`ReservationOrder`Belirtilen Rezervorderıd siparişiyle birlikte</span><span class="sxs-lookup"><span data-stu-id="73ceb-112">Get `ReservationOrder` with the specified ReservationOrderId</span></span>

## <span data-ttu-id="73ceb-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="73ceb-113">PARAMETERS</span></span>

### <span data-ttu-id="73ceb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73ceb-114">-DefaultProfile</span></span>
<span data-ttu-id="73ceb-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="73ceb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73ceb-116">-Rezervationorderıd</span><span class="sxs-lookup"><span data-stu-id="73ceb-116">-ReservationOrderId</span></span>
<span data-ttu-id="73ceb-117">Kullanıcının görmek istediği belirli Rezervsırası kodu</span><span class="sxs-lookup"><span data-stu-id="73ceb-117">Id of the specific ReservationOrder that user wants to see</span></span>

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

### <span data-ttu-id="73ceb-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73ceb-118">CommonParameters</span></span>
<span data-ttu-id="73ceb-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="73ceb-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73ceb-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73ceb-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73ceb-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="73ceb-121">INPUTS</span></span>

### <span data-ttu-id="73ceb-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="73ceb-122">None</span></span>

## <span data-ttu-id="73ceb-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="73ceb-123">OUTPUTS</span></span>

### <span data-ttu-id="73ceb-124">Microsoft. Azure. Commands. rezervasyonlar. modeller. Psrezervationorderpage</span><span class="sxs-lookup"><span data-stu-id="73ceb-124">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

### <span data-ttu-id="73ceb-125">Microsoft. Azure. Commands. rezervasyonlar. model. psrezerv</span><span class="sxs-lookup"><span data-stu-id="73ceb-125">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

## <span data-ttu-id="73ceb-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="73ceb-126">NOTES</span></span>

## <span data-ttu-id="73ceb-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="73ceb-127">RELATED LINKS</span></span>
