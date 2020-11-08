---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionreservationsummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationSummary.md
ms.openlocfilehash: a76254f1aeb369e6f93ed8edccfd6f74ff79ceb0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279102"
---
# <span data-ttu-id="2471e-101">Get-AzConsumptionReservationSummary</span><span class="sxs-lookup"><span data-stu-id="2471e-101">Get-AzConsumptionReservationSummary</span></span>

## <span data-ttu-id="2471e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2471e-102">SYNOPSIS</span></span>
<span data-ttu-id="2471e-103">Günlük veya aylık Gren için rezervasyon özetlerini alın.</span><span class="sxs-lookup"><span data-stu-id="2471e-103">Get reservation summaries for daily or monthly grain.</span></span>

## <span data-ttu-id="2471e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2471e-104">SYNTAX</span></span>

```
Get-AzConsumptionReservationSummary -Grain <String> -ReservationOrderId <String> [-ReservationId <String>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2471e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2471e-105">DESCRIPTION</span></span>
<span data-ttu-id="2471e-106">**Get-Azsarf Mptionrezervationsummary** cmdlet 'i günlük veya aylık grelük özetlerini alır.</span><span class="sxs-lookup"><span data-stu-id="2471e-106">The **Get-AzConsumptionReservationSummary** cmdlet gets reservation summaries for daily or monthly grain.</span></span>

## <span data-ttu-id="2471e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2471e-107">EXAMPLES</span></span>

### <span data-ttu-id="2471e-108">Örnek 1: aylık grenin RESERVATION Order ID ile rezervasyon özetlerini alma</span><span class="sxs-lookup"><span data-stu-id="2471e-108">Example 1: Get reservation summaries with reservation order Id for monthly grain</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationSummary -Grain monthly -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b
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

### <span data-ttu-id="2471e-109">Örnek 2: bir aylık grenin rezervasyonu</span><span class="sxs-lookup"><span data-stu-id="2471e-109">Example 2: Get reservation summaries with reservation order Id and reservation Id for monthly grain</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationSummary -Grain monthly -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -ReservationId f37f4b70-52ba-4344-a8bd-28abfd21d640
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

### <span data-ttu-id="2471e-110">Örnek 3: günlük noktalı, rezervasyon sipariş kimliği</span><span class="sxs-lookup"><span data-stu-id="2471e-110">Example 3: Get reservation summaries with reservation order Id for daily grain provided date range</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationSummary -Grain daily -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -StartDate 2017-10-01 -EndDate 2017-12-07
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

### <span data-ttu-id="2471e-111">Örnek 4: rezervasyon düzeni kimliği ve rezervasyon kimliği</span><span class="sxs-lookup"><span data-stu-id="2471e-111">Example 4: Get reservation summaries with reservation order Id and reservation Id for daily grain provided date range</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationSummary -Grain daily -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -ReservationId f37f4b70-52ba-4344-a8bd-28abfd21d640 -StartDate 2017-10-01 -EndDate 2017-12-07
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

## <span data-ttu-id="2471e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2471e-112">PARAMETERS</span></span>

### <span data-ttu-id="2471e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2471e-113">-DefaultProfile</span></span>
<span data-ttu-id="2471e-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2471e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2471e-115">-EndDate</span><span class="sxs-lookup"><span data-stu-id="2471e-115">-EndDate</span></span>
<span data-ttu-id="2471e-116">Rezervasyon özetinin son verileri (YYYY-AA-DD); yalnızca günlük greiçin gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2471e-116">The end data (YYYY-MM-DD in UTC) of the reservation summary, required only for daily grain.</span></span>

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

### <span data-ttu-id="2471e-117">Noktalı</span><span class="sxs-lookup"><span data-stu-id="2471e-117">-Grain</span></span>
<span data-ttu-id="2471e-118">Ayırma özetinin zaman çizgisi, günlük veya aylık olabilir.</span><span class="sxs-lookup"><span data-stu-id="2471e-118">The time grain of the reservation summary, can be daily or monthly.</span></span>

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

### <span data-ttu-id="2471e-119">-Rezervationıd</span><span class="sxs-lookup"><span data-stu-id="2471e-119">-ReservationId</span></span>
<span data-ttu-id="2471e-120">Rezervasyon sırasındaki rezervasyonun tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="2471e-120">The identifier of a reservation within a reservation order.</span></span>

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

### <span data-ttu-id="2471e-121">-Rezervationorderıd</span><span class="sxs-lookup"><span data-stu-id="2471e-121">-ReservationOrderId</span></span>
<span data-ttu-id="2471e-122">Bir rezervasyon satınalmanın tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="2471e-122">The identifier of a reservation purchase.</span></span>

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

### <span data-ttu-id="2471e-123">-StartDate</span><span class="sxs-lookup"><span data-stu-id="2471e-123">-StartDate</span></span>
<span data-ttu-id="2471e-124">Rezervasyon özetinin başlangıç verileri (YYYY-AA-DD); yalnızca günlük greiçin gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2471e-124">The start data (YYYY-MM-DD in UTC) of the reservation summary, required only for daily grain.</span></span>

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

### <span data-ttu-id="2471e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2471e-125">CommonParameters</span></span>
<span data-ttu-id="2471e-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2471e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2471e-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2471e-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2471e-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2471e-128">INPUTS</span></span>

### <span data-ttu-id="2471e-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2471e-129">None</span></span>

## <span data-ttu-id="2471e-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2471e-130">OUTPUTS</span></span>

### <span data-ttu-id="2471e-131">Microsoft. Azure. Commands. tüketim. modeller. Psrezervationsummary</span><span class="sxs-lookup"><span data-stu-id="2471e-131">Microsoft.Azure.Commands.Consumption.Models.PSReservationSummary</span></span>

## <span data-ttu-id="2471e-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2471e-132">NOTES</span></span>

## <span data-ttu-id="2471e-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2471e-133">RELATED LINKS</span></span>
