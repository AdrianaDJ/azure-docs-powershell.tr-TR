---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionreservationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationDetail.md
ms.openlocfilehash: 0776e824d9463a0577f64f2b19f0d71ece29cfa0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917615"
---
# <span data-ttu-id="4db08-101">Get-AzConsumptionReservationDetail</span><span class="sxs-lookup"><span data-stu-id="4db08-101">Get-AzConsumptionReservationDetail</span></span>

## <span data-ttu-id="4db08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4db08-102">SYNOPSIS</span></span>
<span data-ttu-id="4db08-103">Sağlanan tarih aralığı için rezervasyonlar bilgilerini alın.</span><span class="sxs-lookup"><span data-stu-id="4db08-103">Get reservations details for provided date range.</span></span>

## <span data-ttu-id="4db08-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4db08-104">SYNTAX</span></span>

```
Get-AzConsumptionReservationDetail -StartDate <DateTime> -EndDate <DateTime> -ReservationOrderId <String>
 [-ReservationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4db08-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4db08-105">DESCRIPTION</span></span>
<span data-ttu-id="4db08-106">**Get-Azsarf Mptionrezervationdetail** cmdlet 'i, sağlanan tarih aralığı için rezervasyonlar ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="4db08-106">The **Get-AzConsumptionReservationDetail** cmdlet gets reservations details for provided date range.</span></span>

## <span data-ttu-id="4db08-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4db08-107">EXAMPLES</span></span>

### <span data-ttu-id="4db08-108">Örnek 1: sağlanan tarih aralığı için rezervasyon sipariş kimliğiyle rezervasyon ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="4db08-108">Example 1: Get reservation details with reservation order Id for provided date range</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationDetail -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -StartDate 2017-10-01 -EndDate 2017-12-07
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640providers/Microsoft.Consumption/reservationDetails/20171007
InstanceId:  subscriptions/a98d6dc5-eb8f-46cf-8938-f1fb08f03706/resourcegroups/testrg/providers/microsoft.compute/virtualmachines/std2swindows
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20171007
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  24
SkuName:  Standard_DS2_v2
TotalReservedQuantity:  1
Type:  Microsoft.Consumption/reservationDetails
UsageDate:  10/7/2017 12:00:00 AM
UsedHour:  24
```

### <span data-ttu-id="4db08-109">Örnek 2: sağlanan tarih aralığı için rezervasyon</span><span class="sxs-lookup"><span data-stu-id="4db08-109">Example 2: Get reservation details with reservation order Id and reservation Id for provided date range</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationDetail -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -ReservationId f37f4b70-52ba-4344-a8bd-28abfd21d640 -StartDate 2017-10-01 -EndDate 2017-12-07
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640providers/Microsoft.Consumption/reservationDetails/20171007
InstanceId:  subscriptions/a98d6dc5-eb8f-46cf-8938-f1fb08f03706/resourcegroups/testrg/providers/microsoft.compute/virtualmachines/std2swindows
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20171007
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  24
SkuName:  Standard_DS2_v2
TotalReservedQuantity:  1
Type:  Microsoft.Consumption/reservationDetails
UsageDate:  10/7/2017 12:00:00 AM
UsedHour:  24
```

## <span data-ttu-id="4db08-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4db08-110">PARAMETERS</span></span>

### <span data-ttu-id="4db08-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4db08-111">-DefaultProfile</span></span>
<span data-ttu-id="4db08-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4db08-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4db08-113">-EndDate</span><span class="sxs-lookup"><span data-stu-id="4db08-113">-EndDate</span></span>
<span data-ttu-id="4db08-114">Ayırma detaysının son verileri (UTC 'deki YYYY-AA-GG).</span><span class="sxs-lookup"><span data-stu-id="4db08-114">The end data (YYYY-MM-DD in UTC) of the reservation detail.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4db08-115">-Rezervationıd</span><span class="sxs-lookup"><span data-stu-id="4db08-115">-ReservationId</span></span>
<span data-ttu-id="4db08-116">Rezervasyon sırasındaki rezervasyonun tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="4db08-116">The identifier of a reservation within a reservation order.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4db08-117">-Rezervationorderıd</span><span class="sxs-lookup"><span data-stu-id="4db08-117">-ReservationOrderId</span></span>
<span data-ttu-id="4db08-118">Bir rezervasyon satınalmanın tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="4db08-118">The identifier of a reservation purchase.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4db08-119">-StartDate</span><span class="sxs-lookup"><span data-stu-id="4db08-119">-StartDate</span></span>
<span data-ttu-id="4db08-120">Ayırma detaysının başlangıç verileri (UTC 'deki YYYY-AA-GG).</span><span class="sxs-lookup"><span data-stu-id="4db08-120">The start data (YYYY-MM-DD in UTC) of the reservation detail.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4db08-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4db08-121">CommonParameters</span></span>
<span data-ttu-id="4db08-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4db08-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4db08-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4db08-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4db08-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4db08-124">INPUTS</span></span>

### <span data-ttu-id="4db08-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4db08-125">None</span></span>

## <span data-ttu-id="4db08-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4db08-126">OUTPUTS</span></span>

### <span data-ttu-id="4db08-127">Microsoft. Azure. Commands. tüketim. model. Psrezervationdetail</span><span class="sxs-lookup"><span data-stu-id="4db08-127">Microsoft.Azure.Commands.Consumption.Models.PSReservationDetail</span></span>

## <span data-ttu-id="4db08-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4db08-128">NOTES</span></span>

## <span data-ttu-id="4db08-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4db08-129">RELATED LINKS</span></span>