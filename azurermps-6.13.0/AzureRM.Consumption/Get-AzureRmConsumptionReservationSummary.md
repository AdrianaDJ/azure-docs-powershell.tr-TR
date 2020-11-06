---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.consumption/get-azurermconsumptionreservationsummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionReservationSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionReservationSummary.md
ms.openlocfilehash: 18f12e6ccf7f43aa832c00864192142457f45520
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592024"
---
# <span data-ttu-id="09155-101">Get-AzureRmConsumptionReservationSummary</span><span class="sxs-lookup"><span data-stu-id="09155-101">Get-AzureRmConsumptionReservationSummary</span></span>

## <span data-ttu-id="09155-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09155-102">SYNOPSIS</span></span>
<span data-ttu-id="09155-103">Günlük veya aylık Gren için rezervasyon özetlerini alın.</span><span class="sxs-lookup"><span data-stu-id="09155-103">Get reservation summaries for daily or monthly grain.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09155-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="09155-104">SYNTAX</span></span>

```
Get-AzureRmConsumptionReservationSummary -Grain <String> -ReservationOrderId <String> [-ReservationId <String>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09155-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="09155-105">DESCRIPTION</span></span>
<span data-ttu-id="09155-106">**Get-Azurermtüketimptionrezervheerererererererererererer**</span><span class="sxs-lookup"><span data-stu-id="09155-106">The **Get-AzureRmConsumptionReservationSummay** cmdlet gets reservation summaries for daily or monthly grain.</span></span>

## <span data-ttu-id="09155-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="09155-107">EXAMPLES</span></span>

### <span data-ttu-id="09155-108">Örnek 1: aylık grenin RESERVATION Order ID ile rezervasyon özetlerini alma</span><span class="sxs-lookup"><span data-stu-id="09155-108">Example 1: Get reservation summaries with reservation order Id for monthly grain</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionReservationSummary -Grain monthly -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b
AvgUtilizationPercentage:  100
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640/providers/Microsoft.Consumption/reservationSummaries/20170901
MaxUtilizationPercentage:  100
MinUtilizationPercentage:  100
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20170901
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  288
SkuName:  Standard_DS2_v2
Type:  Microsoft.Consumption/reservationSummaries
UsageDate:  9/1/2017 12:00:00 AM
UsedHour:  288
```

### <span data-ttu-id="09155-109">Örnek 2: bir aylık grenin rezervasyonu</span><span class="sxs-lookup"><span data-stu-id="09155-109">Example 2: Get reservation summaries with reservation order Id and reservation Id for monthly grain</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionReservationSummary -Grain monthly -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -ReservationId f37f4b70-52ba-4344-a8bd-28abfd21d640
AvgUtilizationPercentage:  100
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640/providers/Microsoft.Consumption/reservationSummaries/20170901
MaxUtilizationPercentage:  100
MinUtilizationPercentage:  100
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20170901
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  288
SkuName:  Standard_DS2_v2
Type:  Microsoft.Consumption/reservationSummaries
UsageDate:  9/1/2017 12:00:00 AM
UsedHour:  288
```

### <span data-ttu-id="09155-110">Örnek 3: günlük noktalı, rezervasyon sipariş kimliği</span><span class="sxs-lookup"><span data-stu-id="09155-110">Example 3: Get reservation summaries with reservation order Id for daily grain provided date range</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionReservationSummary -Grain daily -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -StartDate 2017-10-01 -EndDate 2017-12-07
AvgUtilizationPercentage:  100
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640/providers/Microsoft.Consumption/reservationSummaries/20171101
MaxUtilizationPercentage:  100
MinUtilizationPercentage:  100
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20171101
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  24
SkuName:  Standard_DS2_v2
Type:  Microsoft.Consumption/reservationSummaries
UsageDate:  11/1/2017 12:00:00 AM
UsedHour:  24
```

### <span data-ttu-id="09155-111">Örnek 4: rezervasyon düzeni kimliği ve rezervasyon kimliği</span><span class="sxs-lookup"><span data-stu-id="09155-111">Example 4: Get reservation summaries with reservation order Id and reservation Id for daily grain provided date range</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionReservationSummary -Grain daily -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -ReservationId f37f4b70-52ba-4344-a8bd-28abfd21d640 -StartDate 2017-10-01 -EndDate 2017-12-07
AvgUtilizationPercentage:  100
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640/providers/Microsoft.Consumption/reservationSummaries/20171101
MaxUtilizationPercentage:  100
MinUtilizationPercentage:  100
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20171101
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  24
SkuName:  Standard_DS2_v2
Type:  Microsoft.Consumption/reservationSummaries
UsageDate:  11/1/2017 12:00:00 AM
UsedHour:  24
```

## <span data-ttu-id="09155-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="09155-112">PARAMETERS</span></span>

### <span data-ttu-id="09155-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09155-113">-DefaultProfile</span></span>
<span data-ttu-id="09155-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="09155-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09155-115">-EndDate</span><span class="sxs-lookup"><span data-stu-id="09155-115">-EndDate</span></span>
<span data-ttu-id="09155-116">Rezervasyon özetinin son verileri (YYYY-AA-DD); yalnızca günlük greiçin gereklidir.</span><span class="sxs-lookup"><span data-stu-id="09155-116">The end data (YYYY-MM-DD in UTC) of the reservation summary, required only for daily grain.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09155-117">Noktalı</span><span class="sxs-lookup"><span data-stu-id="09155-117">-Grain</span></span>
<span data-ttu-id="09155-118">Reservation summaryy zaman çizgisi, günlük veya aylık olabilir.</span><span class="sxs-lookup"><span data-stu-id="09155-118">The time grain of the reservation summaryy, can be daily or monthly.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: daily, monthly

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09155-119">-Rezervationıd</span><span class="sxs-lookup"><span data-stu-id="09155-119">-ReservationId</span></span>
<span data-ttu-id="09155-120">Rezervasyon sırasındaki rezervasyonun tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="09155-120">The identifier of a reservation within a reservation order.</span></span>

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

### <span data-ttu-id="09155-121">-Rezervationorderıd</span><span class="sxs-lookup"><span data-stu-id="09155-121">-ReservationOrderId</span></span>
<span data-ttu-id="09155-122">Bir rezervasyon satınalmanın tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="09155-122">The identifier of a reservation purchase.</span></span>

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

### <span data-ttu-id="09155-123">-StartDate</span><span class="sxs-lookup"><span data-stu-id="09155-123">-StartDate</span></span>
<span data-ttu-id="09155-124">Rezervasyon özetinin başlangıç verileri (YYYY-AA-DD); yalnızca günlük greiçin gereklidir.</span><span class="sxs-lookup"><span data-stu-id="09155-124">The start data (YYYY-MM-DD in UTC) of the reservation summary, required only for daily grain.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09155-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09155-125">CommonParameters</span></span>
<span data-ttu-id="09155-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="09155-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09155-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09155-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09155-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="09155-128">INPUTS</span></span>

### <span data-ttu-id="09155-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="09155-129">None</span></span>

## <span data-ttu-id="09155-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="09155-130">OUTPUTS</span></span>

### <span data-ttu-id="09155-131">Microsoft. Azure. Commands. tüketim. modeller. Psrezervationsummary</span><span class="sxs-lookup"><span data-stu-id="09155-131">Microsoft.Azure.Commands.Consumption.Models.PSReservationSummary</span></span>

## <span data-ttu-id="09155-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="09155-132">NOTES</span></span>

## <span data-ttu-id="09155-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="09155-133">RELATED LINKS</span></span>
