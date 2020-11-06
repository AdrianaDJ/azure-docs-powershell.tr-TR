---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: afef81ad904ccd5bf53f0b2a09bb10511e71fca1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594194"
---
# <span data-ttu-id="440b6-101">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="440b6-101">Get-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="440b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="440b6-102">SYNOPSIS</span></span>
<span data-ttu-id="440b6-103">Belirtilen ASR işinin ayrıntılarını veya kurtarma hizmetleri kasasındaki en son ASR işlerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="440b6-103">Gets the details of the specified ASR job or the list of recent ASR jobs in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="440b6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="440b6-104">SYNTAX</span></span>

### <span data-ttu-id="440b6-105">ByParam (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="440b6-105">ByParam (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [<CommonParameters>]
```

### <span data-ttu-id="440b6-106">ByName</span><span class="sxs-lookup"><span data-stu-id="440b6-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrJob -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="440b6-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="440b6-107">ByObject</span></span>
```
Get-AzureRmRecoveryServicesAsrJob -Job <ASRJob> [<CommonParameters>]
```

## <span data-ttu-id="440b6-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="440b6-108">DESCRIPTION</span></span>
<span data-ttu-id="440b6-109">**Get-AzureRmRecoveryServicesAsrJob** cmdlet 'ı Azure Site Recovery işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="440b6-109">The **Get-AzureRmRecoveryServicesAsrJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="440b6-110">Kurtarma Hizmetleri kasasındaki ASR işlerini görüntülemek için bu cmdlet 'i kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="440b6-110">You can use this cmdlet to view the ASR jobs in the Recovery Services vault.</span></span>

## <span data-ttu-id="440b6-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="440b6-111">EXAMPLES</span></span>

### <span data-ttu-id="440b6-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="440b6-112">Example 1</span></span>
```
PS C:\> $jobs = Get-AzureRmRecoveryServicesAsrJob -TargetObjectId $ASRObjectId
```

<span data-ttu-id="440b6-113">Belirli bir ASR nesnesindeki tüm işleri döndürür (çoğaltılmış öğe veya kurtarma planı gibi ASR nesnesini KIMLIĞIYLE başvuru.)</span><span class="sxs-lookup"><span data-stu-id="440b6-113">Returns all the jobs on a particular ASR object(reference the ASR object such as replicated item or recovery plan by its ID.)</span></span> 

## <span data-ttu-id="440b6-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="440b6-114">PARAMETERS</span></span>

### <span data-ttu-id="440b6-115">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="440b6-115">-EndTime</span></span>
<span data-ttu-id="440b6-116">İşlerin bitiş zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="440b6-116">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="440b6-117">Bu cmdlet belirtilen süreden önce başlatılan tüm işleri alır.</span><span class="sxs-lookup"><span data-stu-id="440b6-117">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="440b6-118">Bu parametre için bir **DateTime** nesnesi almak istiyorsanız Get-Date cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="440b6-118">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="440b6-119">Daha fazla bilgi için yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="440b6-119">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="440b6-120">-Job</span><span class="sxs-lookup"><span data-stu-id="440b6-120">-Job</span></span>
<span data-ttu-id="440b6-121">Güncelleştirme ayrıntılarının alınacağı ASR iş nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="440b6-121">Specifies the ASR job object to get updated details for.</span></span>

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="440b6-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="440b6-122">-Name</span></span>
<span data-ttu-id="440b6-123">ASR işini ada göre belirtin.</span><span class="sxs-lookup"><span data-stu-id="440b6-123">Specify the ASR job by name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="440b6-124">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="440b6-124">-StartTime</span></span>
<span data-ttu-id="440b6-125">İşlerin başlangıç zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="440b6-125">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="440b6-126">Bu cmdlet belirtilen süreden sonra başlatılan tüm işleri alır.</span><span class="sxs-lookup"><span data-stu-id="440b6-126">This cmdlet gets all jobs that started after the specified time.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="440b6-127">Durumlu</span><span class="sxs-lookup"><span data-stu-id="440b6-127">-State</span></span>
<span data-ttu-id="440b6-128">ASR işinin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="440b6-128">Specifies the state for a ASR job.</span></span>
<span data-ttu-id="440b6-129">Bu cmdlet belirtilen durumla eşleşen tüm işleri alır.</span><span class="sxs-lookup"><span data-stu-id="440b6-129">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="440b6-130">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="440b6-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="440b6-131">NotStarted</span><span class="sxs-lookup"><span data-stu-id="440b6-131">NotStarted</span></span>
- <span data-ttu-id="440b6-132">Progress</span><span class="sxs-lookup"><span data-stu-id="440b6-132">InProgress</span></span>
- <span data-ttu-id="440b6-133">Oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="440b6-133">Succeeded</span></span>
- <span data-ttu-id="440b6-134">Diğerini</span><span class="sxs-lookup"><span data-stu-id="440b6-134">Other</span></span>
- <span data-ttu-id="440b6-135">Erişilemedi</span><span class="sxs-lookup"><span data-stu-id="440b6-135">Failed</span></span>
- <span data-ttu-id="440b6-136">İptal</span><span class="sxs-lookup"><span data-stu-id="440b6-136">Cancelled</span></span>
- <span data-ttu-id="440b6-137">Etsin</span><span class="sxs-lookup"><span data-stu-id="440b6-137">Suspended</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 
Accepted values: NotStarted, InProgress, Succeeded, Other, Failed, Cancelled, Suspended

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="440b6-138">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="440b6-138">-TargetObjectId</span></span>
<span data-ttu-id="440b6-139">Nesnenin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="440b6-139">Specifies the ID of the object.</span></span> <span data-ttu-id="440b6-140">Belirtilen nesnedeki işleri aramak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="440b6-140">Used to search for jobs on the specified object.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="440b6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="440b6-141">CommonParameters</span></span>
<span data-ttu-id="440b6-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="440b6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="440b6-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="440b6-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="440b6-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="440b6-144">INPUTS</span></span>

### <span data-ttu-id="440b6-145">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="440b6-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="440b6-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="440b6-146">OUTPUTS</span></span>

### <span data-ttu-id="440b6-147">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. Sıterecovery. ASRJob, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="440b6-147">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="440b6-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="440b6-148">NOTES</span></span>

## <span data-ttu-id="440b6-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="440b6-149">RELATED LINKS</span></span>

[<span data-ttu-id="440b6-150">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="440b6-150">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="440b6-151">Özgeçmiş-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="440b6-151">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="440b6-152">Stop-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="440b6-152">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
