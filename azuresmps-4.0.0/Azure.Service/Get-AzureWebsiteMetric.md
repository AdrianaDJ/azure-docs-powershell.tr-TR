---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 717023DA-AA2D-4F1B-AE46-67ED75AA0D15
online version: ''
schema: 2.0.0
ms.openlocfilehash: b6d8dae704946680dd72ff8227d2a88d55f8b77a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106271"
---
# <span data-ttu-id="16933-101">Get-AzureWebsiteMetric</span><span class="sxs-lookup"><span data-stu-id="16933-101">Get-AzureWebsiteMetric</span></span>

## <span data-ttu-id="16933-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16933-102">SYNOPSIS</span></span>
<span data-ttu-id="16933-103">Geçerli abonelikteki Azure Web sitesi için ölçümleri alır.</span><span class="sxs-lookup"><span data-stu-id="16933-103">Gets metrics for the Azure website in the current subscription.</span></span>

## <span data-ttu-id="16933-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="16933-104">SYNTAX</span></span>

```
Get-AzureWebsiteMetric [-MetricNames <String[]>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-TimeGrain <String>] [-InstanceDetails] [-SlotView] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="16933-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="16933-105">DESCRIPTION</span></span>
<span data-ttu-id="16933-106">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="16933-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="16933-107">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="16933-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="16933-108">**Get-AzureWebsiteMetric** cmdlet 'i geçerli abonelikteki Azure Web sitesi için ölçümleri alır.</span><span class="sxs-lookup"><span data-stu-id="16933-108">The **Get-AzureWebsiteMetric** cmdlet gets metrics for the Azure website in the current subscription.</span></span>

## <span data-ttu-id="16933-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="16933-109">EXAMPLES</span></span>

### <span data-ttu-id="16933-110">Örnek 1: Web sitesi için örnek temelinde son üç saat için ölçümleri alma</span><span class="sxs-lookup"><span data-stu-id="16933-110">Example 1: Get metrics for the last three hours on a per-instance level for a website</span></span>
```
PS C:\> Get-AzureWebsiteMetric -Name "ContosoWebSite" -StartDate (get-date).AddHours(-3) -MetricNames "Requests" -InstanceDetails -SlotView -TimeGrain "PT1M" 
PS C:\> $metrics[1].Data Name : Requests 

Unit : Count 

StartTime : 8/11/2014 7:05:00 AM 

EndTime : 8/11/2014 5:06:01 PM 

TimeGrain : PT1M 
PrimaryAggregationType : Instance 
Values : {Time:8/11/2014 7:05:00 AM, Total:4, Min:, Max:, Time:8/11/2014 7:06:00 AM, Total:3, Min:, Max:, 
Time:8/11/2014 7:07:00 AM, Total:3, Min:, Max:, Time:8/11/2014 7:08:00 AM, Total:12, Min:, Max:...} 
$metrics[1].Data.Values | ft 
TimeCreated Total Minimum Maximum Count InstanceName 
----------- ----- ------- ------- ----- ------------ 
8/11/2014 7:05:00 AM 4 1 RD00155DC24599 
8/11/2014 7:06:00 AM 3 1 RD00155DC24599 
8/11/2014 7:07:00 AM 3 1 RD00155DC24589 
8/11/2014 7:08:00 AM 12 1 RD00155DC24599
8/11/2014 7:09:00 AM 37 1 RD00155DC24599 
8/11/2014 7:10:00 AM 9 1 RD00155DC24599
```

<span data-ttu-id="16933-111">Bu komut, Web sitesi için en son üç saatlik ölçümleri alır.</span><span class="sxs-lookup"><span data-stu-id="16933-111">This command gets metrics for the last three hours on a per-instance level for a website.</span></span>

## <span data-ttu-id="16933-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="16933-112">PARAMETERS</span></span>

### <span data-ttu-id="16933-113">-EndDate</span><span class="sxs-lookup"><span data-stu-id="16933-113">-EndDate</span></span>
<span data-ttu-id="16933-114">Ölçümleri almayı durdurmak için **Tarih saat**</span><span class="sxs-lookup"><span data-stu-id="16933-114">Specifies the time, as a **DateTime** object, to stop getting metrics.</span></span>
<span data-ttu-id="16933-115">**TarihSaat** nesnesi almak için **Get-Date** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="16933-115">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="16933-116">Daha fazla bilgi için yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="16933-116">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16933-117">-Instancedetails</span><span class="sxs-lookup"><span data-stu-id="16933-117">-InstanceDetails</span></span>
<span data-ttu-id="16933-118">Bu cmdlet 'in ayrıntıları örnek başına olarak içerdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="16933-118">Indicates that this cmdlet includes details on a per-instance level.</span></span>
<span data-ttu-id="16933-119">Web barındırma planı iki veya daha çok bilgisayarda çalışıyorsa, bu cmdlet her bilgisayar için ölçümleri döndürür.</span><span class="sxs-lookup"><span data-stu-id="16933-119">If the web hosting plan runs on two or more computers, this cmdlet returns metrics for each computer.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16933-120">-Metrik adları</span><span class="sxs-lookup"><span data-stu-id="16933-120">-MetricNames</span></span>
<span data-ttu-id="16933-121">Alınacak ölçümler dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="16933-121">Specifies an array of metrics to get.</span></span>
<span data-ttu-id="16933-122">Bu parametreyi belirtmezseniz, cmdlet tüm ölçümleri alır.</span><span class="sxs-lookup"><span data-stu-id="16933-122">If you do not specify this parameter, the cmdlet gets all metrics.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16933-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="16933-123">-Name</span></span>
<span data-ttu-id="16933-124">Abonelikteki bir Web sitesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="16933-124">Specifies the name of a website in the subscription.</span></span>
<span data-ttu-id="16933-125">Bu parametre joker karakterleri desteklemez.</span><span class="sxs-lookup"><span data-stu-id="16933-125">This parameter does not support wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16933-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="16933-126">-Profile</span></span>
<span data-ttu-id="16933-127">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="16933-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="16933-128">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="16933-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16933-129">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="16933-129">-Slot</span></span>
<span data-ttu-id="16933-130">Bulut hizmeti dağıtımının ortamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="16933-130">Specifies the environment of a cloud service deployment.</span></span>
<span data-ttu-id="16933-131">Geçerli değerler: üretim ve hazırlama.</span><span class="sxs-lookup"><span data-stu-id="16933-131">Valid values are: Production and Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16933-132">-SlotView</span><span class="sxs-lookup"><span data-stu-id="16933-132">-SlotView</span></span>
<span data-ttu-id="16933-133">Bu cmdlet 'in geçerli yuvada trafiği alan ana bilgisayar adları için ölçümleri aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="16933-133">Indicates that this cmdlet gets metrics for the host names that receive traffic at the current slot.</span></span>
<span data-ttu-id="16933-134">Zaman aralığında bir değiştirme gerçekleşirse, ölçümler birleştirilir.</span><span class="sxs-lookup"><span data-stu-id="16933-134">If a swap occurs during the time period, the metrics are merged.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16933-135">-StartDate</span><span class="sxs-lookup"><span data-stu-id="16933-135">-StartDate</span></span>
<span data-ttu-id="16933-136">Ölçümleri almayı başlatmak için saati bir **DateTime** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="16933-136">Specifies the time, as a **DateTime** object, to start getting metrics.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16933-137">-Zaman çizgisi</span><span class="sxs-lookup"><span data-stu-id="16933-137">-TimeGrain</span></span>
<span data-ttu-id="16933-138">Ölçümler için zaman birimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="16933-138">Specifies the time unit for metrics.</span></span>
<span data-ttu-id="16933-139">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="16933-139">Valid values are:</span></span> 

- <span data-ttu-id="16933-140">PT1M (dakika)</span><span class="sxs-lookup"><span data-stu-id="16933-140">PT1M (Minute)</span></span> 
- <span data-ttu-id="16933-141">PT1H (saat)</span><span class="sxs-lookup"><span data-stu-id="16933-141">PT1H (Hour)</span></span> 
- <span data-ttu-id="16933-142">P1D (gün)</span><span class="sxs-lookup"><span data-stu-id="16933-142">P1D (Day)</span></span>

<span data-ttu-id="16933-143">Varsayılan değer PT1H ' dır.</span><span class="sxs-lookup"><span data-stu-id="16933-143">The default value is PT1H.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16933-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16933-144">CommonParameters</span></span>
<span data-ttu-id="16933-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="16933-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16933-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16933-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16933-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="16933-147">INPUTS</span></span>

###  
<span data-ttu-id="16933-148">Bu cmdlet 'e girişi, değer olarak değil, özellik adıyla geçirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="16933-148">You can pass input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="16933-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="16933-149">OUTPUTS</span></span>

### <span data-ttu-id="16933-150">Microsoft. Windowsazve. Commands. Utilities. WebEntities. Services. WebEntities. MetricResponse</span><span class="sxs-lookup"><span data-stu-id="16933-150">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.MetricResponse</span></span>
<span data-ttu-id="16933-151">**Get-AzureWebsiteMetric** varsayılan olarak **metricresponse** nesnelerinin dizisini döndürür.</span><span class="sxs-lookup"><span data-stu-id="16933-151">By default, **Get-AzureWebsiteMetric** returns an array of **MetricResponse** objects.</span></span>

## <span data-ttu-id="16933-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="16933-152">NOTES</span></span>

## <span data-ttu-id="16933-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="16933-153">RELATED LINKS</span></span>

[<span data-ttu-id="16933-154">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="16933-154">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)


